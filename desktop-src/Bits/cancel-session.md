---
title: Cancel-Session
description: Usare il pacchetto Cancel-Session per terminare la sessione di caricamento con il server BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- BIT Cancel-Session
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299055"
---
# <a name="cancel-session"></a>Cancel-Session

Utilizzare il pacchetto **Annulla sessione** per terminare la sessione di caricamento con il server BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_post BITS
</dt> <dd>

Verbo specifico di BITS che identifica il pacchetto nel server BITS.

Sostituire Remote-URL con l'URI assoluto o relativo. In genere, sostituire Remote-URL con il nome file remoto del processo. Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-host-ID nel pacchetto di [**creazione della sessione**](create-session.md) .

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto
</dt> <dd>

Identifica il pacchetto della richiesta come pacchetto di Cancel-Session.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID
</dt> <dd>

GUID di stringa che identifica la sessione al server. Sostituire {GUID} con l'identificatore di sessione restituito dal server nell' [**ACK per**](ack-for-create-session.md) il pacchetto di risposta per la creazione della sessione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo pacchetto Annulla un processo di caricamento se viene inviato prima dell'invio dell'ultimo frammento. Cancel-Session non ha alcun effetto su un file il cui ultimo frammento è già stato inviato. Quando il server BITS riceve l'ultimo frammento, scrive il file nella destinazione finale e, nel caso di upload-Reply, invia il file all'applicazione server. Nel caso di caricamento-risposta, il pacchetto di Cancel-Session Annulla la parte di risposta di un processo di caricamento-risposta.

Il server BITS rilascia tutte le risorse ed Elimina tutti i file temporanei al momento della ricezione del pacchetto.

Il client BITS Invia questo pacchetto quando l'utente annulla il processo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACK per create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Chiudi sessione**](close-session.md)
</dt> </dl>

 

 




