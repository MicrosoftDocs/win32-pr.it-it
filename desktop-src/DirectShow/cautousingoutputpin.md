---
description: La classe CAutoUsingOutputPin ottiene e rilascia l'accesso a un oggetto CDynamicOutputPin.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Classe CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331820"
---
# <a name="cautousingoutputpin-class"></a>Classe CAutoUsingOutputPin

La classe **CAutoUsingOutputPin** ottiene e rilascia l'accesso a un oggetto [**CDynamicOutputPin**](cdynamicoutputpin.md) .

**CAutoUsingOutputPin** dispone di questi tipi di membri:



| Metodi pubblici                                                           | Descrizione                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)   | Metodo del costruttore. Ottiene l'accesso al pin specificato. |
| [**~ CAutoUsingOutputPin**](cautousingoutputpin--cautousingoutputpin.md) | Metodo del distruttore. Ottiene l'accesso al pin specificato.  |



 

## <a name="remarks"></a>Commenti

Quando vengono chiamati determinati metodi su [**CDynamicOutputPin**](cdynamicoutputpin.md), il chiamante deve ottenere l'accesso al pin e quindi rilasciare tale accesso. Per ottenere l'accesso, il chiamante usa il metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) . Per rilasciare l'accesso, viene chiamato il metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) . La classe **CAutoUsingOutputPin** è una classe helper che gestisce queste attività nei relativi metodi di costruttore e distruttore. Nell'esempio di codice seguente viene illustrato come utilizzare questa classe:


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento alla classe di base](base-class-reference.md)
</dt> </dl>

 

 




