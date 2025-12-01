# Book
"Install the docusauras project using the command npx create-docusaurus@latest my-website classic --typescript
start Writing the book with the topic **Physical AI & Humanoid Robotics**. Search Online for to write these book and check only authentic and trusted websites.
Target Audience: Beginner (no prior experience in robotics or AI).
Research and Citation: Prioritize official documentation, open-source repos, academic papers, online tutorials, and reputable blogs. Use formal citation (e.g., IEEE) for academic sources and inline linking for web sources. Present only the most current and widely accepted approaches, briefly mentioning alternatives.
Content Depth for Introductions: Include definitions, brief historical context, and immediate practical relevance.
Revision Process: Continuous integration of feedback with version control tracking.
Code Examples: Must be provided in code markdown blocks. Full CMD/PowerShell commands should be given for Windows, Mac, and Linux users where applicable. Examples should demonstrate practical code and use cases."
Markdown Format: The content must be written in the markdown format

## Modules and Focus Points:
 Module 1: The Robotic Nervous System (ROS 2)
       Focus: Middleware for robot control.
       ROS 2 Nodes, Topics, and Services.
           Bridging Python Agents to ROS controllers using rclpy.
       Understanding URDF (Unified Robot Description Format) for humanoids.

 Module 2: The Digital Twin (Gazebo & Unity)
       Focus: Physics simulation and environment building.
       Simulating physics, gravity, and collisions in Gazebo.
       High-fidelity rendering and human-robot interaction in Unity.
       Simulating sensors: LiDAR, Depth Cameras, and IMUs.

 Module 3: The AI-Robot Brain (NVIDIA Isaac™)
       Focus: Advanced perception and training.
       NVIDIA Isaac Sim: Photorealistic simulation and synthetic data generation.
       Isaac ROS: Hardware-accelerated VSLAM (Visual SLAM) and navigation.
       Nav2: Path planning for bipedal humanoid movement.


  Module 4: Vision-Language-Action (VLA)
       Focus: The convergence of LLMs and Robotics.
       Voice-to-Action: Using OpenAI Whisper for voice commands.
       Cognitive Planning: Using LLMs to translate natural language ("Clean the room") into a sequence of ROS 2 actions.
       Capstone Project: The Autonomous Humanoid. A final project where a simulated robot receives a voice command, plans a path, navigates obstacles, identifies an object using computer vision, and manipulates it.

## User Scenarios & Testing

### User Story 1 - Learning ROS 2 Fundamentals (Priority: P1)

Readers will learn the core concepts of ROS 2, including nodes, topics, services, and how to bridge Python agents to ROS controllers using `rclpy`. They will also understand URDF for humanoid robot description.

**Why this priority**: ROS 2 is foundational for robotic control and is essential for understanding the subsequent modules.

**Independent Test**: Can be fully tested by successfully creating and running basic ROS 2 packages with Python and understanding URDF structures, delivering foundational knowledge.

**Acceptance Scenarios**:

1.  **Given** a basic understanding of robotics, **When** the reader completes Module 1, **Then** they can explain ROS 2 architecture and create simple ROS 2 nodes in Python.
2.  **Given** a URDF file, **When** the reader reviews Module 1 content, **Then** they can identify the components and their relationships within a humanoid robot model.

---

### User Story 2 - Simulating Digital Twins (Priority: P1)

Readers will learn to create and simulate digital twins of humanoid robots using Gazebo for physics simulation and Unity for high-fidelity rendering and human-robot interaction. They will also understand how to simulate various sensors.

**Why this priority**: Digital twins are crucial for safe and efficient development and testing of robotic systems without needing physical hardware.

**Independent Test**: Can be fully tested by successfully setting up a Gazebo and Unity simulation environment, spawning a robot, and simulating basic sensor outputs, delivering practical simulation skills.

**Acceptance Scenarios**:

1.  **Given** a robot model, **When** the reader completes Module 2, **Then** they can set up a Gazebo environment and run a physics simulation.
2.  **Given** a Unity environment, **When** the reader completes Module 2, **Then** they can integrate a robot model for high-fidelity visualization and basic interaction.

---

