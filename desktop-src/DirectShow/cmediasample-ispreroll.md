---
description: Il metodo IsPreroll determina se questo esempio è un esempio di preroll. Non dovrebbe essere visualizzato un esempio di preroll. Questo metodo implementa il metodo IMediaSample::IsPreroll.
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Metodo CMediaSample.IsPreroll (Amfilter.h)
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
ms.openlocfilehash: 7f4c4b192d72c5edcfdb9c318f7420ca6ae5797446ec4f99cb6871aad2abd241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634641"
---
# <a name="cmediasampleispreroll-method"></a>Metodo CMediaSample.IsPreroll

Il `IsPreroll` metodo determina se questo esempio è un esempio di preroll. Non dovrebbe essere visualizzato un esempio di preroll. Questo metodo implementa il [**metodo IMediaSample::IsPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se l'esempio è un esempio di preroll e S \_ FALSE in caso contrario.

## <a name="remarks"></a>Commenti

La [**variabile membro CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) specifica questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




