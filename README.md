# ChatAvatar-Plugin-for-UE4
This is the official reposity of ChatAvatar Plugin for UE4, you can view our UE5 version through this link: https://www.unrealengine.com/marketplace/zh-CN/product/b7d1bab7547c4baa8eab0787a29eef73

## How to install (for UE4 version)

1. Unzip the package you downloaded from the Releases page, you will get a folder named 'ChatAvatarPlugin'. Please make sure that you download the same version as that of your project.

2. Copy the 'ChatAvatarPlugin' folder into the 'Plugins' folder in your project. If the 'Plugins' folder does not exist in your project, please create one :)

3. Run your project, then open the Plugins Tab, you will see 'ChatAvatarPlugin' plugin in the 'Other' category, please enable it (and restart your project).

## How to use

1. In your project, you will see Deemos's Logo <img src="Resources/logo_black.png" height="30px">
on the right of Platforms button in UE 5.x (at the bottom of Window tab in UE 4.x)

2. Click the logo to open the plugin's widget window. As soon as you have opened the widget window, you can find it at Tool - Editor Utility Widgets - Deemos Import Tool, and open it in later use.

## How to import your package

1. In the widget window, please click 'Import', then select the .zip file you have downloaded from ChatAvatar website (https://hyperhuman.deemos.com) in the file dialog, then click Confirm.

2. After the plugin has checked if your package is a valid ChatAvatar asset package, you will see the Setting page and can select the resolution of texture and topology of model you want in your scene. Then click Next.

3. Next you can choose the features you want in your mesh. You can choose multiple options of them ranging from rigged body to back head textures. Please notice that we do not support back head material slot for obj model. 

4. Next you can choose whether you want basic facial controls or/and body controls. You can select both at the same time.

5. Click Confirm, then the plugin will import all assets needed into your project and do the necessary setup on the model. You can find them later in All - Content - ChatAvatar folder. The window will then close and you will see your mesh in the scene. Please enjoy!

## How to use facial control

1. We use Apple ARKit for basic facial control. So before you use facial control, please ensure that you have enabled the following plugins in your project: LiveLink, Apple ARKit, Apple ARKit Face Support.

2. You need to know what your IP is to connect your facial capture device to the project, here we use Live Link Face application in iOS App Store for example: 
* Open cmd on your computer and type: ipconfig
* Please find the IP of the network you are currently using, type it in the target ip area, and leave the port be default. Then please have a look at your subject's name.
* Please run the project, click the screen and press the Tab key, 
    * if you see your subject's name in the upper left corner, it proves that the facial control is available; 
    * if you see "No ARKit Devices.", please follow the above steps to check your settings and tap the Tab key again until you see your subject name.

## Notes

1. The material your mesh uses is a material instance, which means you can adjust the material's detail parameters at will and easily to enhance the mesh's presentation in your scene.

2. If you cannot move your body model or rotate your camera view, please try either of the solutions following:
* See Edit - Project Settings - Engine - Input, and import the 'InputConfig.ini' we provided in the plugin folder
* See Edit - Project Settings - Project - Maps & Modes, and change the Default GameMode to 'BP_ThirdPersonGameMode'

3. If you happen to see that the materials of your model went missing as soon as you linked your LiveLink device, please manually update the following materials: 
* Face_Mat_CreateBase, M_EyeOcclusion, M_EyeRefractive, M_lacrimal_fluid, M-003_Lash_Albedo_Mat, teeth (M_Solid optional if your body material went missing too)
* Method to update: double click the mat, in the mat window, link or unlink any line and undo it, then click Save, to trigger material re-compilation.

## Please Enjoy!

