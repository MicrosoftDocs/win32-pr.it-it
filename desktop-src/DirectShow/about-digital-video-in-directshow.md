---
description: Informazioni sul video digitale in DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Informazioni sul video digitale in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061927618c1cb3340e0771376a7a1e232e078e043a554829f99580262ea29c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664815"
---
# <a name="about-digital-video-in-directshow"></a>Informazioni sul video digitale in DirectShow

I video digitali (DV) possono essere acquisiti da una videocamera DV, archiviati in un file nel computer dell'utente o archiviati su nastro usando un registratore video. Di conseguenza, le operazioni che un'applicazione potrebbe eseguire su un flusso DV includono:

-   Acquisire video live da una fotocamera DV.
-   Trasmettere i dati DV dal nastro VTR al computer.
-   Trasmettere i dati DV dal computer alla VTR.
-   Legge i dati DV da un file.
-   Scrivere dati DV in un file.
-   Eseguire il rendering di audio e video in un flusso DV.

DirectShow fornisce i filtri DV seguenti:

-   [Driver MSDV](msdv-driver.md). Il driver MSDV controlla un dispositivo DV, ad esempio un videocamere. Il dispositivo può avere una sottounità della fotocamera e una sottounità VTR; MSDV controlla entrambe le sottounità. Il driver MSDV viene visualizzato nelle applicazioni come DirectShow filtro.
-   [Filtro DV Splitter.](dv-splitter-filter.md) I fotogrammi DV contengono audio e video nello stesso fotogramma. Il filtro DV Splitter estrae i dati audio e restituisce i dati come uno o due flussi audio. Restituisce i dati originali come flusso video DV separato.
-   [Filtro decodificatore video DV.](dv-video-decoder-filter.md) Decodifica il video DV in un video non compresso.
-   [Filtro del codificatore video DV.](dv-video-encoder-filter.md) Codifica video non compresso in video con codifica DV.
-   [DV Muxer](dv-muxer-filter.md). Combina un flusso video DV con uno o due flussi audio per creare un singolo flusso DV interleaved.

Lo splitter DV e il decodificatore video DV funzionano insieme. La barra di divisione accetta il flusso interleaved e restituisce flussi video audio e DV separati. Il decodificatore converte il video DV in video non compresso. L'immagine seguente illustra questo processo.

![Separatore dv e decodificatore dv](images/dv-filters1.png)

DV Video Encoder e DV Muxer invertono il processo: il codificatore converte i video non compressi in video DV e il mux combina audio e video DV per creare un singolo flusso interleaved, come illustrato nel diagramma seguente.

![Codificatore dv e muxer dv](images/dv-filters2.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



