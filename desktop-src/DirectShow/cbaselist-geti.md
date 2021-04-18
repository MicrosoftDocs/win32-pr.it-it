---
description: Il metodo GetI recupera l'elemento in corrispondenza della posizione specificata.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Metodo CBaseList. GetI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2473401aeaee201456b4eede39ffb492f40ee2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328661"
---
# <a name="cbaselistgeti-method"></a>CBaseList. GetI, metodo

Il `GetI` metodo recupera l'elemento in corrispondenza della posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
void* GetI(
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

Restituisce un puntatore all'elemento.

## <a name="remarks"></a>Commenti

Se *pos* è **null**, il metodo restituisce **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




