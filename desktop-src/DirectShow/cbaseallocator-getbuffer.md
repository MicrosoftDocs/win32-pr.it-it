---
description: Il metodo GetBuffer recupera un campione di supporti che contiene un buffer. Questo metodo implementa il metodo IMemAllocator::GetBuffer.
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Metodo CBaseAllocator.GetBuffer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a183079e954b3a0d8b07fc1d7daf039db8fcc840243a6ea421b2390ce02a3625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661683"
---
# <a name="cbaseallocatorgetbuffer-method"></a>Metodo CBaseAllocator.GetBuffer

Il `GetBuffer` metodo recupera un campione di supporti che contiene un buffer. Questo metodo implementa il [**metodo IMemAllocator::GetBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Riceve un puntatore all'interfaccia [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) buffer. Il chiamante deve rilasciare l'interfaccia .

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntatore all'ora di inizio dell'esempio.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntatore all'ora di fine dell'esempio.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinazione bit per bit di zero o più flag. La classe base supporta il flag seguente.



| Valore                                                                                                                                                          | Significato                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <dt>**AM \_ GBF \_ NOWAIT**</dt> </dl> | Non attendere che un buffer diventi disponibile. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                           | Descrizione                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                     |
| <dl> <dt>**VFW \_ E NON È STATO ESEGUITO IL \_ \_ COMMIT**</dt> </dl> | Non è stato eseguito il commit dell'allocatore.<br/> |
| <dl> <dt>**VFW \_ E \_ TIMEOUT**</dt> </dl>        | Timeout.<br/>                   |



 

## <a name="remarks"></a>Commenti

A meno che il chiamante non specifichi il flag **\_ AM GBF \_ NOWAIT** in *dwFlags*, questo metodo si blocca fino a quando non è disponibile l'esempio successivo.

L'esempio di supporto recuperato ha un puntatore valido al buffer allocato. Il chiamante è responsabile dell'impostazione di qualsiasi altra proprietà nell'esempio, ad esempio i timestamp, gli orari dei supporti o la proprietà sync-point. Per altre informazioni, vedere [**IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample)

Nella classe di base i *parametri pStartTime* *e pEndTime* vengono ignorati. Le classi derivate possono usare questi valori. Ad esempio, l'allocatore per il filtro [Renderer video](video-renderer-filter.md) usa questi valori per sincronizzare il passaggio tra le superfici directdraw.

Se il metodo deve attendere un esempio, incrementa il numero di oggetti in attesa ([**CBaseAllocator::m \_ lCount**](cbaseallocator-m-lcount.md)) e chiama la funzione [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) sul semaforo ([**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md)). Quando un esempio diventa disponibile, chiama il metodo [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) sull'allocatore, che aumenta il conteggio dei semafori di **m \_ lCount** (rilasciando quindi i thread in attesa) e imposta **m \_ lCount** su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

