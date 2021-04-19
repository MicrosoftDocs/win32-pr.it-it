---
description: Il metodo IncrementTypeVersion incrementa il numero di versione nel set di tipi di supporto preferiti.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Metodo CBasePin. IncrementTypeVersion (Amfilter. h)
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
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332877"
---
# <a name="cbasepinincrementtypeversion-method"></a>CBasePin. IncrementTypeVersion, metodo

Il `IncrementTypeVersion` metodo incrementa il numero di versione nel set di tipi di supporto preferiti.

## <a name="syntax"></a>Sintassi


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo incrementa la variabile membro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) . Se il pin modifica in modo dinamico l'elenco dei tipi di supporto preferiti, chiamare questo metodo ogni volta che l'elenco viene modificato. Per ulteriori informazioni, vedere [**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




