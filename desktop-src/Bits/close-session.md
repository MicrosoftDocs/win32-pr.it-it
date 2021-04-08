---
title: Close-Session
description: Usare il pacchetto Close-Session per indicare al server BITS che il caricamento del file è stato completato e terminare la sessione.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- BIT Close-Session
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857129"
---
# <a name="close-session"></a>Close-Session

Usare il pacchetto di **chiusura sessione** per indicare al server BITS che il caricamento del file è stato completato e terminare la sessione.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
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

Identifica il pacchetto della richiesta come pacchetto di Close-Session.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID
</dt> <dd>

GUID di stringa che identifica la sessione al server. Sostituire {GUID} con l'identificatore di sessione restituito dal server nell' [**ACK per**](ack-for-create-session.md) il pacchetto di risposta per la creazione della sessione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il server BITS rilascia tutte le risorse ed Elimina tutti i file temporanei al momento della ricezione del pacchetto.

Per i processi di caricamento-risposta, è necessario scaricare la risposta prima di inviare la **sessione di chiusura**. In caso contrario, la risposta viene persa.

Se si invia questo pacchetto prima di caricare tutti i frammenti, il file di caricamento viene eliminato. non è possibile caricare un file parziale.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACK per chiusura sessione**](ack-for-close-session.md)
</dt> <dt>

[**Annulla-sessione**](cancel-session.md)
</dt> <dt>

[**Creazione sessione**](create-session.md)
</dt> </dl>

 

 




