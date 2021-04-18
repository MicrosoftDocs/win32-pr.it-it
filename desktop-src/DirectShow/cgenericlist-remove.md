---
description: Il metodo Remove rimuove l'elemento in corrispondenza della posizione specificata.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Metodo CGenericList. Remove (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329795"
---
# <a name="cgenericlistremove-method"></a>Metodo CGenericList. Remove

Il `Remove` metodo rimuove l'elemento in corrispondenza della posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
OBJECT* Remove(
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

Restituisce un puntatore a un oggetto di tipo **Object** (il tipo di modello).

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

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




