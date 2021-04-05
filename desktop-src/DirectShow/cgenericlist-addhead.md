---
description: Il metodo AddHead aggiunge un elemento all'inizio dell'elenco.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Metodo CGenericList. AddHead (Wxlist. h)-parametro pObj
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
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104058706"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a>Metodo CGenericList. AddHead (Wxlist. h)-parametro pObj

Il `AddHead` metodo aggiunge un elemento all'inizio dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObj* 
</dt> <dd>

Puntatore a un oggetto di tipo **Object** (il tipo di modello).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore di posizione che indica la nuova posizione Head. Se il metodo ha esito negativo, il valore restituito è **null**.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




