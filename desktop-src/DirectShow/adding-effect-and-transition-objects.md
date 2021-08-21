---
description: Aggiunta di oggetti Effect e Transition
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Aggiunta di oggetti Effect e Transition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929678759d55a51b022cd7b870ddfa7cc5abb72279bcabe1694b5cc4eef211b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160062"
---
# <a name="adding-effect-and-transition-objects"></a>Aggiunta di oggetti Effect e Transition

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

In DES un effetto o una transizione è rappresentato con due oggetti:

-   Un *oggetto sequenza temporale rappresenta* l'effetto o la transizione all'interno della sequenza temporale. Per gli effetti, l'oggetto sequenza temporale supporta [**l'interfaccia IAMTimelineEffect.**](iamtimelineeffect.md) Per le transizioni, supporta [**l'interfaccia IAMTimelineTrans.**](iamtimelinetrans.md) Entrambi i tipi supportano [**l'interfaccia IAMTimelineObj.**](iamtimelineobj.md)
-   Il *sottooggetto* è un oggetto che implementa l'elaborazione dati per l'effetto o la transizione. L'oggetto sequenza temporale contiene un puntatore al sottooggetto.

Per aggiungere un effetto o una transizione, seguire questa procedura.

**1. Creare l'oggetto Sequenza temporale**

Per creare l'oggetto sequenza temporale, chiamare [**il metodo IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md) Impostare il tipo su **TIMELINE MAJOR TYPE EFFECT \_ \_ \_ per** un effetto oppure **su TIMELINE MAJOR TYPE \_ \_ \_ TRANSITION** per una transizione.

L'esempio seguente crea un oggetto transition:


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



**2. Specificare il subobject**

L'oggetto sequenza temporale funge da wrapper per un altro oggetto, denominato *oggetto secondario*, che esegue il lavoro reale. Il sottooggetto implementa una trasformazione dei dati che produce l'effetto o la transizione desiderata. Per un elenco di transizioni ed effetti forniti con DES, vedere [Transizioni ed effetti.](transitions-and-effects.md)

Per impostare il sottooggetto, chiamare il metodo [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) sull'oggetto sequenza temporale, passando l'identificatore di classe (CLSID) del sottooggetto. DirectShow fornisce un enumeratore per gli effetti video e le transizioni video, che è possibile usare per ottenere il CLSID. Per altre informazioni, vedere [Enumerazione di effetti e transizioni.](enumerating-effects-and-transitions.md)

L'esempio seguente imposta la [transizione di cancellazione SMPTE](smpte-wipe-transition.md) come oggetto secondario :


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



**3. Impostare l'ora di inizio e di arresto**

Per impostare l'ora di inizio e di arresto, chiamare il [**metodo IAMTimelineObj::SetStartStop.**](iamtimelineobj-setstartstop.md) Questi orari sono relativi all'ora di inizio dell'oggetto padre. Gli effetti possono sovrapporsi all'interno dello stesso oggetto, ma le transizioni non possono.

L'esempio seguente imposta l'ora di inizio su 5 secondi e l'ora di arresto su 10 secondi:


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



Quando viene eseguito il rendering di una transizione, lo stato di avanzamento della transizione in ogni frame viene calcolato in base a una proprietà **Progress,** normalizzata in un intervallo compreso tra 0,0 e 1,0. DES usa l'ora di inizio di ogni fotogramma per calcolare il valore di avanzamento. Ciò significa che se l'ora di arresto  della transizione è uguale all'ora di arresto di origine, il valore progress non raggiungerà mai esattamente 1,0, perché l'ora di inizio dell'ultimo fotogramma è leggermente diversa dall'ora di arresto. Per fare in modo che la transizione raggiunga la versione 1.0, impostare l'ora di arresto della transizione su almeno un fotogramma precedente all'ora di arresto di origine.

**4. Inserire l'oggetto nella sequenza temporale**

Per inserire l'oggetto nella sequenza temporale, chiamare uno dei metodi seguenti sull'elemento padre, a seconda del tipo di oggetto:

-   Effetti: [ **IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)
-   Transizioni: [ **IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)

Nel metodo [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) è necessario specificare la priorità dell'effetto. Quando gli effetti si sovrappongono allo stesso oggetto, vengono applicati in ordine di priorità. L'effetto audio Volume Envelope è un'eccezione. Per informazioni [dettagliate,](volume-envelope-effect.md) vedere le informazioni di riferimento sull'effetto volume envelope. All'interno di una composizione, tutte le tracce audio vengono miste prima dell'applicazione degli effetti audio per tale composizione.

Poiché le transizioni non possono sovrapporsi allo stesso oggetto, non hanno un valore di priorità.

L'esempio seguente aggiunge l'oggetto transizione a una traccia:


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



L'esempio esegue una query sull'oggetto track [**per l'interfaccia IAMTimelineTransable**](iamtimelinetransable.md) prima di chiamare AddTrans.

**5. Impostare le proprietà**

Molti effetti e transizioni supportano proprietà personalizzate. Per informazioni, vedere [Impostazione delle proprietà su effetti e transizioni.](setting-properties-on-effects-and-transitions.md)

Esempio

L'esempio di codice seguente aggiunge una [transizione di cancellazione SMPTE](smpte-wipe-transition.md) a una traccia. Presuppone che l'oggetto traccia esista già nella sequenza temporale.


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di effetti e transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



