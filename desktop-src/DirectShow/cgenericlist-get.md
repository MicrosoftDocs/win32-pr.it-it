---
description: Il metodo Get recupera l'elemento in corrispondenza della posizione specificata.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Metodo CGenericList. Get (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329811"
---
# <a name="cgenericlistget-method"></a>Metodo CGenericList. Get

Il `Get` metodo recupera l'elemento in corrispondenza della posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Indicatore di posizione per l'elemento da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a un oggetto di tipo **Object** (il tipo di modello).

## <a name="remarks"></a>Commenti

Se *pos* è **null**, il metodo restituisce **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




