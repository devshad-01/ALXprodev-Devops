# Advanced Shell Scripting - Pokémon API Automation

This project demonstrates advanced shell scripting techniques through automation of Pokémon API data retrieval and processing.

## Project Overview

This repository contains shell scripts that interact with the Pokémon API (https://pokeapi.co) to fetch, process, and analyze Pokémon data using various shell tools and techniques.

## Tasks Completed

### Task 0: API Request Automation (`apiAutomation-0x00`)
- **Objective**: Automate API requests to fetch Pikachu data
- **Features**:
  - Fetches data from Pokémon API for Pikachu
  - Saves response to `data.json`
  - Error handling with logging to `errors.txt`
  - JSON validation

**Usage**:
```bash
./apiAutomation-0x00
```

### Task 1: Extract Pokémon Data (`data_extraction_automation-0x01`)
- **Objective**: Extract specific data using advanced text manipulation tools
- **Features**:
  - Uses `jq`, `awk`, and `sed` for data extraction
  - Formats output in human-readable format
  - Converts units (decimeters to meters, hectograms to kilograms)

**Usage**:
```bash
./data_extraction_automation-0x01
```

**Expected Output**:
```
Pikachu is of type Electric, weighs 6kg, and is 0.4m tall.
```

### Task 2: Batch Pokémon Data Retrieval (`batchProcessing-0x02`)
- **Objective**: Retrieve data for multiple Pokémon
- **Features**:
  - Fetches data for: Bulbasaur, Ivysaur, Venusaur, Charmander, Charmeleon
  - Saves each Pokémon to separate JSON files
  - Rate limiting with delays between requests
  - Retry logic with error handling
  - Creates `pokemon_data/` directory structure

**Usage**:
```bash
./batchProcessing-0x02
```

### Task 3: Summarize Pokémon Data (`summaryData-0x03`)
- **Objective**: Generate reports and calculate statistics
- **Features**:
  - Reads all JSON files from Task 2
  - Generates CSV report with name, height, and weight
  - Calculates average height and weight using `awk`
  - Creates `pokemon_report.csv`

**Usage**:
```bash
./summaryData-0x03
```

**Expected Output**:
```
CSV Report generated at: pokemon_report.csv

Name,Height (m),Weight (kg)
Bulbasaur,0.7,6.9
Charmander,0.6,8.5
Charmeleon,1.1,19.0
Ivysaur,1.0,13.0
Venusaur,2.0,100.0

Average Height: 1.08 m
Average Weight: 29.48 kg
```

### Task 4: Parallel Data Fetching (`batchProcessing-0x04`)
- **Objective**: Speed up data retrieval using parallel processing
- **Features**:
  - Fetches multiple Pokémon data simultaneously
  - Uses background processes with proper process management
  - Waits for all processes to complete
  - Reports success/failure status for each fetch

**Usage**:
```bash
./batchProcessing-0x04
```

## File Structure

```
Advanced_shell/
├── README.md
├── apiAutomation-0x00              # Task 0: API automation
├── data_extraction_automation-0x01  # Task 1: Data extraction
├── batchProcessing-0x02             # Task 2: Batch processing
├── summaryData-0x03                 # Task 3: Data summarization
├── batchProcessing-0x04             # Task 4: Parallel processing
├── data.json                        # Pikachu data from Task 0
├── pokemon_report.csv               # CSV report from Task 3
├── pokemon_data/                    # Directory containing individual Pokémon JSON files
│   ├── bulbasaur.json
│   ├── ivysaur.json
│   ├── venusaur.json
│   ├── charmander.json
│   └── charmeleon.json
└── errors.txt                       # Error log file (created if errors occur)
```

## Requirements

- `curl` - for API requests
- `jq` - for JSON processing
- `bc` - for floating-point calculations
- `awk` - for text processing
- `sed` - for text manipulation

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/ALXprodev-Devops.git
cd ALXprodev-Devops/Advanced_shell
```

2. Make scripts executable:
```bash
chmod +x apiAutomation-0x00
chmod +x data_extraction_automation-0x01
chmod +x batchProcessing-0x02
chmod +x summaryData-0x03
chmod +x batchProcessing-0x04
```

3. Install required tools (Ubuntu/Debian):
```bash
sudo apt update
sudo apt install -y curl jq bc
```

## Usage Examples

Run all tasks in sequence:
```bash
# Task 0: Fetch Pikachu data
./apiAutomation-0x00

# Task 1: Extract and format Pikachu data
./data_extraction_automation-0x01

# Task 2: Fetch multiple Pokémon data
./batchProcessing-0x02

# Task 3: Generate summary report
./summaryData-0x03

# Task 4: Demonstrate parallel fetching
./batchProcessing-0x04
```

## Advanced Features

- **Error Handling**: Robust error handling with retry mechanisms
- **Rate Limiting**: Proper delays to respect API limits
- **Parallel Processing**: Background processes for improved performance
- **Data Validation**: JSON validation and integrity checks
- **Logging**: Error logging and status reporting
- **Unit Conversion**: Automatic conversion between metric units

## API Reference

This project uses the [PokéAPI](https://pokeapi.co/):
- Base URL: `https://pokeapi.co/api/v2/pokemon/`
- No authentication required
- Free and open API

## Author

ALX Software Engineering Program - Advanced Shell Scripting Project

## License

This project is part of the ALX Software Engineering curriculum.
