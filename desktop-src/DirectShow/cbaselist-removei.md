---
description: Il metodo RemoveI rimuove l'elemento nella posizione specificata.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Metodo CBaseList.RemoveI (Wxlist.h)
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
ms.openlocfilehash: ac3277f30e959e42cf2fd2d1aeeb13f81cb17515abb8434a8ae13406d244aaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823738"
---
# <a name="cbaselistremovei-method"></a>Metodo CBaseList.RemoveI

Il `RemoveI` metodo rimuove l'elemento nella posizione specificata.

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

Valore POSITION che indica l'elemento da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'elemento.

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

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




