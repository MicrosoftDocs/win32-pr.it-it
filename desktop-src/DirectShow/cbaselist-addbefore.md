---
description: Il metodo AddBefore inserisce un elenco prima della posizione specificata.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Metodo CBaseList.AddBefore (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b4f85536b6a9372f164f596f96758a503096dbb0a5e5ed55adab42bc406b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016969"
---
# <a name="cbaselistaddbefore-method"></a>Metodo CBaseList.AddBefore

Il `AddBefore` metodo inserisce un elenco prima della posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Posizione prima della quale inserire l'elenco.

</dd> <dt>

*Plist* 
</dt> <dd>

Puntatore all'elenco da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo. In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

Gli indicatori di posizione esistenti, incluso quello specificato nel *parametro pos,* rimangono validi. Se il metodo ha esito negativo, è possibile che alcuni elementi siano stati aggiunti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




