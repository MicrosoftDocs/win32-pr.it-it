---
title: Chiamate di procedure remote con RPC tramite HTTP
description: I programmi del browser Internet utilizzano comunemente il protocollo HTTP (Hypertext Transport Protocol) come mezzo principale per esplorare il World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- RPC (Remote Procedure Call), attività, utilizzo di RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955065"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Chiamate di procedure remote con RPC tramite HTTP

I programmi del browser Internet utilizzano comunemente il protocollo HTTP (Hypertext Transport Protocol) come mezzo principale per esplorare il World Wide Web. Il protocollo HTTP, quindi, rileva un utilizzo estensivo nella maggior parte dei computer. Microsoft ha esteso le funzionalità di Internet Information Server (IIS) per fornire servizi RPC (Remote Procedure Call) tramite HTTP.

L'implementazione di Microsoft RPC su HTTP (RPC su HTTP) consente ai client RPC di connettersi in modo sicuro ed efficiente attraverso Internet ai programmi server RPC ed eseguire chiamate a procedure remote. Questa operazione viene eseguita con l'ausilio di un intermediario noto come proxy RPC-over-HTTP o semplicemente del proxy RPC.

Il proxy RPC viene eseguito in un computer IIS. Accetta le richieste RPC provenienti da Internet, esegue l'autenticazione, la convalida e i controlli di accesso su tali richieste. se la richiesta supera tutti i test, il proxy RPC inoltra la richiesta al server RPC che esegue l'elaborazione effettiva. Con RPC su HTTP, il client e il server RPC non comunicano direttamente; usano invece il proxy RPC come intermediario. Questo modello è stato scelto per diversi motivi. Per ulteriori informazioni, vedere la pagina relativa alla [sicurezza RPC su http](rpc-over-http-security.md).

In questa sezione viene fornita una panoramica di RPC su HTTP negli argomenti seguenti:

-   [Utilizzo di HTTP come trasporto RPC](using-http-as-an-rpc-transport.md)
-   [Sicurezza RPC su HTTP](rpc-over-http-security.md)
-   [Requisiti di sistema e interoperabilità per RPC su HTTP](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Configurazione dei computer per RPC su HTTP](configuring-computers-for-rpc-over-http.md)
-   [Raccomandazioni sulla distribuzione RPC su HTTP](rpc-over-http-deployment-recommendations.md)

Per informazioni sugli scenari RPC con volume elevato su HTTP, vedere [Microsoft RPC Load Balancing](rpc-load-balancing.md).

 

 




