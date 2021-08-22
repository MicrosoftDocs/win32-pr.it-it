---
title: Ack per Create-Session
description: Usare L'Ack per Create-Session pacchetto per confermare la richiesta Create-Session client.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Ack per Create-Session BITS
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dbfcaeab897d55064fe11a506cefbc9d85dd6852a32d279133e6fe7a33a692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588801"
---
# <a name="ack-for-create-session"></a>Ack per Create-Session

Usare il **pacchetto Ack for Create-Session** per confermare la richiesta [**create-session del**](create-session.md) client.

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

Sostituire reason-code con il codice motivo HTTP. La tabella seguente illustra i codici motivo tipici per una risposta a una [**richiesta create-session.**](create-session.md) Per un elenco dei codici motivo HTTP, vedere [RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt)



| Codice motivo    | Descrizione                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | OK. La richiesta è stata completata.<br/>                                          |
| 201<br/> | Creazione riuscita. La sessione è stata creata.<br/>                                        |
| 403<br/> | Non consentito. L'utente non è autorizzato a caricare file nell'URL specificato.<br/> |
| 404<br/> | Non trovato. L'URL specificato non esiste.<br/>                             |
| 409<br/> | Conflitto. Il file esiste nel server e non può essere sovrascritto.<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Sostituire reason-description con la descrizione HTTP associata al codice motivo. Ad esempio, impostare reason-description su OK se il codice motivo è 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>TIPO DI PACCHETTO BITS
</dt> <dd>

Identifica questo pacchetto di risposta come pacchetto Ack.

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>Protocollo BITS
</dt> <dd>

GUID stringa che identifica il protocollo che il server desidera utilizzare per questa sessione. Sostituire {guid} con l'identificatore di protocollo dall'elenco dei protocolli inclusi dal client nella [**richiesta Create-Session;**](create-session.md) L'intestazione BITS-Supported-Protocol contiene l'elenco. Includere questa intestazione solo se il codice motivo è 200 o 201.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID stringa che identifica la sessione al client. Sostituire {guid} con l'identificatore di sessione inviato dal client in tutti i pacchetti di richiesta successivi.

BITS usa un GUID per identificare la sessione, ma è possibile usare qualsiasi stringa valida per HTTP con un massimo di 100 caratteri.

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-Id
</dt> <dd>

facoltativo. Includere questa intestazione solo se è impostata la proprietà [dell'estensione IIS BITS,](bits-iis-extension-properties.md)BITSHostId. Sostituire PublicHostName con il nome del server o l'indirizzo IP della proprietà BITSHostId.

Il client deve sostituire la parte server dell'URL remoto in tutti i pacchetti successivi. Se il client non specifica questo nome host nei pacchetti successivi, è possibile che il processo inizi di nuovo in un altro server della farm, lasciando un file di caricamento parziale nel server precedente.

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout
</dt> <dd>

facoltativo. Includere questa intestazione solo se è specificata l'intestazione BITS-Host-Id. Sostituire Timeout con il valore di timeout della proprietà BITSHostIdFallbackTimeout. La proprietà BITSHostIdFallbackTimeout è una delle proprietà [dell'estensione IIS BITS.](bits-iis-extension-properties.md)

Il client usa il periodo di timeout per determinare per quanto tempo tenta di riconnettersi al nome del server specificato nell'intestazione BITS-Host-Id prima di ripristinare il nome host specificato nel nome file remoto del processo. Il timer inizia quando BITS non riesce a connettersi al server BITS-Host-Id. Il timer viene reimpostato quando viene ripristinata una connessione al server. Se non viene specificato un periodo di timeout, il client non ripristina mai il nome host specificato nel nome file remoto.

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding
</dt> <dd>

Identifica lo schema di codifica da utilizzare sui frammenti inviati al server. Il pacchetto Fragment contiene il frammento codificato nel corpo del pacchetto. Il server BITS richiede la codifica dell'identità (testo non crittografato). Includere questa intestazione solo se il codice motivo è 200 o 201.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza contenuto
</dt> <dd>

Sostituire length con il numero di byte inclusi nel corpo della risposta. Obbligatorio anche se il corpo della risposta non include contenuto.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>CODICE DI ERRORE BITS
</dt> <dd>

Sostituire error-code con un numero esadecimale che rappresenta un valore HRESULT associato a un errore sul lato server. Includere questa intestazione solo se il codice motivo non è 200 o 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>Contesto degli errori BITS
</dt> <dd>

Sostituire error-context con un numero esadecimale che rappresenta il contesto in cui si è verificato l'errore. Specificare il numero esadecimale per [**BG \_ ERROR CONTEXT REMOTE \_ \_ \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se il server ha generato l'errore. In caso contrario, specificare il numero esadecimale per **BG \_ ERROR CONTEXT REMOTE \_ \_ \_ APPLICATION** (0x7) se l'errore è stato generato dall'applicazione a cui viene passato il file di caricamento. Includere questa intestazione solo se il codice motivo non è 200 o 201.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 





