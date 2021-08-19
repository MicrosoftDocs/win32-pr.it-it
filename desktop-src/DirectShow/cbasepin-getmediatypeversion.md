---
description: Il metodo GetMediaTypeVersion recupera un numero di versione per il set di tipi di supporti preferiti.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Metodo CBasePin.GetMediaTypeVersion (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f1b50b16a099c8698bbf5bef270173334f1c3ac2c3d2d67ff87778cffddf2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955190"
---
# <a name="cbasepingetmediatypeversion-method"></a>Metodo CBasePin.GetMediaTypeVersion

Il `GetMediaTypeVersion` metodo recupera un numero di versione per il set di tipi di supporti preferiti.

## <a name="syntax"></a>Sintassi


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la [**variabile membro CBasePin::m \_ TypeVersion.**](cbasepin-m-typeversion.md)

## <a name="remarks"></a>Commenti

Il **costruttore CBasePin** inizializza il numero di versione su 1. Nella classe di base questo numero non cambia mai. Se il segnaposto modifica dinamicamente l'elenco dei tipi di supporti preferiti, deve incrementare il numero di versione ogni volta che l'elenco cambia. Per incrementare il numero di versione, chiamare il [**metodo CBasePin::IncrementTypeVersion.**](cbasepin-incrementtypeversion.md)

L'enumeratore del tipo di supporto, implementato dalla [**classe CEnumMediaTypes,**](cenummediatypes.md) usa il numero di versione per mantenersi sincronizzato con il pin.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




