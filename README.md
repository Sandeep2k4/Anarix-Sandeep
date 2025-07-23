# Analytics 🚀

**Advanced Business Intelligence & Data Analytics Platform**

A comprehensive Python-based business intelligence system that transforms retail data into actionable insights using natural language queries, AI-powered analysis, and interactive visualizations.

## 🌟 Features

### 📊 **Core Analytics Engine**
- **Multi-Dataset Integration**: Seamlessly combines advertising metrics, revenue data, and product catalog information
- **SQLite Data Warehouse**: In-memory database for optimized query performance
- **Business Intelligence Queries**: Transform complex business questions into SQL automatically

### 🤖 **AI-Powered Query Processing**
- **Natural Language Interface**: Ask questions in plain English like "What is my total revenue?"
- **Gemini AI Integration**: Leverages Google's Gemini AI for intelligent SQL generation
- **Smart Fallback System**: Handles queries even when AI is unavailable

### 📈 **Interactive Visualizations**
- **Executive Dashboard**: Comprehensive performance metrics visualization
- **Cost Efficiency Analysis**: Track advertising spend effectiveness
- **Revenue Performance Charts**: Monitor ROI and sales correlations
- **Product Eligibility Insights**: Understand promotional campaign readiness

### 💻 **Multiple User Interfaces**
- **Interactive Dashboard**: Widget-based interface for Jupyter/Colab environments
- **Console Interface**: Text-based interaction for any Python environment
- **Quick Query Functions**: Single-line commands for rapid analysis

## 📋 Prerequisites

### Required Python Packages
```bash
pip install pandas google-generativeai sqlalchemy matplotlib seaborn plotly numpy ipywidgets
```

### Data Requirements
The system expects three CSV files with the following naming pattern:
1. **Advertising Data**: `Product-Level Ad Sales and Metrics (mapped) - Product-Level Ad Sales and Metrics (mapped).csv`
2. **Revenue Data**: `Product-Level Total Sales and Metrics (mapped) - Product-Level Total Sales and Metrics (mapped).csv`
3. **Product Catalog**: `Product-Level Eligibility Table (mapped) - Product-Level Eligibility Table (mapped).csv`

### API Configuration
- **Gemini API Key**: Required for AI-powered query processing
- Set up in Google Colab Secrets as `GEMINI_API_KEY`

## 🚀 Quick Start

### 1. **Data Setup**
```python
# Update file paths in the script to match your data files
advertising_data_path = 'your_advertising_data.csv'
revenue_data_path = 'your_revenue_data.csv'
product_status_path = 'your_product_catalog.csv'
```

### 2. **Launch Interactive Interface**
```python
# Start the main dashboard
launch_interface()
```

### 3. **Alternative Interfaces**
```python
# Console-based interface
console_interface()

# Quick single questions
ask_quick_question("What is my total revenue?")

# Generate visualizations
create_quick_dashboard()
```

## 💡 Sample Business Questions

### 💰 **Revenue & Sales Analysis**
- "What is the total revenue across all products?"
- "Which products generate the most revenue?"
- "Show me the top 5 products by total sales"
- "What is the average revenue per product?"

### 📈 **Marketing & Advertising Insights**
- "Calculate the overall marketing return on investment"
- "Which product has the highest advertising spend?"
- "Show products with zero advertising clicks"
- "What is the average cost per click?"

### 🎯 **Performance Optimization**
- "Which products have the best conversion rates?"
- "Show me products with low click-through rates"
- "Find products with high impressions but low clicks"
- "What are the most expensive products to advertise?"

### 📊 **Operational Intelligence**
- "Show all products not eligible for promotional campaigns"
- "Find underperforming products that need attention"
- "What products need more marketing investment?"
- "Which products have the highest inventory turnover?"

## 🏗️ System Architecture

### **Data Layer**
- **CSV Ingestion**: Automated loading and validation of business data
- **SQLite Warehouse**: In-memory database with optimized schema
- **Data Quality Checks**: Comprehensive validation and error handling

### **Intelligence Layer**
- **AI Query Engine**: Natural language to SQL conversion
- **Business Logic**: Domain-specific query processing
- **Fallback Mechanisms**: Ensures system reliability

