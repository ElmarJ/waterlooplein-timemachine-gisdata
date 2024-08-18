# Waterlooplein Timemachine: GIS data
Project to reconstruct the development of the Waterlooplein neighborhood between 1800 and 2000 in GeoJson. Data is used by the [Waterlooplein Time Machine project](https://github.com/ElmarJ/waterlooplein-timemachine). See [https://waterlooplein3d.nl] for more information about the whole project.

## Aim
Reconstruct vector maps of Amsterdam around 1880. This project serves as the basis for a 3D Unity project, which makes it possible to walk through a reconstruction of Amsterdam around 1880. The current focus is on the Waterloopleinbuurt, mainly because this neighborhood is the most interesting (as it changed entirely), and also because I live there. :)

## Notes about the process
Because I began this project with a very specific purpose in mind (the 3D project mentioned above), it is important to see what I do and what I do not intent. A few points:

- The map is primarily based on the Loman Buurtatlas.
- Relative accuracy is more important than absolute positions. As the intention is to create a 3D-world that convincingly models Amsterdam, I rather have inaccuracies in absolute position than inaccuracies in the relation between buildings and other constructions. For example: it is important that buildings connect perfectly - else we end up with weird allies and other artifacts. Same applies to the relation between canals and buildings: if a building is built next to the water, the edges of the building polygon and the canal-island polygon should overlap perfectly.
- If the Lohman map positions are inaccurate, we should try to follow real world map positions as much as possible - so where possible, I'll try to do better than the Lohman map if I know better. This means for example that historical buildings that still exist, can probably be mapped more accurately straight from (more) modern maps. However, this means that we have to take care not to break local accuracy (so previous point).
- Because my core interest lies in reconstructing the Waterlooplein neighborhood, 

## Contributing
All contributions are welcome! The repository contains a QGis file (see https://www.qgis.org/) that can be opened to edit the geoJSON-files.

## Roadmap
Some plans:
- Merge / incorporate data from more reliable and better documented sources, such as:
  - http://verdwenengebouwen.nl/
  - http://histograph.io/ (see also https://github.com/histograph)
  - http://3dbag.bk.tudelft.nl/ (see also https://github.com/tudelft3d/3dfier)
- Store more building-characteristics, such as height, building type, facade type (e.g. klokgevel / lijstgevel / trapgevel), facade direction (normal of the front wall), window grid (number of floors, number of windows per floor). All these characteristics could be taken into account when making the 3D reconstruction
- Map bridges (probably as vector with width en type parameters)
- Map street level height
