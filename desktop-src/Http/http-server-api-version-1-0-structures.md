---
title: Strutture API server HTTP versione 1,0
description: Strutture API server HTTP versione 1,0
ms.assetid: e38f7a05-f966-4853-be3b-5cdbf224719e
keywords:
- Strutture API del server HTTP
- Strutture HTTP, API del server HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67cdd426bbe9329e089352999acf5c0f79b6f94f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398982"
---
# <a name="http-server-api-version-10-structures"></a><span data-ttu-id="e2372-105">Strutture API server HTTP versione 1,0</span><span class="sxs-lookup"><span data-stu-id="e2372-105">HTTP Server API Version 1.0 Structures</span></span>

<span data-ttu-id="e2372-106">L'API server HTTP fornisce le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2372-106">The HTTP Server API provides the following structures:</span></span>

-   [<span data-ttu-id="e2372-107">**versione di HTTPAPI \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-107">**HTTPAPI\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-httpapi_version)
-   [<span data-ttu-id="e2372-108">**\_intervallo di byte http \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-108">**HTTP\_BYTE\_RANGE**</span></span>](/windows/desktop/api/Http/ns-http-http_byte_range)
-   [<span data-ttu-id="e2372-109">**\_criteri della cache HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-109">**HTTP\_CACHE\_POLICY**</span></span>](/windows/desktop/api/Http/ns-http-http_cache_policy)
-   [<span data-ttu-id="e2372-110">**\_URL cotto \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-110">**HTTP\_COOKED\_URL**</span></span>](/windows/desktop/api/Http/ns-http-http_cooked_url)
-   [<span data-ttu-id="e2372-111">**\_blocco di dati http \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-111">**HTTP\_DATA\_CHUNK**</span></span>](/windows/desktop/api/Http/ns-http-http_data_chunk)
-   [<span data-ttu-id="e2372-112">**\_intestazione Nota \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-112">**HTTP\_KNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_known_header)
-   <span data-ttu-id="e2372-113">[**\_richiesta http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e2372-113">[**HTTP\_REQUEST**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span></span>
-   [<span data-ttu-id="e2372-114">**\_intestazioni di richiesta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-114">**HTTP\_REQUEST\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_headers)
-   [<span data-ttu-id="e2372-115">**\_risposta http**</span><span class="sxs-lookup"><span data-stu-id="e2372-115">**HTTP\_RESPONSE**</span></span>](http-response.md)
-   [<span data-ttu-id="e2372-116">**\_intestazioni della risposta http \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-116">**HTTP\_RESPONSE\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_response_headers)
-   [<span data-ttu-id="e2372-117">**\_ \_ \_ \_ parametro ascolto IP di configurazione servizio http \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-117">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_param)
-   [<span data-ttu-id="e2372-118">**\_query di \_ \_ ascolto IP \_ di configurazione servizio http \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-118">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_query)
-   [<span data-ttu-id="e2372-119">**\_ \_ \_ chiave SSL per la configurazione del servizio http \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-119">**HTTP\_SERVICE\_CONFIG\_SSL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_key)
-   [<span data-ttu-id="e2372-120">**\_ \_ \_ param SSL configurazione servizio \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-120">**HTTP\_SERVICE\_CONFIG\_SSL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_param)
-   [<span data-ttu-id="e2372-121">**\_ \_ \_ query SSL configurazione servizio \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-121">**HTTP\_SERVICE\_CONFIG\_SSL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_query)
-   [<span data-ttu-id="e2372-122">**\_configurazione SSL del servizio http \_ \_ \_ impostata**</span><span class="sxs-lookup"><span data-stu-id="e2372-122">**HTTP\_SERVICE\_CONFIG\_SSL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set)
-   [<span data-ttu-id="e2372-123">**\_ \_ \_ \_ chiave SNI SSL configurazione servizio \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-123">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_key)
-   [<span data-ttu-id="e2372-124">**\_ \_ \_ \_ query SNI SSL configurazione servizio \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-124">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_query)
-   [<span data-ttu-id="e2372-125">**\_ \_ \_ \_ set SNI SSL configurazione servizio \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-125">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_set)
-   [<span data-ttu-id="e2372-126">**\_chiave di configurazione del servizio http \_ \_ URLACL \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-126">**HTTP\_SERVICE\_CONFIG\_URLACL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_key)
-   [<span data-ttu-id="e2372-127">**\_ \_ \_ param URLACL configurazione servizio \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-127">**HTTP\_SERVICE\_CONFIG\_URLACL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_param)
-   [<span data-ttu-id="e2372-128">**\_ \_ \_ query URLACL configurazione servizio \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-128">**HTTP\_SERVICE\_CONFIG\_URLACL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_query)
-   [<span data-ttu-id="e2372-129">**\_ \_ \_ set URLACL configurazione servizio \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-129">**HTTP\_SERVICE\_CONFIG\_URLACL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set)
-   [<span data-ttu-id="e2372-130">**\_informazioni sul \_ \_ certificato client SSL HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-130">**HTTP\_SSL\_CLIENT\_CERT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_client_cert_info)
-   [<span data-ttu-id="e2372-131">**\_informazioni SSL \_ http**</span><span class="sxs-lookup"><span data-stu-id="e2372-131">**HTTP\_SSL\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_info)
-   [<span data-ttu-id="e2372-132">**\_indirizzo di trasporto HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-132">**HTTP\_TRANSPORT\_ADDRESS**</span></span>](/windows/desktop/api/Http/ns-http-http_transport_address)
-   [<span data-ttu-id="e2372-133">**\_intestazione HTTP sconosciuta \_**</span><span class="sxs-lookup"><span data-stu-id="e2372-133">**HTTP\_UNKNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_unknown_header)
-   [<span data-ttu-id="e2372-134">**\_versione http**</span><span class="sxs-lookup"><span data-stu-id="e2372-134">**HTTP\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-http_version)

## <a name="related-topics"></a><span data-ttu-id="e2372-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2372-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2372-136">Funzioni API server HTTP versione 1,0</span><span class="sxs-lookup"><span data-stu-id="e2372-136">HTTP Server API Version 1.0 Functions</span></span>](http-server-api-version-1-0-functions.md)
</dt> </dl>

 

 