---
description: Metodo del costruttore.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Costruttore CBaseList. CBaseList (TCHAR *, INT) (Wxlist. h)
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
ms.openlocfilehash: 9c947c8ffa6b61f919d03470b386ffa82945f3b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328671"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a>Costruttore CBaseList. CBaseList (TCHAR \* , int)

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

*pName* 
</dt> <dd>

Puntatore al nome dell'elenco.

</dd> <dt>

*iItems* 
</dt> <dd>

Dimensioni della cache del nodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per migliorare l'efficienza, la `CBaseList` classe mantiene una cache di nodi elenco. Se si conosce approssimativamente il numero di elementi che l'elenco conterrà, usare questa versione del costruttore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




