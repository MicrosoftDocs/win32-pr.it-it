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
# <a name="url"></a><span data-ttu-id="314b1-106">URL</span><span class="sxs-lookup"><span data-stu-id="314b1-106">Url</span></span>

<span data-ttu-id="314b1-107">Gli elementi dell'API URL WWSAPI forniscono meccanismi per suddividere e non eseguire l'escape degli URL in parti componente e per eseguire l'escape e combinare le parti componente in un URL.</span><span class="sxs-lookup"><span data-stu-id="314b1-107">The WWSAPI URL API elements provide mechanisms to split and unescape URLs into component parts, and to escape and combine component parts back into a URL.</span></span>

-   <span data-ttu-id="314b1-108">Per suddividere e non eseguire l'escape degli URL in parti del componente, usare la funzione [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .</span><span class="sxs-lookup"><span data-stu-id="314b1-108">To split and unescape URLs into component parts, use the [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) function.</span></span>
-   <span data-ttu-id="314b1-109">Per eseguire l'escape e combinare le parti del componente in un URL, usare la funzione [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .</span><span class="sxs-lookup"><span data-stu-id="314b1-109">To escape and combine component parts back into a URL, use the [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) function.</span></span>
-   <span data-ttu-id="314b1-110">Per combinare URL relativi con un URL di base assoluto che costituisce un URL assoluto, usare la funzione [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .</span><span class="sxs-lookup"><span data-stu-id="314b1-110">To combine relative URLs with an absolute base URL forming an absolute URL, use the [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) function.</span></span>

<span data-ttu-id="314b1-111">Le enumerazioni seguenti fanno parte dell'URL:</span><span class="sxs-lookup"><span data-stu-id="314b1-111">The following enumerations are part of the URL:</span></span>

-   [<span data-ttu-id="314b1-112">**\_flag WS URL \_**</span><span class="sxs-lookup"><span data-stu-id="314b1-112">**WS\_URL\_FLAGS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="314b1-113">**\_tipo di \_ schema \_ URL WS**</span><span class="sxs-lookup"><span data-stu-id="314b1-113">**WS\_URL\_SCHEME\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

<span data-ttu-id="314b1-114">Le funzioni seguenti fanno parte dell'URL:</span><span class="sxs-lookup"><span data-stu-id="314b1-114">The following functions are part of the URL:</span></span>

-   [<span data-ttu-id="314b1-115">**WsCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="314b1-115">**WsCombineUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [<span data-ttu-id="314b1-116">**WsDecodeUrl**</span><span class="sxs-lookup"><span data-stu-id="314b1-116">**WsDecodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [<span data-ttu-id="314b1-117">**WsEncodeUrl**</span><span class="sxs-lookup"><span data-stu-id="314b1-117">**WsEncodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

<span data-ttu-id="314b1-118">Le strutture seguenti fanno parte dell'URL:</span><span class="sxs-lookup"><span data-stu-id="314b1-118">The following structures are part of the URL:</span></span>

-   [<span data-ttu-id="314b1-119">**URL di WS \_ https \_**</span><span class="sxs-lookup"><span data-stu-id="314b1-119">**WS\_HTTPS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [<span data-ttu-id="314b1-120">**\_URL http \_ WS**</span><span class="sxs-lookup"><span data-stu-id="314b1-120">**WS\_HTTP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [<span data-ttu-id="314b1-121">**URL di WS \_ combinazione NetPipe \_**</span><span class="sxs-lookup"><span data-stu-id="314b1-121">**WS\_NETPIPE\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="314b1-122">**URL di WS \_ NetTcp \_**</span><span class="sxs-lookup"><span data-stu-id="314b1-122">**WS\_NETTCP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [<span data-ttu-id="314b1-123">**URL di WS \_ SOAPUDP \_**</span><span class="sxs-lookup"><span data-stu-id="314b1-123">**WS\_SOAPUDP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [<span data-ttu-id="314b1-124">**\_URL WS**</span><span class="sxs-lookup"><span data-stu-id="314b1-124">**WS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




