---
description: Il metodo SetPreroll specifica se questo esempio è un esempio di preroll. Non dovrebbe essere visualizzato un esempio di preroll. Questo metodo implementa il metodo IMediaSample::SetPreroll.
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Metodo CMediaSample.SetPreroll (Amfilter.h)
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
ms.openlocfilehash: 410031ccf60e830c51615d267d3324167169c5de7960f79dc05b8c9e267463bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832101"
---
# <a name="cmediasamplesetpreroll-method"></a>Metodo CMediaSample.SetPreroll

Il `SetPreroll` metodo specifica se questo esempio è un esempio di preroll. Non dovrebbe essere visualizzato un esempio di preroll. Questo metodo implementa il [**metodo IMediaSample::SetPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll)

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

Valore booleano che specifica se si tratta di un esempio di preroll. Se **TRUE,** si tratta di un esempio di preroll.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo aggiorna la [**variabile membro \_ dwFlags CMediaSample::m,**](cmediasample-m-dwflags.md) che specifica la proprietà preroll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




