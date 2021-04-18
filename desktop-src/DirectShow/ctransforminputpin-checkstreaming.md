---
description: Il metodo CheckStreaming determina se il pin può accettare esempi.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Metodo CTransformInputPin. CheckStreaming (Transfrm. h)
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
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328811"
---
# <a name="ctransforminputpincheckstreaming-method"></a>CTransformInputPin. CheckStreaming, metodo

Il `CheckStreaming` metodo determina se il pin può accettare esempi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                         |
| <dl> <dt>**S \_ false**</dt> </dl>               | È in corso lo scaricamento del PIN.<br/>       |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il pin di output non è connesso.<br/> |
| <dl> <dt>**errore di runtime di VFW \_ E \_ \_**</dt> </dl> | Si è verificato un errore in fase di esecuzione.<br/>       |
| <dl> <dt>**\_ \_ stato non corretto di VFW E \_**</dt> </dl>   | Il PIN è stato arrestato.<br/>              |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




