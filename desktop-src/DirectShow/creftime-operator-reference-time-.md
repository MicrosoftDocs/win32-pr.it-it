---
description: L' \_ operatore time () di riferimento esegue il cast dell'oggetto a un \_ tipo di dati time di riferimento.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Metodo CRefTime. operator REFERENCE_TIME (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329046"
---
# <a name="creftimeoperator-reference_time-method"></a>Metodo time di riferimento CRefTime. Operator \_

L' `REFERENCE_TIME()` operatore esegue il cast dell'oggetto a un tipo di dati [**\_ time di riferimento**](reference-time.md) .

## <a name="syntax"></a>Sintassi


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore di [**CRefTime:: m \_ Time**](creftime-m-time.md).

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrato come utilizzare questo operatore cast:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Reftime. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




