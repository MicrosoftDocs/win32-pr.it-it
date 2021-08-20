---
description: Il metodo Unadvise rimuove una richiesta di consulenza in sospeso. Questo metodo implementa il metodo IReferenceClock::Unadvise.
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Metodo CBaseReferenceClock.Unadvise (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26e6519d1a94091c0afc0bafffe40fdaac47364d25f54e068ae503f32abccbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652451"
---
# <a name="cbasereferenceclockunadvise-method"></a>Metodo CBaseReferenceClock.Unadvise

Il `Unadvise` metodo rimuove una richiesta di consulenza in sospeso. Questo metodo implementa il [**metodo IReferenceClock::Unadvise.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwAdviseToken* 
</dt> <dd>

Identificatore della richiesta da rimuovere. Usare il valore restituito dai metodi [**CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) o [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) nel *parametro pdwAdviseToken.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Non trovato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




