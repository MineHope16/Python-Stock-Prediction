# Changelog

All notable changes to the Stock Market Predictor project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.1.0] - 2026-04-01

### Added

- 📊 **Dropdown Stock Selector**: Replaced text input with a searchable dropdown containing 15 popular stocks (AAPL, MSFT, GOOG, AMZN, TSLA, NVDA, META, JPM, JNJ, V, PG, MA, COST, XOM, WMT)
- 🔍 **Search Functionality**: Users can now type to search/filter stocks quickly in the dropdown
- ✅ **Error Prevention**: Eliminates invalid stock symbol entries

### Changed

- UI/UX improvement: More user-friendly stock selection interface
- Better stock discovery for new users

### Benefits

- Faster stock selection for users
- Reduced errors from typos or invalid symbols
- Cleaner, more professional interface

---

## [1.0.1] - 2026-03-XX

### Fixed

- 🔧 **Critical Bug - Hardcoded Model Path**: Fixed hardcoded Windows path that prevented running on other machines
  - **Before**: `C:\Users\Administrator\Desktop\...Stock Predictions Model.keras`
  - **After**: Dynamic path using `os.path.join()` to load model from app directory
  - **Impact**: App is now portable and works on any machine

- ✏️ **Typo Fix**: Corrected "Stock Symnbol" → "Stock Symbol" in UI label

### Technical Details

- Model now loads from relative path: `Stock Predictions Model.keras` (same directory as `app.py`)
- Uses `os.path.dirname(__file__)` for cross-platform compatibility
- Works on Windows, Mac, and Linux

---

## [1.0.0] - 2026-03-XX

### Initial Release

- ✨ **Stock Market Predictor Application** using Streamlit
- 📈 Real-time stock data fetching via Yahoo Finance (yfinance)
- 🤖 Pre-trained Keras neural network for price predictions
- 📊 **Technical Analysis Charts**:
  - Price vs 50-Day Moving Average (MA50)
  - Price vs 50-Day & 100-Day Moving Averages (MA50 vs MA100)
  - Price vs 100-Day & 200-Day Moving Averages (MA100 vs MA200)
- 🎯 **Prediction Visualization**: Original vs Predicted prices comparison
- ⚡ Interactive interface for quick analysis

### Features

- Data range: 2013-01-01 to 2024-03-01
- Default stock: GOOG
- Automatic 80/20 train-test split
- MinMax scaling for data normalization
- Real-time chart updates

---

## Future Roadmap

### Planned for v1.2.0

- [ ] Custom date range selection
- [ ] Prediction accuracy metrics (RMSE, MAPE)
- [ ] Key metrics display (Current Price, % Change, Volume)
- [ ] Additional technical indicators (RSI, MACD, Bollinger Bands)

### Planned for v1.3.0

- [ ] Multi-stock comparison view
- [ ] Stock correlation analysis
- [ ] Future price forecasting (7-day, 30-day predictions)
- [ ] Export data to CSV
- [ ] Export charts as images

### Planned for v2.0.0

- [ ] Model retraining capability
- [ ] Custom model upload
- [ ] API integration for live predictions
- [ ] Historical prediction accuracy tracking
- [ ] User dashboard with saved favorites

---

## Installation & Usage

### Requirements

- Python 3.8+
- Dependencies listed in `requirements.txt`

### Quick Start

```bash
pip install -r requirements.txt
streamlit run app.py
```

### Stock Symbols

This version includes 15 popular stocks. Use the dropdown to select any of them.

---

## Known Issues

- None at this time

## Support

For issues or feature requests, please refer to the project repository.

---

**Last Updated**: April 1, 2026
