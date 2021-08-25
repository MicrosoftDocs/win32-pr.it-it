---
description: Il metodo AddAfter inserisce un elemento dopo la posizione specificata e usa i parametri 'p' e 'pObj'.
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Metodo CGenericList.AddAfter (Wxlist.h) - p, pObj parameters
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
ms.openlocfilehash: 6de0037d76e63049294b0455c8ec1fbac82963d94febb35f7c9400ec8eae9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697531"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>Metodo CGenericList.AddAfter (Wxlist.h) - p, pObj parameters

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

*P* 
</dt> <dd>

Posizione dopo la quale aggiungere l'elemento. Se *p* è **NULL,** il metodo aggiunge l'elemento all'inizio dell'elenco.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntatore a un oggetto di tipo **OBJECT** (tipo di modello).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indicatore di posizione dell'elemento inserito.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist.h (includere Flussi.h) |
| Libreria| Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




