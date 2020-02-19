https://pastebin.com/ZEiPWTiY

04a9eb897c655dd0db15c0f6a30805373fa70ebb36ce17c7280163c5fa03e2d648d9ea68938dfeb352635b4dd3730c48e9dd554c8a17e8b53769759b5fe90f0444

Private-Key: (256 bit)
priv:
    f302579990e0597dc3f3ede15c524432515a9d8ffac019b125f78a735f3127be


pub:
    04790f9122a6f5ac6ae7d322c88e24
    dbd5538dd3c3c28bc3c9a6e552669c
    9e1a1c25652a2c999a93c29a6704fe
    5059963a706a2a051b79de39334c7f
    20767627a0
ASN1 OID: secp256k1
-----BEGIN EC PRIVATE KEY-----
MHQCAQEEIPMCV5mQ4Fl9w/Pt4VxSRDJRWp2P+sAZsSX3inNfMSe+oAcGBSuBBAAK
oUQDQgAEeQ+RIqb1rGrn0yLIjiTb1VON08PCi8PJpuVSZpyeGhwlZSosmZqTwppn
BP5QWZY6cGoqBRt53jkzTH8gdnYnoA==
-----END EC PRIVATE KEY-----





root@server:~/Documents# cat testnetalert.hex
Private-Key: (256 bit)
priv:
    13:55:c6:b8:f9:60:85:f6:7f:f0:00:1d:55:ae:bb:
    b8:b8:6b:b6:99:f6:88:08:36:f7:57:5f:7e:1b:e8:
    77:ef
pub:

    04a9eb897c655dd0db15c0f6a30805
    373fa70ebb36ce17c7280163c5fa03
    e2d648d9ea68938dfeb352635b4dd3
    730c48e9dd554c8a17e8b53769759b
    5fe90f0444
ASN1 OID: secp256k1
-----BEGIN EC PRIVATE KEY-----
MHQCAQEEIBNVxrj5YIX2f/AAHVWuu7i4a7aZ9ogINvdXX34b6HfvoAcGBSuBBAAK
oUQDQgAEqeuJfGVd0NsVwPajCAU3P6cOuzbOF8coAWPF+gPi1kjZ6miTjf6zUmNb
TdNzDEjp3VVMihfotTdpdZtf6Q8ERA==
-----END EC PRIVATE KEY-----


04a9eb897c655dd0db15c0f6a30805373fa70ebb36ce17c7280163c5fa03e2d648d9ea68938dfeb352635b4dd3730c48e9dd554c8a17e8b53769759b5fe90f0444


root@server:~/Documents# cat genesiscoinbase.hex
Private-Key: (256 bit)
priv:
    13:55:c6:b8:f9:60:85:f6:7f:f0:00:1d:55:ae:bb:
    b8:b8:6b:b6:99:f6:88:08:36:f7:57:5f:7e:1b:e8:
    77:ef
pub:
    04a9eb897c655dd0db15c0f6a30805
    373fa70ebb36ce17c7280163c5fa03
    e2d648d9ea68938dfeb352635b4dd3
    730c48e9dd554c8a17e8b53769759b
    5fe90f0444
ASN1 OID: secp256k1
-----BEGIN EC PRIVATE KEY-----
MHQCAQEEIBNVxrj5YIX2f/AAHVWuu7i4a7aZ9ogINvdXX34b6HfvoAcGBSuBBAAK
oUQDQgAEqeuJfGVd0NsVwPajCAU3P6cOuzbOF8coAWPF+gPi1kjZ6miTjf6zUmNb
TdNzDEjp3VVMihfotTdpdZtf6Q8ERA==
-----END EC PRIVATE KEY-----



-----

if (false && block.GetHash() != hashGenesisBlock)
        {
            printf("Searching for genesis block...\n");
            // This will figure out a valid hash and Nonce if you're
            // creating a different genesis block:
            uint256 hashTarget = CBigNum().SetCompact(block.nBits).getuint256();
            uint256 thash;
            char scratchpad[SCRYPT_SCRATCHPAD_SIZE];

            loop
            {
#if defined(USE_SSE2)
                // Detection would work, but in cases where we KNOW it always has SSE2,
                // it is faster to use directly than to use a function pointer or conditional.
#if defined(_M_X64) || defined(__x86_64__) || defined(_M_AMD64) || (defined(MAC_OSX) && defined(__i386__))
                // Always SSE2: x86_64 or Intel MacOS X
                scrypt_1024_1_1_256_sp_sse2(BEGIN(block.nVersion), BEGIN(thash), scratchpad);
#else
                // Detect SSE2: 32bit x86 Linux or Windows
                scrypt_1024_1_1_256_sp(BEGIN(block.nVersion), BEGIN(thash), scratchpad);
#endif
#else
                // Generic scrypt
                scrypt_1024_1_1_256_sp_generic(BEGIN(block.nVersion), BEGIN(thash), scratchpad);
#endif
                if (thash <= hashTarget)
                    break;
                if ((block.nNonce & 0xFFF) == 0)
                {
                    printf("nonce %08X: hash = %s (target = %s)\n", block.nNonce, thash.ToString().c_str(), hashTarget.ToString().c_str());
                }
                ++block.nNonce;
                if (block.nNonce == 0)
                {
                    printf("NONCE WRAPPED, incrementing time\n");
                    ++block.nTime;
                }
            }
            printf("block.nTime = %u \n", block.nTime);
            printf("block.nNonce = %u \n", block.nNonce);
            printf("block.GetHash = %s\n", block.GetHash().ToString().c_str());
        }
