---
title: Ack for Ping
description: Usare il pacchetto Ack for Ping per confermare la richiesta Ping del client.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- Ack for Ping BITS
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f31850599331027f3f8135a42dac8c8ea54519c04291d42fb06b5c7b8735fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835181"
---
# <a name="ack-for-ping"></a>Ack for Ping

Usare il **pacchetto Ack for Ping** per confermare la richiesta Ping [**del**](ping.md) client.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>codice motivo
</dt> <dd>

Sostituire reason-code con il codice motivo HTTP. Ad esempio, impostare il codice motivo su 200 in caso di esito positivo. Per un elenco dei codici motivo HTTP, vedere [RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt)

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Sostituire reason-description con la descrizione HTTP associata al codice motivo. Ad esempio, impostare reason-description su OK se il codice motivo è 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>TIPO DI PACCHETTO BITS
</dt> <dd>

Identifica questo pacchetto di risposta come pacchetto Ack.

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

[**Ping**](ping.md)
</dt> </dl>

 

 




