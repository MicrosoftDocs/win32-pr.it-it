---
description: Il metodo AddBefore inserisce un elenco prima della posizione specificata. Questo metodo usa i parametri "pos" e "pList".
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Metodo CGenericList. AddBefore (Wxlist. h)-pos, parametri pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762424"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>Metodo CGenericList. AddBefore (Wxlist. h)-pos, parametri pList

Il `AddBefore` metodo inserisce un elenco prima della posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Posizione in cui inserire l'elenco. L'elenco viene inserito prima di questa posizione.

</dd> <dt>

*pList* 
</dt> <dd>

Puntatore all'elenco da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo. In caso contrario, restituisce **false**.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




