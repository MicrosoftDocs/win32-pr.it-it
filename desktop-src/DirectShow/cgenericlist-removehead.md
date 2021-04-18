---
description: Il metodo RemoveHead rimuove il primo elemento nell'elenco.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Metodo CGenericList. RemoveHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329794"
---
# <a name="cgenericlistremovehead-method"></a>CGenericList. RemoveHead, metodo

Il `RemoveHead` metodo rimuove il primo elemento nell'elenco.

## <a name="syntax"></a>Sintassi


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a un oggetto di tipo **Object** (il tipo di modello) o **null** se l'elenco è vuoto.

## <a name="remarks"></a>Commenti

Questo metodo elimina il nodo elenco, ma non l'elemento contenuto nel nodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




