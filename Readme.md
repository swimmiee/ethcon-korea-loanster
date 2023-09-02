# Loanster
## Make Easy and Various Strategy for LP using Lending Protocol 

## Contract Address 
(We didn't verify yet)
[Linea Mainnet]
- Menu Contract : [0xa48719d977e5823a7881ba3d7a49b81673adaebb](https://lineascan.build/address/0xa48719d977e5823a7881ba3d7a49b81673adaebb)
- Toaster Contract: [0xb8e0cdbad514edc1e8e790f4b6f5f613361802a7](https://lineascan.build/address/0xb8e0cdbad514edc1e8e790f4b6f5f613361802a7)
  
[Polygon zkEVM]
- Menu Contract: [0xa48719d977e5823a7881ba3d7a49b81673adaebb](https://zkevm.polygonscan.com/address/0xa48719d977e5823a7881ba3d7a49b81673adaebb)
- Toaster Contract: [0xb8e0cdbad514edc1e8e790f4b6f5f613361802a7](https://zkevm.polygonscan.com/address/0xb8e0cdbad514edc1e8e790f4b6f5f613361802a7)

## Problem
### 1.UniswapV3 IL (Unstable - stable pool)
Uniswap V3 is more damaging to ILs than the original Uniswap V2.  Below is a graph of IL as a function of range for a pair of unstable and stable coins (x-axis is the percentage change in price, y-axis is the value of liquidity).

https://github.com/swimmiee/ethcon-seoul-toaster/assets/89185836/454b6792-e14c-4cbe-8e7d-0397f07dfd3e

As you can see, the narrower the range, the more the value of liquidity changes per price change. In other words, the narrower the price range, the worse the IL.
### 2. Limited LP strategy
This is not possible with traditional LPs, who can make high-return, high-risk investments and low-return, low-risk investments based on the user's situation and appetite. 
They simply provide liquidity and earn fees for doing so. 
However, there are 3 types of markets: rising, falling, and sideways, and LPs only benefit from sideways markets and do not suffer from IL. 
In a rising market, it may be a better strategy to choose a product with more upside potential than the opportunity cost of suffering IL and investing LPs. 
In a falling market, it may be a better choice to invest in other markets (Nasdaq, real estate) rather than crypto. 
This is a very difficult problem in the Defi market, where liquidity is critical. 

### 3. UniswapV3 Investment UX Problem

Unlike V2, Uniswap V3 will determine the amount of both tokens based on a price range (maximum, current, minimum) rather than providing liquidity with the value of both tokens being the same. 
Users will then have to calculate how much they need to swap to provide liquidity and what range they need to put it in to get all the value they want (exactly what I want to put in if I want to invest $1000). 
However, if I'm using a pool that I'm trying to liquidate, the swaps that I'm executing to liquidate could actually impact the current price and cause me to put in less liquidity than I wanted to put in. 

## Solution
### Use Lending Protocol(Spark Protocol) for hedging : Solution of Problem 1,2
### Toaster Contract : Solution of Problem 3


## How to use Loanster?
### 
