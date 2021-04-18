---
title: URL
description: Gli elementi dell'API URL WWSAPI forniscono meccanismi per suddividere e non eseguire l'escape degli URL in parti componente e per eseguire l'escape e combinare le parti componente in un URL.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- Servizi Web URL per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: 6f8c895f4d43c4463f6f33fa8014c5de413ece1f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/20/2020
ms.locfileid: "106299499"
---
# <a name="url"></a>URL

Gli elementi dell'API URL WWSAPI forniscono meccanismi per suddividere e non eseguire l'escape degli URL in parti componente e per eseguire l'escape e combinare le parti componente in un URL.

-   Per suddividere e non eseguire l'escape degli URL in parti del componente, usare la funzione [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .
-   Per eseguire l'escape e combinare le parti del componente in un URL, usare la funzione [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .
-   Per combinare URL relativi con un URL di base assoluto che costituisce un URL assoluto, usare la funzione [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .

Le enumerazioni seguenti fanno parte dell'URL:

-   [**\_flag WS URL \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [**\_tipo di \_ schema \_ URL WS**](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

Le funzioni seguenti fanno parte dell'URL:

-   [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

Le strutture seguenti fanno parte dell'URL:

-   [**URL di WS \_ https \_**](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [**\_URL http \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [**URL di WS \_ combinazione NetPipe \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**URL di WS \_ NetTcp \_**](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [**URL di WS \_ SOAPUDP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [**\_URL WS**](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




