---
description: Il metodo MoveToHead suddivide l'elenco e inserisce la parte finale all'inizio di un altro elenco.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Metodo CBaseList. MoveToHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328650"
---
# <a name="cbaselistmovetohead-method"></a>CBaseList. MoveToHead, metodo

Il `MoveToHead` metodo suddivide l'elenco e inserisce la parte finale all'inizio di un altro elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Indicatore di posizione che contrassegna la suddivisione nell'elenco.

</dd> <dt>

*pList* 
</dt> <dd>

Puntatore a un altro elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo suddivide l'elenco prima della posizione specificata dal parametro *pos* . La parte Head rimane nell'elenco. La parte finale viene inserita all'inizio dell'altro elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




