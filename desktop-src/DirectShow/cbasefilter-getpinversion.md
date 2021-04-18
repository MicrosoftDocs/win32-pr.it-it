---
description: Il metodo GetPinVersion recupera un numero di versione per il set di pin in questo filtro.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Metodo CBaseFilter. GetPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331549"
---
# <a name="cbasefiltergetpinversion-method"></a>CBaseFilter. GetPinVersion, metodo

Il `GetPinVersion` metodo recupera un numero di versione per il set di pin in questo filtro.

## <a name="syntax"></a>Sintassi


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la variabile membro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) .

## <a name="remarks"></a>Commenti

Il costruttore **CBaseFilter** Inizializza la versione del pin su 1. Nella classe base questo numero non viene mai modificato. Se il filtro crea o Elimina in modo dinamico i pin, è necessario incrementare la versione del PIN ogni volta che i pin cambiano. Per incrementare il numero di versione, chiamare il metodo [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .

L'oggetto enumeratore pin, implementato dalla classe [**CEnumPins**](cenumpins.md) , usa la versione pin per mantenersi sincronizzata con il filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




