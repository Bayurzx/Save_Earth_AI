## Inspiration
### `For the joy of a new discovery!!!`
*What's a better way to describe the beauty of life on earth than with a simple picture?*
I wanted to create a project that could create awareness on rare, unique, endangered plants and animals. It's vital that people understand the impact we have on the natural world around us with respect to extinction of other species.

## What it does
- It allows any one on earth or beyond 👽 `😉` To feature their discovery! And with the help of AI, The app can help detect high priority images, add it to a special collection which the admin can easily utilize.
- It also creates a community for we, the environmental/nature freaks, NGOs, scientists, researchers, explorers, adventurers of the world who care about nature...  etc... To come together and feature, discuss something weird you saw from some where on earth and save it. Hence, Save-Earth get it... 😁😊😓😓
- It allows any one to send image datasets to custom vision for training.
---

## How we built it
Save_Earth_AI Architecture 👇

![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/saveearth%20architecture1.png)
- A user fills the form at the upload page, includes an image but first, sends the image data to Custom Vision AI
- If the image is detected by AI, It is prioritized and sent to a blob container
- User receives response and can continue with uploading data
- The data is then stored in the database (Blobs go the Blob container; documents go to NoSQL)
---

## Challenges we ran into
### Gathering the right image datasets was almost a nightmare.
- **Getting the right datasets:** I found out the hard way that the images required for training were actually rare, unique or nearly extinct...😉. After scouring the internet for suitable images for rare animals, like the `White Bengal Tiger`, to build and train a model; I faced challenges such as
  - Maintaining a uniform datasets since such image datasets were mostly rare or insufficient
  - Time consuming process of checking if images were free to use or met specification.
  - Ensuring that the images were diverse enough.
-  **Had to Settle:** So I had few opportunities to train images for rare species and I had to settle for more common images such as bird species (e.g. parrot) to train the AI models.
- **AllUser Access Restriction**I discovered that allowing access to all users to train the model through the frontend would have been costly both financially and data quality in the sense that not all users could easily identify the right image datasets to use and may require supervision.
---

## Accomplishments that we're proud of
- The app, with the help of the Custom Vision Prediction API was able to detect and then classify images returning a probability percent and give responses based on the probability.

![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/AI_test.gif)

- The app was able to automatically store high priority images that were detected by the Custom Vision AI by creating and saving it into Blob Containers.

![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/auto_containers.jpg)

- It also allowed people, given admin access, to tag and send image datasets for training.
![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/image_dataset1.jpg)
![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/image%20dataset2.jpg)


## What we learned
- **Custom Vision:** The first time I ever used custom vision was about 4weeks ago and it's amazing how useful and easy to learn it is. I was able to integrate it to the app thanks to the following resources.
    - [Cognitive Services' Custom Vision](https://docs.microsoft.com/en-us/azure/cognitive-services/Custom-Vision-Service/quickstarts/image-classification?tabs=visual-studio&pivots=programming-language-javascript#add-tags-to-the-project)
    - [Cognitive Services Quick Start](https://github.com/Azure-Samples/cognitive-services-quickstart-code)

- **Azure Blob Container:** I also learned how to utilize blob containers to easily store files and create logically isolated containers.
    -
    - [BlobStream Azure Samples](https://github.com/Azure-Samples/azure-sdk-for-js-storage-blob-stream-nodejs)
    - [BlobServiceClient class](https://docs.microsoft.com/en-us/javascript/api/@azure/storage-blob/blobserviceclient?view=azure-node-latest)

## What's next for Save Earth With Azure AI
- To see the feasibility of implementing Azure IoT Edge with smart wearables in a case of tracking the progress of rare discovered animals.
- Enterprise Scalability for production.
