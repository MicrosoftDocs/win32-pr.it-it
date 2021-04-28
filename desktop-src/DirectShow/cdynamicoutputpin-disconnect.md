---
description: 'Metodo CDynamicOutputPin.Disconnect: il metodo Disconnect interrompe la connessione pin corrente. Questo metodo implementa il metodo IPin::D isconnect.'
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Metodo CDynamicOutputPin.Disconnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099299"
---
# <a name="cdynamicoutputpindisconnect-method"></a>Metodo CDynamicOutputPin.Disconnect

Il `Disconnect` metodo interrompe la connessione pin corrente. Questo metodo implementa il [**metodo IPin::D isconnect.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il pin non è stato connesso.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                   |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBasePin::D isconnect**](cbasepin-disconnect.md) per abilitare la disconnessione mentre il filtro è attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




