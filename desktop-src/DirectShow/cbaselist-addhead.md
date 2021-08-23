---
description: Il metodo AddHead inserisce un altro elenco all'inizio dell'elenco.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Metodo CBaseList.AddHead (Wxlist.h)
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
ms.openlocfilehash: fa8108af5f779bea4c1a1e756ab018ed9c902d3e516556c42b7899f442cb7704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814321"
---
# <a name="cbaselistaddhead-method"></a>Metodo CBaseList.AddHead

Il `AddHead` metodo inserisce un altro elenco all'inizio dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Plist* 
</dt> <dd>

Puntatore all'elenco di elementi da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, è possibile che alcuni elementi siano stati aggiunti all'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




