---
description: Questi attributi e modificatori vengono usati da WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Flag informazioni query (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9ffc8f4ba4a947fe6fb277617c99460c43ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050235"
---
# <a name="query-info-flags-winhttph"></a><span data-ttu-id="d4b36-103">Flag informazioni query (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="d4b36-103">Query Info Flags (Winhttp.h)</span></span>

<span data-ttu-id="d4b36-104">Questi attributi e modificatori vengono usati da [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="d4b36-104">These attributes and modifiers are used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

<span data-ttu-id="d4b36-105">I flag di attributo vengono usati da [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) per indicare quali informazioni recuperare.</span><span class="sxs-lookup"><span data-stu-id="d4b36-105">The attribute flags are used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) to indicate what information to retrieve.</span></span> <span data-ttu-id="d4b36-106">La maggior parte dei flag di attributo è mappata direttamente a un'intestazione HTTP specifica.</span><span class="sxs-lookup"><span data-stu-id="d4b36-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="d4b36-107">Esistono anche alcuni flag speciali, ad esempio le \_ intestazioni RAW della query WinHTTP \_ \_ , che non sono correlati a un'intestazione specifica.</span><span class="sxs-lookup"><span data-stu-id="d4b36-107">There are also some special flags, such as WINHTTP\_QUERY\_RAW\_HEADERS, that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="d4b36-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**\_accettazione query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-109">Recupera i tipi di supporto accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-109">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**\_set di \_ caratteri Accept della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-111">Recupera i set di caratteri accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-111">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**\_codifica di \_ accettazione della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-113">Recupera i valori di codifica del contenuto accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-113">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**\_lingua di \_ accettazione \_ query WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-115">Recupera i linguaggi naturali accettabili per la risposta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-115">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**\_intervalli di \_ accettazione della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-117">Recupera i tipi di richieste di intervallo accettate per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="d4b36-117">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**\_tempo di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-119">Recupera il campo Age Response-header, che contiene la stima del mittente relativa alla quantità di tempo trascorsa dalla generazione della risposta nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="d4b36-119">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**\_Consenti query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-121">Riceve il [*verbo http*](glossary.md)s supportato dal server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-121">Receives the [*HTTP verb*](glossary.md)s supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_informazioni di \_ autenticazione della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP\_QUERY\_AUTHENTICATION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-123">Recupera l'intestazione del Authentication-Info.</span><span class="sxs-lookup"><span data-stu-id="d4b36-123">Retrieves the Authentication-Info header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_autorizzazione per query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-125">Recupera le credenziali di autorizzazione utilizzate per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-125">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_ \_ controllo cache query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-127">Recupera le direttive di controllo della cache.</span><span class="sxs-lookup"><span data-stu-id="d4b36-127">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**\_connessione query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-129">Recupera tutte le opzioni specificate per una particolare connessione e non devono essere comunicate tramite proxy tramite ulteriori connessioni.</span><span class="sxs-lookup"><span data-stu-id="d4b36-129">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_ \_ base contenuto query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-131">Recupera la Uniform Resource Identifier di base (URI) per risolvere gli URL relativi nell'entità.</span><span class="sxs-lookup"><span data-stu-id="d4b36-131">Retrieves the base Uniform Resource Identifier (URI) to resolve relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**\_ \_ Descrizione contenuto query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-133">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-133">Obsolete.</span></span> <span data-ttu-id="d4b36-134">Gestito per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="d4b36-134">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_disposizione del \_ contenuto della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-136">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-136">Obsolete.</span></span> <span data-ttu-id="d4b36-137">Gestito per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="d4b36-137">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**\_codifica del \_ contenuto della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-139">Recupera la codifica del contenuto aggiuntiva applicata all'intera risorsa.</span><span class="sxs-lookup"><span data-stu-id="d4b36-139">Retrieves additional content coding that has been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**\_ \_ ID contenuto query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-141">Recupera l'identificazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="d4b36-141">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_lingua del \_ contenuto della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-143">Recupera la lingua in cui è scritto il contenuto.</span><span class="sxs-lookup"><span data-stu-id="d4b36-143">Retrieves the language that the content is written in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**\_ \_ lunghezza contenuto query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-145">Recupera le dimensioni, in byte, della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d4b36-145">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**\_percorso del \_ contenuto della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-147">Recupera il percorso della risorsa per l'entità racchiusa nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="d4b36-147">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**\_ \_ MD5 contenuto query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-149">Recupera un digest MD5 del corpo dell'entità allo scopo di fornire un controllo di integrità dei messaggi end-to-end per il corpo dell'entità.</span><span class="sxs-lookup"><span data-stu-id="d4b36-149">Retrieves an MD5 digest of the entity body for the purpose of providing an end-to-end message integrity check for the entity body.</span></span> <span data-ttu-id="d4b36-150">Per ulteriori informazioni, vedere [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span><span class="sxs-lookup"><span data-stu-id="d4b36-150">For more information, see [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_ \_ intervallo contenuto query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-152">Recupera la posizione nel corpo dell'entità completo in cui deve essere inserito il corpo dell'entità parziale e le dimensioni totali del corpo dell'entità completo.</span><span class="sxs-lookup"><span data-stu-id="d4b36-152">Retrieves the location in the full entity body where the partial entity body should be inserted and the total size of the full entity body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**\_codifica del \_ trasferimento del contenuto delle query WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-154">Recupera una trasformazione di codifica applicabile a un corpo di entità.</span><span class="sxs-lookup"><span data-stu-id="d4b36-154">Retrieves an encoding transformation applicable to an entity-body.</span></span> <span data-ttu-id="d4b36-155">Potrebbe essere già stato applicato, potrebbe essere necessario applicarlo o eventualmente applicabile.</span><span class="sxs-lookup"><span data-stu-id="d4b36-155">It may already have been applied, may need to be applied, or may be optionally applicable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**\_tipo di \_ contenuto della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-157">Riceve il tipo di contenuto della risorsa, ad esempio testo o HTML.</span><span class="sxs-lookup"><span data-stu-id="d4b36-157">Receives the content type of the resource, such as text or html.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_cookie di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-159">Recupera tutti i cookie associati alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-159">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_costo query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-161">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="d4b36-161">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**\_personalizzata della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-163">Fa in modo che [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) cerchi il nome di intestazione specificato nel parametro *pwszName* e archivia le informazioni di intestazione in *lpBuffer*.</span><span class="sxs-lookup"><span data-stu-id="d4b36-163">Causes [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) to search for the header name specified in the *pwszName* parameter and store the header information in *lpBuffer*.</span></span> <span data-ttu-id="d4b36-164">Un'applicazione può utilizzare **il \_ \_ timeout di \_ risposta \_ di ricezione dell'opzione WinHTTP** per limitare il tempo massimo di attesa della query per la ricezione di tutte le intestazioni.</span><span class="sxs-lookup"><span data-stu-id="d4b36-164">An application can use **WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT** to limit the maximum time this query waits for all headers to be received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**\_data query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-166">Riceve la data e l'ora in cui è stato originato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="d4b36-166">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_query WinHTTP \_ derivata \_ da**</span><span class="sxs-lookup"><span data-stu-id="d4b36-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**WINHTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-168">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="d4b36-168">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ETag query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-170">Recupera il tag di entità per l'entità associata.</span><span class="sxs-lookup"><span data-stu-id="d4b36-170">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**\_ \_ si prevede che la query WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-172">Recupera l'intestazione Expect, che indica se l'applicazione client deve prevedere le risposte della serie 100.</span><span class="sxs-lookup"><span data-stu-id="d4b36-172">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**\_scadenza della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-174">Riceve la data e l'ora in cui la risorsa deve essere considerata obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-174">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_query WinHTTP \_ avanzata**</span><span class="sxs-lookup"><span data-stu-id="d4b36-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**WINHTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-176">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-176">Obsolete.</span></span> <span data-ttu-id="d4b36-177">Gestito per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="d4b36-177">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**\_query WinHTTP \_ da**</span><span class="sxs-lookup"><span data-stu-id="d4b36-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-179">Recupera l'indirizzo di posta elettronica dell'utente che controlla l' [*agente utente*](glossary.md) richiedente se l'intestazione From viene assegnata.</span><span class="sxs-lookup"><span data-stu-id="d4b36-179">Retrieves the e-mail address for the user who controls the requesting [*user agent*](glossary.md) if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_host query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-181">Recupera l'host Internet e il numero di porta della risorsa richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-181">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**\_query WinHTTP \_ se \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="d4b36-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-183">Recupera il contenuto del If-Match campo di intestazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-183">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_query WinHTTP \_ se \_ modificata \_ dopo**</span><span class="sxs-lookup"><span data-stu-id="d4b36-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WINHTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-185">Recupera il contenuto dell'intestazione If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="d4b36-185">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_query WinHTTP \_ se \_ Nessuna \_ corrispondenza**</span><span class="sxs-lookup"><span data-stu-id="d4b36-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WINHTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-187">Recupera il contenuto del campo dell'intestazione della richiesta If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="d4b36-187">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**\_query WinHTTP \_ se \_ intervallo**</span><span class="sxs-lookup"><span data-stu-id="d4b36-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-189">Recupera il contenuto del If-Range campo di intestazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-189">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="d4b36-190">Questa intestazione consente all'applicazione client di verificare se l'entità correlata a una copia parziale dell'entità nella cache dell'applicazione client non è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="d4b36-190">This header allows the client application to check if the entity related to a partial copy of the entity in the client application's cache has not been updated.</span></span> <span data-ttu-id="d4b36-191">Se l'entità non è stata aggiornata, inviare le parti mancanti nell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="d4b36-191">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="d4b36-192">Se l'entità è stata aggiornata, inviare l'intera entità aggiornata.</span><span class="sxs-lookup"><span data-stu-id="d4b36-192">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**\_query WinHTTP \_ se non \_ modificata \_ dopo**</span><span class="sxs-lookup"><span data-stu-id="d4b36-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-194">Recupera il contenuto del campo di intestazione della richiesta If-Unmodified-Since.</span><span class="sxs-lookup"><span data-stu-id="d4b36-194">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_collegamento alla query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-196">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-196">Obsolete.</span></span> <span data-ttu-id="d4b36-197">Gestito per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="d4b36-197">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ Ultima modifica della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**WINHTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-199">Riceve la data e l'ora dell'Ultima modifica della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d4b36-199">Receives the date and time at which the resource was last modified.</span></span> <span data-ttu-id="d4b36-200">La data e l'ora sono determinate dal server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-200">The date and time are determined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**\_percorso della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-202">Recupera l'URI assoluto utilizzato in un'intestazione di risposta della posizione.</span><span class="sxs-lookup"><span data-stu-id="d4b36-202">Retrieves the absolute URI used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**\_Max query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-204">Indica il valore massimo di un \_ valore di query WinHTTP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="d4b36-204">Indicates the maximum value of a WINHTTP\_QUERY\_\* value.</span></span> <span data-ttu-id="d4b36-205">Non è un flag di query.</span><span class="sxs-lookup"><span data-stu-id="d4b36-205">Not a query flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**\_ \_ numero massimo di \_ inoltri della query WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-207">Recupera il numero di proxy o gateway che è in grado di inoltrare la richiesta al server in ingresso successivo.</span><span class="sxs-lookup"><span data-stu-id="d4b36-207">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ \_ ID messaggio di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-209">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="d4b36-209">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_ \_ versione MIME della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-211">Riceve la versione del protocollo MIME (Multipurpose Internet Mail Extensions) utilizzato per costruire il messaggio.</span><span class="sxs-lookup"><span data-stu-id="d4b36-211">Receives the version of the Multipurpose Internet Mail Extensions (MIME) protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_ \_ URI orig query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-213">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-213">Obsolete.</span></span> <span data-ttu-id="d4b36-214">Gestito per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="d4b36-214">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_pragma query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-216">Riceve le direttive specifiche dell'implementazione che potrebbero essere applicabili a qualsiasi destinatario lungo la catena di richiesta/risposta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-216">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_ \_ autenticazione proxy query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-218">Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal proxy.</span><span class="sxs-lookup"><span data-stu-id="d4b36-218">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_ \_ autorizzazione proxy query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-220">Recupera l'intestazione utilizzata per identificare l'utente a un proxy che richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d4b36-220">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="d4b36-221">Questa intestazione può essere recuperata solo prima dell'invio della richiesta al server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-221">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_ \_ connessione proxy di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-223">Recupera l'intestazione del Proxy-Connection.</span><span class="sxs-lookup"><span data-stu-id="d4b36-223">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_supporto del \_ proxy di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP\_QUERY\_PROXY\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-225">Recupera l'intestazione del Proxy-Support.</span><span class="sxs-lookup"><span data-stu-id="d4b36-225">Retrieves the Proxy-Support header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**\_query WinHTTP \_ pubblica**</span><span class="sxs-lookup"><span data-stu-id="d4b36-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-227">Riceve i verbi HTTP disponibili in questo server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-227">Receives HTTP verbs available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_intervallo di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-229">Recupera l'intervallo di byte di un'entità.</span><span class="sxs-lookup"><span data-stu-id="d4b36-229">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ intestazioni RAW della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-231">Riceve tutte le intestazioni restituite dal server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-231">Receives all the headers returned by the server.</span></span> <span data-ttu-id="d4b36-232">Ogni intestazione viene terminata con " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="d4b36-232">Each header is terminated by "\\0".</span></span> <span data-ttu-id="d4b36-233">Un " \\ 0" aggiuntivo termina l'elenco di intestazioni.</span><span class="sxs-lookup"><span data-stu-id="d4b36-233">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**\_intestazioni RAW di query WinHTTP \_ \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="d4b36-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-235">Riceve tutte le intestazioni restituite dal server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-235">Receives all the headers returned by the server.</span></span> <span data-ttu-id="d4b36-236">Ogni intestazione è separata da una sequenza di ritorno a capo/avanzamento riga (CR/LF).</span><span class="sxs-lookup"><span data-stu-id="d4b36-236">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_Referer della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-238">Riceve l'URI della risorsa in cui è stato ottenuto l'URI richiesto.</span><span class="sxs-lookup"><span data-stu-id="d4b36-238">Receives the URI of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_aggiornamento query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-240">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-240">Obsolete.</span></span> <span data-ttu-id="d4b36-241">Gestito per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="d4b36-241">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_metodo di \_ richiesta di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-243">Riceve il verbo HTTP usato nella richiesta, in genere GET o POST.</span><span class="sxs-lookup"><span data-stu-id="d4b36-243">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**\_tentativo di query WinHTTP \_ \_ dopo**</span><span class="sxs-lookup"><span data-stu-id="d4b36-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-245">Recupera l'intervallo di tempo per cui il servizio non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="d4b36-245">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_server di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-247">Recupera le informazioni sul software utilizzato dal server di origine per gestire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-247">Retrieves information about the software used by the originating server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_ \_ cookie set di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-249">Riceve il valore del set di cookie per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-249">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**\_codice di \_ stato della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-251">Riceve il codice di stato restituito dal server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-251">Receives the status code returned by the server.</span></span> <span data-ttu-id="d4b36-252">Per un elenco di valori possibili, vedere [**codici di stato http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d4b36-252">For a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**\_ \_ testo stato query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-254">Riceve il testo aggiuntivo restituito dal server nella riga di risposta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-254">Receives additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**\_titolo della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-256">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-256">Obsolete.</span></span> <span data-ttu-id="d4b36-257">Gestito per la compatibilità delle applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="d4b36-257">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**\_codifica di \_ trasferimento \_ query WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-259">Recupera il tipo di trasformazione applicato al corpo del messaggio in modo che possa essere trasferito in modo sicuro tra il mittente e il destinatario.</span><span class="sxs-lookup"><span data-stu-id="d4b36-259">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_query WinHTTP \_ a meno che non venga \_ modificata \_ da**</span><span class="sxs-lookup"><span data-stu-id="d4b36-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WINHTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-261">Recupera l'intestazione a meno che non venga modificata.</span><span class="sxs-lookup"><span data-stu-id="d4b36-261">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_aggiornamento di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-263">Recupera i protocolli di comunicazione aggiuntivi supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-263">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_URI di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-265">Riceve parte o tutto l'URI mediante il quale è possibile identificare la risorsa Request-URI.</span><span class="sxs-lookup"><span data-stu-id="d4b36-265">Receives some or all of the URI by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_ \_ agente utente query \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="d4b36-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-267">Recupera le informazioni sull'agente utente che ha effettuato la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-267">Retrieves information about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**\_query WinHTTP \_ Vary**</span><span class="sxs-lookup"><span data-stu-id="d4b36-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-269">Recupera l'intestazione che indica che l'entità è stata selezionata da un numero di rappresentazioni disponibili della risposta mediante la negoziazione basata su server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-269">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**\_versione della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-271">Recupera la versione HTTP presente nella riga di stato.</span><span class="sxs-lookup"><span data-stu-id="d4b36-271">Retrieves the HTTP version that is present in the status line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_query WinHTTP \_ tramite**</span><span class="sxs-lookup"><span data-stu-id="d4b36-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-273">Recupera i protocolli intermedi e i destinatari tra l'agente utente e il server nelle richieste e tra il server di origine e il client sulle risposte.</span><span class="sxs-lookup"><span data-stu-id="d4b36-273">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_avviso di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-275">Recupera informazioni aggiuntive sullo stato di una risposta che potrebbero non essere riflesse dal codice di stato della risposta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-275">Retrieves additional information about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**\_autenticazione del \_ sito Web di query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-277">Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal server.</span><span class="sxs-lookup"><span data-stu-id="d4b36-277">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="d4b36-278">I flag di modifica vengono utilizzati in combinazione con un flag di attributo per modificare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4b36-278">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="d4b36-279">I flag di modifica possono modificare il formato dei dati restituiti o indicare il punto in cui la funzione [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) deve cercare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="d4b36-279">Modifier flags either modify the format of the data returned or indicate where the [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function should search for the information.</span></span>

<dl> <dt>

<span data-ttu-id="d4b36-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**\_numero di \_ flag della query WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-281">Restituisce i dati come numero a 32 bit per le intestazioni il cui valore è un numero, ad esempio il codice di stato.</span><span class="sxs-lookup"><span data-stu-id="d4b36-281">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_intestazioni di \_ richiesta del flag di query WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-283">Solo intestazioni della richiesta di query.</span><span class="sxs-lookup"><span data-stu-id="d4b36-283">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4b36-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**\_flag di query WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4b36-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d4b36-285">Restituisce il valore dell'intestazione come struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , che non richiede l'analisi dei dati da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d4b36-285">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="d4b36-286">Utilizzare per le intestazioni il cui valore è una stringa di data/ora, ad esempio "Last-Modified-Time".</span><span class="sxs-lookup"><span data-stu-id="d4b36-286">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4b36-287">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4b36-287">Requirements</span></span>



| <span data-ttu-id="d4b36-288">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4b36-288">Requirement</span></span> | <span data-ttu-id="d4b36-289">Valore</span><span class="sxs-lookup"><span data-stu-id="d4b36-289">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b36-290">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4b36-290">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b36-291">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="d4b36-291">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="d4b36-292">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4b36-292">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b36-293">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="d4b36-293">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="d4b36-294">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4b36-294">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4b36-295"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4b36-295"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b36-296">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4b36-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b36-297">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d4b36-297">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

