# CPU vs GPU vs TPU in MLOps
 Serdar Biçici - 150210331
 
![](Turing-Tensor-Core_30fps_FINAL_736x414.gif)

---

## Role of Hardware in MLOps
Hardware determines training and inference speed, scalability, cost, and deployment efficiency.  
The choice depends on model type, data size, and latency needs.  
MLOps pipelines use **CPUs**, **GPUs**, **TPUs**, and sometimes **NPUs** or **DPUs**.

---

## CPU (Central Processing Unit)
- General-purpose processor for all computing tasks  
- Handles logic, control, and sequential operations  
- Limited parallelism (few cores)  
- Best for data preprocessing, orchestration, and light inference  
- Found in all servers and edge devices  

---

## GPU (Graphics Processing Unit)
- Designed for massive parallel computation  
- Thousands of cores optimized for matrix operations  
- Ideal for deep learning training and inference  
- High memory bandwidth and compute throughput  
- Used widely in AI research and production  

---

## TPU (Tensor Processing Unit)
- Custom hardware by Google for neural network workloads  
- Optimized for TensorFlow and matrix math  
- Extremely fast for deep learning training/inference  
- Available only on Google Cloud  
- Less flexible than GPU but more efficient for large models  
- TPUs will be sold to other corporations in 2026  

---

## Comparison Table

| Feature | CPU | GPU | TPU |
|----------|-----|-----|-----|
| Purpose | General computation | Parallel computation | Tensor operations |
| Parallelism | Low | High | Very High |
| Training Speed | Slow | Fast | Very Fast |
| Flexibility | High | Medium | Low |
| Cost Efficiency | Low for large models | High | Very High (Cloud) |
| Best For | Preprocessing, orchestration | Deep learning, graphics | TensorFlow workloads |

---

## Where to Use What

| Use Case | Recommended Hardware |
|-----------|----------------------|
| Small models | CPU |
| Data preprocessing | CPU |
| Edge inference | CPU |
| Deep learning workloads | GPU |
| PyTorch / TensorFlow training | GPU |
| Distributed TensorFlow on Google Cloud | TPU |

---

## Hardware Experiments

| Task | Dataset / Model | Hardware Used |
|------|------------------|----------------|
| Neural Network | MNIST (60k) | CPU, GPU, TPU |
| Gradient Boosting | Wine Dataset (178) | CPU, GPU |
| LLM Inference | TinyLlama-1.1B-Chat-v1.0 | CPU, GPU |

Performance metrics include **Training Time (s)** and **Throughput (samples/s)**.

---

## Extra Knowledge
- **NPU (Neural Processing Unit):** On-device AI accelerator  
- **DPU (Data Processing Unit):** Offloads networking, encryption, and data tasks from CPU  
- **FPGA (Field-Programmable Gate Array):** Reconfigurable hardware for custom acceleration  
