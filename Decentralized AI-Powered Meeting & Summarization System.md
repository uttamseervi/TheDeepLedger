**Decentralized AI-Powered Meeting & Summarization System**

---

### **Overview**
Develop a decentralized, AI-powered meeting platform where users can **initiate meetings, invite participants via a shareable link, and join using their crypto wallets**. The platform will **transcribe and analyze conversations in real time, store raw speech data securely, and generate AI-powered summaries** at intervals or upon request. Finalized summaries will be **stored on a blockchain** for tamper-proof verification.

This system is **entirely audio-based**, meaning all interactions are voice-driven. Additionally, it provides **AI-generated prompts** if required, ensuring smoother conversation flow and structured discussions.

---

### **Core Functionalities**

#### **1. Meeting Initiation & Participation**
- Any user can start a meeting and generate a **unique shareable link**.
- Participants **join using their wallet address** (via **MetaMask, WalletConnect**).
- No traditional sign-ups—**wallet authentication serves as identity**.

#### **2. Real-Time Speech Processing & AI Summarization**
- **AI transcribes and processes** conversations in real time.
- When a participant speaks, their **wallet address is linked** to their speech.
- AI can **generate summaries at intervals** (if needed) or at the end.
- AI can also **provide contextual prompts** during discussions if required.

#### **3. Data Storage & Security**
- **Raw speech data & transcripts are stored securely** (**IPFS/Filecoin/Arweave**).
- AI summaries are **hashed and stored on the blockchain** for **tamper-proof verification**.

#### **4. Real-Time Speaker Highlighting (Google Meet Style)**
- Active speakers are **detected in real time** (via **WebSockets & AI**).
- Their **wallet-linked identity** is temporarily highlighted on the UI.

---

### **Handling Audio Processing Under the Hood**

1. **Real-Time Speech Detection & Processing**  
   - **Microphone Capture**: Audio streams are captured in real time from participants.
   - **AI-Based Speaker Recognition**: **Pyannote, Google ASR, Whisper AI** are used to differentiate speakers.
   - **Speech-to-Text Conversion**: AI converts spoken words into text in real-time.
   - **Speaker Wallet Mapping**: Each transcribed segment is tagged with the speaker's **wallet address**.

2. **Storage & Security**  
   - **Raw Audio & Transcripts**: Stored in decentralized storage (**IPFS, Filecoin, or Arweave**).
   - **Blockchain Summary Storage**: Summaries are hashed and stored on **Ethereum/Polygon**.
   - **Verification**: Users can verify summaries against original transcripts using **blockchain records**.

3. **AI-Generated Prompts & Summarization**  
   - **AI listens for discussion gaps** and provides contextual **prompts** when needed.
   - **AI summarizes key points** at periodic intervals and upon meeting completion.

4. **Real-Time UI Updates**  
   - **WebSockets handle real-time speaker updates**, ensuring that the **active speaker is dynamically highlighted**.
   - **AI continuously updates transcripts and generates real-time insights.**

---

### **Tech Stack & Frameworks Used**

#### **Frontend (User Interface)**
- **React.js / Next.js** → UI framework with Web3 integration
- **WebSockets** → Enables real-time updates & speaker highlighting
- **MetaMask / WalletConnect** → Facilitates wallet authentication

#### **Backend (Processing & Storage)**
- **Node.js (Express / Fastify)** → Handles API & WebSocket communication
- **Google Speech-to-Text / Pyannote / AssemblyAI** → Transcription & speaker diarization
- **IPFS / Arweave / Filecoin** → Decentralized transcript & audio storage

#### **Blockchain Integration**
- **Ethereum / Polygon Smart Contracts** → Stores conversation summaries securely
- **On-chain verification** → Ensures summary **matches the raw transcript**

#### **Additional Tools & Services**
- **Whisper AI** → Advanced speech-to-text model
- **Web3.js / Ethers.js** → Blockchain interaction & smart contract integration
- **Socket.io** → Manages real-time communication

---

### **Expected Outcome**
✅ **Decentralized Google Meet alternative** with **Web3 authentication**  
✅ **AI-powered live transcription & speaker identification**  
✅ **Tamper-proof, verifiable summaries stored on blockchain**  
✅ **Speaker tracking without revealing personal details (only wallet-linked identities)**  
✅ **Fully decentralized storage & computation**  
✅ **AI-generated prompts enhance conversations**  

---


