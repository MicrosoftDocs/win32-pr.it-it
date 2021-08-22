---
description: La funzione StretchDIBits copia i dati di colore per un rettangolo di pixel in un DIB nel rettangolo di destinazione specificato.
ms.assetid: d4e3f631-3852-4cee-8e97-2244c39b200e
title: Ridimensionamento di un'immagine JPEG o PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2380b03f562d950cf8ff9ca4ab03197b9da8eed02ac10652dcb120dce279895c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613681"
---
# <a name="sizing-a-jpeg-or-png-image"></a>Ridimensionamento di un'immagine JPEG o PNG

La [**funzione StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) copia i dati di colore per un rettangolo di pixel in un dib nel rettangolo di destinazione specificato. Se il rettangolo di destinazione è più grande del rettangolo di origine, questa funzione estende le righe e le colonne di dati di colore per adattarle al rettangolo di destinazione. Se il rettangolo di destinazione è più piccolo del rettangolo di origine, **StretchDIBits** comprime le righe e le colonne usando l'operazione raster specificata.

[**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) viene esteso per consentire il passare un'immagine JPEG o PNG come immagine di origine.

Ad esempio:


```C++
// pvJpgImage points to a buffer containing the JPEG image 
// nJpgImageSize is the size of the buffer 
// ulJpgWidth is the width of the JPEG image 
// ulJpgHeight is the height of the JPEG image 
// 

// 
// Check if CHECKJPEGFORMAT is supported (device has JPEG support) 
// and use it to verify that device can handle the JPEG image. 
// 

ul = CHECKJPEGFORMAT;

if (
    // Check if CHECKJPEGFORMAT exists: 

    (ExtEscape(hdc, QUERYESCSUPPORT,
               sizeof(ul), &ul, 0, 0) > 0) &&

    // Check if CHECKJPEGFORMAT executed without error: 

    (ExtEscape(hdc, CHECKJPEGFORMAT,
               nJpgImageSize, pvJpgImage, sizeof(ul), &ul) > 0) &&

    // Check status code returned by CHECKJPEGFORMAT: 

    (ul == 1)
   )
{
    // 
    // Initialize the BITMAPINFO. 
    // 

    memset(&bmi, 0, sizeof(bmi));
    bmi.bmiHeader.biSize        = sizeof(BITMAPINFOHEADER);
    bmi.bmiHeader.biWidth       = ulJpgWidth;
    bmi.bmiHeader.biHeight      = -ulJpgHeight; // top-down image 
    bmi.bmiHeader.biPlanes      = 1;
    bmi.bmiHeader.biBitCount    = 0;
    bmi.bmiHeader.biCompression = BI_JPEG;
    bmi.bmiHeader.biSizeImage   = nJpgImageSize;

    // 
    // Do the StretchDIBits. 
    // 

    iRet = StretchDIBits(hdc,
                         // destination rectangle 
                         ulDstX, ulDstY, ulDstWidth, ulDstHeight,
                         // source rectangle 
                         0, 0, ulJpgWidth, ulJpgHeight,
                         pvJpgImage,
                         &bmi,
                         DIB_RGB_COLORS,
                         SRCCOPY);

    if (iRet == GDI_ERROR)
        return FALSE;
}
else
{
    // 
    // Decompress image into a DIB and call StretchDIBits  
    // with the DIB instead. 
    // 
}
```



 

 



