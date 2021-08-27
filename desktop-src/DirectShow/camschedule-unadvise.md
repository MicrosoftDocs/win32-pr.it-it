---
description: Il metodo Unadvise rimuove una richiesta di consulenza.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Metodo CAMSchedule.Unadvise (Dsschedule.h)
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
ms.openlocfilehash: 6bc9b1c964d698e1c1323846c7a25a29f60c0cd71009fbb60f1a09a6757b50b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057601"
---
# <a name="camscheduleunadvise-method"></a>Metodo CAMSchedule.Unadvise

Il `Unadvise` metodo rimuove una richiesta di consulenza.

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

Identificatore della richiesta di consulenza, restituita dal [**metodo CAMSchedule::AddAdvisePacket.**](camschedule-addadvisepacket.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Non trovato<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione riuscita<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule.h (includere Flussi.h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




