---
description: Questo argomento identifica le strutture utilizzate da WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Strutture WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ecf91702a2f49e2c0a754fcc69d9d34febf229
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174981"
---
# <a name="winhttp-structures"></a><span data-ttu-id="e0e8b-103">Strutture WinHTTP</span><span class="sxs-lookup"><span data-stu-id="e0e8b-103">WinHTTP structures</span></span>

<span data-ttu-id="e0e8b-104">WinHTTP usa le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0e8b-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="e0e8b-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="e0e8b-106">Contiene la versione HTTP globale.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="e0e8b-108">Contiene le parti costituenti di un URL.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="e0e8b-109">Questa struttura viene usata con le [**funzioni WinHttpUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) e [**WinHttpCreateUrl.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)</span><span class="sxs-lookup"><span data-stu-id="e0e8b-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="e0e8b-111">Contiene il risultato di una chiamata a una funzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="e0e8b-112">Questa struttura viene usata con il [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototipo.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="e0e8b-114">Usato per indicare alla funzione [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) se specificare l'URL del file di configurazione automatica del proxy o individuare automaticamente l'URL con query DHCP o DNS per la rete.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="e0e8b-116">Contiene le informazioni sul certificato restituite dal server.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="e0e8b-117">Questa struttura viene usata dalla [**funzione WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="e0e8b-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="e0e8b-119">Rappresenta un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="e0e8b-121">Contiene l'indirizzo IP di origine e di destinazione della richiesta che ha generato la risposta.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="e0e8b-123">Contiene le informazioni sulle credenziali utente utilizzate per l'autenticazione del server e del proxy.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="e0e8b-124">Questa struttura è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-124">This structure has been deprecated.</span></span> <span data-ttu-id="e0e8b-125">È invece consigliabile usare [**la WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) struttura .</span><span class="sxs-lookup"><span data-stu-id="e0e8b-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="e0e8b-127">Contiene le informazioni sulle credenziali utente utilizzate per l'autenticazione del server e del proxy.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="e0e8b-129">Contiene le informazioni Internet Explorer configurazione del proxy.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-130">**WINHTTP_EXTENDED_HEADER**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-130">**WINHTTP_EXTENDED_HEADER**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header)
</dt> <dd>

<span data-ttu-id="e0e8b-131">Rappresenta un'intestazione di richiesta HTTP come coppia nome/valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-131">Represents an HTTP request header as a name/value string pair.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-132">**WINHTTP_HEADER_NAME**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-132">**WINHTTP_HEADER_NAME**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)
</dt> <dd>

<span data-ttu-id="e0e8b-133">Rappresenta il nome di un'intestazione di richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-133">Represents an HTTP request header name.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-134">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-134">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="e0e8b-135">Rappresenta una raccolta di gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-135">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-136">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-136">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="e0e8b-137">Rappresenta il GUID di una connessione, ai fini della corrispondenza della connessione.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-137">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-138">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-138">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="e0e8b-139">Contiene la configurazione della sessione o del proxy predefinito.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-139">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-140">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-140">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="e0e8b-141">Raccolta di voci dei risultati del proxy fornite da [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="e0e8b-141">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-142">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-142">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="e0e8b-143">Voce del risultato da una chiamata a [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="e0e8b-143">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="e0e8b-145">Rappresenta una descrizione dello stato corrente delle connessioni di WinHttp.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-145">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-146">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-146">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="e0e8b-147">Contiene statistiche per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-147">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-148">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-148">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="e0e8b-149">Contiene informazioni sull'intervallo per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-149">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-150">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-150">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="e0e8b-151">Contiene informazioni di connessione e crittografia SChannel per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-151">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="e0e8b-153">Stato del risultato di un'operazione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-153">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="e0e8b-154">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="e0e8b-154">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="e0e8b-155">Stato di un'operazione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-155">Status of a WebSocket operation.</span></span>

</dd> </dl>
