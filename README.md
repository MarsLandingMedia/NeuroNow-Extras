# NeuroNow Extras

This repository is a companion resource to the core [NeuroNow project](https://github.com/MarsLandingMedia/NeuroNow). It provides supplemental files, standards, prompts, and tools to support the development and maintenance of the NeuroNow AI integration for ServiceNow.

The NeuroNow Extras folder contains supporting developer documentation, UI code snippets, standards, and configuration instructions used to extend and maintain the NeuroNow AI platform in ServiceNow.

These resources are intended for advanced implementers building assistant tools, server-side skills, and custom front-end components for ServiceNow and OpenAI integrations.

---

## Purpose

This package provides:

- Internal coding and formatting standards used in the NeuroNow implementation  
- Agent instruction sets for GPT-powered ServiceNow assistants  
- AngularJS integration examples for Service Portal widgets  
- Response formatting rules for HTML-based output  
- A markdown-to-HTML guide to support consistent rendering in widgets  

---

## Installation (video includes NeuroNow and NeuroNow Extras)

[![Watch the video](https://img.youtube.com/vi/BatQu_sBEFQ/0.jpg)](https://www.youtube.com/watch?v=BatQu_sBEFQ)

---

## Included Files

### system instructions
- This file is located at the root of this repo.
- Copy and past the contents into the 'System Instructinos' of your Assistant's configuration page. 


### agent-instructions.md

Instruction set for configuring LLM behavior and enforcing specific practices within the ServiceNow context. Includes:

- Catalog item creation rules  
- Record creation/update enforcement policies  
- Field resolution logic  
- Function usage best practices  
- Secure reference lookups and table query strategies  

### coding_standards.txt

Defines standardized ServiceNow scripting rules:

- Commenting requirements and formatting conventions  
- GlideRecord query handling using encoded string variables (e.g., `gr_q`)  
- Preferred structure for Script Includes and functions  
- Guidelines for efficient, readable, and reusable code  

### g_form_client_script.txt and sp_widget_with_gform.txt

Service Portal code snippets showing how to:

- Use `g_form` in AngularJS controllers  
- Listen for `field.change` events  
- Handle client-side logic for catalog variables  

### how_to_display_code_snippets.txt

Outlines formatting rules for displaying code in responses:

- Use of `<pre><code class="language-xxx">` blocks  
- Required escaping of code content  
- Applies to all system-generated code examples  

### response_standards.txt

Rules for formatting LLM responses returned to the ServiceNow UI:

- Required use of HTML structure and semantic tags  
- Bullet and section formatting  
- Code snippet presentation guidelines  
- Notes on tone and spacing  

### Guide_to_Converting_Markdown_to_HTML.pdf

Guide for converting Markdown syntax to compliant HTML for ServiceNow widgets:

- Covers headings, bold/italic, links, images, blockquotes, and code  
- Explains escaping, nesting, and table rendering  
- Intended for GPT-based rendering engines or build processes  

---

## Reference Files

This folder also contains quick-reference documentation used for assistant training and developer support:

### css_cheatsheet  
Quick reference for basic CSS syntax and style properties.

### css_cheatsheet_advanced  
Advanced CSS usage patterns including layout, animation, and specificity.

### html_cheatsheet  
Reference guide for standard HTML tags, structure, and usage.

### html_reference_tag  
List and descriptions of common HTML tags and their attributes.

### servicenow-yokohama-api-reference-enus  
Official API documentation for the ServiceNow Yokohama release. Useful for implementing or validating function calls within custom Script Includes.

### servicenow-yokohama-intelligent-experiences-enus  
Documentation specific to Yokohama's intelligent experiences (e.g., Agent Assist, Next Experience UI).

### technical_documentation  
This file is assumed to be a custom or internal index of best practices, templates, or deployment standards related to NeuroNow.

---

## Assistant Initialization

The `primary prompt` file serves as a system-level instruction to GPT-based agents. It explicitly points the assistant to follow the rules defined in `agent-instructions.md`.

This ensures that all conversational logic, access restrictions, and function usage behavior adhere to a centralized and auditable policy.

---

## Limitations

- These materials are intended for internal or demonstration use only.  
- Code examples and patterns may contain assumptions or simplifications.  
- Not all snippets have been hardened for production use.  

---

## Licensing

This content is provided under the <a href="https://www.gnu.org/licenses/gpl-3.0.html" target="_blank">GNU Affero General Public License</a>. by Mars Landing Media LLC for demonstration and educational purposes only.

No warranties, maintenance, or official support are provided. Mars Landing Media LLC assumes no responsibility for any damages, loss of data, or operational disruption resulting from incorrect, inappropriate, or enterprise use of this product or any part of it.

This code is not production-ready and may contain errors or incomplete logic.

Use of this project assumes that you remain in compliance with ServiceNow’s Terms of Service and OpenAI's Terms of Use.

This project does not utilize `GlideRecordSecure`, and therefore does not enforce full ACL-based access controls. Data access assumes a trusted and sandboxed development environment and may not meet ServiceNow security best practices.
