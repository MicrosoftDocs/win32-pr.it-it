---
description: Questo operatore verifica se un'ora di riferimento è maggiore o uguale a un'altra.
ms.assetid: 1182db5b-2d58-4abb-b9ec-f14c3de5a942
title: Metodo COARefTime.operator<= (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 448f36a9c746c22878d8bb0e48028dff211962cbf49827eab3c14f2b4af6b38c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087281"
---
# <a name="coareftimeoperator-method"></a>Metodo COARefTime.operator<=

Questo operatore verifica se un'ora di riferimento è maggiore o uguale a un'altra.

## <a name="syntax"></a>Sintassi


```C++
BOOL operator<=(
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

Restituisce **TRUE** se questo oggetto è maggiore o uguale a *rt*. In caso contrario, restituisce **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




