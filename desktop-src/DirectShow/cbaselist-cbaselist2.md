---
description: 'Costruttore CBaseList.CBaseList : metodo costruttore.'
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Costruttore CBaseList.CBaseList (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b734722371aa80e3c120dde3c6fb629785dfc6cdf9786c7f4ab1cbea87e5559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016979"
---
# <a name="cbaselistcbaselist-constructor"></a>Costruttore CBaseList.CBaseList

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore al nome dell'elenco.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per migliorare l'efficienza, `CBaseList` la classe gestisce una cache di nodi elenco. Questa versione del costruttore usa le dimensioni predefinite della cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




