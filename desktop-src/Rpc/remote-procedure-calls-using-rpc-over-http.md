---
title: Chiamate di procedure remote con RPC tramite HTTP
description: I programmi browser Internet in genere utilizzano il protocollo HTTP (Hypertext Transport Protocol) come mezzo principale per esplorare il World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- RPC remote procedure call , attività, con RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fedeb1700d798a616d3441b356f6f31867eed0399f412ed1f82923bcc4ac5f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101661"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Chiamate di procedure remote con RPC tramite HTTP

I programmi browser Internet in genere utilizzano il protocollo HTTP (Hypertext Transport Protocol) come mezzo principale per esplorare il World Wide Web. HTTP, pertanto, è attualmente ampiamente in uso nella maggior parte dei computer. Microsoft ha esteso le funzionalità di Internet Information Server (IIS) per fornire servizi di chiamata di procedura remota tramite HTTP.

L'implementazione Microsoft RPC-over-HTTP (RPC su HTTP) consente ai client RPC di connettersi in modo sicuro ed efficiente attraverso Internet ai programmi server RPC ed eseguire chiamate di procedura remota. Questa operazione viene eseguita con l'aiuto di un intermediario noto come proxy RPC su HTTP o semplicemente proxy RPC.

Il proxy RPC viene eseguito in un computer IIS. Accetta le richieste RPC provenienti da Internet, esegue l'autenticazione, la convalida e i controlli di accesso su tali richieste e, se la richiesta supera tutti i test, il proxy RPC inoltra la richiesta al server RPC che esegue l'elaborazione effettiva. Con RPC su HTTP, il client e il server RPC non comunicano direttamente; usano invece il proxy RPC come intermediario. Questo modello è stato scelto per molti motivi. Per altre informazioni, vedere [Rpc over HTTP Security](rpc-over-http-security.md).

In questa sezione viene fornita una panoramica di RPC su HTTP negli argomenti seguenti:

-   [Utilizzo di HTTP come trasporto RPC](using-http-as-an-rpc-transport.md)
-   [Sicurezza RPC su HTTP](rpc-over-http-security.md)
-   [Requisiti di sistema e interoperabilità per RPC su HTTP](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Configurazione dei computer per RPC su HTTP](configuring-computers-for-rpc-over-http.md)
-   [Rpc over HTTP Deployment Consigli](rpc-over-http-deployment-recommendations.md)

Per informazioni sugli scenari RPC su HTTP con volumi elevati, vedere [Microsoft RPC Load Balancing](rpc-load-balancing.md).

 

 




