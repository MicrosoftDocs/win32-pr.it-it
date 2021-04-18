---
description: L'operatore = assegna una nuova ora di riferimento. Questo metodo usa il parametro *ll* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: Metodo CRefTime. Operator = (Reftime. h)-ll parametro
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
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334344"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a>Metodo CRefTime. Operator = (Reftime. h)-ll parametro

L'operatore = assegna una nuova ora di riferimento.

## <a name="syntax"></a>Sintassi


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ll* 
</dt> <dd>

Nuova ora di riferimento, in unità 100-nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un riferimento all'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Reftime. h (include Streams. h)                                                                                   |
| Libreria | Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |



 

 




