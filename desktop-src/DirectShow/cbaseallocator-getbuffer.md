---
description: 'Il metodo GetBuffer recupera un esempio di supporto che contiene un buffer. Questo metodo implementa il metodo IMemAllocator:: GetBuffer.'
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Metodo CBaseAllocator. GetBuffer (Amfilter. h)
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
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331814"
---
# <a name="cbaseallocatorgetbuffer-method"></a>CBaseAllocator. GetBuffer, metodo

Il `GetBuffer` metodo recupera un esempio di supporto che contiene un buffer. Questo metodo implementa il metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .

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

Riceve un puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del buffer. Il chiamante deve rilasciare l'interfaccia.

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
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <dt>**AM \_ GBF \_ nowait**</dt> </dl> | Non attendere che un buffer diventi disponibile. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                           | Descrizione                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                     |
| <dl> <dt>**non è stato \_ \_ eseguito il \_ commit di VFW E**</dt> </dl> | Non è stato eseguito il commit dell'allocatore.<br/> |
| <dl> <dt>**TIMEOUT di VFW \_ E \_**</dt> </dl>        | Timeout.<br/>                   |



 

## <a name="remarks"></a>Commenti

A meno che il chiamante non specifichi il flag **\_ GBF \_ nowait** in *dwFlags*, questo metodo si blocca fino a quando non è disponibile l'esempio successivo.

L'esempio di supporto recuperato ha un puntatore valido al buffer allocato. Il chiamante è responsabile dell'impostazione di qualsiasi altra proprietà nell'esempio, ad esempio i timestamp, i tempi dei supporti o la proprietà del punto di sincronizzazione. Per ulteriori informazioni, vedere [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).

Nella classe di base, i parametri *pStartTime* e *pEndTime* vengono ignorati. Le classi derivate possono usare questi valori. Ad esempio, l'allocatore per il filtro [renderer video](video-renderer-filter.md) utilizza questi valori per sincronizzare il cambio tra superfici di DirectDraw.

Se il metodo deve attendere un campione, incrementa il numero di oggetti in attesa ([**CBaseAllocator:: m \_ lCount**](cbaseallocator-m-lcount.md)) e chiama [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) Function sul semaforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)). Quando un campione diventa disponibile, viene chiamato il metodo [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) sull'allocatore, che aumenta il numero di semafori per **m \_ lCount** (rilasciando quindi i thread in attesa) e imposta **m \_ lCount** su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

