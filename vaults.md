# 金庫 (Vaults)

*[Offical English Manual-Valuts](https://alchemix-finance.gitbook.io/alchemix-finance/vaults)

Vaults 是 Alchemix 協議的中心. Alchemist.sol 智能合約驅動著 Vaults. 以下是在初始的版本中使用 DAI 作為合成穩定幣的運作機制: 

1. 儲存 DAI 到 Vault
2. 借出 alUSD  最多可達借貸資產的50%. 貸款將有一個最少200% 的抵押品比例.
3. 存入 DAI 就是等於存入 yearn.finance 的 yDAI Vault
4. 收益來自收割 yDai 的 Vault 代幣
5. 此收益將用來給付給系統裡全域債務, 以便減輕所有存入者的債務. 假如你有存入 DAI 但卻沒借 alUSD, 收益將會以 alUSD 計入你的帳戶.
6. 一但收穫利益減少了全域債務以後, 它將會被轉移到煉金師(transmuter) 智能合約
7. 使用者可以提取至多200%抵押品比例的存款. 因此隨著協議清還你的債務, 你可以提取更多的DAI.
8. 你隨時可以償還你部分或全部的債務來解除你的抵押品. 在還款或是清算時, DAI 與 alUSD 會被視為 1:1 的關係. 因此可以使用 alUSD 以及/或是 DAI 來償還你的 alUSD 債務. 使用 alUSD 來償還債務也是一個釘住的機制. 假如 alUSD 在釘住之下, 使用者可以從各個不同的AMM買進然後來償還他們的貸款
9. 任何時間你都可以清算一部分或全部的抵押品. 智能合約從你的抵押品裡使用 DAI 來償還你的 alUSD 債務
 

基本上來說 vaults 提供了使用者一個他們未來收益信用的柔性管路. 使用者任何時候都可以進場跟出場而不用承諾長時的鎖定. 使用者的抵押品不會被清算, 因為你的債務只會減少. 在產品上架之後, 很快的我們會讓更多穩定幣當作抵押品來讓使用者借貸 alUSD.

我們最重視的是使用者存入資產的安全. 這就是為何我們選擇 yearn 當作我們的收益聚合器.(yield aggregator) Alchemix 也正在進行安全性的審查以及審核, 儘管如此嚴謹, 這並不保證不會有任何不好的事發生. Vaults 有一個緊急關閉的機制為此而生. 假如這個程序啟動了, 那麼所有的資金會被從 yearn.finace 裡抽回. 存入動作會被暫停, 使用者可以付清它們的債務然後安全的離開系統. 希望如此可以避免或是減輕任何損失.

另外有兩個安全衡量可以來保護 Alchemix 的合成代幣.第一, 每個資產可以鑄造的的 alUSD 是有限制的. 這個限制決定在這個資產的技術的程度, 市場以及法律的風險. 第二, Alchemix 會使用 Chainlin 預言機上的價格.(price feeds)  當一個穩定幣的價格在某個筏值之下, 鑄造, 使用基礎資產的償還以及清會被暫停值到價格回到一個可接受的的程度. 這些安全衡量無法完全的制止stable coin 失去它的釘住(peg)或是失去價值所帶來的傷害, 但可以保護大部分 Alchemix 合成代幣的價值.


###### tags: `Defi` `Alchemix` `User Manual` `Tranditional Chinese` `zh_tw`