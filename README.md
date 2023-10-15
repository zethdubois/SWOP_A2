Coinmarketcap ontology

# Concept

## Domain Coverage
The ontology will cover the domain of cryptocurrency market data, specifically focusing on aspects related to:

* Cryptocurrencies and their attributes (e.g., price, market cap, volume, etc.)
* Exchanges and market pairs
* Wallets and their reviews
* Users and their interactions (e.g., reviews)
* Developers and ICOs
* News articles related to cryptocurrencies
* Historical data and trading volumes

## Use of the Ontology
The ontology could be used for:

* Information Retrieval: Enabling users to query and retrieve detailed information about cryptocurrencies, exchanges, market pairs, wallets, and related news.
* Data Integration: Integrating data from various sources to provide a comprehensive view of the cryptocurrency market.
* Semantic Search: Enabling users to perform semantic searches related to cryptocurrencies, exchanges, and other related entities.
* Knowledge Discovery: Identifying relationships and patterns within the cryptocurrency market data.
* Decision Support: Assisting investors and traders in making informed decisions by providing structured and semantically enriched data.

## API
Integrating an ontology with CoinMarketCap's API involves fetching data from the API, transforming it into a format that aligns with the ontology, and then populating the ontology with this data. Here are some steps and issues to consider:


# Requirements

- Properties like `:circulatingSupply`, `:totalSupply`, and `:maxSupply` represent numerical values related to the supply of a cryptocurrency, hence have a range of `xsd:float`.
- Properties like `:launchDate`, `:newsDate`, `:icoStartDate`, and `:icoEndDate` represent dates and thus have a range of `xsd:date`.
- Textual properties like `:reviewText` and `:newsTitle` have a range of `xsd:string`.
- The `:reviewRating` property, which might represent a score or rating, has a range of `xsd:float`.

- [x] 15 classes
- [x] 15 object properties
- [x] 20 datatype properties
- [x] 20 individuals
- [x] Use class constructs
	- [x] unionOf
	- [x] disjointWith
	- [x] intersectionOf
	- [x] allValuesFrom
	- [x] oneOf
- [x] Use property constructs
	- [x] transitive property
	- [x] symmetric property
	- [x] inverse property
	- [x] disjoint property
- [x] Assert the domain and rage of **AT LEAST 10** properties

## Classes
The ontology defines the following 27 classes:

