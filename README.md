zkArb SDK is a zero-setup developer toolkit that simplifies zero-knowledge proof integration on Arbitrum. It abstracts the full ZK lifecycle—Circom compilation, Groth16 trusted setup, Solidity verifier generation, contract deployment, and on-chain proof verification—into a single CLI and JavaScript function, requiring no prior Web3 or ZK knowledge.
Key Features:
One-Command ZK Compilation: Convert .circom files into .r1cs, .wasm, .zkey, and Solidity verifier contracts
Proof Testing & Generation: Automatically generate proof.json and public.json with developer-provided inputs
Arbitrum Verifier Deployment: Deploy verifier contracts to Arbitrum One, Nova, or Orbit with simplified CLI commands
Programmatic On-Chain Verification: Verify proofs in-app with a single verifyProof() call
Fully Abstracted: No need to write Web3 scripts, manage ABI, or format calldata manually
Planned Arbitrum-Specific Enhancements:
L1 ↔ L2 Proof Result Messaging: Enable seamless relay of proof results between Arbitrum and Ethereum using native Arbitrum messaging
Gas-Optimized Verifier Contracts: Auto-optimize generated verifiers for Arbitrum’s Nitro environment to minimize calldata and cost
ZK Template Library: Prebuilt templates for age verification, DAO membership, private token gating, and more—targeted for Arbitrum-native apps
Hosted ZK Playground: Web-based interface to simulate circuits, generate proofs, and deploy verifiers on Arbitrum testnets and mainnet
Verifier Explorer: UI to browse and interact with deployed ZK verifiers on Arbitrum
zkArb SDK aims to democratize zero-knowledge application development on Arbitrum by eliminating complexity and providing an end-to-end ZK experience tailored for the ecosystem. It empowers developers to build privacy-preserving, identity-aware dApps with just a few lines of code.
Telegram

@jatin102938

Twitter

@jatinsahijwani1

What innovation or value will your project bring to Arbitrum? What previously unaddressed problems is it solving? Is the project introducing genuinely new mechanisms.

zkArb SDK introduces a breakthrough developer experience by abstracting the entire zero-knowledge proof lifecycle into a simple, no-setup toolkit purpose-built for Arbitrum. It empowers any developer — even those with no blockchain or cryptography background — to integrate ZK-powered features into their Arbitrum applications using a single CLI and function call.

Unaddressed Problems We’re Solving:

ZK Integration Complexity
Despite growing interest in zero-knowledge applications, most developers struggle with the fragmented and highly technical process of writing Circom circuits, running trusted setups, generating Solidity verifiers, formatting calldata, and verifying proofs on-chain. zkArb SDK unifies all of this into one streamlined CLI and JS function.

Lack of Arbitrum-Specific ZK Tooling
Arbitrum lacks tooling that is tailored to its verifier environment, gas constraints, and L2 execution model. zkArb SDK introduces the first plug-and-play ZK developer kit built specifically for Arbitrum's Nitro stack, supporting contract deployment on Arbitrum One, Nova, and Orbit chains.

High Entry Barriers for Application Developers
Developers building dApps often avoid ZK due to the perceived complexity. zkArb SDK eliminates this barrier by handling every low-level detail — from proof generation to contract deployment — allowing frontend developers to integrate ZK features with zero Web3 or cryptography knowledge.

Genuine Innovation
End-to-End ZK Abstraction for Arbitrum
zkArb SDK introduces a fully abstracted ZK workflow — from .circom to on-chain verification — with no manual ABI handling, calldata formatting, or Solidity compilation required. This radically lowers the barrier to entry and opens ZK to a broader class of developers.

L1 ↔ L2 Proof Messaging (Planned)
We will introduce a native mechanism to bridge proof verification outcomes between Arbitrum and Ethereum using Arbitrum’s cross-chain messaging protocol. This enables trustless proofs to impact logic across L1 and L2, unlocking powerful interoperability.

Gas-Optimized Solidity Verifier Generation for Nitro
Our SDK will automatically optimize Solidity verifier contracts for Arbitrum’s Nitro runtime, minimizing calldata size and reducing gas costs for proof verification transactions — something that current tooling does not support.

ZK Template Library and Hosted Playground
We will offer ready-to-use circuit templates (e.g. age verification, DAO membership, private token gating) and a hosted playground for testing, compiling, and deploying ZK apps on Arbitrum directly from the browser.

