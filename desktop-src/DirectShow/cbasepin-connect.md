---
description: Il Connessione metodo connette il pin a un altro pin. Questo metodo implementa il metodo IPin::Connessione.
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: CBasePin. Connessione metodo (Amfilter.h)
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
ms.openlocfilehash: a134b87e9c7c4d0f665ae37df7ec9cd0ecb3a37c0d0548f27835ead7b8ecca21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074795"
---
# <a name="cbasepinconnect-method"></a>CBasePin. Connessione metodo

Il `Connect` metodo connette il pin a un altro pin. Questo metodo implementa il [**metodo IPin::Connessione.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect)

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

Puntatore all'interfaccia [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin ricevente.

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntatore a [**una struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto per la connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                                  | Descrizione                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Operazione completata.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ GIÀ \_ CONNESSO**</dt> </dl>    | Il pin è già connesso.<br/>                                           |
| <dl> <dt>**VFW \_ E NESSUN TIPO \_ \_ \_ ACCETTABILE**</dt> </dl> | Impossibile trovare un tipo di supporto accettabile.<br/>                                |
| <dl> <dt>**VFW \_ E \_ NON \_ ARRESTATO**</dt> </dl>          | Il filtro è attivo e il pin non supporta la riconnessione dinamica.<br/> |
| <dl> <dt>**TIPO E VFW \_ \_ NON \_ \_ ACCETTATO**</dt> </dl>   | Il tipo di supporto specificato non è accettabile.<br/>                             |



 

## <a name="remarks"></a>Commenti

Il *parametro pmt* può essere **NULL.** Può anche specificare un tipo di supporto parziale, con valore GUID NULL per il tipo principale, il \_ sottotipo o il formato.

Nella classe di base questo metodo verifica se il pin è già connesso e se il filtro viene arrestato. Delega il resto del processo di connessione al [**metodo CBasePin::AgreeMediaType.**](cbasepin-agreemediatype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




