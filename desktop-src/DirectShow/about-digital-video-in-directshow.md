---
description: Informazioni sui video digitali in DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Informazioni sui video digitali in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569259"
---
# <a name="about-digital-video-in-directshow"></a>Informazioni sui video digitali in DirectShow

Il video digitale (DV) può essere acquisito da una videocamera DV, archiviato in un file nel computer dell'utente o archiviato su nastro utilizzando un videoregistratore (video tape registrar). Pertanto, le operazioni che un'applicazione può eseguire su un flusso DV includono:

-   Acquisisci video live da una videocamera DV.
-   Trasmettere i dati DV dal nastro VTR al computer.
-   Trasmettere i dati DV dal computer al VTR.
-   Leggere i dati DV da un file.
-   Scrive i dati DV in un file.
-   Eseguire il rendering dell'audio e del video in un flusso DV.

DirectShow fornisce i filtri DV seguenti:

-   [Driver Msdv](msdv-driver.md). Il driver MSDV controlla un dispositivo DV, ad esempio una videocamera. Il dispositivo può avere una sottounità della fotocamera e un'unità secondaria VTR; MSDV controlla entrambe le sottounità. Il driver MSDV viene visualizzato come filtro DirectShow per le applicazioni.
-   Filtro [barra di divisione DV](dv-splitter-filter.md) . I frame DV contengono audio e video nello stesso frame. Il filtro Splitter DV estrae i dati audio e li restituisce come uno o due flussi audio. Restituisce i dati originali come flusso video DV separato.
-   Filtro [decodificatore video DV](dv-video-decoder-filter.md) . Decodifica il video DV in un video non compresso.
-   Filtro [codificatore video DV](dv-video-encoder-filter.md) . Codifica il video non compresso in un video con codifica DV.
-   [Muxer DV](dv-muxer-filter.md). Combina un flusso video DV con uno o due flussi audio, per creare un singolo flusso DV con interfoliazione.

La barra di divisione DV e il decodificatore video DV interagiscono. Il separatore acquisisce il flusso con interfoliazione e genera flussi video audio e DV distinti. Il decodificatore converte il video DV in un video non compresso. Questo processo è illustrato nella figura seguente.

![Splitter DV e decoder DV](images/dv-filters1.png)

Il codificatore video DV e il muxer DV invertino il processo: il codificatore converte il video non compresso in video DV e Mux combina audio e video DV per creare un singolo flusso Interleaved, come illustrato nel diagramma seguente.

![codificatore DV e muxer DV](images/dv-filters2.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



