---
description: 'Il metodo QueryAccept determina se il pin accetta un tipo di supporto specificato. Questo metodo implementa il metodo IPin:: QueryAccept.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Metodo CBasePin. QueryAccept (Amfilter. h)
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
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333796"
---
# <a name="cbasepinqueryaccept-method"></a>CBasePin. QueryAccept, metodo

Il `QueryAccept` metodo determina se il pin accetta un tipo di supporto specificato. Questo metodo implementa il metodo [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il tipo di supporto è accettabile. In caso contrario, restituisce \_ false.

## <a name="remarks"></a>Commenti

Nella classe di base, questo metodo delega al metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) . Se **CheckMediaType** ha esito negativo, `QueryAccept` restituisce \_ false.

Questo metodo non è contenuta nella sezione critica del PIN ([**CBasePin:: m \_ pLock**](cbasepin-m-plock.md)). Se la classe derivata modifica dinamicamente il set di tipi di supporti accettabili, è necessario eseguire l'override di questo metodo per mantenere la sezione critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




