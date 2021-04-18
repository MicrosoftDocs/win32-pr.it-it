---
description: Il metodo Wait si blocca fino a quando l'evento non viene segnalato o fino a quando non si verifica un timeout.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Metodo CAMEvent. Wait (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331332"
---
# <a name="cameventwait-method"></a>Metodo CAMEvent. Wait

Il `Wait` metodo si blocca fino a quando l'evento non viene segnalato o fino a quando non si verifica un timeout.

## <a name="syntax"></a>Sintassi


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Valore di timeout facoltativo, rappresentato in millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'evento viene segnalato. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Per gli eventi di reimpostazione automatica, l'evento viene reimpostato su uno stato non segnalato quando il metodo restituisce un risultato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




