# Code Scanning
So, your team is developing a software and likely your code depends on external 3rd party libraries or open-source software (dependencies). Any vulnerability in these dependencies can translate to security risk in your solution. By continuously run code/security analysis in your CI/CD process, you can greatly reduce security risk and prevent bugs from every appearing in your solution.


# How to do this effectively? 

## Static code analysis
The following are tools that you may considered.
* [CodeQL](https://help.semmle.com/codeql/about-codeql.html) - [Learning CodeQL (Security Lab)](https://help.semmle.com/QL/learn-ql/index.html)
* GitHub build-in [code scanning](https://docs.github.com/en/free-pro-team@latest/github/finding-security-vulnerabilities-and-errors-in-your-code/automatically-scanning-your-code-for-vulnerabilities-and-errors) features.
* [Managing security vulnerabilities](https://docs.github.com/en/free-pro-team@latest/github/managing-security-vulnerabilities) in GitHub.
* [Dependabot](https://github.com/dependabot/dependabot-core#dependabot)
* [DevSkim](https://github.com/Microsoft/DevSkim#devskim) - a framework of IDE extensions and language analyzers that provide inline security analysis in the dev environment as the developer writes code.
* [BinSkim](https://github.com/microsoft/binskim/blob/main/docs/UserGuide.md) - a checker that examines Portable Executable (PE) files and their associated Program Database File Formats (PDB) to identify various security problems.
* [Security Code Scan for .NET](https://security-code-scan.github.io/)
* [Secure DevOps Kit for Azure](https://github.com/azsk/DevOpsKit-docs)
* [Additional tools](https://www.microsoft.com/en-us/securityengineering/sdl/resources)

## OWASP Scanning

* **What is OWASP Scanning?**
This is a way of scanning your deployed application with an engine which will test the application endpoint effectiveness by launching simulated attacks. A report is generated afterwards which can be assessed. 

* **How does this fit into DevOps?**
Usualy Penetration Testing (or Pen Testing) is carried out at the latter stages of development against the completed web site (and may continue at a regular cadence thereafter). However it doesn't have to be this way. Scanning/Pen testing can be undertaken during development against the deployed website, during release as an extension of integration testing steps. The advantage is that you learn about any potential new vulnerabilities quickly. These could be issues created by new code/features or issues introduced by regression. 

* **What exists that can help me here?**
Quite a bit of technical effort is required to write a tool that can undertake this kind of synthetic testing/scanning and keep it up to date. For the vast majority of teams writing and maintaining their own tools is not going to be a good use of time and in most cases would not be recommended (mistakes here could lead to a false sense of security).
[OWASP themselves maintain an open source product called Zap](https://owasp.org/www-project-zap/), this tool is regularly maintained and free to use with good online usage instruction and documentation. [An extension of this tool can be obtained from the VS marketplace. The extension can be utilised to run in a Build or Release Pipeline. Full instructions provided in this link.](https://marketplace.visualstudio.com/items?itemName=CSE-DevOps.zap-scanner)

**Zap Extension instructions, too long didnt read**
  * Install docker onto the devops agent
  * Add script task for "docker run" that launches the container and Zap with the correct configuration
  * Use custom XSLT to convert the ZAP XML output to a NUNIT style that works with devops
  * publish the converted output

Community blog posts exist which describe these steps in more detail, in addition to the detailed instructions provided on the marketplace page linked above.

## Container Scanning
* Code scanning in a container using [CodeQL](https://docs.github.com/en/free-pro-team@latest/github/finding-security-vulnerabilities-and-errors-in-your-code/running-codeql-code-scanning-in-a-container)
* [Azure Defender for container registries](https://docs.microsoft.com/en-us/azure/security-center/defender-for-container-registries-introduction)


