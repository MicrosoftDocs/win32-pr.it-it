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
# <a name="using-a-cached-bitmap-to-improve-performance"></a><span data-ttu-id="9d94b-103">Utilizzo di una bitmap memorizzata nella cache per migliorare le prestazioni</span><span class="sxs-lookup"><span data-stu-id="9d94b-103">Using a Cached Bitmap to Improve Performance</span></span>

<span data-ttu-id="9d94b-104">Gli oggetti [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) archiviano le immagini in un formato indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9d94b-104">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) objects store images in a device-independent format.</span></span> <span data-ttu-id="9d94b-105">Un oggetto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) archivia un'immagine nel formato del dispositivo di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="9d94b-105">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object stores an image in the format of the current display device.</span></span> <span data-ttu-id="9d94b-106">Il rendering di un'immagine archiviata in un oggetto **CachedBitmap** è veloce perché non viene impiegato alcun tempo di elaborazione per la conversione dell'immagine nel formato richiesto dal dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9d94b-106">Rendering an image stored in a **CachedBitmap** object is fast because no processing time is spent converting the image to the format required by the display device.</span></span>

<span data-ttu-id="9d94b-107">Nell'esempio seguente vengono creati un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e un oggetto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) dal file Texture.jpg.</span><span class="sxs-lookup"><span data-stu-id="9d94b-107">The following example creates a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object and a [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object from the file Texture.jpg.</span></span> <span data-ttu-id="9d94b-108">La **bitmap** e il **CachedBitmap** sono disegnati ogni 30.000 volte.</span><span class="sxs-lookup"><span data-stu-id="9d94b-108">The **Bitmap** and the **CachedBitmap** are each drawn 30,000 times.</span></span> <span data-ttu-id="9d94b-109">Se si esegue il codice, si noterà che le immagini **CachedBitmap** vengono disegnate notevolmente più velocemente delle immagini **bitmap** .</span><span class="sxs-lookup"><span data-stu-id="9d94b-109">If you run the code, you will see that the **CachedBitmap** images are drawn substantially faster than the **Bitmap** images.</span></span>


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
> <span data-ttu-id="9d94b-110">Un oggetto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) corrisponde al formato del dispositivo di visualizzazione nel momento in cui è stato creato l'oggetto **CachedBitmap** .</span><span class="sxs-lookup"><span data-stu-id="9d94b-110">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object matches the format of the display device at the time the **CachedBitmap** object was constructed.</span></span> <span data-ttu-id="9d94b-111">Se l'utente del programma modifica le impostazioni di visualizzazione, il codice deve costruire un nuovo oggetto **CachedBitmap** .</span><span class="sxs-lookup"><span data-stu-id="9d94b-111">If the user of your program changes the display settings, your code should construct a new **CachedBitmap** object.</span></span> <span data-ttu-id="9d94b-112">Il metodo **DrawImage** avrà esito negativo se si passa un oggetto **CachedBitmap** creato prima di una modifica nel formato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9d94b-112">The **DrawImage** method will fail if you pass it a **CachedBitmap** object that was created prior to a change in the display format.</span></span>

 

 

 



