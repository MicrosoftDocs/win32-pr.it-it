---
description: Il metodo successivo recupera la posizione successiva nell'elenco.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Metodo CBaseList. Next (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328647"
---
# <a name="cbaselistnext-method"></a>Metodo CBaseList. Next

Il `Next` metodo recupera la posizione successiva nell'elenco.

## <a name="syntax"></a>Sintassi


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Valore della posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indicatore di posizione che segue la posizione specificata da *pos*.

## <a name="remarks"></a>Commenti

Se *pos* è l'ultima posizione nell'elenco, il metodo restituisce **null**. Se *pos* è **null**, il metodo restituisce la prima posizione nell'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




