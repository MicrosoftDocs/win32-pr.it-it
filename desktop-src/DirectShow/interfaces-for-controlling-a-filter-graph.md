---
description: Interfacce per il controllo di un grafico di filtro
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Interfacce per il controllo di un grafico di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747106"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a>Interfacce per il controllo di un grafico di filtro

Queste interfacce forniscono metodi per il controllo di un grafico di filtro.



| Interfaccia                                  | Descrizione                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | Modificare il clock del grafico.                                                                                   |
| [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | Sincronizzare i flussi live in un grafico di filtro.                                                               |
| [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | Catene di controllo dei filtri.                                                                                |
| [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)     | Eseguire, sospendere e arrestare il grafico del filtro. Fornisce anche metodi compatibili con l'automazione per la creazione di grafici. |
| [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)     | Rispondere agli eventi nel grafico.                                                                           |
| [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | Ricerca all'interno di un file.                                                                                       |
| [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)     | Accodare i comandi da eseguire in un secondo momento.                                                                    |
| [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | Frame-Step in un flusso video.                                                                        |



 

 

 



