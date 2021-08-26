---
description: Il metodo Pause segnala al thread di streaming di diventare attivo.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Metodo CSourceStream.Pause (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454f6e64461c036e9e3d9ef2f13033e5a210d783f3f6b734b7137a99b16402c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079311"
---
# <a name="csourcestreampause-method"></a>Metodo CSourceStream.Pause

Il `Pause` metodo segnala al thread di streaming di diventare attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o E \_ UNEXPECTED.

## <a name="remarks"></a>Commenti

Il [**metodo CSourceStream::Active**](csourcestream-active.md) chiama questo metodo. Quando il [**metodo CSourceStream::ThreadProc**](csourcestream-threadproc.md) riceve questa richiesta, chiama il metodo [**CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




