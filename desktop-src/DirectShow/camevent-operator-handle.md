---
description: Recupera l'handle dell'evento. Questo operatore non è supportato come L-value.
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: Metodo CAMEvent. operator HANDLE (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72193e89f415aabebfea4288fcdb986ccf8d73bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326948"
---
# <a name="cameventoperator-handle-method"></a>Metodo CAMEvent. operator HANDLE

Recupera l'handle dell'evento. Questo operatore non è supportato come L-value.

## <a name="syntax"></a>Sintassi


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la variabile membro [**CAMEvent:: m \_ hEvent**](camevent-m-hevent.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




