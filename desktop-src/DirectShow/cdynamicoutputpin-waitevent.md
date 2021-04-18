---
description: Il metodo WaitEvent attende fino a quando non viene segnalato l'evento specificato.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Metodo CDynamicOutputPin. WaitEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b27f3c387c82eaeebc119f967deaca8e7314ccd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330405"
---
# <a name="cdynamicoutputpinwaitevent-method"></a>CDynamicOutputPin. WaitEvent, metodo

Il `WaitEvent` metodo attende fino a quando non viene segnalato l'evento specificato.

## <a name="syntax"></a>Sintassi


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hEvent* 
</dt> <dd>

Handle per un evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>          |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Errore imprevisto.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




