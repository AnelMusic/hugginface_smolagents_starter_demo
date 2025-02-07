# hugginface_smolagents_starter_demo
# SmolagentsDemo - Appointment Scheduling Agent
A demonstration project showing how to use Smolagents to create a simple appointment scheduling system with AI agents.

## Overview
This project demonstrates the basic usage of Smolagents by implementing a medical appointment scheduling system. The example agent helps find an orthopedic specialist based on specific criteria such as insurance acceptance, availability, and specialization.

This is a starter project intended to showcase:
- How to set up and use Smolagents tools
- Basic agent implementation patterns
- Integration with HuggingFace models
- Proper error handling and logging in tools

## Features
The demo implements four tools that simulate a medical appointment system:

1. `get_orthopedic_specialists()`: Returns a list of available orthopedic specialists with their subspecialties
2. `get_doctor_specialty(doctor_name)`: Retrieves detailed specialty information for a specific doctor
3. `get_doctor_availability(doctor_name)`: Gets available appointment slots for a doctor (Mondays in February 2025, CET timezone)
4. `accepts_uninsured_patients(doctor_name)`: Checks if a doctor accepts uninsured patients

## Installation

### Prerequisites
- Python 3.8 or higher
- A HuggingFace account and API token

### Setting up the Environment

1. Clone the repository:
```bash
git clone https://github.com/yourusername/smolagents-demo.git
cd smolagents-demo
```

2. Create and activate a virtual environment:
```bash
# On Windows
python -m venv venv
.\venv\Scripts\activate

# On macOS/Linux
python -m venv venv
source venv/bin/activate
```

3. Install requirements:
```bash
pip install -r requirements.txt
```

### Configuration
1. Create a `.env` file in the project root:
```bash
touch .env
```

2. Add your HuggingFace token to the `.env` file:
```
HF_TOKEN=your_huggingface_token_here
```

## Usage
Run the script with:
```bash
python doctor_appointment_agent.py
```

The agent will attempt to find doctors matching these criteria:
1. Specializes in knee orthopedics
2. Accepts uninsured patients
3. Has availability for 30-minute appointments on Mondays between 8:00 - 12:00 CET
4. Can schedule appointments for February 2025

## Getting a HuggingFace Token
1. Create an account at [HuggingFace](https://huggingface.co/)
2. Go to your profile settings
3. Navigate to "Access Tokens"
4. Create a new token with read access
5. Copy the token to your `.env` file

## Project Structure
```
hugginface_smolagents_starter_demo/
├── doctor_appointment_agent.py   # Main script
├── requirements.txt             # Project dependencies
├── .env                        # Environment variables (create this)
└── README.md                   # This file
```

## Important Notes
- This is a demonstration project with simulated data
- The tools use hardcoded values for demonstration purposes
- In a real application, these would connect to actual databases or APIs
- The time slots are fixed to February 2025 for demonstration

## Contributing
This is a starter project meant for learning and demonstration. Feel free to fork and expand upon it for your own use cases.

## License
MIT

## Disclaimer
This is a demonstration project and should not be used in production environments without significant modifications. The appointment data and doctor information are simulated for educational purposes.

---

For more information about Smolagents, visit the [official documentation](https://github.com/huggingface/smolagents).
