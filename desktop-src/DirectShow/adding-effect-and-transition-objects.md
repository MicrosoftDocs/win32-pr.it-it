---
description: Aggiunta di oggetti Effect e Transition
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Aggiunta di oggetti Effect e Transition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048948"
---
# <a name="adding-effect-and-transition-objects"></a>Aggiunta di oggetti Effect e Transition

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

In DES un effetto o una transizione viene rappresentato con due oggetti:

-   Un *oggetto Timeline* rappresenta l'effetto o la transizione all'interno della sequenza temporale. Per gli effetti, l'oggetto Timeline supporta l'interfaccia [**IAMTimelineEffect**](iamtimelineeffect.md) . Per le transizioni, supporta l'interfaccia [**IAMTimelineTrans**](iamtimelinetrans.md) . Entrambi i tipi supportano l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) .
-   Il *sottooggetto* è un oggetto che implementa l'elaborazione dei dati per l'effetto o la transizione. L'oggetto sequenza temporale include un puntatore all'oggetto SubObject.

Per aggiungere un effetto o una transizione, seguire questa procedura.

**1. creare l'oggetto sequenza temporale**

Per creare l'oggetto sequenza temporale, chiamare il metodo [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) . Impostare il tipo su un **\_ effetto del \_ tipo \_ principale della sequenza temporale** per un effetto o una **\_ \_ \_ transizione di tipo principale della sequenza temporale** per una transizione.

Nell'esempio seguente viene creato un oggetto di transizione:


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



**2. specificare l'oggetto SubObject**

L'oggetto sequenza temporale funge da wrapper per un altro oggetto, denominato *sottooggetto*, che esegue le operazioni effettive. L'oggetto SubObject implementa una trasformazione dei dati che produce l'effetto o la transizione desiderata. Per un elenco delle transizioni e degli effetti forniti con DES, vedere [transizioni ed effetti](transitions-and-effects.md).

Per impostare il sottooggetto, chiamare il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) sull'oggetto Timeline, passandogli l'identificatore di classe (CLSID) dell'oggetto SubObject. DirectShow fornisce un enumeratore per gli effetti video e le transizioni video, che è possibile usare per ottenere il CLSID. Per ulteriori informazioni, vedere [enumerazione degli effetti e delle transizioni](enumerating-effects-and-transitions.md).

Nell'esempio seguente viene impostata la [transizione di cancellazione SMPTE](smpte-wipe-transition.md) come oggetto SubObject:


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



**3. impostare l'ora di inizio e di fine**

Per impostare l'ora di inizio e di fine, chiamare il metodo [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) . Questi orari sono relativi all'ora di inizio dell'oggetto padre. Gli effetti possono sovrapporsi all'interno dello stesso oggetto, ma le transizioni non possono.

L'esempio seguente imposta l'ora di inizio su 5 secondi e l'ora di arresto su 10 secondi:


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



Quando viene eseguito il rendering di una transizione, lo stato di avanzamento della transizione in ogni frame viene calcolato in base a una proprietà **Progress** , che viene normalizzata in un intervallo compreso tra 0,0 e 1,0. DES usa l'ora di inizio di ogni frame per calcolare il valore di avanzamento. Ciò significa che se l'ora di arresto della transizione è uguale all'ora di arresto dell'origine, il valore di **avanzamento** non raggiungerà mai esattamente 1,0, perché l'ora di inizio dell'ultimo frame è leggermente diversa dall'ora di arresto. Per raggiungere il 1,0 della transizione, impostare l'ora di arresto della transizione su almeno un frame prima dell'ora di arresto dell'origine.

**4. Inserire l'oggetto nella sequenza temporale**

Per inserire l'oggetto nella sequenza temporale, chiamare uno dei metodi seguenti sull'elemento padre, a seconda del tipo di oggetto:

-   Effetti: [ **IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)
-   Transizioni: [ **IAMTimelineTransable:: TransAdd**](iamtimelinetransable-transadd.md)

Nel metodo [**IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) è necessario specificare la priorità dell'effetto. Quando gli effetti si sovrappongono allo stesso oggetto, vengono applicati in ordine di priorità. L'effetto audio della busta del volume è un'eccezione. per informazioni dettagliate, vedere la Guida di riferimento all' [effetto envelope del volume](volume-envelope-effect.md) . All'interno di una composizione, tutte le tracce audio vengono combinate prima che vengano applicati gli effetti audio per tale composizione.

Poiché le transizioni non possono sovrapporsi allo stesso oggetto, non hanno un valore di priorità.

Nell'esempio seguente l'oggetto Transition viene aggiunto a una traccia:


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



Nell'esempio viene eseguita una query sull'oggetto Track per l'interfaccia [**IAMTimelineTransable**](iamtimelinetransable.md) prima di chiamare AddTrans.

**5. impostare le proprietà**

Molti effetti e transizioni supportano proprietà personalizzate. Per informazioni, vedere [impostazione delle proprietà per gli effetti e le transizioni](setting-properties-on-effects-and-transitions.md).

Esempio

Nell'esempio di codice seguente viene aggiunta una [transizione di cancellazione SMPTE](smpte-wipe-transition.md) a una traccia. Si presuppone che l'oggetto Track esista già nella sequenza temporale.


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

[Utilizzo degli effetti e delle transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



