---
description: Il metodo RemoveI rimuove l'elemento in corrispondenza della posizione specificata.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Metodo CBaseList. RemoveI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330700"
---
# <a name="cbaselistremovei-method"></a>Metodo CBaseList. RemoveI

Il `RemoveI` metodo rimuove l'elemento in corrispondenza della posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Valore di posizione che indica l'elemento da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'elemento.

## <a name="remarks"></a>Commenti

Questo metodo elimina il nodo dall'elenco, ma non elimina l'elemento contenuto nel nodo.

Se *pos* è **null**, il metodo restituisce **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




