---
description: Oggetti Timeline
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Oggetti Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319541"
---
# <a name="timeline-objects"></a>Oggetti Timeline

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Ogni tipo di oggetto nella sequenza temporale, ovvero origine, traccia, effetto e così via, è un oggetto COM distinto. Tuttavia, un'applicazione non li crea utilizzando la funzione **CoCreateInstance** . Chiama invece il metodo [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) . Questo metodo crea un oggetto del tipo richiesto, lo inizializza e restituisce un puntatore all'oggetto. Per informazioni dettagliate, vedere [creazione di una sequenza temporale](constructing-a-timeline.md).

Ogni oggetto sequenza temporale espone l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) . Inoltre, i vari tipi di oggetto supportano le proprie interfacce specializzate:

-   Origine: [ **IAMTimelineSrc**](iamtimelinesrc.md)
-   Traccia: [ **IAMTimelineTrack**](iamtimelinetrack.md)
-   Composizione: [ **IAMTimelineComp**](iamtimelinecomp.md)
-   Gruppo: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)
-   Effetto: [ **IAMTimelineEffect**](iamtimelineeffect.md)
-   Transizione: [ **IAMTimelineTrans**](iamtimelinetrans.md)

Si noti che i gruppi sono un tipo di composizione, quindi supportano [**IAMTimelineComp**](iamtimelinecomp.md), nonché la propria interfaccia [**IAMTimelineGroup**](iamtimelinegroup.md) .

Oltre alle interfacce elencate in precedenza, gli oggetti sequenza temporale espongono altre interfacce secondarie. Queste interfacce determinano le relazioni tra i tipi di oggetto.



| Interfaccia                                                  | Significato                                                                                                       | Esposto da                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | L'oggetto è una traccia virtuale. Le tracce virtuali possono risiedere all'interno di composizioni e tenere altri oggetti della sequenza temporale. | Composizione, traccia                |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | L'oggetto può avere effetti.                                                                                  | Composizione, traccia, origine        |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | L'oggetto può avere transizioni.                                                                              | Composizione, traccia                |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | L'oggetto può essere suddiviso in due oggetti.                                                                     | Track, source, Effect, Transition |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dei componenti della sequenza temporale](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



