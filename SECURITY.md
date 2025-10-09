# Security Policy for GrouplyGiftr Website

## Deployment Keys

This repository uses deployment keys to allow automated deployments from the [website-source](https://github.com/yourusername/website-source) repository. These keys provide write access to this repository for continuous deployment purposes.

### How It Works

1. A SSH key pair is generated specifically for deployments
2. The public key is added as a deployment key to this repository with write access
3. The private key is stored as a secret in the source repository
4. GitHub Actions in the source repository use this key to push built website files to this repository

### Security Considerations

- The deployment key has limited scope (only this repository)
- The private key is stored as an encrypted secret in GitHub Actions
- The key should be rotated periodically for security
- Never commit private keys directly to any repository

## Reporting a Vulnerability

If you discover a security vulnerability in this project:

1. **Do not** disclose it publicly on issues or discussions
2. Email us at [security@grouplygiftr.com](mailto:security@grouplygiftr.com) with details
3. Allow time for us to address the vulnerability before public disclosure

## More Information

For more information on GitHub deployment keys, please refer to:

- [GitHub Documentation: Managing Deploy Keys](https://docs.github.com/en/developers/overview/managing-deploy-keys)
- [GitHub Documentation: Using environment secrets](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions)
