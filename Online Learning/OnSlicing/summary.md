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

## 🔬 3. Setup & Experiment Details
- **Datasets used**:  Used hardware to create node in the network layers; and traffic traces [https://doi.org/10.1038/sdata.2015.55] for network traffic; custom applications emulating slices
- **Architecture / Algorithm**:
  - Onslice manager: virtualizes physical resources and performs the action for resource allocation
  - Onslice orchestrator: consists of onslice agents (1 per slice) which allocate resources in the nodes
      - Onslice agents are constraint-aware (SLA violations)
      - Can switch to baseline (rule-based) when the predicted future cost will violate SLA, ensuring _no_ violations
      - Modifies action in such a way allocate resource do not exceed the current capacity
- **Training tricks / Hyperparameters (if given)**:
  - Policy trained using behaviour cloning (offline from baseline) and PPO
  - Small network architecture insspired from OpenAirInterface [https://openairinterface.org/]
- **Evaluation metrics**:  Average resource utilization (%) and SLA violations(%)

---

## 📊 4. Results
- **How well did it perform? Compared to what?**
  <br>→ Was the best in both the metrics
- **Any strong baselines beaten?**
  <br>→ Particularly no, tweaked the popular OnRL [https://www.doi.org/10.1145/3372224.3419186] to fit the use case
- **Was the improvement significant or just marginal?**
  <br>→ The results in itself are pretty good and back the claims of the researchers

---

## ⚠️ 5. Limitations / Weaknesses
- **What does it assume?**
  <br>→ No particular assumptions given, but the testing architecture is (very) small and traffic data rates are low
- **Where does it break?**
  <br>→ It might break in a large network, while trying to handle multiple agents and scaling domain managers to multiple nodes. Too many policies involved can it lead to overfitting?
- **What’s missing?**
  <br>→ N/A, couldn't point out

---

## 💡 6. Key Takeaways  
🔹 **Big idea**: individualized agents for each slice; online drl <br>
🔹 **What makes it different**: ensures minimumum SLA violations <br>
🔹 **Why it matters**: maximum resource utilization

