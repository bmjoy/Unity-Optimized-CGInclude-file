# Optimized CGInclude files

## Introduction:
Writing custom PBR Shaders(include standard surface shaders) usually will call the lightingStandard functions in CGIncludes. However, there are lots of performance defection in Unity's default cginc. Thus, this project deeply optimized the lighting calculation functions in cginc files. Include deferred rendering path PBS functions, forward rendering path(forward base pass and forward add pass) PBS functions and Standard BRDF functions.

## Manual:
### For native cginclude:
1. Open your UnityEditor's CGIncludes folder. For example: "C:/Program Files/Unity/Editor/Data/CGIncludes"
2. Backup the origin folder;
3. replace it with the new CGIncludes folder.
4. Restart your Unity Editor;
### For custom cginclude:
1. Drag the CustomIncludes into your project's Assets folder.
2. Add "#include "CustomLighting.cginc"" in your custom PBR shaders.
3. Do not use "Lighting.cginc", "UnityGlobalIllumination.cginc", "UnityImageBasedLighting.cginc", "UnityPBSLighting.cginc" or "UnityStandardBRDF.cginc" in your shaders! That will cause an conflict!
4. You do not have to change any other code in your shaders!.

## TODO List in the future:
1. Fast PBR functions for PC;
2. Fast PBR functions for Mobile;
3. Subsurface Scattering Skin shader and post processing  (different from Unity official HDRP)
