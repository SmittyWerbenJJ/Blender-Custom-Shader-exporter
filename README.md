# Blender Custom Shader exporter
This Addon Exports your custom PBR Shaders for use in other 3D Software like Unreal or Unity 

<p class="logo-title"> 
    <img src="src\images\Logo.png" alt="Logo"  />
</p>

## How it works
The Script will search your Blender File for all objects materials and export information about each the ShaderGroup used in each Material to a file.

It will export this Information to a Json File, which can be used in other 3dSoftware.

Information that will be exported:
- Object:
    - Object Name
    - Material Slots
    - Material used in each Slot

- Materials:
    - Material Name
    - Custom Shader type
    - Textures attached to each Node 
    - Material Values


## Installation
There is no Proper Installation method yet. For the time being the Script can be launched from inside Blenders Script editor. 

Run the Script via Blenders Text Editor:
- Inside Blender, go to the Scripting Tab or open a new Text editor window
- In the Header go to  the ``Text``-> ``Open`` then browse for the Python File:  ``materialexporter.py`` and open it

The File can then be executed directly with no setup Needed, if your materials are Set up Correctly (See) [How To Use Section](#How-to-use)

## How to use

- Make sure, your textures are stored in a dedicated Location on your Hard Drive and not packed in the Blend File

- Make sure **ALL** your materials are set up like this:
    ### Sample Setup
    <p class="logo-image"> 
        <img src="src\images\sample-setup.png" alt="Logo"  />
    </p>

    - You can put *your* Shader Magic in the Group Node.<br>That way it will look Similar in Blender, as you would for example Recreate it in Unreal Engine or Unity.
    - You can put as many slots as you want as Input for the Node Group, but the Script will (for now) only Recognize and export Textures/Float Values of these Slots:    
        - Diffuse
        - Alpha
        - Roughness
        - Normal 
        - Specular
        - Metal
        - Subsurface

    - Put Your Textures in the Sockets or twak the values
    - Every Texture Node Attached to the Group, Should have a valid texture in it 

## Known Errors
- No export of Color Values
- No export of Vector Values

- Many more Errors, this addon is still wip
## Future Plans 
- Proper Error catching
- Make it a proper BLender addon with a decent UI and all that Jazz


<style>
.logo-title{
    display:block;
    margin-left:auto;
    margin-right:auto;    
    width :50%;    
}
.logo-image{
    display:block;
    margin-left:auto;
    margin-right:auto;    
    width :80%;    
}
</style>