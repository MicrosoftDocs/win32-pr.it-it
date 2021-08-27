---
description: 'Metodo CBasePin.BreakConnect: il metodo BreakConnect rilascia il pin da una connessione.'
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Metodo CBasePin.BreakConnect (Amfilter.h)
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
ms.openlocfilehash: c40c7614f94b2be5e5f588a706b4b0bd1eec92c3181ffbedcad3ae1e57183f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955230"
---
# <a name="cbasepinbreakconnect-method"></a>Metodo CBasePin.BreakConnect

Il `BreakConnect` metodo rilascia il pin da una connessione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato durante la disconnessione del pin dal metodo [**CBasePin::D isconnect.**](cbasepin-disconnect.md) Viene chiamato anche durante un tentativo di connessione se il [**metodo CBasePin::CheckConnect ha**](cbasepin-checkconnect.md) esito negativo.

Questo metodo deve liberare tutte le risorse ottenute dal **metodo CheckConnect.** Ad esempio, se **CheckConnect alloca** memoria, `BreakConnect` deve liberare la memoria. Se **CheckConnect esegue** una query sul pin di connessione per un'interfaccia, `BreakConnect` deve liberare l'interfaccia.

Si noti `BreakConnect` che può essere chiamato senza una chiamata corrispondente a **CompleteConnect**. Pertanto, non è possibile presupporre che **CompleteConnect** sia stato chiamato in precedenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




