---
description: 'Metodo CTransformInputPin.EndOfStream: il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il metodo IPin::EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Metodo CTransformInputPin.EndOfStream (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2035d0261447826098162f480ddc959544b101b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084979"
---
# <a name="ctransforminputpinendofstream-method"></a>Metodo CTransformInputPin.EndOfStream

Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il [**metodo IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | Il pin è attualmente in fase di scaricamento.<br/>       |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin di output non è connesso.<br/> |
| <dl> <dt>**ERRORE DI RUNTIME DI VFW \_ E \_ \_**</dt> </dl> | Si è verificato un errore di run-time.<br/>       |
| <dl> <dt>**VFW \_ E \_ STATO \_ ERRATO**</dt> </dl>   | Il pin è stato arrestato.<br/>              |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) del filtro per recapitare la notifica di fine flusso a valle.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




