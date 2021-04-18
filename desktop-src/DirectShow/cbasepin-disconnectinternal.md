---
description: Il metodo DisconnectInternal interrompe la connessione al pin corrente.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Metodo CBasePin. DisconnectInternal (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329543"
---
# <a name="cbasepindisconnectinternal-method"></a>CBasePin. DisconnectInternal, metodo

Il `DisconnectInternal` metodo interrompe la connessione al pin corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                         | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | Il PIN non era connesso.<br/>                                              |
| <dl> <dt>**\_OK**</dt> </dl>                | Esito positivo.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ non \_ arrestato**</dt> </dl> | Il filtro è attivo e il PIN non supporta la riconnessione dinamica.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo [**CBasePin::D di disconnessione**](cbasepin-disconnect.md) delega il processo di disconnessione a questo metodo. Questo metodo chiama il metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) . Rilascia anche il conteggio dei riferimenti sull'altro pin, che è contenuto dalla variabile membro [**\_ connesso CBasePin:: m**](cbasepin-m-connected.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




