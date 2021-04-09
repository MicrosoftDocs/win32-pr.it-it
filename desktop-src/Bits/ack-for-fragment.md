---
title: ACK per il frammento
description: Utilizzare il ACK per il pacchetto del frammento per confermare la richiesta del frammento del client.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- ACK per BITS frammenti
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103963549"
---
# <a name="ack-for-fragment"></a>ACK per il frammento

Utilizzare il **ACK per** il pacchetto del frammento per confermare la richiesta del [**frammento**](fragment.md) del client.

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

<span id="reason-code"></span><span id="REASON-CODE"></span>codice motivo
</dt> <dd>

Sostituire Reason-Code con un codice motivo HTTP. La tabella seguente illustra i codici motivo tipici per una risposta a una richiesta di [**frammento**](fragment.md) . Per un elenco di codici motivo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Codice motivo    | Descrizione                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | OK. La richiesta è stata completata.<br/>                                                                             |
| 416<br/> | Range: not-Impossibile attenersi all'. Il client ha inviato un frammento il cui intervallo non è contiguo al frammento precedente.<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-Descrizione
</dt> <dd>

Sostituire Reason-Description con la descrizione HTTP associata al codice motivo. Ad esempio, impostare Reason-Description su OK se Reason-Code è 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto
</dt> <dd>

Identifica il pacchetto di risposta come pacchetto ACK.

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range
</dt> <dd>

Offset in base zero al byte successivo che il server prevede che il client invii. Se, ad esempio, il frammento contiene l'intervallo 128 212, impostare intervallo su 213.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID
</dt> <dd>

GUID di stringa che identifica la sessione per il client. Sostituire {GUID} con l'identificatore di sessione inviato dal client nel pacchetto di richiesta del [**frammento**](fragment.md) . Se non si riconosce l'identificatore di sessione, impostare l'intestazione BITS-Error-Code su BG \_ E la \_ sessione \_ non \_ trovata.

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL
</dt> <dd>

Contiene l'URL dei dati di risposta di un processo di caricamento-risposta. Includere questa intestazione nella risposta del frammento finale dopo che il caricamento è stato completato e si riceve una risposta dall'applicazione server, se applicabile.

Usare l'intestazione Content-Range della richiesta Fragment per determinare se il caricamento è stato completato. Il caricamento è completo se l'offset finale del valore dell'intervallo è uguale al valore di lunghezza totale meno uno.

Il server BITS inserisce il file di caricamento nell'applicazione server dopo aver determinato che il caricamento è stato completato. L'applicazione server elabora il file e genera la risposta. Il server BITS imposta il valore di BITS-Reply-URL sull'URL del file di risposta dall'applicazione server.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza del contenuto
</dt> <dd>

Sostituire length con il numero di byte inclusi nel corpo della risposta. Content-Length è obbligatorio, anche se il corpo della risposta non include il contenuto.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-errore-codice
</dt> <dd>

Sostituire error-code con un numero esadecimale che rappresenta un valore HRESULT associato a un errore sul lato server. Includere questa intestazione solo se il codice motivo non è 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-errore-contesto
</dt> <dd>

Sostituire Error-context con un numero esadecimale che rappresenta il contesto in cui si è verificato l'errore. Specificare il numero esadecimale per il [**\_ \_ \_ \_ file remoto del contesto di errore BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se il server ha generato l'errore. In caso contrario, specificare il numero esadecimale per l' **\_ \_ \_ \_ applicazione remota del contesto di errore BG** (0x7) se l'errore è stato generato dall'applicazione a cui viene passato il file di caricamento. Includere questa intestazione solo se il codice motivo non è 200 o 201.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la sessione è per un processo di caricamento-risposta, potrebbe verificarsi un ritardo prima che il client riceva l'ACK finale per la risposta del **frammento** . La lunghezza del ritardo dipende dalla quantità di tempo richiesta dall'applicazione server (applicazione a cui il server invia il file di caricamento) per generare la risposta.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Creazione sessione**](create-session.md)
</dt> <dt>

[**Frammento**](fragment.md)
</dt> </dl>

 

 





