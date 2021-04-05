---
description: Il metodo AddBefore inserisce un elemento prima della posizione specificata. Questo metodo usa i parametri "p" e "pObj".
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Metodo CGenericList. AddBefore (Wxlist. h)-p, parametri di pObj
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
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969538"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a>Metodo CGenericList. AddBefore (Wxlist. h)-p, parametri di pObj

Il `AddBefore` metodo inserisce un elemento prima della posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*p* 
</dt> <dd>

Posizione prima della quale inserire l'elenco. Se *p* è **null**, questo metodo aggiunge l'elemento alla parte finale dell'elenco.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntatore a un oggetto di tipo **Object** (il tipo di modello).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indicatore di posizione per l'elemento inserito.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




