---
description: "Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico. Questo metodo esegue l'override del Metodo CBasePin:: CheckMediaType."
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Metodo CRendererInputPin. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328629"
---
# <a name="crendererinputpincheckmediatype-method"></a>CRendererInputPin. CheckMediaType, metodo

Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico. Questo metodo esegue l'override del metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore a un oggetto del tipo di supporto che contiene il tipo di supporto proposto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




