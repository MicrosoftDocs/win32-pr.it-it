---
description: 'Il metodo Unadvise rimuove una richiesta di notifica in sospeso. Questo metodo implementa il metodo IReferenceClock:: Unadvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Metodo CBaseReferenceClock. Unadvise (Refclock. h)
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
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332215"
---
# <a name="cbasereferenceclockunadvise-method"></a>Metodo CBaseReferenceClock. Unadvise

Il `Unadvise` metodo rimuove una richiesta di notifica in sospeso. Questo metodo implementa il metodo [**IReferenceClock:: Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .

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

Identificatore della richiesta da rimuovere. Usare il valore restituito dai metodi [**CBaseReferenceClock:: AdviseTime**](cbasereferenceclock-advisetime.md) o [**CBaseReferenceClock:: AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) nel parametro *pdwAdviseToken* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Non trovato.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




