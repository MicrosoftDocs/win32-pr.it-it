---
description: Il metodo AlignDown tronca un valore a un limite di allineamento specificato.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Metodo CPullPin.AlignDown (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdf16f3759bb7637fa243ce98bc4886b65e31d25bf62f5e9f581064d3741ea1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585351"
---
# <a name="cpullpinaligndown-method"></a>Metodo CPullPin.AlignDown

Il `AlignDown` metodo tronca un valore a un limite di allineamento specificato.

## <a name="syntax"></a>Sintassi


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ll* 
</dt> <dd>

Specifica il numero da allineare.

</dd> <dt>

*lAlign* 
</dt> <dd>

Specifica il limite di allineamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il risultato allineato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




