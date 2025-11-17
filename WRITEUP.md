# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*

**Option 1: Virtual Machine (VM)**  
- **Costs:** More expensive since you pay for the compute resource even when it’s idle. Licensing, OS management, and maintenance add extra costs.  
- **Scalability:** Requires manual setup for scaling using load balancers, scale sets, or multiple VM instances. Offers greater control but increases operational complexity.  
- **Availability:** You are responsible for ensuring high availability through redundancy and failover setups.  
- **Workflow:** Full control over OS-level configuration, package installation, and runtime setup, but requires manual updates and deployments.

**Option 2: App Service (PaaS)**  
- **Costs:** Cost-efficient for small projects. Offers a **Free F1 plan** for development and pay-as-you-go scalability for production.  
- **Scalability:** Built-in auto-scaling and easy configuration through Azure Portal. No manual server setup required.  
- **Availability:** Microsoft handles patching, uptime, and redundancy automatically with guaranteed SLAs in paid tiers.  
- **Workflow:** Integrates directly with GitHub for CI/CD. Supports environment variable configuration, quick deployments, and minimal infrastructure management.

**Choice:**  Here’s a revised version starting the way you requested:

**Choice:**
I chose Azure App Service because the project I am doing is a lightweight Flask-based CMS, and this service provides an easy, automated deployment process with minimal setup. It integrates smoothly with GitHub for CI/CD, handles scaling and availability on its own, and keeps sensitive information secure through Application Settings, making it the ideal choice for this project.

---

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

If the CMS application required:
- Custom OS configurations or low-level access (e.g., installing special system dependencies)
- Heavy background processing or high compute workloads
- Advanced network configurations or on-premises integration  

Then, a **Virtual Machine (VM)** would be more appropriate since it allows full control over the environment and can be tailored for specific performance or system requirements.
