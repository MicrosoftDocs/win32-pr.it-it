---
description: Il metodo Active notifica al segnaposto che il filtro è ora attivo. Questo metodo esegue l'override del metodo CBasePin::Active. Se il pin è connesso, questo metodo avvia il thread di streaming.
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Metodo CSourceStream.Active (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 427c0318bad4df810b29f3596e3a9516f8dbb73e97dd7e378c561bef28bf2f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073344"
---
# <a name="csourcestreamactive-method"></a>Metodo CSourceStream.Active

Il `Active` metodo notifica al segnaposto che il filtro è ora attivo. Questo metodo esegue l'override [**del metodo CBasePin::Active.**](cbasepin-active.md) Se il pin è connesso, questo metodo avvia il thread di streaming.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il segnaposto è già attivo.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Impossibile avviare il thread.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




