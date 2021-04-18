---
description: Il metodo AddHead inserisce un altro elenco all'inizio dell'elenco.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Metodo CBaseList. AddHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328675"
---
# <a name="cbaselistaddhead-method"></a>CBaseList. AddHead, metodo

Il `AddHead` metodo inserisce un altro elenco all'inizio dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pList* 
</dt> <dd>

Puntatore all'elenco di elementi da aggiungere.

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

 

 




