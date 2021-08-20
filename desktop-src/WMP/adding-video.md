---
title: Aggiunta di video
description: Aggiunta di video
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- creazione di interfaccia, video
- Windows Media Player, video
- skins, video
- video nelle interfaccia, aggiunta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099778395146cb0bf0f27b483d55dd75c0fb8a0b28b879cc2d388f8e8cb7ba75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055409"
---
# <a name="adding-video"></a>Aggiunta di video

È possibile aggiungere un video al file semplicemente usando **l'elemento VIDEO** e definendo il punto in cui si vuole inserire la finestra video.

Usare lo stesso codice della sezione Scelta dei file. È necessario solo aggiungere **l'elemento VIDEO** con gli attributi top, left, width e height.


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



Quindi, quando si riproduce un video, questo verrà visualizzato nella finestra. L'immagine per l'esempio video è stata modificata per creare un'interfaccia leggermente più grande. Poiché i livelli sono stati usati in Photoshop, i pulsanti sono stati spostati facilmente e un nuovo set è stato creato molto rapidamente. È stata modificata solo l'immagine di sfondo. È stato usato un riempimento in un livello vuoto ed è stato aggiunto un effetto smussato e rilievo.

È possibile visualizzare un'interfaccia video funzionante simile nella sezione di esempio dell'SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




