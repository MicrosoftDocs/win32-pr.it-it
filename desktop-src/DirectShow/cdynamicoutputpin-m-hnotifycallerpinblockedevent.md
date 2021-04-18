---
description: Evento segnalato quando il pin si blocca correttamente oppure l'utente annulla un blocco in sospeso.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Membro CDynamicOutputPin:: m_hNotifyCallerPinBlockedEvent (Amfilter. h)'
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
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325193"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a>Membro hNotifyCallerPinBlockedEvent di CDynamicOutputPin:: m \_

Evento segnalato quando il pin si blocca correttamente oppure l'utente annulla un blocco in sospeso.

## <a name="syntax"></a>Sintassi


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a>Osservazioni

Prima di accedere a questa variabile, conservare la sezione [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




