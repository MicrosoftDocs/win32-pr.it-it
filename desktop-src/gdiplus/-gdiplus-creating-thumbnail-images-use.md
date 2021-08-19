---
description: Un'immagine di anteprima è una versione ridotta di un'immagine. È possibile creare un'immagine di anteprima chiamando il metodo GetThumbnailImage di un oggetto Image.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Creazione di immagini di anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d44fec3220bef7a6691d3852d16f90e9cf43635c99f69bba16f3b569ebabc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696312"
---
# <a name="creating-thumbnail-images"></a>Creazione di immagini di anteprima

Un'immagine di anteprima è una versione ridotta di un'immagine. È possibile creare un'immagine di anteprima chiamando il **metodo GetThumbnailImage** di un [**oggetto**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Image.

Nell'esempio seguente viene costruito un [**oggetto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Compass.bmp. L'immagine originale ha una larghezza di 640 pixel e un'altezza di 479 pixel. Il codice crea un'immagine di anteprima con una larghezza di 100 pixel e un'altezza di 100 pixel.


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



La figura seguente mostra l'immagine di anteprima.

![Illustrazione di un piccolo grafico che mostra una bussola](images/thumbnail1.png)

 

 



