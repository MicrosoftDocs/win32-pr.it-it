---
description: Questo operatore moltiplica un'ora di riferimento per un valore.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Metodo COARefTime. Operator * (Ctlutil. h)
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
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330293"
---
# <a name="coareftimeoperator-method"></a>Metodo COARefTime. Operator \*

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

Restituisce un nuovo oggetto **COARefTime** uguale al prodotto di questo oggetto e **l**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




