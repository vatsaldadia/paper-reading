# 🧠 Research Paper Summary

---

## 📄 0. Paper Info
- **Title**:  OnSlicing: Online End-to-End Network Slicing with Reinforcement Learning
- **Authors**:  Q. Liu, et. al.
- **Year**:  2021
- **Conference/Journal**:  Conference on emerging Networking EXperiments and Technologies (CoNEXT)
- **Link to paper**:  https://doi.org/10.48550/arXiv.2111.01616
- **Read date**:  May 6, 2025

> Initial thoughts: Too many things proposed, but are all novel? Seems a good approach, granular control over many things, will be interesting to see how is everything tied up. Results seem to good to be true.

---

## 🚀 1. What’s the Point?
**What problem does this paper solve, and why is it important?**  

The paper introduces a online drl solution to e2e (ran - tn - core - en) network slicing. Slicing allows operators to virtualize the physical insfrastruture to meet the QoS of different slices in 5G. Rule-based systems don't ensure maximum utilization, and offline learing methods fail to show results in real networks as they are often trained on simulations. Current online approaches fail to comply to SLA for all slices at all times specially at the start when they are still capturing context. The given solution handles all the given problems.

---

## 🧠 2. The Core Idea
**What’s the main idea, approach, or innovation in one sentence?**

The main idea is minimize the usage of virtual resources in all the layers while not violating the individual slice SLA.

---

## 🔬 3. Setup & Experiment Details (Fill after *Methods + Experiments section*)  
- **Datasets used**:  
- **Architecture / Algorithm**:  
- **Training tricks / Hyperparameters (if given)**:  
- **Evaluation metrics**:  

> ✅ **Checkpoint:** Can you sketch the pipeline on paper or explain it out loud?

---

## 📊 4. Results (Fill after *Results section*)  
- **How well did it perform? Compared to what?**  
- **Any strong baselines beaten?**  
- **Was the improvement significant or just marginal?**

---

## ⚠️ 5. Limitations / Weaknesses (Skim *Discussion or Conclusion*)  
- **What does it assume?**  
- **Where does it break?**  
- **What’s missing?**

> ⚠️ If the authors didn’t mention it, think critically — **no model is perfect**.

---

## 💡 6. Key Takeaways (Do this last)  
Summarize the whole paper into 3 short bullets:
- 🔹 Big idea  
- 🔹 What makes it different  
- 🔹 Why it matters  

---

## 🎙️ 7. “Explain it to someone” Drill (Final checkpoint)
**Q: What’s this paper about?**  
→ _1-2 sentences._  
**Q: Why is it interesting?**  
→ _1-2 sentences._  
**Q: How is it different from prior work?**  
→ _1-2 sentences._

> 🔁 Repeat this from memory 2 days later. If you blank out, revisit the summary — don't reread the full paper.

---

## 🧪 8. How (or if) I can use this (Optional — after thinking a bit)
- Could I implement this in code?  
- Could I apply this to my dataset/project?  
- What toy version of this can I try?
