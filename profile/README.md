# Plantarium Platform 🌱

Welcome to **Plantarium Platform**, an open-source energy-efficient FAAS (Function as a Service) platform designed for small-scale projects and development environments. The core idea is to provide a lightweight, resource-saving alternative to large-scale cloud services, inspired by cloud-native principles but optimized for minimal costs and environmental impact.

## 🚀 Project Vision

Plantarium Platform aims to be a **“pocket-sized AWS”**, offering a simplified, cost-effective solution for hosting services on a VPS or container. The primary goal is to deliver a platform that minimizes resource usage, thus reducing both operational costs and carbon footprint.

The platform is architected to be close enough to existing cloud standards, enabling an easier transition to major cloud providers when projects scale beyond a small footprint. This small footprint is achieved through radical minimalism, which may impact the performance of some requests to the platform.

## 🌍 Why Build Plantarium Platform?

1. **High Cloud Costs**: Major cloud providers charge significant fees, especially for their extensive feature sets. For small projects, this complexity often translates into high, unnecessary costs.
2. **Resource Efficiency**: With the increasing need for energy savings, Plantarium Platform focuses on using the bare minimum resources, inspired by the principle of using “only what you need.”
3. **Reduced Complexity**: The current infrastructure landscape is bloated, overflowing with abstraction layers like Docker and Kubernetes that consume excessive resources. Each Docker container carries a separate OS, which is unnecessary when multiple services could run efficiently on a single Linux instance. Plantarium Platform simplifies this by cutting down on abstraction and focusing on lightweight Linux processes.

## 🌱 Core Concepts

- **Leafs**: The analog of Docker pods in Plantarium Platform, these are lightweight service instances that dynamically scale.
- **Stems**: Service deployments.

## 🛠️ Platform Components

- **[GraftNode](https://github.com/plantarium-platform/graftnode-go)**: The component responsible for keeping zero instances of a service until client requests are received. When a request arrives, GraftNode quickly starts the real service instance. **[Status: POC done]**  
- **[SproutScaler](https://github.com/plantarium-platform/sproutscaler-go)**: An aggressive auto-scaler that adds or removes leaf instances based on real-time performance data. **[Status: POC Done]**
- **[Herbarium](https://github.com/plantarium-platform/herbarium-go)**: The service registry component that tracks Stems and Leafs, manage their state integrated with the auto-scaler for efficient resource management. **[Status: In Progress]**
- **[Planter](https://github.com/plantarium-platform/planter-go)**: The component that handles service deployments via CLI **[Status: Designing]**
- **SeedVault**: The secure configuration management component, akin to a key vault, for handling secrets and sensitive data. **[Status: Not Started]**
- **GardenPanel**: A web-based admin panel for monitoring and managing leafs, observing how many instances are active and their states. **[Status: Not Started]**

## 📜 License

Plantarium Platform is licensed under the **MIT License**. 

## 👥 Contact

For anyone interested in contributing to Plantarium Platform or discussing collaboration, feel free to reach out:

- GitHub: [glorko](https://github.com/glorko)
- Telegram: [glorfindeil](https://t.me/glorfindeil)
