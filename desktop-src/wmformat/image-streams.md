---
title: Immagine Flussi
description: Immagine Flussi
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows MEDIA Format SDK, flussi di immagini
- Advanced Systems Format (ASF), flussi di immagini
- ASF (Advanced Systems Format), flussi di immagini
- Windows MEDIA Format SDK, flussi
- Advanced Systems Format (ASF), flussi
- ASF (Advanced Systems Format), flussi
- flussi di immagini, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2067710e6b2be627bd16125d73e567a2f1ba1557ae01b81f55712d8c5a7b8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702865"
---
# <a name="image-streams"></a>Immagine Flussi

Un flusso di immagini è un tipo speciale di flusso che contiene immagini fisse assegnate agli orari di presentazione. Un'applicazione può visualizzare le immagini in un flusso di immagini in base alle esigenze, ma l'implementazione tipica è quella di visualizzare ogni immagine fino a quando non viene recapitata l'immagine successiva, ad esempio una presentazione. In genere, un flusso di immagini viene codificato in un file con un flusso audio per produrre una semplice presentazione di immagini sincronizzate con musica o voce.

I flussi di immagini sono simili ai flussi video in quanto vengono creati da esempi non compressi compressi come parte del processo di scrittura di file, ma sono anche simili a flussi arbitrari perché è necessario assegnare una frequenza in bit e una finestra del buffer appropriate al contenuto senza basarsi sulle proprietà assegnate dal codec.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Codice Flussi**](arbitrary-streams.md)
</dt> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**Audio e video Flussi**](audio-and-video-streams.md)
</dt> <dt>

[**Scrittura di immagini Flussi**](writing-image-streams.md)
</dt> </dl>

 

 




