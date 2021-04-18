---
description: Il metodo CanReconnectWhenActive esegue una query se il pin supporta la riconnessione dinamica.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Metodo CBasePin. CanReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330859"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>CBasePin. CanReconnectWhenActive, metodo

Il `CanReconnectWhenActive` metodo esegue una query se il pin supporta la riconnessione dinamica.

## <a name="syntax"></a>Sintassi


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che specifica se il PIN è in grado di riconnettersi dinamicamente. Se **true**, il pin può riconnettersi dinamicamente.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, è necessario arrestare un filtro prima di riconnettere i relativi pin. Se un pin supporta la riconnessione dinamica, tuttavia, può riconnettersi mentre il filtro è attivo. Per altre informazioni, vedere [creazione di grafici dinamici](dynamic-graph-building.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




