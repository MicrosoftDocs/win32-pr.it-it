---
description: Se si passa solo l'angolo superiore sinistro di un'immagine al metodo DrawImage, Windows GDI+ potrebbe ridimensionare l'immagine, riducendo le prestazioni.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Miglioramento delle prestazioni evitando il ridimensionamento automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979007"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a>Miglioramento delle prestazioni evitando il ridimensionamento automatico

Se si passa solo l'angolo superiore sinistro di un'immagine al metodo **DrawImage** , Windows GDI+ potrebbe ridimensionare l'immagine, riducendo le prestazioni.

La chiamata seguente al metodo **DrawImage** specifica un angolo superiore sinistro di (50, 30) ma non specifica un rettangolo di destinazione:


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



Sebbene si tratta della versione più semplice del metodo **DrawImage** in termini di numero di argomenti obbligatori, non è necessariamente il più efficiente. Se il numero di punti per pollice sul dispositivo di visualizzazione corrente è diverso dal numero di punti per pollice sul dispositivo in cui è stata creata l'immagine, GDI+ ridimensiona l'immagine in modo che le dimensioni fisiche sul dispositivo di visualizzazione corrente siano il più vicino possibile alle dimensioni fisiche del dispositivo in cui è stato creato.

Se si desidera impedire tale scalabilità, passare la larghezza e l'altezza di un rettangolo di destinazione al metodo **DrawImage** . Nell'esempio seguente viene disegnata due volte la stessa immagine. Nel primo caso, la larghezza e l'altezza del rettangolo di destinazione non sono specificate e l'immagine viene ridimensionata automaticamente. Nel secondo caso, la larghezza e l'altezza (misurate in pixel) del rettangolo di destinazione vengono specificate come la larghezza e l'altezza dell'immagine originale.


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



La figura seguente mostra il rendering dell'immagine due volte.

![Screenshot di una finestra che contiene due versioni di un'immagine a scale diverse](images/scaledtexture1.png)

 

 



