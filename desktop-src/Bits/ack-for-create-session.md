---
title: ACK per Create-Session
description: Usare ACK per Create-Session pacchetto per confermare la richiesta di Create-Session del client.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- ACK per Create-Session BITS
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "106300669"
---
# <a name="ack-for-create-session"></a>ACK per Create-Session

Usare ACK per il pacchetto di **creazione sessione** per confermare la richiesta di [**creazione sessione**](create-session.md) del client.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>codice motivo
</dt> <dd>

Sostituire Reason-Code con il codice motivo HTTP. La tabella seguente illustra i codici motivo tipici per una risposta a una richiesta di [**creazione sessione**](create-session.md) . Per un elenco di codici motivo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Codice motivo    | Descrizione                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | OK. La richiesta è stata completata.<br/>                                          |
| 201<br/> | Creazione riuscita. La sessione è stata creata.<br/>                                        |
| 403<br/> | Non consentito. L'utente non è autorizzato a caricare i file nell'URL specificato.<br/> |
| 404<br/> | Non trovato. L'URL specificato non esiste.<br/>                             |
| 409<br/> | Conflitto. Il file esiste nel server e non può essere sovrascritto.<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-Descrizione
</dt> <dd>

Sostituire Reason-Description con la descrizione HTTP associata al codice motivo. Ad esempio, impostare Reason-Description su OK se Reason-Code è 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto
</dt> <dd>

Identifica il pacchetto di risposta come pacchetto ACK.

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-protocollo
</dt> <dd>

GUID di stringa che identifica il protocollo che il server vuole usare per questa sessione. Sostituire {GUID} con l'identificatore di protocollo dall'elenco dei protocolli inclusi dal client nella richiesta di [**creazione sessione**](create-session.md) . l'intestazione BITS-supported-Protocol contiene l'elenco. Includere questa intestazione solo se il codice motivo è 200 o 201.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID
</dt> <dd>

GUID di stringa che identifica questa sessione con il client. Sostituire {GUID} con l'identificatore di sessione inviato dal client in tutti i pacchetti di richiesta successivi.

BITS usa un GUID per identificare la sessione, ma è possibile usare qualsiasi stringa HTTP-Legal fino a 100 caratteri.

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BIT-host-ID
</dt> <dd>

facoltativo. Includere questa intestazione solo se è impostata la [Proprietà estensione IIS BITS](bits-iis-extension-properties.md), BITSHostId. Sostituire PublicHostName con il nome o l'indirizzo IP del server della proprietà BITSHostId.

Il client deve sostituire la parte server dell'URL remoto in tutti i pacchetti successivi. Se il client non specifica questo nome host nei pacchetti successivi, è possibile che il processo venga riavviato in un altro server della farm, lasciando un file di caricamento parziale nel server precedente.

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-host-ID-fallback-timeout
</dt> <dd>

facoltativo. Includere questa intestazione solo se è specificata l'intestazione BITS-host-ID. Sostituire timeout con il valore di timeout della proprietà BITSHostIdFallbackTimeout. La proprietà BITSHostIdFallbackTimeout è una delle [proprietà dell'estensione IIS BITS](bits-iis-extension-properties.md).

Il client usa il periodo di timeout per determinare il tempo che tenta di riconnettersi al nome del server specificato nell'intestazione BITS-host-ID prima di ripristinare il nome host specificato nel nome file remoto del processo. Il timer inizia quando BITS non è in grado di connettersi al server BITS-host-ID. Il timer viene reimpostato quando viene ripristinata una connessione al server. Se non viene specificato un periodo di timeout, il client non viene mai ripristinato al nome host specificato nel nome file remoto.

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding
</dt> <dd>

Identifica lo schema di codifica da utilizzare per i frammenti inviati al server. Il pacchetto del frammento contiene il frammento codificato nel corpo del pacchetto. Il server BITS richiede la codifica dell'identità (testo normale). Includere questa intestazione solo se il codice motivo è 200 o 201.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza del contenuto
</dt> <dd>

Sostituire length con il numero di byte inclusi nel corpo della risposta. Obbligatorio anche se il corpo della risposta non include il contenuto.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-errore-codice
</dt> <dd>

Sostituire error-code con un numero esadecimale che rappresenta un valore HRESULT associato a un errore sul lato server. Includere questa intestazione solo se il codice motivo non è 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-errore-contesto
</dt> <dd>

Sostituire Error-context con un numero esadecimale che rappresenta il contesto in cui si è verificato l'errore. Specificare il numero esadecimale per il [**\_ \_ \_ \_ file remoto del contesto di errore BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se il server ha generato l'errore. In caso contrario, specificare il numero esadecimale per l' **\_ \_ \_ \_ applicazione remota del contesto di errore BG** (0x7) se l'errore è stato generato dall'applicazione a cui viene passato il file di caricamento. Includere questa intestazione solo se il codice motivo non è 200 o 201.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Creazione sessione**](create-session.md)
</dt> </dl>

 

 





