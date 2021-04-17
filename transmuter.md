# 煉金師 (Transmuter)
*[Offical English Manual-Transmulter](https://alchemix-finance.gitbook.io/alchemix-finance/transmuter)

Transmuter 是主要的alchemix 合成代幣的釘住機制. Transmuter.sol 智能合約驅動著Transmuter. 收穫收益會直接流入它. 它的參與會確保參與者會履行一個 1:1 alUSD 對 DAI 的贖回.

使用者存入 alUSD 到 Transmuter. 當收益進入時, 它將依使用者鎖定比例來分配DAI收益給使用者. 當使用者選擇提取被轉化的DAI時, 等量的 alUSD 會被燒毀.

這個流程的一個有趣的副作用是使用者的頭寸(position)可能會被過度填滿.例如, 一個使用者存入 1000 alUSD, 過一段時間後, 鎖定的頭寸會變為 1050 DAI. 一旦這個使用者超越這個限制,很有可能的另一個使用者會代為索取.對任何一個 DAI 結餘超過 alUSD 鎖定量的帳號,代表索取的使用者將會把他們的鎖定 alUSD 轉化部分成那個差額. 在上述的例子中, 代表索取的使用者將會有 50 alUSD立即成轉成 DAI. 假如代表索取的使用者是 alUSD 鎖倉者本人索取這個 DAI的差額的話, 差額將會回到 Transmuter 然後分散的全域. 

現在煉金師升級了並且將其資本放到 yearn yvDAI vault 裡了. 收穫的收益會被放到 Alchemix Vault 的智能合約中, 然後快速增加 DAI 存款者的收益. 這個循環也有效的增加了系統的複合收益, 因此加速了債務的償還速度. 有五百萬DAI 沒有放進 yearn yvDAI 來作為緩衝. 其作用是省下使用者呼叫 Transmuter 的費用來改善 Transmuter 的使用者體驗.  

###### tags: `Defi` `Alchemix` `User Manual` `Tranditional Chinese` `zh_tw`