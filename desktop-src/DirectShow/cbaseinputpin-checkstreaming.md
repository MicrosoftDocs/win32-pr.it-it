---
description: Determina se il pin può accettare esempi.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Metodo CBaseInputPin. CheckStreaming (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324274"
---
# <a name="cbaseinputpincheckstreaming-method"></a>CBaseInputPin. CheckStreaming, metodo

Determina se il pin può accettare esempi.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                   |
| <dl> <dt>**S \_ false**</dt> </dl>               | È in corso lo scaricamento del PIN.<br/> |
| <dl> <dt>**errore di runtime di VFW \_ E \_ \_**</dt> </dl> | Si è verificato un errore in fase di esecuzione.<br/> |
| <dl> <dt>**\_ \_ stato non corretto di VFW E \_**</dt> </dl>   | Il PIN è stato arrestato.<br/>        |



 

## <a name="remarks"></a>Commenti

La classe derivata può eseguire l'override di questo metodo per eseguire ulteriori controlli. Nel metodo che esegue l'override, chiamare anche l'implementazione della classe di base.

Il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) chiama questo metodo. È necessario eseguire l'override del metodo [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) per chiamare anche questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




