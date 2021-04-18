---
description: Il metodo pause segnala al thread di streaming che diventa attivo.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Metodo CSourceStream. pause (source. h)
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
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330663"
---
# <a name="csourcestreampause-method"></a>CSourceStream. pause (metodo)

Il `Pause` metodo segnala al thread di streaming di essere attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o e \_ imprevisto.

## <a name="remarks"></a>Commenti

Il metodo [**CSourceStream:: Active**](csourcestream-active.md) chiama questo metodo. Quando il metodo [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md) riceve la richiesta, chiama il metodo [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




