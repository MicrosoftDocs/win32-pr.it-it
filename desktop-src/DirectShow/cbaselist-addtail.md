---
description: Il metodo AddTail aggiunge un altro elenco alla fine dell'elenco.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Metodo CBaseList. AddTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328672"
---
# <a name="cbaselistaddtail-method"></a>CBaseList. AddTail, metodo

Il `AddTail` metodo aggiunge un altro elenco alla fine dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pList* 
</dt> <dd>

Puntatore all'elenco da accodare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, è possibile che alcuni elementi siano stati aggiunti all'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




