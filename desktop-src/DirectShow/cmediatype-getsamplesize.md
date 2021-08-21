---
description: Il metodo GetSampleSize recupera le dimensioni del campione.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Metodo CMediaType.GetSampleSize (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 120ae54e615e96b368f44c1523703ca35f89d40313f79b450e2cbbd8923829dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156405"
---
# <a name="cmediatypegetsamplesize-method"></a>Metodo CMediaType.GetSampleSize

Il `GetSampleSize` metodo recupera le dimensioni del campione.

## <a name="syntax"></a>Sintassi


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se le dimensioni del campione sono fisse, restituisce le dimensioni del campione in byte. In caso contrario, restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




