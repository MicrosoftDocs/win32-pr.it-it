---
description: Introduzione alle classi di base dei filtri
ms.assetid: db6324d7-1914-44a8-a202-dff752b61c1a
title: Introduzione alle classi di base dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c0682a5ba9f6a051506911cf143474d9958f1caa926464d9a4c236366e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952560"
---
# <a name="introduction-to-the-filter-base-classes"></a>Introduzione alle classi di base dei filtri

Questo articolo descrive la libreria di classi DirectShow base di Microsoft. Questa libreria è destinata agli sviluppatori di filtri, ma i writer di applicazioni potrebbero trovare utili alcune delle classi helper e delle utilità di debug. La libreria di classi base non è tuttavia necessaria per DirectShow programmazione.

Le sezioni seguenti riepilogano le classi di base più importanti nella libreria.

**Classi di oggetti COM**

Le classi seguenti supportano la creazione di oggetti COM:



| Classe                              | Descrizione                            |
|------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject.md) | Classe dell'oggetto di base.                     |
| [**CUnknown**](cunknown.md)       | Implementa **l'interfaccia IUnknown.** |



 

La maggior parte delle DirectShow derivano da **CBaseObject.** Questa classe fornisce assistenza per il debug mantenendo un conteggio di tutti gli oggetti attivi nella DLL in fase di esecuzione. Nelle build di debug, la DLL asserzione se viene scaricata mentre il conteggio degli oggetti è maggiore di zero. In questo modo è più facile rilevare le perdite causate da problemi di conteggio dei riferimenti.

Tutte le classi di base che supportano le interfacce COM derivano da **CUnknown,** che eredita **CBaseObject.** La **classe CUnknown** supporta il conteggio dei riferimenti, **QueryInterface** e aggregration. Per altre informazioni, vedere [Come implementare IUnknown.](how-to-implement-iunknown.md)

**Filtrare e aggiungere classi**

Le classi seguenti supportano la creazione di oggetti DirectShow filtro e puntina:



| Classe                                    | Descrizione                                                                                                                                                     |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBaseFilter**](cbasefilter.md)       | Classe di base per i filtri. Implementa [**l'interfaccia IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                            |
| [**CBasePin**](cbasepin.md)             | Classe di base per i segnaposto. Implementa le [**interfacce IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**e IQualityControl.**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| [**CBaseInputPin**](cbaseinputpin.md)   | Classe di base per i pin di input che usano il trasporto di memoria locale. Implementa [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) Questa classe deriva da **CBasePin.** |
| [**CBaseOutputPin**](cbaseoutputpin.md) | Classe di base per i pin di output che usano **connessioni IMemInputPin.** Questa classe deriva da **CBasePin.**                                                         |



 

Le classi seguenti sono utili per la creazione di tipi di filtri più specializzati:



| Classe                                                  | Descrizione                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CSource**](csource.md)                             | Classe di base per i filtri di origine. Questa classe è progettata per la creazione di origini push. Non è adatto per le origini pull, ad esempio i lettori di file. Per creare pin di output per questa classe, usare la [**classe CSourceStream.**](csourcestream.md)                                                                   |
| [**CTransformFilter**](ctransformfilter.md)           | Classe di base per i filtri di trasformazione. Questa classe esegue una copia dei dati. I segnaposto per questa classe sono [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin.**](ctransformoutputpin.md)                                                                                            |
| [**CTransInPlaceFilter**](ctransinplacefilter.md)     | Classe di base per i filtri di trasformazione che non copiano i dati. Questa classe esegue l'elaborazione dei dati direttamente sui dati di input prima di passarla a valle. I segnaposto per questa classe sono [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin.**](ctransinplaceoutputpin.md) |
| [**CVideoTransformFilter**](cvideotransformfilter.md) | Classe di base per i filtri di trasformazione video. Questa classe deriva da **CTransformFilter e** aggiunge il supporto per il controllo qualità.                                                                                                                                                                                |
| [**CBaseRenderer**](cbaserenderer.md)                 | Classe di base per i filtri del renderer. Il pin di input per questa classe è [**CRendererInputPin.**](crendererinputpin.md)                                                                                                                                                                                          |
| [**CBaseVideoRenderer**](cbasevideorenderer.md)       | Classe di base per renderer video. Questa classe deriva da **CBaseRenderer**.                                                                                                                                                                                                                                |



 

Per usare queste classi, è necessario derivare la propria classe e scrivere codice per supportare la funzionalità specifica del filtro. Più specializzata è la classe di base, minore sarà il codice che sarà necessario scrivere nella classe derivata.

**Oggetti helper**

Le classi seguenti implementano oggetti helper usati da filtri e segnaposto. La maggior parte di queste classi può essere usata senza derivare nuove classi:



| Classe                                              | Descrizione                                                                                                                                                        |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPullPin**](cpullpin.md)                       | Oggetto helper per i pin di input nei filtri del parser. Supporta le [**connessioni IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) con origini pull.                                       |
| [**COutputQueue**](coutputqueue.md)               | Oggetto helper per i pin di output che accoda i campioni per il recapito in un thread di lavoro.                                                                                  |
| [**CSourceSeeking**](csourceseeking.md)           | Oggetto della Guida per l'implementazione della ricerca in un filtro di origine con esattamente un pin di output. Questa classe non è progettata per i filtri con più pin, ad esempio parser. |
| [**CEnumPins**](cenumpins.md)                     | Oggetto Enumeratore per l'enumerazione dei segnaposto in un filtro. Implementa [**l'interfaccia IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins)                                                       |
| [**CEnumMediaTypes**](cenummediatypes.md)         | Oggetto Enumerator per l'enumerazione dei tipi di supporti preferiti su un segnaposto. Implementa [**l'interfaccia IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)                             |
| [**CMemAllocator**](cmemallocator.md)             | Oggetto allocatore di memoria. Implementa [**l'interfaccia IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)                                                                          |
| [**CMediaSample**](cmediasample.md)               | Oggetto di esempio multimediale. Implementa [**l'interfaccia IMediaSample2.**](/windows/desktop/api/Strmif/nn-strmif-imediasample2)                                                                              |
| [**CBaseReferenceClock**](cbasereferenceclock.md) | Classe di base per gli orologi di riferimento. Implementa [**l'interfaccia IReferenceClock.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)                                                              |
| [**CMediaType**](cmediatype.md)                   | Oggetto helper per la modifica [**delle strutture AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                |



 

 

 



