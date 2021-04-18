---
description: Il metodo SetReconnectWhenActive specifica se il pin supporta la riconnessione dinamica.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Metodo CBasePin. SetReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324201"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a>CBasePin. SetReconnectWhenActive, metodo

Il `SetReconnectWhenActive` metodo specifica se il pin supporta la riconnessione dinamica.

## <a name="syntax"></a>Sintassi


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bCanReconnect* 
</dt> <dd>

Valore booleano che specifica se il pin può riconnettersi dinamicamente. Se **true**, il pin può riconnettersi dinamicamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, è necessario arrestare un filtro prima di riconnettere i relativi pin. Se il PIN è in grado di riconnettersi mentre il filtro è attivo, chiamare questo metodo con un valore **true**. Per altre informazioni, vedere [creazione di grafici dinamici](dynamic-graph-building.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




