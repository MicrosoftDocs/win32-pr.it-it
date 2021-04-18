---
description: L'operatore-= sottrae un'ora di riferimento da un'altra.
ms.assetid: 5b0ec72e-87d8-4562-96b1-40e4f5036fd4
title: Metodo CRefTime. Operator-= (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bf66abe11d5c61edbb70118020d882c82b08847
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329048"
---
# <a name="creftimeoperator--method"></a>Metodo CRefTime. operator-=

L'operatore-= sottrae un'ora di riferimento da un'altra.

## <a name="syntax"></a>Sintassi


```C++
CRefTime& operator-=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RT* \[ Ref\]
</dt> <dd>

Riferimento a un oggetto **CRefTime** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un riferimento all'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Reftime. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




