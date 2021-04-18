---
description: Restituisce FALSE se il thread corrente è il proprietario della sezione critica specificata.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Funzione CritCheckOut (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327189"
---
# <a name="critcheckout-function"></a>CritCheckOut (funzione)

Restituisce **false** se il thread corrente è il proprietario della sezione critica specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcCrit* 
</dt> <dd>

Puntatore a una sezione critica [**CCritSec**](ccritsec.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nelle build di debug, restituisce **false** se il thread corrente è il proprietario di questa sezione critica o **true** in caso contrario. Nelle compilazioni finali restituisce sempre **true**.

## <a name="remarks"></a>Commenti

Questa funzione è l'inverso della funzione [**CritCheckIn**](critcheckin.md) . Se **CritCheckIn** restituisce **true**, **CritCheckOut** restituisce **false** e viceversa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di debug della sezione critica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




