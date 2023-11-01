# Kocsis & Scotese Model

This model is imported from the PaleoMap model
and the paleocoastline model of Kocsis and Scotese (2021),
which is found in the supplementary information
of that [paper](https://doi.org/10.1016/j.earscirev.2020.103463).

## Time frame

The rotations are defined from 540 million years ago
(up to 600 for the plate motion model)
to today,
in time stages of 5 million years.

## Pixelation

The model is available in three resolutions:
e360 (360 pixels in the equatorial ring),
e180,
and e120.
For reference,
Pixel IDs are stored as `pixel-ids-xxx.tab`,
in which `xxx` is used to indicate the resolution.

## File descriptions

All the model files are prefixed as `kocsis-*`
usually followed by the pixelation resolution,
the size of the time step,
and the kind of file.

### Pixelated features

It is based on the plate polygons
from the PaleoMap model
(Scotese, 2016),
but using the updates found in the supplementary information
of Kocsis and Scotese (2021).
It is stored in the file `kocsis-pixels-xxx.tab`,
in which `xxx` is used to indicate the resolution.

### Plate motion model

The plate motion model
(or rotation model)
was the PaleoMap model of Scotese (2016),
updated with version *v19o_r1c*,
found in the supplementary information
of Kocsis and Scotese (2021).

The model is stored in the file `kocsis-motion-xxx-5.tab`,
in which `xxx` is the pixelation resolution
and 5 is the time resolution (in million years).

### Paleolandscape

The landscape features are taken from the plate polygons
(for the continental crust borders)
and from the paleocoastlines of Kocsis and Scotese (2021).
The digitalization uses the following convetions
to make it more or less compatible with the [EarthByte model](https://github.com/js-arias/gm-earthbyte):

Elevation   | Key | Environment
----------- | --- | -----------
0m or more  |   3 | emerged land
0 tp -1500m |   1 | continental shelf

Note that this paleolandscape does not include glacial ice sheets.

The model is stored in the file `kocsis-landscape-xxx-5.tab`,
in which `xxx` is the pixel resolution
and 5 is the time resolution (in million years).

A color key, which is compatible with color blindness
and can be used with the `plates timepix map` [command](https://github.com/js-arias/earth),
is stored in the file `kocsis-landscape-key.tab`.

## Citation and data license

This model is the product of the direct processing
of the Kocsis and Scotese (2021) model files.
As such,
the original publication should be cited
when the model is used.
Relevant papers are given in this file
and provided as bibTeX.

It is not required to cite this repository,
but if you do not include the model in the supplementary material
of your publication,
it might be a good idea to link this repository
and help others to replicate or re-use your analysis.

## Disclaimer

As the models are a product of a pixelation of vectorial models,
it is possible that some pixels will not be defined,
particularly in the boundaries of plates.
Depending on the usage of the models,
this problem will be either annoying
(for example,
a deep ocean pixel in the middle of a continent)
or critical
(if the feature of interest is near the absent pixel).
So be careful when using the models.

## References

Kocsis, Á. T., & Scotese, C. R.
(2021)
Mapping paleocoastlines and continental flooding during the Phanerozoic.
Earth-Science Reviews, 213, 103463.
DOI: [10.1016/j.earscirev.2020.103463](https://doi.org/10.1016/j.earscirev.2020.103463).

Scotese, C.S.
(2016)
PALEOMAP PaleoAtlas for GPlates.
URL: <https://www.earthbyte.org/paleomap-paleoatlas-for-gplates/>.
