---
description: "Il metodo SetTimeFormat imposta il formato dell'ora. Questo metodo implementa il metodo IMediaSeeking:: SetTimeFormat."
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Metodo CSourceSeeking. SetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 61ab0cdf7c954e0fa5f370127f00529bb9ef7b16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333714"
---
# <a name="csourceseekingsettimeformat-method"></a>CSourceSeeking. SetTimeFormat, metodo

Il `SetTimeFormat` metodo imposta il formato dell'ora. Questo metodo implementa il metodo [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTimeFormat(
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



| Codice restituito                                                                                  | Descrizione                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il formato specificato non è supportato.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null** .<br/>         |



 

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

 

 




