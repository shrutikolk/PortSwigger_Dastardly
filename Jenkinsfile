name: 'Dastardly Scan Action'
description: 'Runs a Dastardly scan against a target site'
author: 'PortSwigger'
inputs:
  target-url:
    description: 'The full url (including scheme) of the site to scan'
    required: true
  output-filename:
    description: 'The filename used for the scan report. This filepath relates to the dastardly container, and will exist in the github workspace (/github/workspace)'
    required: false
    default: dastardly-report.xml
runs:
  using: 'docker'
  image: 'Dockerfile'
  env:
    DASTARDLY_TARGET_URL: ${{ inputs.target-url }}
    DASTARDLY_OUTPUT_FILE: /github/workspace/${{ inputs.output-filename }}
branding:
  icon: 'activity'
  color: 'green'
