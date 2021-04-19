---
description: Il metodo Stop arresta il filtro.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Metodo CBaseRenderer. Stop (Renbase. h)
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
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332995"
---
# <a name="cbaserendererstop-method"></a>Metodo CBaseRenderer. Stop

Il `Stop` metodo interrompe il filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseFilter:: Stop**](cbasefilter-stop.md) . Esegue le azioni seguenti:

-   Chiama [**CBaseFilter:: Stop**](cbasefilter-stop.md).
-   Decommit dell'allocatore. (Vedere [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)).
-   Annulla qualsiasi rendering pianificato e rilascia il thread di streaming.
-   Attende il completamento di qualsiasi chiamata di **ricezione** in sospeso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




