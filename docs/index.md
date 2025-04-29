# Welcome to **ChatFed** 🚀

ChatFed is an open-source “Lego-style” tool-stack that lets you build, mix and deploy
chatbots quickly while **re-using** components paid for by previous projects.

![ChatFed architecture](assets/architecture_small.png)

---

## Why ChatFed?

| Challenge in typical chatbot projects | How ChatFed fixes it |
|---------------------------------------|----------------------|
| Components are rebuilt from scratch → high cost & long lead time | Reusable, containerised bricks published in a shared registry |
| Each vendor picks its own tech stack → lock-in | Opinionated runtime + open API spec; internals stay flexible |
| Hard to add low-resource languages & IVR | Plug-and-play language / channel adapters |
| No consistent governance | Apache-style contribution model & automated CI templates |

---

## Key Concepts

* **Brick** – A Docker container exposing a single capability (e.g. Retriever, TTS, WhatsApp adapter) via the ChatFed OpenAPI contract.  
* **Bot definition** – A YAML file that lists which bricks—and which versions—compose a running chatbot.  
* **Registry** – Static catalogue (`registry.md`) where every brick is documented and versioned.  
* **Core runtime** – The API gateway and orchestration layer that wires bricks together at run-time.

---

## Get started in 30 seconds ⏱

```bash
git clone https://github.com/your-org/ChatFed
cd ChatFed
make demo          # spins up vector store + retriever + generator + web UI
