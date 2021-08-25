---
description: Il metodo DisconnectInternal interrompe la connessione del pin corrente.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Metodo CBasePin.DisconnectInternal (Amfilter.h)
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
ms.openlocfilehash: c420419e49f7093e6fdf1fdc66880035f4844d03277db18b5c134d9ee69b10fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916531"
---
# <a name="cbasepindisconnectinternal-method"></a>Metodo CBasePin.DisconnectInternal

Il `DisconnectInternal` metodo interrompe la connessione del pin corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                         | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | Il pin non è stato connesso.<br/>                                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione completata.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ NON \_ ARRESTATO**</dt> </dl> | Il filtro è attivo e il pin non supporta la riconnessione dinamica.<br/> |



 

## <a name="remarks"></a>Commenti

Il [**metodo CBasePin::D isconnect**](cbasepin-disconnect.md) delega il processo di disconnessione a questo metodo. Questo metodo chiama il [**metodo CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Rilascia anche il conteggio dei riferimenti sull'altro pin, che viene mantenuto dalla variabile membro [**CBasePin::m \_ Connected.**](cbasepin-m-connected.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




