##YXlite (YXC) - 

=======================================================================    
##Installation Linux (Ubuntu, Debian)

$ sudo apt-get install   
$ sudo apt-get install build-essential libboost-all-dev libcurl4-openssl-dev libdb5.1-dev libdb5.1++-dev git qt-sdk libminiupnpc-dev

Libraries & dependencies:   
libboost-all-dev - Boost C++ Libraries dev   
libcurl4-openssl-dev - libcurl (OpenSSL flavour)   
libdb5.1-dev - Berkeley v5.1 Database Libraries   
libdb5.1++-dev - Berkeley v5.1 Database Libraries runtime   
git - git version control system   
qt-sdk - QT-SDK platform  https://qt-project.org/    
libminiupnpc-dev - UPnP IGD client lightweight library dev   

s sudo dd if=/dev/zero of=/swapfile bs=64M count=16    
$ sudo mkswap /swapfile   
$ sudo swapon /swapfile   
  
 $ sudo apt-get install git    
 $ cd /usr/local/src    
 $ git clone https://github.com/erikYX/yxlite.git    
 $ cd yxlite/src    
 yxlite/src$ make -f makefile.unix    
 yxlite/src$ strip yxlite    
 yxlite/src$ cp -r yxlite /usr/local/bin/yxlite    
    
 $ yxlite &    
 to  start yxlite server daemon     
    
It will prompt to xreate configuration file:    
   
yxlite/src$ cd /home/USER/.yxlite       
/home/USER/.yxlite$ nano yxlite.conf  

Enter following: 
rpcuser=yxliterpc   
rpcpassword=Av6VRZUMruN7cn6dEHAGvGokAYTpKAwxtBrP7BmQPKbu   
   
server=1   
listen=1   
daemon=1   
rpcallowip=localhost   
   
addnode=104.236.7.110   
addnode=107.170.254.130    


 Commands:   
 $ yxlite & - start yxlite server daemon   
 $ yxlite getinfo - basic info JSON array   
 $ yxlite excryptwallet <passphrase>   
 $ yxlite listtransactions - show transactions to wallet   
 $ yxlite setgenerate true 1 - start mining   
 $ yxlite getmininginfo - mining status   
 $ yxlited setgenerate false - stop mining   
 $ yxlite stop - stop server daemon   
 
 $ sudo tail -f /home/USER/.yxlite/debug.log - watch yxlite network activity   
 
  
  
Ports:   
RPC	  Main 17985, Testnet 27985
p2p	  Main 17986, Testnet 27986
 
   
Coin data:    
Coins per block = 23   
Block Interval = 300   // 5 minutes   
Difficulty reset  =  1 * 24 * 60 * 60 // once/day     
Max Money = 1000000 // 1 million total coins   
Estimated coins per day = 6624 // 24 * 60 / 5 = 288 blocks * 23 YXC per block   

Pubkey Address prefix = 77  // starts with Y or X  

Images and icons in  /src/qt/res/     

Genesis Block:    
block.nTime = 1424404186   
block.nNonce = 2086780778    
block.GetHash = 9a3149370ea97c017b3d8853abadd614c28d59a96084efb3f97c25178cd943a1   
CBlock(hash=9a3149370ea97c017b3d, PoW=00000c1a342387447aea, ver=1, hashPrevBlock=00000000000000000000,    hashMerkleRoot=f9669a1832, nTime=1424404186, nBits=1e0ffff0, nNonce=2086780778, vtx=1)    
  CTransaction(hash=f9669a1832, ver=1, vin.size=1, vout.size=1, nLockTime=0)   
    CTxIn(COutPoint(0000000000, -1), coinbase    04ffff001d010446322e31392e323031352d56616e696c6c61204963652072656c6561736564206166746572206265696e67206368617267656420696e20466c6f7269646120627572676c617279)   
    CTxOut(error)   
  vMerkleTree: f9669a1832   
  
  
    
diff - https://github.com/bfroemel/yxlite/commit/947a0fafd8d033f6f0960c4ff0748f76a3d58326   




