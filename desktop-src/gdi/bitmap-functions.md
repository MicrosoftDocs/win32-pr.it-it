---
description: Le funzioni seguenti vengono utilizzate con le bitmap.
ms.assetid: ef3abc8a-5d95-41d0-8eb6-47719d472414
title: Funzioni bitmap (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e61ef02f5065d746f0d82a7b3352c3445ebf61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994133"
---
# <a name="bitmap-functions-windows-gdi"></a>Funzioni bitmap (Windows GDI)

Le funzioni seguenti vengono utilizzate con le bitmap.



| Funzione                                                 | Descrizione                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)                         | Visualizza una bitmap con pixel trasparenti o semitrasparenti.  |
| [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)                                 | Esegue un trasferimento a blocchi di bit.                                 |
| [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)                     | Crea una bitmap.                                              |
| [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)     | Crea una bitmap.                                              |
| [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) | Crea una bitmap compatibile con un dispositivo.                     |
| [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                 | Crea una bitmap dipendente dal dispositivo (DDB) da un DIB.            |
| [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)             | Crea una DIB in cui le applicazioni possono scrivere direttamente.         |
| [**ExtFloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-extfloodfill)                     | Riempie un'area della superficie di visualizzazione con il pennello corrente.   |
| [**GetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapdimensionex)     | Ottiene le dimensioni di una bitmap.                               |
| [**GetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-getdibcolortable)             | Recupera i valori di colore RGB da una bitmap di sezione DIB.          |
| [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits)                           | Copia una bitmap in un buffer.                                 |
| [**GetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-getpixel)                             | Ottiene il valore di colore RGB del pixel in corrispondenza di una determinata coordinata.   |
| [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode)           | Ottiene la modalità di adattamento corrente.                              |
| [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)                     | Riempie le strutture Rectangle e Triangle.                       |
| [**LoadBitmap**](/windows/desktop/api/Winuser/nf-winuser-loadbitmapa)                         | Carica una bitmap da un file eseguibile del modulo.                |
| [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)                               | Combina i dati del colore nelle bitmap di origine e di destinazione. |
| [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt)                                 | Esegue un trasferimento a blocchi di bit.                                 |
| [**SetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapdimensionex)     | Imposta le dimensioni preferite su una bitmap.                     |
| [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)             | Imposta i valori RGB in una DIB.                                      |
| [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)                           | Imposta i pixel in una bitmap usando i dati di colore di una DIB.       |
| [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)           | Imposta i pixel in un rettangolo usando i dati di colore di una DIB.    |
| [**SetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-setpixel)                             | Imposta il colore per un pixel.                                    |
| [**SetPixelV**](/windows/desktop/api/Wingdi/nf-wingdi-setpixelv)                           | Imposta un pixel sulla migliore approssimazione di un colore.             |
| [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode)           | Imposta la modalità di adattamento della bitmap.                               |
| [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)                         | Copia una bitmap e la estende o la comprime.                |
| [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)                   | Copia i dati del colore in una DIB.                                |
| [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt)                 | Esegue un trasferimento a blocchi di bit dei dati relativi al colore.                   |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

Le funzioni seguenti vengono fornite solo per la compatibilità con le versioni a 16 bit di Microsoft Windows:

-   [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)
-   [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)
-   [**GetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapbits)
-   [**SetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapbits)

 

 



