---
description: 'Metodo CBaseRenderer.GetPin: il metodo GetPin recupera un pin.'
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Metodo CBaseRenderer.GetPin (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c85b1a33abec4dfd10cf093e8673e270e7df02533846791a5d5d37702b51313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822702"
---
# <a name="cbaserenderergetpin-method"></a>Metodo CBaseRenderer.GetPin

Il `GetPin` metodo recupera un segnaposto.

## <a name="syntax"></a>Sintassi


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Numero del pin specificato. Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il [**puntatore \_ pInputPin CBaseRenderer::m.**](cbaserenderer-m-pinputpin.md)

## <a name="remarks"></a>Commenti

Questo metodo implementa il [**metodo CBaseFilter::GetPin,**](cbasefilter-getpin.md) che è virtuale puro nella **classe CBaseFilter.** Il filtro supporta esattamente un pin (pin di input). La prima volta che questo metodo viene chiamato, crea il segnaposto come nuovo [**oggetto CRendererInputPin.**](crendererinputpin.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




