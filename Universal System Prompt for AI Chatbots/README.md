# Universal Structure of System Prompts for AI Chatbots

**Natalia Kazakevych**, November 2026

**Keywords:** system prompt, prompt engineering, AI chatbot, website chatbot, conversational AI, prompt structure, prompt template, tourism, camping


## Overview

This project presents a universal structure for system prompts of AI chatbots that answer questions from website visitors (hereafter, users). The structure is demonstrated on a camping site chatbot, but it can be easily adapted to other industries.

### Goal
To provide a standardized structure that separates universal instructions from business-specific content. This enables adaptation to different industries with minimal modifications while keeping the overall organization consistent.


## Background and Motivation

Businesses increasingly use AI chatbots to automate communication with visitors on their websites. However, developing a high-quality system prompt still requires significant time and effort, because existing solutions are tailored to a specific business and are difficult to reuse. In addition, the production-ready system prompts reviewed for this project consistently have a poorly organized structure, and their instructions are often duplicated or conflicting.

### Key Features
To address this challenge, the proposed structure:

- is precise and consistent;
- avoids redundancy and conflicting instructions;
- separates reusable components from business-specific information;
- relies on clear concise and easy-to-maintain instructions.


## Collaboration

This project originated during work with [Mittelstand-Digital Zentrum Tourismus](https://www.mittelstand-digital.de/MD/Navigation/DE/Service/EnglischeSeite/englische-seite.html) on a chatbot for a tourism business. The production-ready system prompts provided by the center served as a starting point for analyzing existing approaches. The universal structure presented here was developed independently by the author while writing a system prompt for one of the camping sites.


## Architecture

```
├── specific-components/  # Screenshots outlining universal prompt components
├── universal-components/ # Screenshots outlining business-specific prompt components
├── README.md             # Project documentation
```


## Visual Overview

<img width="500" height="530" alt="image" src="https://github.com/user-attachments/assets/c50343bf-69f2-4e84-b83c-725f24420036" />


## Overview of the Nine Sections
```
├── 1 🟩 Identity and Role               # Definition of the chatbot's identity, purpose, and responsibilities
├── 2 🟩 Knowledge and Information       # Definition of available information sources and rules for their use
├── 3 🟩 Intent Understanding            # Identification of the user's query
├── 4 🟩 Query Processing Logic          # Algorithms for processing queries
├── 5 🟩 Information Selection           # Criteria for selecting information for responses
├── 6 🟥 Key Query Topics                # Special handling of high-priority or business-critical queries
├── 7 🟥 Constraints and Special Cases   # Restrictions, exceptions, and special-case behavior
├── 8 🟩 Response Generation             # Standards for response structure, style, and formatting
└── 9 🟩 Hallucination Prevention
          and Instruction Compliance      # Prevention of hallucinations and enforcement of prompt instructions
```


## Core Components

Also, all system prompt components fall into two groups: universal (marked in green 🟩) and business-specific (marked in red 🟥).

Universal components retain their structure and logic regardless of the chatbot's domain. Business-specific components require substantial adaptation to the specifics of each organization, and their content can differ even within the same business.

### Universal Components
Universal components define the general operating rules of an AI assistant as a website chatbot and do not depend on the specifics of the business. When creating a system prompt for another business, their structure and content remain unchanged. Only project-specific data needs to be edited: the chatbot's name, the organization's name, and other details.

The content of each component can be found in the [`universal-components/`](https://github.com/NataLK-tech/Internship_Projects/tree/main/Universal%20System%20Prompt%20for%20AI%20Chatbots/universal-components) folder.

### Adaptable Components
Business-specific components were developed for a camping site chatbot and serve as an example of what this part of the prompt may look like. When used in another industry, they need to be redesigned completely: both the set of items and the content will be entirely different. Substantial rework may also be required for another camping site: the structure of the example can be kept, but the content depends on the specifics of each organization, and minor structural changes may be needed depending on the priorities and rules of the business.

The content of these components can be found in the [`specific-components/`](https://github.com/NataLK-tech/Internship_Projects/tree/main/Universal%20System%20Prompt%20for%20AI%20Chatbots/specific-components) folder.


## Recommended Workflow

Based on practical experience, I recommend following this sequence to optimize the prompt development process:

1. **Preparation**
   - Study the universal structure (for beginners).
   - Review the website content from the user's perspective and compile a list of 100 questions that reflect different interests and behavior scenarios.
   - Prepare a list of questions for the client (the website owner):
         what matters for the prompt;
         key user queries and business specifics;
         what is missing from the website content, based on the 100 questions.
3. **First meeting with the client**
   - Get answers to the prepared questions.
   - Extend the question list with provocative queries:
         request for a discount,
         complaint,
         question about competitors,
         attempt to make the chatbot step out of its role, etc.
5. **Development and internal testing**
   - Write the initial version of the prompt.
   - Test it with the full list of questions by the development team.
6. **Client testing**
   - The client tests the prompt.
   - The prompt is revised based on the client's feedback.
7. **Delivery**
   - Hand over the final version of the prompt to the client.
   - Integrate the chatbot into the website.


## Acknowledgements

I would like to thank [Mittelstand-Digital Zentrum Tourismus](https://www.mittelstand-digital.de/MD/Navigation/DE/Service/EnglischeSeite/englische-seite.html) and , in particular, [Rozaliia Tarnovetckaia](https://www.linkedin.com/in/rozaliia-tarnovetckaia-756531101/) for the internship opportunity, for their support, and for the practical experience and materials that gave rise to this work.

## Author

Natalia Kazakevych
[LinkedIn](https://www.linkedin.com/in/natalia-kazakevych-131478348/)


## License

This work is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You are free to use and adapt it, provided that you give appropriate credit to the author.


## Citation

If you use this work, please cite it as:

Kazakevych, N. (2026). *Universal System Prompt for AI Chatbots*. GitHub. [https://github.com/NataLK-tech/Internship_Projects/tree/main/Universal%20System%20Prompt%20for%20AI%20Chatbots]
