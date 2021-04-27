# Solana 基礎教學—Sollet 

[![hackmd-github-sync-badge](https://hackmd.io/uefTN-dqSRK9H0FIxBJ1BQ/badge)](https://hackmd.io/uefTN-dqSRK9H0FIxBJ1BQ)

:::info
Sollet 錢包是 Solana 生態系支援度最好的錢包，是 Serum 團隊開發出的第一個 Solana 網頁錢包
:::

>Sollet 錢包有兩種（網頁版及插件版），目前以網頁版做示範

 [TOC]
 
## 創建錢包

### 1.打開[Sollet](https://www.sollet.io)

 ![](https://i.imgur.com/yoCpI3y.png)

+ 中間白色那塊是註記詞，是網頁隨機生成的
+ 如果怕不安全可以[恢復註記詞](#恢復錢包)
+ 記下24個英文單字後將下面Check box 打勾就能進下一步

:::warning
注意！請保存好註記詞，詞在幣在。
寫在紙上，或刻在[硬邦邦金屬錢包](https://jlopp.github.io/metal-bitcoin-storage-reviews/)，不要拍照、不要截圖、不要存 [evernote](https://www.blocktempo.com/300-k-stablecoin-hacked-due-to-the-victim-left-wallet-key-online/)
:::

- [x] <span style="color:red">我已將我的註記詞存放在安全的地方，而且不會以數位的形式存放</span>

### 2.確認註記詞
![](https://i.imgur.com/kdI47aM.png)
+ 在格子填入剛剛抄下的詞
+ 點 CONTINUE

### 3.設定密碼

![](https://i.imgur.com/oYDMisc.png)

+ 這個密碼只負責解鎖錢包，跟註記詞沒有關係，忘記一樣可以恢復
+ 建議設定密碼，雖然每次解鎖都要打密碼，但是安全性較高
+ 不想設定直接點 Create Wallet 就可以了

### 4.錢包介面

![](https://i.imgur.com/L23yFzj.png)

+ 可以看到SOL的餘額
+ Receive點了可以複製錢包地址
+ Send 可以發錢，Solana的手續費極度便宜，普通轉帳只要0.000005 SOL

> ~~可以發進我錢包~~ Eju2tkwFmYLZZyiEEFuHSEGAK9YXkbGsP8sKX57CneEG

+ View on Solana 會帶你到[Explorer](https://explorer.solana.com/)
+ Export 可以存取私鑰
+ 右上的 Account 可以連 Ledger 或是創不同帳號、輸出註記詞

## 恢復錢包

### 1.打開[Sollet](https://www.sollet.io)

 ![](https://i.imgur.com/yoCpI3y.png)
 
 + 點左下 Restore existing wallet
 + 準備好註記詞，12字或是24字都可以

### 2.輸入註記詞

![](https://i.imgur.com/4n6Lx77.png)

+ 第一格輸入註記詞
+ 下面密碼自訂
+ 這個密碼只負責解鎖錢包，跟註記詞沒有關係，忘記一樣可以恢復
+ 建議設定密碼，雖然每次解鎖都要打密碼，但是安全性較高
+ 不想設定直接點 NEXT 就可以了

### 3.選擇 derivation path

:::info
Solana 的 Path 規定一直改，目前 sollet 預設是 m/44'/501'/0'/0' 所以恢復時選這個最好
:::

![](https://i.imgur.com/ULDuA3U.png)

+ 右上角每個 Path 都看一次，建議全部轉到 m/44'/501'/0'/0'
+ 選好後在右下角點 RESTORE，就會到[錢包介面](#4.錢包介面)了

## SPL token 地址

### Mint 新地址

![](https://i.imgur.com/7Xt3wqk.png)

+ 點錢包介面右上角加號

![](https://i.imgur.com/bYMym7J.png)

+ 確定錢包裡有足夠的 SOL （建議放0.1顆以上） 支付 Rent
+ 在列表中選擇要 mint 的 Token 點 ADD

:::warning
沒在列表內的 Token 要注意安全，不要加來路不明的 Token
:::

#### Manual input (自訂 Mint)

![](https://i.imgur.com/K143YDm.png)

+ 第一格填 Mint 地址
+ 第二格填名字
+ 第三格填代號
+ 點 Add 就會送出交易了

:::info
SPL 地址可以刪除，會退回部分的 Rent。沒 mint 過的 token，從 [FTX](https://ftx.com/#a=wei1769) 提出會幫你出 Rent，~~嚕爆~~
:::

## 刪除重複的 Mint

:::info
有時候從 [FTX](https://ftx.com/#a=wei1769) 轉出會多一個同 Mint 的地址
:::

![](https://i.imgur.com/XlbPlpi.png)


### 解決方法

+ 用 [SPL token UI](https://hackmd.io/@wei0403/SJtCp2Hvu)

## SPL 轉帳

![](https://i.imgur.com/XdKT3lI.png)

+ 點要轉帳或是收款的幣
+ 選 Receive 可以複製收款地址
+ 選 Send 可以轉帳

:::info
目前 Sollet 支援 SPL 地址和 SOL 地址轉帳
轉給 SOL 地址： Sollet 會自動判定對方有沒有這個 Mint，直接轉進去
如果對方沒有，你會幫對方出 Rent 直接 Mint 一個新帳號再轉進去
:::

## 連結網站

+ 以 [Step Finance](https://test.step.finance) 為例

![](https://i.imgur.com/iftPaPN.png)

+ 點 Connect

![](https://i.imgur.com/FnNaisR.png)

+ 點 Sollet，會另外開一個 Tab

![](https://i.imgur.com/ZU6gpHr.png)

* 確定好網址正確後點 Connect
* 就能開始使用網站功能了

:::warning
另外打開的分頁不能關掉，否則錢包連結會斷線
:::

## 簽署交易
+ 在已連結的網站上送出交易時，會跳到 Sollet 的分頁

![](https://i.imgur.com/Dl5yywx.png)

+ 確定好交易細節後就可以滑到最下面點 Approve，交易就會送出並回到原網站

:::warning
請確定所有資料正確、網址正確再簽署
Don't trust, Verify.
:::

## 結語
:::success
可以訂閱我的 [Telegram 頻道](https://t.me/wei9103)取得更多資訊
有任何問題都可以私訊[我](https://t.me/wei1769)
想要補充可以自行加入，或是告訴我漏掉什麼
覺得本篇有幫助可以分享出去造福更多人
歡迎自由捐贈  
Solana: Eju2tkwFmYLZZyiEEFuHSEGAK9YXkbGsP8sKX57CneEG  
Ethereum, BSC: 0x2618026D22C4F6320FCBAC34C45CC4A1f0A92F6B (wei1769.eth)
:::