# DDNS Updater Script

This script updates a DNS A record on Cloudflare with the current public IP address of the machine. It is useful for maintaining a dynamic DNS setup.

## Configuration

- **auth_email**: Your Cloudflare account email.
- **auth_method**: Authentication method, either "token" or "global".
- **auth_key**: API token or global API key.
- **zone_identifier**: Cloudflare zone ID.
- **record_name**: DNS record name to update.
- **ttl**: Time-to-live for the DNS record.
- **proxy**: Whether to enable Cloudflare proxy (true/false).
- **slackchannel**: Slack channel for notifications.
- **slackuri**: Slack webhook URL.
- **discorduri**: Discord webhook URL.

## Functionality

1. **Get Public IP**: Fetches the current public IP using Cloudflare or fallback services.
2. **Validate IP**: Ensures the IP is valid.
3. **Check DNS Record**: Retrieves the current DNS A record from Cloudflare.
4. **Compare IPs**: Checks if the current IP matches the DNS record.
5. **Update DNS Record**: Updates the DNS record if the IP has changed.
6. **Notifications**: Sends updates to Slack and Discord if configured.

## Usage

1. Configure the script by setting the variables in the configuration section.
2. Run the script to update the DNS record.

Ensure you have the necessary permissions and API access configured in Cloudflare.
