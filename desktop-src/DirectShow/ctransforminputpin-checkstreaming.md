---
description: Il metodo CheckStreaming determina se il pin può accettare campioni.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Metodo CTransformInputPin.CheckStreaming (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c32dce44e48b033e0a76f5bb5af6aff3eb71948d54c73d670c6226571a1c938b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767607"
---
# <a name="ctransforminputpincheckstreaming-method"></a>Metodo CTransformInputPin.CheckStreaming

Il `CheckStreaming` metodo determina se il pin può accettare campioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | Lo scaricamento del pin è in corso.<br/>       |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin di output non è connesso.<br/> |
| <dl> <dt>**ERRORE DI RUNTIME DI VFW \_ E \_ \_**</dt> </dl> | Si è verificato un errore di run-time.<br/>       |
| <dl> <dt>**VFW \_ E \_ STATO \_ ERRATO**</dt> </dl>   | Il pin viene arrestato.<br/>              |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseInputPin::CheckStreaming.**](cbaseinputpin-checkstreaming.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




