---
description: Questo operatore divide un'ora di riferimento per un valore.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: Metodo COARefTime.operator/ (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ff5f23691a3c4c44fdb9b93006834913648391ed473cf84906dff3eb8afb21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566021"
---
# <a name="coareftimeoperator-method"></a>Metodo COARefTime.operator/

Questo operatore divide un'ora di riferimento per un valore.

## <a name="syntax"></a>Sintassi


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*l* 
</dt> <dd>

Divisore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un nuovo **oggetto COARefTime** uguale al quoziente di questo oggetto e **l .**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




