---
description: Il metodo UnblockOutputPin Sblocca il PIN. Quando il PIN viene sbloccato, può fornire esempi, modificare il formato di output e riconnettersi.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Metodo CDynamicOutputPin. UnblockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331645"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a>CDynamicOutputPin. UnblockOutputPin, metodo

Il `UnblockOutputPin` metodo sblocca il PIN. Quando il PIN viene sbloccato, può fornire esempi, modificare il formato di output e riconnettersi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il PIN è già stato sbloccato.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




