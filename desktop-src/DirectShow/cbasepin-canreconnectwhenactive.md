---
description: Il metodo CanReconnectWhenActive esegue una query se il pin supporta riconnessioni dinamiche.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Metodo CBasePin.CanReconnectWhenActive (Amfilter.h)
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
ms.openlocfilehash: ffe4cc09efa53ac4d3ab8089a1061d860206f9734c214d250b5c3cdc907eaf84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916921"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>Metodo CBasePin.CanReconnectWhenActive

Il `CanReconnectWhenActive` metodo esegue una query se il pin supporta riconnessioni dinamiche.

## <a name="syntax"></a>Sintassi


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che specifica se il pin può riconnettersi dinamicamente. Se **TRUE,** il pin può riconnettersi dinamicamente.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, è necessario arrestare un filtro prima di riconnettersi a uno dei relativi pin. Se un pin supporta la riconnessione dinamica, tuttavia, può riconnettersi mentre il filtro è attivo. Per altre informazioni, vedere [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




