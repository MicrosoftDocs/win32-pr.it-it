---
description: Il metodo Unadvise rimuove una richiesta di notifica.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Metodo CAMSchedule. Unadvise (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329561"
---
# <a name="camscheduleunadvise-method"></a>Metodo CAMSchedule. Unadvise

Il `Unadvise` metodo rimuove una richiesta di notifica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

Identificatore della richiesta di notifica, restituito dal metodo [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Non trovato<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Operazione riuscita<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule. h (include Streams. h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




