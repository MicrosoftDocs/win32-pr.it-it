---
title: Ack for Fragment
description: Usare il pacchetto Ack for Fragment per confermare la richiesta frammento del client.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- Ack for Fragment BITS
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd4b8bf5580a5724c689ced1886051006d34cd3c9ba0561d253f36428178c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702121"
---
# <a name="ack-for-fragment"></a>Ack for Fragment

Usare il **pacchetto Ack for Fragment** per confermare la richiesta [**frammento del**](fragment.md) client.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>reason-code
</dt> <dd>

Sostituire il codice motivo con un codice motivo HTTP. La tabella seguente illustra i codici motivo tipici per una risposta a una [**richiesta fragment.**](fragment.md) Per un elenco dei codici motivo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Codice motivo    | Descrizione                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | OK. La richiesta è stata completata.<br/>                                                                             |
| 416<br/> | Intervallo non soddisfabile. Il client ha inviato un frammento il cui intervallo non è contiguo al frammento precedente.<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Sostituire reason-description con la descrizione HTTP associata al codice motivo. Ad esempio, impostare reason-description su OK se il codice motivo è 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica questo pacchetto di risposta come pacchetto Ack.

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range
</dt> <dd>

Offset in base zero al byte successivo che il server prevede che il client invii. Ad esempio, se il frammento contiene l'intervallo 128 212, impostare l'intervallo su 213.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-ID
</dt> <dd>

GUID stringa che identifica la sessione al client. Sostituire {guid} con l'identificatore di sessione inviato dal client nel pacchetto di richiesta [**fragment.**](fragment.md) Se non si riconosce l'identificatore di sessione, impostare l'intestazione BITS-Error-Code su BG \_ E \_ SESSION NOT \_ \_ FOUND.

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL
</dt> <dd>

Contiene l'URL dei dati di risposta di un processo di caricamento-risposta. Includere questa intestazione nella risposta del frammento finale al termine del caricamento e ricevere una risposta dall'applicazione server, se applicabile.

Usare l'intestazione Content-Range della richiesta Fragment per determinare se il caricamento è stato completato. Il caricamento è completo se l'offset finale del valore dell'intervallo è uguale al valore di lunghezza totale meno uno.

Il server BITS invia il file di caricamento all'applicazione server dopo aver determinato che il caricamento è stato completato. L'applicazione server elabora il file e genera la risposta. Il server BITS imposta il valore di BITS-Reply-URL sull'URL del file di risposta dall'applicazione server.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza contenuto
</dt> <dd>

Sostituire length con il numero di byte inclusi nel corpo della risposta. Content-Length è obbligatorio, anche se il corpo della risposta non include contenuto.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

Sostituire il codice di errore con un numero esadecimale che rappresenta un valore HRESULT associato a un errore sul lato server. Includere questa intestazione solo se il codice motivo non è 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context
</dt> <dd>

Sostituire error-context con un numero esadecimale che rappresenta il contesto in cui si è verificato l'errore. Specificare il numero esadecimale per [**BG \_ ERROR CONTEXT REMOTE \_ \_ \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se il server ha generato l'errore. In caso contrario, specificare il numero esadecimale per **BG \_ ERROR CONTEXT REMOTE \_ \_ \_ APPLICATION** (0x7) se l'errore è stato generato dall'applicazione a cui viene passato il file di caricamento. Includere questa intestazione solo se il codice motivo non è 200 o 201.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la sessione è per un processo di caricamento-risposta, potrebbe verificarsi un ritardo prima che il client riceva la risposta **finale Ack for Fragment.** La durata del ritardo dipende dalla quantità di tempo richiesta dall'applicazione server (applicazione in cui il server invia il file di caricamento) per generare la risposta.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Create-Session**](create-session.md)
</dt> <dt>

[**Frammento**](fragment.md)
</dt> </dl>

 

 





