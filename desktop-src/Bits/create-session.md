---
title: Create-Session
description: Usare il Create-Session pacchetto per richiedere una sessione di caricamento con il server BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session BITS
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639db08c5a29b09f5c32d7b0243de66f2c4dced001a1ff2afa7e74837c8d67e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021189"
---
# <a name="create-session"></a>Create-Session

Usare il **pacchetto Create-Session** per richiedere una sessione di caricamento con il server BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo specifico di BITS che identifica il pacchetto al server BITS.

Sostituire remote-URL con l'URI assoluto o relativo. In genere, sostituire remote-URL con il nome file remoto del processo. Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-Host-Id.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica questo pacchetto di richiesta come Create-Session pacchetto.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>Protocolli supportati da BITS
</dt> <dd>

Elenco delimitato da spazi dei protocolli supportati dal client. Usare GUID di stringa per identificare i protocolli. Specificare l'elenco in ordine di preferenza dal più preferito al meno preferito. La tabella seguente elenca il protocollo supportato dal client BITS. Sostituire {guid1} ... {guidN} con uno o più GUID di stringa nell'elenco.



| Protocollo                                          | Descrizione                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | Protocollo Upload BITS 1.5<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È necessario inviare un [**pacchetto Ping**](ping.md) per stabilire una connessione HTTP prima di inviare Create-Session pacchetto. Il Create-Session pacchetto può anche stabilire la connessione. tuttavia, il Create-Session pacchetto è meno efficiente.

Il server seleziona il protocollo che vuole usare dall'elenco fornito dal client nell'intestazione BITS-Supported-Protocols. Il server restituisce il protocollo selezionato nell'intestazione BITS-Protocol del pacchetto di risposta [**Ack for Create-Session.**](ack-for-create-session.md)

Il client prevede che il server restituirà un [**pacchetto di risposta Ack for Create-Session.**](ack-for-create-session.md) Se il server è stato in grado di stabilire una sessione, il client usa il pacchetto di richiesta [**Frammento**](fragment.md) per inviare intervalli del file al server.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ack for Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Frammento**](fragment.md)
</dt> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 





