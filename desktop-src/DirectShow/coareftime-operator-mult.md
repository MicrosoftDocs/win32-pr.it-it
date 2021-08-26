---
description: Questo operatore moltiplica un'ora di riferimento per un valore.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Metodo COARefTime.operator* (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57060f3b0436422c34ba947c0025cc6796d534e16ff64be029e68ab140faa4af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079351"
---
# <a name="coareftimeoperator-method"></a>Metodo COARefTime.operator \*

Questo operatore moltiplica un'ora di riferimento per un valore.

## <a name="syntax"></a>Sintassi


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*l* 
</dt> <dd>

Moltiplicatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un nuovo **oggetto COARefTime** uguale al prodotto di questo oggetto e **a l**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