1. `:Blockchain`
2. `:Cryotpocurrency`
	1. `:Coin
	2. `:Token`
3. `:Developer`
4. `:Exchange`
5. `:FinancialEntity`
	1. `:Bank`
	2. `:CryptocurrencyExchange`
		1. `:VerifiedExchange`
6. `:HistoricalData`
7. `:ICO`
8. `:Investor`
9. `:Liquidity`
10. `:MarketCap`
11. `:MarketPair`
12. `:NewsArticle`
13. `:Person`
14. `:PopularCryptocurrency`
15. `:Review`
16. `:SecureEncryption`
17. `:TradingVolume`
18. `:User`
19. `:VerifiedEntity`
	1. `:VerifiedExchange`
20. `:Wallet`
	1. `:SecureWallet`
## Object Properties
The ontology defines the following 23 object properties:

1. `:hasDeveloper`
2. `:hasExchange`
3. `:hasHistoricalData`
4. `:hasLiquidity`
5. `:hasMarketCap`
6. `:hasRoadmap`
7. `:hasToken`
8. `:hasTradingVolume`
9. `:hasUserReview`
10. `:hasWallet`
11. `:hasWebProfile`
12. `:hasWebsite`
13. `:hasWhitepaper`
14. `:investedIn`
15. `:isLinkedTo`
16. `:launchedBy`
17. `:launchedICO`
18. `:relatedToNews`
19. `:tradedInPair`
20. `:tradedOnExchange`
21. `:usesBlockchain`
22. `:usesEncryption`
23. `:writtenBy`
## Datatype Properties

The ontology defines the following 20 datatype properties:

1. `:allTimeHighPrice`
2. `:allTimeLowPrice`
3. `:circulatingSupply`
4. `:currentPrice`
5. `:icoEndDate`
6. `:icoRaisedAmount`
7. `:icoStartDate`
8. `:launchDate`
9. `:marketCapValue`
10. `:maxSupply`
11. `:name`
12. `:newsDate`
13. `:newsTitle`
14. `:priceChange24h`
15. `:priceChangePercentage24h`
16. `:reviewRating`
17. `:reviewText`
18. `:symbol`
19. `:totalSupply`
20. `:volume24h`

## Individuals

The ontology defines the following 26 individuals:

1. `:AES256Encryption
2. `:BasicEncryption
3. `:Binance`
4. `:Bitcoin`
5. `:BitcoinMarketCap`
6. `:Coinbase`
7. `:Doge`
8. `:DogeMarketCap`
9. `:Ethereum`
10. `:EthereumMarketCap`
11. `:FoxToken`
12. `:FoxTokenICO`
13. `:FoxTokenMarketCap`
14. `:Investor1`
15. `:JohnDoe`
16. `:Kraken`
17. `:Litecoin`
18. `:LitecoinMarketCap`
19. `:Monero`
20. `:MoneroMarketCap`
21. `:Stellar`
22. `:StellarICO`
23. `:StellarMarketCap`
24. `:StellarToken`
25. `:ZCash`
26. `:ZCashMarketCap`

## Properties with domain and range
The following properties have their domains and ranges defined:

1. **Property**: `:hasDeveloper`  
    **Domain**: `:Cryptocurrency`  
    **Range**: `:Developer`
    
2. **Property**: `:hasExchange`  
    **Domain**: `:Cryptocurrency`  
    **Range**: `:Exchange`
    
3. **Property**: `:hasHistoricalData`  
    **Domain**: `:Cryptocurrency`  
    **Range**: `:HistoricalData`
    
4. **Property**: `:hasLiquidity`  
    **Domain**: `:Cryptocurrency`  
    **Range**: `:Liquidity`
    
5. **Property**: `:hasMarketCap`  
    **Domain**: `:Cryptocurrency`  
    **Range**: `:MarketCap`
    
6. **Property**: `:hasToken`  
    **Domain**: `:ICO`  
    **Range**: `:Token`
    
7. **Property**: `:hasTradingVolume`  
    **Domain**: `:Cryptocurrency`  
    **Range**: `:TradingVolume`
    
8. **Property**: `:hasUserReview`  
    **Domain**: `:Cryptocurrency`  
    **Range**: `:Review`
    
9. **Property**: `:hasWallet`  
    **Domain**: `:User`  
    **Range**: `:Wallet`
    
10. **Property**: `:investedIn`  
    **Domain**: `:Investor`  
    **Range**: `:ICO`

## Class Constructs
### owl:disjointWith
This is used to specify that two classes have no instances in common.

```turtle
:Exchange owl:disjointWith :Cryptocurrency .
```

### owl:unionOf
This is used to define a class that is a union of two or more classes.

```turtle
:FinancialEntity a owl:Class ;
    owl:unionOf ( :Exchange :Cryptocurrency ) .

```
`:FinancialEntity` could be defined as a class that includes individuals that are either of type `:Bank` or `:CryptocurrencyExchange`.
### owl:intersectionOf
This is used to define a class that is an intersection of two or more classes.

```turtle
:VerifiedExchange rdf:type owl:Class ;
                 owl:intersectionOf (:CryptocurrencyExchange :VerifiedEntity) .

```
`:VerifiedExchange` could represent entities that are both `:CryptocurrencyExchange` and `:VerifiedEntity`.

### owl:oneOf
This is used to define a class by explicitly listing its instances.

```turtle
:PopularCryptocurrency rdf:type owl:Class ;
                       owl:oneOf (:Bitcoin :Ethereum :Litecoin) .

