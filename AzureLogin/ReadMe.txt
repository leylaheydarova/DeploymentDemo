Instroctions for azure Deployment:
1. az login (or az login --use-device-code -burada unique kod gelir ve linkdeki yerden istediyin akkounta giris edirsen)

2. az account show (dogru akkountla login olduguna emin olmaq ucun)

3. If you've never created web applications on your Azure subscription before, you'll need to register the Microsoft.Web provider in order to create a web application in your subscription. Run:
az provider register --namespace Microsoft.Web

4. Create a resource group (replace <resource-group-name> with your own name):
az group create --name MyDemoResourceGroup  --location eastus(bu islemedi F1 ile, westeurope isletdim)

az group list --output table (grouplari yoxlamaq ucun)

5. Create an Azure App Service Plan (replace <app-service-plan> with your chosen name):
az appservice plan create --name <app-service-plan> --resource-group <resource-group-name> --sku F1

az appservice plan list --resource-group MyDemoResourceGroup --output table(planlari yoxlamaq ucun)

6. Deploy an App Service instance (replace <app-name> with your chosen name):
az webapp create --name <app-name> --resource-group <resource-group-name> --plan <app-service-plan>

7. Navigate to your project folder in the VS Code terminal. (.sln olan qovluqa kec)

8. Deploy the app by running: az webapp up --name <app-name>

9. Wait for the deployment to complete. The output should display the app’s public URL.

