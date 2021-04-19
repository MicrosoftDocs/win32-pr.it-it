---
description: Il metodo GetNext recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Metodo CGenericList. GetNext (Wxlist. h)
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
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329800"
---
# <a name="cgenericlistgetnext-method"></a>Metodo CGenericList. GetNext

Il `GetNext` metodo recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.

## <a name="syntax"></a>Sintassi


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*componente* \[ di Ref\]
</dt> <dd>

Riferimento a un valore di posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a un oggetto di tipo **Object** (il tipo di modello).

## <a name="remarks"></a>Commenti

Questo metodo sposta l'indicatore di posizione nella posizione successiva. Se l'indicatore di posizione si sposta oltre la fine dell'elenco, il metodo lo imposta su **null**.

Se *RP* è **null**, il metodo restituisce **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




