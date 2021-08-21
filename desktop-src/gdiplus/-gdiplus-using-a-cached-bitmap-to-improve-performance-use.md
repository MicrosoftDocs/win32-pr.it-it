---
description: Gli oggetti Image e Bitmap archiviano le immagini in un formato indipendente dal dispositivo.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Uso di una bitmap memorizzata nella cache per migliorare le prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ffee17a2c8d564a38235cc83d204eacc9b4edf2e8070cb5971d55f1f991169f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036329"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Uso di una bitmap memorizzata nella cache per migliorare le prestazioni

[**Gli**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) oggetti [**Image e Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) archiviano le immagini in un formato indipendente dal dispositivo. Un [**oggetto CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) archivia un'immagine nel formato del dispositivo di visualizzazione corrente. Il rendering di un'immagine archiviata in un oggetto **CachedBitmap** è veloce perché non viene impiegato alcun tempo di elaborazione per convertire l'immagine nel formato richiesto dal dispositivo di visualizzazione.

Nell'esempio seguente vengono creati un [**oggetto Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e un [**oggetto CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) dal file Texture.jpg. Le **proprietà Bitmap** e **CachedBitmap** vengono disegnate 30.000 volte. Se si esegue il codice, le immagini **CachedBitmap** vengono disegnate in modo notevolmente più veloce rispetto alle **immagini bitmap.**


```
Bitmap        bitmap(L"Texture.jpg");
UINT          width = bitmap.GetWidth();
UINT          height = bitmap.GetHeight();
CachedBitmap  cBitmap(&bitmap, &graphics);
int           j, k;
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
     graphics.DrawImage(&bitmap, j, j / 2, width, height);
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
      graphics.DrawCachedBitmap(&cBitmap, j, 150 + j / 2 );
```



> [!Note]  
> Un [**oggetto CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) corrisponde al formato del dispositivo di visualizzazione al momento della costruzione dell'oggetto **CachedBitmap.** Se l'utente del programma modifica le impostazioni di visualizzazione, il codice deve costruire un nuovo **oggetto CachedBitmap.** Il **metodo DrawImage** avrà esito negativo se si passa un **oggetto CachedBitmap** creato prima di una modifica nel formato di visualizzazione.

 

 

 



