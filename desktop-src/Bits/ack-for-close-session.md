---
title: ACK per Close-Session
description: Usare ACK per Close-Session pacchetto per confermare la richiesta di Close-Session del client. Il server invia il riconoscimento dopo il rilascio di tutte le risorse associate alla sessione di caricamento.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- ACK per Close-Session BITS
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7142bfd8d1d5d65d1f669a328c75a2c8cdfb036
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104118642"
---
# <a name="ack-for-close-session"></a>ACK per Close-Session

Usare ACK per il pacchetto di **chiusura sessione** per confermare la richiesta di [**chiusura della sessione**](close-session.md) del client. Il server invia il riconoscimento dopo il rilascio di tutte le risorse associate alla sessione di caricamento.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>codice motivo
</dt> <dd>

Sostituire Reason-Code con il codice motivo HTTP. Ad esempio, impostare Reason-Code su 200 in caso di esito positivo. Per un elenco di codici motivo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-Descrizione
</dt> <dd>

Sostituire Reason-Description con la descrizione HTTP associata al codice motivo. Ad esempio, impostare Reason-Description su OK se Reason-Code è 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto
</dt> <dd>

Identifica il pacchetto di risposta come pacchetto ACK.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID
</dt> <dd>

GUID di stringa che identifica la sessione per il client. Sostituire {GUID} con l'identificatore di sessione inviato dal client nel pacchetto di richiesta di [**chiusura della sessione**](close-session.md) . Se non si riconosce l'identificatore di sessione, impostare l'intestazione BITS-Error-Code su BG \_ E la \_ sessione \_ non \_ trovata.

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

Il client BITS invia nuovamente il pacchetto di [**chiusura della sessione**](close-session.md) se il codice motivo è compreso nell'intervallo da 500 a 599, a meno che non sia presente l'intestazione bits-error-code con un valore di BG \_ E \_ Session \_ non \_ trovato. Il client non tenterà di eseguire un nuovo tentativo per i codici motivo da 100 a 499.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACK per la sessione di annullamento**](ack-for-cancel-session.md)
</dt> <dt>

[**Chiudi sessione**](close-session.md)
</dt> </dl>

 

 




