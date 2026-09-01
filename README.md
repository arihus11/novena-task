# NovenaTask
**Simple Windows 2D application made with Unity3D for the Novena Task**

**1.**

The executable file is located inside the `NovenaAppExe` folder, while the source code is located inside `NovenaAppSrc/NovenaApp`.

**2.**

Data is stored in a JSON file only for the gallery elements, and the entire gallery is loaded during the initialization of the third screen. Each gallery element is defined by its name and image.

Other text and graphical elements are not stored as data but are defined by default. The idea was to use the same approach for storing and loading data for the content of the second screen, as I assume that in a real application it would also be possible to list elements there. However, due to the lack of data for that screen (texts, images, etc.), its content is hardcoded. The interactive element on that screen is stored as a prefab.

**3.**

Bilingual support is implemented only on the second screen. Selecting the other language on any screen will change the text only on the second screen.

This was implemented solely for testing purposes. If more data were available, the same approach could be used to change the text throughout the entire application. Naturally, this would also require a greater level of code structure and organization.

**4.**

The gallery elements have been converted into prefabs, while the gallery itself is generally designed as a `ScriptableObject`. Given the simplicity of this version of the application, the additional functionality that could be achieved through this approach has not been implemented. Therefore, the gallery `ScriptableObject` currently stores only the currently selected gallery element and the list of gallery elements.

Such an implementation would also significantly improve the structure and functionality of the code.

**5.**

No animations have been implemented, such as scene transitions or element selection animations, as these were not specifically requested. Interactive text elements have a highlight effect, but other icons representing buttons do not.

**6.**

When selecting an element in the gallery, the enlarged image is not in the format it ideally should be. Instead, it is the same Sprite used as the element's icon, simply displayed at a larger scale.

The reason for this is that I was unable to obtain the original full-resolution images from Figma.

**7.**

When selecting an element within the gallery, an overlay is displayed over the selected element, as expected. The overlay must be closed before another element can be selected.

This functionality was implemented intentionally. If necessary, it could also be modified so that selecting another element automatically closes the overlay of the previously selected element.

**8.**

One of the fonts used in the Figma design is a custom font, so I was unable to use it. Instead, another available font downloaded from DaFont.com was used.
