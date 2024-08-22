This project involves the analysis of Apple's 10-K filings, focusing on Items 1A and 7 to extract summaries, sentiment, polarity, and readability. Additionally, financial data is used to compare various factors such as gross profit, revenue, return on equity (ROE), regional sales, and revenue by productivity.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Sources](#data-sources)
3. [Requirements](#requirements)
4. [Data Processing](#data-processing)
5. [Analysis](#analysis)
   - [Text Analysis](#text-analysis)
   - [Financial Data Comparison](#financial-data-comparison)
6. [Results](#results)
7. [Usage](#usage)
8. [Contributing](#contributing)
9. [License](#license)



## Project Overview


The goal of this project is to analyze Apple's 10-K filings over multiple years, specifically focusing on the following:

1. **Summarization**: Extracting key information from Item 1A (Risk Factors) and Item 7 (Management's Discussion and Analysis).
2. **Sentiment Analysis**: Assessing the sentiment (e.g., positive, negative, neutral) of the summarized text.
3. **Polarity and Subjectivity**: 
   1. **Polarity**: Measuring the degree of positivity or negativity in the text.
   2. **Subjectivity**: Evaluating the degree to which the text expresses personal opinions or factual information.
4. **Readability**: Evaluating the readability of the text using various indices.
5. **Financial Data Comparison**: Analyzing and comparing key financial metrics such as gross profit, revenue, ROE, regional sales, and productivity.
6. **Q and A Pipeline**:analzed the textual text and got the reason why decline in revenue was seen from 2022 to 2023





## Data Sources

- **Apple's 10-K Filings**: The primary data source for the text and financial data is Apple's 10-K filings, which are available on the SEC EDGAR database for 5 years.

**Items Analyzed:**
- Item 1A: Risk Factors
- Item 7: Management's Discussion and Analysis

## Requirements

To run the analysis, the following libraries and tools are required:

- Python 3.7+
- `pandas`
- `numpy`
- `re` (Regular Expressions)
- `nltk` (Natural Language Toolkit)
- `sumy` (Text Summarization)
- `transformers` (Hugging Face's Transformer Models)
- `textblob`
- `spacy`
- `textstat`


-Install the necessary libraries using pip:

-```bash
pip install pandas numpy nltk sumy transformers textblob spacy textstat
python -m spacy download en_core_web_sm

## Results

The analysis of Apple's 10-K filings provides detailed insights into the company's performance and management discussions over several years. The following sections summarize the key findings based on the data:

### Item 1A: Risk Factors

1. **2023**
   - **Summary**: While these arrangements can lower operating costs...
   - **Sentiment**: Neutral
   - **Polarity**: 0.067
   - **Subjectivity**: 0.400
   - **Readability**: 15.31 (Flesch Reading Ease)
   - **Sentiment Confidence**: 0.991
   - **Factors Contributing to Revenue Decline**: Lower net sales of laptops.

2. **2022**
   - **Summary**: In addition to an adverse impact on demand for...
   - **Sentiment**: Negative
   - **Polarity**: 0.052
   - **Subjectivity**: 0.388
   - **Readability**: NaN
   - **Sentiment Confidence**: 0.767
   - **Factors Influencing Revenue**: Higher net sales of iPhone, Services, and Mac. The weakness in foreign currencies.

3. **2021**
   - **Summary**: Apple Inc. | 2021 Form 10-K | 6 In addition to...
   - **Sentiment**: Negative
   - **Polarity**: 0.061
   - **Subjectivity**: 0.367
   - **Readability**: NaN
   - **Sentiment Confidence**: 0.993

4. **2020**
   - **Summary**: Because of the following factors, as well as...
   - **Sentiment**: Neutral
   - **Polarity**: 0.029
   - **Subjectivity**: 0.283
   - **Readability**: {'Flesch Reading Ease': 15.85, 'Flesch-Kincaid Grade': 10.47}
   - **Sentiment Confidence**: 0.993

5. **2019**
   - **Summary**: Because of the following factors, as well as...
   - **Sentiment**: Negative
   - **Polarity**: 0.048
   - **Subjectivity**: 0.295
   - **Readability**: {'Flesch Reading Ease': 13.41, 'Flesch-Kincaid Grade': 13.57}
   - **Sentiment Confidence**: 0.999

### Item 7: Management's Discussion and Analysis

1. **2023**
   - **Summary**: The weakness in foreign currencies relative to...
   - **Sentiment**: Neutral
   - **Polarity**: 0.065
   - **Subjectivity**: 0.336
   - **Readability**: 37.03 (Flesch Reading Ease)
   - **Sentiment Confidence**: 0.996

2. **2022**
   - **Summary**: Second Quarter 2022: • Updated iPhone SE with...
   - **Sentiment**: Neutral
   - **Polarity**: 0.018
   - **Subjectivity**: 0.313
   - **Readability**: NaN
   - **Sentiment Confidence**: 1.000

3. **2021**
   - **Summary**: Refer to Part I, Item 1A of this Form 10-K und...
   - **Sentiment**: Positive
   - **Polarity**: 0.087
   - **Subjectivity**: 0.375
   - **Readability**: NaN
   - **Sentiment Confidence**: 0.952

4. **2020**
   - **Summary**: Fiscal Year Highlights COVID-19 Update COVID-1...
   - **Sentiment**: Neutral
   - **Polarity**: -0.001
   - **Subjectivity**: 0.322
   - **Readability**: {'Flesch Reading Ease': 33.44, 'Flesch-Kincaid Grade': 8.24}
   - **Sentiment Confidence**: 0.987

5. **2019**
   - **Summary**: Rest of Asia Pacific includes Australia and th...
   - **Sentiment**: Negative
   - **Polarity**: -0.073
   - **Subjectivity**: 0.251
   - **Readability**: {'Flesch Reading Ease': 33.85, 'Flesch-Kincaid Grade': 12.87}
   - **Sentiment Confidence**: 0.752

## Key Observations

- **Factors Influencing Revenue**:
  - **2022**: Higher net sales of iPhone, Services, and Mac, along with the weakness in foreign currencies.
  - **2023**: Decline in revenue primarily due to lower net sales of laptops.

- **Sentiment Trends**: Over the years, the sentiment of Item 1A has varied from neutral to negative, reflecting potential risks and challenges. In contrast, Item 7 has shown a mix of neutral and positive sentiments, indicating management's discussion and strategies.

- **Polarity and Subjectivity**: The polarity and subjectivity scores for Item 1A and Item 7 provide insights into the emotional tone and opinion level of the text. Higher polarity values indicate more positive content, while higher subjectivity suggests more opinion-based content.

- **Readability**: The readability scores indicate how accessible the text is to the general public. Lower scores suggest more complex text, while higher scores indicate simpler, more readable content.

These results offer valuable insights into the evolving risk factors, management's perspective, and overall readability of Apple's 10-K filings over the years.



