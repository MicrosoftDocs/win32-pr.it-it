---
description: Il metodo ResetMediaTime Reimposta i timestamp memorizzati nella cache su zero.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Metodo CRendererPosPassThru. ResetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327194"
---
# <a name="crendererpospassthruresetmediatime-method"></a>CRendererPosPassThru. ResetMediaTime, metodo

Il `ResetMediaTime` metodo reimposta i timestamp memorizzati nella cache su zero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il filtro deve chiamare questo metodo ogni volta che i timestamp memorizzati nella cache dal metodo [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) diventano non validi. In particolare, deve chiamare questo metodo in risposta ai metodi [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) e [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

Dopo la chiamata a questo metodo, il metodo [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) restituisce zero per le ore di inizio e di fine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




