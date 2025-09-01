# 🚀 INVARIFI: Core Smart Contracts Showcase

## 📖 Overview

This directory contains the essential smart contracts that demonstrate INVARIFI's core functionality: **auto-swap**, **auto-compound**, **rebalancing**, and **stop-loss** mechanisms.

## 🏗️ Core Smart Contracts

### **Main Components:**

1. **`VaultV7.sol`** - Main vault with automation
   - User deposit/withdrawal management
   - Automatic fund allocation to strategies via `earn()`
   - Strategy upgrade capabilities through `upgradeStrat()`
   - Fee management and access control

2. **`StrategyCurveConvex.sol`** - Core strategy with ALL functions
   - Auto-compound via `harvest()`
   - Auto-swap via `_swapRewardsToNative()`
   - Auto-stop via `panic()`, `pause()`, `unpause()`
   - Rebalancing via `setConvexPid()`

3. **`Harvester.sol`** - Automatic reward collection
   - Chainlink Keepers integration
   - Multi-vault harvesting
   - Gas optimization
   - Automatic execution scheduling

4. **`EarnPool.sol`** - Advanced pool with stop-loss
   - Stop-loss automation
   - Gelato integration
   - OneInch swap integration
   - User position automation

5. **`StrategyExactlyLeverage.sol`** - Strategy with rebalancing
   - LTV-based rebalancing
   - Flash loan integration
   - Dynamic position management
   - Risk parameter optimization

6. **`VelodromeV2Zap.sol`** - Automatic token swapping
   - Automatic liquidity calculation
   - Optimal swap routing
   - LP token management
   - Vault integration

7. **`BaseZapOneInch.sol`** - OneInch integration for optimal swaps
   - OneInch router integration
   - Error handling and propagation
   - Token approval management
   - Asset return functionality

### **Multiple OneInch Zap Strategies:**

8. **`BalancerAuraZapOneInchETH.sol`** - Balancer + Aura integration
9. **`BaseSwapZapOneInchBase.sol`** - BaseSwap integration
10. **`CurveZapOneInchOp.sol`** - Curve integration on Optimism
11. **`VelodromeZapOneInchOp.sol`** - Velodrome integration on Optimism

### **Base Classes:**

12. **`StratFeeManagerAccessableInitializable.sol`** - Base strategy class
    - Fee management
    - Access control
    - Pausable functionality
    - Router management

## 🔄 Core Features Demonstrated

### **✅ Auto-Swap (Auto-Swap)**
- **StrategyCurveConvex.sol**: `_swapRewardsToNative()` - Multi-DEX reward swapping
- **BaseZapOneInch.sol**: `_swapViaOneInch()` - OneInch optimal routing
- **VelodromeV2Zap.sol**: `_swapAndStake()` - Automatic entry/exit swapping

### **✅ Auto-Compound (Auto-Compound)**
- **StrategyCurveConvex.sol**: `_harvest()` - Automatic reward reinvestment
- **Harvester.sol**: `_multiHarvest()` - Multi-vault automated harvesting

### **✅ Rebalancing (Rebalance)**
- **StrategyCurveConvex.sol**: `setConvexPid()` - Strategy switching
- **StrategyExactlyLeverage.sol**: `rebalance()` - LTV-based rebalancing

### **✅ Stop-Loss (Stop-Loss)**
- **EarnPool.sol**: `closeByStopLoss()` - Automated position closure
- **StrategyCurveConvex.sol**: `panic()` - Emergency withdrawal

### **✅ Auto-Stop (Auto-Stop)**
- **StrategyCurveConvex.sol**: `pause()`, `unpause()` - Emergency controls
- **StratFeeManagerAccessableInitializable.sol**: Pausable functionality

## 🎯 Technical Specifications

### **Solidity Version:** ^0.8.0
### **Key Dependencies:**
- OpenZeppelin contracts
- Chainlink Keepers
- Gelato automation
- OneInch aggregator
- Multiple DEX protocols

### **Security Features:**
- Access control and role management
- Reentrancy protection
- Pausable functionality
- Fee caps and limits
- Emergency withdrawal functions

## 🚀 What These Contracts Demonstrate

These smart contracts showcase the complete INVARIFI ecosystem:

1. **Vault management** with automated strategy allocation
2. **Strategy execution** with auto-compound and auto-swap
3. **Risk management** with stop-loss and emergency controls
4. **Automation** through keepers and external services
5. **Optimal routing** via OneInch and multiple DEX
6. **Advanced rebalancing** with flash loan integration
7. **Multi-chain support** across different networks

---

*This collection represents the core smart contracts that power INVARIFI's advanced DeFi automation platform, demonstrating industry-leading features in yield farming optimization.*
