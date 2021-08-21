---
description: Il metodo ConnectedIMemInputPin recupera un puntatore al pin di input downstream. Questo metodo restituisce la variabile membro CBaseOutputPin::m \_ pInputPin.
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Metodo CTransInPlaceOutputPin.ConnectedIMemInputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 180cce9bc0d52c6e11bbd90b64cfe7d57d4dcc99eada3a794f924df6857c4698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076181"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a>Metodo CTransInPlaceOutputPin.ConnectedIMemInputPin

Il `ConnectedIMemInputPin` metodo recupera un puntatore al pin di input downstream. Questo metodo restituisce la [**variabile membro CBaseOutputPin::m \_ pInputPin.**](cbaseoutputpin-m-pinputpin.md)

## <a name="syntax"></a>Sintassi


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore [**all'interfaccia IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sul pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




