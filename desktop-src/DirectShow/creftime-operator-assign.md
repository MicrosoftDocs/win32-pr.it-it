---
description: L'operatore = assegna una nuova ora di riferimento.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: Metodo CRefTime. Operator = (Reftime. h)
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
ms.openlocfilehash: b87e6517946c64cb2a60e95912aba423a1880215
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331458"
---
# <a name="creftimeoperator-method-reftimeh"></a>Metodo CRefTime. Operator = (Reftime. h)

L'operatore = assegna una nuova ora di riferimento.

## <a name="syntax"></a>Sintassi


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RT* \[ Ref\]
</dt> <dd>

Riferimento a un oggetto **CRefTime** che specifica la nuova ora di riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un riferimento all'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Reftime. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




