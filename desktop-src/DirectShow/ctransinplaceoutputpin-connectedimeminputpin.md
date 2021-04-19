---
description: 'Il metodo ConnectedIMemInputPin recupera un puntatore al pin di input downstream. Questo metodo restituisce la variabile membro CBaseOutputPin:: m \_ pInputPin.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Metodo CTransInPlaceOutputPin. ConnectedIMemInputPin (Transip. h)
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
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326182"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a>CTransInPlaceOutputPin. ConnectedIMemInputPin, metodo

Il `ConnectedIMemInputPin` metodo recupera un puntatore al pin di input downstream. Questo metodo restituisce la variabile membro [**CBaseOutputPin:: m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) .

## <a name="syntax"></a>Sintassi


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sul pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




