# SeEar SDK Documentation

## Introduction
The SeEar SDK is developed to showcase any speech received by a mounted mobile device and display it as text on an Augmented Reality (AR) glass. The SDK utilizes stereoscopic rendering to properly showcase recognized speech as text. For further information about the Head Mounted Display (HMD) used with this SDK, please contact [yasith.sam7@gmail.com](mailto:yasith.sam7@gmail.com).

## SDK Setup

To properly set up the SeEar SDK, follow these steps:

1. Download the project as a Zip file and extract it to a desired location on your computer.
2. Install Unity (version 2021.3.29f1) with Android Build support.
3. After installing Unity, create a new 3D project.
4. Navigate to Assets -> Import Package -> Custom Package and select the SeEar-SDK.unitypackage from the extracted location. Import all the files inside the package.
5. You will need an active Azure subscription. Create a new Azure Speech Service resource and obtain an authentication key.
6. After importing the package, navigate to the Scripts folder and open the ContinuousSpeechConverter.cs script. In line 75, replace the key and region values with the values obtained from the Azure Speech Service you created earlier. Also, change the configured language if needed (default is set to Sinhala "si-LK").
7. Save the script and navigate to GcAr -> Scene -> SeEar to load the scene.
8. Run the scene and speak to the device. Check if your speech is displayed as stereo-pair images. If so, the SDK is properly set up.

## Sinhala Converter Asset

During the development of the SDK, it was observed that recognized Sinhala text was not properly displayed within Unity applications. To address this issue, we created a Converter Asset to convert recognized text to its proper Sinhala presentation, building on the work done by the Language Technology Research Laboratory - University of Colombo School of Computing.

If you are working with the Sinhala language within Unity, you can use the Sinhala-Converter-Asset.unitypackage provided in this repository to overcome Sinhala text issues. The corresponding asset is already included in the SeEar SDK, so you don't need to import the Converter Asset separately.

To import the asset, navigate to Assets -> Import Package -> Custom Package and select the Sinhala-Converter-Asset.unitypackage. Import it to access the script containing the converter function, which you can use as necessary in your application.

If any issues arise during the setup of the SDK or Converter Asset, feel free to reach out me at [thavinduushan@gmail.com](mailto:thavinduushan@gmail.com).
