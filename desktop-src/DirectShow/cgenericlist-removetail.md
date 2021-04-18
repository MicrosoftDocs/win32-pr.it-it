---
description: Il metodo RemoveTail rimuove l'ultimo elemento dell'elenco.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Metodo CGenericList. RemoveTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329793"
---
# <a name="cgenericlistremovetail-method"></a>CGenericList. RemoveTail, metodo

Il `RemoveTail` metodo rimuove l'ultimo elemento dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
OBJECT* RemoveTail();
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

 

 




