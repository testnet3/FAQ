### Raptoreum cli FAQ


#### abandontransaction

Mark in-wallet transaction  as abandoned

```raptoreum-cli abandontransaction "123456789012345678901234567890123456789012345678901234567890000"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "abandontransaction", "params": ["123456789012345678901234567890123456789012345678901234567890000"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "abandontransaction", "params": ["123456789012345678901234567890123456789012345678901234567890000"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### abortrescan

Stops current wallet rescan triggered by an RPC call, e.g. by an importprivkey call.

Import a private key

```raptoreum-cli importprivkey "12345678901234567890123456789000"```

Abort the running wallet rescan

```raptoreum-cli abortrescan```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "abortrescan", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "abortrescan", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### backupwallet

Safely copies current wallet file to destination, which can be a directory or a path with filename.

```raptoreum-cli backupwallet "backup.dat"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "backupwallet", "params": ["backup.dat"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "backupwallet", "params": ["backup.dat"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### createwallet

Creates and loads a new wallet.

```raptoreum-cli createwallet "mywallet"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "createwallet", "params": ["mywallet"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "createwallet", "params": ["mywallet"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### createrawtransaction **testnet only** 

Create a transaction spending the given inputs and creating new outputs.
Outputs can be addresses or data.
Returns hex-encoded raw transaction.

```raptoreum-cli createrawtransaction "[{\"txid\":\"myid\",\"vout\":0}]" "[{\"address\":0.01}]"```

```raptoreum-cli createrawtransaction "[{\"txid\":\"myid\",\"vout\":0}]" "[{\"data\":\"00010203\"}]"```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "createrawtransaction", "params": ["[{\"txid\":\"myid\",\"vout\":0}]", "[{\"address\":0.01}]"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "createrawtransaction", "params": ["[{\"txid\":\"myid\",\"vout\":0}]", "[{\"data\":\"00010203\"}]"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```



#### dumpprivkey

Reveals private key corresponding to **myaddress**.

```raptoreum-cli  dumpprivkey "myaddress"```

```raptoreum-cli importprivkey "mykey"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "dumpprivkey", "params": ["myaddress"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "dumpprivkey", "params": ["myaddress"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### dumpwallet

Dumps all wallet keys in a human-readable format to a file. 

```raptoreum-cli dumpwallet "mykey"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "dumpwallet", "params": ["mykey"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "dumpwallet", "params": ["mykey"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### encryptwallet

Encrypt your wallet

```raptoreum-cli  encryptwallet "my pass phrase"```

Now set the passphrase to use wallet, such as for signing or sending raptoreum

```raptoreum-cli walletpassphrase "my pass phrase"```

Now lock the wallet again by removing the passphrase

```raptoreum-cli walletlock```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "encryptwallet", "params": ["my pass phrase"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "encryptwallet", "params": ["my pass phrase"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### getaddressesbylabel

Returns the list of addresses assigned specified label.

```raptoreum-cli getaddressesbylabel "main"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressesbylabel", "params": ["main"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressesbylabel", "params": ["main"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### getaddressinfo

Return information about given raptoreum address. 

```raptoreum-cli getaddressinfo "RTM123456789012345678901234567890"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressinfo", "params": ["RTM123456789012345678901234567890"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressinfo", "params": ["RTM123456789012345678901234567890"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### getnewaddress

Returns a new Raptoreum address for receiving payments.

```raptoreum-cli getnewaddress```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getnewaddress", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet 
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getnewaddress", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### getreceivedbyaddress

Returns total amount received by given address in transactions.

Amount from transactions with at least 1 confirmation

```raptoreum-cli  getreceivedbyaddress "RTM123456789012345678901234567890" 1```

Amount including unconfirmed transactions, zero confirmations

```raptoreum-cli  getreceivedbyaddress "RTM123456789012345678901234567890" 0```

Amount from transactions with at least 100 confirmation

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getreceivedbyaddress", "params": ["RTM123456789012345678901234567890", 100] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getreceivedbyaddress", "params": ["RTM123456789012345678901234567890", 100] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### getreceivedbylabel

Returns total amount received by addresses.

Amount received by default label with at least 1 confirmation

```raptoreum-cli getreceivedbylabel ""```

Amount received at the **main** label including unconfirmed amounts with zero confirmations

```raptoreum-cli getreceivedbylabel "main" 0```

Amount with at least 9 confirmations

```raptoreum-cli getreceivedbylabel "main" 9```

Amount with at least 100 confirmations

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getreceivedbylabel", "params": ["main", 100] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getreceivedbylabel", "params": ["main", 100] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### gettransaction "txid"

Get detailed information about wallet transaction 

```raptoreum-cli gettransaction "123456789012345678901234567890123456789012345678901234567890000"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "gettransaction", "params": ["123456789012345678901234567890123456789012345678901234567890000"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "gettransaction", "params": ["123456789012345678901234567890123456789012345678901234567890000"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### getwalletinfo

Returns an object containing various wallet state info.

```raptoreum-cli getwalletinfo```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getwalletinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet 
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getwalletinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### importaddress

Adds an address that can be watched as if it were in your wallet but cannot be used to spend.

Import an address with rescan

```raptoreum-cli importaddress "myaddress"```

Import using a label without rescan

```raptoreum-cli  importaddress "myaddress" "testing" false```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "importaddress", "params": ["myaddress", "testing", false] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "importaddress", "params": ["myaddress", "testing", false] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### importprivkey

Adds a private key (as returned by dumpprivkey) to your wallet. 

```raptoreum-cli dumpprivkey "myaddress"```

Import the private key with rescan

```raptoreum-cli  importprivkey "mykey"```

Import using a label and without rescan

```raptoreum-cli importprivkey "mykey" "testing" false```

Import using default blank label and without rescan

```raptoreum-cli importprivkey "mykey" "" false```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "importprivkey", "params": ["mykey", "testing", false] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet 
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "importprivkey", "params": ["mykey", "testing", false] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### importpubkey 

Adds a public key that can be watched as if it were in your wallet but cannot be used to spend.

Import a public key with rescan

```raptoreum-cli importpubkey "mypubkey"```

Import using a label without rescan

```raptoreum-cli importpubkey "mypubkey" "testing" false```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "importpubkey", "params": ["mypubkey", "testing", false] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "importpubkey", "params": ["mypubkey", "testing", false] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### importwallet

Imports keys from a wallet dump file (see **dumpwallet**).

Dump wallet
```raptoreum-cli dumpwallet "test"```

Import wallet

```raptoreum-cli importwallet "test"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "importwallet", "params": ["test"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "importwallet", "params": ["test"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### listreceivedbyaddress

List balances by receiving address.

Minimum 6 confirmations 

```raptoreum-cli listreceivedbyaddress 6```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listreceivedbyaddress", "params": [6, true, true] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

OR

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listreceivedbyaddress", "params": [6, true, true, "RTM1234567890123456789000"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```


testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listreceivedbyaddress", "params": [6, true, true] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```

OR

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listreceivedbyaddress", "params": [6, true, true, "RTM1234567890123456789000"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### listreceivedbylabel 

List received transactions by label.

```raptoreum-cli listreceivedbylabel```

List received transactions by label witch minimum 6 confirmations

```raptoreum-cli  listreceivedbylabel 6 true```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listreceivedbylabel", "params": [6, true, true] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listreceivedbylabel", "params": [6, true, true] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### listwallets

Returns a list of currently loaded wallets.

For full information on wallet, use **getwalletinfo**

```raptoreum-cli listwallets```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listwallets", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listwallets", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### loadwallet

Loads a wallet from a wallet file or directory.

```raptoreum-cli loadwallet "test.dat"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "loadwallet", "params": ["test.dat"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "loadwallet", "params": ["test.dat"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### sendtoaddress

Send an amount to a given address.

```raptoreum-cli sendtoaddress "RTM1234567890123456789012345678900" 0.1```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "sendtoaddress", "params": ["RTM1234567890123456789012345678900", 0.1, "comment", "comment_to"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "sendtoaddress", "params": ["RTM1234567890123456789012345678900", 0.1, "comment", "comment_to"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### setlabel

Sets the label associated with the given address.

```raptoreum-cli setlabel "RTM1234567890123456789012345678900" "main"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "setlabel", "params": ["RTM1234567890123456789012345678900", "main"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "setlabel", "params": ["RTM1234567890123456789012345678900", "main"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### settxfee

Set the transaction fee per kB for this wallet.

```raptoreum-cli settxfee 0.00001```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "settxfee", "params": [0.00001] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "settxfee", "params": [0.00001] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### signmessage

Sign a message with the private key of an address

```raptoreum-cli signmessage "RTM1234567890123456789012345678900" "my message"```

Verify the signature

```raptoreum-cli verifymessage "RTM1234567890123456789012345678900" "signature" "my message"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "signmessage", "params": ["RTM1234567890123456789012345678900", "my message"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "signmessage", "params": ["RTM1234567890123456789012345678900", "my message"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### unloadwallet

Unloads wallet referenced by request endpoint otherwise unloads wallet specified in the argument.

```raptoreum-cli unloadwallet wallet_name```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "unloadwallet", "params": [wallet_name] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "unloadwallet", "params": [wallet_name] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### walletlock

Removes wallet encryption key from memory, locking wallet.

Set passphrase for 2 minutes to perform a transaction

```raptoreum-cli walletpassphrase "my pass phrase" 120```

Perform a send (requires passphrase set)

```raptoreum-cli sendtoaddress "RTM1234567890123456789012345678900" 1.0```

Clear the passphrase since we are done before 2 minutes is up

```raptoreum-cli walletlock```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "walletlock", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "walletlock", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### walletpassphrase

Stores wallet decryption key in memory for 'timeout' seconds.

Unlock the wallet for 60 seconds

```raptoreum-cli walletpassphrase "my pass phrase" 60```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "walletpassphrase", "params": ["my pass phrase", 60] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "walletpassphrase", "params": ["my pass phrase", 60] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```


#### walletpassphrasechange

Changes wallet passphrase from 'oldpassphrase' to 'newpassphrase'.

```raptoreum-cli walletpassphrasechange "oldpassphrase" "newpassphrase"```

```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "walletpassphrasechange", "params": ["oldpassphrase", "newpassphrase"] }' -H 'content-type: text/plain;' http://127.0.0.1:9998/```

testnet
```curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "walletpassphrasechange", "params": ["oldpassphrase", "newpassphrase"] }' -H 'content-type: text/plain;' http://127.0.0.1:19998/```

