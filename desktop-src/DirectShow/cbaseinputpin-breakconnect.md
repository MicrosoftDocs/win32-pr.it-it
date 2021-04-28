---
description: 'Metodo CBaseInputPin.BreakConnect: il metodo BreakConnect rilascia il pin da una connessione.'
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Metodo CBaseInputPin.BreakConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099739"
---
# <a name="cbaseinputpinbreakconnect-method"></a>Metodo CBaseInputPin.BreakConnect

Il `BreakConnect` metodo rilascia il pin da una connessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Decomminzione dell'allocatore e rilascio [**dell'interfaccia IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo di override. In caso contrario, potrebbero verificarsi perdite di memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




