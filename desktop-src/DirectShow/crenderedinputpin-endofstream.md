---
description: Il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi, fino a quando non viene eseguito un nuovo comando run per il filtro. Questo metodo implementa il metodo IPin::EndOfStream.
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Metodo CRenderedInputPin.EndOfStream (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26f7a5075e06a3943978a8e938f034fbabcaddfa31c9ffa2a2b37d33a0120640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107991"
---
# <a name="crenderedinputpinendofstream-method"></a>Metodo CRenderedInputPin.EndOfStream

Il metodo notifica al pin che non sono previsti dati aggiuntivi, fino a quando non viene eseguito un nuovo comando `EndOfStream` run per il filtro. Questo metodo implementa il [**metodo IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

Se il filtro è in esecuzione, questo metodo invia un evento [**EC \_ COMPLETE**](ec-complete.md) a Filter Graph Manager. In caso contrario, viene impostato un flag in modo che l'evento EC \_ COMPLETE venga inviato alla successiva esecuzione del filtro. Lo scaricamento del filtro cancella il flag.

È necessario eseguire l'override di questo metodo per contenere il blocco di streaming del pin:


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



Inoltre, se il filtro elabora le chiamate **Receive** in modo asincrono, il pin deve attendere l'invio dell'evento EC COMPLETE fino a quando il filtro \_ non ha elaborato tutti i campioni in sospeso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amextra.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




