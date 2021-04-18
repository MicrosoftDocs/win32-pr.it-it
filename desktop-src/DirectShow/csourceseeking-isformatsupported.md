---
description: 'Il metodo IsFormatSupported determina se è supportato un formato di ora specificato. Questo metodo implementa il metodo IMediaSeeking:: IsFormatSupported.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Metodo CSourceSeeking. IsFormatSupported (Ctlutil. h)
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
ms.openlocfilehash: 7d027a2ee6e94e4ccf4944c27e77f02d1d1c5edb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329498"
---
# <a name="csourceseekingisformatsupported-method"></a>CSourceSeeking. IsFormatSupported, metodo

Il `IsFormatSupported` metodo determina se è supportato un formato di ora specificato. Questo metodo implementa il metodo [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .

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

Puntatore a un GUID del formato ora. Vedere [**GUID del formato ora**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Il formato non è supportato.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Il formato è supportato.<br/>     |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null** .<br/>   |



 

## <a name="remarks"></a>Commenti

L'unico formato di ora supportato dalla classe base è il \_ tempo medio di formato dell'ora \_ \_ (unità 100-nanosecondi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




