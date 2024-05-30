# Release Notes

## Blender 3.6

### Version 2.3.0

Support for importing and exporting the legacy `3ds` format is back
since it is still used by many applications and was missed by many
Blender users.  
(blender/blender-addons!104493)

Animations and almost all 3ds definitions can be imported and exported.  
(blender/blender-addons@2dc2c1c3e4, 
blender/blender-addons@6525a57a32,  
blender/blender-addons@febc4b4433, 
blender/blender-addons@859a2c1b9a)

All backporting changes are listed in the [commit details](https://projects.blender.org/blender/blender-addons/commit/c7a4b16aed).


## Blender 4.0

### Version 2.4.0

#### Export Animation
- The 3ds exporter now got the property to export animation keyframes.
  (blender/blender-addons!104613)
- Keyframe export is optional to avoid crashing any importers wich can
  not handle the keyframe section.  
  (blender/blender-addons@585a682ef8,
  blender/blender-addons@da9bb97bea)

#### Export Hierarchy
- 3ds objects now got hierarchy chunks to preserve the object tree. (blender/blender-addons!104682)
- The object tree can now be exported without the keyframe section
  needed. (blender/blender-addons@0d26a2a017)

#### Export Scale
- Global scale for exporting a 3ds can now be setted. (blender/blender-addons!104767)
- Since many applications are using millimeters, this option is useful
  to convert the measure units.
  (blender/blender-addons@17f142e55d)

#### Convert Measure
- The 3ds importer and exporter now got the ability to converts the unit
  measure for all metric and imperial units. (blender/blender-addons!104769)
- Many 3ds files were exported in millimeter unit scale, this option
  converts too big meshes to Blender meter scale.
  (blender/blender-addons@675987e938)

#### Object Filter
- Both, the importer and the exporter got the new option to filter
  objects for import and export.  
  (blender/blender-addons!104778, blender/blender-addons!104782)

#### Volume, fog, gradient and background bitmap
- Atmosphere settings, layerfog parameter and background image can now
  be imported and exported.  
  (blender/blender-addons!104795, blender/blender-addons@6fad9e9725)
- Gradient and fog chunks can now be imported and exported.  
  (blender/blender-addons!104811, blender/blender-addons@a53788722b,
  blender/blender-addons@7cd6969b3e)

#### Spotlight aspect and projector
- If a spotlight includes a gobo image, it will be exported in the light
  bitmap chunk and imported the same way.  
  (blender/blender-addons!104813, blender/blender-addons@f1e443f119)
- The x/y scale of a spotlight can now be exported in the aspect ratio
  chunk, the importer calculates the aspect back to x/y scale.  
  (blender/blender-addons!104815, blender/blender-addons@7e2f96796a)

#### Cursor location
- The 3D cursor can now saved to a 3ds file and imported again. (blender/blender-addons!104797,
  blender/blender-addons@75ea7633f6)

#### New Principled BSDF material support
- Moved specular texture to specular tint. (blender/blender-addons!104918,
  blender/blender-addons@fef728a568)
- Added transmission and coat weight parameters. (blender/blender-addons@a5d3364c33,  
  blender/blender-addons@d82ce1770f, blender/blender-addons@9d57b190b8, blender/blender-addons@8f6d8d9fc9)
- Added tint colors for coat and sheen.
  (blender/blender-addons@ec069c3b6a)


## Blender 4.1

### Version 2.5.0

- Export auto smooth angle from ´Smooth by Angle ´modifier.
  (blender/blender-addons@9a9142f160)


## Blender 4.2

### Version 2.6.0

- Import is now possible by drag & drop from desktop window.
  (blender/blender-addons@79077f3b7f)
- Multiple selected files can now be imported.
  (blender/blender-addons!105227)
- Added option to create new collections for imported files.
  (blender/blender-addons!105232)
- Enabled the collection exporter feature.
  (blender/blender-addons@8250852c04)
- Added support to export non-mesh objects.
  (blender/blender-addons@540de86d70)
- Improved importing bitmap and gradient world nodes setup.
  (blender/blender-addons@e8c1acd430)
- Added distance cue import and export.
  (blender/blender-addons@0a2b786336, blender/blender-addons@f139aea3f6)

### Version 2.6.1

- Improved importing instanced objects. (extensions/io_scene_3ds@193e1355ea)