---
title: Flag informazioni query (WinInet. h)
description: Gli elenchi seguenti contengono gli attributi e i modificatori usati da HttpQueryInfo e QueryInfo.
ms.assetid: b1613193-ae03-411e-bf05-de42f471cd8c
topic_type:
- apiref
api_name:
- HTTP_QUERY_ACCEPT
- HTTP_QUERY_ACCEPT_CHARSET
- HTTP_QUERY_ACCEPT_ENCODING
- HTTP_QUERY_ACCEPT_LANGUAGE
- HTTP_QUERY_ACCEPT_RANGES
- HTTP_QUERY_AGE
- HTTP_QUERY_ALLOW
- HTTP_QUERY_AUTHORIZATION
- HTTP_QUERY_CACHE_CONTROL
- HTTP_QUERY_CONNECTION
- HTTP_QUERY_CONTENT_BASE
- HTTP_QUERY_CONTENT_DESCRIPTION
- HTTP_QUERY_CONTENT_DISPOSITION
- HTTP_QUERY_CONTENT_ENCODING
- HTTP_QUERY_CONTENT_ID
- HTTP_QUERY_CONTENT_LANGUAGE
- HTTP_QUERY_CONTENT_LENGTH
- HTTP_QUERY_CONTENT_LOCATION
- HTTP_QUERY_CONTENT_MD5
- HTTP_QUERY_CONTENT_RANGE
- HTTP_QUERY_CONTENT_TRANSFER_ENCODING
- HTTP_QUERY_CONTENT_TYPE
- HTTP_QUERY_COOKIE
- HTTP_QUERY_COST
- HTTP_QUERY_CUSTOM
- HTTP_QUERY_DATE
- HTTP_QUERY_DERIVED_FROM
- HTTP_QUERY_ECHO_HEADERS
- HTTP_QUERY_ECHO_HEADERS_CRLF
- HTTP_QUERY_ECHO_REPLY
- HTTP_QUERY_ECHO_REQUEST
- HTTP_QUERY_ETAG
- HTTP_QUERY_EXPECT
- HTTP_QUERY_EXPIRES
- HTTP_QUERY_FORWARDED
- HTTP_QUERY_FROM
- HTTP_QUERY_HOST
- HTTP_QUERY_IF_MATCH
- HTTP_QUERY_IF_MODIFIED_SINCE
- HTTP_QUERY_IF_NONE_MATCH
- HTTP_QUERY_IF_RANGE
- HTTP_QUERY_IF_UNMODIFIED_SINCE
- HTTP_QUERY_LAST_MODIFIED
- HTTP_QUERY_LINK
- HTTP_QUERY_LOCATION
- HTTP_QUERY_MAX
- HTTP_QUERY_MAX_FORWARDS
- HTTP_QUERY_MESSAGE_ID
- HTTP_QUERY_MIME_VERSION
- HTTP_QUERY_ORIG_URI
- HTTP_QUERY_PRAGMA
- HTTP_QUERY_PROXY_AUTHENTICATE
- HTTP_QUERY_PROXY_AUTHORIZATION
- HTTP_QUERY_PROXY_CONNECTION
- HTTP_QUERY_PUBLIC
- HTTP_QUERY_RANGE
- HTTP_QUERY_RAW_HEADERS
- HTTP_QUERY_RAW_HEADERS_CRLF
- HTTP_QUERY_REFERER
- HTTP_QUERY_REFRESH
- HTTP_QUERY_REQUEST_METHOD
- HTTP_QUERY_RETRY_AFTER
- HTTP_QUERY_SERVER
- HTTP_QUERY_SET_COOKIE
- HTTP_QUERY_STATUS_CODE
- HTTP_QUERY_STATUS_TEXT
- HTTP_QUERY_TITLE
- HTTP_QUERY_TRANSFER_ENCODING
- HTTP_QUERY_UNLESS_MODIFIED_SINCE
- HTTP_QUERY_UPGRADE
- HTTP_QUERY_URI
- HTTP_QUERY_USER_AGENT
- HTTP_QUERY_VARY
- HTTP_QUERY_VERSION
- HTTP_QUERY_VIA
- HTTP_QUERY_WARNING
- HTTP_QUERY_WWW_AUTHENTICATE
- HTTP_QUERY_X_CONTENT_TYPE_OPTIONS
- HTTP_QUERY_P3P
- HTTP_QUERY_X_P2P_PEERDIST
- HTTP_QUERY_TRANSLATE
- HTTP_QUERY_X_UA_COMPATIBLE
- HTTP_QUERY_DEFAULT_STYLE
- HTTP_QUERY_X_FRAME_OPTIONS
- HTTP_QUERY_X_XSS_PROTECTION
- HTTP_QUERY_FLAG_COALESCE
- HTTP_QUERY_FLAG_NUMBER
- HTTP_QUERY_FLAG_REQUEST_HEADERS
- HTTP_QUERY_FLAG_SYSTEMTIME
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f3a6166c59e158d041e730d2198f6e1b066a8b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302735"
---
# <a name="query-info-flags-winineth"></a><span data-ttu-id="6f3fd-103">Flag informazioni query (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="6f3fd-103">Query Info Flags (Wininet.h)</span></span>

