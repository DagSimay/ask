# ask

A Bash (zsh) CLI tool that sends prompts to an OpenAI compatible LLM API using only 'curl' and 'jq'.

## Dependencies

- 'curl'
- 'jq'

## Setup

1. Get a free API key. (I used groq because of it's free option) (https://console.groq.com)
2. Set the three environmental variables: ASK_API_URL , ASK_MODEL , ASK_API_KEY.
3. Make the script executable:  chmod +x ask


## Usage

# Multiple arguments can be joined into one prompt. Ex: 
ask "Establishment dates of" "Turkey" "Azerbaijan" "Japan"

# Pipe input ex:
cat doriangrey.sh | ask "Explain what this script does:"

# Pipe and argument input can be combined. Ex:
uname -a | ask "Explain this system info:"

## Some Limits

-No conversation history, each call is stateless.
-Requires culr and jq to be installed.
-Has limits related to API provider's limits.
