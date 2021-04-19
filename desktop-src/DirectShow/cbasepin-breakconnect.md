---
description: Il metodo BreakConnect rilascia il pin da una connessione.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Metodo CBasePin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332770"
---
# <a name="cbasepinbreakconnect-method"></a>CBasePin. BreakConnect, metodo

Il `BreakConnect` metodo rilascia il pin da una connessione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato durante la disconnessione del PIN tramite il metodo [**CBasePin::D la connessione**](cbasepin-disconnect.md) . Viene anche chiamato durante un tentativo di connessione se il metodo [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) ha esito negativo.

Questo metodo deve liberare tutte le risorse ottenute dal metodo **CheckConnect** . Se, ad esempio, **CheckConnect** alloca memoria, `BreakConnect` deve liberare la memoria. Se **CheckConnect** esegue una query sul pin di connessione per un'interfaccia, `BreakConnect` deve liberare l'interfaccia.

Si noti che `BreakConnect` può essere chiamato senza una chiamata corrispondente a **CompleteConnect**. Pertanto, non è possibile presupporre che **CompleteConnect** sia stato chiamato in precedenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




