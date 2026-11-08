--------------------
OPS STAIN SEPARATION
--------------------



1. VERSION AND AUTHOR

Version: 1.9.1
Name: © Nektarios Valous
Website: https://nekvalous.github.io



2. INSTALLATION

Requirements: ImageJ1 or Fiji with ImageJ1 support, Java 8 or newer.

1. Close ImageJ/Fiji.
2. Locate OPS_Stain_Separation.jar.
3. Copy the JAR into your ImageJ/Fiji plugins folder, for example:
   Fiji.app/plugins/ or ImageJ/plugins/.
   On macOS, use Show Package Contents if needed.
4. Remove older or duplicate copies of this plugin.
5. Restart ImageJ/Fiji.
6. Open Plugins > OPS Stain Separation > Separate Stains...

Install the JAR. Keep the underscores in the JAR filename.
No compiler or additional numerical libraries are needed to run it.



3. HOW TO USE THE PLUGIN

Prepare your image:

Open a single 24-bit RGB image in ImageJ/Fiji. To work with a slice from
an image stack, first duplicate that slice as a single RGB image.


Select a stain combination. Choose exactly one checkbox:

- H + E
- Blue + Brown
- Blue + Red
- Blue + Green
- Blue + Brown + Red

Processing cannot continue until you select a combination.


Automated mode:

1. Keep Automated (Macenko), the default mode, selected.
2. Select your stain combination and leave the other settings at their
   defaults for a first run.
3. Click Separate.


Manual mode:

1. Choose Manual in the same form and select your stain combination.
2. Click the first sampling button, such as Pick H or Pick Blue.
3. Click one representative pixel of that stain in the source image.
   The cursor becomes a crosshair and advances to the next stain.
4. Click one pixel for each remaining stain in the displayed order.
   Use exactly one click per stain: two clicks for a two-stain selection,
   or three clicks for Blue + Brown + Red.
5. Click Separate once all stains have been selected.


Choose distinct stained pixels and avoid white background, pure black,
and strongly mixed colors. You do not need to draw a region of interest.
To replace a sample, click its named sampling button and choose again.
If the form rejects a sample, choose a different stained pixel.


Challenging case:

For an image that is difficult to separate, select Challenging case
before clicking Separate. This option is available in both modes.


Save your results:

The plugin opens two or three final grayscale images, depending on your
selection. It does not open a processing log or intermediate images.
Save each result using ImageJ's File > Save As menu. Results are not
saved automatically.


Controls:

- Escape stops pixel selection.
- Cancel closes the form.
- Changing the source image clears the manual samples. Select them again
  before running Manual mode.
- If Separate is disabled, check that a stain combination is selected
  and all required manual samples are complete.



4. CITATIONS

Please cite both papers:

1. Valous, N. A., et al. (2025).
   Computational workflows for natural and biomedical image processing
   based on hypercomplex algebras.
   Patterns, 6(11), 101388.
   https://doi.org/10.1016/j.patter.2025.101388
   https://www.cell.com/patterns/fulltext/S2666-3899(25)00236-3

2. Valous, N. A., et al. (2026).
   Protocol for natural and biomedical image processing in the hypercomplex
   domain using the 2D orthogonal planes split.
   STAR Protocols, 7(2), 104548.
   https://doi.org/10.1016/j.xpro.2026.104548
   https://www.cell.com/star-protocols/fulltext/S2666-1667(26)00201-7

Additional references:

3. Macenko, M., Niethammer, M., Marron, J. S., Borland, D., Woosley, J. T.,
   Guan, X., Schmitt, C., and Thomas, N. E. (2009).
   A method for normalizing histology slides for quantitative analysis.
   IEEE International Symposium on Biomedical Imaging: From Nano to Macro,
   1107-1110.
   https://doi.org/10.1109/ISBI.2009.5193250

Citation links are also available at:
Plugins > OPS Stain Separation > About and Citations...