---
description: Il metodo AddHead aggiunge un elenco all'inizio dell'elenco.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Metodo CGenericList.AddHead (Wxlist.h) - parametro pList
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
ms.openlocfilehash: c26667ce12af902f3d5cf355a6556dc95e5dd1f5e0cad77f944e663eeef8ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656147"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>Metodo CGenericList.AddHead (Wxlist.h) - parametro pList

Il `AddHead` metodo aggiunge un elenco all'inizio dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Plist* 
</dt> <dd>

Puntatore all'elenco di elementi da aggiungere.

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

 

 




