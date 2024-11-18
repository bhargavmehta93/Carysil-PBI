# Carysil-PBI
We Are Looking For Dashboard where we can check our Financial Performance and various financial metrics to judge our business

# Carysil Financial Analysis
Understanding The Business
Understand the Data First To Understand the Business in Better Way….Excel

# # Data Preparation
1. Data Arrangement : Dimension & Fact able
• P&L=INDEX('Profit & Loss'!$A$4:$L$20,MATCH('P&L Fact'!C2,'Profit & Loss'!$A$4:$A$20,0),MATCH('P&L Fact'!E2,'Profit & Loss'!$A$4:$L$4,0))
• BS=INDEX('Balance Sheet'!$A$3:$L$36,MATCH('BS Fact'!E2,'Balance Sheet'!$A$3:$A$36,0),MATCH('BS Fact'!G2,'Balance Sheet'!$A$3:$L$3,0))
2. Data Modelling : Relationship Development for Insight

# # Client Requirement 
We Are Looking For Dashboard where we can check our Financial Performance and various financial metrics to judge our business
1.	Financial Statement Data Arrangement
2.	Financial Performance & Analysis
3.	Ratio Analysis

# # Financial Performance Analysis
1.	Overall Sales, Gross, Profit, EBITDA, PAT
2.	Growth YoY Change
3.	Assets Distribution & Common Sizing of Balance Sheet
4.	Profitability Flow
5.	Sales Trend with Rev Change
6.	Trend of Efficiency Metrics
7.	Margin Analysis & Revenue Bifurcation

# # Statement Analysis
1.	P&L Statement
2.	P&L Breakup
3.	CAGR % with Trend
4.	Target Sales Metrics
5.	Comparison GP Vs PAT
6.	Dept & Interest % of Sales
7.	Cost Breakup

# # Balance Sheet Visuals
1.	Balance Sheet Visuals
2.	Assets Breakup & Liabilities Breakup
3.	Balance Sheet Health
4.	Balance Sheet Deep Insight

# # Cash Flow Statement Analysis
1.	CFS Visuals
2.	CFO/EBITDA Trend
3.	Free Cash Flow Trend


# Used Chart
•	Slicer
•	Visual card
•	100% Stacked Bar Chart
•	Funnel Chart
•	Line And Clustered Column Chart
•	Line Chart
•	Donut Chart
•	Matrix
•	Treemap Chart
•	Gauge Chart
•	Clustered Column Chart
•	 Stacked Area Chart

# DAX
# # Profit & Loss
•	Target Revenue = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Sales")*1.15
•	Sales LY = CALCULATE([Sales], SAMEPERIODLASTYEAR(Date_Dim[Date].[Date]) )
•	Sales % = ([Sales]-[Sales LY])/ [Sales LY]
•	Sales = CALCULATE(SUM('P&L_Fct'[Values]),'P&L_Dim'[P&L_Main_Head]="Sales")
•	ROE % = [Actual Total PAT]/[Total Equity]
•	ROCE% = [EBIT]/([Total Equity]+[Total Debt])
•	Rev CAGR % = ([Ending Rev]/[Begining Rev])^(1/5) -1
•	PAT CAGR % = ([Ending PAT]/[Begining PAT])^(1/5)-1
•	PAT % = [Actual Total PAT]/[Sales]
•	No.of Share = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="No. Of Share")
•	Interest % = (CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Interest"))/[Sales] 
•	Gross Profit = [Sales]-[Actual Total COGS]
•	GP % = [Gross Profit]/[Sales]
•	Finacial Levrage = [Total Assets]/[Total Equity]
•	EPS = [Actual Total PAT]/ [No.of Share]
•	Ending Rev = (CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Sales",Date_Dim[Year]=2024))
•	Ending PAT = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Net Profit +",Date_Dim[Year]=2024)
•	Ending EBITDA = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head] = "Operating Profit", Date_Dim[Year] = 2024)
•	EBITDA CAGR % = ([Ending EBITDA]/[Begining EBITDA])^(1/5)-1
•	EBITDA % = [Actual Total EBITDA]/[Sales]
•	EBIT = [Actual Total EBITDA]-[D&A]
•	Dep % = (CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Depreciation"))/[Sales]
•	D&A = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Depreciation")
•	BVPS = [Total Equity]/ [No.of Share]
•	Begining Rev = CALCULATE(SUM(BS_Fct[Value]), 'P&L_Fct'[P&L_Main_Head]="Sales",Date_Dim[Year]=2019)
•	Begining PAT = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Net Profit +",Date_Dim[Year]=2019)
•	Begining EBITDA = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head] = "Operating Profit", Date_Dim[Year] = 2019)
•	Actual Value_PY = CALCULATE(SUM('P&L_Fct'[Values]),SAMEPERIODLASTYEAR(Date_Dim[Date].[Date]))
•	Actual Value = CALCULATE(SUM('P&L_Fct'[Values]))
•	Actual Total PAT = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Net Profit +")
•	Actual Total EBITDA = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Operating Profit") 
•	Actual Total COGS = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="COGS")
•	% Change = DIVIDE(([Actual Value]-[Actual Value_PY]),ABS([Actual Value_PY]),0)

# #	Balance Sheet
•	Working Capital = [Trade Receivables]+[Inventories]-[Trade Payables]
•	Trade Receivables = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head]="Trade receivables")
•	Trade Payables = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head] = "Trade Payables")
•	Total Equity = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Group_Head] = "Equity")
•	Total Debt = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head] = "Borrowings -")
•	Total Assets = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head]="Total Assets")
•	Inventories = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head]= "Inventories")
•	D/E = [Total Debt]/[Total Equity]
•	Current Ratio = [Current assets]/ [Current Liabilities]
•	Current Liabilities = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Group_Head] = "Current Liabilities")
•	Current assets = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Group_Head] = "Current Assets")
•	Assets Turnover = [Sales]/[Total Assets]

# # cash Flow
•	FCF = [CFO]+[CAPEX]
•	FCF = [CFO]+[CAPEX]
•	CFO = CALCULATE(SUM(CFS_Fct[Value]), CFS_Fct[CFS_Sub Head]="Cash from Operating Activity -")
•	CAPEX = CALCULATE(SUM(CFS_Fct[Value]), CFS_Fct[CFS_Sub Head]="Fixed assets purchased")





