---
description: Il rimapping è il processo di conversione dei colori in un'immagine in base a una tabella di modifica del mapping dei colori. La tabella di modifica del mapping dei colori è una matrice di strutture mappate. Ogni struttura della mappa colori nella matrice ha un membro oldColor e un membro newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Uso di una tabella di rimappatura dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129055"
---
# <a name="using-a-color-remap-table"></a><span data-ttu-id="43f29-105">Uso di una tabella di rimappatura dei colori</span><span class="sxs-lookup"><span data-stu-id="43f29-105">Using a Color Remap Table</span></span>

<span data-ttu-id="43f29-106">Il rimapping è il processo di conversione dei colori in un'immagine in base a una tabella di modifica del mapping dei colori.</span><span class="sxs-lookup"><span data-stu-id="43f29-106">Remapping is the process of converting the colors in an image according to a color remap table.</span></span> <span data-ttu-id="43f29-107">La tabella di modifica del mapping dei colori è una matrice di strutture [**mappate**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="43f29-107">The color remap table is an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="43f29-108">Ogni struttura della **mappa colori** nella matrice ha un membro **oldColor** e un membro **NewColor** .</span><span class="sxs-lookup"><span data-stu-id="43f29-108">Each **ColorMap** structure in the array has an **oldColor** member and a **newColor** member.</span></span>

<span data-ttu-id="43f29-109">Quando GDI+ disegna un'immagine, ogni pixel dell'immagine viene confrontato con la matrice dei colori precedenti.</span><span class="sxs-lookup"><span data-stu-id="43f29-109">When GDI+ draws an image, each pixel of the image is compared to the array of old colors.</span></span> <span data-ttu-id="43f29-110">Se il colore di un pixel corrisponde a un colore precedente, il colore viene modificato nel nuovo colore corrispondente.</span><span class="sxs-lookup"><span data-stu-id="43f29-110">If a pixel's color matches an old color, its color is changed to the corresponding new color.</span></span> <span data-ttu-id="43f29-111">I colori vengono modificati solo per il rendering: i valori dei colori dell'immagine stessa (archiviati in un' [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) o in un oggetto [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) ) non vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="43f29-111">The colors are changed only for rendering — the color values of the image itself (stored in an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object) are not changed.</span></span>

<span data-ttu-id="43f29-112">Per tracciare un'immagine rimappata, inizializzare una matrice di strutture della [**mappa colori**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="43f29-112">To draw a remapped image, initialize an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="43f29-113">Passare l'indirizzo della matrice al metodo [**ImageAttributes:: SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) di un oggetto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , quindi passare l'indirizzo dell'oggetto **ImageAttributes** al metodo [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="43f29-113">Pass the address of that array to the [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) method of an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object, and then pass the address of the **ImageAttributes** object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="43f29-114">Nell'esempio seguente viene creato un oggetto [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) dal file RemapInput.bmp.</span><span class="sxs-lookup"><span data-stu-id="43f29-114">The following example creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file RemapInput.bmp.</span></span> <span data-ttu-id="43f29-115">Il codice consente di creare una tabella di modifica del mapping dei colori costituita da una singola struttura della [**mappa colori**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="43f29-115">The code creates a color remap table that consists of a single [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structure.</span></span> <span data-ttu-id="43f29-116">Il membro **oldColor** della struttura **mappa colori** è rosso e il membro **NewColor** è blu.</span><span class="sxs-lookup"><span data-stu-id="43f29-116">The **oldColor** member of the **ColorMap** structure is red, and the **newColor** member is blue.</span></span> <span data-ttu-id="43f29-117">L'immagine viene disegnata una volta senza modificarne il mapping e una volta con il mapping.</span><span class="sxs-lookup"><span data-stu-id="43f29-117">The image is drawn once without remapping and once with remapping.</span></span> <span data-ttu-id="43f29-118">Il processo di modifica del mapping modifica tutti i pixel rossi in blu.</span><span class="sxs-lookup"><span data-stu-id="43f29-118">The remapping process changes all the red pixels to blue.</span></span>


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="43f29-119">Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine rimappata a destra.</span><span class="sxs-lookup"><span data-stu-id="43f29-119">The following illustration shows the original image on the left and the remapped image on the right.</span></span>

![illustrazione che mostra due versioni di un'immagine multicolore; l'area rossa nella prima versione è blu nella seconda versione](images/colortrans7.png)

 

 



