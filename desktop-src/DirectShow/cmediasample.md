---
description: La classe CMediaSample definisce un esempio di supporto che supporta l'interfaccia IMediaSample2. L'esempio multimediale contiene un puntatore a un buffer di memoria e varie proprietà archiviate come variabili membro protette.
ms.assetid: 1e609c7c-3200-4540-904e-7659976df0da
title: Classe CMediaSample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72cfe0f86ff6b6643f2f7793822899136a5c6454
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324023"
---
# <a name="cmediasample-class"></a>Classe CMediaSample

![gerarchia di classi cmediasample](images/wutil03.png)

La `CMediaSample` classe definisce un esempio multimediale che supporta l'interfaccia [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) . L'esempio multimediale contiene un puntatore a un buffer di memoria e varie proprietà archiviate come variabili membro protette.

Gli esempi di supporti vengono creati dagli allocatori, che sono derivati dalla classe [**CBaseAllocator**](cbaseallocator.md) . Il `CMediaSample` costruttore riceve un puntatore a un buffer allocato, insieme alle dimensioni del buffer. Le altre proprietà vengono in genere impostate e recuperate tramite i metodi dell'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .

Il ciclo di vita di un campione multimediale è diverso da quello della maggior parte degli oggetti COM:

-   L'allocatore include un elenco di esempi gratuiti. Quando un filtro necessita di un nuovo esempio, chiama il metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) dell'allocatore. L'allocatore recupera un esempio dal relativo elenco di disponibilità, incrementa il conteggio dei riferimenti dell'esempio e restituisce un puntatore all'esempio.
-   Una volta eseguito il filtro con l'esempio, viene chiamato il metodo **IUnknown:: Release** nell'esempio. A differenza della maggior parte degli oggetti, l'esempio non elimina se stesso quando il conteggio dei riferimenti raggiunge zero. Chiama invece il metodo [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) sull'allocatore e l'allocatore restituisce l'esempio nell'elenco di disponibilità.
-   L'allocatore non elimina gli esempi fino a quando non viene chiamato il metodo [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .



| Variabili membro protette                                           | Descrizione                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**\_dwFlags m**](cmediasample-m-dwflags.md)                         | Flag di proprietà di esempio.                                                                          |
| [**\_dwTypeSpecificFlags m**](cmediasample-m-dwtypespecificflags.md) | Flag specifici del tipo.                                                                            |
| [**\_pbuffer m**](cmediasample-m-pbuffer.md)                         | Puntatore al buffer di memoria che contiene i dati multimediali.                                      |
| [**\_lActual m**](cmediasample-m-lactual.md)                         | Lunghezza dei dati validi nel buffer, in byte.                                               |
| [**\_cbBuffer m**](cmediasample-m-cbbuffer.md)                       | Dimensioni del buffer, in byte.                                                                   |
| [**\_pAllocator m**](cmediasample-m-pallocator.md)                   | Puntatore all'allocatore che ha creato l'esempio.                                              |
| [**\_pNext m**](cmediasample-m-pnext.md)                             | Puntatore all'esempio successivo nell'elenco di esempi dell'allocatore.                                  |
| [**\_inizio m**](cmediasample-m-start.md)                             | Ora di inizio dell'esempio.                                                                              |
| [**\_fine m**](cmediasample-m-end.md)                                 | Ora di fine campione.                                                                                |
| [**\_MediaStart m**](cmediasample-m-mediastart.md)                   | Ora di inizio del supporto.                                                                               |
| [**\_MediaEnd m**](cmediasample-m-mediaend.md)                       | Ora di arresto del supporto.                                                                                |
| [**\_pMediaType m**](cmediasample-m-pmediatype.md)                   | Puntatore al tipo di supporto, se il tipo è stato modificato rispetto all'esempio precedente nel flusso di dati. |
| [**\_dwStreamId m**](cmediasample-m-dwstreamid.md)                   | Identificatore di flusso.                                                                              |
| Variabili membro pubblico                                              | Descrizione                                                                                     |
| [**\_cref m**](cmediasample-m-cref.md)                               | Conteggio riferimenti.                                                                                |
| Metodi pubblici                                                       | Descrizione                                                                                     |
| [**CMediaSample**](cmediasample-cmediasample.md)                    | Metodo del costruttore.                                                                             |
| [**~ CMediaSample**](cmediasample--cmediasample.md)                 | Metodo del distruttore. Virtuale.                                                                     |
| [**Setpoint**](cmediasample-setpointer.md)                        | Imposta il puntatore al buffer di memoria.                                                          |
| Metodi IMediaSample                                                 | Descrizione                                                                                     |
| [**Getpointer**](cmediasample-getpointer.md)                        | Recupera un puntatore di lettura/scrittura nel buffer.                                                   |
| [**GetSize**](cmediasample-getsize.md)                              | Recupera la dimensione del buffer.                                                               |
| [**GetTime**](cmediasample-gettime.md)                              | Recupera l'ora del flusso in cui l'esempio deve iniziare e terminare.                        |
| [**SetTime**](cmediasample-settime.md)                              | Imposta il flusso di tempo in cui l'esempio deve iniziare e terminare.                             |
| [**IsSyncPoint**](cmediasample-issyncpoint.md)                      | Determina se l'inizio dell'esempio è un punto di sincronizzazione.                           |
| [**SetSyncPoint**](cmediasample-setsyncpoint.md)                    | Specifica se l'inizio di questo esempio è un punto di sincronizzazione.                      |
| [**IsPreroll**](cmediasample-ispreroll.md)                          | Determina se questo esempio è un esempio di preroll.                                                  |
| [**SetPreroll**](cmediasample-setpreroll.md)                        | Specifica se questo esempio è un esempio di preroll.                                              |
| [**GetActualDataLength**](cmediasample-getactualdatalength.md)      | Recupera la lunghezza dei dati validi nel buffer.                                           |
| [**SetActualDataLength**](cmediasample-setactualdatalength.md)      | Imposta la lunghezza dei dati validi nel buffer.                                                |
| [**GetMediaType**](cmediasample-getmediatype.md)                    | Recupera il tipo di supporto, se il tipo di supporto è diverso rispetto all'esempio precedente.                   |
| [**SetMediaType**](cmediasample-setmediatype.md)                    | Imposta il tipo di supporto per l'esempio.                                                             |
| [**IsDiscontinuity**](cmediasample-isdiscontinuity.md)              | Determina se questo esempio rappresenta un'interruzioni nel flusso di dati.                                |
| [**SetDiscontinuity**](cmediasample-setdiscontinuity.md)            | Specifica se questo esempio rappresenta un'interruzioni nel flusso di dati.                            |
| [**GetMediaTime**](cmediasample-getmediatime.md)                    | Recupera i tempi di supporto per questo esempio.                                                      |
| [**SetMediaTime**](cmediasample-setmediatime.md)                    | Imposta i tempi dei supporti per questo esempio.                                                           |
| Metodi IMediaSample2                                                | Descrizione                                                                                     |
| [**GetProperties**](cmediasample-getproperties.md)                  | Recupera le proprietà dell'esempio.                                                         |
| [**SetProperties**](cmediasample-setproperties.md)                  | Imposta le proprietà dell'esempio.                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




