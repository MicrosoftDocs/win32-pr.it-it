---
description: Informazioni sul metodo costruttore per CGenericList.CGenericList (Wxlist.h). Questo metodo usa il parametro 'pName'.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Costruttore CGenericList.CGenericList (Wxlist.h) - parametro pName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 117138e80db91529d6a2baf93577a6a4dfd542d2975bf2ce6f89124a3d7aefe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813841"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>Costruttore CGenericList.CGenericList (Wxlist.h) - parametro pName

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore al nome dell'elenco.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per migliorare l'efficienza, `CGenericList` la classe gestisce una cache di nodi elenco. Questa versione del costruttore usa le dimensioni predefinite della cache.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist.h (includere Flussi.h) |
| Libreria| Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




