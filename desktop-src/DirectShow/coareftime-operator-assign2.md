---
description: L'operatore assegna una nuova ora di riferimento e usa il parametro 'rt [ref]'.
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: Metodo COARefTime.operator= (Ctlutil.h) - rt [ref] parameter
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
ms.openlocfilehash: e1a1e4c9482c187db7d5d5377535763b9fbab126b2153e0efa56bc341b402b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103161"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a>Metodo COARefTime.operator= (Ctlutil.h) - rt [ref] parameter

Questo operatore assegna una nuova ora di riferimento.

## <a name="syntax"></a>Sintassi


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Riferimento a un [**valore REFERENCE \_ TIME**](reference-time.md) che specifica il nuovo tempo di riferimento in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un riferimento all'oggetto .

## <a name="requirements"></a>Requisiti

| Requisito                    | Valore                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Ctlutil.h (includere Flussi.h)                                                                                   |
| Libreria | Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




