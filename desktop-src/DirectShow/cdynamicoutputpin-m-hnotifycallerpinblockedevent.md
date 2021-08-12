---
description: Evento segnalato quando il pin si blocca correttamente o l'utente annulla un blocco in sospeso.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: Membro CDynamicOutputPin::m_hNotifyCallerPinBlockedEvent (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfea481a3f24aee808fffba9be91b1fecf63fce8a875dc056420a8f075b677d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656406"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a>Membro CDynamicOutputPin::m \_ hNotifyCallerPinBlockedEvent

Evento segnalato quando il pin si blocca correttamente o l'utente annulla un blocco in sospeso.

## <a name="syntax"></a>Sintassi


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a>Osservazioni

Prima di accedere a questa variabile, mantenere la [**sezione critica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




