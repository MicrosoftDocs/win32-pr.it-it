---
description: Il metodo AddAfter inserisce un elenco dopo la posizione specificata e usa i parametri 'pos' e 'plist'.
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Metodo CGenericList.AddAfter (Wxlist.h) - parametri pos e plist
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
ms.openlocfilehash: 846e37b961af8d2492b3aff032193e87fb3603eb1751c25f0e3ca8e0c5d38618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697481"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>Metodo CGenericList.AddAfter (Wxlist.h) - parametri pos e plist

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

*Plist* 
</dt> <dd>

Puntatore all'elenco da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist.h (includere Flussi.h) |
| Libreria| Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




