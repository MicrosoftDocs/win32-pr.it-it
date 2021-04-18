---
description: Il metodo getnexti recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Metodo CBaseList. getnexto (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328659"
---
# <a name="cbaselistgetnexti-method"></a>CBaseList. getnexti (metodo)

Il `GetNextI` metodo recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.

## <a name="syntax"></a>Sintassi


```C++
void* GetNextI(
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

Restituisce un puntatore all'elemento. Se *RP* è **null**, il metodo restituisce **null**.

## <a name="remarks"></a>Commenti

Questo metodo sposta l'indicatore di posizione nella posizione successiva. Se l'indicatore di posizione si sposta oltre la fine dell'elenco, il metodo lo imposta su **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




