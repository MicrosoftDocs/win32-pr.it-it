---
description: Questo operatore sottrae un'ora di riferimento da un'altra.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: Metodo COARefTime. Operator-(Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327542"
---
# <a name="coareftimeoperator--method"></a>COARefTime. Operator-(metodo)

Questo operatore sottrae un'ora di riferimento da un'altra.

## <a name="syntax"></a>Sintassi


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RT* \[ Ref\]
</dt> <dd>

Riferimento all'oggetto **COARefTime** da sottrarre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un nuovo oggetto **COARefTime** uguale alla differenza dei tempi di riferimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




