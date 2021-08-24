---
description: Il metodo WaitEvent attende finché non viene segnalato l'evento specificato.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Metodo CDynamicOutputPin.WaitEvent (Amfilter.h)
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
ms.openlocfilehash: 3797c9127d3e931cd64fa35e822eac3151acc7fa1a8c4c0c9e93d6a36c0dfe99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871931"
---
# <a name="cdynamicoutputpinwaitevent-method"></a>Metodo CDynamicOutputPin.WaitEvent

Il `WaitEvent` metodo attende finché non viene segnalato l'evento specificato.

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>          |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl> | Errore imprevisto.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




