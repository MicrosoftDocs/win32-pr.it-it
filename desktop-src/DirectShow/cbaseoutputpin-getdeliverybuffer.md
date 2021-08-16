---
description: Il metodo GetDeliveryBuffer recupera un campione di supporti che contiene un buffer vuoto.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Metodo CBaseOutputPin.GetDeliveryBuffer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d118e21ea67932529c41b35595619c6e03b907718708ba285aa2a6578177f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823610"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>Metodo CBaseOutputPin.GetDeliveryBuffer

Il `GetDeliveryBuffer` metodo recupera un campione di supporti che contiene un buffer vuoto.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSample* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) buffer.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntatore all'ora di inizio dell'esempio o **NULL.**

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntatore all'ora di fine dell'esempio o **NULL.**

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinazione bit per bit di flag supportati [**dall'interfaccia IMemAllocator::GetBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | Nessun allocatore disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il **metodo IMemAllocator::GetBuffer** sull'allocatore e passa i parametri a tale metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




