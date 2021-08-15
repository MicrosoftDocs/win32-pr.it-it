---
description: Il metodo AddBefore inserisce un elenco prima della posizione specificata. Questo metodo usa i parametri 'pos' e 'pList'.
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Metodo CGenericList.AddBefore (Wxlist.h) - parametri pos, pList
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
ms.openlocfilehash: 6f05d67477bb7e6c89eddfe0a68ad47d83760762fc68cddf6f73c731886f88d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697451"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>Metodo CGenericList.AddBefore (Wxlist.h) - parametri pos, pList

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

*Plist* 
</dt> <dd>

Puntatore all'elenco da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo. In caso contrario, **restituisce FALSE.**

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist.h (includere Flussi.h) |
| Libreria| Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




