---
description: Il metodo SetSyncPoint specifica se l'inizio di questo esempio è un punto di sincronizzazione. Questo metodo implementa il metodo IMediaSample::SetSyncPoint.
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Metodo CMediaSample.SetSyncPoint (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0be51ed18e25bcbd12e33f9167493d73f0c140480f4ec0042fb0c43928720d3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156523"
---
# <a name="cmediasamplesetsyncpoint-method"></a>Metodo CMediaSample.SetSyncPoint

Il `SetSyncPoint` metodo specifica se l'inizio di questo esempio è un punto di sincronizzazione. Questo metodo implementa il [**metodo IMediaSample::SetSyncPoint.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bIsSyncPoint* 
</dt> <dd>

Valore booleano che specifica se si tratta di un punto di sincronizzazione. Se **TRUE,** si tratta di un punto di sincronizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo aggiorna la [**variabile membro \_ dwFlags CMediaSample::m,**](cmediasample-m-dwflags.md) che specifica la proprietà del punto di sincronizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




