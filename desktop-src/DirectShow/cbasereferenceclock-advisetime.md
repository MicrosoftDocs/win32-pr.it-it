---
description: Il metodo AdviseTime crea una richiesta di consulenza in un'unica operazione. Questo metodo implementa il metodo IReferenceClock::AdviseTime.
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Metodo CBaseReferenceClock.AdviseTime (Refclock.h)
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
ms.openlocfilehash: e50b864a63cdd021d82c0a2a73f4f9c3acb68d1afb1f6a2dcd8d8d575966a5fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502791"
---
# <a name="cbasereferenceclockadvisetime-method"></a>Metodo CBaseReferenceClock.AdviseTime

Il `AdviseTime` metodo crea una richiesta di consulenza in un'unica operazione. Questo metodo implementa il [**metodo IReferenceClock::AdviseTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime)

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

Tempo di riferimento di base, in unità di 100 nanosecondi.

</dd> <dt>

*streamTime* 
</dt> <dd>

Tempo di offset del flusso, in unità di 100 nanosecondi.

</dd> <dt>

*hEvent* 
</dt> <dd>

Handle per un evento creato dal chiamante.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Puntatore a una variabile che riceve un identificatore per la richiesta di consulenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valori di ora non validi<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Operazioni non riuscite<br/>                   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | **Argomento puntatore NULL**<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo crea una richiesta di consulenza unica per l'ora di *riferimento baseTime*  +  *streamTime*. La somma deve essere maggiore di zero e minore di MAX \_ TIME oppure il metodo restituisce E \_ INVALIDARG. All'ora richiesta, il clock segnala l'evento specificato nel *parametro hEvent.*

Per annullare la notifica prima che venga raggiunto il tempo, chiamare il metodo [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) e passare il valore *pdwAdviseToken* restituito da questa chiamata. Dopo che la notifica si è verificata, l'orologio la cancella automaticamente, quindi non è necessario chiamare **Unadvise.** Tuttavia, non è un errore eseguire questa operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




