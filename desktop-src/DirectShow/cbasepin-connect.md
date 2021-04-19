---
description: 'Il metodo Connect connette il pin a un altro pin. Questo metodo implementa il metodo IPin:: Connect.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: Metodo CBasePin. Connect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333006"
---
# <a name="cbasepinconnect-method"></a>Metodo CBasePin. Connect

Il `Connect` metodo connette il pin a un altro pin. Questo metodo implementa il metodo [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di ricezione.

</dd> <dt>

*PMT* 
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto per la connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                                  | Descrizione                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Esito positivo.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ già \_ connesso**</dt> </dl>    | Il PIN è già connesso.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ nessun \_ \_ tipo accettabile**</dt> </dl> | Impossibile trovare un tipo di supporto accettabile.<br/>                                |
| <dl> <dt>**VFW \_ E \_ non \_ arrestato**</dt> </dl>          | Il filtro è attivo e il PIN non supporta la riconnessione dinamica.<br/> |
| <dl> <dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt> </dl>   | Il tipo di supporto specificato non è accettabile.<br/>                             |



 

## <a name="remarks"></a>Commenti

Il parametro *PMT* può essere **null**. Può inoltre specificare un tipo di supporto parziale, con un valore GUID \_ null per il tipo principale, il sottotipo o il formato.

Nella classe di base, questo metodo verifica se il PIN è già connesso e se il filtro è stato arrestato. Delega il resto del processo di connessione al metodo [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