### **Presentation Layer**
- **Interactive Widgets**: Rich UI components for Jupyter environments
- **Visualization Engine**: Advanced matplotlib/seaborn charts
- **Multi-Format Output**: Tables, charts, and formatted insights

## 📊 Data Schema

### **Marketing Performance Table**
- `item_id`: Product identifier
- `date`: Transaction date
- `ad_spend`: Advertising investment
- `ad_sales`: Revenue from advertising
- `clicks`: Number of ad clicks
- `impressions`: Ad impression count

### **Revenue Analytics Table**
- `item_id`: Product identifier
- `date`: Transaction date
- `total_sales`: Total product revenue
- `units_sold`: Quantity sold
- `conversion_rate`: Sales conversion metrics

### **Product Intelligence Table**
- `item_id`: Product identifier
- `eligibility`: Promotional campaign eligibility (0/1)
- `eligibility_datetime_utc`: Eligibility status timestamp
- `category`: Product classification

## 🎨 Visualization Features

### **Performance Dashboard**
- **Revenue Distribution**: Top products by sales performance
- **ROI Analysis**: Marketing return on investment visualization
- **Cost Efficiency**: Advertising spend effectiveness charts
- **Eligibility Status**: Product promotional readiness distribution

### **Advanced Analytics**
- **Correlation Analysis**: Spend vs. sales relationship mapping
- **Trend Analysis**: Time-series performance tracking
- **Comparative Metrics**: Cross-product performance benchmarking

## 🔧 Configuration Options

### **File Path Updates**
```python
# Modify these paths to match your data files
advertising_data_path = 'path/to/your/advertising/data.csv'
revenue_data_path = 'path/to/your/revenue/data.csv'
product_status_path = 'path/to/your/product/catalog.csv'
```

### **AI Model Selection**
The system automatically selects the best available Gemini model:
- `gemini-1.5-flash` (preferred)
- `gemini-1.0-pro` (fallback)
- Automatic model discovery and selection

## 🚦 Usage Examples

### **Interactive Dashboard Usage**
1. Run `launch_interface()`
2. Enter questions in natural language
3. Click "🔍 Analyze" to process
4. Use dropdown for sample questions

### **Console Mode Usage**
```python
console_interface()
# Then type questions like:
# > What is my total revenue?
# > Show me top 5 products by sales
# > help (for guidance)
# > quit (to exit)
```

### **Programmatic Usage**
```python
# Direct query processing
result = query_engine.process_business_query("What is my marketing ROI?")
print(result)

# Quick visualization
create_quick_dashboard()

# Display examples
display_sample_questions()
```

## 🛠️ Troubleshooting

### **Common Issues**

**Data Loading Errors**
- Verify CSV file names match exactly
- Ensure files are uploaded to your environment
- Check file encoding (UTF-8 recommended)

**AI Query Failures**
- Verify Gemini API key is properly configured
- Check internet connectivity
- System falls back to predefined queries automatically

**Visualization Problems**
- Ensure matplotlib and seaborn are properly installed
- Check that data exists in the warehouse tables
- Verify sufficient data for meaningful charts

**Widget Interface Issues**
- ipywidgets may not be available in all environments
- System automatically falls back to console interface
- Use `console_interface()` as alternative

## 🔐 Security & Privacy

- **In-Memory Processing**: Data remains in session memory
- **No Persistent Storage**: No data written to permanent storage
- **API Key Protection**: Secure handling of Gemini API credentials
- **Local Processing**: Business logic runs entirely in your environment

## 🤝 Contributing

This is a business intelligence tool designed for retail analytics. For customization:

1. **Data Schema Modifications**: Update table structures in `setup_data_warehouse()`
2. **Query Extensions**: Add new business logic in `RetailPulseQueryEngine`
3. **Visualization Enhancements**: Extend `RetailPulseVisualizer` class
4. **UI Improvements**: Modify `RetailPulseUserInterface` components

## 📝 License

This project is designed for business intelligence and analytics use cases. Please ensure compliance with your organization's data handling policies.

## 🆘 Support

For technical issues:
1. Check data file formats and naming
2. Verify API key configuration
3. Review console output for error messages
4. Use fallback interfaces if widgets fail

---

**RetailPulse Analytics** - Transforming retail data into business intelligence through advanced analytics and AI-powered insights. 🚀📊
