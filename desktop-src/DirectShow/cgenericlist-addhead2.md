---
description: Il metodo AddHead aggiunge un elenco all'inizio dell'elenco.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Metodo CGenericList. AddHead (Wxlist. h)-parametro pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323803"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>Metodo CGenericList. AddHead (Wxlist. h)-parametro pList

Il `AddHead` metodo aggiunge un elenco all'inizio dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pList* 
</dt> <dd>

Puntatore all'elenco di elementi da aggiungere.

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

 

 