<span data-ttu-id="6f3fd-104">Gli elenchi seguenti contengono gli attributi e i modificatori usati da [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) e [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6f3fd-104">The following lists contain the attributes and modifiers used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) and [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span></span>

<span data-ttu-id="6f3fd-105">I flag di attributo vengono utilizzati da [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (o [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) per indicare quali dati recuperare.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-105">The attribute flags are used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) to indicate what data to retrieve.</span></span> <span data-ttu-id="6f3fd-106">La maggior parte dei flag di attributo è mappata direttamente a un'intestazione HTTP specifica.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="6f3fd-107">Esistono anche alcuni flag speciali, ad esempio le [ \_ \_ \_ intestazioni RAW della query http](/windows), che non sono correlati a un'intestazione specifica.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-107">There are also some special flags, such as [HTTP\_QUERY\_RAW\_HEADERS](/windows), that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="6f3fd-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**\_accettazione query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-109">24</span><span class="sxs-lookup"><span data-stu-id="6f3fd-109">24</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-110">Recupera i tipi di supporto accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-110">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**\_set di \_ caratteri Accept della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-112">25</span><span class="sxs-lookup"><span data-stu-id="6f3fd-112">25</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-113">Recupera i set di caratteri accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-113">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**\_ \_ codifica Accept della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-115">26</span><span class="sxs-lookup"><span data-stu-id="6f3fd-115">26</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-116">Recupera i valori di codifica del contenuto accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-116">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**\_lingua di \_ accettazione \_ query http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-118">27</span><span class="sxs-lookup"><span data-stu-id="6f3fd-118">27</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-119">Recupera i linguaggi naturali accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-119">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**\_intervalli di \_ accettazione \_ query http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**HTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-121">42</span><span class="sxs-lookup"><span data-stu-id="6f3fd-121">42</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-122">Recupera i tipi di richieste di intervallo accettate per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-122">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**\_tempo di query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-124">48</span><span class="sxs-lookup"><span data-stu-id="6f3fd-124">48</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-125">Recupera il campo Age Response-header, che contiene la stima del mittente relativa alla quantità di tempo trascorsa dalla generazione della risposta nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-125">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**\_Consenti query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-127">7</span><span class="sxs-lookup"><span data-stu-id="6f3fd-127">7</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-128">Riceve i verbi HTTP supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-128">Receives the HTTP verbs supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_autorizzazione query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-130">28</span><span class="sxs-lookup"><span data-stu-id="6f3fd-130">28</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-131">Recupera le credenziali di autorizzazione utilizzate per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-131">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_ \_ controllo cache query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-133">49</span><span class="sxs-lookup"><span data-stu-id="6f3fd-133">49</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-134">Recupera le direttive di controllo della cache.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-134">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**\_connessione query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-136">23</span><span class="sxs-lookup"><span data-stu-id="6f3fd-136">23</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-137">Recupera tutte le opzioni specificate per una particolare connessione e non devono essere comunicate tramite proxy tramite ulteriori connessioni.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-137">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**\_ \_ base contenuto query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**HTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-139">50</span><span class="sxs-lookup"><span data-stu-id="6f3fd-139">50</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-140">Recupera l'URI di base (Uniform Resource Identifier) per la risoluzione degli URL relativi nell'entità.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-140">Retrieves the base URI (Uniform Resource Identifier) for resolving relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**\_ \_ Descrizione contenuto query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**HTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-142">4</span><span class="sxs-lookup"><span data-stu-id="6f3fd-142">4</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-143">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-143">Obsolete.</span></span> <span data-ttu-id="6f3fd-144">Gestito solo per compatibilità con le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-144">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**\_disposizione del \_ contenuto della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-146">47</span><span class="sxs-lookup"><span data-stu-id="6f3fd-146">47</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-147">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-147">Obsolete.</span></span> <span data-ttu-id="6f3fd-148">Gestito solo per compatibilità con le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-148">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**\_codifica del \_ contenuto della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**HTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-150">29</span><span class="sxs-lookup"><span data-stu-id="6f3fd-150">29</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-151">Recupera tutte le codifiche di contenuto aggiuntive applicate all'intera risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-151">Retrieves any additional content codings that have been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_ \_ ID contenuto query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**HTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-153">3</span><span class="sxs-lookup"><span data-stu-id="6f3fd-153">3</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-154">Recupera l'identificazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-154">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**\_lingua del \_ contenuto della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**HTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-156">6</span><span class="sxs-lookup"><span data-stu-id="6f3fd-156">6</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-157">Recupera la lingua in cui si trova il contenuto.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-157">Retrieves the language that the content is in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**\_ \_ lunghezza contenuto query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**HTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-159">5</span><span class="sxs-lookup"><span data-stu-id="6f3fd-159">5</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-160">Recupera le dimensioni, in byte, della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-160">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**\_percorso del \_ contenuto della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**HTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-162">51</span><span class="sxs-lookup"><span data-stu-id="6f3fd-162">51</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-163">Recupera il percorso della risorsa per l'entità racchiusa nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-163">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**\_ \_ MD5 contenuto query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-165">52</span><span class="sxs-lookup"><span data-stu-id="6f3fd-165">52</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-166">Recupera un digest MD5 del corpo dell'entità allo scopo di fornire un controllo di integrità dei messaggi end-to-end per il corpo dell'entità.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-166">Retrieves an MD5 digest of the entity-body for the purpose of providing an end-to-end message integrity check (MIC) for the entity-body.</span></span> <span data-ttu-id="6f3fd-167">Per ulteriori informazioni, vedere RFC1864, il campo dell'intestazione Content-MD5, all'indirizzo [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .</span><span class="sxs-lookup"><span data-stu-id="6f3fd-167">For more information, see RFC1864, The Content-MD5 Header Field, at [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_ \_ intervallo contenuto query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**HTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-169">53</span><span class="sxs-lookup"><span data-stu-id="6f3fd-169">53</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-170">Recupera la posizione nel corpo entità completo in cui deve essere inserito il corpo dell'entità parziale e le dimensioni totali del corpo dell'entità completo.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-170">Retrieves the location in the full entity-body where the partial entity-body should be inserted and the total size of the full entity-body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**\_ \_ \_ codifica trasferimento contenuto query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**HTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-172">2</span><span class="sxs-lookup"><span data-stu-id="6f3fd-172">2</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-173">Riceve la codifica del contenuto aggiuntiva applicata alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-173">Receives the additional content coding that has been applied to the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_tipo di \_ contenuto \_ query http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**HTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-175">1</span><span class="sxs-lookup"><span data-stu-id="6f3fd-175">1</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-176">Riceve il tipo di contenuto della risorsa (ad esempio testo/HTML).</span><span class="sxs-lookup"><span data-stu-id="6f3fd-176">Receives the content type of the resource (such as text/html).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_cookie di query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-178">44</span><span class="sxs-lookup"><span data-stu-id="6f3fd-178">44</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-179">Recupera tutti i cookie associati alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-179">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**\_costo query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**HTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-181">15</span><span class="sxs-lookup"><span data-stu-id="6f3fd-181">15</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-182">Non più supportata.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-182">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_query http \_ personalizzata**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**HTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-184">65535</span><span class="sxs-lookup"><span data-stu-id="6f3fd-184">65535</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-185">Fa in modo che [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) cerchi il nome dell'intestazione specificato in *lpvBuffer* e memorizzi i dati dell'intestazione in *lpvBuffer*.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-185">Causes [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to search for the header name specified in *lpvBuffer* and store the header data in *lpvBuffer*.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**\_data query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**HTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-187">9</span><span class="sxs-lookup"><span data-stu-id="6f3fd-187">9</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-188">Riceve la data e l'ora in cui è stato originato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-188">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_query http \_ derivata \_ da**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**HTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-190">14</span><span class="sxs-lookup"><span data-stu-id="6f3fd-190">14</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-191">Non più supportata.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-191">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_ \_ intestazioni echo della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**HTTP\_QUERY\_ECHO\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-193">73</span><span class="sxs-lookup"><span data-stu-id="6f3fd-193">73</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-194">Non implementato attualmente.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-194">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**\_intestazioni echo della query http \_ \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP\_QUERY\_ECHO\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-196">74</span><span class="sxs-lookup"><span data-stu-id="6f3fd-196">74</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-197">Non implementato attualmente.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-197">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**\_ \_ risposta echo query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP\_QUERY\_ECHO\_REPLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-199">72</span><span class="sxs-lookup"><span data-stu-id="6f3fd-199">72</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-200">Non implementato attualmente.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-200">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_ \_ richiesta echo di query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP\_QUERY\_ECHO\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-202">71</span><span class="sxs-lookup"><span data-stu-id="6f3fd-202">71</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-203">Non implementato attualmente.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-203">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**\_ETag query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-205">54</span><span class="sxs-lookup"><span data-stu-id="6f3fd-205">54</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-206">Recupera il tag di entità per l'entità associata.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-206">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_ \_ si prevede che la query http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-208">68</span><span class="sxs-lookup"><span data-stu-id="6f3fd-208">68</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-209">Recupera l'intestazione Expect, che indica se l'applicazione client deve prevedere le risposte della serie 100.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-209">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**\_scadenza della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-211">10</span><span class="sxs-lookup"><span data-stu-id="6f3fd-211">10</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-212">Riceve la data e l'ora in cui la risorsa deve essere considerata obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-212">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_query http \_ avanzata**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**HTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-214">30</span><span class="sxs-lookup"><span data-stu-id="6f3fd-214">30</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-215">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-215">Obsolete.</span></span> <span data-ttu-id="6f3fd-216">Gestito solo per compatibilità con le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-216">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**\_query http \_ da**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-218">31</span><span class="sxs-lookup"><span data-stu-id="6f3fd-218">31</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-219">Recupera l'indirizzo di posta elettronica dell'utente che controlla l'agente utente richiedente se l'intestazione From viene assegnata.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-219">Retrieves the email address for the human user who controls the requesting user agent if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**\_host query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-221">55</span><span class="sxs-lookup"><span data-stu-id="6f3fd-221">55</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-222">Recupera l'host Internet e il numero di porta della risorsa richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-222">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**\_query http \_ se \_ corrisponde**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-224">56</span><span class="sxs-lookup"><span data-stu-id="6f3fd-224">56</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-225">Recupera il contenuto del If-Match campo di intestazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-225">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**\_query http \_ se \_ modificata \_ dopo**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-227">32</span><span class="sxs-lookup"><span data-stu-id="6f3fd-227">32</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-228">Recupera il contenuto dell'intestazione If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-228">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**\_query http \_ se \_ Nessuna \_ corrispondenza**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-230">57</span><span class="sxs-lookup"><span data-stu-id="6f3fd-230">57</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-231">Recupera il contenuto del campo dell'intestazione della richiesta If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-231">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**\_query http \_ se l' \_ intervallo**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-233">58</span><span class="sxs-lookup"><span data-stu-id="6f3fd-233">58</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-234">Recupera il contenuto del If-Range campo di intestazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-234">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="6f3fd-235">Questa intestazione consente all'applicazione client di verificare che l'entità correlata a una copia parziale dell'entità nella cache dell'applicazione client non sia stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-235">This header enables the client application to verify that the entity related to a partial copy of the entity in the client application cache has not been updated.</span></span> <span data-ttu-id="6f3fd-236">Se l'entità non è stata aggiornata, inviare le parti mancanti nell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-236">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="6f3fd-237">Se l'entità è stata aggiornata, inviare l'intera entità aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-237">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**\_query http \_ se non \_ modificata \_ da**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-239">59</span><span class="sxs-lookup"><span data-stu-id="6f3fd-239">59</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-240">Recupera il contenuto del campo di intestazione della richiesta If-Unmodified-Since.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-240">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ Ultima modifica della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**HTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-242">11</span><span class="sxs-lookup"><span data-stu-id="6f3fd-242">11</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-243">Riceve la data e l'ora in cui il server ritiene che la risorsa sia stata modificata per ultima.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-243">Receives the date and time at which the server believes the resource was last modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**\_collegamento query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-245">16</span><span class="sxs-lookup"><span data-stu-id="6f3fd-245">16</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-246">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-246">Obsolete.</span></span> <span data-ttu-id="6f3fd-247">Gestito solo per compatibilità con le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-247">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**\_percorso query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-249">33</span><span class="sxs-lookup"><span data-stu-id="6f3fd-249">33</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-250">Recupera il Uniform Resource Identifier assoluto (URI) utilizzato in un'intestazione di risposta della posizione.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-250">Retrieves the absolute Uniform Resource Identifier (URI) used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**\_Max query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-252">78</span><span class="sxs-lookup"><span data-stu-id="6f3fd-252">78</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-253">Non è un flag di query.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-253">Not a query flag.</span></span> <span data-ttu-id="6f3fd-254">Indica il valore massimo di un \_ valore di query http \_ \* .</span><span class="sxs-lookup"><span data-stu-id="6f3fd-254">Indicates the maximum value of an HTTP\_QUERY\_\* value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ numero massimo di \_ INOLTRi query http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**HTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-256">60</span><span class="sxs-lookup"><span data-stu-id="6f3fd-256">60</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-257">Recupera il numero di proxy o gateway che è in grado di inoltrare la richiesta al server in ingresso successivo.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-257">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ \_ ID messaggio query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**HTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-259">12</span><span class="sxs-lookup"><span data-stu-id="6f3fd-259">12</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-260">Non più supportata.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-260">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_ \_ versione MIME della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-262">0</span><span class="sxs-lookup"><span data-stu-id="6f3fd-262">0</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-263">Riceve la versione del protocollo MIME utilizzato per costruire il messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-263">Receives the version of the MIME protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_ \_ URI orig della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**HTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-265">34</span><span class="sxs-lookup"><span data-stu-id="6f3fd-265">34</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-266">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-266">Obsolete.</span></span> <span data-ttu-id="6f3fd-267">Gestito solo per compatibilità con le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-267">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_pragma query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-269">17</span><span class="sxs-lookup"><span data-stu-id="6f3fd-269">17</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-270">Riceve le direttive specifiche dell'implementazione che potrebbero essere applicabili a qualsiasi destinatario lungo la catena di richiesta/risposta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-270">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_ \_ autenticazione proxy query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-272">41</span><span class="sxs-lookup"><span data-stu-id="6f3fd-272">41</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-273">Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal proxy.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-273">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_ \_ autorizzazione proxy query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-275">61</span><span class="sxs-lookup"><span data-stu-id="6f3fd-275">61</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-276">Recupera l'intestazione utilizzata per identificare l'utente a un proxy che richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-276">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="6f3fd-277">Questa intestazione può essere recuperata solo prima dell'invio della richiesta al server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-277">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_ \_ connessione proxy query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-279">69</span><span class="sxs-lookup"><span data-stu-id="6f3fd-279">69</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-280">Recupera l'intestazione del Proxy-Connection.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-280">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**\_query http \_ pubblica**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**HTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-282">8</span><span class="sxs-lookup"><span data-stu-id="6f3fd-282">8</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-283">Riceve i metodi disponibili in questo server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-283">Receives methods available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**\_intervallo query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-285">62</span><span class="sxs-lookup"><span data-stu-id="6f3fd-285">62</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-286">Recupera l'intervallo di byte di un'entità.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-286">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ intestazioni RAW della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**HTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-288">21</span><span class="sxs-lookup"><span data-stu-id="6f3fd-288">21</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-289">Riceve tutte le intestazioni restituite dal server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-289">Receives all the headers returned by the server.</span></span> <span data-ttu-id="6f3fd-290">Ogni intestazione viene terminata con " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="6f3fd-290">Each header is terminated by "\\0".</span></span> <span data-ttu-id="6f3fd-291">Un " \\ 0" aggiuntivo termina l'elenco di intestazioni.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-291">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**\_intestazioni RAW della query http \_ \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-293">22</span><span class="sxs-lookup"><span data-stu-id="6f3fd-293">22</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-294">Riceve tutte le intestazioni restituite dal server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-294">Receives all the headers returned by the server.</span></span> <span data-ttu-id="6f3fd-295">Ogni intestazione è separata da una sequenza di ritorno a capo/avanzamento riga (CR/LF).</span><span class="sxs-lookup"><span data-stu-id="6f3fd-295">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**\_ \_ Referer query http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-297">35</span><span class="sxs-lookup"><span data-stu-id="6f3fd-297">35</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-298">Riceve il Uniform Resource Identifier (URI) della risorsa in cui è stato ottenuto l'URI richiesto.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-298">Receives the Uniform Resource Identifier (URI) of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**\_aggiornamento query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**HTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-300">46</span><span class="sxs-lookup"><span data-stu-id="6f3fd-300">46</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-301">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-301">Obsolete.</span></span> <span data-ttu-id="6f3fd-302">Gestito solo per compatibilità con le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-302">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**\_metodo di \_ richiesta di query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-304">45</span><span class="sxs-lookup"><span data-stu-id="6f3fd-304">45</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-305">Riceve il verbo HTTP usato nella richiesta, in genere GET o POST.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-305">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**\_tentativo di query http \_ \_ dopo**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-307">36</span><span class="sxs-lookup"><span data-stu-id="6f3fd-307">36</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-308">Recupera l'intervallo di tempo per cui il servizio non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-308">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**\_server di query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-310">37</span><span class="sxs-lookup"><span data-stu-id="6f3fd-310">37</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-311">Recupera i dati sul software utilizzato dal server di origine per gestire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-311">Retrieves data about the software used by the origin server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_cookie del \_ set di query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-313">43</span><span class="sxs-lookup"><span data-stu-id="6f3fd-313">43</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-314">Riceve il valore del set di cookie per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-314">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_codice di \_ stato della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**HTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-316">19</span><span class="sxs-lookup"><span data-stu-id="6f3fd-316">19</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-317">Riceve il codice di stato restituito dal server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-317">Receives the status code returned by the server.</span></span> <span data-ttu-id="6f3fd-318">Per ulteriori informazioni e un elenco di valori possibili, vedere [**codici di stato http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6f3fd-318">For more information and a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**\_ \_ testo stato query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**HTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-320">20</span><span class="sxs-lookup"><span data-stu-id="6f3fd-320">20</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-321">Riceve qualsiasi testo aggiuntivo restituito dal server nella riga di risposta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-321">Receives any additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**\_titolo della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-323">38</span><span class="sxs-lookup"><span data-stu-id="6f3fd-323">38</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-324">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-324">Obsolete.</span></span> <span data-ttu-id="6f3fd-325">Gestito solo per compatibilità con le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-325">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**\_ \_ codifica trasferimento query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-327">63</span><span class="sxs-lookup"><span data-stu-id="6f3fd-327">63</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-328">Recupera il tipo di trasformazione applicato al corpo del messaggio in modo che possa essere trasferito in modo sicuro tra il mittente e il destinatario.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-328">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**\_query http \_ a meno che non venga \_ modificata \_ da**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-330">70</span><span class="sxs-lookup"><span data-stu-id="6f3fd-330">70</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-331">Recupera l'intestazione a meno che non venga modificata.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-331">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**\_aggiornamento query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**HTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-333">64</span><span class="sxs-lookup"><span data-stu-id="6f3fd-333">64</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-334">Recupera i protocolli di comunicazione aggiuntivi supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-334">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_URI query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-336">13</span><span class="sxs-lookup"><span data-stu-id="6f3fd-336">13</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-337">Riceve alcuni o tutti gli URI (Uniform Resource Identifier) in base ai quali è possibile identificare la risorsa Request-URI.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-337">Receives some or all of the Uniform Resource Identifiers (URIs) by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_ \_ agente utente query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**HTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-339">39</span><span class="sxs-lookup"><span data-stu-id="6f3fd-339">39</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-340">Recupera i dati relativi all'agente utente che ha effettuato la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-340">Retrieves data about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**\_variazione query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-342">65</span><span class="sxs-lookup"><span data-stu-id="6f3fd-342">65</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-343">Recupera l'intestazione che indica che l'entità è stata selezionata da un numero di rappresentazioni disponibili della risposta mediante la negoziazione basata su server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-343">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**\_versione query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-345">18</span><span class="sxs-lookup"><span data-stu-id="6f3fd-345">18</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-346">Riceve l'ultimo codice di risposta restituito dal server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-346">Receives the last response code returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**\_query http \_ tramite**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-348">66</span><span class="sxs-lookup"><span data-stu-id="6f3fd-348">66</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-349">Recupera i protocolli intermedi e i destinatari tra l'agente utente e il server nelle richieste e tra il server di origine e il client sulle risposte.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-349">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**\_avviso query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-351">67</span><span class="sxs-lookup"><span data-stu-id="6f3fd-351">67</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-352">Recupera dati aggiuntivi sullo stato di una risposta che potrebbero non essere riflesse dal codice di stato della risposta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-352">Retrieves additional data about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**\_ \_ autenticazione www della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-354">40</span><span class="sxs-lookup"><span data-stu-id="6f3fd-354">40</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-355">Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-355">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_Opzioni del \_ \_ tipo di contenuto query HTTP X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**HTTP\_QUERY\_X\_CONTENT\_TYPE\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-357">79</span><span class="sxs-lookup"><span data-stu-id="6f3fd-357">79</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-358">Recupera il valore dell'intestazione X-Content-Type-Options.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-358">Retrieves the X-Content-Type-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**\_P3P query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP\_QUERY\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-360">80</span><span class="sxs-lookup"><span data-stu-id="6f3fd-360">80</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-361">Recupera il valore dell'intestazione P3P.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-361">Retrieves the P3P header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**\_Query http \_ X \_ \_ PEERDIST P2P**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP\_QUERY\_X\_P2P\_PEERDIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-363">81</span><span class="sxs-lookup"><span data-stu-id="6f3fd-363">81</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-364">Recupera il valore dell'intestazione X-P2P-PeerDist.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-364">Retrieves the X-P2P-PeerDist header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**\_traduzione query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP\_QUERY\_TRANSLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-366">82</span><span class="sxs-lookup"><span data-stu-id="6f3fd-366">82</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-367">Recupera il valore dell'intestazione translate.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-367">Retrieves the translate header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**\_compatibilità con query http \_ X \_ UA \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP\_QUERY\_X\_UA\_COMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-369">83</span><span class="sxs-lookup"><span data-stu-id="6f3fd-369">83</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-370">Recupera il valore dell'intestazione X-UA-Compatible.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-370">Retrieves the X-UA-Compatible header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ stile predefinito query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**HTTP\_QUERY\_DEFAULT\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-372">84</span><span class="sxs-lookup"><span data-stu-id="6f3fd-372">84</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-373">Recupera il valore dell'intestazione Default-Style.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-373">Retrieves the Default-Style header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**\_ \_ \_ Opzioni frame X query \_ http**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP\_QUERY\_X\_FRAME\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-375">85</span><span class="sxs-lookup"><span data-stu-id="6f3fd-375">85</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-376">Recupera il valore dell'intestazione X-frame-options.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-376">Retrieves the X-Frame-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**\_protezione XSS della query http \_ X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP\_QUERY\_X\_XSS\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-378">86</span><span class="sxs-lookup"><span data-stu-id="6f3fd-378">86</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-379">Recupera il valore dell'intestazione X-XSS-Protection.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-379">Retrieves the X-XSS-Protection header value.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="6f3fd-380">I flag di modifica vengono utilizzati in combinazione con un flag di attributo per modificare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-380">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="6f3fd-381">I flag di modifica possono modificare il formato dei dati restituiti o indicare dove [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (o [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) deve cercare i dati.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-381">Modifier flags either modify the format of the data returned or indicate where [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) should search for the data.</span></span>

<dl> <dt>

<span data-ttu-id="6f3fd-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_flag di query http \_ \_ COALESCE**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP\_QUERY\_FLAG\_COALESCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-383">0x10000000</span><span class="sxs-lookup"><span data-stu-id="6f3fd-383">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-384">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-384">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**\_numero di \_ flag della query http \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-386">0x20000000</span><span class="sxs-lookup"><span data-stu-id="6f3fd-386">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-387">Restituisce i dati come numero a 32 bit per le intestazioni il cui valore è un numero, ad esempio il codice di stato.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-387">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_intestazioni di \_ richiesta del flag di query http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-389">0x80000000</span><span class="sxs-lookup"><span data-stu-id="6f3fd-389">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-390">Solo intestazioni della richiesta di query.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-390">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f3fd-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**\_flag di query http \_ \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="6f3fd-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3fd-392">0x40000000</span><span class="sxs-lookup"><span data-stu-id="6f3fd-392">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="6f3fd-393">Restituisce il valore dell'intestazione come struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , che non richiede l'analisi dei dati da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-393">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="6f3fd-394">Utilizzare per le intestazioni il cui valore è una stringa di data/ora, ad esempio "Last-Modified-Time".</span><span class="sxs-lookup"><span data-stu-id="6f3fd-394">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f3fd-395">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f3fd-395">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6f3fd-396">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-396">WinINet does not support server implementations.</span></span> <span data-ttu-id="6f3fd-397">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="6f3fd-397">In addition, it should not be used from a service.</span></span> <span data-ttu-id="6f3fd-398">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="6f3fd-398">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f3fd-399">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f3fd-399">Requirements</span></span>



| <span data-ttu-id="6f3fd-400">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f3fd-400">Requirement</span></span> | <span data-ttu-id="6f3fd-401">Valore</span><span class="sxs-lookup"><span data-stu-id="6f3fd-401">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3fd-402">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f3fd-402">Minimum supported client</span></span><br/> | <span data-ttu-id="6f3fd-403">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f3fd-403">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6f3fd-404">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f3fd-404">Minimum supported server</span></span><br/> | <span data-ttu-id="6f3fd-405">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f3fd-405">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6f3fd-406">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f3fd-406">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f3fd-407"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f3fd-407"><dt>Wininet.h</dt></span></span> </dl> |



 

