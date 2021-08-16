---
description: Il metodo Stop arresta il filtro.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Metodo CBaseRenderer.Stop (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 942fae3ee1ea2c7481f475dc2d8dba421fd21d44290c98b822b9bc489ee25334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822621"
---
# <a name="cbaserendererstop-method"></a>Metodo CBaseRenderer.Stop

Il `Stop` metodo arresta il filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseFilter::Stop.**](cbasefilter-stop.md) Esegue le azioni seguenti:

-   Chiama [**CBaseFilter::Stop.**](cbasefilter-stop.md)
-   Disaccommia l'allocatore. Vedere [**IMemAllocator::D ecommit.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)
-   Annulla qualsiasi rendering pianificato e rilascia il thread di streaming.
-   Attende il completamento di qualsiasi **chiamata Receive** in sospeso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




