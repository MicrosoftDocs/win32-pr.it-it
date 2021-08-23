---
title: Close-Session
description: Usare il Close-Session pacchetto per indicare al server BITS che il caricamento del file è stato completato e per terminare la sessione.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session BITS
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ae1318a99e690b13f4f0cad03624fb351c359efbcb1be9e105076ce53ceba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021199"
---
# <a name="close-session"></a>Close-Session

Usare il **pacchetto Close-Session** per indicare al server BITS che il caricamento dei file è stato completato e per terminare la sessione.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo specifico di BITS che identifica il pacchetto al server BITS.

Sostituire remote-URL con l'URI assoluto o relativo. In genere, sostituire remote-URL con il nome file remoto del processo. Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-Host-Id nel [**pacchetto Create-Session.**](create-session.md)

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica questo pacchetto di richiesta come Close-Session pacchetto.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-ID
</dt> <dd>

GUID stringa che identifica la sessione nel server. Sostituire {guid} con l'identificatore di sessione restituito dal server nel pacchetto di risposta [**Ack for Create-Session.**](ack-for-create-session.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Il server BITS rilascia tutte le risorse ed elimina tutti i file temporanei quando riceve questo pacchetto.

Per i processi upload-reply, è necessario scaricare la risposta prima di **inviare Close-Session**. In caso contrario, la risposta viene persa.

Se si invia questo pacchetto prima di caricare tutti i frammenti, il file di caricamento viene eliminato. non è possibile caricare un file parziale.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ack for Close-Session**](ack-for-close-session.md)
</dt> <dt>

[**Annulla sessione**](cancel-session.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




