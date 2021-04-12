---
description: Riferimento alla classe base DirectShow
ms.assetid: 56f3685f-3df8-4358-b04e-3efc04b58008
title: Riferimento alla classe base DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8816656f0ae87224cc95886ad32aaa1a098f177
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482276"
---
# <a name="directshow-base-class-reference"></a>Riferimento alla classe base DirectShow

Questa sezione contiene le voci di riferimento per tutte le [classi base Microsoft DirectShow](directshow-base-classes.md), i relativi membri dati e le relative funzioni.



| Classe                                                                  | Descrizione                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**CAggDirectDraw**](caggdirectdraw.md)                               | Deprecato.                                                                                                                       |
| [**CAggDrawSurface**](caggdrawsurface.md)                             | Deprecato.                                                                                                                       |
| [**CAMEvent**](camevent.md)                                           | Classe wrapper per gli eventi di reimpostazione manuale e automatica.                                                                                  |
| [**CAMMsgEvent**](cammsgevent.md)                                     | Classe wrapper per oggetti evento che eseguono l'elaborazione dei messaggi.                                                                  |
| [**CAMSchedule**](camschedule.md)                                     | Utilità di pianificazione per gli orologi di riferimento.                                                                                                   |
| [**CAMThread**](camthread.md)                                         | Classe Bass per la gestione dei thread di lavoro.                                                                                           |
| [**CAutoLock**](cautolock.md)                                         | Include una sezione critica per l'ambito di un blocco.                                                                                |
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md) | Ottiene e rilascia l'accesso a un oggetto [**CDynamicOutputPin**](cdynamicoutputpin.md) .                                           |
| [**CBaseAllocator**](cbaseallocator.md)                               | Classe Bass per gli allocatori.                                                                                                        |
| [**CBaseBasicVideo**](cbasebasicvideo.md)                             | Gestisce il componente IDispatch dell'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .                                              |
| [**CBaseControlVideo**](cbasecontrolvideo.md)                         | Implementa l'interfaccia IBasicVideo per una finestra video generica.                                                                  |
| [**CBaseControlWindow**](cbasecontrolwindow.md)                       | Implementa l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .                                                                    |
| [**CBaseDispatch**](cbasedispatch.md)                                 | Classe di base per l'implementazione dell'interfaccia IDispatch.                                                                              |
| [**CBaseFilter**](cbasefilter.md)                                     | Classe di base per i filtri.                                                                                                           |
| [**CBaseInputPin**](cbaseinputpin.md)                                 | Classe di base per i pin di input.                                                                                                        |
| [**CBaseList**](cbaselist.md)                                         | Classe di base per elenchi generici.                                                                                                     |
| [**CBaseMediaFilter**](cbasemediafilter.md)                           | Implementa l'interfaccia [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) .                                                                    |
| [**CBaseObject**](cbaseobject.md)                                     | Classe di base per l'implementazione di oggetti DirectShow.                                                                                   |
| [**CBaseOutputPin**](cbaseoutputpin.md)                               | Classe di base per i pin di output.                                                                                                       |
| [**CBasePin**](cbasepin.md)                                           | Classe di base per i pin.                                                                                                              |
| [**CBasePropertyPage**](cbasepropertypage.md)                         | Classe di base per l'implementazione di pagine delle proprietà.                                                                                       |
| [**CBaseReferenceClock**](cbasereferenceclock.md)                     | Implementa un orologio di riferimento.                                                                                                     |
| [**CBaseRenderer**](cbaserenderer.md)                                 | Classe di base per l'implementazione di filtri renderer.                                                                                     |
| [**CBaseStreamControl**](cbasestreamcontrol.md)                       | Implementa l'interfaccia [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) .                                                            |
| [**CBaseVideoRenderer**](cbasevideorenderer.md)                       | Classe di base per renderer video.                                                                                                   |
| [**CBaseVideoWindow**](cbasevideowindow.md)                           | Gestisce il componente IDispatch dell'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .                                            |
| [**CBaseWindow**](cbasewindow.md)                                     | Classe di base per la gestione di Windows.                                                                                                  |
| [**CBasicAudio**](cbasicaudio.md)                                     | Gestisce il componente dell'interfaccia IDispatch dell'interfaccia [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) .                                    |
| [**CCmdQueue**](ccmdqueue.md)                                         | Classe helper per l'implementazione dell'interfaccia [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) .                                               |
| [**CCritSec**](ccritsec.md)                                           | Fornisce un blocco del thread.                                                                                                           |
| [**CDeferredCommand**](cdeferredcommand.md)                           | Implementa l'interfaccia [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) .                                                            |
| [**CDispParams**](cdispparams.md)                                     | Classe wrapper per la struttura DISPPARAMS.                                                                                       |
| [**CDrawImage**](cdrawimage.md)                                       | Classe helper per il disegno in una finestra.                                                                                             |
| [**CDynamicOutputPin**](cdynamicoutputpin.md)                         | Pin di output che supporta le riconnessioni dyanamic e le modifiche del formato.                                                               |
| [**CEnumMediaTypes**](cenummediatypes.md)                             | Enumeratore per i tipi di supporto preferiti.                                                                                             |
| [**CEnumPins**](cenumpins.md)                                         | Enumeratore per i pin.                                                                                                              |
| [**CFactoryTemplate**](cfactorytemplate.md)                           | Classe che fornisce informazioni per un class factory.                                                                              |
| [**CGenericList**](cgenericlist.md)                                   | Modello di classe che implementa un elenco specifico del tipo.                                                                              |
| [**CImageAllocator**](cimageallocator.md)                             | Allocatore per le sezioni DIB.                                                                                                       |
| [**CImageDisplay**](cimagedisplay.md)                                 | Classe helper per la gestione dei formati di visualizzazione delle immagini.                                                                                  |
| [**CImagePalette**](cimagepalette.md)                                 | Classe helper per la gestione delle tavolozze.                                                                                               |
| [**CImageSample**](cimagesample.md)                                   | Esempio multimediale che usa le sezioni DIB.                                                                                              |
| [**CLoadDirectDraw**](cloaddirectdraw.md)                             | Deprecato.                                                                                                                       |
| [**CMediaControl**](cmediacontrol.md)                                 | Gestisce i metodi IDispatch dell'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .                                            |
| [**CMediaEvent**](cmediaevent.md)                                     | Gestisce i metodi IDispatch dell'interfaccia [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .                                                |
| [**CMediaPosition**](cmediaposition.md)                               | Gestisce i metodi IDispatch dell'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .                                          |
| [**CMediaSample**](cmediasample.md)                                   | Esempio multimediale.                                                                                                                     |
| [**CMediaType**](cmediatype.md)                                       | Classe per la gestione dei tipi di supporto.                                                                                                   |
| [**CMemAllocator**](cmemallocator.md)                                 | Allocatore di memoria.                                                                                                                 |
| [**CMsg**](cmsg.md)                                                   | Classe helper per la gestione delle richieste effettuate a un oggetto [**CMsgThread**](cmsgthread.md) .                                             |
| [**CMsgThread**](cmsgthread.md)                                       | Thread di lavoro che accoda le richieste al thread di Accodamento per il completamento asincrono.                                             |
| [**COARefTime**](coareftime.md)                                       | Converte i tempi di riferimento tra i secondi e le unità 100-nanosecondi.                                                                |
| [**COutputQueue**](coutputqueue.md)                                   | Oggetto che accoda gli esempi multimediali per il recapito.                                                                                    |
| [**CPersistStream**](cpersiststream.md)                               | Classe di base per l'implementazione dell'interfaccia IPersistStream.                                                                         |
| [**CPosPassThru**](cpospassthru.md)                                   | Gestisce i comandi Seek per i filtri con un pin di input.                                                                             |
| [**CPullPin**](cpullpin.md)                                           | Classe helper che estrae i dati da un pin di output che supporta l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .                 |
| [**CQueue**](cqueue.md)                                               | Modello di classe che implementa una semplice coda a dimensione statica.                                                                  |
| [**CRefTime**](creftime.md)                                           | Classe helper per gestire i tempi di riferimento.                                                                                           |
| [**CRenderedInputPin**](crenderedinputpin.md)                         | Pin di input per i filtri renderer che supportano più input.                                                                      |
| [**CRendererInputPin**](crendererinputpin.md)                         | Pin di input per la classe [**CBaseRenderer**](cbaserenderer.md) .                                                                   |
| [**CRendererPosPassThru**](crendererpospassthru.md)                   | Gestisce i comandi Seek per i filtri renderer.                                                                                       |
| [**CSeekingPassThru**](cseekingpassthru.md)                           | Oggetto helper che crea oggetti [**CPosPassThru**](cpospassthru.md) e [**CRendererPosPassThru**](crendererpospassthru.md) . |
| [**CSource**](csource.md)                                             | Classe di base per l'implementazione dei filtri di origine.                                                                                       |
| [**CSourcePosition**](csourceposition.md)                             | Classe astratta per l'implementazione dell'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) . Obsoleta.                                 |
| [**CSourceSeeking**](csourceseeking.md)                               | Classe astratta per l'implementazione della ricerca nei filtri di origine con un pin di output.                                                    |
| [**CSourceStream**](csourcestream.md)                                 | Pin di output per la classe [**CSource**](csource.md) .                                                                              |
| [**CSystemClock**](csystemclock.md)                                   | Clock di sistema.                                                                                                                     |
| [**CTransformFilter**](ctransformfilter.md)                           | Classe di base per l'implementazione dei filtri di trasformazione.                                                                                    |
| [**CTransformInputPin**](ctransforminputpin.md)                       | Pin di input usato dalla classe CTransformFilter.                                                                                     |
| [**CTransformOutputPin**](ctransformoutputpin.md)                     | Pin di output usato dalla classe CTransformFilter.                                                                                    |
| [**CTransInPlaceFilter**](ctransinplacefilter.md)                     | Classe per l'implementazione di filtri di trasformazione che non copiano i dati.                                                                   |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin.md)                 | Pin di input per la classe CTransInPlaceFilter.                                                                                      |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)               | Pin di output per la classe CTransInPlaceFilter.                                                                                     |
| [**CUnknown**](cunknown.md)                                           | Implementa l'interfaccia IUnknown.                                                                                                |
| [**CVideoTransformFilter**](cvideotransformfilter.md)                 | Classe di base per i filtri di trasformazione video.                                                                                           |
| [**FOURCCMap**](fourccmap.md)                                         | Classe helper per la conversione tra GUID e FourCC.                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 



