---
description: Metodo del costruttore. Il costruttore ottiene l'accesso al pin specificato.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Costruttore CAutoUsingOutputPin.CAutoUsingOutputPin (Amfilter.h)
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
ms.openlocfilehash: c0594eed7f253f7e540f843dfc3c3de6481d7dbede3f25d1534e52181ef0585b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057521"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>Costruttore CAutoUsingOutputPin.CAutoUsingOutputPin

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

Puntatore a [**un oggetto CDynamicOutputPin.**](cdynamicoutputpin.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che contiene un **valore HRESULT.** Il valore deve essere S \_ OK.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando il metodo viene restituito, il valore *\* di phr* indica l'esito positivo o negativo del metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




