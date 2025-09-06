# 🏆 Gold-Digger
<p align="center">
  <img src="https://via.placeholder.com/400x400/FFD700/000000?text=⛏️%0AGold%0ADigger%0A💰%0AML%20Data%0AMiner" alt="Gold-Digger Banner"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/python-3.8%2B-blue?style=for-the-badge&logo=python" alt="Python Version"/>
  <img src="https://img.shields.io/badge/license-MIT-green?style=for-the-badge" alt="License"/>
  <img src="https://img.shields.io/badge/crypto-exchanges-orange?style=for-the-badge&logo=bitcoin" alt="Crypto Exchanges"/>
  <img src="https://img.shields.io/badge/ML-ready-purple?style=for-the-badge&logo=tensorflow" alt="ML Ready"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-active-brightgreen?style=flat-square" alt="Status"/>
  <img src="https://img.shields.io/badge/exchanges-6-blue?style=flat-square" alt="Exchanges"/>
  <img src="https://img.shields.io/badge/indicators-15+-red?style=flat-square" alt="Technical Indicators"/>
  <img src="https://img.shields.io/badge/data%20format-SQLite-lightgrey?style=flat-square" alt="Data Format"/>
</p>

## 🎯 What is Gold-Digger?

**Gold-Digger** is the ultimate cryptocurrency data mining bot that strikes digital gold for your ML applications! 💎 This Python powerhouse collects, processes, and stores crypto trading data with a focus on **volume breakouts** and **technical patterns** - perfect for training machine learning models to predict market movements.

### 🚀 Key Features

- **⛏️ Multi-Exchange Mining**: Collects data from 6 major exchanges (Binance, Kraken, Crypto.com, OKX, Bitfinex, Coinbase)
- **💰 Volume Breakout Detection**: Advanced algorithms to identify volume jackpots and trading opportunities
- **🧠 ML-Ready Data**: Pre-processed feature vectors and targets for supervised learning
- **🔧 Technical Arsenal**: 15+ technical indicators (RSI, MACD, Bollinger Bands, etc.)
- **🏦 Secure Data Vault**: SQLite database optimized for ML training workflows
- **🎪 Entertaining Logs**: Funny mining-themed messages that make data collection enjoyable!

## 📊 Volume Breakout Focus

Gold-Digger specializes in identifying **volume breakouts** - those golden moments when trading volume explodes, often preceding significant price movements:

- **2x Volume Spikes**: Early warning signals
- **3x Volume Explosions**: Strong breakout candidates  
- **5x Volume Jackpots**: Rare mega-breakouts for premium opportunities
- **Follow-through Analysis**: Price impact tracking for breakout validation

## 🛠️ Installation

### Prerequisites

```bash
Python 3.8+
pip package manager
```

### Quick Setup

```bash
# Clone the golden repository
git clone https://github.com/xtoor/gold-digger.git
cd gold-digger

# Install dependencies
pip install pandas numpy sqlite3 requests ccxt ta schedule

# Configure your API keys (optional but recommended)
# Edit the setup_mining_operations() function with your exchange API credentials

# Start mining!
python gold_digger.py
```

### Required Libraries

```txt
pandas>=1.3.0
numpy>=1.21.0
requests>=2.25.0
ccxt>=4.0.0
ta>=0.10.0
schedule>=1.1.0
sqlite3 (built-in)
```

## 🎮 Usage

### Basic Mining Operation

```python
from gold_digger import GoldDigger

# Initialize the mining rig
digger = GoldDigger()

# Launch full expedition (top 30 cryptos, 30 days history)
digger.launch_full_mining_expedition(top_n=30, days=30)

# Get ML training data
training_data = digger.get_ml_training_gold()
feature_vectors = digger.get_ml_features()
```

### Scheduled Mining

```python
import schedule

# Set up automated mining every 2 hours
schedule.every(2).hours.do(
    lambda: digger.launch_full_mining_expedition(top_n=20, days=1)
)
```

## 📁 Database Schema

### Core Tables

