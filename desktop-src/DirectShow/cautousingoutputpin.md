---
description: La classe CAutoUsingOutputPin ottiene e rilascia l'accesso a un oggetto CDynamicOutputPin.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Classe CAutoUsingOutputPin (Amfilter.h)
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
ms.openlocfilehash: 141c65507a0d983a2b4531b93617ed741e7403b8b2a5ead9c196f78dcf61acdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955380"
---
# <a name="cautousingoutputpin-class"></a>Classe CAutoUsingOutputPin

La **classe CAutoUsingOutputPin** ottiene e rilascia l'accesso a un [**oggetto CDynamicOutputPin.**](cdynamicoutputpin.md)

**CAutoUsingOutputPin** ha questi tipi di membri:



| Metodi pubblici                                                           | Descrizione                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)   | Metodo del costruttore. Ottiene l'accesso al pin specificato. |
| [**~CAutoUsingOutputPin**](cautousingoutputpin--cautousingoutputpin.md) | Metodo del distruttore. Ottiene l'accesso al pin specificato.  |



 

## <a name="remarks"></a>Commenti

Quando alcuni metodi vengono chiamati in [**CDynamicOutputPin,**](cdynamicoutputpin.md)il chiamante deve ottenere l'accesso al pin e quindi rilasciare l'accesso. Per ottenere l'accesso, il chiamante usa il [**metodo CDynamicOutputPin::StartUsingOutputPin.**](cdynamicoutputpin-startusingoutputpin.md) Per rilasciare l'accesso, chiama [**il metodo CDynamicOutputPin::StopUsingOutputPin.**](cdynamicoutputpin-stopusingoutputpin.md) La **classe CAutoUsingOutputPin** è una classe helper che gestisce queste attività nei metodi costruttore e distruttore. Nell'esempio di codice seguente viene illustrato come utilizzare questa classe:


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
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento sulla classe base](base-class-reference.md)
</dt> </dl>

 

 




