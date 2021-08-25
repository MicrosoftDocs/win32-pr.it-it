---
description: Il metodo Receive recapita un campione multimediale al pin di input.
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: Metodo COutputQueue.Receive (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8fb896429e53c16b30dbc4301f2e54fca5a2087dc1c89635fa33395f68ba0f5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871501"
---
# <a name="coutputqueuereceive-method"></a>Metodo COutputQueue.Receive

Il `Receive` metodo recapita un campione multimediale al pin di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Notifica di fine flusso ricevuta prima dell'elaborazione di questo esempio.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                                           |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama [**il metodo COutputQueue::ReceiveMultiple.**](coutputqueue-receivemultiple.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




