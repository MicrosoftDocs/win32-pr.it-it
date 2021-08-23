---
description: Numero di thread di streaming che usano questo pin.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: Membro CDynamicOutputPin::m_dwNumOutstandingOutputPinUsers (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29fc593065af4252f58ce4bb08dd41fac82926dc11490377f6a8af614794b22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688711"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a>Membro CDynamicOutputPin::m \_ dwNumOutstandingOutputPinUsers

Numero di thread di streaming che usano questo pin.

## <a name="syntax"></a>Sintassi


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a>Osservazioni

Il [**metodo CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) incrementa questa variabile e il metodo [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) la decrementa. Quando il valore è maggiore di zero, alcuni thread usano questo pin per trasmettere i dati o per modificare il tipo di connessione. Il pin non può essere bloccato in questo caso.

Prima di accedere a questa variabile, mantenere la [**sezione critica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> <dt>

[**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




