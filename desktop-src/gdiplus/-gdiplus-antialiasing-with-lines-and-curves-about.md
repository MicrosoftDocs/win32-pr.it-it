---
description: Quando si utilizza Windows GDI+ per creare una linea, si specifica il punto iniziale e il punto finale della linea, ma non è necessario fornire informazioni sui singoli pixel della riga.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Anti-aliasing con linee e curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c817d3e11b4699c9fc892b41dcc827c0861f192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755775"
---
# <a name="antialiasing-with-lines-and-curves"></a>Anti-aliasing con linee e curve

Quando si utilizza Windows GDI+ per creare una linea, si specifica il punto iniziale e il punto finale della linea, ma non è necessario fornire informazioni sui singoli pixel della riga. GDI+ funziona insieme al software per i driver di visualizzazione per determinare quali pixel verranno accesi per visualizzare la riga in un particolare dispositivo di visualizzazione.

Prendere in considerazione una linea rossa diritta che va dal punto (4, 2) al punto (16, 10). Si supponga che il sistema di coordinate abbia l'origine nell'angolo superiore sinistro e che l'unità di misura sia il pixel. Si supponga inoltre che l'asse x punti a destra e che l'asse y punti verso il basso. Nella figura seguente viene illustrata una vista ingrandita della linea rossa disegnata su uno sfondo a più colori.

![illustrazione che mostra i pixel rossi a tinta unita su uno sfondo multicolore](images/aboutgdip02-art33.png)

Si noti che i pixel rossi utilizzati per il rendering della linea sono opachi. Non sono presenti pixel parzialmente trasparenti per la visualizzazione della riga. Questo tipo di rendering della linea fornisce un aspetto irregolare alla riga e la linea appare come una scalinata. Questa tecnica di rappresentazione di una linea con una scala è detta aliasing; la scala è un alias per la linea teorica.

Una tecnica più sofisticata per il rendering di una linea prevede l'uso di pixel parzialmente trasparenti insieme ai pixel rossi puri. I pixel sono impostati su rosso puro o su una combinazione di rosso e il colore di sfondo, a seconda della distanza con cui si trovano nella riga. Questo tipo di rendering è denominato anti-aliasing e produce una linea che l'occhio umano percepisce come più uniforme. Nella figura seguente viene illustrato il modo in cui alcuni pixel vengono combinati con lo sfondo per produrre una riga con antialiasing.

![illustrazione che mostra i pixel con sfumature di rosso sullo stesso sfondo](images/aboutgdip02-art34.png)

L'anti-aliasing (smussamento) può essere applicato anche alle curve. La figura seguente mostra una visualizzazione ingrandita di un'ellisse smussata.

![illustrazione di un'ellisse composta da diverse sfumature di pixel blu su uno sfondo bianco](images/aboutgdip02-art35.png)

La figura seguente mostra la stessa ellisse nelle dimensioni effettive, una volta senza anti-aliasing e una volta con l'anti-aliasing.

![Screenshot di due puntini di sospensione: quello con anti-aliasing appare più semplice](images/aboutgdip02-art36.png)

Per creare linee e curve che usano l'anti-aliasing, creare un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passare *SmoothingModeAntiAlias* al relativo metodo [**Graphics:: SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) . Quindi, chiamare uno dei metodi di disegno dello stesso oggetto **Graphics** .


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



**SmoothingModeAntiAlias** è un elemento dell'enumerazione [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) .

 

 



