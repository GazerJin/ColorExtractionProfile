# Color Extraction Profile - YouTube Thumbnail Analysis Project

A comprehensive analysis system for extracting and analyzing color profiles from YouTube video thumbnails, including text extraction, clustering, and correlational analysis with engagement metrics [Color and Text].

## 📋 Project Overview

This project performs an analysis of YouTube video thumbnails to understand the relationship between visual elements (colors, text) and video engagement metrics (views, likes, comments, subscribers). The system includes:

- **Color Extraction**: Dominant color analysis using predefined color profiles
- **Text Extraction**: OCR-based text detection and analysis
- **Clustering**: K-means clustering of thumbnails based on color profiles
- **Correlational Analysis**: Statistical analysis of color/text patterns vs. engagement metrics
- **Social Media Metrics**: YouTube API integration for engagement data extraction

## 🏗️ Project Structure

```
ColorExtractionProfile/
├── Data/
│   ├── cleaned.csv                           # Main dataset
│   ├── Color Cluster/                        # Color clustering results
│   ├── Correlation/                          # Correlational analysis outputs
│   ├── Text Cluster/                         # Text clustering results
│   └── Failed Extraction (Video ID)/         # Error logs
├── Notebooks/
│   ├── Color Extraction/                     # Color analysis notebooks
│   ├── Text Extraction/                      # Text analysis notebooks
│   ├── Correlational Analysis (Color and Text)/ # Statistical analysis
│   ├── Pixel Checker/                        # Image analysis tools
│   └── Suscribers and Video Engagement Extraction/ # YouTube API integration
├── Pictures/                                 # Generated visualizations
└── Cluster thumbnails/                       # Thumbnail samples by cluster
```

## 🚀 Installation & Setup

### Prerequisites
- Python 3.7+
- Jupyter Notebook or JupyterLab

### Required Dependencies

```bash
# Core image processing and analysis
pip install opencv-python scikit-learn numpy pandas matplotlib

# Data handling
pip install openpyxl

# File operations
pip install gdown

# Web scraping and API
pip install requests beautifulsoup4 selenium

# YouTube API
pip install google-api-python-client

# Additional utilities
pip install seaborn plotly
```

## 📚 Notebook Descriptions

### Color Extraction Notebooks

#### `Color_Extraction.ipynb`
- **Purpose**: Main color extraction using predefined color profiles
- **Features**: 
  - Fast color proportion calculation
  - Predefined color palette (Yellow, Orange, Red, Violet, Blue, Green, Black, White, Brown)
  - Vectorized distance calculations for performance
  - Color proportion visualization

#### `Color_Dominant_Extraction.ipynb`
- **Purpose**: Extract top N dominant colors from thumbnails
- **Features**: K-means clustering for dominant color identification

#### `Color_Extraction_DLSU.ipynb`
- **Purpose**: Chronological development and testing of color extraction methods
- **Features**: Iterative improvements and algorithm testing

#### `clustering_v2.ipynb`
- **Purpose**: Advanced clustering algorithms for thumbnail grouping
- **Features**: Multiple clustering approaches and evaluation metrics

### Text Analysis Notebooks

#### `Text_grid_pic.ipynb`
- **Purpose**: OCR-based text extraction from thumbnails
- **Features**: Text detection, extraction, and analysis

### Correlational Analysis Notebooks

#### `Correlation_Analysis_Color.ipynb`
- **Purpose**: Statistical analysis of color patterns vs. engagement metrics
- **Features**: Correlation coefficients, statistical significance testing

#### `Correlation_Analysis_Text.ipynb`
- **Purpose**: Analysis of text patterns vs. engagement metrics
- **Features**: Text-based correlation analysis

### Utility Notebooks

#### `pixel_checker.ipynb`
- **Purpose**: Analyze pixel distribution in color profiles
- **Features**: Pixel-level analysis and visualization

#### `Image_Diagram_Search.ipynb`
- **Purpose**: Search and analyze specific images within clusters
- **Features**: 
  - Image similarity search
  - Cluster centroid visualization
  - Thumbnail organization by clusters

#### `Social_Blade_Extract.ipynb`
- **Purpose**: YouTube API integration for engagement metrics
- **Features**:
  - View, like, and comment count extraction
  - Subscriber count analysis
  - Error handling and retry logic
  - IPv4/IPv6 compatibility fixes

## 🔧 Usage Instructions

### 1. Data Preparation
- Ensure your dataset is in the `Data/` directory
- Update file paths in notebooks as needed
- Modify thumbnail paths according to your setup

### 2. Running Analysis

#### Color Extraction
1. Open `Notebooks/Color Extraction/Color_Extraction.ipynb`
2. Update the image path variable
3. Run cells sequentially
4. Results will be saved to `Data/Color Cluster/`

#### Text Analysis
1. Open `Notebooks/Text Extraction/Text_grid_pic.ipynb`
2. Configure OCR settings
3. Process thumbnails for text extraction

#### Engagement Metrics
1. Open `Notebooks/Suscribers and Video Engagement Extraction/Social_Blade_Extract.ipynb`
2. Add your YouTube API key
3. Run the extraction process

#### Correlational Analysis
1. Open correlation analysis notebooks
2. Ensure all required data files are present
3. Run statistical analysis

### 3. Output Interpretation
- **Color Clusters**: Thumbnails grouped by similar color profiles
- **Correlation Results**: Statistical relationships between visual elements and engagement
- **Visualizations**: Charts and graphs in `Pictures/` directory

## 📊 Key Features

### Color Analysis
- **Predefined Color Profiles**: 9 basic colors for consistent analysis
- **Fast Processing**: Vectorized calculations for large datasets
- **Proportional Analysis**: Percentage-based color distribution
- **Clustering**: K-means clustering for pattern recognition

### Text Analysis
- **OCR Integration**: Optical Character Recognition for text extraction
- **Text Pattern Analysis**: Statistical analysis of text elements
- **Grid-based Processing**: Systematic thumbnail analysis

### Statistical Analysis
- **Correlation Coefficients**: Pearson, Spearman correlations
- **Outlier Detection**: Statistical outlier identification
- **Weighted Analysis**: Channel-weighted statistical measures
- **Visualization**: Comprehensive plotting and charting

### API Integration
- **YouTube Data API**: Official API for engagement metrics
- **Error Handling**: Robust error management and retry logic
- **Rate Limiting**: Respectful API usage with delays
- **IPv4/IPv6 Compatibility**: Network compatibility fixes

## 🎯 Research Applications

This project is designed for:
- **Content Creator Analysis**: Understanding successful thumbnail patterns
- **Marketing Research**: Color psychology in video marketing
- **Data Science Education**: Practical application of clustering and correlation
- **Academic Research**: Media studies and digital content analysis

## ⚠️ Important Notes

### Configuration Requirements
- **File Paths**: Update file names and paths in notebooks before running
- **API Keys**: Add your YouTube API key for engagement data extraction
- **Thumbnail Paths**: Ensure correct thumbnail directory paths

### Performance Considerations
- **Large Datasets**: Use appropriate batch sizes for large thumbnail collections
- **API Limits**: Respect YouTube API rate limits
- **Memory Usage**: Monitor memory usage for large image processing tasks

### Error Handling
- **Failed Extractions**: Check `Data/Failed Extraction (Video ID)/` for error logs
- **API Errors**: Review error logs for API-related issues
- **Processing Errors**: Monitor notebook outputs for processing issues

License

This project is developed for academic and research purposes. Please ensure compliance with YouTube's Terms of Service when using the API.

