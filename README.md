# Development-of-Python-Code-with-Multiple-AI-Tools

## Name :MOENISH BAALAN G
## Register no: 212223220014

# Aim: 
Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

# AI Tools Required:

ChatGPT (GPT-5 or GPT-4) – for generating and explaining Python code.

Google Gemini / Bard – for comparing code logic and alternative API uses.

GitHub Copilot – for in-editor code suggestions and real-time debugging help.

Replit / Jupyter Notebook – for executing and testing AI-generated code.

Postman / RapidAPI – to explore and test API requests and responses.

# Explanation:

Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 

# Objective:

To design effective prompts that guide AI tools to generate Python programs, compare outputs from multiple APIs, and produce useful insights, improving the ability to communicate coding requirements to AI systems.

# Stage 1: Generate Python Code for Interacting with Multiple APIs

## Prompt:

Write a Python program that connects to two weather APIs — OpenWeatherMap and WeatherAPI. Fetch current temperature and humidity data for a given city, and print the results neatly.

## OUTPUT:

#### CODE BY CHATGPT

```
import requests

def get_coingecko_price():
    url = "https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd"
    data = requests.get(url).json()
    return data["bitcoin"]["usd"]

def get_coincap_price():
    url = "https://api.coincap.io/v2/assets/bitcoin"
    data = requests.get(url).json()
    return float(data["data"]["priceUsd"])

coingecko_price = get_coingecko_price()
coincap_price = get_coincap_price()

print(f"CoinGecko Bitcoin Price: ${coingecko_price}")
print(f"CoinCap Bitcoin Price: ${coincap_price}")

```

## AI Explanation:

The AI explained that this Python program uses the requests library to send HTTP requests to two cryptocurrency APIs.

The program:

Retrieves Bitcoin price data from CoinGecko.

Retrieves Bitcoin price data from CoinCap.

Extracts the USD price from the API response.

Prints both prices for comparison.

# Stage 2: Compare Outputs from Different APIs

## Prompt:

Modify the previous code so that it compares the temperature and humidity values from both APIs and highlights the differences clearly

## Output:

#### CODE BY GEMINI AI

```
temp_diff = abs(open_temp - weather_temp)
price_difference = abs(coingecko_price - coincap_price)

print(f"Price Difference: ${price_difference:.2f}")

if price_difference > 50:
    print("Noticeable difference between the APIs.")
else:
    print("Both APIs report similar Bitcoin prices.")

```

## AI Explanation:

Gemini AI suggested calculating the absolute difference between the two API prices.

The program checks if the difference exceeds a certain threshold and prints a message indicating whether the data from both APIs is consistent.

# Stage 3: Suggest Insights or Next Steps

## Prompt:

Based on the compared weather data, suggest how the program could automatically choose the more reliable API result and display an average value.

## Output:

#### CODE BY CLAUDE AI

```
average_price = (coingecko_price + coincap_price) / 2

print(f"Average Bitcoin Price: ${average_price:.2f}")

if price_difference > 100:
    print("Large variation detected. Consider checking API refresh times.")
else:
    print("Average price can be considered reliable for analysis.")

```

## AI Explanation:

Claude AI proposed calculating the average value of the Bitcoin price from both APIs.

This improves reliability because:

If both APIs give similar values, the average represents a more stable estimate.

If the difference is large, the program warns that the data may need verification.

# Reflection Note:

Initially, the prompts were short and vague, which resulted in incomplete or basic code.

After refining the prompts by including:

API names

Type of data required

Expected program output

the generated code became more accurate and structured.

This experiment shows that clear and specific prompts significantly improve AI-generated programming solutions.


# Conclusion:

This experiment demonstrates how multiple AI tools can collaborate in software development.

Each AI contributed differently:

ChatGPT generated the base Python program.

Gemini improved comparison logic.

Claude suggested analytical insights.

Using AI tools effectively allows students to:

Automate data collection from multiple APIs.

Compare and analyze results efficiently.

Improve coding productivity through better prompt engineering.

Prompt engineering plays an important role in guiding AI systems to produce meaningful and reliable outputs.

# Result: 

The corresponding prompt was executed successfully and the Python program was generated using multiple AI tools to retrieve, compare, and analyze cryptocurrency price data.
