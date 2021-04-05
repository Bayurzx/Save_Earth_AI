<!--- STARTEXCLUDE --->
# Save Earth with Azure AI

Create entries of newly discovered, rare, or near-extinct life discoveries on earth with the help of `AI` 🤖 for the world to see!

<!---Add Image here --->
![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/Home.jpg)
![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/AI_test.gif)
![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/upload.jpg)


# Why I Did It (Inspiration) ???
## `For the joy of a new discovery!!!`
*What's a better way to describe the beauty of life on earth than with a simple picture?*
I wanted to create a project that could create awareness on rare, unique, endangered plants and animals. It's vital that people understand the impact we have on the natural world around us with respect to extinction of other species.

# What It Does???
- It allows any one on earth or beyond 👽 `😉` To feature their discovery! And with the help of AI, The app can help detect high priority images, add it to a special collection which the admin can easily utilize.
- It also creates a community for we, the environmental/nature freaks, NGOs, scientists, researchers, explorers, adventurers of the world who care about nature...  etc... To come together and feature, discuss something weird you saw from some where on earth and save it. Hence, Save-Earth get it... 😁😊😓😓
---

# What Do You Do???
## Checkout the site here 👉 [SaveearthAI](https://saveearth.xyz/) 👈
### (Might need to refresh sometimes; Server closes on the 14th April. [Contact me](mailto:bayurzx@gmail.com) to create/ open server)
---
- First, signup and then signin, ensure your password has the following: alphanumeric, symbol and one capital letter. e.g P@$$word1234
- Upload link shows only show after signin
- Give it a name, add a caption, give some description, tell us where you saw it. Take a pic and upload it or send us the link. Upload it to AI 🤖 to see if it's on our radar. Then add a location. Have in mind that the app uses `Google Geocoder API` So use a language Google map will understand. It also uses `Google Javascript Map API` for exact coordinates so don't forget to click the coordinate button!.
- The donation is in a sandbox for now (braintree) feel free to use this fake card detail for testing:
    4111 1111 1111 1111
    12/22
---

# How we built it???
![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/saveearth%20architecture1.png)

## Stack Highlights 🥪🥪🥪
- Azure Cognitive Services' **Custom Vision** : Custom Vision makes it easy for anyone to train and analyze tagged `Image Datasets` without much prior experience with an already provided machine learning algorithm without, the complexity of spinning up VMs or GPU clusters. You can then communicate with the Custom Vision API to run image detection or classification quickly from anywhere around the world with the aid of Azure Cloud edge networks!
- Azure Container Storage: This enables storing blob files such as images for backups, archiving, retrieval and analysis on Azure-hosted service such as Custom Vision.
---
### This web app also made use of :
| Languages  | Frameworks | Cloud services | Databases        | APIs        | Platform    |
 | ---------- | ---------- | -------------- | ---------------- | ----------- | ----------- |
| JS, HTML,CSS | Reactjs, expressjs  | Azure(VM, VNet etc.) | DataStax Astra(Frontend), MongoDB(Backend)     | Google Geocoder API, Google JavaScript Map API   |  Netlify   |

---
## You Should Know That...
*Microservices do not have to be a Nightmare, you can decide to use whatever stack that favors you. I decided on the stacks and services to use based on preferences (Nahh, they were probably already paid for or free 😂).  Other than your core services: Azure Custom Vision and Containers, Feel free to use whatever stack that burst your bubble 😊 .*

## Here are examples of trained images the AI will detect
Alpaca, American Crow, American Goldfinch (Female), American Goldfinch (Male), American Robin (Adult), American Robin (Juvenile), Blue Jay, Common Grackle, `Hedgehog`, House Sparrow (Female), House Sparrow (Male), House Wren, Mourning Dove, Northern Cardinal (Adult Male), Northern Cardinal (Female), `Parrot`, `Red Panda`, Red-tailed Hawk (Dark morph), Red-tailed Hawk (Light morph immature), `Sunflower`, Tufted Titmouse, `White Tiger`.

## Here is the `Admin Login` and `regular user login` to test out creation of image Datasets
user: eren_yeager@gmail.com
password: P@$$word1234

regular user: superman@gmail.com
regular user password: P@$$word1234

---
## Setting UP!.

### Setup Azure Custom Vision
- Follow this 👉 [link](https://portal.azure.com/#create/Microsoft.CognitiveServicesCustomVision) 👈 to create a custom vision resource
- Fill in the details as shown below
![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/Custom%20Vision%20UI.jpg)
- You will be directed to your Custom Vision UI. Remember to collect and keep your keys and endpoints url safely.
![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/customvision.jpg)
- For more info on custom vision click 👉 [link](https://docs.microsoft.com/en-us/learn/modules/classify-images-with-custom-vision-service/) 👈

### Setting up DB
- You can either use [CosmosDB](https://docs.microsoft.com/en-us/learn/modules/create-cosmos-db-for-scale/), || [DataStax Astra](https://github.com/DataStax-Examples/sample-app-template) or  [Azure SQL Database](https://docs.microsoft.com/en-us/learn/paths/azure-sql-fundamentals/)
- Follow the links for more info on how to setup the respective DBs

### Setting Up Geocoder APIs
- You can easily get the keys for the Google Geocoder API and Google Javascript Map API [here](https://console.cloud.google.com/marketplace)

---

Clone to your local machine...
`git clone <put copied git link here>`

Install all dependencies in package.json
`npm install`

While that is working, you should sort out your .env file, go to the .env.sample file you will get details on your environment variables

While you can run the app with `npm start` I would advise using `npx netlify dev` to enable you utilize netlify-functions

Happy coding!

*Make sure to get the backend for authentication at 👉* [save-earth-BE](https://github.com/Bayurzx/Save_Earth_AI_BE)
Note that after signup, you can switch the role from regular user => `user: 0` to Administrator => `admin:1` at the database backend
