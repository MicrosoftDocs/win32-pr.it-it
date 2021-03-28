---
description: La classe bitmap (che eredita dalla classe Image) e la classe ImageAttributes forniscono funzionalità per ottenere e impostare i valori dei pixel.
ms.assetid: e3d67431-6098-4b2a-8910-5695a8473216
title: Uso di una matrice di colori per impostare valori alfa nelle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81180b1f09b11e37b322e37106dab1879a00bbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526059"
---
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a><span data-ttu-id="d39a0-103">Uso di una matrice di colori per impostare valori alfa nelle immagini</span><span class="sxs-lookup"><span data-stu-id="d39a0-103">Using a Color Matrix to Set Alpha Values in Images</span></span>

<span data-ttu-id="d39a0-104">La classe [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) (che eredita dalla classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ) e la classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) forniscono funzionalità per ottenere e impostare i valori dei pixel.</span><span class="sxs-lookup"><span data-stu-id="d39a0-104">The [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class (which inherits from the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class) and the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class provide functionality for getting and setting pixel values.</span></span> <span data-ttu-id="d39a0-105">È possibile utilizzare la classe **ImageAttributes** per modificare i valori alfa per un'intera immagine oppure è possibile chiamare il metodo [**bitmap:: sepixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) della classe **bitmap** per modificare i valori dei singoli pixel.</span><span class="sxs-lookup"><span data-stu-id="d39a0-105">You can use the **ImageAttributes** class to modify the alpha values for an entire image, or you can call the [**Bitmap::SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) method of the **Bitmap** class to modify individual pixel values.</span></span> <span data-ttu-id="d39a0-106">Per ulteriori informazioni sull'impostazione di singoli valori pixel, vedere [impostazione dei valori alfa dei singoli pixel](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span><span class="sxs-lookup"><span data-stu-id="d39a0-106">For more information on setting individual pixel values, see [Setting the Alpha Values of Individual Pixels](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span></span>

<span data-ttu-id="d39a0-107">Nell'esempio seguente viene disegnata una linea nera ampia e viene visualizzata un'immagine opaca che copre parte della riga.</span><span class="sxs-lookup"><span data-stu-id="d39a0-107">The following example draws a wide black line and then displays an opaque image that covers part of that line.</span></span>


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



<span data-ttu-id="d39a0-108">Nella figura seguente viene illustrata l'immagine risultante, disegnata in corrispondenza di (30, 0).</span><span class="sxs-lookup"><span data-stu-id="d39a0-108">The following illustration shows the resulting image, which is drawn at (30, 0).</span></span> <span data-ttu-id="d39a0-109">Si noti che la linea nera estesa non viene visualizzata nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="d39a0-109">Note that the wide black line doesn't show through the image.</span></span>

![illustrazione che mostra un'immagine opaca sovrapposta a un rettangolo sottile, ampio e nero](images/image1.png)

<span data-ttu-id="d39a0-111">La classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) dispone di molte proprietà che è possibile utilizzare per modificare le immagini durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="d39a0-111">The [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class has many properties that you can use to modify images during rendering.</span></span> <span data-ttu-id="d39a0-112">Nell'esempio seguente viene usato un oggetto **ImageAttributes** per impostare tutti i valori alfa sul 80% di ciò che erano.</span><span class="sxs-lookup"><span data-stu-id="d39a0-112">In the following example, an **ImageAttributes** object is used to set all the alpha values to 80 percent of what they were.</span></span> <span data-ttu-id="d39a0-113">Questa operazione viene eseguita inizializzando una matrice di colori e impostando il valore di scalabilità alfa nella matrice su 0,8.</span><span class="sxs-lookup"><span data-stu-id="d39a0-113">This is done by initializing a color matrix and setting the alpha scaling value in the matrix to 0.8.</span></span> <span data-ttu-id="d39a0-114">L'indirizzo della matrice di colori viene passato al metodo [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) dell'oggetto **ImageAttributes** e l'indirizzo dell'oggetto **ImageAttributes** viene passato al metodo [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="d39a0-114">The address of the color matrix is passed to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object, and the address of the **ImageAttributes** object is passed to the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
// Create a Bitmap object and load it with the texture image.
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// Initialize the color matrix.
// Notice the value 0.8 in row 4, column 4.
ColorMatrix colorMatrix = {1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.8f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
// Create an ImageAttributes object and set its color matrix.
ImageAttributes imageAtt;
imageAtt.SetColorMatrix(&colorMatrix, ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw the semitransparent bitmap image.
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
graphics.DrawImage(
   &bitmap, 
   Rect(30, 0, iWidth, iHeight),  // Destination rectangle
   0,                             // Source rectangle X 
   0,                             // Source rectangle Y
   iWidth,                        // Source rectangle width
   iHeight,                       // Source rectangle height
   UnitPixel, 
   &imageAtt);
```



<span data-ttu-id="d39a0-115">Durante il rendering, i valori alfa nella bitmap vengono convertiti nel 80% di ciò che erano.</span><span class="sxs-lookup"><span data-stu-id="d39a0-115">During rendering, the alpha values in the bitmap are converted to 80 percent of what they were.</span></span> <span data-ttu-id="d39a0-116">In questo modo si ottiene un'immagine che viene fusa con lo sfondo.</span><span class="sxs-lookup"><span data-stu-id="d39a0-116">This results in an image that is blended with the background.</span></span> <span data-ttu-id="d39a0-117">Come illustrato nella figura seguente, l'immagine bitmap sembra trasparente; è possibile visualizzare la linea nera a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="d39a0-117">As the following illustration shows, the bitmap image looks transparent; you can see the solid black line through it.</span></span>

![illustrazione simile a quella precedente, ma l'immagine è sem-trasparente](images/image2.png)

<span data-ttu-id="d39a0-119">Quando l'immagine è sulla parte bianca dello sfondo, l'immagine è stata mescolata con il colore bianco.</span><span class="sxs-lookup"><span data-stu-id="d39a0-119">Where the image is over the white portion of the background, the image has been blended with the color white.</span></span> <span data-ttu-id="d39a0-120">Quando l'immagine incrocia la linea nera, l'immagine viene fusa con il colore nero.</span><span class="sxs-lookup"><span data-stu-id="d39a0-120">Where the image crosses the black line, the image is blended with the color black.</span></span>

 

 



