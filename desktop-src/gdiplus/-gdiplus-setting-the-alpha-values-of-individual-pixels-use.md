---
description: L'argomento utilizzo di una matrice di colori per impostare i valori alfa nelle immagini Mostra un metodo non distruttivo per la modifica dei valori alfa di un'immagine.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Impostazione dei valori alfa dei singoli pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526071"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a><span data-ttu-id="1a189-103">Impostazione dei valori alfa dei singoli pixel</span><span class="sxs-lookup"><span data-stu-id="1a189-103">Setting the Alpha Values of Individual Pixels</span></span>

<span data-ttu-id="1a189-104">L'argomento [utilizzo di una matrice di colori per impostare i valori alfa nelle immagini](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) Mostra un metodo non distruttivo per la modifica dei valori alfa di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="1a189-104">The topic [Using a Color Matrix to Set Alpha Values in Images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) shows a nondestructive method for changing the alpha values of an image.</span></span> <span data-ttu-id="1a189-105">Nell'esempio riportato in questo argomento viene eseguito il rendering di un'immagine semitransparently, ma i dati pixel nella bitmap non vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="1a189-105">The example in that topic renders an image semitransparently, but the pixel data in the bitmap is not changed.</span></span> <span data-ttu-id="1a189-106">I valori alfa vengono modificati solo durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="1a189-106">The alpha values are altered only during rendering.</span></span>

<span data-ttu-id="1a189-107">Nell'esempio seguente viene illustrato come modificare i valori alfa dei singoli pixel.</span><span class="sxs-lookup"><span data-stu-id="1a189-107">The following example shows how to change the alpha values of individual pixels.</span></span> <span data-ttu-id="1a189-108">Il codice nell'esempio modifica effettivamente le informazioni alfa in un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="1a189-108">The code in the example actually changes the alpha information in a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="1a189-109">L'approccio è molto più lento rispetto all'uso di una matrice di colori e di un oggetto [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , ma consente di controllare i singoli pixel della bitmap.</span><span class="sxs-lookup"><span data-stu-id="1a189-109">The approach is much slower than using a color matrix and an [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object but gives you control over the individual pixels in the bitmap.</span></span>


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



<span data-ttu-id="1a189-110">Nell'illustrazione seguente viene mostrata l'immagine risultante.</span><span class="sxs-lookup"><span data-stu-id="1a189-110">The following illustration shows the resulting image.</span></span>

![illustrazione che mostra un'immagine che diventa più opaca da sinistra verso destra, su un rettangolo nero](images/image3.png)

<span data-ttu-id="1a189-112">Nell'esempio di codice precedente vengono utilizzati cicli annidati per modificare il valore alfa di ogni pixel della bitmap.</span><span class="sxs-lookup"><span data-stu-id="1a189-112">The preceding code example uses nested loops to change the alpha value of each pixel in the bitmap.</span></span> <span data-ttu-id="1a189-113">Per ogni pixel, [**bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) ottiene il colore esistente, [**color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) crea un colore temporaneo che contiene il nuovo valore alfa, quindi [**bitmap:: sepixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) imposta il nuovo colore.</span><span class="sxs-lookup"><span data-stu-id="1a189-113">For each pixel, [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) gets the existing color, [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) creates a temporary color that contains the new alpha value, and then [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) sets the new color.</span></span> <span data-ttu-id="1a189-114">Il valore alfa viene impostato in base alla colonna della bitmap.</span><span class="sxs-lookup"><span data-stu-id="1a189-114">The alpha value is set based on the column of the bitmap.</span></span> <span data-ttu-id="1a189-115">Nella prima colonna, alfa è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="1a189-115">In the first column, alpha is set to 0.</span></span> <span data-ttu-id="1a189-116">Nell'ultima colonna Alpha è impostato su 255.</span><span class="sxs-lookup"><span data-stu-id="1a189-116">In the last column, alpha is set to 255.</span></span> <span data-ttu-id="1a189-117">Quindi, l'immagine risultante passa da completamente trasparente (sul bordo sinistro) a completamente opaca (sul bordo destro).</span><span class="sxs-lookup"><span data-stu-id="1a189-117">So the resulting image goes from fully transparent (on the left edge) to fully opaque (on the right edge).</span></span>

<span data-ttu-id="1a189-118">[**Bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) e [**bitmap:: sepixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) consentono di controllare i singoli valori dei pixel.</span><span class="sxs-lookup"><span data-stu-id="1a189-118">[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) and [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) give you control of the individual pixel values.</span></span> <span data-ttu-id="1a189-119">Tuttavia, l'utilizzo di **bitmap:: GetPixel** e **bitmap:: sepixel** non è quasi altrettanto veloce quanto l'utilizzo della classe [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e della struttura [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="1a189-119">However, using **Bitmap::GetPixel** and **Bitmap::SetPixel** is not nearly as fast as using the [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class and the [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>

 

 



