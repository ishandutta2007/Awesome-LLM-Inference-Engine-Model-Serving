# Awesome-LLM-Inference-Engine-Model-Serving

# Awesome-LLM-Inference-Engine-Model-Serving

Top LLM Inference Engine Model Serving (Opensource) 🌟 Star if you like it! 🌟

A curated list of top LLM inference engines, high-throughput GPU/CPU model serving runtimes, local inference backends, speculative decoding frameworks, and distributed serving orchestrators—featuring commercial SaaS/Hosted platforms alongside their open-source equivalents.

---

## Table of Contents

- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source Equivalents & Tools](#open-source-equivalents--tools)
  - [High-Throughput GPU LLM Inference Engines](#high-throughput-gpu-llm-inference-engines)
  - [Local, Edge, CPU & Apple Silicon Inference Runtimes](#local-edge-cpu--apple-silicon-inference-runtimes)
  - [Enterprise Multi-Model & Distributed Serving Servers](#enterprise-multi-model--distributed-serving-servers)
  - [Speculative Decoding, Quantization & Kernel Accelerators](#speculative-decoding-quantization--kernel-accelerators)
  - [Browser, WebGPU & Mobile LLM Inference Engines](#browser-webgpu--mobile-llm-inference-engines)
- [Contributing](#contributing)

---

## SaaS/Hosted Platforms

Commercial, cloud-hosted ultra-fast AI inference clouds, specialized LPU/WSE hardware endpoints, and managed serverless model serving APIs.

* **[GroqCloud](https://groq.com)** - Ultra-low-latency AI inference cloud powered by custom LPU (Language Processing Unit) hardware delivering hundreds of tokens per second.
* **[Cerebras Inference Cloud](https://cerebras.ai)** - Wafer-Scale Engine (WSE-3) cloud inference platform offering industry-leading token generation speeds for frontier open-weights LLMs.
* **[SambaNova Cloud](https://sambanova.ai)** - Enterprise AI inference cloud running on Reconfigurable Dataflow Units (RDUs) for high-speed, massive-context LLM serving.
* **[Together Inference Engine](https://together.ai)** - Managed cloud inference platform powered by FlashAttention and speculative decoding optimizations for open-source foundation models.
* **[Fireworks AI](https://fireworks.ai)** - High-speed, low-latency generative AI inference cloud engineered with custom CUDA kernels and multi-LoRA serving.
* **[vLLM Cloud / Red Hat AI Inference Server](https://redhat.com)** - Enterprise-supported cloud and hybrid deployments of vLLM with production SLAs, security hardening, and distributed scaling.
* **[NVIDIA NIM (TensorRT-LLM & Triton Cloud)](https://nvidia.com)** - Managed cloud microservices packaging TensorRT-LLM and Triton Inference Server into enterprise-ready containers.
* **[Hugging Face Inference Endpoints (Managed TGI)](https://huggingface.co)** - Dedicated, fully managed cloud deployment platform powered by Text Generation Inference (TGI) across AWS, GCP, and Azure.
* **[Baseten](https://baseten.co)** - Commercial high-performance model serving infrastructure offering autoscaling GPU clusters, cold-start optimization, and TensorRT-LLM pipelines.
* **[Modal / Replicate / DeepInfra](https://deepinfra.com)** - Serverless GPU cloud platforms providing instant API endpoints and pay-per-token inference for open-weights LLMs.

---

## Open-Source Equivalents & Tools

Free and open-source software (FOSS) LLM inference engines, PagedAttention/RadixAttention runtimes, C/C++ local model runners, quantization kernels, and Kubernetes serving orchestrators.

### High-Throughput GPU LLM Inference Engines

* **[DeepInfer (deepseek-ai)](https://github.com)** - High-performance open-source LLM inference engine and optimization framework developed by DeepSeek AI for efficient model serving.
* **[vLLM](https://github.com)** - The industry-standard open-source high-throughput and memory-efficient LLM inference and serving engine powered by PagedAttention.
* **[SGLang](https://github.com)** - Blazingly fast serving framework for Large Language Models and Vision Language Models featuring RadixAttention prefix caching and zero-overhead CPU scheduling.
* **[TensorRT-LLM (NVIDIA)](https://github.com)** - Open-source library by NVIDIA compiling LLMs into optimized TensorRT engines with FP8/INT4 quantization, in-flight batching, and multi-GPU tensor parallelism.
* **[Text Generation Inference (TGI - Hugging Face)](https://github.com)** - Production-grade open-source Rust and Python toolkit for deploying and serving Large Language Models with continuous batching and tensor parallelism.
* **[LMDeploy (InternLM)](https://github.com)** - High-throughput open-source toolkit for compressing, deploying, and serving LLMs and VLMs powered by the C++/CUDA TurboMind engine.
* **[Aphrodite Engine](https://github.com)** - High-throughput open-source LLM inference engine supporting extensive quantization formats (EXL2, AWQ, GPTQ, GGUF, FP8) and dynamic batching.
* **[DeepSpeed-FastGen / DeepSpeed-MII](https://github.com)** - Microsoft's open-source low-latency, high-throughput inference system utilizing DeepSpeed-FastGen dynamic SplitFuse scheduling.

### Local, Edge, CPU & Apple Silicon Inference Runtimes

* **[llama.cpp](https://github.com)** - The foundational open-source C/C++ LLM inference engine enabling fast quantized execution on consumer CPUs, NVIDIA/AMD/Intel GPUs, and Apple Metal.
* **[Ollama](https://github.com)** - Effortless open-source local model runner and REST server built on llama.cpp for running Llama, Qwen, DeepSeek, and Gemma locally.
* **[MLX & MLX-LM (Apple)](https://github.com)** - Apple's open-source array framework and LLM inference package engineered specifically for unified memory on Apple Silicon (M1–M4).
* **[ExLlamaV2](https://github.com)** - Ultra-fast open-source inference library for running quantized EXL2/GPTQ LLMs on consumer NVIDIA GPUs with minimal VRAM overhead.
* **[KoboldCpp](https://github.com)** - Single-file, zero-dependency open-source LLM inference binary built on llama.cpp with an integrated web UI and OpenAI-compatible API.
* **[ik_llama.cpp](https://github.com)** - Performance-focused fork of llama.cpp introducing advanced quantization formats (IQK) and accelerated CPU/hybrid GPU throughput.
* **[PowerInfer](https://github.com)** - High-speed open-source LLM inference engine exploiting neuron activation locality for fast CPU/GPU hybrid execution on consumer PCs.

### Enterprise Multi-Model & Distributed Serving Servers

* **[NVIDIA Triton Inference Server](https://github.com)** - Open-source multi-framework inference serving software streamlining deployment across TensorRT-LLM, vLLM, ONNX Runtime, and PyTorch.
* **[KServe](https://github.com)** - Standard open-source Kubernetes-native model inference platform supporting serverless autoscaling, canary rollouts, and vLLM/Triton runtimes.
* **[Ray Serve](https://github.com)** - Scalable, programmable open-source model serving library built on Ray for distributed multi-node LLM pipelines and model composition.
* **[BentoML & OpenLLM](https://github.com)** - Open-source platform for packaging, containerizing, and serving any open-weights LLM as an OpenAI-compatible production API.
* **[LitServe (Lightning AI)](https://github.com)** - High-speed, flexible open-source AI model serving engine built on FastAPI supporting dynamic batching, streaming, and multi-GPU workers.
* **[Dynamo (NVIDIA) / llm-d](https://github.com)** - Open-source distributed inference serving framework designed for disaggregated prefill/decode execution across multi-node GPU clusters.

### Speculative Decoding, Quantization & Kernel Accelerators

* **[FlashInfer](https://github.com)** - High-performance open-source library and kernel suite for LLM serving providing customizable attention, KV-cache storage, and sampling kernels.
* **[FlashAttention (Tri Dao)](https://github.com)** - Fast, memory-efficient exact attention CUDA kernels serving as the core building block of modern LLM inference engines.
* **[AutoAWQ](https://github.com)** - Open-source Activation-Aware Weight Quantization (AWQ) toolkit delivering up to 3x faster 4-bit LLM inference with minimal accuracy loss.
* **[GPTQModel](https://github.com)** - Production-grade open-source LLM quantization toolkit supporting GPTQ, Marlin, and Triton kernels for accelerated inference.
* **[SpecForge / Medusa / EAGLE](https://github.com)** - Open-source speculative decoding frameworks accelerating LLM generation speed by 2x–3x without altering output distributions.

### Browser, WebGPU & Mobile LLM Inference Engines

* **[MLC LLM](https://github.com)** - Universal open-source LLM deployment engine compiling models natively for WebGPU browsers, iOS, Android, Vulkan, Metal, and CUDA.
* **[WebLLM](https://github.com)** - High-performance open-source in-browser LLM inference engine leveraging WebGPU hardware acceleration with zero server backend required.
* **[Transformers.js (Hugging Face)](https://github.com)** - Run quantized LLMs and multimodal models directly inside web browsers via ONNX Runtime Web and WebGPU.
* **[ONNX Runtime GenAI](https://github.com)** - Microsoft's open-source generative AI extensions for running optimized LLMs across Windows DirectML, mobile, and edge CPUs.
* **[ExecuTorch (Meta)](https://github.com)** - PyTorch-native open-source edge inference runtime engineered for running Llama and multimodal models on iOS, Android, and embedded devices.

---

## Contributing
