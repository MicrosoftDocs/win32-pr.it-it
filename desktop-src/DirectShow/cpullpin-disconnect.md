---
description: Il metodo Disconnect interrompe la connessione con il pin di output.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Metodo CPullPin. Disconnect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331175"
---
# <a name="cpullpindisconnect-method"></a>Metodo CPullPin. Disconnect

Il `Disconnect` metodo interrompe la connessione con il pin di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo interrompe qualsiasi connessione eseguita nel metodo [**CPullPin:: Connect**](cpullpin-connect.md) . Chiamare questo metodo all'interno del metodo [**Ipin::D la connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) . Se il pin deriva da [**CBasePin**](cbasepin.md), eseguire l'override di [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) per chiamare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