### User Story 3 - Developing AI-Robot Brains (Priority: P2)

Readers will explore advanced AI for robotics using NVIDIA Isaac Sim for photorealistic simulation and synthetic data generation, Isaac ROS for hardware-accelerated perception and navigation, and Nav2 for bipedal path planning.

**Why this priority**: This module introduces cutting-edge AI techniques crucial for autonomous humanoid behavior.

**Independent Test**: Can be fully tested by implementing a basic perception pipeline using Isaac ROS and demonstrating path planning for a bipedal robot in a simulated environment, delivering advanced AI integration skills.

**Acceptance Scenarios**:

1.  **Given** a simulated environment, **When** the reader completes Module 3, **Then** they can use NVIDIA Isaac Sim to generate synthetic data for training.
2.  **Given** a navigation task for a bipedal robot, **When** the reader applies Nav2 concepts, **Then** the robot can plan and execute a path while avoiding obstacles.

---

### User Story 4 - Integrating Vision-Language-Action (VLA) (Priority: P2)

Readers will learn how to converge LLMs and robotics, enabling voice-to-action commands using OpenAI Whisper and cognitive planning to translate natural language into ROS 2 actions for autonomous humanoids.

**Why this priority**: VLA represents a significant step towards more intuitive and capable human-robot interaction.

**Independent Test**: Can be fully tested by integrating OpenAI Whisper for voice commands and demonstrating an LLM translating a natural language command into a sequence of simulated robot actions, delivering advanced HRI skills.

**Acceptance Scenarios**:

1.  **Given** a voice command, **When** the reader implements the VLA concepts, **Then** the robot can recognize the command using OpenAI Whisper and initiate a corresponding action.
2.  **Given** a natural language instruction (e.g., "Clean the room"), **When** the reader integrates LLMs for cognitive planning, **Then** the robot can generate a sequence of ROS 2 actions to achieve the task.

---

### User Story 5 - Capstone Project (Priority: P1)

Readers will apply all learned concepts to a capstone project where a simulated robot receives a voice command, plans a path, navigates obstacles, identifies an object using computer vision, and manipulates it.

**Why this priority**: The capstone project is the ultimate demonstration of integrated knowledge and practical application.

**Independent Test**: Can be fully tested by running the complete simulated autonomous humanoid demonstration, receiving a voice command, executing the full sequence of actions, and manipulating an object successfully, delivering a comprehensive project outcome.

**Acceptance Scenarios**:

1.  **Given** a simulated environment and a voice command, **When** the autonomous humanoid is activated, **Then** it plans a path, navigates to a target, identifies an object, and manipulates it as instructed.

---

### Edge Cases

- What happens when a sensor fails or provides noisy data during simulation?
- How does the system handle ambiguous or out-of-scope voice commands?
- What if the robot encounters an unexpected obstacle not present in its map during navigation?
- How does the system recover from unexpected physics engine glitches in Gazebo or Unity?

## Requirements

### Functional Requirements

- **FR-001**: The book MUST provide clear and comprehensive explanations of ROS 2 concepts.
- **FR-002**: The book MUST guide the reader through setting up Gazebo and Unity for digital twin simulation.
- **FR-003**: The book MUST cover the integration and usage of NVIDIA Isaac Sim, Isaac ROS, and Nav2.
- **FR-004**: The book MUST explain the convergence of LLMs and robotics for Vision-Language-Action capabilities.
- **FR-005**: The book MUST include a step-by-step guide for the Capstone Project.
- **FR-006**: The book MUST provide reproducible code examples and snippets for all modules.
- **FR-007**: The book MUST ensure a logical and coherent progression of topics.
- **FR-008**: The book MUST instruct on deploying the Docusaurus project to GitHub Pages.
- **FR-009**: The book MUST demonstrate effective use of Docusaurus features for content structuring and navigation.
- **FR-010**: The book MUST detail hardware requirements for successfully following the course material.

### Key Entities

