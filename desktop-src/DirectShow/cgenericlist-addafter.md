---
description: Il metodo AddAfter inserisce un elemento dopo la posizione specificata e usa i parametri "p" e "pObj".
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Metodo CGenericList. AddAfter (Wxlist. h)-p, parametri di pObj
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
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356154"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>Metodo CGenericList. AddAfter (Wxlist. h)-p, parametri di pObj

Il `AddAfter` metodo inserisce un elemento dopo la posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*p* 
</dt> <dd>

Posizione dopo la quale aggiungere l'elemento. Se *p* è **null**, il metodo aggiunge l'elemento all'inizio dell'elenco.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntatore a un oggetto di tipo **Object** (il tipo di modello).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indicatore di posizione dell'elemento inserito.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




