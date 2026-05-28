A Siamese network is a type of neural network architecture designed to compare two inputs and measure how similar they are, rather than classify each input independently.

🧠 Core idea of the project
update this 
Instead of learning “what is this?”, it learns “are these two things the same (or similar)?”

It consists of:

Two identical subnetworks (same architecture, shared weights)
Each processes one input
Outputs are compared using a distance metric (e.g., Euclidean distance)
⚙️ How it works
Input pair: (x1, x2)
Both pass through the same network → produce embeddings:
f(x1)
f(x2)
Compute similarity:
Distance: ||f(x1) - f(x2)||
Train using:
Contrastive Loss or triplet loss
🧩 Why “Siamese”?

The name comes from Chang and Eng Bunker (conjoined twins), because the two networks are identical and connected.

📌 Key features
Shared weights → consistent feature extraction
Learns embeddings (feature vectors)
Works well with limited labeled data
Focuses on relative similarity, not absolute labels
🔍 Common applications
Face verification (e.g., “are these two faces the same?”)
Signature verification
Image similarity search
One-shot / few-shot learning
Medical imaging (e.g., comparing tumor regions across scans)
🧪 Simple intuition

Imagine teaching a model:

These two images → same person
These two images → different people

Over time, it learns a space where:

Similar items are close together
Different items are far apart
