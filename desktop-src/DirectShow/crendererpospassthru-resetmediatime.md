---
description: Il metodo ResetMediaTime reimposta i timestamp memorizzati nella cache su zero.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Metodo CRendererPosPassThru.ResetMediaTime (Ctlutil.h)
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
ms.openlocfilehash: f1babc39ad3329ec18be663ffcc6eb882933bead0be5f631ef82ce363391f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953815"
---
# <a name="crendererpospassthruresetmediatime-method"></a>Metodo CRendererPosPassThru.ResetMediaTime

Il `ResetMediaTime` metodo reimposta i timestamp memorizzati nella cache su zero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il filtro deve chiamare questo metodo ogni volta che i timestamp memorizzati nella cache dal metodo [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) diventano non validi. In particolare, deve chiamare questo metodo in risposta ai metodi [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) e [**IMediaFilter::Stop.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

Dopo la chiamata di questo metodo, il metodo [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) restituisce zero per l'ora di inizio e di fine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




