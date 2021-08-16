---
title: Ack per Close-Session
description: Usare Ack per Close-Session pacchetto per confermare la richiesta Close-Session client. Il server invia il riconoscimento dopo il rilascio di tutte le risorse associate alla sessione di caricamento.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Ack per Close-Session BITS
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289f2cfc2ca9f1e879e0aa592af28d86ae433f6e06d007aa71e00581baba2af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835414"
---
# <a name="ack-for-close-session"></a>Ack per Close-Session

Usare il **pacchetto Ack for Close-Session** per confermare la richiesta [**close-session del**](close-session.md) client. Il server invia il riconoscimento dopo il rilascio di tutte le risorse associate alla sessione di caricamento.

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

<span id="reason-code"></span><span id="REASON-CODE"></span>reason-code
</dt> <dd>

Sostituire il codice motivo con il codice motivo HTTP. Ad esempio, impostare il codice motivo su 200 in caso di esito positivo. Per un elenco dei codici motivo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Sostituire reason-description con la descrizione HTTP associata al codice motivo. Ad esempio, impostare reason-description su OK se il codice motivo è 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica questo pacchetto di risposta come pacchetto Ack.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-ID
</dt> <dd>

GUID stringa che identifica la sessione al client. Sostituire {guid} con l'identificatore di sessione inviato dal client nel [**pacchetto di richiesta Close-Session.**](close-session.md) Se non si riconosce l'identificatore di sessione, impostare l'intestazione BITS-Error-Code su BG \_ E \_ SESSION NOT \_ \_ FOUND.

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

Il client BITS invia nuovamente il pacchetto [**Close-Session**](close-session.md) se il codice motivo è compreso nell'intervallo da 500 a 599, a meno che l'intestazione BITS-Error-Code non sia presente con un valore BG \_ E SESSION NOT \_ \_ \_ FOUND. Il client non ritenterà i codici motivo da 100 a 499.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ack per Cancel-Session**](ack-for-cancel-session.md)
</dt> <dt>

[**Chiudi sessione**](close-session.md)
</dt> </dl>

 

 




