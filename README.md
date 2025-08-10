# Pokémon API Automation Scripts

This project contains a collection of Bash scripts that interact with the [PokéAPI](https://pokeapi.co/) to fetch, process, and report Pokémon data.  
It uses tools such as `curl`, `jq`, `awk`, and `sed` to retrieve and format data.

---

## **Task 0 – Fetch Single Pokémon Data**
- Fetches data for a single Pokémon (`Pikachu`) from the API.  
- Saves the response to `data.json`.  
- Logs errors to `errors.txt` if the request fails.

---

## **Task 1 – Extract & Format Pokémon Details**
- Reads `data.json` and extracts **name**, **type**, **height**, and **weight**.  
- Converts units (height in meters, weight in kilograms).  
- Formats output: Pikachu is of type Electric, weighs 6.0kg, and is 0.4m tall.

---

## **Task 2 – Fetch Multiple Pokémon**
- Loops through a list of Pokémon: Bulbasaur, Ivysaur, Venusaur, Charmander, Charmeleon
- Saves each Pokémon’s data to a separate file in `pokemon_data/`.  
- Adds a delay between requests to prevent rate-limiting.

---

## **Task 3 – Generate CSV Report**
- Reads all JSON files in `pokemon_data/`.  
- Extracts **name**, **height (m)**, and **weight (kg)**.  
- Generates `pokemon_report.csv`.  
- Uses `awk` to calculate average height and weight.

---

## **Task 4 – Add Retry Logic**
- Enhances fetching scripts with retry mechanism (up to 3 attempts).  
- Skips Pokémon if all retries fail and logs errors to `errors.txt`.

---

## **Task 5 – Parallel Data Fetching**
- Fetches multiple Pokémon **in parallel** using background processes (`&`).  
- Uses `wait` to ensure all processes finish before moving on.  
- Improves speed compared to sequential fetching.

---

### **Requirements**
- `bash`, `curl`, `jq`, `awk`, `sed` installed.  
- Internet connection to access the PokéAPI.


