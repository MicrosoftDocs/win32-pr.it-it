---
description: Questo operatore verifica la disuguaglianza tra due tempi di riferimento.
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: Metodo COARefTime.operator!= (Ctlutil.h)
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
ms.openlocfilehash: 86e138eecf387cf85bf57776f05e6e2711f58883e92a02cac83c4d2e8b1ebe19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954350"
---
# <a name="coareftimeoperator-method"></a>Metodo COARefTime.operator!=

Questo operatore verifica la disuguaglianza tra due tempi di riferimento.

## <a name="syntax"></a>Sintassi


```C++
BOOL operator!=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Riferimento **all'oggetto COARefTime** da confrontare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se i due oggetti non sono uguali. In caso contrario, **restituisce FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




