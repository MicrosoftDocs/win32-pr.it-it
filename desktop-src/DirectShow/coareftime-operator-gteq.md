---
description: Questo operatore verifica se un'ora di riferimento è minore o uguale a un'altra.
ms.assetid: ae7449b7-d319-4e76-892f-0f9ae63ddf94
title: Metodo COARefTime.operator>= (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6d19686fc2c904534f66882172db6bec52b4873a36104ce78d2d826a771978d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108471"
---
# <a name="coareftimeoperator-method"></a>Metodo COARefTime.operator>=

Questo operatore verifica se un'ora di riferimento è minore o uguale a un'altra.

## <a name="syntax"></a>Sintassi


```C++
BOOL operator>=(
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

Restituisce **TRUE** se questo oggetto è minore o uguale a *rt*. In caso contrario, restituisce **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




