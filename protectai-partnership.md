---
title: "Hugging Face Teams Up with Protect AI: Enhancing Model Security for the Community"
thumbnail: /blog/assets/protectai-partnership/thumbnail.png
authors:
- user: mcpotato
---


We are very pleased to announce our partnership with Protect AI, as part of our [long-standing commitment](https://huggingface.co/blog/2024-security-features) to provide a safe and reliable platform for the community.

[Protect AI](https://protectai.com/) is a company operating at the crossroads of AI and Security, developing powerful tools, namely [Guardian](https://protectai.com/guardian), with a mission to become the platform for AI security.

Our decision to partner with Protect AI stems from their [community driven](https://huntr.com/) approach to security, active support of open source and expertise in all things security x AI.


## Model security refresher

To share models, we serialize the data structures we use to interact with the models, in order to facilitate storage and transport. Some serialization formats are vulnerable to nasty exploits, such as arbitrary code execution (looking at you pickle), making sharing models potentially dangerous.


As Hugging Face has become the de facto platform for model sharing, we’d like to protect the community from this, hence why we have developed tools like picklescan and why we are integrating Guardian in our scanner suite.

Pickle is not the only exploitable format out there, [see for reference](https://github.com/Azure/counterfit/wiki/Abusing-ML-model-file-formats-to-create-malware-on-AI-systems:-A-proof-of-concept) how one can exploit Keras Lambda layers to achieve arbitrary code execution. The good news is that Guardian catches both kinds of exploits!


## Integration

In the effort of integrating Guardian, we have capitalized on the opportunity to revamp our frontend to display scan results. Here is what it now looks like:

*<Insert pictures of the new design / maybe old design as well side by side for comparison>*

As you can see from the pictures, you have nothing to do to benefit from this! All public model repos will be scanned by Guardian automatically as soon as you push your files to the Hub.
*Mention backlink to the platform? Or add screenshot of it above*

Note that you might not see a scan for your model as of today, as we have over 1 million, it may take some time to catch up.

