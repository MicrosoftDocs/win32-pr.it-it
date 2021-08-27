---
description: L'operatore REFERENCE \_ TIME() esegue il cast dell'oggetto a un tipo di dati REFERENCE \_ TIME.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Metodo REFERENCE_TIME CRefTime.operator (Reftime.h)
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
ms.openlocfilehash: 9a084d4e142f57b724343ac5a353461b41aac0be216b8e3851bc8b7e40000a1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108031"
---
# <a name="creftimeoperator-reference_time-method"></a>Metodo CRefTime.operator REFERENCE \_ TIME

`REFERENCE_TIME()`L'operatore esegue il cast dell'oggetto a un [**tipo di dati REFERENCE \_ TIME.**](reference-time.md)

## <a name="syntax"></a>Sintassi


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore di [**CRefTime::m \_ time**](creftime-m-time.md).

## <a name="remarks"></a>Commenti

L'esempio seguente illustra come usare questo operatore cast:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Reftime.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




