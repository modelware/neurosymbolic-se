# NSEE Course Guide

Modelware · Neurosymbolic Systems Engineering (NSEE)

**Modelware provides this course**, including its learning materials, delivery arrangements, support, and review guidance.

## Audience and prerequisites

This course is for systems engineers, methodology developers, and technical practitioners who want to make engineering knowledge computable and use AI with explicit verification.

Bring an engineering domain you understand, a computer on which you can install the tools, a GitHub account, and willingness to work with text-based models and command-line tools. Module 1 walks through the initial setup. Prior OML expertise is not assumed.

## Pacing

The course has eight modules. Complete them in sequence because later modules build on earlier artifacts. Follow the pacing and review arrangements provided by Modelware. When working independently, use the module completion criteria and capstone milestones to decide when to continue.

Use the current module guides and the [capstone roadmap](CapstoneRoadmap.md) for the practical work and milestone progression.

## Two practical tracks

- **Labs:** extend or investigate the Sierra / Fire Force VI running example in your own `sierra-method` fork. Module 8 focuses on the capstone and has no separate lab.
- **Capstone:** choose your own engineering system, define its methodology, and develop a model that answers specific stakeholder questions. Four milestones combine work across the eight modules.

Keep the lab fork separate from the capstone. Where a guide uses an illustrative `example.com` IRI or repository name, replace it consistently for your own work.

## Tools and access

Follow [Module 1](Module1.md) for VS Code, OML Code, the OML CLI, Node.js, Git, and the running example.

OML Code access must be arranged for the account you use. Confirm your access arrangements with your Modelware NSEE course contact. Use the [official OML Code information](https://www.modelware.io/oml-code) for platform and access details.

Use an AI coding assistant available to you. Module 6 requires an MCP-capable agent. Arrange access to the AI service you will use before starting the lab.

Module 8 requires an `OML_PLATFORM_API_KEY` for unattended CI/CD. Obtain it through your OML Platform access arrangements. Store the value as a GitHub Actions secret; screenshots should show its name, never its value. Ask your Modelware NSEE course contact if your account cannot obtain the required access.

## Evidence and review

Each module describes what to produce. Keep a local evidence document or folder containing the relevant repository URLs, exact commit hashes, commands, results, screenshots, findings, and explanations. Retain original AI chat logs for Module 6.

Send all lab and capstone submissions directly to the lecturer, **Dr Maged Elaasar**, by email at [melaasar@modelware.io](mailto:melaasar@modelware.io). Include the requested documents, screenshots, repository URLs and exact commit hashes for the relevant deliverable. Keep a copy of the submitted evidence in your learning portfolio.

A successful command is one piece of evidence. Also check that the result answers the engineering question, that generated artifacts reflect the intended model, and that another person could reproduce the work from the recorded revision.

For Module 8, seek a peer review when one is available. If working independently, record a self-review and its limitations; a self-review is not an independent engineering approval.

## Repository visibility

Use repository visibility appropriate to the information you are modeling. Course exercises can use public example repositories; proprietary engineering models and credentials should remain in an environment authorized for that information. GitHub feature availability may depend on the repository and account configuration.

## Help

Use Modelware’s course support channel or [contact Modelware](https://www.modelware.io/contact). For a technical issue, include the module, tool versions, command, expected outcome, and a redacted error log.
