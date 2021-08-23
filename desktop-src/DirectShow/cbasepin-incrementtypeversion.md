---
description: Il metodo IncrementTypeVersion incrementa il numero di versione nel set di tipi di supporti preferiti.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Metodo CBasePin.IncrementTypeVersion (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a8c2536b91d5630141e5a62fa1aa895555537b61f89a574f4cdc1ec208810c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526861"
---
# <a name="cbasepinincrementtypeversion-method"></a>Metodo CBasePin.IncrementTypeVersion

Il `IncrementTypeVersion` metodo incrementa il numero di versione nel set di tipi di supporti preferiti.

## <a name="syntax"></a>Sintassi


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo incrementa la [**variabile membro CBasePin::m \_ TypeVersion.**](cbasepin-m-typeversion.md) Se il segnaposto modifica dinamicamente l'elenco dei tipi di supporti preferiti, chiamare questo metodo ogni volta che l'elenco viene modificato. Per altre informazioni, vedere [**CBasePin::GetMediaTypeVersion.**](cbasepin-getmediatypeversion.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




