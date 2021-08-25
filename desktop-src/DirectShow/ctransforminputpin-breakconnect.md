---
description: 'Metodo CTransformInputPin.BreakConnect: il metodo BreakConnect rilascia il pin da una connessione.'
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Metodo CTransformInputPin.BreakConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad97061bda8ec4703464d21ad4817cfd97740f4a98904255150ce75fba37c425
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812891"
---
# <a name="ctransforminputpinbreakconnect-method"></a>Metodo CTransformInputPin.BreakConnect

Il `BreakConnect` metodo rilascia il pin da una connessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseInputPin::BreakConnect.**](cbaseinputpin-breakconnect.md) Chiama il metodo [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) del filtro, che restituisce S \_ OK nella classe di base. La classe derivata può eseguire l'override **del metodo CTransformFilter::BreakConnect.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




