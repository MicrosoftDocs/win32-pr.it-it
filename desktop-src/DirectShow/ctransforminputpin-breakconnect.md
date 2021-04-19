---
description: Il metodo BreakConnect rilascia il pin da una connessione.
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Metodo CTransformInputPin. BreakConnect (Transfrm. h)
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
ms.openlocfilehash: 2274b71b67a54ecacb291d77d2eef4ad8a110fa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332707"
---
# <a name="ctransforminputpinbreakconnect-method"></a>CTransformInputPin. BreakConnect, metodo

Il `BreakConnect` metodo rilascia il pin da una connessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseInputPin:: BreakConnect**](cbaseinputpin-breakconnect.md) . Chiama il metodo [**CTransformFilter:: BreakConnect**](ctransformfilter-breakconnect.md) del filtro, che restituisce \_ OK nella classe di base. La classe derivata può eseguire l'override del metodo **CTransformFilter:: BreakConnect** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




