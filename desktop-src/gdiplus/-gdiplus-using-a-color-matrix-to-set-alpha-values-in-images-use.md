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
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a>Uso di una matrice di colori per impostare valori alfa nelle immagini

La classe [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) (che eredita dalla classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ) e la classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) forniscono funzionalità per ottenere e impostare i valori dei pixel. È possibile utilizzare la classe **ImageAttributes** per modificare i valori alfa per un'intera immagine oppure è possibile chiamare il metodo [**bitmap:: sepixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) della classe **bitmap** per modificare i valori dei singoli pixel. Per ulteriori informazioni sull'impostazione di singoli valori pixel, vedere [impostazione dei valori alfa dei singoli pixel](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).

Nell'esempio seguente viene disegnata una linea nera ampia e viene visualizzata un'immagine opaca che copre parte della riga.


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



Nella figura seguente viene illustrata l'immagine risultante, disegnata in corrispondenza di (30, 0). Si noti che la linea nera estesa non viene visualizzata nell'immagine.

![illustrazione che mostra un'immagine opaca sovrapposta a un rettangolo sottile, ampio e nero](images/image1.png)

La classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) dispone di molte proprietà che è possibile utilizzare per modificare le immagini durante il rendering. Nell'esempio seguente viene usato un oggetto **ImageAttributes** per impostare tutti i valori alfa sul 80% di ciò che erano. Questa operazione viene eseguita inizializzando una matrice di colori e impostando il valore di scalabilità alfa nella matrice su 0,8. L'indirizzo della matrice di colori viene passato al metodo [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) dell'oggetto **ImageAttributes** e l'indirizzo dell'oggetto **ImageAttributes** viene passato al metodo [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .


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



Durante il rendering, i valori alfa nella bitmap vengono convertiti nel 80% di ciò che erano. In questo modo si ottiene un'immagine che viene fusa con lo sfondo. Come illustrato nella figura seguente, l'immagine bitmap sembra trasparente; è possibile visualizzare la linea nera a tinta unita.

![illustrazione simile a quella precedente, ma l'immagine è sem-trasparente](images/image2.png)

Quando l'immagine è sulla parte bianca dello sfondo, l'immagine è stata mescolata con il colore bianco. Quando l'immagine incrocia la linea nera, l'immagine viene fusa con il colore nero.

 

 



