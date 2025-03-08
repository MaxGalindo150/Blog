### **AI That "Reasons"... But Does It Really?**

Artificial intelligence seems to be advancing at a rapid pace, with new models that supposedly "reason." However, if we analyze the situation with a cold, rational mind, we realize that we are still in the same place we were 10 years ago.

Why don’t we fully trust autonomous cars yet? Why don't we have robotic assistants in our daily lives if our models are supposed to be capable of reasoning? The answer lies in the fundamental limitations of current AI systems.

---

## 🔍 A Look at AI Progress

Since the advent of **transformers** in 2017, artificial intelligence has gained massive popularity. Previously, the field was confined to researchers and professionals using *machine learning* for statistics and data analysis. Then, **OpenAI** launched **ChatGPT**, which, to the general public, seemed like magic: you enter a prompt, and the computer responds in a way that mimics human conversation.

However, at its core, these models are relatively simple. In essence, they predict the next word based on the previous context. This boils down to modeling a **conditional probability**:

$$ P(w_t | w_{t-1}, w_{t-2}, ..., w_1) $$

Over time, researchers found that increasing dataset diversity, model size, and training scales led to emergent capabilities like **meta-learning** and **few-shot learning**. This evolution gave rise to **ChatGPT** and even more advanced models.

Then came **o1**, OpenAI’s first "reasoning" model. Shortly after, Chinese AI company **DeepSeek** introduced their own model, equaling or even surpassing **o1** in several benchmarks. The most remarkable aspect? DeepSeek achieved this with **fewer computational resources** and released their model as **open-source**, igniting excitement within the AI research community.

This marked the beginning of a new race: the competition to develop the best reasoning model.

---

## 🎯 GRPO: Teaching AI to "Reason" with Reinforcement Learning

DeepSeek made this breakthrough by leveraging **Reinforcement Learning (RL)**, introducing an algorithm called **GRPO (Group Relative Policy Optimization)**—a variant of the well-known **PPO (Proximal Policy Optimization)**. PPO is a popular algorithm in RL that helps models improve their performance by optimizing policies in a stable and efficient manner.

GRPO’s reward system operates on two key components:

- **Accuracy Rewards:** Evaluates whether the model’s response is correct. For problems like math or coding challenges (*LeetCode*), this can be objectively verified.
- **Format Rewards:** Encourages the model to generate reasoning steps enclosed within **`<think>` ... `<think>`** tags.

This approach is intriguing because the model **learns to generate more tokens within these tags** to maximize its reward. The result? A model that outputs long reasoning chains before reaching a final answer. If you want to learn more about this, check out the [Reinforcement Learning In LLMs](https://app.gitbook.com/o/Yp4DzKrc4S9EklIKkZ4K/s/vedEAf8lekeEqjv4WpBU/dive-deeper/rl-in-llms) article.

---

## 🤔 Is This Really Reasoning?

If we break it down, this process is **similar to a search algorithm**: the model generates different token sequences and selects the one that maximizes its reward function. This mirrors traditional **pathfinding algorithms**, such as **A* or Dijkstra**, which explore multiple paths before selecting the optimal one.

The problem? **Generating and evaluating thousands of tokens is computationally expensive.** Fundamentally, we are still doing what we did in 2017—just in a more efficient and structured way.

The so-called "reasoning" in these models is **primitive and brute-force-driven**. Their "thought process" happens in an **abstract token space**, not the real world. For example, if you ask an AI model whether a cube will still look like a cube after rotating it 90°, it may generate tokens that simulate reasoning and arrive at the correct answer. However, it lacks true **spatial understanding**. It doesn’t *visualize* the cube rotating as a human would; it merely predicts the most likely response based on text patterns seen during training.

---

## 🔄 Contrast with Human Reasoning

Human reasoning is fundamentally different from AI’s so-called reasoning. Here’s why:

### Mental Models & Internal Simulations

Humans build mental models of the world. If you imagine a ball rolling down a hill, you can visualize the scene, predict its trajectory, and understand gravity’s effects.

AI models, on the other hand, lack any internal understanding of the physical world. They merely predict token sequences based on statistical patterns.

### Common Sense

Humans use common sense to make quick and effective decisions in novel situations. For example, we instinctively know that a glass of water will spill if tilted too much.

AI models lack common sense. They can generate plausible responses but don’t truly understand underlying concepts. A model might even suggest that a glass of water could float if it hasn't been exposed to enough examples related to gravity.

### Generalization & Adaptability

Humans excel at generalizing knowledge across different domains. If we learn to ride a bicycle, we can apply that balance to rollerblading.

AI models struggle with generalization. A model trained in algebra may solve equations efficiently but fail to apply its knowledge to a physics problem without specific training.

### Creativity & Abstract Thinking

Humans can think abstractly and create new ideas. We can imagine fictional worlds, invent stories, and solve problems in innovative ways.

AI models can only recombine information they have been trained on. They cannot truly "imagine" something entirely new.

### Context Awareness

Humans understand context and intent behind words. We can detect irony, sarcasm, or metaphorical meanings effortlessly.

AI models can recognize language patterns suggesting sarcasm or irony, but they don’t actually comprehend the deeper meaning behind these expressions.

---

### **Why This Matters: Real-World Implications**

The limitations of current AI models have significant implications for real-world applications. For instance:

- **Autonomous Vehicles**: These systems require not just pattern recognition but also the ability to reason about complex, dynamic environments. Current AI struggles with tasks that require **common sense** or **anticipating unexpected events**.
- **Robotic Assistants**: While AI can perform specific tasks well, it lacks the **generalization** and **adaptability** needed for real-world interactions. For example, a robot might fail to understand context or make decisions in unpredictable scenarios.

---

## 🚀 The Future of AI: Beyond Text Generation

Language models remain **clumsy**, albeit incredibly good at predicting the next word. Our challenge as AI researchers is to **develop new training strategies** that push models beyond simple token prediction and toward **true reasoning and common sense**. Only then can we make real progress toward **intelligent agents, robots, autonomous vehicles, and other groundbreaking technologies**.

**Reasoning and consciousness are two entirely different concepts.** Reasoning involves planning and decision-making based on a belief system, while consciousness is an elusive phenomenon that remains difficult to define or measure.

---

### **EigenCore: Bridging Research and Real-World AI**

At **EigenCore**, we are working to push AI beyond mere text generation. Our mission is to build intelligent systems applicable to the real world—closing the gap between academic research and industrial applications.

If you are passionate about AI and want to collaborate, **reach out**, and let’s discuss the future of artificial intelligence. ✌️

---

### **Final Thoughts**

While AI has made remarkable progress, it’s important to recognize its current limitations. True reasoning requires more than just predicting the next word—it demands **understanding, generalization, and adaptability**. As we continue to innovate, we must focus on developing models that can truly reason and interact with the world in meaningful ways.

What do you think? Is AI on the brink of true reasoning, or are we still far from achieving it? Let’s keep the conversation going. 🚀

---

### **Referencias y lecturas recomendadas**:
- [Reinforcement Learning In LLMs](https://app.gitbook.com/o/Yp4DzKrc4S9EklIKkZ4K/s/vedEAf8lekeEqjv4WpBU/dive-deeper/rl-in-llms)
- [DeepSeek’s Open-Source Model](https://www.deepseek.com)
- [PPO Algorithm Explained](https://openai.com/blog/openai-baselines-ppo)
