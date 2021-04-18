---
title: Ping
description: Usare il pacchetto ping per stabilire una connessione e negoziare la sicurezza con il server.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- BIT ping
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "106299269"
---
# <a name="ping"></a>Ping

Usare il pacchetto **ping** per stabilire una connessione e negoziare la sicurezza con il server.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_post BITS
</dt> <dd>

Verbo specifico di BITS che identifica il pacchetto nel server BITS.

Sostituire Remote-URL con l'URI assoluto o relativo. In genere, sostituire Remote-URL con il nome file remoto del processo.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto
</dt> <dd>

Identifica il pacchetto di richiesta come un pacchetto ping.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il pacchetto **ping** è facoltativo. Anziché inviare un pacchetto **ping** , è possibile usare il pacchetto [**create-Session**](create-session.md) per stabilire una connessione e negoziare la sicurezza. Tuttavia, è più efficiente usare il pacchetto **ping** a questo scopo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACK per ping**](ack-for-ping.md)
</dt> <dt>

[**Creazione sessione**](create-session.md)
</dt> </dl>

 

 




