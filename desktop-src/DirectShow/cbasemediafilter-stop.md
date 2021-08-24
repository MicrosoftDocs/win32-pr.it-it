---
description: Il metodo Stop arresta l'oggetto. Questo metodo implementa il metodo IMediaFilter::Stop.
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Metodo CBaseMediaFilter.Stop (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: effe2df53508cd9c1f6523356eb7296458208c3ee0e61c1dd12c94bd87b6ad31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793231"
---
# <a name="cbasemediafilterstop-method"></a>Metodo CBaseMediaFilter.Stop

Il `Stop` metodo arresta l'oggetto . Questo metodo implementa il [**metodo IMediaFilter::Stop.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Nella classe di base questo metodo imposta la variabile membro [**CBaseMediaFilter::m \_ State**](cbasemediafilter-m-state.md) su State \_ Stopped, ma non esegue altre operazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




