---
title: Ping
description: Usare il pacchetto Ping per stabilire una connessione e negoziare la sicurezza con il server.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Ping BITS
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479e03e6e18c0ec7421bd225744c5181029fc2b2e220f35c7bae7a3b02d42b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004891"
---
# <a name="ping"></a>Ping

Usare il **pacchetto Ping** per stabilire una connessione e negoziare la sicurezza con il server.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo specifico di BITS che identifica il pacchetto al server BITS.

Sostituire remote-URL con l'URI assoluto o relativo. In genere, sostituire remote-URL con il nome file remoto del processo.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifica questo pacchetto di richiesta come pacchetto Ping.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **pacchetto Ping** è facoltativo. Anziché inviare un **pacchetto Ping,** è possibile usare [**il pacchetto Create-Session**](create-session.md) per stabilire una connessione e negoziare la sicurezza. Tuttavia, è più efficiente usare il **pacchetto Ping** a questo scopo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ack for Ping**](ack-for-ping.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




