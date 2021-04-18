---
description: Il metodo AddTail Accoda un elenco alla fine dell'elenco.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: Metodo CGenericList. AddTail (Wxlist. h)-parametro pList
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
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323798"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a>Metodo CGenericList. AddTail (Wxlist. h)-parametro pList

Il `AddTail` Metodo Accoda un elenco alla fine dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pList* 
</dt> <dd>

Puntatore all'elenco da accodare.

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

 

 




