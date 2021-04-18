---
description: Il metodo Stop segnala al thread di streaming di arrestarsi.
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: Metodo CSourceStream. Stop (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44c9f845c092280ef5fafa808036654bd868a796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327529"
---
# <a name="csourcestreamstop-method"></a>Metodo CSourceStream. Stop

Il `Stop` metodo segnala al thread di streaming di arrestarsi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o e \_ imprevisto.

## <a name="remarks"></a>Commenti

Il metodo [**CSourceStream:: inactive**](csourcestream-inactive.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