zkArb SDK brings truly new mechanisms to the Arbitrum ecosystem by transforming ZK integration from a months-long engineering effort into a one-command workflow. This leap in developer experience will unlock a wave of private, permissionless, and identity-based applications on Arbitrum — without requiring developers to be ZK experts.

What is the current stage of your project.

We are currently in the architectural design and planning stage, with implementation to begin from scratch specifically for Arbitrum.

While our previous work on zk-polka-sdk gave us deep experience in abstracting ZK tooling (Circom → Solidity verifier → on-chain proof verification), zkArb SDK will be built entirely ground-up for Arbitrum’s Nitro stack, taking into account:

Arbitrum’s unique L2 contract deployment flow

Gas cost optimization for ZK verifiers in Nitro

Compatibility with Arbitrum One, Nova, and Orbit

Support for L1 ↔ L2 messaging for proof outcomes

We’re not reusing code from other ecosystems — we’re building a clean, Arbitrum-native developer SDK that aligns tightly with the needs of the ecosystem, and offers the smoothest ZK onboarding experience for Arbitrum developers.

Our learnings from previous ZK tooling will guide us, but the implementation will be fully focused on delivering the best zero-knowledge toolkit for Arbitrum from day one.

Do you have a target audience? If so, which one.

Primary Audiences

Application Developers New to ZK
Frontend and full-stack developers who want to add ZK-powered features (like private identity checks, DAO gating, or selective disclosure) to their Arbitrum dApps without needing to learn Circom, snarkjs, or Solidity verifier logic.

Web3 Hackathon Participants
Builders looking to integrate ZK in hackathons on Arbitrum in a short time frame. zkArb SDK drastically reduces setup and complexity, making ZK proofs viable even under weekend deadlines.

Arbitrum dApp Developers Exploring ZK
Existing Arbitrum builders who want to enhance their applications with privacy-preserving or verification features but currently face friction due to the complexity of ZK toolchains.

Secondary Audiences

Blockchain Education Programs
Bootcamps and university courses teaching smart contract development and zero-knowledge proofs. zkArb SDK offers a simple, guided introduction to real-world ZK usage on Arbitrum.

ZK Curious Developers
Developers familiar with Ethereum or Arbitrum who are interested in zero-knowledge proofs but haven’t integrated them due to tooling complexity or lack of onboarding material.

Enterprise and B2B Teams Exploring On-Chain Credential Verification
Teams building trustless KYC, private access control, or compliant DeFi systems on Arbitrum that require seamless integration of ZK verifiers without deep cryptography knowledge.

Open Source Contributors and DX Enthusiasts
Developers who want to improve or extend zkArb SDK, contribute templates, circuits, or integrations with other Arbitrum-based tools and ZK workflows.

Do you know about any comparable protocol, event, game, tool or project within the Arbitrum ecosystem.

Yes, we are aware of a few tools and projects in the Arbitrum ecosystem that touch on zero-knowledge or developer tooling, though none currently offer the end-to-end abstraction for ZK circuits that zkArb SDK provides.

Comparable or Related Projects:

ZK Stack on Arbitrum Orbit: Projects like Risc Zero and zkSync have expressed interest in integrating ZK features into custom Arbitrum Orbit chains. However, these are lower-level infrastructure efforts rather than developer-facing SDKs.

