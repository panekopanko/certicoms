# Certicoms
**AD CS Command Reference** - A cute interactive reference tool for Certipy & Certify commands.

Inspired by [WADComs](https://wadcoms.github.io/), CertiComs provides an easy-to-use interface for finding the right Active Directory Certificate Services commands during pentests and CTFs.

## Features

### 🎯 Dual Tool Support
- **Certipy** (Linux/Python) - 15+ commands
- **Certify** (Windows/.NET) - 13+ commands

### ⚙️ Quick Variables Panel
- Input your environment variables once (domain, DC IP, credentials, etc.)
- Variables auto-populate in all commands
- Saved to browser localStorage for persistence
- Visual highlighting of variable placeholders

### 🔍 Smart Filtering
- **Tool**: Filter by Certipy or Certify
- **Credentials**: Filter by Password, Hash, Certificate, or No Credentials
- **Attack Type**: Enumeration, Exploitation, Forge, Relay

### 💜 Beautiful UI
- Cute pink & purple gradient theme
- One-click command copying
- Real-time search across all commands
- Collapsible variables section
- Responsive design

### ⌨️ Keyboard Shortcuts
- Type any key to focus search
- `Esc` to clear all filters and search

## Usage

### Start the Web Server

```bash
cd /home/kali/cyberspace/certicoms
python3 -m http.server 8888
```

Then open your browser to: `http://localhost:8888`

### Using Variables

1. Click "⚙️ Quick Variables" to expand the variables panel
2. Fill in your environment details:
   - Domain (e.g., `domain.local`)
   - DC IP (e.g., `10.10.10.10`)
   - DC Hostname (e.g., `dc.domain.local`)
   - Username (e.g., `user@domain.local`)
   - Password, Hash, CA Name, etc.
3. Variables automatically save on change
4. All commands will show with your variables substituted
5. Copy button includes your actual values

### Example Workflow

1. **Set Variables**: Fill in your domain info in the variables panel
2. **Filter by Tool**: Click "Certipy" or "Certify" depending on your OS
3. **Filter by Access**: Select what credentials you have (Password/Hash/Certificate)
4. **Search**: Type "ESC1" to find relevant exploitation techniques
5. **Copy**: Click the copy button to get the command with your variables

## Covered Techniques

### Certipy Commands
- **ESC1-ESC16**: All major AD CS escalation techniques
- **Shadow Credentials**: Key Credential Link manipulation
- **Golden Certificates**: CA certificate abuse
- **NTLM Relay**: ESC8 (HTTP) and ESC11 (RPC)
- **Certificate Request Agent**: ESC3 on-behalf-of attacks
- **CA Management**: ESC7 certificate issuance
- **Template Manipulation**: Making templates vulnerable
- **Account Operations**: ESC10/ESC13 attacks

### Certify Commands
- **Enumeration**: Find vulnerable CAs and templates
- **Certificate Requests**: ESC1 with alternative names
- **Agent Certificates**: ESC3 enrollment agent attacks
- **PKI Objects**: Issuance policies and permissions
- **CA Security**: Permission analysis for escalation paths

## Variables Supported

| Variable | Description | Example |
|----------|-------------|---------|
| `DOMAIN` | Active Directory domain | `contoso.local` |
| `DC_IP` | Domain Controller IP | `10.10.10.10` |
| `DC_HOST` | Domain Controller hostname | `dc.contoso.local` |
| `USER` | Username for authentication | `user@contoso.local` |
| `PASSWORD` | User password | `Password123!` |
| `HASH` | NTLM hash | `aad3b435b51404ee...` |
| `CA_NAME` | Certificate Authority name | `CONTOSO-CA` |
| `TEMPLATE` | Certificate template name | `User` |
| `TARGET` | Target user/computer | `administrator` |
| `PFX_FILE` | Certificate file path | `admin.pfx` |

## About

CertiComs was created to make AD CS attack commands more accessible during security assessments. The tool combines both Certipy (Linux) and Certify (Windows) commands in one convenient interface with variable substitution.

## Credits

- **Certipy**: [ly4k/Certipy](https://github.com/ly4k/Certipy) - Python-based AD CS toolkit
- **Certify**: [GhostPack/Certify](https://github.com/GhostPack/Certify) - C# AD CS enumeration and abuse
- **Inspiration**: [WADComs](https://wadcoms.github.io/) - Windows/AD offensive command reference
- **Theme**: Custom pink & purple gradient design

## Contributing

Feel free to add more commands, improve filtering, or suggest new features!

## Tips

- Variables are stored in browser localStorage - they persist across sessions
- Use the "Clear All" button to reset all variables
- Filter combinations work together (e.g., "Certipy + Password + Exploitation")
- Search works on command names, syntax, and descriptions
- Commands show highlighted variable placeholders when no variables are set
- Commands show actual values when variables are saved
                                                       
