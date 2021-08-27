---
description: 'Metodo CTransformOutputPin.BreakConnect: il metodo BreakConnect rilascia il pin da una connessione.'
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Metodo CTransformOutputPin.BreakConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf468e9f7d9cb439cfe369e3034f76b044001b31be3fd9c7a72ca475aa77d1a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103011"
---
# <a name="ctransformoutputpinbreakconnect-method"></a>Metodo CTransformOutputPin.BreakConnect

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

Questo metodo esegue l'override [**del metodo CBaseOutputPin::BreakConnect.**](cbaseoutputpin-breakconnect.md) Chiama il metodo [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) del filtro, che restituisce S \_ OK nella classe di base. La classe derivata può eseguire l'override del **metodo CTransformFilter::BreakConnect.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




