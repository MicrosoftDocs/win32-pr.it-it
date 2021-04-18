---
description: "Il metodo IsPreroll determina se l'esempio è un esempio di preroll. Non è necessario visualizzare un campione di preroll. Questo metodo implementa il metodo IMediaSample:: IsPreroll."
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Metodo CMediaSample. IsPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324956"
---
# <a name="cmediasampleispreroll-method"></a>CMediaSample. IsPreroll, metodo

Il `IsPreroll` metodo determina se l'esempio è un esempio di preroll. Non è necessario visualizzare un campione di preroll. Questo metodo implementa il metodo [**IMediaSample:: IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se l'esempio è un campione di preroll e \_ in caso contrario è false.

## <a name="remarks"></a>Commenti

La variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) specifica questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




