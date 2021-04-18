---
description: "Il metodo GetTimeFormat Recupera il formato dell'ora corrente. Questo metodo implementa il metodo IMediaSeeking:: GetTimeFormat."
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Metodo CSourceSeeking. GetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce53f4a6cabcc5face6c332666701dc208c3f8bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329500"
---
# <a name="csourceseekinggettimeformat-method"></a>CSourceSeeking. GetTimeFormat, metodo

Il `GetTimeFormat` metodo recupera il formato dell'ora corrente. Questo metodo implementa il metodo [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntatore a una variabile che riceve un GUID del formato dell'ora. Vedere [**GUID del formato ora**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Operazione riuscita<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Valore del puntatore **null**<br/> |



 

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

 

 




