---
title: Flussi di immagini
description: Flussi di immagini
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows Media Format SDK, flussi di immagini
- Formati di sistemi avanzati (ASF), flussi di immagini
- ASF (formato avanzato dei sistemi), flussi di immagini
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- flussi di immagini, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331607"
---
# <a name="image-streams"></a>Flussi di immagini

Un flusso di immagini è un tipo speciale di flusso che contiene ancora le immagini assegnate ai tempi di presentazione. Un'applicazione può visualizzare le immagini in un flusso di immagini come desiderato, ma l'implementazione tipica consiste nel visualizzare ogni immagine fino a quando non viene recapitata l'immagine successiva, ad esempio una presentazione. In genere, un flusso di immagini è codificato in un file con un flusso audio per produrre una semplice presentazione di immagini sincronizzate con musica o sintesi vocale.

I flussi di immagini sono simili ai flussi video in quanto vengono creati da campioni non compressi compressi come parte del processo di scrittura di file, ma sono simili anche a flussi arbitrari perché è necessario assegnare una velocità in bit e una finestra del buffer appropriata per il contenuto senza basarsi sulle proprietà assegnate dal codec.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Flussi arbitrari**](arbitrary-streams.md)
</dt> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Flussi audio e video**](audio-and-video-streams.md)
</dt> <dt>

[**Scrittura di flussi di immagini**](writing-image-streams.md)
</dt> </dl>

 

 




