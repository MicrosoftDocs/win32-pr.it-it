---
description: Gli indirizzi di trasporto (XAddrs) inclusi nei messaggi ProbeMatches e ResolveMatches sono soggetti alla convalida di base prima che WSDAPI invii un messaggio HTTP, ad esempio una richiesta di metadati.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Regole di convalida XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226797"
---
# <a name="xaddr-validation-rules"></a>Regole di convalida XAddr

Gli indirizzi di trasporto (XAddrs) inclusi nei messaggi [ProbeMatches](probematches-message.md) e [ResolveMatches](resolvematches-message.md) sono soggetti alla convalida di base prima che WSDAPI invii un messaggio http, ad esempio una richiesta di metadati.

Per assicurarsi che XAddrs si trovino nella stessa subnet del client.

Nel codice XML seguente viene illustrato un elemento XAddrs di esempio. Il prefisso WSD si riferisce allo spazio dei nomi `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

Tutte le condizioni seguenti devono essere soddisfatte prima che il messaggio HTTP venga spostato in transito.

-   XAddrs deve essere un indirizzo HTTP o HTTPS. XAddrs di altri schemi vengono ignorati.
-   Se sono presenti XAddrs HTTPS, tutti i XAddrs devono essere HTTPS. Le sezioni XAddr che includono indirizzi HTTP e HTTPS vengono completamente ignorate. Inoltre, l'indirizzo endpoint del dispositivo deve corrispondere esattamente a HTTPS XAddrs.
-   XAddrs deve essere costituito da indirizzi IP o nomi host risolvibili tramite DNS. In genere, vengono usati gli indirizzi IP.
-   Almeno un indirizzo IP incluso in XAddrs (o indirizzo IP risolto da un nome host incluso in XAddrs) deve trovarsi nella stessa subnet dell'adapter su cui è stato ricevuto il messaggio [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) .
-   L'indirizzo e la porta specificati nel primo XAddr devono essere accessibili. WSDAPI tenta di connettersi a questo indirizzo quando si stabilisce una connessione HTTP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ProbeMatches](probematches-message.md)
</dt> <dt>

[ResolveMatches](resolvematches-message.md)
</dt> <dt>

[Modelli di messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



