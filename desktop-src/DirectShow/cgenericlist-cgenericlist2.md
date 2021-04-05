---
description: Informazioni sul metodo del costruttore per CGenericList. CGenericList (Wxlist. h). Questo metodo usa il parametro ' pName '.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Costruttore CGenericList. CGenericList (Wxlist. h)-parametro pName
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
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103886336"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>Costruttore CGenericList. CGenericList (Wxlist. h)-parametro pName

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* 
</dt> <dd>

Puntatore al nome dell'elenco.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per migliorare l'efficienza, la `CGenericList` classe mantiene una cache di nodi elenco. Questa versione del costruttore usa una dimensione della cache predefinita.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




