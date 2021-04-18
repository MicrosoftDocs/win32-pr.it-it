---
description: Il metodo AlignDown tronca un valore in un limite di allineamento specificato.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Metodo CPullPin. AlignDown (Pullpin. h)
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
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328492"
---
# <a name="cpullpinaligndown-method"></a>CPullPin. AlignDown, metodo

Il `AlignDown` Metodo tronca un valore in un limite di allineamento specificato.

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
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




