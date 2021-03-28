---
description: Gli oggetti Image e Bitmap archiviano le immagini in un formato indipendente dal dispositivo.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Utilizzo di una bitmap memorizzata nella cache per migliorare le prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8e546460741342bcac8f1633e21d104984af9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994173"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Utilizzo di una bitmap memorizzata nella cache per migliorare le prestazioni

Gli oggetti [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) archiviano le immagini in un formato indipendente dal dispositivo. Un oggetto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) archivia un'immagine nel formato del dispositivo di visualizzazione corrente. Il rendering di un'immagine archiviata in un oggetto **CachedBitmap** è veloce perché non viene impiegato alcun tempo di elaborazione per la conversione dell'immagine nel formato richiesto dal dispositivo di visualizzazione.

Nell'esempio seguente vengono creati un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e un oggetto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) dal file Texture.jpg. La **bitmap** e il **CachedBitmap** sono disegnati ogni 30.000 volte. Se si esegue il codice, si noterà che le immagini **CachedBitmap** vengono disegnate notevolmente più velocemente delle immagini **bitmap** .


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
> Un oggetto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) corrisponde al formato del dispositivo di visualizzazione nel momento in cui è stato creato l'oggetto **CachedBitmap** . Se l'utente del programma modifica le impostazioni di visualizzazione, il codice deve costruire un nuovo oggetto **CachedBitmap** . Il metodo **DrawImage** avrà esito negativo se si passa un oggetto **CachedBitmap** creato prima di una modifica nel formato di visualizzazione.

 

 

 



