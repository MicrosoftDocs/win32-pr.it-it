---
description: Costruttore CBaseList.CBaseList(TCHAR \* , INT) - Metodo costruttore.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Costruttore CBaseList.CBaseList(TCHAR*, INT) (Wxlist.h)
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
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099639"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a>Costruttore CBaseList.CBaseList(TCHAR \* , INT)

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore al nome dell'elenco.

</dd> <dt>

*iItems* 
</dt> <dd>

Dimensioni della cache del nodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per migliorare l'efficienza, `CBaseList` la classe gestisce una cache di nodi elenco. Se si conosce approssimativamente il numero di elementi che saranno presenti nell'elenco, usare questa versione del costruttore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




