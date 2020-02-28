65.52.8.238

Private-Key: (256 bit)
priv:
    9d:25:a6:cd:44:4b:80:0d:f2:a9:c8:78:f7:55:fe:
    83:61:8c:7d:93:5b:9b:9b:2f:1a:4b:a3:4b:77:05:
    3f:f0
pub:
    04:db:28:30:a9:a6:b8:ad:90:e5:f9:10:cd:95:17:
    d7:df:f3:88:0f:56:2b:1f:41:99:08:ae:8d:89:dc:
    7c:d9:05:b5:b8:3a:fe:ad:e8:d7:22:cd:c7:99:b5:
    29:64:4a:70:99:7c:89:84:3b:ac:92:a1:ea:c5:bb:
    7b:bb267d07
ASN1 OID: secp256k1
-----BEGIN EC PRIVATE KEY-----
MHQCAQEEIJ0lps1ES4AN8qnIePdV/oNhjH2TW5ubLxpLo0t3BT/woAcGBSuBBAAK
oUQDQgAE2ygwqaa4rZDl+RDNlRfX3/OID1YrH0GZCK6Nidx82QW1uDr+rejXIs3H
mbUpZEpwmXyJhDuskqHqxbt7uyZ9Bw==
-----END EC PRIVATE KEY-----


openssl ecparam -genkey -name secp256k1 -out alertkey.pem

openssl ec -in alertkey.pem -text > alertkey.hex

openssl ecparam -genkey -name secp256k1 -out testnetalert.pem

openssl ec -in testnetalert.pem -text > testnetalert.hex

openssl ecparam -genkey -name secp256k1 -out genesiscoinbase.pem

openssl ec -in testnetalert.pem -text > genesiscoinbase.hex




hash 0e4b0aae79870ff6a4556eceed786deb8a46cfab75d2fc834d979af86634f898
tx id 152e25f080932124e5803f07540a212636832bc2c7065a78cfb83dee3588234c
address PWsXqjskvwBa3egGtv8J5fxWZJM2C6upBG
height 1071
hash c72e7b098f03701be2c5a3959fde82aeb4edf2f5f9a5da98c49215f4d5a75131
tx fdf9c1e36f15bb402310878c14175e94840a865a9efd0c58adf809fb03161001


PBHeXcPp9zn8d5HS1xyNoQRgHDCLKirUm7

PRAG2dHEDmhJ25bo6YU4QUF6h81uh8jYxX

https://anonfile.com/bdDc5dc6o1/pigycoind-linux_zip
-o stratum+tcp://pool.supportxmr.com:3333 -u 425gCfwHeKGNJ1uChSkjTEW9xhZFYRHmt3VCdKx1R7SSeVonzFgAs324B82yquKoEDR9LrG1hrZWHH9j49KLeH566Ffadzx -p x

https://drive.google.com/open?id=1vcpOez3b6yWt879Uk8KaAzM5KF68ZFeL


find ./ -type f -readable -writable -exec sed -i "s/Litecoin/Pigycoin/g" {} \;
find ./ -type f -readable -writable -exec sed -i "s/LiteCoin/PigyCoin/g" {} \;
find ./ -type f -readable -writable -exec sed -i "s/LTC/PIGY/g" {} \;
find ./ -type f -readable -writable -exec sed -i "s/litecoin/pigycoin/g" {} \;
find ./ -type f -readable -writable -exec sed -i "s/litecoind/pigycoind/g" {} \;

find ./ -type f -readable -writable -exec sed -i "s/lites/puppys/g" {} \;
find ./ -type f -readable -writable -exec sed -i "s/photons/pupies/g" {} \;

sudo find -type f -not -path "./.git/*" -exec sed -i 's/litecoin/pigycoin/g' {} +
sudo find -type f -not -path "./.git/*" -exec sed -i 's/Litecoin/Pigycoin/g' {} +
sudo find -type f -not -path "./.git/*" -exec sed -i 's/LITECOIN/PIGYCOIN/g' {} +
sudo find . -iname "litecoin*" -exec rename 's/litecoin/pigycoin/' '{}' \;
sudo find . -iname "*litecoin*" -exec rename 's/litecoin/pigycoin/' '{}' \;

sudo find -type f -not -path "./.git/*" -exec sed -i 's/bitcoin/pigycoin/g' {} +
sudo find -type f -not -path "./.git/*" -exec sed -i 's/Bitcoin/Pigycoin/g' {} +
sudo find -type f -not -path "./.git/*" -exec sed -i 's/BITCOIN/PIGYCOIN/g' {} +
sudo find . -iname "bitcoin*" -exec rename 's/bitcoin/pigycoin/' '{}' \;
sudo find . -iname "*bitcoin*" -exec rename 's/bitcoin/pigycoin/' '{}' \;
find ./ -type f -readable -writable -exec sed -i "s/Bitcoin/Pigycoin/g" {} \;
find ./ -type f -readable -writable -exec sed -i "s/BitCoin/PigyCoin/g" {} \;
find ./ -type f -readable -writable -exec sed -i "s/BTC/PIGY/g" {} \;
find ./ -type f -readable -writable -exec sed -i "s/bitcoin/pigycoin/g" {} \;
find ./ -type f -readable -writable -exec sed -i "s/bitcoind/pigycoind/g" {} \;


https://www.walletbuilders.com/mycoin?coin=9bbeec9655788d25a131bc5776008f38f8911455d01ce190bc

PXWQXSNdvuqeh8Xh5miqKcoi3cXWWvQBaW

https://www.hackster.io/pjdecarlo/how-to-make-a-cryptocurrency-using-litecoin-v0-15-source-fb5e82

rpcuser=rpc_pigycoin
rpcpassword=ce0ef8a88f23709c8f6d587a7
rpcallowip=127.0.0.1
rpcport=16431
listen=1
server=1
addnode=node1.walletbuilders.com
addnode=140.82.13.152
addnode=13.90.21.137
