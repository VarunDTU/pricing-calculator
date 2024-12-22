# Profitability Calculator

## Overview
This is currently a front-end application that calculates various fees and profitability metrics for transactions. We aim to extend it into a full-stack solution with an API backend.

## Explanation of business terms:

Product Category: Determines referral fee percentage and category-specific requirements
Selling Price: Your listing price, including GST
Weight: Actual product weight, affects shipping costs
Shipping Mode:

Easy Ship: Amazon picks up and delivers, you store
FBA: Amazon stores and ships

Service Level:

Standard: Regular delivery timeline
Express: Faster delivery, higher fees

Product Size:

Standard: Normal sized items
Oversize: Larger items with special handling

Location:

Local: Within city delivery
National: Pan-India delivery

These factors combine to determine your total Amazon fees and potential profits.


## Current Features
- Interactive pricing calculator
- Fee structure visualization
- Detailed cost breakdown
- Static fee calculations


## Proposed API Extension

### Goals(Achieved)
- Create a backend API to manage fee structures
- Integration with the given spreadsheet data(See below)
- Dynamic fee calculation(From the api)

### API Endpoints
```http
POST /api/v1/profitability-calculator
```

## Extending the Project

How to run

1. Clone the repository
2. Install dependencies: `npm install`
3. Add an .env file following the .example.env file given
4. Run development server: `npm run dev`

## API Documentation

### Calculate Profitability
http
POST /api/v1/profitability-calculator
Content-Type: application/json

Response:
```
json
{
 
"referralFee": 10,
"weightHandlingFee": 10.0,
"closingFee": 5.0,
"pickAndPackFee": 20
"totalFees": 45,
"netEarnings": 200
}
```