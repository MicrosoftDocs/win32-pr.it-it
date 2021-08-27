---
description: L'operatore = assegna una nuova ora di riferimento.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: Metodo CRefTime.operator= (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4fe9a8f6f40dd1d0a7b0e38339c3ab21c44a989648e6c032b17a0ed3ac3b4f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108071"
---
# <a name="creftimeoperator-method-reftimeh"></a>Metodo CRefTime.operator= (Reftime.h)

L'operatore = assegna una nuova ora di riferimento.

## <a name="syntax"></a>Sintassi


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Riferimento a un **oggetto CRefTime** che specifica la nuova ora di riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un riferimento all'oggetto .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Reftime.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




