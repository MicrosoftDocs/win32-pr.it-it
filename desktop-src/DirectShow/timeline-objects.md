---
description: Oggetti Sequenza temporale
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Oggetti Sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbcf3496770dee7664e08ffabe6537356c7b37ad13abee1dce149698748745e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072305"
---
# <a name="timeline-objects"></a>Oggetti Sequenza temporale

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Ogni tipo di oggetto nella sequenza temporale, ovvero origine, traccia, effetto e così via, è un oggetto COM distinto. Tuttavia, un'applicazione non li crea usando la **funzione CoCreateInstance.** Chiama invece il [**metodo IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md) Questo metodo crea un oggetto del tipo richiesto, lo inizializza e restituisce un puntatore all'oggetto . Per informazioni dettagliate, vedere [Costruzione di una sequenza temporale.](constructing-a-timeline.md)

Ogni oggetto sequenza temporale espone [**l'interfaccia IAMTimelineObj.**](iamtimelineobj.md) Inoltre, i vari tipi di oggetto supportano le proprie interfacce specializzate:

-   Origine: [ **IAMTimelineSrc**](iamtimelinesrc.md)
-   Traccia: [ **IAMTimelineTrack**](iamtimelinetrack.md)
-   Composizione: [ **IAMTimelineComp**](iamtimelinecomp.md)
-   Gruppo: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)
-   Effetto: [ **IAMTimelineEffect**](iamtimelineeffect.md)
-   Transizione: [ **IAMTimelineTrans**](iamtimelinetrans.md)

Si noti che i gruppi sono un tipo di composizione, quindi supportano [**IAMTimelineComp**](iamtimelinecomp.md)e la propria [**interfaccia IAMTimelineGroup.**](iamtimelinegroup.md)

Oltre alle interfacce elencate in precedenza, gli oggetti sequenza temporale espongono altre interfacce secondarie. Queste interfacce determinano le relazioni tra i tipi di oggetto.



| Interfaccia                                                  | Significato                                                                                                       | Esposto da                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | L'oggetto è una traccia virtuale. Le tracce virtuali possono risiedere all'interno delle composizione e contenere altri oggetti della sequenza temporale. | Composizione, traccia                |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | L'oggetto può avere effetti.                                                                                  | Composition, Track, Source        |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | L'oggetto può avere transizioni.                                                                              | Composizione, traccia                |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | L'oggetto può essere suddiviso in due oggetti .                                                                     | Track, Source, Effect, Transition |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dei componenti della sequenza temporale](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