- **Module**: A distinct section of the book focusing on a specific technological area (e.g., ROS 2, Digital Twin).
- **Chapter**: A subdivision within a module, covering specific topics.
- **Concept**: A fundamental idea or technique explained within a chapter.
- **Code Example**: A short, runnable snippet demonstrating a concept.
- **Simulation Environment**: The virtual space where robots operate (Gazebo, Unity, Isaac Sim).
- **Robot Model**: A digital representation of a humanoid or proxy robot (URDF, USD).
- **Sensor**: Devices providing data to the robot (LiDAR, Depth Camera, IMU).
- **AI Model**: Machine learning models used for perception, planning, or language processing.

## Success Criteria

### Measurable Outcomes

- **SC-001**: Readers can articulate core ROS 2 concepts and build basic ROS 2 Python packages upon completing Module 1.
- **SC-002**: Readers can successfully set up and run digital twin simulations in both Gazebo and Unity after completing Module 2.
- **SC-003**: Readers can integrate NVIDIA Isaac components for perception and navigation, and implement bipedal path planning upon completing Module 3.
- **SC-004**: Readers can integrate voice commands and LLM-based cognitive planning for robot actions after completing Module 4.
- **SC-005**: The Capstone Project is successfully demonstrated as a fully autonomous humanoid responding to voice commands in simulation.
- **SC-006**: All code examples provided are reproducible and function as described by 95% of readers with the recommended setup.
- **SC-007**: The Docusaurus book is successfully deployed to GitHub Pages and accessible via a public URL, with 100% of core content rendering correctly.
- **SC-008**: The book's Docusaurus navigation, search, and content organization are rated as intuitive and effective by reader feedback.
- **SC-009**: The book is structured into the specified preface, 5 parts (including introduction and 4 modules), and assessments and also requirements, with clear chapter subdivisions.

## Constraints

### Content Constraints:
  - **Target Audience**: Beginner (no prior experience in robotics or AI).
  - Technical Depth: Balancing detailed technical explanations with accessibility for a broader audience.
  - Research and Citation: Prioritize official documentation, open-source project repositories, academic papers, online tutorials, and reputable blog posts. Use formal citation (e.g., IEEE style) for academic sources and inline linking for web sources. Present only the most current and widely accepted approach, briefly mentioning alternatives as deprecated or less common.
  - **Content Depth for Introductions**: Include definitions, brief historical context, and immediate practical relevance.
  - Software Versions: Ensuring compatibility and relevance across different versions of ROS 2, Gazebo, Unity, NVIDIA Isaac Sim/ROS, and other tools.
  - Hardware Requirements: Acknowledging that some advanced simulations (e.g., NVIDIA Isaac Sim) may require specific hardware (GPUs), which could be a barrier for some readers.
  - Pace of Technology: Keeping the content up-to-date with the rapid advancements in AI, robotics, and related software.
  - Scope Management: Avoiding feature creep and ensuring the book remains focused on the defined modules.

### Docusaurus Constraints:
  - Markdown Limitations: Potential limitations or workarounds needed for complex layouts or interactive elements that are not natively supported by Markdown.
  - Customization: The extent to which Docusaurus can be customized to achieve a unique visual design or specific functionalities.
  - Learning Curve: The effort required to learn Docusaurus for content creation and site management.

### GitHub Pages Deployment Constraints:
  - Build Time Limits: GitHub Pages might have build time limits for complex Docusaurus sites.
  - Storage Limits: While generous, there are storage limits for GitHub Pages repositories.
  - Custom Domain Configuration: Any complexities in setting up a custom domain (if desired).
  - Jekyll Dependency: Ensuring Docusaurus builds correctly with GitHub Pages' Jekyll processing (or disabling Jekyll if needed).

### Revision Process:
  - Continuous integration of feedback with version control tracking.

## Learning Outcomes

- Understand Physical AI principles and embodied intelligence.
- Master ROS 2 (Robot Operating System) for robotic control.
- Simulate robots with Gazebo and Unity.
- Develop with NVIDIA Isaac AI robot platform.
- Design humanoid robots for natural interactions.
- Integrate GPT models for conversational robotics.

## Content of book in Book format:

- Separate each module so that there would be five (one of intro which will not be further divided) parts and some other bonus parts.
- Divide These book chapters as follows and also divide the chapters into the sub-topics.

### Preface:
- Why Physical AI Matters
- Learning outcomes of this books

