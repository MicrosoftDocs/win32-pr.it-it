---
description: Quando si usa Windows GDI+ per disegnare una linea, si specificano il punto iniziale e il punto finale della linea, ma non è necessario fornire informazioni sui singoli pixel sulla linea.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Anti-aliasing con linee e curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6fd1df9c8dca6bb600c723fa61cf14b99e53a51670768a7323ca33e12b9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117697110"
---
# <a name="antialiasing-with-lines-and-curves"></a>Anti-aliasing con linee e curve

Quando si usa Windows GDI+ per disegnare una linea, si specificano il punto iniziale e il punto finale della linea, ma non è necessario fornire informazioni sui singoli pixel sulla linea. GDI+ funziona in combinazione con il software del driver di visualizzazione per determinare quali pixel verranno attivati per visualizzare la riga in un particolare dispositivo di visualizzazione.

Si consideri una linea rossa retta che va dal punto (4, 2) al punto (16, 10). Si supponga che il sistema di coordinate abbia l'origine nell'angolo superiore sinistro e che l'unità di misura sia il pixel. Si supponga anche che l'asse x punti verso destra e che l'asse y punti verso il basso. La figura seguente mostra una visualizzazione ingrandita della linea rossa disegnata su uno sfondo multicolore.

![Illustrazione che mostra pixel rossi a tinta unita su uno sfondo multicolore](images/aboutgdip02-art33.png)

Si noti che i pixel rossi usati per eseguire il rendering della linea sono opachi. Non sono presenti pixel parzialmente trasparenti coinvolti nella visualizzazione della linea. Questo tipo di rendering delle linee offre alla linea un aspetto frastagliato e la linea ha un aspetto leggermente simile a una barra verticale. Questa tecnica di rappresentazione di una linea con una scala è detta aliasing. la scala è un alias per la linea teorica.

Una tecnica più sofisticata per il rendering di una linea prevede l'uso di pixel parzialmente trasparenti insieme ai pixel rossi puri. I pixel sono impostati sul rosso puro o su una sfumatura di rosso e sul colore di sfondo a seconda della vicinanza alla linea. Questo tipo di rendering è detto antialiasing e determina una linea che l'occhio umano considera più uniforme. La figura seguente mostra come determinati pixel vengono uniti allo sfondo per produrre una linea antialias.

![Illustrazione che mostra i pixel con sfumature di rosso sullo stesso sfondo](images/aboutgdip02-art34.png)

L'antialiasing (smoothing) può essere applicato anche alle curve. La figura seguente mostra una visualizzazione ingrandita di un'ellisse smussata.

![illustrazione di un ellisse costituito da diverse sfumature di pixel blu su uno sfondo bianco](images/aboutgdip02-art35.png)

La figura seguente mostra la stessa ellisse nelle dimensioni effettive, una volta senza antialiasing e una volta con l'antialiasing.

![Screenshot di due puntini di sospensione: quello con antialiasing risulta notevolmente più uniforme](images/aboutgdip02-art36.png)

Per disegnare linee e curve che usano l'antialiasing, creare un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passare *SmoothingModeAntiAlias* al relativo [**metodo Graphics::SetSmoothingMode.**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) Chiamare quindi uno dei metodi di disegno dello stesso **oggetto Graphics.**


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



**SmoothingModeAntiAlias** è un elemento [**dell'enumerazione SmoothingMode.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)

 

 



