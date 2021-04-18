---
description: Metodo del costruttore. Il costruttore ottiene l'accesso al pin specificato.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Costruttore CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331818"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>Costruttore CAutoUsingOutputPin. CAutoUsingOutputPin

Metodo del costruttore. Il costruttore ottiene l'accesso al pin specificato.

## <a name="syntax"></a>Sintassi


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOutputPin* 
</dt> <dd>

Puntatore a un oggetto [**CDynamicOutputPin**](cdynamicoutputpin.md) .

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che contiene un valore **HRESULT** . Il valore deve essere S \_ OK.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando il metodo restituisce, il valore di *\* PHR* indica l'esito positivo o negativo del metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




