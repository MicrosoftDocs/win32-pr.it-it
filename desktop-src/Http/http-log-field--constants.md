---
title: Costanti HTTP_LOG_FIELD_ (http. h)
description: Definire i campi nel registro W3C e nei log degli errori.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301379"
---
# <a name="http_log_field_-constants"></a><span data-ttu-id="71c4d-103">\_ \_ Costanti campi del log http \_</span><span class="sxs-lookup"><span data-stu-id="71c4d-103">HTTP\_LOG\_FIELD\_ Constants</span></span>

<span data-ttu-id="71c4d-104">Le costanti dei campi di **\_ \_ \_ log http** definiscono i campi nel registro W3C e nei log degli errori.</span><span class="sxs-lookup"><span data-stu-id="71c4d-104">The **HTTP\_LOG\_FIELD\_** constants define the fields in the W3C log and the error logs.</span></span>

<span data-ttu-id="71c4d-105">Queste costanti vengono utilizzate nella struttura di [**\_ \_ informazioni di registrazione http**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="71c4d-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="71c4d-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_ \_ data campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**HTTP\_LOG\_FIELD\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-107">Data in cui si è verificata l'attività.</span><span class="sxs-lookup"><span data-stu-id="71c4d-107">The date on which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_ \_ ora campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HTTP\_LOG\_FIELD\_TIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-109">Ora, in formato UTC (Coordinated Universal Time), in cui si è verificata l'attività.</span><span class="sxs-lookup"><span data-stu-id="71c4d-109">The time, in coordinated universal time (UTC), at which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_ \_ \_ IP client campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP\_LOG\_FIELD\_CLIENT\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-111">Indirizzo IP del client che ha eseguito la richiesta.</span><span class="sxs-lookup"><span data-stu-id="71c4d-111">The IP address of the client that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_ \_ \_ nome utente campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**HTTP\_LOG\_FIELD\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-113">Nome dell'utente autenticato che ha eseguito l'accesso al server.</span><span class="sxs-lookup"><span data-stu-id="71c4d-113">The name of the authenticated user who accessed your server.</span></span> <span data-ttu-id="71c4d-114">Gli utenti anonimi sono indicati da un trattino.</span><span class="sxs-lookup"><span data-stu-id="71c4d-114">Anonymous users are indicated by a hyphen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_ \_ \_ nome sito campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP\_LOG\_FIELD\_SITE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-116">Nome del sito in cui è stata generata la voce del file di log.</span><span class="sxs-lookup"><span data-stu-id="71c4d-116">The name of the site on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Http \_ \_ \_ \_ nome computer campo Registro**</span><span class="sxs-lookup"><span data-stu-id="71c4d-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span> **HTTP\_LOG\_FIELD\_COMPUTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-118">Nome del computer in cui è stata generata la voce del file di log.</span><span class="sxs-lookup"><span data-stu-id="71c4d-118">The name of the computer on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_IP del \_ server del campo di log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="71c4d-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP\_LOG\_FIELD\_SERVER\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-120">Indirizzo IP del server in cui è stata generata la voce del file di log.</span><span class="sxs-lookup"><span data-stu-id="71c4d-120">The IP address of the server on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_ \_ Metodo campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP\_LOG\_FIELD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-122">Azione richiesta, ad esempio, un metodo Get.</span><span class="sxs-lookup"><span data-stu-id="71c4d-122">The requested action, for example, a get method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Http \_ \_ \_ \_ radice URI campo Registro**</span><span class="sxs-lookup"><span data-stu-id="71c4d-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span> **HTTP\_LOG\_FIELD\_URI\_STEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-124">Destinazione dell'azione, ad esempio Default.htm.</span><span class="sxs-lookup"><span data-stu-id="71c4d-124">The target of the action, for example, Default.htm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_ \_ \_ query URI campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP\_LOG\_FIELD\_URI\_QUERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-126">Eventuale query che il client sta tentando di eseguire.</span><span class="sxs-lookup"><span data-stu-id="71c4d-126">The query, if any, that the client was trying to perform.</span></span> <span data-ttu-id="71c4d-127">Una query URI è necessaria solo per le pagine dinamiche.</span><span class="sxs-lookup"><span data-stu-id="71c4d-127">A Universal Resource Identifier (URI) query is necessary only for dynamic pages.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_ \_ stato campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**HTTP\_LOG\_FIELD\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-129">Codice di stato HTTP.</span><span class="sxs-lookup"><span data-stu-id="71c4d-129">The HTTP status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_ \_ \_ Stato Win32 campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**HTTP\_LOG\_FIELD\_WIN32\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-131">Codice di stato di Windows.</span><span class="sxs-lookup"><span data-stu-id="71c4d-131">The Windows status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_byte del campo di log http \_ \_ \_ inviati**</span><span class="sxs-lookup"><span data-stu-id="71c4d-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**HTTP\_LOG\_FIELD\_BYTES\_SENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-133">Numero, in byte, inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="71c4d-133">The number, in bytes, sent by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_ \_ byte campo registro \_ http \_ ricezione**</span><span class="sxs-lookup"><span data-stu-id="71c4d-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP\_LOG\_FIELD\_BYTES\_RECV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-135">Numero, in byte, ricevuto dal server.</span><span class="sxs-lookup"><span data-stu-id="71c4d-135">The number, in bytes, received by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**\_ \_ tempo campo registro \_ http \_ impiegato**</span><span class="sxs-lookup"><span data-stu-id="71c4d-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**HTTP\_LOG\_FIELD\_TIME\_TAKEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-137">Tempo, in millisecondi, dell'azione.</span><span class="sxs-lookup"><span data-stu-id="71c4d-137">The time, in milliseconds, of the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_porta del \_ server del campo di log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="71c4d-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP\_LOG\_FIELD\_SERVER\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-139">Numero di porta del server configurato per il servizio.</span><span class="sxs-lookup"><span data-stu-id="71c4d-139">The server port number that is configured for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Http \_ \_ \_ \_ agente utente campo di log**</span><span class="sxs-lookup"><span data-stu-id="71c4d-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span> **HTTP\_LOG\_FIELD\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-141">Applicazione utilizzata dal client.</span><span class="sxs-lookup"><span data-stu-id="71c4d-141">The application that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_ \_ cookie campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP\_LOG\_FIELD\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-143">Contenuto del cookie inviato o ricevuto, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="71c4d-143">The content of the cookie sent or received, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_ \_ riferimento campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP\_LOG\_FIELD\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-145">Sito che l'utente ha visitato per ultimo.</span><span class="sxs-lookup"><span data-stu-id="71c4d-145">The site that the user last visited.</span></span> <span data-ttu-id="71c4d-146">Questo sito fornisce un collegamento al sito corrente.</span><span class="sxs-lookup"><span data-stu-id="71c4d-146">This site provided a link to the current site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_ \_ versione campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP\_LOG\_FIELD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-148">Versione del protocollo HTTP utilizzata dal client.</span><span class="sxs-lookup"><span data-stu-id="71c4d-148">The HTTP protocol version that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_ \_ host campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP\_LOG\_FIELD\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-150">Nome dell'intestazione host, se presente.</span><span class="sxs-lookup"><span data-stu-id="71c4d-150">The host header name, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_ \_ \_ stato secondario campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**HTTP\_LOG\_FIELD\_SUB\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-152">Codice di errore dello stato secondario.</span><span class="sxs-lookup"><span data-stu-id="71c4d-152">The substatus error code.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="71c4d-153">Per la registrazione degli errori HTTP vengono utilizzate le costanti seguenti.</span><span class="sxs-lookup"><span data-stu-id="71c4d-153">The following constants are used for HTTP error logging.</span></span>

<dl> <dt>

<span data-ttu-id="71c4d-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_ \_ \_ porta client campo di log http \_**</span><span class="sxs-lookup"><span data-stu-id="71c4d-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP\_LOG\_FIELD\_CLIENT\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-155">Numero di porta client da cui viene ricevuta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="71c4d-155">The client port number from which the request is received.</span></span> <span data-ttu-id="71c4d-156">Questo campo di log viene usato solo per la registrazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="71c4d-156">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_ \_ URI campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP\_LOG\_FIELD\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-158">URI ricevuto nella richiesta, inclusa la parte della query.</span><span class="sxs-lookup"><span data-stu-id="71c4d-158">The URI received in the request including the query portion.</span></span> <span data-ttu-id="71c4d-159">Questo campo di log viene usato solo per la registrazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="71c4d-159">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_ \_ \_ ID sito campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**HTTP\_LOG\_FIELD\_SITE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-161">ID numerico specifico dell'applicazione del gruppo di URL in cui viene indirizzata la richiesta.</span><span class="sxs-lookup"><span data-stu-id="71c4d-161">The application-specific numeric ID of the URL Group on which the request is routed.</span></span> <span data-ttu-id="71c4d-162">Questo campo di log viene usato solo per la registrazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="71c4d-162">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_ \_ motivo campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**HTTP\_LOG\_FIELD\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-164">La frase del motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="71c4d-164">The error reason phrase.</span></span> <span data-ttu-id="71c4d-165">Questo campo di log viene usato solo per la registrazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="71c4d-165">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_ \_ \_ nome coda campo registro \_ http**</span><span class="sxs-lookup"><span data-stu-id="71c4d-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP\_LOG\_FIELD\_QUEUE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-167">Nome della coda di richieste a cui viene inviata la richiesta.</span><span class="sxs-lookup"><span data-stu-id="71c4d-167">The name of the request queue to which the request is dispatched.</span></span> <span data-ttu-id="71c4d-168">Questo campo di log viene usato solo per la registrazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="71c4d-168">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71c4d-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_campo registro \_ http \_ STREAMID**</span><span class="sxs-lookup"><span data-stu-id="71c4d-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP\_LOG\_FIELD\_STREAMID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71c4d-170">ID del flusso.</span><span class="sxs-lookup"><span data-stu-id="71c4d-170">The stream id.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71c4d-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71c4d-171">Requirements</span></span>



| <span data-ttu-id="71c4d-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="71c4d-172">Requirement</span></span> | <span data-ttu-id="71c4d-173">Valore</span><span class="sxs-lookup"><span data-stu-id="71c4d-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71c4d-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71c4d-174">Minimum supported client</span></span><br/> | <span data-ttu-id="71c4d-175">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71c4d-175">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71c4d-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71c4d-176">Minimum supported server</span></span><br/> | <span data-ttu-id="71c4d-177">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71c4d-177">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71c4d-178">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71c4d-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="71c4d-179"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="71c4d-179"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71c4d-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71c4d-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c4d-181">Costanti API server HTTP versione 2,0</span><span class="sxs-lookup"><span data-stu-id="71c4d-181">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="71c4d-182">**\_informazioni di registrazione http \_**</span><span class="sxs-lookup"><span data-stu-id="71c4d-182">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="71c4d-183">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="71c4d-183">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="71c4d-184">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="71c4d-184">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="71c4d-185">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="71c4d-185">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="71c4d-186">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="71c4d-186">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





