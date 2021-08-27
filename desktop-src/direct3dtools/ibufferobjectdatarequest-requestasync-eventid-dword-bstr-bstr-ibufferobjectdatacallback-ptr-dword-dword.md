---
description: Richieste per ottenere il contenuto non elaborato di un oggetto (buffer, trama, visualizzazione di destinazione del rendering e così via).
MS-HAID: vspixengine.IBufferObjectDataRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_BSTR\_IBufferObjectDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IBufferObjectDataRequest::RequestAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 899954DC-6196-4F79-AFB4-5E692DAA03EC
api_name:
- IBufferObjectDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c021627fd3a5c7d7f0e5f014437bd376c08e7c1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624937"
---
# <a name="span-idvspixengineibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dwordspanibufferobjectdatarequestrequestasync-method"></a><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>Metodo IBufferObjectDataRequest::RequestAsync

Richieste per ottenere il contenuto non elaborato di un oggetto (buffer, trama, visualizzazione destinazione di rendering e così via)

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   BSTR                        Format,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*Eventid*   
Evento specificato a cui associare il contenuto del buffer( ad esempio, una destinazione di rendering potrebbe cambiare nel tempo).

*RequestedDataUID*   
Indirizzo dell'oggetto specificato.

*File*   
Stringa COM che contiene il percorso del file in cui vengono scritti i risultati.

*Formato*   
Attualmente non utilizzato. Stringa COM che specifica il formato di output.

*requestCallback*   
Indirizzo del callback utilizzato per inviare una notifica all'host dei risultati.

*requestCookie*   
Cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IBufferObjectDataRequest**](/windows/desktop/direct3dtools/ibufferobjectdatarequest)

 

 
