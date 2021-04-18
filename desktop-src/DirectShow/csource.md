---
description: La classe CSource è una classe di base per l'implementazione dei filtri di origine. Un filtro derivato da CSource contiene uno o più pin di output derivati dalla classe CSourceStream. Ogni pin di output crea un thread di lavoro che esegue il push degli esempi di supporti downstream.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Classe CSource (source. h)
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
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329362"
---
# <a name="csource-class"></a>Classe CSource

![gerarchia di classi CSource](images/source01.png)

La classe **CSource** è una classe di base per l'implementazione dei filtri di origine. Un filtro derivato da **CSource** contiene uno o più pin di output derivati dalla classe [**CSourceStream**](csourcestream.md) . Ogni pin di output crea un thread di lavoro che esegue il push degli esempi di supporti downstream.

> [!Note]  
> La classe **CSource** è progettata per supportare il modello push per il flusso di dati. Questa classe non è consigliata per la creazione di filtri di lettura file. I lettori di file devono supportare il modello pull tramite l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Per ulteriori informazioni, vedere [flusso di dati per gli sviluppatori di filtri](data-flow-for-filter-developers.md).

 



| Variabili membro protette                     | Descrizione                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**\_iPins m**](csource-m-ipins.md)            | Numero di pin sul filtro.                                |
| [**\_paStreams m**](csource-m-pastreams.md)    | Matrice di pin.                                               |
| [**\_cStateLock m**](csource-m-cstatelock.md)  | Oggetto sezione critica che protegge lo stato del filtro.      |
| Metodi pubblici                                 | Descrizione                                                  |
| [**CSource**](csource-csource.md)             | Metodo del costruttore.                                          |
| [**~ CSource**](csource--csource.md)           | Metodo del distruttore.                                           |
| [**GetPinCount**](csource-getpincount.md)     | Recupera il numero di pin sul filtro.                  |
| [**GetPin**](csource-getpin.md)               | Recupera un PIN.                                             |
| [**pStateLock**](csource--pstatelock.md)      | Recupera un puntatore all'oggetto sezione critica del filtro. |
| [**AddPin**](csource-addpin.md)               | Aggiunge un nuovo PIN di output al filtro.                         |
| [**RemovePin**](csource-removepin.md)         | Rimuove un PIN specificato dal filtro.                     |
| [**FindPinNumber**](csource-findpinnumber.md) | Recupera il numero di un PIN specificato sul filtro.       |
| Metodi IBaseFilter                            | Descrizione                                                  |
| [**FindPin**](csource-findpin.md)             | Recupera il pin con l'identificatore specificato.             |



 

## <a name="remarks"></a>Commenti

Per implementare un pin di output, procedere come segue:

-   Derivare una classe da [**CSourceStream**](csourcestream.md).
-   Eseguire l'override del metodo [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) ed eventualmente del metodo [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) , che convalida i tipi di supporto per il PIN.
-   Implementare il metodo [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , che restituisce i requisiti del buffer del PIN.
-   Implementare il metodo [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , che compila un buffer di esempio multimediale con i dati.

Per implementare il filtro, eseguire le operazioni seguenti:

-   Derivare una classe da **CSource**.
-   Nel costruttore creare uno o più pin di output derivati da [**CSourceStream**](csourcestream.md). I pin si aggiungono automaticamente al filtro nei metodi del costruttore e si rimuovono nei metodi del distruttore.

Per sincronizzare lo stato del filtro tra più thread, chiamare il metodo [**CSource::P stateLock**](csource--pstatelock.md) . Questo metodo restituisce un puntatore alla sezione critica dello stato del filtro. Usare la classe [**CAutoLock**](cautolock.md) per mantenere la sezione critica. Da un PIN è possibile accedere a **pStateLock** dalla variabile membro [**CBasePin:: m \_ pFilter**](cbasepin-m-pfilter.md) del PIN, come indicato di seguito:


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scrittura di filtri di origine](writing-source-filters.md)
</dt> </dl>

 

 




