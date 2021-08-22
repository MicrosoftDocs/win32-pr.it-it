---
description: Il metodo Remove rimuove l'elemento nella posizione specificata.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Metodo CGenericList.Remove (Wxlist.h)
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
ms.openlocfilehash: 40b00d0772f391978fa6e581623446c67c2f37deabb1737e2602d7da7382fbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317761"
---
# <a name="cgenericlistremove-method"></a>Metodo CGenericList.Remove

Il `Remove` metodo rimuove l'elemento nella posizione specificata.

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

Valore POSITION che indica l'elemento da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a un oggetto di tipo **OBJECT** (il tipo di modello).

## <a name="remarks"></a>Commenti

Questo metodo elimina il nodo dall'elenco, ma non elimina l'elemento contenuto in tale nodo.

Se *pos* è **NULL,** il metodo restituisce **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




