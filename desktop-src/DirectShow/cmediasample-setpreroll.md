---
description: "Il metodo SetPreroll specifica se l'esempio è un esempio di preroll. Non è necessario visualizzare un campione di preroll. Questo metodo implementa il metodo IMediaSample:: SetPreroll."
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Metodo CMediaSample. SetPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325306"
---
# <a name="cmediasamplesetpreroll-method"></a>CMediaSample. SetPreroll, metodo

Il `SetPreroll` metodo specifica se l'esempio è un esempio di preroll. Non è necessario visualizzare un campione di preroll. Questo metodo implementa il metodo [**IMediaSample:: SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bIsPreroll* 
</dt> <dd>

Valore booleano che specifica se si tratta di un campione di preroll. Se **true**, si tratta di un esempio di preroll.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo aggiorna la variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) , che specifica la proprietà preroll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




