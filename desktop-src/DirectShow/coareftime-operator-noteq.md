---
description: Questo operatore verifica la disuguaglianza tra due tempi di riferimento.
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: Metodo COARefTime. Operator! = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e93934d7b31715422f2cc091e606b681a57e7f61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330291"
---
# <a name="coareftimeoperator-method"></a>Metodo COARefTime. operator! =

Questo operatore verifica la disuguaglianza tra due tempi di riferimento.

## <a name="syntax"></a>Sintassi


```C++
BOOL operator!=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RT* \[ Ref\]
</dt> <dd>

Riferimento all'oggetto **COARefTime** da confrontare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se i due oggetti non sono uguali. In caso contrario, restituisce **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




