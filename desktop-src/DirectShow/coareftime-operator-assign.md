---
description: Questo operatore assegna una nuova ora di riferimento.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: Metodo COARefTime.operator= (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31784a008a2074156c69abf868739ec27c459dabdba1437397780086d28f9847
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084461"
---
# <a name="coareftimeoperator-method-ctlutilh"></a>Metodo COARefTime.operator= (Ctlutil.h)

Questo operatore assegna una nuova ora di riferimento.

## <a name="syntax"></a>Sintassi


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rd* \[ Ref\]
</dt> <dd>

Riferimento a un **valore double** che specifica il nuovo tempo di riferimento in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un riferimento all'oggetto .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




