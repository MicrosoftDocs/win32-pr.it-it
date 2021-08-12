---
description: Il metodo Next recupera la posizione successiva nell'elenco.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Metodo CBaseList.Next (Wxlist.h)
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
ms.openlocfilehash: d07030c046f3fe55178707af297542f383bfd5cf75f40169b5c93cfafa1c698b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658957"
---
# <a name="cbaselistnext-method"></a>Metodo CBaseList.Next

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

Valore POSITION.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indicatore di posizione che segue la posizione specificata da *pos*.

## <a name="remarks"></a>Commenti

Se *pos* è l'ultima posizione nell'elenco, il metodo restituisce **NULL.** Se *pos* è **NULL,** il metodo restituisce la prima posizione nell'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




