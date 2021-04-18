---
description: Metodo del costruttore.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Costruttore CAMEvent. CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324429"
---
# <a name="cameventcamevent-constructor"></a>Costruttore CAMEvent. CAMEvent

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fManualReset* 
</dt> <dd>

Valore booleano che specifica se l'oggetto è un evento di reimpostazione manuale o un evento di reimpostazione automatica. Se **true**, l'oggetto è un evento di reimpostazione manuale. In caso contrario, si tratta di un evento di reimpostazione automatica.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** . Se il costruttore ha esito negativo, questo parametro riceve un codice di errore. In tal caso, lo stato dell'oggetto non è valido.

Per la compatibilità con le versioni precedenti di strmbase. lib, il valore predefinito di questo parametro è **null**. Tuttavia, è preferibile passare un valore non **null** , in modo che il chiamante possa controllare lo stato dell'oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'evento inizia con uno stato non segnalato.

Con un evento di reimpostazione automatica, il metodo [**CAMEvent:: wait**](camevent-wait.md) Reimposta l'evento su non segnalato quando il metodo restituisce un risultato. Con un evento di reimpostazione manuale, l'evento rimane segnalato fino a quando non viene chiamato il metodo [**CAMEvent:: Reset**](camevent-reset.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




