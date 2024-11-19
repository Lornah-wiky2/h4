                       ## Bitcoin: A Peer-to-Peer Electronic Cash System
                                      Satoshi Nakamoto
                                       satoshin@gmx.com
                                          www.bitcoin.org
## Read and summarize (with some bullet points)

### 1 Introduction
Online payments currently rely on banks and credit card companies to process transactions, which can be slow and costly.
This system has problems: transactions can be reversed, leading to disputes and fraud concerns, and small payments are often not practical. 
The authors propose a new way to make online payments without needing banks or credit card companies as middlemen. 
This new system would use complex math (cryptography) to make sure payments are secure and can't be reversed or faked. 
It would work like digital cash, allowing people to pay each other directly over the internet, just like handing over physical money in person.

### 2 Transactions
Digital coins are like a chain of signatures, where each owner signs the coin to pass it to the next person. 
The main problem is making sure nobody spends the same coin twice (double-spending).
One solution is to have a central authority (like a mint) check every transaction, but this makes the system depend on a single company. 
The proposed system should make all transactions public, so everyone can see and verify them. 
For this to work, there needs to be a way for everyone to agree on the order of transactions, ensuring the first use of a coin is the only valid one.
 
### 3 Timestamp Server 
A timestamp server creates a unique digital fingerprint (hash) of a group of items and publishes it widely.
Each new timestamp includes the previous timestamp's hash, creating a chain of timestamps that build on each other. 
This chain makes the system stronger over time, as each new timestamp confirms all the ones that came before it.

### 4 Proof-of-Work 
Proof-of-Work is a system used to create a distributed timestamp server without relying on a central authority. 
It involves finding a special number (nonce) that, when added to a block of data and hashed, produces a result with a certain number of leading zeros. 
This process requires significant computer power, making it difficult to change past blocks without redoing all the work for that block and all subsequent blocks. 
The system ensures fairness by making the influence of participants proportional to their computing power, not the number of IP addresses they control. 
The difficulty of the Proof-of-Work adjusts automatically to maintain a steady rate of block creation, regardless of changes in total computing power on the network.

### 5 Network 
The network operates by broadcasting new transactions, with each computer (node) collecting these into blocks and trying to solve a difficult math puzzle (proof-of-work) for their block. 
When a node solves the puzzle, it shares the block with everyone, and other nodes accept it if all transactions in it are valid. 
Nodes always work on extending the longest chain of blocks they know about, which helps resolve conflicts when two different versions of the next block are created at the same time.
The system is designed to be robust, working even if some messages don't reach all nodes or if some nodes miss a block, ensuring the network can continue to function smoothly.
  
### 6 Incentive

The first transaction in each block creates new coins, rewarding the block creator for supporting the network. 
This system distributes new coins into circulation without needing a central authority, similar to how gold miners add new gold to the market. 
Transaction fees can also be added as an incentive, where the difference between a transaction's input and output becomes a fee for the block creator. 
Over time, as a set number of coins enter circulation, the system can shift entirely to transaction fees, becoming inflation-free. 
This incentive structure encourages honesty, as it's more profitable for participants to play by the rules and earn new coins than to try to cheat the system.

## Reference: 
Nakamoto 2008: Bitcoin: A Peer-to-Peer Electronic Cash System (A colored HTML version)

