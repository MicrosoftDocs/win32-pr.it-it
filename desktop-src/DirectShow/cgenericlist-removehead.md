---
description: Il metodo RemoveHead rimuove il primo elemento nell'elenco.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Metodo CGenericList.RemoveHead (Wxlist.h)
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
ms.openlocfilehash: 7b374ad6a08aac039de3c7d54ee4403f240fdf6bf9839a5ea2554901de789f11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317751"
---
# <a name="cgenericlistremovehead-method"></a>Metodo CGenericList.RemoveHead

Il `RemoveHead` metodo rimuove il primo elemento nell'elenco.

## <a name="syntax"></a>Sintassi


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a un oggetto di tipo **OBJECT** (tipo di modello) o **NULL se** l'elenco è vuoto.

## <a name="remarks"></a>Commenti

Questo metodo elimina il nodo elenco, ma non l'elemento contenuto nel nodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




