# Stormstout Contract

![maxresdefault](https://user-images.githubusercontent.com/3152452/192136997-c064a433-102d-49e2-a3c4-729b9ef90581.jpeg)

## **Getting started**

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

## **Features**

- [x] List token
- [x] Buy token
- [ ] Cancel token
- [ ] Bid mode

## **Contributing**

Bug report or pull request are welcome.

## **Make a pull request**

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

Please write unit test with your code if necessary.

## **License**

web3 is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).