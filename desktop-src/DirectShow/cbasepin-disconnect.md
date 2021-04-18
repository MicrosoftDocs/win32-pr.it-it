---
description: Il metodo Disconnect interrompe la connessione al pin corrente. Questo metodo implementa il metodo IPin::D la connessione.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Metodo CBasePin. Disconnect (Amfilter. h)
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
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329544"
---
# <a name="cbasepindisconnect-method"></a>Metodo CBasePin. Disconnect

Il `Disconnect` metodo interrompe la connessione al pin corrente. Questo metodo implementa il metodo [**Ipin::D la connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                         | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | Il PIN non era connesso.<br/>                                              |
| <dl> <dt>**\_OK**</dt> </dl>                | Esito positivo.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ non \_ arrestato**</dt> </dl> | Il filtro è attivo e il PIN non supporta la riconnessione dinamica.<br/> |



 

## <a name="remarks"></a>Commenti

La classe base delega la maggior parte del lavoro al metodo [**CBasePin::D isconnectinternal**](cbasepin-disconnectinternal.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




