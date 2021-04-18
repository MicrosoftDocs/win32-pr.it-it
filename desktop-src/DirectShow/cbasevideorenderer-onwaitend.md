---
description: Il metodo OnWaitEnd viene chiamato al termine di un tempo di attesa.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Metodo CBaseVideoRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325365"
---
# <a name="cbasevideorendereronwaitend-method"></a>CBaseVideoRenderer. OnWaitEnd, metodo

Il metodo OnWaitEnd viene chiamato al termine di un tempo di attesa.

## <a name="syntax"></a>Sintassi


```C++
void OnWaitEnd();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro esegue solo la registrazione delle prestazioni. Viene chiamato quando il thread viene risvegliato dall'attesa nella finestra o quando l'esempio successivo è dovuto al rendering. Potrebbe essere usato per raccogliere informazioni che controllano la sincronizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




