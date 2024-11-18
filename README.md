# Carysil-PBI
We Are Looking For Dashboard where we can check our Financial Performance and various financial metrics to judge our business
Power Bi Report For carysil Project : <a href "https://github.com/bhargavmehta93/Carysil-PBI/blob/main/Carysil.pbix"</a>
Data : <a href "https://github.com/bhargavmehta93/Carysil-PBI/blob/main/Carysil%20OG%20DIM.xlsx"</a>
Power Bi Report PDF: <a href "https://github.com/bhargavmehta93/Carysil-PBI/blob/main/Carysil%20Project%20PDF.pdf"</a>
Power Bi Report Screenshort: <a href "https://github.com/bhargavmehta93/Carysil-PBI/blob/main/Carysil%20Project%20PDF.pdf"</a>
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
1.	Target Revenue = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Sales")*1.15
2.	Sales LY = CALCULATE([Sales], SAMEPERIODLASTYEAR(Date_Dim[Date].[Date]) )
3.	Sales % = ([Sales]-[Sales LY])/ [Sales LY]
4.	Sales = CALCULATE(SUM('P&L_Fct'[Values]),'P&L_Dim'[P&L_Main_Head]="Sales")
5.	ROE % = [Actual Total PAT]/[Total Equity]
6.	ROCE% = [EBIT]/([Total Equity]+[Total Debt])
7.	Rev CAGR % = ([Ending Rev]/[Begining Rev])^(1/5) -1
8.	PAT CAGR % = ([Ending PAT]/[Begining PAT])^(1/5)-1
9.	PAT % = [Actual Total PAT]/[Sales]
10.	No.of Share = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="No. Of Share")
11.	Interest % = (CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Interest"))/[Sales] 
12.	Gross Profit = [Sales]-[Actual Total COGS]
13.	GP % = [Gross Profit]/[Sales]
14.	Finacial Levrage = [Total Assets]/[Total Equity]
15.	EPS = [Actual Total PAT]/ [No.of Share]
16.	Ending Rev = (CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Sales",Date_Dim[Year]=2024))
17.	Ending PAT = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Net Profit +",Date_Dim[Year]=2024)
18.	Ending EBITDA = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head] = "Operating Profit", Date_Dim[Year] = 2024)
19.	EBITDA CAGR % = ([Ending EBITDA]/[Begining EBITDA])^(1/5)-1
20.	EBITDA % = [Actual Total EBITDA]/[Sales]
21.	EBIT = [Actual Total EBITDA]-[D&A]
22.	Dep % = (CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Depreciation"))/[Sales]
23.	D&A = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Depreciation")
24.	BVPS = [Total Equity]/ [No.of Share]
25.	Begining Rev = CALCULATE(SUM(BS_Fct[Value]), 'P&L_Fct'[P&L_Main_Head]="Sales",Date_Dim[Year]=2019)
26.	Begining PAT = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Net Profit +",Date_Dim[Year]=2019)
27.	Begining EBITDA = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head] = "Operating Profit", Date_Dim[Year] = 2019)
28.	Actual Value_PY = CALCULATE(SUM('P&L_Fct'[Values]),SAMEPERIODLASTYEAR(Date_Dim[Date].[Date]))
29.	Actual Value = CALCULATE(SUM('P&L_Fct'[Values]))
30	Actual Total PAT = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Net Profit +")
31.	Actual Total EBITDA = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="Operating Profit") 
32.	Actual Total COGS = CALCULATE(SUM('P&L_Fct'[Values]), 'P&L_Fct'[P&L_Main_Head]="COGS")
33.	% Change = DIVIDE(([Actual Value]-[Actual Value_PY]),ABS([Actual Value_PY]),0)

# #	Balance Sheet
1.	Working Capital = [Trade Receivables]+[Inventories]-[Trade Payables]
2.	Trade Receivables = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head]="Trade receivables")
3.	Trade Payables = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head] = "Trade Payables")
4.	Total Equity = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Group_Head] = "Equity")
5.	Total Debt = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head] = "Borrowings -")
6.	Total Assets = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head]="Total Assets")
7.	Inventories = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Node Head]= "Inventories")
8.	D/E = [Total Debt]/[Total Equity]
9.	Current Ratio = [Current assets]/ [Current Liabilities]
10.	Current Liabilities = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Group_Head] = "Current Liabilities")
11.	Current assets = CALCULATE(SUM(BS_Fct[Value]), BS_Dim[BS_Group_Head] = "Current Assets")
12.	Assets Turnover = [Sales]/[Total Assets]

# # cash Flow
1.	FCF = [CFO]+[CAPEX]
2.	FCF = [CFO]+[CAPEX]
3.	CFO = CALCULATE(SUM(CFS_Fct[Value]), CFS_Fct[CFS_Sub Head]="Cash from Operating Activity -")
4.	CAPEX = CALCULATE(SUM(CFS_Fct[Value]), CFS_Fct[CFS_Sub Head]="Fixed assets purchased")





