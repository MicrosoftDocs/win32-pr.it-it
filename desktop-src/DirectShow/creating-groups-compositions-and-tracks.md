---
description: Creazione di composizioni e tracce di gruppi
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Creazione di composizioni e tracce di gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103877025"
---
# <a name="creating-groups-compositions-and-tracks"></a>Creazione di composizioni e tracce di gruppi

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Gruppi, composizioni e tracce sono i livelli intermedi tra la sequenza temporale e i clip di origine. Sono distinti dal tipo di oggetto che possono contenere.

-   Le tracce contengono oggetti di origine.
-   Le composizioni contengono tracce e altre composizioni, ma non oggetti di origine.
-   I gruppi sono composizioni di primo livello. I gruppi contengono composizioni e tracce, ma le composizioni non possono contenere gruppi.
-   Una *traccia virtuale* è qualsiasi oggetto che può risiedere all'interno di una composizione o di un gruppo. Sono incluse le tracce e le composizioni.

Questi oggetti espongono le interfacce seguenti:



| Interfaccia                                                  | Esposto da           |
|------------------------------------------------------------|----------------------|
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Brani               |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Tracce, composizioni |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Composizioni, gruppi |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Gruppi               |



 

Queste interfacce contengono i metodi per l'aggiunta di oggetti alla sequenza temporale.

-   [**IAMTimeline:: addgroup**](iamtimeline-addgroup.md): inserisce un gruppo nella sequenza temporale.
-   [**IAMTimelineComp:: VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): inserisce una traccia virtuale in una composizione o un gruppo.
-   [**IAMTimelineTrack:: SrcAdd**](iamtimelinetrack-srcadd.md): inserisce un'origine in una traccia.

Il codice seguente, ad esempio, inserisce una nuova traccia in un gruppo. Come illustrato nella tabella precedente, un gruppo è considerato un tipo di composizione e una traccia è un tipo di traccia virtuale. Pertanto, per inserire la traccia nel gruppo, è necessario eseguire una query sul gruppo per la relativa interfaccia **IAMTimelineComp** e chiamare il metodo **IAMTimelineComp:: VTrackInsBefore** .


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



Il secondo parametro di **VTrackInsBefore** specifica la priorità della traccia virtuale. I livelli di priorità iniziano da zero. Se si specifica il valore-1, la traccia virtuale viene inserita alla fine dell'elenco di priorità. Se si specifica un valore in cui è già presente una traccia virtuale, tutti gli elementi da quel punto in poi spostano verso il basso l'elenco in base a un livello di priorità. Non inserire una traccia virtuale con una priorità maggiore del numero di tracce virtuali, perché provocherà un comportamento non definito.

Per eliminare un oggetto in modo permanente dalla sequenza temporale, chiamare [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md) sull'oggetto. Questo metodo rimuove l'oggetto e tutti i relativi elementi figlio. Per rimuovere un oggetto per inserirlo in un'altra posizione nella sequenza temporale, chiamare invece [**IAMTimelineObj:: Remove**](iamtimelineobj-remove.md) . Diversamente da **RemoveAll**, questo metodo non elimina gli elementi figlio dell'oggetto. Per rimuovere tutti gli elementi dalla sequenza temporale, chiamare [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 



