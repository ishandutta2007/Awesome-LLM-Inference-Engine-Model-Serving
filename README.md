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

| Platform | Description | Pricing (Starting Tier) | Free Tier Limits |
| :--- | :--- | :--- | :--- |
| **[GroqCloud](https://groq.com)** | Ultra-low-latency AI inference cloud powered by custom LPU (Language Processing Unit) hardware delivering hundreds of tokens per second. | Pay-as-you-go starting at $0.075 / 1M input tokens and $0.30 / 1M output tokens (GPT-OSS 20B) | Free tier available forever: up to 8,000–30,000 TPM (model-dependent), 200,000 tokens/day, 30 RPM, and 1,000 requests/day |
| **[Cerebras Inference Cloud](https://cerebras.ai)** | Wafer-Scale Engine (WSE-3) cloud inference platform offering industry-leading token generation speeds for frontier open-weights LLMs. | Developer Tier starting at $0.35 / 1M input tokens and $0.75 / 1M output tokens (GPT-OSS 120B); subscription bundles from $50/month | Free trial with $5 one-time promotional credit valid for 30 days upon adding a payment method (no permanent free tier) |
| **[SambaNova Cloud](https://sambanova.ai)** | Enterprise AI inference cloud running on Reconfigurable Dataflow Units (RDUs) for high-speed, massive-context LLM serving. | Developer Tier starting at $0.22 / 1M input tokens and $0.59 / 1M output tokens (gpt-oss-120b) | Free tier available forever: 20 requests/minute (RPM), 20 requests/day (RPD), and 200,000 tokens/day per model |
| **[Together Inference Engine](https://together.ai)** | Managed cloud inference platform powered by FlashAttention and speculative decoding optimizations for open-source foundation models. | Pay-as-you-go starting at $0.15 / 1M input tokens and $0.50 / 1M output tokens (initial minimum credit deposit of $15) | No free tier or recurring free trial; strictly prepaid model with baseline starting rate limit of 1 RPS (60 RPM) |
| **[Fireworks AI](https://fireworks.ai)** | High-speed, low-latency generative AI inference cloud engineered with custom CUDA kernels and multi-LoRA serving. | Pay-as-you-go starting at $0.10 / 1M input tokens and $0.30 / 1M output tokens (small/flash models) | Free trial with $1 one-time signup credit capped at 10 requests/minute (no permanent recurring free tier) |
| **[Red Hat AI Inference Server](https://redhat.com)** | Enterprise-supported cloud and hybrid deployments of vLLM with production SLAs, security hardening, and distributed scaling. | Starting at $0.05 / GPU / hour on public cloud marketplaces; 1-year node subscription via enterprise sales | 60-day free trial evaluation available for Red Hat enterprise software platforms upon account registration |
| **[NVIDIA NIM (build.nvidia.com)](https://nvidia.com)** | Managed cloud microservices packaging TensorRT-LLM and Triton Inference Server into enterprise-ready containers. | Self-hosted production licenses via NVIDIA AI Enterprise at $4,500 / GPU / year; cloud partner consumption pricing varies | Free developer account includes 1,000 free inference credits and up to 40 requests/minute (RPM) for prototyping |
| **[Hugging Face Inference Endpoints](https://huggingface.co)** | Dedicated, fully managed cloud deployment platform powered by Text Generation Inference (TGI) across AWS, GCP, and Azure. | Dedicated GPU instances starting at ~$0.50 / hour (e.g., NVIDIA T4 / A10G); billed per hour running | No free tier for dedicated Inference Endpoints; free tier is limited to serverless Inference API with shared community rate limits |
| **[Baseten](https://baseten.co)** | Commercial high-performance model serving infrastructure offering autoscaling GPU clusters, cold-start optimization, and TensorRT-LLM pipelines. | Pay-as-you-go GPU instance billing starting at ~$0.30 / hour (T4) or token APIs; $0 base platform fee | Free trial offering $30 one-time compute credits upon account setup (no permanent recurring free tier) |
| **[Modal](https://modal.com)** | Serverless GPU cloud platform providing container-native execution, rapid cold-starts, and serverless inference runtimes. | Pay-per-second compute starting at ~$0.000164 / second (~$0.59 / hour for T4 GPU) | Free Starter tier forever includes $30 / month recurring compute credit (~50 hours of T4 GPU time, max 10 concurrent GPUs) |
| **[Replicate](https://replicate.com)** | Serverless AI platform running open-source models via hosted cloud API with autoscaling. | Pay-per-second starting at ~$0.000140 / second (~$0.50 / hour for Nvidia T4) or per-token endpoints | Free trial collection allows running select public demo models for a limited initial batch of runs (no recurring free tier) |
| **[DeepInfra](https://deepinfra.com)** | Pay-per-token and serverless GPU hosting platform providing instant API endpoints for open-weights LLMs. | Pay-as-you-go starting at $0.09 / 1M input tokens and $0.15 / 1M output tokens (e.g., Llama-3.1-8B) | No permanent free tier; accounts require credit card or prepayment; offers DeepStart startup credits program for eligible startups |



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
