---
description: 'Il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi, fino a quando non viene emesso un nuovo comando Run nel filtro. Questo metodo implementa il metodo IPin:: EndOfStream.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Metodo CRenderedInputPin. EndOfStream (Amextra. h)
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
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329365"
---
# <a name="crenderedinputpinendofstream-method"></a>CRenderedInputPin. EndOfStream, metodo

Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi, fino a quando non viene emesso un nuovo comando Run nel filtro. Questo metodo implementa il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se l'esito è positivo o un codice di errore.

## <a name="remarks"></a>Commenti

Se il filtro è in esecuzione, questo metodo invia un evento [**EC \_ complete**](ec-complete.md) al gestore del grafico dei filtri. In caso contrario, viene impostato un flag in modo che l' \_ evento di completamento EC venga inviato al successivo esecuzione del filtro. Lo svuotamento del filtro Cancella il flag.

È necessario eseguire l'override di questo metodo per mantenere il blocco di streaming del PIN:


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



Se, inoltre, il filtro elabora **le chiamate in** modo asincrono, il PIN deve attendere l'invio dell'evento di completamento EC fino a \_ quando il filtro non ha elaborato tutti gli esempi in sospeso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amextra. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




