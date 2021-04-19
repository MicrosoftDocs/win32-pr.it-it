---
description: Il metodo GetDeliveryBuffer recupera un esempio di supporto che contiene un buffer vuoto.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Metodo CBaseOutputPin. GetDeliveryBuffer (Amfilter. h)
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
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332061"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>CBaseOutputPin. GetDeliveryBuffer, metodo

Il `GetDeliveryBuffer` metodo recupera un esempio di supporto che contiene un buffer vuoto.

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

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del buffer.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntatore all'ora di inizio dell'esempio, o **null**.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntatore all'ora di fine dell'esempio, o **null**.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinazione bit per bit di flag supportati dall'interfaccia [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | Nessun allocatore disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo **IMemAllocator:: GetBuffer** nell'allocatore e passa i parametri al metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




