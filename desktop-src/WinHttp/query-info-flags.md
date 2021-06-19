---
description: Questi attributi e modificatori vengono usati da WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Flag di informazioni query (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8a7f95f0e093f175901e4bed30f4055a04b8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396626"
---
# <a name="query-info-flags-winhttph"></a><span data-ttu-id="091ca-103">Flag di informazioni query (Winhttp.h)</span><span class="sxs-lookup"><span data-stu-id="091ca-103">Query Info Flags (Winhttp.h)</span></span>

<span data-ttu-id="091ca-104">Questi attributi e modificatori vengono usati [**da WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="091ca-104">These attributes and modifiers are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

<span data-ttu-id="091ca-105">I flag di attributo vengono usati [**da WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) per indicare le informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="091ca-105">The attribute flags are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to indicate what information to retrieve.</span></span> <span data-ttu-id="091ca-106">La maggior parte dei flag di attributo viene mappata direttamente a un'intestazione HTTP specifica.</span><span class="sxs-lookup"><span data-stu-id="091ca-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="091ca-107">Esistono anche alcuni flag speciali, ad esempio WINHTTP QUERY RAW HEADERS, che non \_ \_ sono correlati a \_ un'intestazione specifica.</span><span class="sxs-lookup"><span data-stu-id="091ca-107">There are also some special flags, such as WINHTTP\_QUERY\_RAW\_HEADERS, that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="091ca-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**ACCETTA QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-109">Recupera i tipi di supporti accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="091ca-109">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ CHARSET**</span><span class="sxs-lookup"><span data-stu-id="091ca-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-111">Recupera i set di caratteri accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="091ca-111">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**CODIFICA WINHTTP \_ QUERY \_ ACCEPT \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-113">Recupera i valori accettabili di codifica del contenuto per la risposta.</span><span class="sxs-lookup"><span data-stu-id="091ca-113">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**LINGUAGGIO DI \_ ACCETTAZIONE \_ QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-115">Recupera i linguaggi naturali accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="091ca-115">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**INTERVALLI DI \_ ACCETTAZIONE \_ QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-117">Recupera i tipi di richieste di intervallo accettate per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="091ca-117">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**PERIODO DI \_ VALIDITÀ DELLE QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-119">Recupera il campo Age response-header , che contiene la stima del mittente del periodo di tempo dopo la generazione della risposta nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="091ca-119">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**CONSENTI QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-121">Riceve i [**verbi HTTP supportati**](glossary.md) dal server.</span><span class="sxs-lookup"><span data-stu-id="091ca-121">Receives the [**HTTP verbs**](glossary.md) supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**INFORMAZIONI \_ SULL'AUTENTICAZIONE DELLE QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP\_QUERY\_AUTHENTICATION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-123">Recupera l'intestazione Authentication-Info personalizzata.</span><span class="sxs-lookup"><span data-stu-id="091ca-123">Retrieves the Authentication-Info header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**AUTORIZZAZIONE DELLE QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-125">Recupera le credenziali di autorizzazione usate per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="091ca-125">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**CONTROLLO DELLA \_ \_ CACHE DI QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-127">Recupera le direttive di controllo della cache.</span><span class="sxs-lookup"><span data-stu-id="091ca-127">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**CONNESSIONE A QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-129">Recupera le opzioni specificate per una determinata connessione e non devono essere comunicate dai proxy su altre connessioni.</span><span class="sxs-lookup"><span data-stu-id="091ca-129">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**BASE DEL CONTENUTO \_ DELLE \_ \_ QUERY WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="091ca-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-131">Recupera l'URI Uniform Resource Identifier di base per risolvere gli URL relativi all'interno dell'entità.</span><span class="sxs-lookup"><span data-stu-id="091ca-131">Retrieves the base Uniform Resource Identifier (URI) to resolve relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**DESCRIZIONE DEL CONTENUTO DELLA QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-133">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="091ca-133">Obsolete.</span></span> <span data-ttu-id="091ca-134">Mantenuta per garantire la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="091ca-134">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**DISPOSIZIONE DEL CONTENUTO DELLE QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-136">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="091ca-136">Obsolete.</span></span> <span data-ttu-id="091ca-137">Mantenuta per garantire la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="091ca-137">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**CODIFICA DEL CONTENUTO DELLE QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-139">Recupera il codice del contenuto aggiuntivo applicato all'intera risorsa.</span><span class="sxs-lookup"><span data-stu-id="091ca-139">Retrieves additional content coding that has been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**ID CONTENUTO QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-141">Recupera l'identificazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="091ca-141">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**LINGUAGGIO DEL CONTENUTO DELLE QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-143">Recupera la lingua in cui è scritto il contenuto.</span><span class="sxs-lookup"><span data-stu-id="091ca-143">Retrieves the language that the content is written in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**LUNGHEZZA CONTENUTO QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-145">Recupera le dimensioni della risorsa, in byte.</span><span class="sxs-lookup"><span data-stu-id="091ca-145">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**PERCORSO DEL CONTENUTO DELLE QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-147">Recupera il percorso della risorsa per l'entità racchiusa nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="091ca-147">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP \_ QUERY \_ CONTENT \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="091ca-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-149">Recupera un digest MD5 del corpo dell'entità allo scopo di fornire un controllo di integrità del messaggio end-to-end per il corpo dell'entità.</span><span class="sxs-lookup"><span data-stu-id="091ca-149">Retrieves an MD5 digest of the entity body for the purpose of providing an end-to-end message integrity check for the entity body.</span></span> <span data-ttu-id="091ca-150">Per altre informazioni, vedere [RFC 1864.](https://www.ietf.org/rfc/rfc1864.txt)</span><span class="sxs-lookup"><span data-stu-id="091ca-150">For more information, see [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**INTERVALLO DI CONTENUTO DI QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-152">Recupera la posizione nel corpo completo dell'entità in cui deve essere inserito il corpo dell'entità parziale e le dimensioni totali del corpo completo dell'entità.</span><span class="sxs-lookup"><span data-stu-id="091ca-152">Retrieves the location in the full entity body where the partial entity body should be inserted and the total size of the full entity body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**CODIFICA DI TRASFERIMENTO \_ \_ DEL CONTENUTO \_ DI QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-154">Recupera una trasformazione di codifica applicabile a un corpo dell'entità.</span><span class="sxs-lookup"><span data-stu-id="091ca-154">Retrieves an encoding transformation applicable to an entity-body.</span></span> <span data-ttu-id="091ca-155">Potrebbe essere già stato applicato, potrebbe essere necessario applicarlo o essere facoltativamente applicabile.</span><span class="sxs-lookup"><span data-stu-id="091ca-155">It may already have been applied, may need to be applied, or may be optionally applicable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**TIPO DI CONTENUTO DI QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-157">Riceve il tipo di contenuto della risorsa, ad esempio text o html.</span><span class="sxs-lookup"><span data-stu-id="091ca-157">Receives the content type of the resource, such as text or html.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**COOKIE \_ DI QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-159">Recupera tutti i cookie associati alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="091ca-159">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**COSTO QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-161">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="091ca-161">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP \_ QUERY \_ CUSTOM**</span><span class="sxs-lookup"><span data-stu-id="091ca-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-163">Consente [**a WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) di cercare il nome dell'intestazione specificato nel *parametro pwszName* e di archiviare le informazioni sull'intestazione in *lpBuffer*.</span><span class="sxs-lookup"><span data-stu-id="091ca-163">Causes [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to search for the header name specified in the *pwszName* parameter and store the header information in *lpBuffer*.</span></span> <span data-ttu-id="091ca-164">Un'applicazione può usare **WINHTTP \_ OPTION RECEIVE RESPONSE TIMEOUT \_ \_ \_ per** limitare il tempo massimo di attesa della query per la ricezione di tutte le intestazioni.</span><span class="sxs-lookup"><span data-stu-id="091ca-164">An application can use **WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT** to limit the maximum time this query waits for all headers to be received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**DATA QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-166">Riceve la data e l'ora di origine del messaggio.</span><span class="sxs-lookup"><span data-stu-id="091ca-166">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**QUERY WINHTTP \_ \_ DERIVATA \_ DA**</span><span class="sxs-lookup"><span data-stu-id="091ca-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**WINHTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-168">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="091ca-168">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP \_ QUERY \_ ETAG**</span><span class="sxs-lookup"><span data-stu-id="091ca-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-170">Recupera il tag di entità per l'entità associata.</span><span class="sxs-lookup"><span data-stu-id="091ca-170">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**PREVISTA QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-172">Recupera l'intestazione Expect, che indica se l'applicazione client deve prevedere risposte serie 100.</span><span class="sxs-lookup"><span data-stu-id="091ca-172">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**LA QUERY WINHTTP \_ \_ SCADE**</span><span class="sxs-lookup"><span data-stu-id="091ca-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-174">Riceve la data e l'ora dopo le quali la risorsa deve essere considerata obsoleta.</span><span class="sxs-lookup"><span data-stu-id="091ca-174">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**QUERY WINHTTP \_ \_ INOLTRATA**</span><span class="sxs-lookup"><span data-stu-id="091ca-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**WINHTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-176">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="091ca-176">Obsolete.</span></span> <span data-ttu-id="091ca-177">Mantenuta per garantire la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="091ca-177">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**QUERY WINHTTP \_ \_ DA**</span><span class="sxs-lookup"><span data-stu-id="091ca-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-179">Recupera l'indirizzo di posta elettronica per l'utente che controlla l'agente [*utente*](glossary.md) richiedente se viene specificata l'intestazione From.</span><span class="sxs-lookup"><span data-stu-id="091ca-179">Retrieves the e-mail address for the user who controls the requesting [*user agent*](glossary.md) if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**HOST \_ DI QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-181">Recupera l'host Internet e il numero di porta della risorsa richiesta.</span><span class="sxs-lookup"><span data-stu-id="091ca-181">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP \_ QUERY \_ IF \_ MATCH**</span><span class="sxs-lookup"><span data-stu-id="091ca-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-183">Recupera il contenuto del campo If-Match di intestazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="091ca-183">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**QUERY WINHTTP \_ \_ SE MODIFICATA \_ \_ DA**</span><span class="sxs-lookup"><span data-stu-id="091ca-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WINHTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-185">Recupera il contenuto dell'intestazione If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="091ca-185">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**QUERY WINHTTP \_ \_ SE NESSUNA \_ \_ CORRISPONDENZA**</span><span class="sxs-lookup"><span data-stu-id="091ca-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WINHTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-187">Recupera il contenuto del campo di intestazione della richiesta If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="091ca-187">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**INTERVALLO DI \_ QUERY \_ WINHTTP \_ IF**</span><span class="sxs-lookup"><span data-stu-id="091ca-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-189">Recupera il contenuto del campo If-Range di intestazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="091ca-189">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="091ca-190">Questa intestazione consente all'applicazione client di verificare se l'entità correlata a una copia parziale dell'entità nella cache dell'applicazione client non è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="091ca-190">This header allows the client application to check if the entity related to a partial copy of the entity in the client application's cache has not been updated.</span></span> <span data-ttu-id="091ca-191">Se l'entità non è stata aggiornata, inviare le parti mancanti nell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="091ca-191">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="091ca-192">Se l'entità è stata aggiornata, inviare l'intera entità aggiornata.</span><span class="sxs-lookup"><span data-stu-id="091ca-192">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP \_ QUERY \_ IF \_ UNMODIFIED \_ SINCE**</span><span class="sxs-lookup"><span data-stu-id="091ca-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-194">Recupera il contenuto del campo di intestazione della richiesta If-Unmodified-Since.</span><span class="sxs-lookup"><span data-stu-id="091ca-194">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**COLLEGAMENTO A QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-196">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="091ca-196">Obsolete.</span></span> <span data-ttu-id="091ca-197">Mantenuta per garantire la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="091ca-197">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**ULTIMA MODIFICA DELLA QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**WINHTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-199">Riceve la data e l'ora dell'ultima modifica della risorsa.</span><span class="sxs-lookup"><span data-stu-id="091ca-199">Receives the date and time at which the resource was last modified.</span></span> <span data-ttu-id="091ca-200">La data e l'ora sono determinate dal server.</span><span class="sxs-lookup"><span data-stu-id="091ca-200">The date and time are determined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**PERCORSO \_ DELLA QUERY \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="091ca-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-202">Recupera l'URI assoluto usato in un'intestazione di risposta Location.</span><span class="sxs-lookup"><span data-stu-id="091ca-202">Retrieves the absolute URI used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP \_ QUERY \_ MAX**</span><span class="sxs-lookup"><span data-stu-id="091ca-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-204">Indica il valore massimo di un valore DI \_ QUERY WINHTTP. \_ \*</span><span class="sxs-lookup"><span data-stu-id="091ca-204">Indicates the maximum value of a WINHTTP\_QUERY\_\* value.</span></span> <span data-ttu-id="091ca-205">Non è un flag di query.</span><span class="sxs-lookup"><span data-stu-id="091ca-205">Not a query flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**NUMERO MASSIMO \_ DI INOLTRO QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-207">Recupera il numero di proxy o gateway che possono inoltrare la richiesta al server in ingresso successivo.</span><span class="sxs-lookup"><span data-stu-id="091ca-207">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**ID DEL MESSAGGIO DI QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-209">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="091ca-209">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**VERSIONE MIME DELLA QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-211">Riceve la versione del Multipurpose Internet Mail Extensions (MIME) utilizzato per costruire il messaggio.</span><span class="sxs-lookup"><span data-stu-id="091ca-211">Receives the version of the Multipurpose Internet Mail Extensions (MIME) protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**URI \_ \_ ORIG DELLA QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-213">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="091ca-213">Obsolete.</span></span> <span data-ttu-id="091ca-214">Mantenuta per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="091ca-214">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**PRAGMA \_ DI QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-216">Riceve le direttive specifiche dell'implementazione che possono essere applicate a qualsiasi destinatario lungo la catena di richiesta/risposta.</span><span class="sxs-lookup"><span data-stu-id="091ca-216">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**AUTENTICAZIONE \_ DEL \_ PROXY DI QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-218">Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal proxy.</span><span class="sxs-lookup"><span data-stu-id="091ca-218">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**AUTORIZZAZIONE \_ DEL PROXY DI QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-220">Recupera l'intestazione utilizzata per identificare l'utente in un proxy che richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="091ca-220">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="091ca-221">Questa intestazione può essere recuperata solo prima che la richiesta venga inviata al server.</span><span class="sxs-lookup"><span data-stu-id="091ca-221">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**CONNESSIONE PROXY DI QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-223">Recupera l'Proxy-Connection personalizzata.</span><span class="sxs-lookup"><span data-stu-id="091ca-223">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**SUPPORTO DEL \_ PROXY DI QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP\_QUERY\_PROXY\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-225">Recupera l'Proxy-Support personalizzata.</span><span class="sxs-lookup"><span data-stu-id="091ca-225">Retrieves the Proxy-Support header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP \_ QUERY \_ PUBLIC**</span><span class="sxs-lookup"><span data-stu-id="091ca-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-227">Riceve i verbi HTTP disponibili in questo server.</span><span class="sxs-lookup"><span data-stu-id="091ca-227">Receives HTTP verbs available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**INTERVALLO DI QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-229">Recupera l'intervallo di byte di un'entità.</span><span class="sxs-lookup"><span data-stu-id="091ca-229">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**INTESTAZIONI NON \_ ELABORATI DELLA QUERY \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="091ca-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-231">Riceve tutte le intestazioni restituite dal server.</span><span class="sxs-lookup"><span data-stu-id="091ca-231">Receives all the headers returned by the server.</span></span> <span data-ttu-id="091ca-232">Ogni intestazione termina con " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="091ca-232">Each header is terminated by "\\0".</span></span> <span data-ttu-id="091ca-233">Un ulteriore " \\ 0" termina l'elenco di intestazioni.</span><span class="sxs-lookup"><span data-stu-id="091ca-233">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**INTESTAZIONI NON ELABORATI DELLA QUERY WINHTTP \_ \_ \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="091ca-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-235">Riceve tutte le intestazioni restituite dal server.</span><span class="sxs-lookup"><span data-stu-id="091ca-235">Receives all the headers returned by the server.</span></span> <span data-ttu-id="091ca-236">Ogni intestazione è separata da una sequenza di ritorno a capo/avanzamento riga (CR/LF).</span><span class="sxs-lookup"><span data-stu-id="091ca-236">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**REFERER DI QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-238">Riceve l'URI della risorsa in cui è stato ottenuto l'URI richiesto.</span><span class="sxs-lookup"><span data-stu-id="091ca-238">Receives the URI of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**AGGIORNAMENTO DI QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-240">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="091ca-240">Obsolete.</span></span> <span data-ttu-id="091ca-241">Mantenuta per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="091ca-241">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**METODO DI RICHIESTA DI QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-243">Riceve il verbo HTTP utilizzato nella richiesta, in genere GET o POST.</span><span class="sxs-lookup"><span data-stu-id="091ca-243">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**RIPETIZIONE DEI TENTATIVI DI QUERY WINHTTP \_ \_ \_ DOPO**</span><span class="sxs-lookup"><span data-stu-id="091ca-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-245">Recupera l'intervallo di tempo previsto per l'indisponibilità del servizio.</span><span class="sxs-lookup"><span data-stu-id="091ca-245">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**SERVER DI QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-247">Recupera informazioni sul software usato dal server di origine per gestire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="091ca-247">Retrieves information about the software used by the originating server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**COOKIE DEL SET DI QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-249">Riceve il valore del cookie impostato per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="091ca-249">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**CODICE DI STATO DELLA QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-251">Riceve il codice di stato restituito dal server.</span><span class="sxs-lookup"><span data-stu-id="091ca-251">Receives the status code returned by the server.</span></span> <span data-ttu-id="091ca-252">Per un elenco dei valori possibili, vedere [**Codici di stato HTTP.**](http-status-codes.md)</span><span class="sxs-lookup"><span data-stu-id="091ca-252">For a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**TESTO DELLO STATO DELLA QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-254">Riceve testo aggiuntivo restituito dal server nella riga di risposta.</span><span class="sxs-lookup"><span data-stu-id="091ca-254">Receives additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**TITOLO \_ DELLA QUERY \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="091ca-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-256">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="091ca-256">Obsolete.</span></span> <span data-ttu-id="091ca-257">Mantenuta per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="091ca-257">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**CODIFICA DI TRASFERIMENTO DI QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-259">Recupera il tipo di trasformazione applicato al corpo del messaggio in modo che possa essere trasferito in modo sicuro tra il mittente e il destinatario.</span><span class="sxs-lookup"><span data-stu-id="091ca-259">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**QUERY WINHTTP \_ A MENO CHE NON VENGA MODIFICATA \_ \_ \_ DA**</span><span class="sxs-lookup"><span data-stu-id="091ca-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WINHTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-261">Recupera l'intestazione Unless-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="091ca-261">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**AGGIORNAMENTO DI QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-263">Recupera i protocolli di comunicazione aggiuntivi supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="091ca-263">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**URI DI QUERY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-265">Riceve parte o tutto l'URI in base al quale è possibile identificare la risorsa REQUEST-URI.</span><span class="sxs-lookup"><span data-stu-id="091ca-265">Receives some or all of the URI by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**AGENTE UTENTE DI QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-267">Recupera informazioni sull'agente utente che ha effettuato la richiesta.</span><span class="sxs-lookup"><span data-stu-id="091ca-267">Retrieves information about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP \_ QUERY \_ VARY**</span><span class="sxs-lookup"><span data-stu-id="091ca-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-269">Recupera l'intestazione che indica che l'entità è stata selezionata da una serie di rappresentazioni disponibili della risposta usando la negoziazione basata su server.</span><span class="sxs-lookup"><span data-stu-id="091ca-269">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**VERSIONE \_ DELLA QUERY \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="091ca-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-271">Recupera la versione HTTP presente nella riga di stato.</span><span class="sxs-lookup"><span data-stu-id="091ca-271">Retrieves the HTTP version that is present in the status line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**QUERY WINHTTP \_ \_ TRAMITE**</span><span class="sxs-lookup"><span data-stu-id="091ca-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-273">Recupera i protocolli intermedi e i destinatari tra l'agente utente e il server nelle richieste e tra il server di origine e il client nelle risposte.</span><span class="sxs-lookup"><span data-stu-id="091ca-273">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**AVVISO DI \_ QUERY \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="091ca-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-275">Recupera informazioni aggiuntive sullo stato di una risposta che potrebbero non essere riflesse dal codice di stato della risposta.</span><span class="sxs-lookup"><span data-stu-id="091ca-275">Retrieves additional information about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**AUTENTICAZIONE WWW DI QUERY WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-277">Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal server.</span><span class="sxs-lookup"><span data-stu-id="091ca-277">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="091ca-278">I flag di modifica vengono usati insieme a un flag di attributo per modificare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="091ca-278">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="091ca-279">I flag di modifica modificano il formato dei dati restituiti o indicano dove la [**funzione WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) deve cercare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="091ca-279">Modifier flags either modify the format of the data returned or indicate where the [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) function should search for the information.</span></span>

<dl> <dt>

<span data-ttu-id="091ca-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**NUMERO DI \_ FLAG DI \_ QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-281">Restituisce i dati come numero a 32 bit per le intestazioni il cui valore è un numero, ad esempio il codice di stato.</span><span class="sxs-lookup"><span data-stu-id="091ca-281">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**INTESTAZIONI DI \_ RICHIESTA DEL FLAG \_ DI QUERY \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="091ca-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-283">Esegue query solo sulle intestazioni delle richieste.</span><span class="sxs-lookup"><span data-stu-id="091ca-283">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091ca-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**FLAG DI QUERY WINHTTP \_ \_ \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="091ca-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091ca-285">Restituisce il valore dell'intestazione come [**struttura SYSTEMTIME,**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) che non richiede all'applicazione di analizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="091ca-285">Returns the header value as a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="091ca-286">Usare per le intestazioni il cui valore è una stringa di data/ora, ad esempio "Last-Modified-Time".</span><span class="sxs-lookup"><span data-stu-id="091ca-286">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="091ca-287"><span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**TRAILER DEI \_ \_ FLAG DI QUERY WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="091ca-287"><span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**WINHTTP\_QUERY\_FLAG\_TRAILERS**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="091ca-288">Esegue query sui trailer di risposta.</span><span class="sxs-lookup"><span data-stu-id="091ca-288">Queries response trailers.</span></span> <span data-ttu-id="091ca-289">Prima di eseguire query sui trailer di risposta, è necessario chiamare [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) fino a quando non restituisce 0 byte letti.</span><span class="sxs-lookup"><span data-stu-id="091ca-289">Prior to querying response trailers, you must call [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) until it returns 0 bytes read.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="091ca-290"><span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**CODIFICA \_ CABLATA \_ DEL FLAG DI QUERY \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="091ca-290"><span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**WINHTTP\_QUERY\_FLAG\_WIRE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="091ca-291">Per impostazione predefinita, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) esegue una conversione Unicode prima di restituire l'intestazione su cui è stata eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="091ca-291">By default, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) performs a Unicode conversion before returning the header that was queried.</span></span> <span data-ttu-id="091ca-292">Se questo flag è impostato, WinHttp restituisce l'intestazione al chiamante senza eseguire questa conversione.</span><span class="sxs-lookup"><span data-stu-id="091ca-292">If this flag is set, WinHttp returns the header to the caller without performing this conversion.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="091ca-293">Requisiti</span><span class="sxs-lookup"><span data-stu-id="091ca-293">Requirements</span></span>

| <span data-ttu-id="091ca-294">Requisito</span><span class="sxs-lookup"><span data-stu-id="091ca-294">Requirement</span></span> | <span data-ttu-id="091ca-295">Valore</span><span class="sxs-lookup"><span data-stu-id="091ca-295">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="091ca-296">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="091ca-296">Minimum supported client</span></span> | <span data-ttu-id="091ca-297">Windows XP, Windows 2000 Professional con solo app desktop SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="091ca-297">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>      |
| <span data-ttu-id="091ca-298">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="091ca-298">Minimum supported server</span></span> | <span data-ttu-id="091ca-299">Solo Windows Server 2003, Windows 2000 Server con app desktop SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="091ca-299">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>   |
| <span data-ttu-id="091ca-300">Intestazione</span><span class="sxs-lookup"><span data-stu-id="091ca-300">Header</span></span>                   | <dl> <span data-ttu-id="091ca-301"><dt>Winhttp.h</dt></span><span class="sxs-lookup"><span data-stu-id="091ca-301"><dt>Winhttp.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="091ca-302">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="091ca-302">See also</span></span>

* [<span data-ttu-id="091ca-303">Versioni di WinHTTP</span><span class="sxs-lookup"><span data-stu-id="091ca-303">WinHTTP Versions</span></span>](winhttp-versions.md)