## a) Wallet. Create a BitCoin testnet wallet. (For example, electrum)
I did an upgrade and then installed electrum 
![PIC 1 ELECTRUM INSTALLED](https://github.com/user-attachments/assets/0864f606-d7b4-418e-8bb0-530cdf7e805f)

Configured electrum and created a bitcoin testnet wallet 
![pic 3 created wallet-1](https://github.com/user-attachments/assets/2233aedb-edec-4c0d-bfd4-a7db3969dad0)


## b) Faucet. Get worthless fake money from a testnet Bitcoin faucet.
Went to faucet and got bitcoin money to my wallet (https://coinfaucet.eu/en/btc-testnet/)
![got money from bitcoin faucet](https://github.com/user-attachments/assets/5935c4bd-247b-4490-ac5e-03ac54642deb)

Recieved money
![recieved money in my wallet](https://github.com/user-attachments/assets/c9dd24ec-112e-43a0-8f94-450bbb975e82)

## c) Giveway. Move money to another Bitcoin wallet. Choose an amount where the last two digists are 73.
Created another wallet called liam_wallet. 
![pic 4 created another wallet liam-wallet](https://github.com/user-attachments/assets/9281757f-8d46-42bc-a114-7d8d8a94eb02)

Got address from Liam_wallet which i used to send money from my 1st wallet called Wallet_1 to Liam_wallet.
![moved money to another bitcoin wallet 73 pic 5](https://github.com/user-attachments/assets/08e68d59-aca0-4fa1-9444-05354714f3ba)

Got the error bellow
![error when doing a giveaway pic 6](https://github.com/user-attachments/assets/bee3b5d3-bac4-49a1-9c22-8941a52e2329)

## d) Recycle. Move the testnet money back to the same faucet you got it from.
Moved the money from my wallet back to where i got it from. 
![sent back money qtn d pic 7](https://github.com/user-attachments/assets/8bc7254c-9df6-4287-9416-7cda5db920dc)

## e) Explorer. Use a block explorer to analyze a block on the real Bitcoin blockchain. Explain what each value and field means. You only need to analyze the block information and one sample transaction, as a block can contain many transactions.

To analyze a real Bitcoin block, I'll use the Blockchain.com explorer to examine a recent block. Let's look at block 819,669, which was mined on November 19, 2024.

## Block Information

### Block Height: 819,669
This is the block's position in the blockchain, counting from the genesis block (0).

### Timestamp: 2024-11-19 21:43:45 (UTC)
This indicates when the block was mined.

### Transactions: 2,537
The total number of transactions included in this block.

### Output Total: 8,264.90270775 BTC
The sum of all transaction outputs in this block.

### Size: 1,559,853 bytes
The total size of the block data.

### Weight: 3,993,453
A measure introduced with SegWit to account for the block's impact on node resources.

## Reference:
https://www.gemini.com/cryptopedia/what-is-block-in-blockchain-bitcoin-block-size 

## f) RogeCoin. Critically comment on Honest Ads: If Cryptocurrency Was Honest (Video, about 5 minutes). Identify and list arguments made. Provide commentary to support and challenge each of the claims. If you can, provide references or real life examples to your claims. (This task does not require tests with a computer.)

The video presents a critical view of cryptocurrency, particularly focusing on a fictional "Rochecoin."
### Key Arguments and Claims
### Cryptocurrency is volatile and impractical
-Support: Cryptocurrencies are indeed known for their price volatility
-Challenge: Some cryptocurrencies aim to be "stablecoins," pegged to traditional currencies to reduce volatility.

### Environmental impact
-Support: Bitcoin mining alone consumes more electricity than some countries
-Challenge: Some cryptocurrencies are exploring more energy-efficient consensus mechanisms, like Proof of Stake.

### Limited real-world utility
-Support: Many cryptocurrencies are not widely accepted for everyday transactions.
-Challenge: Some businesses and countries are beginning to accept cryptocurrencies as payment.

### Security risks
-Support: Cryptocurrency exchanges and wallets have been hacked, resulting in significant losses
-Challenge: Proper security measures can mitigate risks, and blockchain technology itself is generally secure.
### Speculation-driven market
-Support: Cryptocurrency prices often fluctuate based on social media trends or celebrity endorsements.
-Challenge: Traditional markets can also be influenced by similar factors, albeit to a lesser extent.
### Regulatory uncertainty
-Support: Many countries have unclear or changing regulations regarding cryptocurrencies.
-Challenge: Some nations are developing comprehensive regulatory frameworks for digital assets.
### Mining hardware issues
-Support: Cryptocurrency mining has led to shortages and price increases in GPUs.
-Challenge: This mainly affects Proof of Work cryptocurrencies, not all digital assets.
Commentary
The document uses humor and exaggeration to highlight legitimate concerns about cryptocurrencies. While some points are valid, the overall tone is overly cynical and dismissive of potential benefits. Real-life examples supporting some claims include the 2022 crypto market crash, which saw major cryptocurrencies lose significant value, and the environmental concerns raised about Bitcoin mining in countries like China and Iran. However, the document overlooks potential benefits of blockchain technology, such as increased financial inclusion in underbanked regions and the development of decentralized finance (DeFi) applications. It's worth noting that the cryptocurrency space is rapidly evolving, with ongoing efforts to address many of the issues raised in this satirical piece. Balanced, informed discussions about the pros and cons of cryptocurrencies are crucial for their responsible development and adoption.

## Reference:
https://www.youtube.com/watch?v=GUs5y9leCyA 
