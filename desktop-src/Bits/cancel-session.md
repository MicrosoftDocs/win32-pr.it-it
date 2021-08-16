---
title: Cancel-Session
description: Usare il Cancel-Session per terminare la sessione di caricamento con il server BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session BITS
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d570a49d1a5ba632fbbb453b6397338af70d29b0dc837db12193d2889c867eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835110"
---
# <a name="cancel-session"></a>Cancel-Session

Usare il **pacchetto Cancel-Session** per terminare la sessione di caricamento con il server BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo specifico di BITS che identifica questo pacchetto per il server BITS.

Sostituire remote-URL con l'URI assoluto o relativo. In genere, sostituire remote-URL con il nome file remoto del processo. Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-Host-Id nel [**pacchetto Create-Session.**](create-session.md)

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>TIPO DI PACCHETTO BITS
</dt> <dd>

Identifica questo pacchetto di richiesta come Cancel-Session pacchetto.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID stringa che identifica la sessione nel server. Sostituire {guid} con l'identificatore di sessione restituito dal server nel pacchetto di risposta [**Ack for Create-Session.**](ack-for-create-session.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo pacchetto annulla un processo di caricamento se viene inviato prima dell'invio dell'ultimo frammento. Cancel-Session non ha alcun effetto su un file il cui ultimo frammento è già stato inviato. Quando il server BITS riceve l'ultimo frammento, scrive il file nella destinazione finale e, in caso di upload-reply, invia il file all'applicazione server. Nel caso di upload-reply, il pacchetto Cancel-Session annulla la parte di risposta di un processo di caricamento/risposta.

Il server BITS rilascia tutte le risorse ed elimina tutti i file temporanei quando riceve questo pacchetto.

Il client BITS invia questo pacchetto quando l'utente annulla il processo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ack for Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Chiudi sessione**](close-session.md)
</dt> </dl>

 

 




