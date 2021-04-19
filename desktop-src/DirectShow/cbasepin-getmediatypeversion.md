---
description: Il metodo GetMediaTypeVersion recupera un numero di versione per il set di tipi di supporto preferiti.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Metodo CBasePin. GetMediaTypeVersion (Amfilter. h)
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
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333604"
---
# <a name="cbasepingetmediatypeversion-method"></a>CBasePin. GetMediaTypeVersion, metodo

Il `GetMediaTypeVersion` metodo recupera un numero di versione per il set di tipi di supporto preferiti.

## <a name="syntax"></a>Sintassi


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la variabile membro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) .

## <a name="remarks"></a>Commenti

Il costruttore **CBasePin** Inizializza il numero di versione su 1. Nella classe base questo numero non viene mai modificato. Se il pin modifica dinamicamente l'elenco dei tipi di supporto preferiti, deve incrementare il numero di versione ogni volta che l'elenco viene modificato. Per incrementare il numero di versione, chiamare il metodo [**CBasePin:: IncrementTypeVersion**](cbasepin-incrementtypeversion.md) .

L'enumeratore Media Type, implementato dalla classe [**CEnumMediaTypes**](cenummediatypes.md) , usa il numero di versione per mantenersi sincronizzato con il PIN.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