```

`:PopularCryptocurrency` might be defined as a class that includes specific individuals, such as `:Bitcoin`, `:Ethereum`, and `:Litecoin`.
### owl:allValuesFrom
(requires defining a restriction)

```turtle
:SecureWallet rdf:type owl:Class ;
             rdfs:subClassOf [ rdf:type owl:Restriction ;
                               owl:onProperty :usesEncryption ;
                               owl:allValuesFrom :SecureEncryption ] .

```

`:SecureWallet` might be a class of wallets, all of which use a type of `:SecureEncryption` for the property `:usesEncryption`.

#### Examples of this restriction

1. **Valid**: A wallet is considered a `:SecureWallet` without having the `:usesEncryption` property (it does not violate the restriction)
```turtle
:MyWallet rdf:type :SecureWallet .
```

2. **Valid**: A wallet is a `:SecureWallet` and uses an encryption method that is a `:SecureEncryption`.

```turtle
:MyWallet rdf:type :SecureWallet ;
          :usesEncryption :SomeSecureEncryptionMethod .

:SomeSecureEncryptionMethod rdf:type :SecureEncryption .
```

3. **Invalid**: A wallet is a `:SecureWallet` but uses an encryption method that is **not** a `:SecureEncryption`

```turtle
:MyWallet rdf:type :SecureWallet ;
          :usesEncryption :SomeInsecureEncryptionMethod .

:SomeInsecureEncryptionMethod rdf:type :InsecureEncryption .
```



## Property Constructs

### Transitive Property: `:isPartnerOf`
```turtle
:ExchangeA :isPartnerOf :ExchangeB .
:ExchangeB :isPartnerOf :ExchangeC .
```
- **Definition**: `:isPartnerOf` is defined as a transitive property.
- **Implication**: If `:ExchangeA` is a partner of `:ExchangeB`, and `:ExchangeB` is a partner of `:ExchangeC`, then it is inferred that `:ExchangeA` is a partner of `:ExchangeC`.

### Symmetric Property: `:isCompetitorOf

```turtle
:CoinA :isCompetitorOf :CoinB .
```

- **Definition**: `:isCompetitorOf` is defined as a symmetric property.
- **Implication**: If `:CoinA` is a competitor of `:CoinB`, then it is automatically inferred that `:CoinB` is a competitor of `:CoinA`.

### Inverse Property: `:owns` and `:isOwnedBy`
```turtle
:InvestorA :owns :WalletA .
```
- **Definition**: `:owns` and `:isOwnedBy` are defined as inverse properties of each other.
- **Implication**: If `:InvestorA` owns `:WalletA`, then it is automatically inferred that `:WalletA` is owned by `:InvestorA`. Conversely, if we state that `:WalletA :isOwnedBy :InvestorA`, it is inferred that `:InvestorA :owns :WalletA`.

### Disjoint Property: `:investsIn` and `:divestsIn`

```turtle
:InvestorB :investsIn :CoinC .
```
- **Definition**: `:investsIn` and `:divestsIn` are defined as disjoint properties.
- **Implication**: If `:InvestorB` invests in `:CoinC`, it cannot be true that `:InvestorB` divests in `:CoinC` at the same time (and vice versa). The ontology will be inconsistent if both statements are true for the same individuals.

# Errors
I used Protege reasoner `HermiT 1.4.3.x` to check for consistency in the code. This helped to isolate a number of mistakes.

One example are the Object Properties
	:hasWhitepaper
	:hasWebsite
	:hasRoadmap

which were each described as Datatype properties, throwing an error in the console:
```
ERROR 15:46:36 Attempt to transform an axiom to correct misuse of properties failed. Property replacement: {hasWhitepaper=hasWhitepaper, hasWebsite=hasWebsite, hasRoadmap=hasRoadmap}, axiom: <http://www.example.org/ontology#StellarICO> hasRoadmap <http://www.stellarico.com/roadmap.pdf>, error: class org.semanticweb.owlapi.model.IRI cannot be cast to class
```

Other errors occurred during development, but I did not capture them.