## Why must distance of near plane from camera be > 0?
* All points will be projected to the camera origin (see matrix)
* Perpsective divide by zero *(Wc = -Ze = 0)*
* Rule of Similar Triangles cannot be used
* Even in Computer Vision, the image plane is not on the camera origin
* The function of *Ze* vs *Zn* is logarithmic; if *Ze = 0*, *Zn* approaches -∞

## Why must far plane be as close as possible to near plane?
* Again with the logarithmic relationship; if f is large, a change in *Ze* at that region will not be noticeable in *Zn*, causing z-fighting

## TL;DR
min *(f - n)*,  
s.t. *(n > 0)*
