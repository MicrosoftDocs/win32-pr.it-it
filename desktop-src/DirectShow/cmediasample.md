---
description: La classe CMediaSample definisce un esempio multimediale che supporta l'interfaccia IMediaSample2. L'esempio di supporto contiene un puntatore a un buffer di memoria e varie proprietà archiviate come variabili membro protette.
ms.assetid: 1e609c7c-3200-4540-904e-7659976df0da
title: Classe CMediaSample (Amfilter.h)
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
ms.openlocfilehash: 7b0b27c8878a2841eeecb3bc1ae24bdcc43d056c57a881596179f5d2bd990fcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084491"
---
# <a name="cmediasample-class"></a>Classe CMediaSample

![Gerarchia di classi cmediasample](images/wutil03.png)

La `CMediaSample` classe definisce un esempio multimediale che supporta l'interfaccia [**IMediaSample2.**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) L'esempio di supporto contiene un puntatore a un buffer di memoria e varie proprietà archiviate come variabili membro protette.

Gli esempi di supporti vengono creati dagli allocatori, derivati dalla [**classe CBaseAllocator.**](cbaseallocator.md) Il `CMediaSample` costruttore riceve un puntatore a un buffer allocato, insieme alle dimensioni del buffer. Altre proprietà vengono in genere impostate e recuperate tramite [**i metodi dell'interfaccia IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample)

Il ciclo di vita di un campione multimediale è diverso da quello della maggior parte degli oggetti COM:

-   L'allocatore contiene un elenco di esempi gratuiti. Quando un filtro richiede un nuovo esempio, chiama il metodo [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) dell'allocatore. L'allocatore recupera un campione dal relativo elenco gratuito, incrementa il conteggio dei riferimenti dell'esempio e restituisce un puntatore all'esempio.
-   Dopo aver eseguito il filtro con l'esempio, chiama il metodo **IUnknown::Release** nell'esempio. A differenza della maggior parte degli oggetti, l'esempio non si elimina quando il conteggio dei riferimenti raggiunge lo zero. Chiama invece il metodo [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) sull'allocatore e l'allocatore restituisce l'esempio al relativo elenco gratuito.
-   L'allocatore non elimina gli esempi finché non viene chiamato il metodo [**IMemAllocator::D ecommit.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)



| Variabili membro protette                                           | Descrizione                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**m \_ dwFlags**](cmediasample-m-dwflags.md)                         | Flag di proprietà di esempio.                                                                          |
| [**m \_ dwTypeSpecificFlags**](cmediasample-m-dwtypespecificflags.md) | Flag specifici del tipo.                                                                            |
| [**m \_ pBuffer**](cmediasample-m-pbuffer.md)                         | Puntatore al buffer di memoria che contiene i dati multimediali.                                      |
| [**m \_ lActual**](cmediasample-m-lactual.md)                         | Lunghezza in byte dei dati validi nel buffer.                                               |
| [**m \_ cbBuffer**](cmediasample-m-cbbuffer.md)                       | Dimensioni del buffer, in byte.                                                                   |
| [**m \_ pAllocator**](cmediasample-m-pallocator.md)                   | Puntatore all'allocatore che ha creato questo esempio.                                              |
| [**m \_ pNext**](cmediasample-m-pnext.md)                             | Puntatore all'esempio successivo nell'elenco di esempi dell'allocatore.                                  |
| [**m \_ Start**](cmediasample-m-start.md)                             | Ora di inizio di esempio.                                                                              |
| [**m \_ End**](cmediasample-m-end.md)                                 | Ora di fine di esempio.                                                                                |
| [**m \_ MediaStart**](cmediasample-m-mediastart.md)                   | Ora di inizio del supporto.                                                                               |
| [**m \_ MediaEnd**](cmediasample-m-mediaend.md)                       | Tempo di arresto del supporto.                                                                                |
| [**m \_ pMediaType**](cmediasample-m-pmediatype.md)                   | Puntatore al tipo di supporto, se il tipo è stato modificato rispetto all'esempio precedente nel flusso di dati. |
| [**m \_ dwStreamId**](cmediasample-m-dwstreamid.md)                   | Identificatore di flusso.                                                                              |
| Variabili membro pubbliche                                              | Descrizione                                                                                     |
| [**m \_ cRef**](cmediasample-m-cref.md)                               | Conteggio dei riferimenti.                                                                                |
| Metodi pubblici                                                       | Descrizione                                                                                     |
| [**CMediaSample**](cmediasample-cmediasample.md)                    | Metodo del costruttore.                                                                             |
| [**~ CMediaSample**](cmediasample--cmediasample.md)                 | Metodo del distruttore. Virtuale.                                                                     |
| [**SetPointer**](cmediasample-setpointer.md)                        | Imposta il puntatore al buffer di memoria.                                                          |
| Metodi di IMediaSample                                                 | Descrizione                                                                                     |
| [**GetPointer**](cmediasample-getpointer.md)                        | Recupera un puntatore di lettura/scrittura al buffer.                                                   |
| [**GetSize**](cmediasample-getsize.md)                              | Recupera le dimensioni del buffer.                                                               |
| [**GetTime**](cmediasample-gettime.md)                              | Recupera l'ora di inizio e fine del flusso in cui questo esempio deve iniziare e terminare.                        |
| [**Settime**](cmediasample-settime.md)                              | Imposta l'ora di inizio e fine dell'esempio.                             |
| [**IsSyncPoint**](cmediasample-issyncpoint.md)                      | Determina se l'inizio dell'esempio è un punto di sincronizzazione.                           |
| [**SetSyncPoint**](cmediasample-setsyncpoint.md)                    | Specifica se l'inizio di questo esempio è un punto di sincronizzazione.                      |
| [**IsPreroll**](cmediasample-ispreroll.md)                          | Determina se questo esempio è un esempio di pre-registrazione.                                                  |
| [**SetPreroll**](cmediasample-setpreroll.md)                        | Specifica se questo esempio è un esempio di pre-registrazione.                                              |
| [**GetActualDataLength**](cmediasample-getactualdatalength.md)      | Recupera la lunghezza dei dati validi nel buffer.                                           |
| [**SetActualDataLength**](cmediasample-setactualdatalength.md)      | Imposta la lunghezza dei dati validi nel buffer.                                                |
| [**GetMediaType**](cmediasample-getmediatype.md)                    | Recupera il tipo di supporto, se il tipo di supporto è diverso dall'esempio precedente.                   |
| [**SetMediaType**](cmediasample-setmediatype.md)                    | Imposta il tipo di supporto per l'esempio.                                                             |
| [**IsDiscontinuity**](cmediasample-isdiscontinuity.md)              | Determina se questo esempio rappresenta un'interruzione nel flusso di dati.                                |
| [**SetDiscontinuity**](cmediasample-setdiscontinuity.md)            | Specifica se questo esempio rappresenta un'interruzione nel flusso di dati.                            |
| [**GetMediaTime**](cmediasample-getmediatime.md)                    | Recupera gli orari dei supporti per questo esempio.                                                      |
| [**SetMediaTime**](cmediasample-setmediatime.md)                    | Imposta gli orari dei supporti per questo esempio.                                                           |
| Metodi di IMediaSample2                                                | Descrizione                                                                                     |
| [**GetProperties**](cmediasample-getproperties.md)                  | Recupera le proprietà dell'esempio.                                                         |
| [**SetProperties**](cmediasample-setproperties.md)                  | Imposta le proprietà dell'esempio.                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




