---
title: Codici di stato HTTP (WinInet. h)
description: La tabella seguente contiene le costanti e i valori corrispondenti per i codici di stato HTTP restituiti dai server su Internet.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6933617b0488e059c029dd783af238a3ddbb3ecb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400907"
---
# <a name="http-status-codes-winineth"></a><span data-ttu-id="e29dd-103">Codici di stato HTTP (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="e29dd-103">HTTP Status Codes (Wininet.h)</span></span>

<span data-ttu-id="e29dd-104">La tabella seguente contiene le costanti e i valori corrispondenti per i codici di stato HTTP restituiti dai server su Internet.</span><span class="sxs-lookup"><span data-stu-id="e29dd-104">The following table contains the constants and corresponding values for the HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="e29dd-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_stato http \_ continua**</span><span class="sxs-lookup"><span data-stu-id="e29dd-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-106">100</span><span class="sxs-lookup"><span data-stu-id="e29dd-106">100</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-107">La richiesta può essere continuata.</span><span class="sxs-lookup"><span data-stu-id="e29dd-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocolli del \_ cambio di stato http \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-109">101</span><span class="sxs-lookup"><span data-stu-id="e29dd-109">101</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-110">Il server ha cambiato i protocolli in un'intestazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e29dd-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**\_stato http \_ OK**</span><span class="sxs-lookup"><span data-stu-id="e29dd-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-112">200</span><span class="sxs-lookup"><span data-stu-id="e29dd-112">200</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-113">La richiesta è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="e29dd-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_stato http \_ creato**</span><span class="sxs-lookup"><span data-stu-id="e29dd-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-115">201</span><span class="sxs-lookup"><span data-stu-id="e29dd-115">201</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-116">La richiesta è stata soddisfatta e ha causato la creazione di una nuova risorsa.</span><span class="sxs-lookup"><span data-stu-id="e29dd-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_stato http \_ accettato**</span><span class="sxs-lookup"><span data-stu-id="e29dd-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-118">202</span><span class="sxs-lookup"><span data-stu-id="e29dd-118">202</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-119">La richiesta è stata accettata per l'elaborazione, ma l'elaborazione non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e29dd-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**\_stato http \_ parziale**</span><span class="sxs-lookup"><span data-stu-id="e29dd-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-121">203</span><span class="sxs-lookup"><span data-stu-id="e29dd-121">203</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-122">Le metainformazioni restituite nell'intestazione dell'entità non sono il set definitivo disponibile dal server di origine.</span><span class="sxs-lookup"><span data-stu-id="e29dd-122">The returned meta information in the entity-header is not the definitive set available from the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_stato http \_ nessun \_ contenuto**</span><span class="sxs-lookup"><span data-stu-id="e29dd-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-124">204</span><span class="sxs-lookup"><span data-stu-id="e29dd-124">204</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-125">Il server ha completato la richiesta, ma non sono presenti nuove informazioni da restituire.</span><span class="sxs-lookup"><span data-stu-id="e29dd-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_contenuto della \_ reimpostazione dello stato http \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-127">205</span><span class="sxs-lookup"><span data-stu-id="e29dd-127">205</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-128">La richiesta è stata completata e il programma client deve reimpostare la visualizzazione del documento che ha causato l'invio della richiesta per consentire all'utente di avviare facilmente un'altra azione di input.</span><span class="sxs-lookup"><span data-stu-id="e29dd-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_contenuto parziale dello stato http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-130">206</span><span class="sxs-lookup"><span data-stu-id="e29dd-130">206</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-131">Il server ha completato la richiesta di GET parziale per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e29dd-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_stato http \_ ambiguo**</span><span class="sxs-lookup"><span data-stu-id="e29dd-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-133">300</span><span class="sxs-lookup"><span data-stu-id="e29dd-133">300</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-134">Il server non è riuscito a decidere cosa restituire.</span><span class="sxs-lookup"><span data-stu-id="e29dd-134">The server couldn't decide what to return.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_stato http \_ spostato**</span><span class="sxs-lookup"><span data-stu-id="e29dd-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-136">301</span><span class="sxs-lookup"><span data-stu-id="e29dd-136">301</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-137">La risorsa richiesta è stata assegnata a un nuovo URI permanente (Uniform Resource Identifier) e tutti i riferimenti futuri a questa risorsa devono essere eseguiti usando uno degli URI restituiti.</span><span class="sxs-lookup"><span data-stu-id="e29dd-137">The requested resource has been assigned to a new permanent URI (Uniform Resource Identifier), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_Reindirizzamento stato \_ http**</span><span class="sxs-lookup"><span data-stu-id="e29dd-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-139">302</span><span class="sxs-lookup"><span data-stu-id="e29dd-139">302</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-140">La risorsa richiesta risiede temporaneamente in un URI diverso (Uniform Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="e29dd-140">The requested resource resides temporarily under a different URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_metodo di \_ Reindirizzamento \_ stato http**</span><span class="sxs-lookup"><span data-stu-id="e29dd-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-142">303</span><span class="sxs-lookup"><span data-stu-id="e29dd-142">303</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-143">La risposta alla richiesta si trova in un URI diverso (Uniform Resource Identifier) e deve essere recuperata usando un verbo HTTP GET su tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="e29dd-143">The response to the request can be found under a different URI (Uniform Resource Identifier) and should be retrieved using a GET HTTP verb on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_stato http \_ non \_ modificato**</span><span class="sxs-lookup"><span data-stu-id="e29dd-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-145">304</span><span class="sxs-lookup"><span data-stu-id="e29dd-145">304</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-146">La risorsa richiesta non è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="e29dd-146">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_ \_ Usa proxy per lo stato http \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-148">305</span><span class="sxs-lookup"><span data-stu-id="e29dd-148">305</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-149">È necessario accedere alla risorsa richiesta tramite il proxy fornito dal campo location.</span><span class="sxs-lookup"><span data-stu-id="e29dd-149">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_ \_ verbo Keep del reindirizzamento dello stato \_ http \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-151">307</span><span class="sxs-lookup"><span data-stu-id="e29dd-151">307</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-152">La richiesta reindirizzata mantiene lo stesso verbo HTTP.</span><span class="sxs-lookup"><span data-stu-id="e29dd-152">The redirected request keeps the same HTTP verb.</span></span> <span data-ttu-id="e29dd-153">Comportamento HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="e29dd-153">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_richiesta non \_ valida di stato http \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-155">400</span><span class="sxs-lookup"><span data-stu-id="e29dd-155">400</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-156">La richiesta non è stata elaborata dal server a causa di una sintassi non valida.</span><span class="sxs-lookup"><span data-stu-id="e29dd-156">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**\_stato http \_ negato**</span><span class="sxs-lookup"><span data-stu-id="e29dd-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-158">401</span><span class="sxs-lookup"><span data-stu-id="e29dd-158">401</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-159">La risorsa richiesta prevede l'autenticazione degli utenti.</span><span class="sxs-lookup"><span data-stu-id="e29dd-159">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_ \_ req pagamento stato \_ http**</span><span class="sxs-lookup"><span data-stu-id="e29dd-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-161">402</span><span class="sxs-lookup"><span data-stu-id="e29dd-161">402</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-162">Attualmente non implementato nel protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="e29dd-162">Not currently implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**stato HTTP non \_ \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="e29dd-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-164">403</span><span class="sxs-lookup"><span data-stu-id="e29dd-164">403</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-165">Il server ha compreso la richiesta, ma sta rifiutando di soddisfarla.</span><span class="sxs-lookup"><span data-stu-id="e29dd-165">The server understood the request, but is refusing to fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_stato http \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e29dd-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-167">404</span><span class="sxs-lookup"><span data-stu-id="e29dd-167">404</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-168">Il server non ha trovato alcun elemento corrispondente all'URI richiesto (Uniform Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="e29dd-168">The server has not found anything matching the requested URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**Metodo di stato HTTP non \_ \_ valido \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-170">405</span><span class="sxs-lookup"><span data-stu-id="e29dd-170">405</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-171">Il verbo HTTP utilizzato non è consentito.</span><span class="sxs-lookup"><span data-stu-id="e29dd-171">The HTTP verb used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_stato http \_ nessuno \_ accettabile**</span><span class="sxs-lookup"><span data-stu-id="e29dd-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-173">406</span><span class="sxs-lookup"><span data-stu-id="e29dd-173">406</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-174">Non sono state trovate risposte accettabili per il client.</span><span class="sxs-lookup"><span data-stu-id="e29dd-174">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**richiesta \_ di \_ autenticazione proxy di stato \_ http \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-176">407</span><span class="sxs-lookup"><span data-stu-id="e29dd-176">407</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-177">Richiesta autenticazione proxy.</span><span class="sxs-lookup"><span data-stu-id="e29dd-177">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ timeout richiesta stato \_ http**</span><span class="sxs-lookup"><span data-stu-id="e29dd-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-179">408</span><span class="sxs-lookup"><span data-stu-id="e29dd-179">408</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-180">Timeout del server durante l'attesa della richiesta.</span><span class="sxs-lookup"><span data-stu-id="e29dd-180">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflitto stato \_ http**</span><span class="sxs-lookup"><span data-stu-id="e29dd-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-182">409</span><span class="sxs-lookup"><span data-stu-id="e29dd-182">409</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-183">Non è stato possibile completare la richiesta a causa di un conflitto con lo stato corrente della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e29dd-183">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="e29dd-184">L'utente deve inviare nuovamente con ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="e29dd-184">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_stato http \_ andato**</span><span class="sxs-lookup"><span data-stu-id="e29dd-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-186">410</span><span class="sxs-lookup"><span data-stu-id="e29dd-186">410</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-187">La risorsa richiesta non è più disponibile nel server e non è noto alcun indirizzo di spedizione.</span><span class="sxs-lookup"><span data-stu-id="e29dd-187">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_lunghezza stato \_ http \_ obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="e29dd-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-189">411</span><span class="sxs-lookup"><span data-stu-id="e29dd-189">411</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-190">Il server rifiuta di accettare la richiesta senza una lunghezza del contenuto definita.</span><span class="sxs-lookup"><span data-stu-id="e29dd-190">The server refuses to accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_Precond stato http \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="e29dd-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-192">412</span><span class="sxs-lookup"><span data-stu-id="e29dd-192">412</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-193">La precondizione specificata in uno o più campi di intestazione della richiesta ha restituito false quando è stato testato nel server.</span><span class="sxs-lookup"><span data-stu-id="e29dd-193">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_richiesta di stato http \_ \_ troppo \_ grande**</span><span class="sxs-lookup"><span data-stu-id="e29dd-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-195">413</span><span class="sxs-lookup"><span data-stu-id="e29dd-195">413</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-196">Il server rifiuta di elaborare una richiesta perché l'entità della richiesta è più grande di quanto il server sia disposto o in grado di elaborare.</span><span class="sxs-lookup"><span data-stu-id="e29dd-196">The server is refusing to process a request because the request entity is larger than the server is willing or able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI stato \_ http \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="e29dd-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-198">414</span><span class="sxs-lookup"><span data-stu-id="e29dd-198">414</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-199">Il server rifiuta di servire la richiesta perché l'URI della richiesta (Uniform Resource Identifier) è più lungo di quello che il server è disposto a interpretare.</span><span class="sxs-lookup"><span data-stu-id="e29dd-199">The server is refusing to service the request because the request URI (Uniform Resource Identifier) is longer than the server is willing to interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**supporto di stato HTTP non \_ \_ supportato \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-201">415</span><span class="sxs-lookup"><span data-stu-id="e29dd-201">415</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-202">Il server rifiuta di servire la richiesta perché l'entità della richiesta è in un formato non supportato dalla risorsa richiesta per il metodo richiesto.</span><span class="sxs-lookup"><span data-stu-id="e29dd-202">The server is refusing to service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_ \_ tentativo di stato http \_ con**</span><span class="sxs-lookup"><span data-stu-id="e29dd-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-204">449</span><span class="sxs-lookup"><span data-stu-id="e29dd-204">449</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-205">La richiesta deve essere ritentata dopo aver eseguito l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="e29dd-205">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_errore del \_ server di stato http \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-207">500</span><span class="sxs-lookup"><span data-stu-id="e29dd-207">500</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-208">Si è verificata una condizione imprevista che ha impedito al server di completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e29dd-208">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_stato http \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="e29dd-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-210">501</span><span class="sxs-lookup"><span data-stu-id="e29dd-210">501</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-211">Il server non supporta la funzionalità necessaria per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e29dd-211">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**GATEWAY di stato HTTP non \_ \_ valido \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-213">502</span><span class="sxs-lookup"><span data-stu-id="e29dd-213">502</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-214">Il server, che funge da gateway o proxy, ha ricevuto una risposta non valida dal server padre a cui ha effettuato l'accesso nel tentativo di completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e29dd-214">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**servizio di stato HTTP non \_ \_ \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="e29dd-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-216">503</span><span class="sxs-lookup"><span data-stu-id="e29dd-216">503</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-217">Il servizio è momentaneamente sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="e29dd-217">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_timeout del \_ gateway di stato http \_**</span><span class="sxs-lookup"><span data-stu-id="e29dd-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-219">504</span><span class="sxs-lookup"><span data-stu-id="e29dd-219">504</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-220">Richiesta scaduta in attesa di un gateway.</span><span class="sxs-lookup"><span data-stu-id="e29dd-220">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e29dd-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_versione stato \_ http \_ non \_ sup**</span><span class="sxs-lookup"><span data-stu-id="e29dd-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29dd-222">505</span><span class="sxs-lookup"><span data-stu-id="e29dd-222">505</span></span>
</dt> <dt>



<span data-ttu-id="e29dd-223">Il server non supporta o rifiuta di supportare la versione del protocollo HTTP utilizzata nel messaggio di richiesta.</span><span class="sxs-lookup"><span data-stu-id="e29dd-223">The server does not support, or refuses to support, the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e29dd-224">Commenti</span><span class="sxs-lookup"><span data-stu-id="e29dd-224">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e29dd-225">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="e29dd-225">WinINet does not support server implementations.</span></span> <span data-ttu-id="e29dd-226">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="e29dd-226">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e29dd-227">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="e29dd-227">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e29dd-228">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e29dd-228">Requirements</span></span>



| <span data-ttu-id="e29dd-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="e29dd-229">Requirement</span></span> | <span data-ttu-id="e29dd-230">Valore</span><span class="sxs-lookup"><span data-stu-id="e29dd-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e29dd-231">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e29dd-231">Minimum supported client</span></span><br/> | <span data-ttu-id="e29dd-232">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e29dd-232">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e29dd-233">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e29dd-233">Minimum supported server</span></span><br/> | <span data-ttu-id="e29dd-234">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e29dd-234">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e29dd-235">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e29dd-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="e29dd-236"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="e29dd-236"><dt>Wininet.h</dt></span></span> </dl> |



 

