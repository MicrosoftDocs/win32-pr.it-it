---
title: Aggiunta di video
description: Aggiunta di video
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- creazione di interfacce, video
- Windows Media Player Skins, video
- interfacce, video
- video in interfacce, aggiunta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298221"
---
# <a name="adding-video"></a>Aggiunta di video

È possibile aggiungere un video al file semplicemente usando l'elemento **video** e definendo la posizione in cui si vuole inserire la finestra video.

Usare lo stesso codice riportato nella sezione scelta dei file; è sufficiente aggiungere l'elemento **video** con gli attributi top, Left, Width e Height.


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



Quando si riproduce un video, questo verrà visualizzato nella finestra. L'immagine per l'esempio video è stata modificata per creare un'interfaccia leggermente più ampia. Poiché i livelli sono stati usati in Photoshop, i pulsanti sono stati spostati in modo semplice e un nuovo set è stato creato molto rapidamente. Solo l'immagine di sfondo è stata modificata. Un riempimento è stato usato in un livello vuoto ed è stato aggiunto un effetto smussato e rilievo.

Nella sezione di esempio dell'SDK è possibile visualizzare una simile interfaccia video funzionante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




