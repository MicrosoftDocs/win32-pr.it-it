---
title: Create-Session
description: Usare il pacchetto Create-Session per richiedere una sessione di caricamento con il server BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- BIT Create-Session
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471859"
---
# <a name="create-session"></a>Create-Session

Usare il pacchetto di **creazione sessione** per richiedere una sessione di caricamento con il server BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_post BITS
</dt> <dd>

Verbo specifico di BITS che identifica il pacchetto nel server BITS.

Sostituire Remote-URL con l'URI assoluto o relativo. In genere, sostituire Remote-URL con il nome file remoto del processo. Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-host-ID.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto
</dt> <dd>

Identifica il pacchetto della richiesta come pacchetto di Create-Session.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-Supported-Protocols
</dt> <dd>

Elenco delimitato da spazi dei protocolli supportati dal client. Usare i GUID di stringa per identificare i protocolli. Specificare l'elenco in ordine di preferenza, dal più o meno preferibile. La tabella seguente elenca il protocollo supportato dal client BITS. Sostituisci {guid1}... {guidn} con uno o più GUID di stringa dall'elenco.



| Protocollo                                          | Descrizione                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | Protocollo di caricamento BITS 1,5<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È necessario inviare un pacchetto [**ping**](ping.md) per stabilire una connessione HTTP prima di inviare il pacchetto di Create-Session. Il pacchetto di Create-Session può inoltre stabilire la connessione. Tuttavia, il pacchetto di Create-Session è meno efficiente.

Il server seleziona il protocollo che si vuole usare dall'elenco fornito dal client nell'intestazione BITS-Supported-Protocols. Il server restituisce il protocollo selezionato nell'intestazione BITS-Protocol del ACK per il pacchetto di risposta di [**creazione-sessione**](ack-for-create-session.md) .

Il client prevede che il server restituisca un ACK per il pacchetto di risposta [**di creazione sessione**](ack-for-create-session.md) . Se il server è stato in grado di stabilire una sessione, il client usa il pacchetto di richiesta del [**frammento**](fragment.md) per inviare gli intervalli del file al server.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACK per create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Frammento**](fragment.md)
</dt> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 





