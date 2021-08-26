---
description: 'Metodo CBasePin.Disconnect: il metodo Disconnect interrompe la connessione del pin corrente. Questo metodo implementa il metodo IPin::D isconnect.'
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Metodo CBasePin.Disconnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0048624b79daa6948851fd9a56142b97c7e185caa9bbcbdeb6c2c1b19f591eb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916631"
---
# <a name="cbasepindisconnect-method"></a>Metodo CBasePin.Disconnect

Il `Disconnect` metodo interrompe la connessione del pin corrente. Questo metodo implementa il [**metodo IPin::D isconnect.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                         | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | Il pin non è stato connesso.<br/>                                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione completata.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ NON \_ ARRESTATO**</dt> </dl> | Il filtro è attivo e il pin non supporta la riconnessione dinamica.<br/> |



 

## <a name="remarks"></a>Commenti

La classe base delega la maggior parte del lavoro al metodo [**CBasePin::D isconnectInternal.**](cbasepin-disconnectinternal.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




