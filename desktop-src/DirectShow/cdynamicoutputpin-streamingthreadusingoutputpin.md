---
description: Il metodo StreamingThreadUsingOutputPin determina se un thread sta eseguendo un'operazione di flusso sul pin.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Metodo CDynamicOutputPin. StreamingThreadUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331646"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a>CDynamicOutputPin. StreamingThreadUsingOutputPin, metodo

Il metodo StreamingThreadUsingOutputPin determina se un thread sta eseguendo un'operazione di flusso sul pin.

## <a name="syntax"></a>Sintassi


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se un thread sta eseguendo un'operazione di flusso sul pin. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Se i thread sono stati restituiti correttamente dal metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) e non hanno eseguito una chiamata corrispondente al metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , questo metodo restituisce **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




