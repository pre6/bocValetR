# bocValetR
bocValetR is a lightweight R wrapper for the Bank of Canada Valet API that makes it easy to access, tidy, and analyze Canadian financial and economic time series data.


# Project Overview

This project builds bocValetR, a lightweight R wrapper for the Bank of Canada Valet API. The Valet API provides programmatic access to thousands of Canadian and global financial and economic time series, including exchange rates, interest rates, inflation, bond yields, and other macroeconomic indicators used in research, forecasting, and policy analysis.

The goal of this package is to make Bank of Canada data easy to discover, download, and analyze directly from R using tidy, user-friendly functions.

# What This Package Will Do

The package will implement a small but complete API client for the Valet service. The core functionality will include:

## 1. Data Discovery

Functions to explore what data is available in the Valet system.

boc_list_series()
Lists all available individual time series, including their IDs, labels, descriptions, frequencies, and units.

boc_list_groups()
Lists all available groups, which are curated collections of related time series (e.g. exchange rates, inflation indicators, interest rates).

These functions allow users to discover datasets without leaving R.

## 2. Data Retrieval

Functions to download actual time series observations.

boc_get_series(series_id, start_date = NULL, end_date = NULL)
Downloads observations for a specific series ID (e.g. "FXUSDCAD" or "V39079") and returns a tidy data frame.

boc_get_group(group_name, start_date = NULL, end_date = NULL)
Downloads observations for all series contained in a group (e.g. "FX_RATES_DAILY").

Both functions will support optional date filtering and return data in a consistent tidy format.


## 3. Search & Convenience Helpers

Optional helper functions for usability:

boc_search_series(keyword)
Searches the series catalog by keyword (e.g. "inflation", "overnight rate").

boc_search_groups(keyword)
Searches available groups by keyword.
