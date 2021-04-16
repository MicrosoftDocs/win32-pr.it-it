---
description: Il metodo AddAfter inserisce un elenco dopo la posizione specificata e usa i parametri "pos" e "plist".
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Metodo CGenericList. AddAfter (Wxlist. h)-pos, parametri plist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531105"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>Metodo CGenericList. AddAfter (Wxlist. h)-pos, parametri plist

Il `AddAfter` metodo inserisce un elenco dopo la posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Posizione in cui inserire l'elenco. L'elenco viene inserito dopo questa posizione.

</dd> <dt>

*pList* 
</dt> <dd>

Puntatore all'elenco da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




