---
description: "Il metodo GetAvailable recupera l'intervallo di tempo in cui la ricerca è efficiente. Questo metodo implementa il metodo IMediaSeeking:: GetAvailable."
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Metodo CPosPassThru. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327539"
---
# <a name="cpospassthrugetavailable-method"></a>Metodo CPosPassThru. GetAvailable

Il `GetAvailable` metodo recupera l'intervallo di tempo in cui la ricerca è efficiente. Questo metodo implementa il metodo [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pEarliest* 
</dt> <dd>

Puntatore a una variabile che riceve la prima ora per una ricerca efficiente.

</dd> <dt>

*Piatto* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora più recente per una ricerca efficiente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore **HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




