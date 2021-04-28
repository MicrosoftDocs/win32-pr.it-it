---
description: 'Metodo CDynamicOutputPin.Active: il metodo Active notifica al segnaposto che il filtro è ora attivo.'
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Metodo CDynamicOutputPin.Active (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099329"
---
# <a name="cdynamicoutputpinactive-method"></a>Metodo CDynamicOutputPin.Active

Il `Active` metodo notifica al segnaposto che il filtro è ora attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                            | Descrizione                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                                                                                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Esito negativo. [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) non è stato chiamato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseOutputPin::Active.**](cbaseoutputpin-active.md) Reimposta l'evento [**\_ HStopEvent CDynamicOutputPin::m.**](cdynamicoutputpin-m-hstopevent.md) Se il filtro proprietario non ha chiamato **SetConfigInfo,** questo metodo restituisce E \_ FAIL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