The Wizard (https://thewizard.app/): A browser-based IDE for Stylus contract development. While it offers a helpful interface for smart contract work, it doesn’t cover ZK tooling or proof integration.

Hardhat + Arbitrum Tooling: While Arbitrum developers often use Hardhat for testing and deployment, integrating Circom circuits and verifier contracts requires a lot of custom scripting and glue logic, which zkArb SDK aims to eliminate.

zkArb SDK is differentiated in that it provides the first dedicated toolkit to help developers compile, test, deploy, and verify ZK circuits on Arbitrum—with zero manual configuration and no requirement to understand snarkjs, Solidity verifiers, or calldata formatting.

We view our SDK as complementary to existing Arbitrum developer tools, helping expand the scope of what developers can build—especially for privacy-preserving, identity-aware, and permissionless on-chain apps.

Have you received a grant from the DAO, Foundation, or any Arbitrum ecosystem related program or conducted any IRL like a hackathon or workshop.

No, we have not received any grant from the Arbitrum DAO, Foundation, or any Arbitrum-related program yet.
However, we have previously built a similar ZK developer toolkit (zk-polka-sdk) for the Polkadot ecosystem, which won first prize at a Web3 hackathon. That experience demonstrated strong community demand for abstracted ZK tooling — and we are now focused on bringing a fully Arbitrum-native version to life through zkArb SDK.

Have you received a grant from any other entity in other blockchains that are not Arbitrum.

Yes, we received a $1500 prize for our previous project zk-polka-sdk, which was awarded for winning first place in a Polkadot ecosystem hackathon. That project focused on building zero-knowledge tooling for Polkadot’s PolkaVM.

We have not received any formal grant funding from other foundations or DAOs outside of that prize. The zkArb SDK will be built independently and from scratch, fully tailored for Arbitrum’s ecosystem, architecture, and developer needs.

What is the idea/project for which you are applying for a grant.

zkArb SDK is a zero-knowledge developer toolkit purpose-built for the Arbitrum ecosystem. It abstracts the entire zkSNARK workflow—Circom circuit compilation, Groth16 trusted setup, Solidity verifier generation, and Arbitrum contract deployment—into a single CLI and JavaScript function call. This enables developers to build privacy-preserving, trust-minimized features such as DAO membership gating, identity proofs, and off-chain credential validation, without needing expertise in Circom, Solidity, or Web3 tooling.

With just a CLI command or a single JavaScript function, developers can compile a ZK circuit, deploy the verifier contract to Arbitrum, and verify proofs on-chain — all while the SDK handles calldata formatting, Groth16 proof generation, and contract interaction behind the scenes.

Implementation Plan
Phase 1: Core SDK Infrastructure (4 Weeks)

Architect the CLI and JS SDK from scratch with Arbitrum as the target chain
Implement Circom-to-ZKey pipeline (.r1cs, .wasm, .zkey, verifier.sol)
Run Groth16 trusted setup via snarkjs
Design SDK folder structure, CLI interface, and internal abstractions
Test local proof generation and circuit outputs

Phase 2: Arbitrum Contract Integration (3 Weeks)

Build deploy flow to Arbitrum One, Nova, and Orbit using cast or ethers.js
Auto-optimize verifier contracts for Arbitrum Nitro (e.g., calldata size reduction, ABI-safe formatting)
Introduce Arbitrum-native verifier formatting logic, including compressed calldata encoding for cheaper proof verification
Implement cross-chain messaging support to bridge ZK verification results from L2 → L1
Add support for Arbitrum’s custom gas pricing model, optimizing for lower calldata costs
Fully implement verifyProof() function for programmatic Arbitrum contract calls
End-to-end test using live Arbitrum testnet deployment of age verification circuit
Begin testing compatibility with Arbitrum Orbit chains

Phase 3: Orbit Chain Research & Prototyping (3 Weeks)

Deploy a local Orbit chain and test verifier deployments to analyze gas usage, contract size limits, and finality differences from Arbitrum One/Sepolia
Benchmark proof verification costs and execution times on Orbit, documenting deviations and optimization opportunities
Prototype cross-chain message passing to relay Orbit-verified proofs to Arbitrum One or Ethereum
Build a minimal working flow (circuit → proof → verifier deployment → on-chain verification) specifically on Orbit to validate feasibility
Identify developer experience gaps and add Orbit-specific abstractions (chain configs, RPCs, gas pricing) into the SDK
Phase 4: Templates, Playground & UX (3 Weeks)

Build and publish circuit templates for ZK use cases: age check, country proof, email hash, DAO badge
Create a hosted zkPlayground with drag-and-drop .circom support and Arbitrum deployment in-browser
Build minimal working frontend demo with zkArb SDK (Next.js + ethers.js)
Ship developer docs + code examples

Phase 5: Community Engagement & Adoption (3 Weeks)

University Workshops (6 total): Conduct 6 in-person workshops across leading universities, focusing on onboarding developers from non-Web3 backgrounds (frontend engineers, data scientists, and general JS developers). Each workshop will provide hands-on training with zkArb SDK, walking participants through compiling a Circom circuit, deploying to Arbitrum testnet, and verifying proofs on-chain.
We will onboard 6 developers for the pilot group. These developers come from non-Web3 backgrounds (frontend engineers, data scientists, and general JavaScript developers) and were selected based on their minimal prior experience with Solidity or Circom. This ensures the testing process reflects our target audience and validates whether zkArb SDK is truly accessible to developers without deep blockchain expertise.
We will maintain the dedicated Telegram support group and GitHub discussion channel for a minimum of three months following the hackathon, ensuring that participants continue to have access to guidance as they further develop or refine their projects. During active hackathon periods, we will provide real-time responses with an average response time of less than one hour. After the hackathon, while maintaining the group, we commit to addressing queries within 12–24 hours, ensuring a reliable feedback loop for both immediate troubleshooting and longer-term support.
Phase 6: Final Report & Submission (2 Weeks)

Summarize all phases of work completed: SDK core infrastructure, Arbitrum contract integration, templates, playground, workshops, and community adoption
Prepare detailed milestone-by-milestone progress overview with KPIs achieved
Document pilot group testing results and feedback from university workshops
Provide final technical report covering SDK architecture, implementation details, and future roadmap
Submit the report to the Arbitrum Foundation for review and grant closure
Outline the major deliverables you will obtain with this grant.

Public GitHub Repository
Production-ready, open-source zkArb SDK with modular CLI and JavaScript SDK
Built-in Circom compilation, ZKey setup, Solidity verifier generation, and proof verification logic
Continuous integration (CI) pipelines for code linting, testing, and releases
Open to community contributions with guidelines, issue templates, and MIT license

zkArb SDK CLI Tool
Publishable npx zk-arb-sdk CLI with commands:
compile: Compiles Circom circuit and runs Groth16 setup
test: Runs local proof generation using input.json
deploy: Deploys verifier.sol to Arbitrum testnet/mainnet
Automatically handles calldata formatting and Solidity verifier ABI encoding for Arbitrum Nitro
Future support for Orbit chain deployment and cross-chain verifier messaging

JavaScript SDK + verifyProof() Function
Clean, developer-friendly JavaScript interface to verify ZK proofs on-chain with one call
Accepts input JSON and compiled folder path, returns boolean for on-chain proof result
Optimized for use in frontend apps (Next.js, Vite, React)
Abstracts snarkjs, ABI encoding, and contract interaction into one utility

zkPlayground (Hosted Web App)
Browser-based playground for testing .circom files, generating proofs, and deploying verifiers to Arbitrum testnets
Drag-and-drop circuit upload and interactive input form
Visual feedback for verification results
Future integration with Orbit chains and age/email proof templates

zkArb.dev Website & Portal
Public-facing landing page and portal for zkArb SDK
Showcase features, example use cases, and circuit templates
Figma-based UI/UX design for clear onboarding
Live deployment at: https://zkArb.dev (to be launched post-Milestone 3)

Documentation & Educational Resources
Full developer docs with step-by-step guides for each CLI command and SDK feature
ZK proof theory primer (simplified for application developers)
Code examples:
Age verification app
DAO whitelist app
Email hash login proof
Video tutorials, and integration walkthroughs

Please explain how your idea/project aligns with the Arbitrum ecosystem goals.

zkArb SDK directly aligns with Arbitrum’s mission to expand developer accessibility, unlock new application verticals like ZK-powered DeFi, and cement its leadership in Ethereum scaling.

Developer Tooling Expansion
zkArb SDK fills a major tooling gap in the Arbitrum ecosystem: zero-knowledge integration.
Currently, ZK workflows require extensive cryptographic, Solidity, and Web3 expertise. zkArb SDK abstracts all of this into a single CLI + JavaScript function—making it possible for any developer to integrate ZK features in minutes, not weeks.

This enables faster experimentation, easier prototyping, and more production-grade use cases powered by privacy and proof-based trust—all natively on Arbitrum.

Ecosystem Growth via Accessibility
By removing technical barriers, zkArb SDK enables:

Frontend developers to build apps with ZK features

Hackathon teams to rapidly prototype on Arbitrum

Enterprises to adopt private on-chain compliance flows

This significantly broadens the range of teams and devs who can ship on Arbitrum—even if they don’t have deep Web3 or cryptography experience.

Enabling a New Class of dApps (ZK + DeFi)
zkArb SDK empowers the creation of ZK-powered DeFi protocols, including:

Private lending or reputation-based credit
Trustless compliance (age, jurisdiction checks)
DAO voting systems with identity protection
Credential-based airdrops or private access tokens

These applications highlight Arbitrum’s unique scalability, composability, and L2 strengths—further reinforcing its position as the go-to chain for serious DeFi and identity-aware protocols.

It directly addresses a key gap in the ecosystem and opens up entirely new categories of applications and builders for Arbitrum.

What is your requested grant.

29000 USD

Website.

https://hacktour.xyz

Please provide a detailed breakdown of the budget in term of utilizations, costs and other relevant information.

https://docs.google.com/spreadsheets/d/12qzRwtGNug0jrcq__EB0zTHgR6Eb5iqcJsck4147EbI/edit?usp=sharing

Provide a list of the milestones, with the USD amount of the grant associated to it, the deliverables that will be provided, and the estimated completion time.

Milestone 1: Core ZK SDK Architecture & Foundation
Funding: $10,000
Timeline: Week 1–4

KPIs:

CLI tool supports compile, test, and output folder generation
Fully automated Groth16 setup pipeline
Generates .r1cs, .wasm, .zkey, verifier.sol from valid .circom input
90% unit test coverage on compile and test modules
Internal test circuits compiled and verified using CLI
CI pipeline integrated with developer-friendly logs

Deliverables:

Public GitHub repo with open-source CLI
Standardized circuit output folder structure
Integrated testing suite with Circom samples
Functional CI/CD pipeline

Milestone 2: Arbitrum Deployment & Proof Verification Module
Funding: $7,000
Timeline: Week 5–7

KPIs:

verifier.sol compiled using solc and deployed on Arbitrum Sepolia
zk-arb deploy CLI command implemented and tested
verifyProof(input, path) JavaScript API verifies proof onchain
At least 3 sample circuits verified on Arbitrum
85% test coverage for deployment and contract modules

Deliverables:

CLI deployment command
JavaScript SDK with verifyProof() API
Verifier contracts live on Arbitrum Sepolia
Demo frontend integrated with deployed verifier

Milestone 3: Orbit Research & Prototyping
Funding: $1,800
Timeline: Week 8–10

KPIs:

Local Orbit chain successfully deployed and running
Proof verifier contract deployed and tested on Orbit
Benchmark report of proof verification costs and execution times on Orbit vs. Arbitrum One
Prototype of cross-chain message passing for verified proof results (Orbit → Arbitrum/Ethereum)
Minimal working developer flow (circuit → proof → verifier deployment → verification on Orbit) completed
Documentation draft outlining Orbit-specific adjustments (configs, RPCs, gas pricing)

Deliverables:

Running local Orbit chain environment with verifier deployment
Benchmarking report on performance and gas usage
Prototype implementation of Orbit → Arbitrum cross-chain verification message flow
Minimal end-to-end demo on Orbit (circuit to verification)
Draft documentation for Orbit integration and SDK adjustments

Milestone 4: Templates, Docs & DX Enhancements
Funding: $2,850
Timeline: Week 11–13

KPIs:

npx create-zkarb-app CLI scaffolding tool released
Includes 2 sample circuits and sample input files
Next.js zk dApp example demonstrating SDK usage
Documentation complete and hosted (e.g., GitHub Pages or Docusaurus)
30+ GitHub stars or 20+ npm downloads

Deliverables:

CLI scaffolding tool
Developer documentation (hosted)
Public zk dApp example
Starter circuits and sample inputs

Milestone 5: Community Engagement & Adoption
Funding: $3,000
Timeline: Week 14–16

KPIs:

6 in-person university workshops conducted, each with 30–50 participants.
6 pilot developers onboarded (non-Web3 backgrounds) completing end-to-end proof deployment using zkArb SDK.
Dedicated Telegram support group + GitHub Discussions live for at least 3 months post-hackathon.
Average query response time: <1 hour during hackathon weeks, 12–24 hours afterward.
100+ workshop participants trained, with 30%+ completing example project using zkArb SDK.

Deliverables:

6 university workshop sessions with recorded content (slides + recordings shared publicly).
Pilot group of 6 developers onboarded and actively testing zkArb SDK.
Maintained Telegram support group and GitHub discussion channel with published activity reports.
Workshop materials, templates, and example projects released as open resources for broader community adoption.

Milestone 6 : Final Report Submission
Funding : $4,350
Timeline : Week 16-18

Total Grant Ask: $29,000
Total Timeline: <=18 weeks

Are milestones clearly defined, time-bound, and measurable with quantitative metrics where applicable? What are your reference KPI, if applicable, for each milestone.

Yes, all milestones are structured around quantifiable KPIs and have clearly defined deliverables with week-wise timelines. Each milestone builds sequentially, with automated tooling, deployment support, developer experience, and adoption layers.

What is the estimated maximum time for the completion of the project.

<18 weeks from the date of grant approval and project initiation.

How should the Arbitrum community measure the success of this grant.

Developer Adoption
Number of GitHub stars, forks, and SDK downloads via npm
Active usage of the SDK’s CLI and verifyProof() function across developer projects
Number of real-world integrations using zkArb SDK, especially by developers with no prior ZK or Web3 experience
Growth in external contributions (e.g., new CLI features, example circuits, templates) via pull requests

Ecosystem Impact
Increase in ZK verifier contract deployments on Arbitrum testnet and mainnet using zkArb SDK
Expansion of use cases built with ZK (e.g., anonymous voting, credential verification, proof of uniqueness) on Arbitrum
Successful onboarding of new developers who previously avoided ZK/Web3 due to high learning barriers — enabled by the zero-config, abstracted design of zkArb SDK
Demonstrated ability of full-stack and frontend-only developers to build production-ready ZK applications without having to learn Circom, Groth16 setup, Solidity, or smart contract deployment workflows

Technical Performance
50% reduction in development time for building ZK-integrated applications (compared to traditional toolchains like snarkjs, solc, manual verifier deployment)
Reliable contract interaction and verification accuracy across CLI and SDK interface
High test coverage, robust DX, and minimal setup friction for new users
Proof of usability across multiple Arbitrum environments (e.g., Sepolia testnet, Arbitrum One)

What is the economic plan for maintaining operations or continuing the growth of your project after the grant period.

Open Source Community Development
Maintain an open and well-documented GitHub repository with clear contribution guidelines
Encourage external developer contributions via good-first-issue tagging and active support channels
Form a core maintainer group from HackTour India and trusted contributors in the Arbitrum developer community
Launch bounties for new circuit templates, SDK extensions, and feature requests to sustain open-source momentum

Strategic Ecosystem Partnerships
Collaborate with Arbitrum-native protocols (DeFi, Identity, DAO tooling) to provide ZK verification capabilities through zkArb SDK
Work with Orbit Chain builders to integrate zkArb SDK for chain-level proof verification tooling
Partner with educational platforms, DAOs, and universities to embed zkArb SDK in blockchain learning programs and developer bootcamps

Ongoing Development & Expansion
Apply for follow-on grants focused on advanced functionality (e.g., privacy-preserving oracles, zkML, L3-specific templates)
Introduce a roadmap-driven release cycle with stable, beta, and experimental branches
Build and maintain a template marketplace where developers can submit and reuse popular ZK circuits built with zkArb SDK
Launch SDK usage analytics (opt-in) to understand feature usage and improve DX iteratively

Market Needs: For developers building apps and interfaces, what specific challenges or opportunities do they face in Arbitrum.

Developers building zero-knowledge applications on Arbitrum today face several critical challenges:

High Barrier to Entry for ZK: Building ZK apps traditionally requires deep familiarity with Circom, Groth16, proof generation, calldata formatting, and smart contract integration — creating an overwhelming barrier for most frontend or full-stack developers.

Fragmented Tooling: There’s no unified pipeline that handles everything from compiling Circom to verifying proofs to deploying contracts on Arbitrum. Developers must stitch together CLI tools (snarkjs, solc, hardhat, web3), often resulting in inconsistent environments and fragile setups.

Onchain Verification Complexity: Even after proof generation, verifying proofs on Arbitrum requires contract deployment, ABI handling, calldata encoding, and proper invocation — all of which are error-prone for non-specialists.

How zkArb SDK Solves This:

The zkArb SDK addresses these pain points by offering a zero-config, end-to-end workflow tailored for Arbitrum:

Fully Abstracted ZK Stack: Developers can go from writing Circom code to verifying a proof onchain with one CLI command and one JavaScript function — without needing to understand Web3 internals or snarkjs commands.

One-Command Deployment to Arbitrum: ZK verifier contracts are deployed using a simple CLI command with no Solidity, Hardhat, or RPC scripting required.

Production-Ready Structure: The SDK enforces a consistent folder structure for outputs, proof files, and contracts — making it easier to integrate into existing dApps.

Zero Web3 Knowledge Required: Developers with no blockchain or ZK background can integrate onchain privacy features into their frontend apps, lowering barriers to adoption.

Opportunities:

With zkArb SDK, Arbitrum can:

Unlock the frontend and full-stack developer audience by enabling simple ZK integration without specialized training

Enable ZK experimentation in hackathons, education programs, and internal tools

Drive adoption of Arbitrum's performant ZK verification capabilities, making it the preferred L2 for privacy-enhanced applications

Composability: How can your proposed developer tooling (existing or new) facilitate seamless interaction between different protocols and tools built on Arbitrum, the Nova ecosystem and other Orbit chains.

The zkArb SDK is designed with cross-chain and multi-environment composability in mind. As zero-knowledge use cases evolve across Arbitrum One, Nova, and Orbit chains, our tooling will support seamless integration with the broader Arbitrum ecosystem through the following mechanisms:

Unified Circuit Output Format: The SDK produces a standardized folder structure (.wasm, .zkey, verifier.sol, proof.json, public.json) that can be easily consumed by different applications, regardless of which chain they deploy to. This makes it possible for developers to use one circuit across multiple dApps or protocols.

Chain-Agnostic Deployment Module: The deploy CLI will include support for multiple RPC endpoints and network-specific configurations, allowing developers to deploy verifier contracts across Arbitrum One, Nova, and custom Orbit chains using a single unified flow.

Flexible Proof Verification Layer: The verifyProof() JavaScript function is designed to work with any deployed verifier address, making it chain-agnostic. Developers can specify the network endpoint and contract address, enabling verification from different frontends and backends interacting with different Arbitrum chains.

Orbit Compatibility (Planned): As Orbit chains begin to explore application-specific ZK circuits, zkArb SDK will allow teams to bundle and reuse circuit logic across multiple subnets. This ensures shared logic (e.g., identity proofs, Merkle membership) can be reused across ecosystem protocols.

Composable Input Handling: Future versions will include tools to serialize/deserialize circuit inputs into ABI-encoded payloads, allowing protocols to generate proofs off-chain and verify them on-chain as part of larger DeFi or gaming flows.

End Goal:
Enable developers to plug zkArb SDK into any Arbitrum-based stack — including DeFi protocols, games, identity systems, and social apps — without worrying about the chain-specific details of verifier deployment, calldata formatting, or proof verification.

Adoption: If your grant focuses on a Growth or Orbit Chain developer tool, how would you ensure its widespread adoption within the developer community.

We are focused on driving real usage of zkArb SDK by providing low-friction onboarding, education, and grassroots developer engagement through HackTour India — a leading Web3 developer community based in India. Our strategy includes:

Low-Friction Onboarding
One-command CLI flow for Circom → ZK Proof → Arbitrum verifier deployment
No prior Web3 or Solidity experience needed to use the SDK
Clear documentation and DX-focused output with human-readable CLI messaging
Example-ready project to demonstrate integration in a full-stack Next.js app

Education-Focused Growth
Developer tutorials content explaining ZK fundamentals and real-world integration using zkArb SDK
Step-by-step guides and video walkthroughs from writing a Circom circuit to verifying a proof on Arbitrum
Involvement in university programs and bootcamps to onboard first-time ZK developers

Hackathon & Campus Adoption via HackTour India
Run focused zkArb SDK tracks in Indian hackathons and university demo days
On-ground evangelism through HackTour India chapters in top tech campuses
Dedicated support for hackathon teams integrating zkArb SDK
Real-time Telegram support group and GitHub discussion for feedback loop

Community & Developer Success
Curate a growing directory of projects built using zkArb SDK
Highlight case studies where zkArb SDK helped integrate ZK verification on Arbitrum without Web3 overhead
Invite community contributors to improve the SDK through features, documentation, and template projects

Strategic Ecosystem Collaboration
Explore integration with Arbitrum-native protocols that want to add ZK features (e.g., privacy voting, anonymous credentials, zkKYC)
Build demo integrations with Orbit chains and DeFi tooling to showcase SDK use cases
Collaborate with the Arbitrum Foundation education initiatives to support developer onboarding

Growth Tracking & Feedback Loop
Actively track SDK downloads, GitHub stars, npm installs, and usage in deployed projects
Use developer surveys to capture pain points and update the SDK accordingly
Push regular SDK releases with improvements in DX, performance, and Arbitrum-specific integrations

If working on Orbit Chain Onboarding and Tooling: How would you adapt your existing developer tooling (or propose a new tool) to simplify building applications on custom Arbitrum Layer 3 chains (Orbit Chains).

While zkArb SDK is primarily focused on simplifying zero-knowledge workflows on Arbitrum One, we are designing the architecture with Orbit Chain compatibility in mind. Our tooling can be adapted to support custom Layer 3 chains through the following enhancements:

Flexible RPC Configuration:

The deploy and verifyProof modules will accept customizable RPC endpoints, allowing developers to point to any Orbit chain without needing to fork or modify core logic. This enables seamless verifier deployment and proof verification on any Orbit environment.

Chain-Agnostic Verifier Support:

Since verifier contracts generated from Circom are standardized, the SDK will allow users to compile once and deploy to multiple Orbit chains with minimal config changes — useful for app-specific chains requiring shared proof logic (e.g., identity, attestations, or access control).

Unified CLI Experience:

Developers won’t need to manage multiple toolchains or networks separately. zkArb SDK will expose a consistent CLI interface for compiling, testing, deploying, and verifying across Arbitrum One, Nova, and Orbit chains.

Instagram.

https://www.instagram.com/jatinsahijwani

If applying for a growth oriented grant: Please provide success metrics for the grant with milestone-oriented disbursements.

Yes, all milestones are structured around quantifiable KPIs and have clearly defined deliverables with week-wise timelines. Each milestone builds sequentially, with automated tooling, deployment support, developer experience, and adoption layers.

LinkedIn.

https://www.linkedin.com/in/jatinsahijwani/

Discord.

@jatinsahijwani

Others.

https://x.com/HackTourIND

Do you acknowledge that your team will be subject to a KYC requirement.

Yes

Do you acknowledge that, in case of approval, you will have to provide a report at the completion of the grant and, three months later, complete a survey about your experience.

Yes

Team experience and completeness.

Jatin Sahijwani (Project Lead):
Full-stack Web3 developer and creator of zk-polka-sdk, a zero-setup toolkit for deploying and verifying Circom-based ZK circuits on Polkadot's PolkaVM. Building on that foundation, Jatin is now leading zkArb SDK to bring similar abstraction and developer experience to Arbitrum. With hands-on expertise in Circom, snarkjs, Solidity verifiers, and zk-proof automation, he specializes in making advanced ZK workflows accessible to developers without Web3 or cryptography background. Jatin has won multiple hackathons in the ZK/Web3 space and is deeply involved in building developer infrastructure across ecosystems.

Anirudh Singh Chouhan (Frontend & UX Engineer):
Responsible for the documentation, UI/UX design, and frontend integration of zk-polka-sdk. He created the example implementation of the SDK by integrating it into a full-stack Next.js application, demonstrating real-world usage of the proof lifecycle. Anirudh brings strong frontend engineering skills and a product-first mindset, ensuring the zkArb SDK is not only technically powerful but also developer-friendly and well-documented. He will lead the design and implementation of SDK integrations, example apps, and onboarding flows tailored for Arbitrum developers.

Jatin Sahijwani (Project Lead)

Languages: Solidity, JavaScript/TypeScript, Circom
Frameworks & Tools: snarkjs, Foundry, Hardhat, Web3.js, Ethers.js
Expertise:

Zero-knowledge proof workflows (Groth16, Circom circuit compilation, verifier deployment)
Smart contract development & deployment on PolkaVM and Arbitrum
SDK/tooling development for ZK automation and abstraction
Full-stack Web3 dApp integration
Anirudh Singh Chouhan (Frontend & UX Engineer)
Languages: JavaScript/TypeScript, HTML/CSS
Frameworks & Tools: Next.js, React, TailwindCSS, Wagmi.js, Ethers.js
Expertise:

Frontend-first SDK integration and developer onboarding
UI/UX design tailored for Web3 developer tools
Documentation and example dApp implementation (proof lifecycle demos)
Building smooth onboarding flows for developers using zk SDKs
Category.

Developer Tooling