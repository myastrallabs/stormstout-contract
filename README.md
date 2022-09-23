# Stormstout Contract

## *Getting started*

1. Initialize the aptos configuration, if you don't already have it

```shell
aptos init
```
2. Fund with faucet
```shell
aptos account fund-with-faucet --account default
```

3. Compile contract

```shell
aptos move compile --named-addresses Stormstout=default
```
4. Test Contract

```shell
# test
aptos move test --named-addresses Stormstout=default
```

5. Publish Contract to Devtest/testNet

```shell
# publish
aptos move publish --named-addresses Stormstout=default
```

6. Calling contract create_market function

```shell
aptos move run --function-id 'default::marketplace::create_market' --type-args '0x1::aptos_coin::AptosCoin' --args string:Stormstout u64:0 address:default u64:0 
```

```shell
aptos move run --function-id 'default::marketplace::list_token' --type-args '0x1::aptos_coin::AptosCoin' --args address:default string:Stormstout address:default string:test1 string:test1 u64:0 u64:100
```