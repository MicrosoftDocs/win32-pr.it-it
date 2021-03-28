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
# <a name="setting-the-alpha-values-of-individual-pixels"></a>Impostazione dei valori alfa dei singoli pixel

L'argomento [utilizzo di una matrice di colori per impostare i valori alfa nelle immagini](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) Mostra un metodo non distruttivo per la modifica dei valori alfa di un'immagine. Nell'esempio riportato in questo argomento viene eseguito il rendering di un'immagine semitransparently, ma i dati pixel nella bitmap non vengono modificati. I valori alfa vengono modificati solo durante il rendering.

Nell'esempio seguente viene illustrato come modificare i valori alfa dei singoli pixel. Il codice nell'esempio modifica effettivamente le informazioni alfa in un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . L'approccio è molto più lento rispetto all'uso di una matrice di colori e di un oggetto [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , ma consente di controllare i singoli pixel della bitmap.


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



Nell'illustrazione seguente viene mostrata l'immagine risultante.

![illustrazione che mostra un'immagine che diventa più opaca da sinistra verso destra, su un rettangolo nero](images/image3.png)

Nell'esempio di codice precedente vengono utilizzati cicli annidati per modificare il valore alfa di ogni pixel della bitmap. Per ogni pixel, [**bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) ottiene il colore esistente, [**color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) crea un colore temporaneo che contiene il nuovo valore alfa, quindi [**bitmap:: sepixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) imposta il nuovo colore. Il valore alfa viene impostato in base alla colonna della bitmap. Nella prima colonna, alfa è impostato su 0. Nell'ultima colonna Alpha è impostato su 255. Quindi, l'immagine risultante passa da completamente trasparente (sul bordo sinistro) a completamente opaca (sul bordo destro).

[**Bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) e [**bitmap:: sepixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) consentono di controllare i singoli valori dei pixel. Tuttavia, l'utilizzo di **bitmap:: GetPixel** e **bitmap:: sepixel** non è quasi altrettanto veloce quanto l'utilizzo della classe [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e della struttura [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .

 

 



