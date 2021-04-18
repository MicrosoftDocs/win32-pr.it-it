---
description: "Il metodo SetDiscontinuity specifica se l'esempio rappresenta un'operazione break nel flusso di dati. Questo metodo implementa il metodo IMediaSample:: SetDiscontinuity."
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Metodo CMediaSample. SetDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325315"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>CMediaSample. SetDiscontinuity, metodo

Il `SetDiscontinuity` metodo specifica se l'esempio rappresenta un'interruzioni nel flusso di dati. Questo metodo implementa il metodo [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bDiscont* 
</dt> <dd>

Valore booleano che specifica se questo esempio è una discontinuità. Se **true**, l'esempio di supporto è discontinuo con l'esempio precedente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo aggiorna la variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) , che specifica la proprietà discontinuity.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




