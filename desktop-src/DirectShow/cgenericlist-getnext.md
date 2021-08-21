---
description: Il metodo GetNext recupera l'elemento nella posizione specificata e fa avanzare la posizione.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Metodo CGenericList.GetNext (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f116dd1a965145e5bdf4808d25a7406b4709967c5cf971ad3529ae9d301ebc4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539741"
---
# <a name="cgenericlistgetnext-method"></a>Metodo CGenericList.GetNext

Il `GetNext` metodo recupera l'elemento nella posizione specificata e fa avanzare la posizione.

## <a name="syntax"></a>Sintassi


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rp* \[ Ref\]
</dt> <dd>

Riferimento a un valore POSITION.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a un oggetto di tipo **OBJECT** (il tipo di modello).

## <a name="remarks"></a>Commenti

Questo metodo sposta l'indicatore di posizione alla posizione successiva. Se l'indicatore di posizione si sposta oltre la fine dell'elenco, il metodo lo imposta su **NULL.**

Se *rp* è **NULL,** il metodo restituisce **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




