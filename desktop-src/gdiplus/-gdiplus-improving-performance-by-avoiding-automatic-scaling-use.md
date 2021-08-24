---
description: Se si passa solo l'angolo superiore sinistro di un'immagine al metodo DrawImage, Windows GDI+ ridimensionare l'immagine, con una riduzione delle prestazioni.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Miglioramento delle prestazioni evitando il ridimensionamento automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac74fbf636f3f1cbdf088939ad76732907c15228e66662a7246b3f0c0313c8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778731"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a>Miglioramento delle prestazioni evitando il ridimensionamento automatico

Se si passa solo l'angolo superiore sinistro di un'immagine al metodo **DrawImage,** Windows GDI+ ridimensionare l'immagine, con una riduzione delle prestazioni.

La chiamata seguente al **metodo DrawImage** specifica un angolo superiore sinistro (50, 30) ma non specifica un rettangolo di destinazione:


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



Anche se questa è la versione più semplice del **metodo DrawImage** in termini di numero di argomenti obbligatori, non è necessariamente la più efficiente. Se il numero di punti per pollice nel dispositivo di visualizzazione corrente è diverso dal numero di punti per pollice nel dispositivo in cui è stata creata l'immagine, GDI+ ridimensiona l'immagine in modo che le dimensioni fisiche nel dispositivo di visualizzazione corrente si avvicinano il più possibile alle dimensioni fisiche del dispositivo in cui è stata creata.

Se si vuole impedire tale ridimensionamento, passare la larghezza e l'altezza di un rettangolo di destinazione al **metodo DrawImage.** Nell'esempio seguente viene disegnata la stessa immagine due volte. Nel primo caso, la larghezza e l'altezza del rettangolo di destinazione non vengono specificate e l'immagine viene ridimensionata automaticamente. Nel secondo caso, la larghezza e l'altezza (misurate in pixel) del rettangolo di destinazione sono specificate come la larghezza e l'altezza dell'immagine originale.


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



La figura seguente mostra l'immagine sottoposta a rendering due volte.

![Screenshot di una finestra che contiene due versioni di un'immagine con scale diverse](images/scaledtexture1.png)

 

 