### Part 1 (Introduction to Physical AI):
- Chapter 1: Foundations of Physical AI and embodied intelligence
- Chapter 2: From digital AI to robots that understand physical laws
- Chapter 3: Overview of humanoid robotics landscape
- Chapter 4: Sensor systems: LIDAR, cameras, IMUs, force/torque sensors

### Part 2 (Module 1: The Robotic Nervous System (ROS 2)):
- Chapter 5: ROS 2 architecture and core concepts
- Chapter 6: Nodes, topics, services, and actions
- Chapter 7: Building ROS 2 packages with Python
- Chapter 8: Launch files and parameter management
- Chapter 9: URDF and SDF robot description formats

### Part 3 (Module 2: The Digital Twin (Gazebo & Unity)):
- Chapter 10: Gazebo simulation environment setup
- Chapter 11: Physics simulation and sensor simulation
- Chapter 12: Introduction to Unity for robot visualization

### Part 4 (Module 3: The AI-Robot Brain (NVIDIA Isaac™)):
- Chapter 13: NVIDIA Isaac SDK and Isaac Sim
- Chapter 14: AI-powered perception and manipulation
- Chapter 15: Reinforcement learning for robot control
- Chapter 16: Sim-to-real transfer techniques

### Part 5 (Module 4: Vision-Language-Action (VLA)):
- Chapter 17: Humanoid robot kinematics and dynamics
- Chapter 18: Bipedal locomotion and balance control
- Chapter 19: Manipulation and grasping with humanoid hands
- Chapter 20: Natural human–robot interaction design
- Chapter 21: Integrating GPT models for conversational AI in robots
- Chapter 22: Speech recognition and natural language understanding
- Chapter 23: Multimodal interaction: speech, gesture, vision

### Assessments:
- ROS 2 package development project
- Gazebo simulation implementation
- Isaac-based perception pipeline
- Capstone: Simulated humanoid robot with conversational AI

### Hardware Requirements

1.  Introduction: Explain why the course requires heavy hardware: physics simulation (Isaac Sim/Gazebo), visual perception (SLAM/CV), and generative AI (LLMs/VLA). State that high-performance workstations and edge kits are essential.

2.  Section: “The Digital Twin Workstation (Required per Student)”
    - GPU: NVIDIA RTX 4070 Ti minimum; ideal 3090/4090 (24GB VRAM).
    - CPU: Intel Core i7 (13th Gen+) or AMD Ryzen 9.
    - RAM: 64 GB DDR5 (32 GB minimum but unstable).
    - OS: Ubuntu 22.04 LTS; ROS 2 prefers Linux.
    - Explain RTX-only Omniverse/Isaac requirements.

3.  Section: “The Physical AI Edge Kit”
    - NVIDIA Jetson Orin Nano 8GB or Orin NX 16GB (brain).
    - Intel RealSense D435i/D455 (vision).
    - Generic USB IMU (BNO055) for balance.
    - ReSpeaker USB Mic Array v2.0 for voice input.
    - Explain purpose: running inference and robotics AI locally.

4.  Section: “The Robot Lab”
    Include all 3 tiers:
    - Option A (Budget Proxy): Unitree Go2 Edu; pros/cons.
    - Option B (Mini Humanoids): Unitree G1, Robotis OP3, Hiwonder TonyPi (with warning about Raspberry Pi limitations).
    - Option C (Premium Sim-to-Real): Unitree G1 Humanoid with open SDK.

5.  Section: “Summary of Architecture”
    Include table mapping:

| Component | Hardware | Function |
| :---- | :---- | :---- |
| **Sim Rig** | PC with RTX 4080 + Ubuntu 22.04 | Runs Isaac Sim, Gazebo, Unity, and trains LLM/VLA models. |
| **Edge Brain** | Jetson Orin Nano | Runs the "Inference" stack. Students deploy their code here. |
| **Sensors** | RealSense Camera + Lidar | Connected to the Jetson to feed real-world data to the AI. |
| **Actuator** | Unitree Go2 or G1 (Shared) | Receives motor commands from the Jetson. |

