---
description: 'Metodo CSourceSeeking.IsFormatSupported: il metodo IsFormatSupported determina se è supportato un formato di ora specificato. Questo metodo implementa il metodo IMediaSeeking::IsFormatSupported.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Metodo CSourceSeeking.IsFormatSupported (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c58e8edd908c101c3045e221cc86420cbb5cb94
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098749"
---
# <a name="csourceseekingisformatsupported-method"></a>Metodo CSourceSeeking.IsFormatSupported

Il `IsFormatSupported` metodo determina se è supportato un formato di ora specificato. Questo metodo implementa il [**metodo IMediaSeeking::IsFormatSupported.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntatore a un GUID di formato ora. Vedere [**GUID di formato dell'ora.**](time-format-guids.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Il formato non è supportato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il formato è supportato.<br/>     |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Argomento del puntatore **NULL.**<br/>   |



 

## <a name="remarks"></a>Commenti

L'unico formato di ora supportato dalla classe di base è TIME \_ FORMAT \_ MEDIA TIME \_ (unità di 100 nanosecondi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




