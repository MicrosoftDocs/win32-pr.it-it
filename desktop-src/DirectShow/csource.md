---
description: La classe CSource è una classe di base per l'implementazione di filtri di origine. Un filtro derivato da CSource contiene uno o più pin di output derivati dalla classe CSourceStream. Ogni pin di output crea un thread di lavoro che esegue il push di campioni multimediali a valle.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Classe CSource (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6708ce38c826aae9ccb40d077972d267a20d5e22b4f67157000c4a62e92afa1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687516"
---
# <a name="csource-class"></a>Classe CSource

![Gerarchia di classi csource](images/source01.png)

La **classe CSource** è una classe di base per l'implementazione di filtri di origine. Un filtro derivato **da CSource** contiene uno o più pin di output derivati dalla [**classe CSourceStream.**](csourcestream.md) Ogni pin di output crea un thread di lavoro che esegue il push di campioni multimediali a valle.

> [!Note]  
> La **classe CSource** è progettata per supportare il modello push per il flusso di dati. Questa classe non è consigliata per la creazione di filtri di lettura file. I lettori di file devono supportare il modello pull tramite [**l'interfaccia IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Per altre informazioni, vedere [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

 



| Variabili membro protette                     | Descrizione                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**m \_ iPins**](csource-m-ipins.md)            | Numero di segnaposto nel filtro.                                |
| [**m \_ paStreams**](csource-m-pastreams.md)    | Matrice di segnaposto.                                               |
| [**m \_ cStateLock**](csource-m-cstatelock.md)  | Oggetto sezione critica che protegge lo stato del filtro.      |
| Metodi pubblici                                 | Descrizione                                                  |
| [**CSource**](csource-csource.md)             | Metodo del costruttore.                                          |
| [**~CSource**](csource--csource.md)           | Metodo del distruttore.                                           |
| [**GetPinCount**](csource-getpincount.md)     | Recupera il numero di segnaposto nel filtro.                  |
| [**GetPin**](csource-getpin.md)               | Recupera un segnaposto.                                             |
| [**pStateLock**](csource--pstatelock.md)      | Recupera un puntatore all'oggetto sezione critica del filtro. |
| [**Aggiungi Elemento Aggiunto**](csource-addpin.md)               | Aggiunge un nuovo pin di output al filtro.                         |
| [**RemovePin**](csource-removepin.md)         | Rimuove un segnaposto specificato dal filtro.                     |
| [**FindPinNumber**](csource-findpinnumber.md) | Recupera il numero di un segnaposto specificato nel filtro.       |
| Metodi IBaseFilter                            | Descrizione                                                  |
| [**FindPin**](csource-findpin.md)             | Recupera il segnaposto con l'identificatore specificato.             |



 

## <a name="remarks"></a>Commenti

Per implementare un pin di output, eseguire le operazioni seguenti:

-   Derivare una classe da [**CSourceStream.**](csourcestream.md)
-   Eseguire [**l'override del metodo CSourceStream::GetMediaType**](csourcestream-getmediatype.md) ed eventualmente del metodo [**CSourceStream::CheckMediaType,**](csourcestream-checkmediatype.md) che convalida i tipi di supporti per il pin.
-   Implementare [**il metodo CBaseOutputPin::D ecideBufferSize,**](cbaseoutputpin-decidebuffersize.md) che restituisce i requisiti del buffer del pin.
-   Implementare [**il metodo CSourceStream::FillBuffer,**](csourcestream-fillbuffer.md) che riempie un buffer di esempio multimediale con dati.

Per implementare il filtro, eseguire le operazioni seguenti:

-   Derivare una classe da **CSource.**
-   Nel costruttore creare uno o più pin di output derivati da [**CSourceStream.**](csourcestream.md) I segnaposto si aggiungono automaticamente al filtro nei metodi del costruttore e si rimuovono nei metodi del distruttore.

Per sincronizzare lo stato del filtro tra più thread, chiamare il [**metodo CSource::p StateLock.**](csource--pstatelock.md) Questo metodo restituisce un puntatore alla sezione critica dello stato del filtro. Usare la [**classe CAutoLock**](cautolock.md) per contenere la sezione critica. Da un pin è possibile accedere **a pStateLock** dalla variabile membro [**CBasePin::m \_ pFilter**](cbasepin-m-pfilter.md) del pin, come indicato di seguito:


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scrittura di filtri di origine](writing-source-filters.md)
</dt> </dl>

 

 