6.  Section: Cloud-Native Option (“The Ether Lab”)
    - AWS g5.2xlarge or g6e.xlarge for Isaac Sim.
    - Cost: ~$1.50/hr, ~120 hrs = ~$205/quarter.
    - Explain need for local Jetson + single robot even in cloud workflows.

7.  Section: “The Economy Jetson Student Kit”
    Include table:

| Component | Model | Price (Approx.) | Notes |
| :---- | :---- | :---- | :---- |
| **The Brain** | **NVIDIA Jetson Orin Nano Super Dev Kit (8GB)** | **$249** | New official MSRP (Price dropped from ~$499). Capable of 40 TOPS. |
| **The Eyes** | **Intel RealSense D435i** | **$349** | Includes IMU (essential for SLAM). Do not buy the D435 (non-i). |
| **The Ears** | **ReSpeaker USB Mic Array v2.0** | **$69** | Far-field microphone for voice commands (Module 4). |
| **Wi-Fi** | (Included in Dev Kit) | $0 | The new "Super" kit includes the Wi-Fi module pre-installed. |
| **Power/Misc** | SD Card (128GB) + Jumper Wires | $30 | High-endurance microSD card required for the OS. |
| **TOTAL** | | **~$700 per kit** | |

8.  Section: Latency Trap
    - Explain that real robots cannot be controlled directly from the cloud.
    - Must train on cloud → download weights → deploy on Jetson.

# Chatbot and RAG pipeline
A RAG chatbot for the above book which will answer the queries of user but will not answer the questions not related with the book. RAG pipeline must be setup of the above book

## Focus Points
  - Data Ingestion and Indexing: Efficiently processing the book's content (text, possibly images/diagrams) and storing it in Qdrant (vector database) in a way that allows for effective retrieval. This includes chunking strategies, metadata extraction, and embedding generation.
  - Retrieval Mechanism: Designing and implementing how the chatbot identifies and fetches the most relevant sections of the book based on a user's
  question, especially the "text selected by the user" feature. This is crucial for the "R" in RAG.
  - Prompt Engineering and LLM Integration: Effectively integrating with the OpenAI Agents/ChatKit SDKs and FastAPI to construct prompts that leverage the
   retrieved context to generate accurate and relevant answers. This includes handling cases where context is limited or ambiguous.
  - Contextual Understanding (Selected Text): Specifically addressing the requirement to answer questions based only on text selected by the user. This
  means the chatbot needs to be able to isolate and interpret the provided text snippet accurately.
  - Scalability and Performance: Ensuring the FastAPI backend, Neon Serverless Postgres, and Qdrant Cloud Free Tier can handle expected user load and
  provide timely responses.
  - Accuracy and Relevance: The ultimate goal is for the chatbot to provide highly accurate and relevant answers directly from the book's content,
  minimizing hallucinations and irrelevant information.
  - User Experience and Embedding: Seamlessly embedding the chatbot within the published book's UI and ensuring a smooth, intuitive user interaction.
    - UI Placement: The chatbot will be located in the bottom corner of the book's UI.
    - Initial State: Normally, it will appear as a button (chatbot logo).
    - Interaction: When the button is clicked, a small dialog box will open, serving as its UI.
    - Customizable Size: The size of the dialog box will be customizable, allowing users to resize it by dragging its edges.
  - Error Handling and Robustness: Implementing robust error handling for API calls, database interactions, and unexpected inputs to provide a stable
  experience.
  - Security and Data Privacy: Protecting user queries and ensuring data handled by FastAPI and Neon Postgres is secure.

