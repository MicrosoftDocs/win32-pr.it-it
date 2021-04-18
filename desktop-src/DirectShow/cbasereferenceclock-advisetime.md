---
description: 'Il metodo AdviseTime crea una richiesta di notifica di un solo tentativo. Questo metodo implementa il metodo IReferenceClock:: AdviseTime.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Metodo CBaseReferenceClock. AdviseTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330307"
---
# <a name="cbasereferenceclockadvisetime-method"></a>CBaseReferenceClock. AdviseTime, metodo

Il `AdviseTime` metodo crea una richiesta di notifica di un solo tentativo. Questo metodo implementa il metodo [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*baseTime* 
</dt> <dd>

Tempo di riferimento di base, in unità 100-nanosecondi.

</dd> <dt>

*streamTime* 
</dt> <dd>

Tempo di offset del flusso, in unità di 100 nanosecondi.

</dd> <dt>

*hEvent* 
</dt> <dd>

Handle per un evento, creato dal chiamante.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Puntatore a una variabile che riceve un identificatore per la richiesta di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valori di ora non validi<br/>       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Errore<br/>                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null**<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo crea una richiesta di notifica monouso per l'ora di riferimento *baseTime*  +  *streamTime*. La somma deve essere maggiore di zero e minore del \_ tempo massimo oppure il metodo restituisce e \_ INVALIDARG. Al momento richiesto, l'orologio segnala l'evento specificato nel parametro *hEvent* .

Per annullare la notifica prima del raggiungimento dell'ora, chiamare il metodo [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) e passare il valore *pdwAdviseToken* restituito dalla chiamata. Dopo che si è verificata la notifica, il clock lo cancella automaticamente, pertanto non è necessario chiamare **Unadvise**. Tuttavia, non si tratta di un errore a tale scopo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




