# Implement-deployment-pipelines-in-Microsoft-Fabric
# Microsoft Fabric Deployment Pipeline Lab

This lab demonstrates how to create and implement deployment pipelines in **Microsoft Fabric**, enabling structured content deployment across **Development**, **Test**, and **Production** environments using **Lakehouse** objects.

> ⏱️ Estimated Completion Time: ~20 minutes  
> 🛠️ Prerequisites: Fabric trial or Fabric capacity enabled, Workspace Admin role

---

## 🚀 Objective

Learn how to:

- Create workspaces in Microsoft Fabric
- Set up a deployment pipeline
- Assign workspaces to pipeline stages
- Create a Lakehouse in the Development workspace
- Use the deployment pipeline to move content between Development, Test, and Production
- Confirm that content is successfully deployed to each stage

---

## 📁 Workspace Setup

1. Go to [Microsoft Fabric Home](https://app.fabric.microsoft.com/home?experience=fabric)
2. Create **three new workspaces**:
   - `Development`
   - `Test`
   - `Production`
3. Ensure that each workspace uses a licensing mode that supports Fabric (e.g., Trial, Premium, or Fabric)

> 💡 If name conflicts occur, append random numbers (e.g., `Development123`)

---

## 🔄 Create Deployment Pipeline

1. From the left menu, select **Deployment pipelines**
2. Click **New pipeline**
3. Name your pipeline (e.g., `LakehouseDeploymentPipeline`)
4. Click **Next** then **Create and continue**

---

## 🔗 Assign Workspaces to Stages

1. Open the created pipeline
2. Assign:
   - `Development` workspace to the **Development** stage
   - `Test` workspace to the **Test** stage
   - `Production` workspace to the **Production** stage
3. Click ✅ **Assign** after each selection

---

## 🏗️ Create Lakehouse in Development

1. Select **Workspaces** > open `Development`
2. Click **New item** > choose **Lakehouse**
3. Name it: `LabLakehouse`
4. Click **Create**
5. In the Lakehouse Explorer, click **Start with sample data**
6. Choose the **NYCTaxi** dataset

---

## 📦 Deploy Content Between Stages

1. Go to the pipeline
2. Under **Development** stage, you should see `LabLakehouse` listed
3. Click **Deploy**
4. In the confirmation dialog, click **Deploy** again

✅ Now the **Test** stage will contain the Lakehouse

5. Repeat the process from **Test ➡ Production**:
   - Select the **Test** stage
   - Click **Deploy**
   - Confirm the deployment

✅ All three stages (Development, Test, Production) are now in sync

---

## 🔍 Verify in Workspaces

1. Go to **Workspaces**
2. Open **Test** workspace – you should see `LabLakehouse`
3. Open **Production** workspace – confirm the same

---

## 🧹 Clean Up (Optional)

1. In each workspace:
   - Click the workspace name
   - Go to **Workspace settings**
   - Select **Remove this workspace**

---

## 📘 References

- [Microsoft Fabric Documentation](https://learn.microsoft.com/fabric)
- [Deployment pipelines overview](https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines-overview)

---

## 🧪 License

This lab is provided for **educational purposes** and assumes a valid Microsoft Fabric trial or capacity license.