## Constraints
  - Technology Stack and purpose:
    - OpenAI Agents/ChatKit SDKs
    - FastAPI (Initial Filter: The selected text is sent to $\text{FastAPI}$ as the primary context. 2. Verification (Retrieval Fallback): The selected text is used as a query to retrieve its immediate surrounding context (e.g., 2-3 overlapping chunks) from $\text{Qdrant}$. 3. Prompt Construction: The $\text{LLM}$ prompt is strictly instructed: "Analyze the user's question only in the context of the Selected Text (Primary Context) and its verified Surrounding Context (Secondary Context). Do not use external knowledge.")
    - Neon Serverless Postgres database (Neon Serverless Postgres will be used to store and manage user session context and conversation history. This ensures that multi-turn questions are supported by passing the last 'N' turns of the conversation history to the FastAPI request, fulfilling the conversational context requirement.It will also be used to store the login records)
    - Qdrant Cloud Free Tier(vector datab)
    - OpenAI Chatkit (for UI and connection with the book)
  - Core Functionality: Must be able to answer user questions about the book's content.
  - Specific Functionality: Must be able to answer questions based only on text selected by the user.
  - Scope of Answers: Must not answer questions outside the book's content.
  - Deployment: Embedded within the published book.
  - Must use the RAG pipeline of the above

# Login/Signup System

## Overview
This system provides secure user authentication and personalized content delivery for the book.

## Functional Requirements

### Login Page
- **LS-FR-001**: The login page MUST allow users to log in using their email and password.
- **LS-FR-002**: The login page MUST include a "Forgot Password" option to initiate password reset.
- **LS-FR-003**: The system MUST implement robust authentication mechanisms (e.g., password hashing, secure session management) to ensure "better auth".

### Signup Page (Step 1: Account Creation)
- **LS-FR-004**: The signup page (first step) MUST prompt users for their email, password, and confirmation password.
- **LS-FR-005**: The system MUST enforce strong password policies (e.g., minimum length, complexity requirements).
- **LS-FR-006**: The system MUST verify that the password and confirm password fields match before proceeding.
- **LS-FR-007**: A "Next" button MUST be present to proceed to the second step of the signup process.

### Signup Page (Step 2: Profile Personalization)
- **LS-FR-008**: The signup page (second step) MUST ask users about their experience in physical AI and humanoid robotics with predefined options which are Expert, Intermediate, Begginer.
- **LS-FR-009**: The signup page (second step) MUST ask users about their hardware background with 5-6 predefined options.
- **LS-FR-010**: The signup page (second step) MUST allow users to select their expertise level (e.g., Beginner, Intermediate, Advanced).
- **LS-FR-011**: The collected background and expertise level data MUST be stored to enable content personalization.

### Book Page Features
- **LS-FR-014**: The sign-in/sign-up button MUST be located in the top corner of every page.
- **LS-FR-015**: After successful sign-up/login, the user's name MUST be displayed instead of the sign-in/sign-up button. Clicking the user's name MUST open a dropdown with two options: "Sign Up" and "Change Experience Level". The "Change Experience Level" option MUST send the updated experience to the chatbot for personalization.
- **LS-FR-012**: A dedicated button MUST be present on each book page to trigger content personalization. When clicked, the page content MUST be sent to the chatbot for editing according to the user's experience. The updated content MUST be displayed, but revert to normal after refreshing the page.

- **LS-FR-013**: A dedicated button MUST be present on each book page to translate the content into Urdu.

## Non-Functional Requirements
- **LS-NFR-001**: **Security**: The system MUST protect against common web vulnerabilities (e.g., SQL injection, XSS, CSRF).
- **LS-NFR-002**: **Authentication Strength**: Passwords MUST be stored securely using industry-standard hashing algorithms (e.g., bcrypt, Argon2).
- **LS-NFR-003**: **User Data Privacy**: Personalization data MUST be stored and handled in compliance with relevant data privacy regulations.

## Technical Considerations
- **Authentication Framework**: A robust, secure authentication framework will be implemented, prioritizing industry best practices for password hashing, secure session management, and protection against common vulnerabilities. (Further definition of specific framework to be determined, focusing on achieving "better auth".)
- **Database Schema**: Design for user profiles, including personalization data, login information, and signup/login records, all stored in Neon Serverless Postgres.
- **Personalization Logic**: The system will dynamically alter book content based on the user's software/hardware background and expertise level, and experience in physical AI and humanoid robotics. The chatbot will be used to edit content, and these personalized changes will be temporary, reverting upon page refresh. The 'Change Experience Level' option will send updated experience data to the chatbot for further personalization.
- **Translation Service**: Urdu translation will be handled by integrating with the RAG Chatbot's underlying language model, which will modify the content of the opened book pages directly (not within the chatbot UI).