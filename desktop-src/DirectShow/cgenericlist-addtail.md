---
description: Il metodo AddTail aggiunge un elemento alla fine dell'elenco.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: Metodo CGenericList. AddTail (Wxlist. h)-parametro pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323799"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a>Metodo CGenericList. AddTail (Wxlist. h)-parametro pObj

Il `AddTail` metodo aggiunge un elemento alla fine dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
POSITION AddTail(
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

Restituisce un valore di posizione per la nuova posizione della coda. Se il metodo ha esito negativo, restituisce **null**.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




