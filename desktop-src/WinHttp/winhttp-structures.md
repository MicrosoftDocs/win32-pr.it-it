---
description: In questo argomento vengono identificate le strutture utilizzate da WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Strutture WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f09615e721b9d34243bd20074e83837e48a6803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226104"
---
# <a name="winhttp-structures"></a><span data-ttu-id="655ec-103">Strutture WinHTTP</span><span class="sxs-lookup"><span data-stu-id="655ec-103">WinHTTP structures</span></span>

<span data-ttu-id="655ec-104">WinHTTP usa le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="655ec-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="655ec-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="655ec-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="655ec-106">Contiene la versione HTTP globale.</span><span class="sxs-lookup"><span data-stu-id="655ec-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="655ec-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="655ec-108">Contiene le parti costituenti di un URL.</span><span class="sxs-lookup"><span data-stu-id="655ec-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="655ec-109">Questa struttura viene utilizzata con le funzioni [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) e [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .</span><span class="sxs-lookup"><span data-stu-id="655ec-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="655ec-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="655ec-111">Contiene il risultato di una chiamata a una funzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="655ec-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="655ec-112">Questa struttura viene utilizzata con il prototipo [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="655ec-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="655ec-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="655ec-114">Usato per indicare alla funzione [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) se specificare l'URL del file di configurazione automatica del proxy (PAC) o per individuare automaticamente l'URL con le query DHCP o DNS nella rete.</span><span class="sxs-lookup"><span data-stu-id="655ec-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="655ec-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="655ec-116">Contiene le informazioni sul certificato restituite dal server.</span><span class="sxs-lookup"><span data-stu-id="655ec-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="655ec-117">Questa struttura viene utilizzata dalla funzione [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) .</span><span class="sxs-lookup"><span data-stu-id="655ec-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-118">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="655ec-118">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="655ec-119">Contiene l'indirizzo IP di origine e di destinazione della richiesta che ha generato la risposta.</span><span class="sxs-lookup"><span data-stu-id="655ec-119">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-120">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="655ec-120">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="655ec-121">Contiene informazioni sulle credenziali utente usate per l'autenticazione del server e del proxy.</span><span class="sxs-lookup"><span data-stu-id="655ec-121">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="655ec-122">Questa struttura è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="655ec-122">This structure has been deprecated.</span></span> <span data-ttu-id="655ec-123">È invece consigliabile utilizzare la struttura [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) .</span><span class="sxs-lookup"><span data-stu-id="655ec-123">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-124">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="655ec-124">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="655ec-125">Contiene informazioni sulle credenziali utente usate per l'autenticazione del server e del proxy.</span><span class="sxs-lookup"><span data-stu-id="655ec-125">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="655ec-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="655ec-127">Contiene le informazioni di configurazione del proxy di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="655ec-127">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-128">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="655ec-128">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="655ec-129">Contiene la configurazione della sessione o del proxy predefinito.</span><span class="sxs-lookup"><span data-stu-id="655ec-129">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-130">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="655ec-130">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="655ec-131">Raccolta di voci di risultati del proxy fornite da [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="655ec-131">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-132">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="655ec-132">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="655ec-133">Una voce di risultato da una chiamata a [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="655ec-133">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-134">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="655ec-134">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="655ec-135">Contiene le statistiche per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="655ec-135">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-136">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="655ec-136">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="655ec-137">Contiene informazioni sull'intervallo per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="655ec-137">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-138">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="655ec-138">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="655ec-139">Contiene informazioni sulla connessione e la crittografia SChannel per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="655ec-139">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="655ec-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="655ec-141">Stato del risultato di un'operazione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="655ec-141">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="655ec-142">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="655ec-142">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="655ec-143">Stato di un'operazione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="655ec-143">Status of a WebSocket operation.</span></span>

</dd> </dl>
