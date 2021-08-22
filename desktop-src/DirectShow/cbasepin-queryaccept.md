---
description: Il metodo QueryAccept determina se il pin accetta un tipo di supporto specificato. Questo metodo implementa il metodo IPin::QueryAccept.
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Metodo CBasePin.QueryAccept (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74a179fd1a7f59dcf4e4d22eadf509db9b00cbe482d55e6a6755d7207de8079d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689001"
---
# <a name="cbasepinqueryaccept-method"></a>Metodo CBasePin.QueryAccept

Il `QueryAccept` metodo determina se il pin accetta un tipo di supporto specificato. Questo metodo implementa il [**metodo IPin::QueryAccept.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore a [**una struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il tipo di supporto è accettabile. In caso contrario, restituisce S \_ FALSE.

## <a name="remarks"></a>Commenti

Nella classe di base questo metodo delega al [**metodo CBasePin::CheckMediaType.**](cbasepin-checkmediatype.md) Se **CheckMediaType ha** esito negativo, `QueryAccept` restituisce S \_ FALSE.

Questo metodo non contiene la sezione critica del pin ([**CBasePin::m \_ pLock**](cbasepin-m-plock.md)). Se la classe derivata modifica dinamicamente il set di tipi di supporti accettabili, è necessario eseguire l'override di questo metodo per contenere la sezione critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




