---
description: Il metodo SetMediaType imposta il tipo di supporto per la connessione. Questo metodo esegue l'override del metodo CBasePin::SetMediaType.
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Metodo CRendererInputPin.SetMediaType (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f248e15c3965305719269a19a1f2ff2c8feddfe0e57b6349985d9133e38789
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054401"
---
# <a name="crendererinputpinsetmediatype-method"></a>Metodo CRendererInputPin.SetMediaType

Il `SetMediaType` metodo imposta il tipo di supporto per la connessione. Questo metodo esegue l'override [**del metodo CBasePin::SetMediaType.**](cbasepin-setmediatype.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




