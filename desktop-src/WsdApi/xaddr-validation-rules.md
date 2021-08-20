---
description: Gli indirizzi di trasporto (XAddrs) inclusi nei messaggi ProbeMatches e ResolveMatches sono soggetti alla convalida di base prima che WSDAPI invii un messaggio HTTP, ad esempio una richiesta di metadati.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Regole di convalida XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3b167101b6012bcf20779381993cfff4ea7ea22d35eef5397ac1349baa2cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049509"
---
# <a name="xaddr-validation-rules"></a>Regole di convalida XAddr

Gli indirizzi di trasporto (XAddrs) inclusi nei [messaggi ProbeMatches](probematches-message.md) e [ResolveMatches](resolvematches-message.md) sono soggetti alla convalida di base prima che WSDAPI invii un messaggio HTTP, ad esempio una richiesta di metadati.

Ciò consente di assicurarsi che gli XAddrs si trovano nella stessa subnet del client.

Il codice XML seguente illustra un elemento XAddrs di esempio. Il prefisso wsd fa riferimento allo spazio dei nomi `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

Prima che il messaggio HTTP venga inviato in transito, è necessario che siano soddisfatte tutte le condizioni seguenti.

-   XAddrs deve essere un indirizzo HTTP o HTTPS. Gli elementi XAddr di altri schemi vengono ignorati.
-   Se sono presenti XAddr HTTPS, tutti gli XAddrs devono essere HTTPS. Le sezioni XAddr che includono indirizzi HTTP e HTTPS vengono completamente ignorate. Inoltre, l'indirizzo dell'endpoint del dispositivo deve corrispondere esattamente a HTTPS XAddrs.
-   XAddrs deve essere indirizzi IP o nomi host risolvibili tramite DNS. In genere, vengono usati indirizzi IP.
-   Almeno un indirizzo IP incluso in XAddrs (o indirizzo IP risolto da un nome host incluso in XAddrs) deve essere nella stessa subnet della scheda su cui è stato ricevuto il messaggio [ProbeMatches](probematches-message.md) o [ResolveMatches.](resolvematches-message.md)
-   L'indirizzo e la porta specificati nel primo XAddr devono essere accessibili. WSDAPI tenta di connettersi a questo indirizzo quando si stabilisce una connessione HTTP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ProbeMatches](probematches-message.md)
</dt> <dt>

[ResolveMatches](resolvematches-message.md)
</dt> <dt>

[Criteri di individuazione e Exchange dei messaggi](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



