---
description: Il metodo check Controlla se l'evento è impostato, senza bloccarsi.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Metodo CAMEvent. check (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324423"
---
# <a name="cameventcheck-method"></a>Metodo CAMEvent. check

Il `Check` metodo controlla se l'evento è impostato, senza bloccarsi.

## <a name="syntax"></a>Sintassi


```C++
BOOL Check();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

Restituisce **true** se l'evento è impostato o **false** in caso contrario. Questo metodo chiama il metodo [**CAMEvent:: wait**](camevent-wait.md) con un timeout di zero. Se l'oggetto è un evento di reimpostazione automatica, questo metodo reimposta l'evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




