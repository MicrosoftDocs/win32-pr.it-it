---
description: 'Il metodo ReceiveConnection accetta una connessione da un altro pin. Questo metodo implementa il metodo IPin:: ReceiveConnection.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Metodo CBasePin. ReceiveConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330316"
---
# <a name="cbasepinreceiveconnection-method"></a>CBasePin. ReceiveConnection, metodo

Il `ReceiveConnection` metodo accetta una connessione da un altro pin. Questo metodo implementa il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pConnector* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di connessione.

</dd> <dt>

*PMT* 
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                                                                |
| <dl> <dt>**\_puntatore E**</dt> </dl>                  | Argomento puntatore **null** .<br/>                                              |
| <dl> <dt>**VFW \_ E \_ già \_ connesso**</dt> </dl>  | Il PIN è già connesso.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ non \_ arrestato**</dt> </dl>        | Il filtro è attivo e il PIN non supporta la riconnessione dinamica.<br/> |
| <dl> <dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt> </dl> | Il tipo di supporto specificato non è accettabile.<br/>                             |



 

## <a name="remarks"></a>Commenti

Il pin di output chiama questo metodo sul pin di input. Se il pin di input restituisce un codice di errore, la connessione ha esito negativo.

Nella classe di base, questo metodo esegue i passaggi seguenti:

-   Controlla se il PIN è già connesso.
-   Controlla se il filtro è stato arrestato.
-   Chiama il metodo [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) per verificare se il pin di connessione è adatto.
-   Chiama il metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) per verificare se il tipo di supporto è accettabile.

Se tutti questi passaggi hanno esito positivo, il metodo chiama i metodi [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) e [**SetMediaType**](cbasepin-setmediatype.md) per completare la connessione. Questi metodi archiviano il tipo di supporto e un puntatore al pin di output.

Se **CheckConnect** o **CheckMediaType** ha esito negativo, la classe base chiama il metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) per interrompere la connessione e quindi restituisce un codice di errore da `ReceiveConnection` .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




