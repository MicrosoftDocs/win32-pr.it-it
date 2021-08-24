---
title: Ack for Cancel-Session
description: Usare L'Ack per Cancel-Session pacchetto per confermare la richiesta Cancel-Session client. Il server invia il riconoscimento dopo il rilascio di tutte le risorse associate alla sessione di caricamento.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Ack per Cancel-Session BITS
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23de0b23b0b87f559326c37ad61ecd09c38f697f0be48b45e92f5e7389b09fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588821"
---
# <a name="ack-for-cancel-session"></a>Ack for Cancel-Session

Usare il **pacchetto Ack for Cancel-Session** per confermare la richiesta [**cancel-session del**](cancel-session.md) client. Il server invia il riconoscimento dopo il rilascio di tutte le risorse associate alla sessione di caricamento.

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

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID stringa che identifica la sessione al client. Sostituire {guid} con l'identificatore di sessione inviato dal client nel [**pacchetto di richiesta Cancel-Session.**](cancel-session.md) Se non si riconosce l'identificatore di sessione, impostare l'intestazione BITS-Error-Code su BG \_ E \_ SESSION NOT \_ \_ FOUND.

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

Sostituire error-context con un numero esadecimale che rappresenta il contesto in cui si è verificato l'errore. Specificare il numero esadecimale [](/windows/win32/api/bits/ne-bits-bg_error_context) per BG_ERROR_CONTEXT_REMOTE_FILE (0x5) se il server ha generato l'errore. In caso contrario, specificare il numero esadecimale per **BG \_ ERROR CONTEXT REMOTE \_ \_ \_ APPLICATION** (0x7) se l'errore è stato generato dall'applicazione a cui viene passato il file di caricamento. Includere questa intestazione solo se il codice motivo non è 200 o 201.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il client BITS invia di nuovo il pacchetto [**Cancel-Session**](cancel-session.md) se il codice motivo è compreso nell'intervallo da 500 a 599, a meno che l'intestazione BITS-Error-Code non sia presente con un valore BG \_ E SESSION NOT \_ \_ \_ FOUND. Il client non riprova per i codici motivo da 100 a 499.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ack for Close-Session**](ack-for-close-session.md)
</dt> <dt>

[**Annulla sessione**](cancel-session.md)
</dt> </dl>

 

 