| Table | Purpose | Key Features |
|-------|---------|--------------|
| `gold_nuggets` | Main trading data | OHLCV + 20+ technical indicators |
| `volume_jackpots` | Breakout events | Volume multipliers, price impacts |
| `utility_treasure_map` | Fundamental metrics | GitHub activity, social buzz, dev metrics |
| `ml_feature_vault` | ML-ready vectors | JSON feature sets + targets |

### Sample Data Structure

```sql
SELECT symbol, timestamp, volume_breakout_score, rsi, macd 
FROM gold_nuggets 
WHERE volume_breakout_score > 70 
ORDER BY timestamp DESC;
```

## 🔥 Volume Breakout Algorithm

The heart of Gold-Digger's intelligence:

```python
# Volume Jackpot Scoring (0-100)
if volume > 5 * volume_ma_20:
    score = 100  # MEGA JACKPOT! 🎰
elif volume > 3 * volume_ma_20:
    score = 85   # BIG JACKPOT! 💰
elif volume > 2 * volume_ma_20:
    score = 70   # MINI JACKPOT! 🎯
else:
    score = volume_ratio * 40  # Building momentum...
```

## 🎯 ML Training Integration

### Feature Engineering

```python
features = {
    'price_momentum_5': recent_price_changes,
    'volume_trend_10': volume_pattern_analysis,
    'rsi_current': momentum_indicator,
    'bb_position': volatility_position,
    'volume_breakout_score': breakout_probability
}
```

### Prediction Targets

- `target_breakout_1h`: Volume breakout in next hour
- `target_breakout_24h`: Volume breakout in next 24h  
- `target_price_change_1h`: Price movement correlation
- `target_price_change_24h`: Extended price impact

## 🏃‍♂️ Quick Start Examples

### 1. Basic Data Collection

```python
# Mine Bitcoin data for the last 7 days
digger = GoldDigger()
digger.strike_gold_for_symbol('BTC/USDT', days=7)
```

### 2. Volume Breakout Hunting

```python
# Find recent volume jackpots
jackpots = digger.detect_volume_jackpots(df, 'ETH/USDT')
for jackpot in jackpots:
    print(f"💥 {jackpot['symbol']} - {jackpot['jackpot_type']}")
```

### 3. ML Model Training

```python
# Get processed features for model training
features_df = digger.get_ml_features(days=30)
X = features_df.drop(['target_breakout_1h'], axis=1)
y = features_df['target_breakout_1h']

# Train your model
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier()
model.fit(X, y)
```

## 🎪 Sample Output

```
⛏️ Digging for digital gold in the crypto mines...
🚀 GOLD-DIGGER EXPEDITION #1 LAUNCHED!
🎯 Target: Top 30 crypto veins, 30 days deep!
⭐ Found 30 golden symbols ready for mining!
💥 BOOM! Volume just went nuclear! ☢️
🏦 Deposited 1440 golden nuggets! Vault total: 43200
🏆 EXPEDITION COMPLETE! Success rate: 96.7%
💎 Total nuggets in vault: 43200
```

## 🤝 Contributing

We welcome fellow gold miners! 

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📈 Supported Exchanges

| Exchange | Status | Volume Data | Real-time |
|----------|--------|-------------|-----------|
| Binance | ✅ | ✅ | ✅ |
| Kraken | ✅ | ✅ | ✅ |
| Crypto.com | ✅ | ✅ | ✅ |
| OKX | ✅ | ✅ | ✅ |
| Bitfinex | ✅ | ✅ | ✅ |
| Coinbase Pro | ✅ | ✅ | ✅ |

## ⚠️ Disclaimer

This tool is for educational and research purposes. Always do your own research before making trading decisions. Cryptocurrency trading involves substantial risk of loss.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [CCXT](https://github.com/ccxt/ccxt) for exchange connectivity
- [TA-Lib](https://github.com/bukosabino/ta) for technical analysis
- The crypto community for inspiration

---

<p align="center">
  <b>Made with 💰 by crypto enthusiasts, for crypto enthusiasts</b><br>
  <i>Strike digital gold with every data point! ⛏️💎</i>
</p>

## 📞 Support

- 🐛 Issues: [GitHub Issues](https://github.com/xtoor/gold-digger/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/xtoor/gold-digger/discussions)
- ⭐ Star this repo if Gold-Digger helps you strike it rich!

**Happy Mining! 🚀💰**
