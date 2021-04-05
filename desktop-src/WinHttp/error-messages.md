---
description: I valori di errore identificati in questo argomento vengono restituiti da GetLastError quando una delle funzioni di servizi HTTP di Microsoft Windows (WinHTTP) ha esito negativo.
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Messaggi di errore (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882877"
---
# <a name="error-messages-winhttph"></a><span data-ttu-id="1af3f-103">Messaggi di errore (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="1af3f-103">Error Messages (Winhttp.h)</span></span>

<span data-ttu-id="1af3f-104">I valori di errore elencati di seguito vengono restituiti da [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando una delle funzioni di servizi HTTP di Microsoft Windows (WinHTTP) ha esito negativo e vengono restituite anche nei 16 bit inferiori di [**HRESULT**](../com/structure-of-com-error-codes.md) restituiti dall'oggetto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="1af3f-104">The error values listed below are returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) when one of the Microsoft Windows HTTP Services (WinHTTP) functions fails, and are also returned in the lower 16 bits of [**HRESULT**](../com/structure-of-com-error-codes.md) error returns from the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

<span data-ttu-id="1af3f-105">I valori di errore i cui nomi iniziano con "ERROR \_ WinHTTP \_ " sono specifici delle funzioni WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1af3f-105">Error values whose names begin with "ERROR\_WINHTTP\_" are specific to the WinHTTP functions.</span></span> <span data-ttu-id="1af3f-106">Le funzioni WinHTTP restituiscono anche messaggi di errore di Windows laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-106">The WinHTTP functions also return Windows error messages where appropriate.</span></span>

<dl> <dt>

<span data-ttu-id="1af3f-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**errore \_ del \_ \_ servizio proxy \_ automatico \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="1af3f-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERROR\_WINHTTP\_AUTO\_PROXY\_SERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-108">12178</span><span class="sxs-lookup"><span data-stu-id="1af3f-108">12178</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-109">Restituito da [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) quando non è possibile trovare un proxy per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-109">Returned by [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) when a proxy for the specified URL cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERRORE \_ di \_ rilevamento automatico WinHTTP \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="1af3f-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR\_WINHTTP\_AUTODETECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-111">12180</span><span class="sxs-lookup"><span data-stu-id="1af3f-111">12180</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-112">Restituito da [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) se WinHTTP non è stato in grado di individuare l'URL del file di configurazione automatica del proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="1af3f-112">Returned by [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) if WinHTTP was unable to discover the URL of the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERRORE \_ WinHTTP \_ \_ \_ script proxy auto \_ errato**</span><span class="sxs-lookup"><span data-stu-id="1af3f-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR\_WINHTTP\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-114">12166</span><span class="sxs-lookup"><span data-stu-id="1af3f-114">12166</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-115">Si è verificato un errore durante l'esecuzione del codice di script nel file di configurazione automatica del proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="1af3f-115">An error occurred executing the script code in the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ chiamare \_ dopo l' \_ apertura**</span><span class="sxs-lookup"><span data-stu-id="1af3f-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-117">12103</span><span class="sxs-lookup"><span data-stu-id="1af3f-117">12103</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-118">Restituito dall'oggetto [**HttpRequest**](winhttprequest.md) se non è possibile richiedere un'opzione specificata dopo che è stato chiamato il metodo [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="1af3f-118">Returned by the [**HttpRequest**](winhttprequest.md) object if a specified option cannot be requested after the [**Open**](iwinhttprequest-open.md) method has been called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ chiamare \_ dopo l' \_ INVIO**</span><span class="sxs-lookup"><span data-stu-id="1af3f-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-120">12102</span><span class="sxs-lookup"><span data-stu-id="1af3f-120">12102</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-121">Restituito dall'oggetto [**HttpRequest**](winhttprequest.md) se non è possibile eseguire un'operazione richiesta dopo la chiamata al metodo [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="1af3f-121">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed after calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ chiamare \_ prima dell' \_ apertura**</span><span class="sxs-lookup"><span data-stu-id="1af3f-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-123">12100</span><span class="sxs-lookup"><span data-stu-id="1af3f-123">12100</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-124">Restituito dall'oggetto [**HttpRequest**](winhttprequest.md) se non è possibile eseguire un'operazione richiesta prima di chiamare il metodo [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="1af3f-124">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Open**](iwinhttprequest-open.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ chiamare \_ prima dell' \_ INVIO**</span><span class="sxs-lookup"><span data-stu-id="1af3f-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-126">12101</span><span class="sxs-lookup"><span data-stu-id="1af3f-126">12101</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-127">Restituito dall'oggetto [**HttpRequest**](winhttprequest.md) se non è possibile eseguire un'operazione richiesta prima di chiamare il metodo [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="1af3f-127">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERRORE \_ WinHTTP \_ non è in grado di \_ connettersi**</span><span class="sxs-lookup"><span data-stu-id="1af3f-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR\_WINHTTP\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-129">12029</span><span class="sxs-lookup"><span data-stu-id="1af3f-129">12029</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-130">Restituito se la connessione al server non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="1af3f-130">Returned if connection to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRORE \_ \_ \_ certificato autenticazione client \_ WinHTTP \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="1af3f-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1af3f-132">Il server richiede l'autenticazione client SSL.</span><span class="sxs-lookup"><span data-stu-id="1af3f-132">The server requires SSL client Authentication.</span></span> <span data-ttu-id="1af3f-133">L'applicazione recupera l'elenco di autorità di certificazione chiamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con l'opzione **WinHTTP \_ opzione \_ client \_ CERT \_ Issuer \_ List** .</span><span class="sxs-lookup"><span data-stu-id="1af3f-133">The application retrieves the list of certificate issuers by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="1af3f-134">Per ulteriori informazioni, vedere l'opzione **WinHTTP opzione \_ \_ client \_ CERT \_ Issuer \_ List** .</span><span class="sxs-lookup"><span data-stu-id="1af3f-134">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

<span data-ttu-id="1af3f-135">Se il server richiede il certificato client, ma non lo richiede, l'applicazione può chiamare alternativamente [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l'opzione del contesto del certificato **client dell' \_ opzione \_ \_ \_ WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="1af3f-135">If the server requests the client certificate, but does not require it, the application can alternately call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="1af3f-136">In questo caso, l'applicazione specifica la \_ macro del \_ contesto del certificato client WinHTTP nessuna \_ \_ nel parametro *lpBuffer* di **WinHttpSetOption**.</span><span class="sxs-lookup"><span data-stu-id="1af3f-136">In this case, the application specifies the WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT macro in the *lpBuffer* parameter of **WinHttpSetOption**.</span></span> <span data-ttu-id="1af3f-137">Per ulteriori informazioni, vedere l'opzione di **\_ \_ \_ \_ contesto certificato client opzione WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="1af3f-137">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>

<span data-ttu-id="1af3f-138">**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-138">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERRORE \_ del \_ certificato client WinHTTP \_ \_ senza \_ accesso \_ \_ chiave privata**</span><span class="sxs-lookup"><span data-stu-id="1af3f-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_ACCESS\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1af3f-140">L'applicazione non dispone dei privilegi necessari per accedere alla chiave privata associata al certificato client.</span><span class="sxs-lookup"><span data-stu-id="1af3f-140">The application does not have the required privileges to access the private key associated with the client certificate.</span></span>

<span data-ttu-id="1af3f-141">**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-141">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERRORE \_ del \_ certificato client WinHTTP \_ \_ senza \_ \_ chiave privata**</span><span class="sxs-lookup"><span data-stu-id="1af3f-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1af3f-143">Al contesto del certificato client SSL non è associata alcuna chiave privata.</span><span class="sxs-lookup"><span data-stu-id="1af3f-143">The context for the SSL client certificate does not have a private key associated with it.</span></span> <span data-ttu-id="1af3f-144">Il certificato client potrebbe essere stato importato nel computer senza la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="1af3f-144">The client certificate may have been imported to the computer without the private key.</span></span>

<span data-ttu-id="1af3f-145">**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-145">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERRORE \_ di \_ dimensioni dell' \_ intestazione di codifica in blocchi WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR\_WINHTTP\_CHUNKED\_ENCODING\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-147">12183</span><span class="sxs-lookup"><span data-stu-id="1af3f-147">12183</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-148">Restituito da [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando viene rilevata una condizione di overflow nel corso dell'analisi della codifica Chunked.</span><span class="sxs-lookup"><span data-stu-id="1af3f-148">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when an overflow condition is encountered in the course of parsing chunked encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRORE \_ \_ \_ certificato autenticazione client \_ WinHTTP \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="1af3f-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-150">12044</span><span class="sxs-lookup"><span data-stu-id="1af3f-150">12044</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-151">Restituito da [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando il server richiede l'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="1af3f-151">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the server requests client authentication.</span></span>

<span data-ttu-id="1af3f-152">**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-152">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**errore \_ di \_ connessione WinHTTP errore \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERROR\_WINHTTP\_CONNECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-154">12030</span><span class="sxs-lookup"><span data-stu-id="1af3f-154">12030</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-155">La connessione al server è stata reimpostata o terminata oppure è stato rilevato un protocollo SSL incompatibile.</span><span class="sxs-lookup"><span data-stu-id="1af3f-155">The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered.</span></span> <span data-ttu-id="1af3f-156">Ad esempio, WinHTTP versione 5,1 non supporta SSL2, a meno che il client non lo consenta in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="1af3f-156">For example, WinHTTP version 5.1 does not support SSL2 unless the client specifically enables it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**l' \_ intestazione WinHTTP dell'errore \_ \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="1af3f-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**ERROR\_WINHTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-158">12155</span><span class="sxs-lookup"><span data-stu-id="1af3f-158">12155</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-159">Obsoleto non più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-159">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERRORE \_ \_ numero intestazioni \_ WinHTTP \_ superate**</span><span class="sxs-lookup"><span data-stu-id="1af3f-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERROR\_WINHTTP\_HEADER\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-161">12181</span><span class="sxs-lookup"><span data-stu-id="1af3f-161">12181</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-162">Restituito da [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando un numero maggiore di intestazioni era presente in una risposta che WinHTTP poteva ricevere.</span><span class="sxs-lookup"><span data-stu-id="1af3f-162">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when a larger number of headers were present in a response than WinHTTP could receive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERRORE \_ di \_ intestazione WinHTTP \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="1af3f-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERROR\_WINHTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-164">12150</span><span class="sxs-lookup"><span data-stu-id="1af3f-164">12150</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-165">Impossibile trovare l'intestazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="1af3f-165">The requested header cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**\_ \_ \_ overflow dimensioni intestazione WinHTTP \_ errore**</span><span class="sxs-lookup"><span data-stu-id="1af3f-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR\_WINHTTP\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-167">12182</span><span class="sxs-lookup"><span data-stu-id="1af3f-167">12182</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-168">Restituito da [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando le dimensioni delle intestazioni ricevute superano il limite per l'handle della richiesta.</span><span class="sxs-lookup"><span data-stu-id="1af3f-168">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the size of headers received exceeds the limit for the request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERRORE \_ WinHTTP \_ \_ stato di handle errato \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-170">12019</span><span class="sxs-lookup"><span data-stu-id="1af3f-170">12019</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-171">Non è possibile eseguire l'operazione richiesta perché l'handle specificato non è nello stato corretto.</span><span class="sxs-lookup"><span data-stu-id="1af3f-171">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERRORE \_ WinHTTP \_ \_ tipo di handle errato \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-173">12018</span><span class="sxs-lookup"><span data-stu-id="1af3f-173">12018</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-174">Il tipo di handle fornito non è corretto per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1af3f-174">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**errore \_ interno WinHTTP errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERROR\_WINHTTP\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-176">12004</span><span class="sxs-lookup"><span data-stu-id="1af3f-176">12004</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-177">Si è verificato un errore interno.</span><span class="sxs-lookup"><span data-stu-id="1af3f-177">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERRORE \_ WinHTTP \_ opzione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR\_WINHTTP\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-179">12009</span><span class="sxs-lookup"><span data-stu-id="1af3f-179">12009</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-180">Una richiesta a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) ha specificato un valore di opzione non valido.</span><span class="sxs-lookup"><span data-stu-id="1af3f-180">A request to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) or [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERRORE \_ WinHTTP \_ \_ richiesta di query non valida \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR\_WINHTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-182">12154</span><span class="sxs-lookup"><span data-stu-id="1af3f-182">12154</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-183">Obsoleto non più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-183">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERRORE \_ WinHTTP \_ \_ risposta server non valida \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR\_WINHTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-185">12152</span><span class="sxs-lookup"><span data-stu-id="1af3f-185">12152</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-186">Impossibile analizzare la risposta del server.</span><span class="sxs-lookup"><span data-stu-id="1af3f-186">The server response cannot be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERRORE \_ WinHTTP \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR\_WINHTTP\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-188">12005</span><span class="sxs-lookup"><span data-stu-id="1af3f-188">12005</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-189">URL non valido.</span><span class="sxs-lookup"><span data-stu-id="1af3f-189">The URL is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**errore \_ di \_ accesso WinHTTP errore \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR\_WINHTTP\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-191">12015</span><span class="sxs-lookup"><span data-stu-id="1af3f-191">12015</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-192">Tentativo di accesso non riuscito.</span><span class="sxs-lookup"><span data-stu-id="1af3f-192">The login attempt failed.</span></span> <span data-ttu-id="1af3f-193">Quando si verifica questo errore, l'handle della richiesta deve essere chiuso con [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span><span class="sxs-lookup"><span data-stu-id="1af3f-193">When this error is encountered, the request handle should be closed with [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span></span> <span data-ttu-id="1af3f-194">Prima di ritentare la funzione che ha generato questo errore, è necessario creare un nuovo handle di richiesta.</span><span class="sxs-lookup"><span data-stu-id="1af3f-194">A new request handle must be created before retrying the function that originally produced this error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERRORE \_ \_ nome WinHTTP \_ non \_ risolto**</span><span class="sxs-lookup"><span data-stu-id="1af3f-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR\_WINHTTP\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-196">12007</span><span class="sxs-lookup"><span data-stu-id="1af3f-196">12007</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-197">Il nome del server non può essere risolto.</span><span class="sxs-lookup"><span data-stu-id="1af3f-197">The server name cannot be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERRORE \_ WinHTTP \_ non \_ inizializzato**</span><span class="sxs-lookup"><span data-stu-id="1af3f-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR\_WINHTTP\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-199">12172</span><span class="sxs-lookup"><span data-stu-id="1af3f-199">12172</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-200">Obsoleto non più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-200">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERRORE \_ WinHTTP \_ operazione \_ annullata**</span><span class="sxs-lookup"><span data-stu-id="1af3f-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR\_WINHTTP\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-202">12017</span><span class="sxs-lookup"><span data-stu-id="1af3f-202">12017</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-203">L'operazione è stata annullata, in genere perché l'handle su cui era in funzione la richiesta è stato chiuso prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1af3f-203">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**\_opzione WinHTTP di errore \_ \_ non \_ impostabile**</span><span class="sxs-lookup"><span data-stu-id="1af3f-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR\_WINHTTP\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-205">12011</span><span class="sxs-lookup"><span data-stu-id="1af3f-205">12011</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-206">Impossibile impostare l'opzione richiesta, solo query.</span><span class="sxs-lookup"><span data-stu-id="1af3f-206">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERRORE \_ WinHTTP \_ \_ di \_ handle**</span><span class="sxs-lookup"><span data-stu-id="1af3f-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR\_WINHTTP\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-208">12001</span><span class="sxs-lookup"><span data-stu-id="1af3f-208">12001</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-209">Obsoleto non più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-209">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERRORE \_ di \_ Reindirizzamento WinHTTP \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="1af3f-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR\_WINHTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-211">12156</span><span class="sxs-lookup"><span data-stu-id="1af3f-211">12156</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-212">Il reindirizzamento non è riuscito perché lo schema è stato modificato o tutti i tentativi di reindirizzamento non sono riusciti (il valore predefinito è cinque tentativi).</span><span class="sxs-lookup"><span data-stu-id="1af3f-212">The redirection failed because either the scheme changed or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERRORE WinHTTP-invia di nuovo la \_ \_ \_ richiesta**</span><span class="sxs-lookup"><span data-stu-id="1af3f-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR\_WINHTTP\_RESEND\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-214">12032</span><span class="sxs-lookup"><span data-stu-id="1af3f-214">12032</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-215">Funzione WinHTTP non riuscita.</span><span class="sxs-lookup"><span data-stu-id="1af3f-215">The WinHTTP function failed.</span></span> <span data-ttu-id="1af3f-216">È possibile ritentare la funzione desiderata nello stesso handle di richiesta.</span><span class="sxs-lookup"><span data-stu-id="1af3f-216">The desired function can be retried on the same request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**\_ \_ \_ overflow svuotamento risposta WinHTTP \_ errore**</span><span class="sxs-lookup"><span data-stu-id="1af3f-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR\_WINHTTP\_RESPONSE\_DRAIN\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-218">12184</span><span class="sxs-lookup"><span data-stu-id="1af3f-218">12184</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-219">Restituito quando una risposta in ingresso supera un limite di dimensioni WinHTTP interno.</span><span class="sxs-lookup"><span data-stu-id="1af3f-219">Returned when an incoming response exceeds an internal WinHTTP size limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**errore \_ di \_ esecuzione dello script WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERROR\_WINHTTP\_SCRIPT\_EXECUTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-221">12177</span><span class="sxs-lookup"><span data-stu-id="1af3f-221">12177</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-222">Si è verificato un errore durante l'esecuzione di uno script.</span><span class="sxs-lookup"><span data-stu-id="1af3f-222">An error was encountered while executing a script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERRORE \_ WinHTTP \_ Secure \_ Certificate \_ NC \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="1af3f-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-224">12038</span><span class="sxs-lookup"><span data-stu-id="1af3f-224">12038</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-225">Restituito quando il nome CN di un certificato non corrisponde al valore passato (equivalente a un errore di **\_ \_ \_ non \_ corrispondenza di CERT E CN** ).</span><span class="sxs-lookup"><span data-stu-id="1af3f-225">Returned when a certificate CN name does not match the passed value (equivalent to a **CERT\_E\_CN\_NO\_MATCH** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERRORE \_ WinHTTP \_ \_ certificato sicuro \_ data \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="1af3f-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-227">12037</span><span class="sxs-lookup"><span data-stu-id="1af3f-227">12037</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-228">Indica che un certificato richiesto non rientra nel periodo di validità durante la verifica in base al clock di sistema corrente o al timestamp nel file firmato oppure che i periodi di validità della catena di certificazione non vengono annidati correttamente (equivalente a un certificato **\_ e \_ scaduto** o a un errore **\_ \_ VALIDITYPERIODNESTING del certificato** ).</span><span class="sxs-lookup"><span data-stu-id="1af3f-228">Indicates that a required certificate is not within its validity period when verifying against the current system clock or the timestamp in the signed file, or that the validity periods of the certification chain do not nest correctly (equivalent to a **CERT\_E\_EXPIRED** or a **CERT\_E\_VALIDITYPERIODNESTING** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERRORE \_ WinHTTP \_ Secure \_ CERT \_ rev \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="1af3f-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-230">12057</span><span class="sxs-lookup"><span data-stu-id="1af3f-230">12057</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-231">Indica che non è possibile controllare la revoca perché il server di revoca è offline (equivalente **alla \_ revoca E alla \_ revoca \_ offline**).</span><span class="sxs-lookup"><span data-stu-id="1af3f-231">Indicates that revocation cannot be checked because the revocation server was offline (equivalent to **CRYPT\_E\_REVOCATION\_OFFLINE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERRORE \_ WinHTTP \_ Secure \_ CERT \_ revocato**</span><span class="sxs-lookup"><span data-stu-id="1af3f-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-233">12170</span><span class="sxs-lookup"><span data-stu-id="1af3f-233">12170</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-234">Indica che un certificato è stato revocato (equivalente alla **crittografia \_ E \_ revocata**).</span><span class="sxs-lookup"><span data-stu-id="1af3f-234">Indicates that a certificate has been revoked (equivalent to **CRYPT\_E\_REVOKED**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**errore durante l'utilizzo del \_ \_ \_ certificato sicuro WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_WRONG\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-236">12179</span><span class="sxs-lookup"><span data-stu-id="1af3f-236">12179</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-237">Indica che un certificato non è valido per l'utilizzo richiesto (equivalente a **certificato \_ E \_ \_ utilizzo errato**).</span><span class="sxs-lookup"><span data-stu-id="1af3f-237">Indicates that a certificate is not valid for the requested usage (equivalent to **CERT\_E\_WRONG\_USAGE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**errore \_ del \_ canale sicuro WinHTTP \_ di errore \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERROR\_WINHTTP\_SECURE\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-239">12157</span><span class="sxs-lookup"><span data-stu-id="1af3f-239">12157</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-240">Indica che si è verificato un errore durante l'esecuzione di un canale sicuro (equivalente ai codici di errore che iniziano con "SEC e \_ \_ " e "sec \_ i \_ " elencati nel file di intestazione "Winerror. h").</span><span class="sxs-lookup"><span data-stu-id="1af3f-240">Indicates that an error occurred having to do with a secure channel (equivalent to error codes that begin with "SEC\_E\_" and "SEC\_I\_" listed in the "winerror.h" header file).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**errore errore \_ WinHTTP \_ sicuro \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR\_WINHTTP\_SECURE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-242">12175</span><span class="sxs-lookup"><span data-stu-id="1af3f-242">12175</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-243">Il certificato Secure Sockets Layer (SSL) inviato dal server sono stati rilevati uno o più errori.</span><span class="sxs-lookup"><span data-stu-id="1af3f-243">One or more errors were found in the Secure Sockets Layer (SSL) certificate sent by the server.</span></span> <span data-ttu-id="1af3f-244">Per determinare il tipo di errore rilevato, verificare la presenza di una notifica di [**\_ \_ \_ \_ errore di stato di callback WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) in una funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-244">To determine what type of error was encountered, check for a [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification in a status callback function.</span></span> <span data-ttu-id="1af3f-245">Per ulteriori informazioni, vedere [**\_ \_ callback di stato WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span><span class="sxs-lookup"><span data-stu-id="1af3f-245">For more information, see [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERRORE \_ WinHTTP \_ Secure \_ CA non valida \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-247">12045</span><span class="sxs-lookup"><span data-stu-id="1af3f-247">12045</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-248">Indica che una catena di certificati è stata elaborata, ma terminata in un certificato radice non attendibile dal provider di attendibilità (equivalente a **CERT \_ E \_ UNTRUSTEDROOT**).</span><span class="sxs-lookup"><span data-stu-id="1af3f-248">Indicates that a certificate chain was processed, but terminated in a root certificate that is not trusted by the trust provider (equivalent to **CERT\_E\_UNTRUSTEDROOT**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERRORE \_ WinHTTP \_ Secure \_ certificato non valido \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-250">12169</span><span class="sxs-lookup"><span data-stu-id="1af3f-250">12169</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-251">Indica che un certificato non è valido (equivalente a errori quali **CERT \_ e \_ Role**, **CERT \_ e \_ PATHLENCONST**, **CERT \_ e \_ Critical**, **certificate e \_ \_ purpose**, **CERT \_ e \_ ISSUERCHAINING**, CERT e non **\_ \_ valido** e il **\_ \_ concatenamento di CERT** e).</span><span class="sxs-lookup"><span data-stu-id="1af3f-251">Indicates that a certificate is invalid (equivalent to errors such as **CERT\_E\_ROLE**, **CERT\_E\_PATHLENCONST**, **CERT\_E\_CRITICAL**, **CERT\_E\_PURPOSE**, **CERT\_E\_ISSUERCHAINING**, **CERT\_E\_MALFORMED** and **CERT\_E\_CHAINING**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERRORE \_ di \_ arresto WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="1af3f-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR\_WINHTTP\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-253">12012</span><span class="sxs-lookup"><span data-stu-id="1af3f-253">12012</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-254">Il supporto della funzione WinHTTP viene arrestato o scaricato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-254">The WinHTTP function support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**\_Timeout WinHTTP \_ errore**</span><span class="sxs-lookup"><span data-stu-id="1af3f-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR\_WINHTTP\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-256">12002</span><span class="sxs-lookup"><span data-stu-id="1af3f-256">12002</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-257">Timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="1af3f-257">The request has timed out.</span></span>

<span data-ttu-id="1af3f-258">Questo errore può essere restituito come risultato del comportamento del timeout TCP/IP, indipendentemente dai valori di timeout impostati nei servizi HTTP di Windows.</span><span class="sxs-lookup"><span data-stu-id="1af3f-258">This error can be returned as a result of TCP/IP time-out behavior, regardless of time-out values set in Windows HTTP Services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ \_ scaricare \_ lo script**</span><span class="sxs-lookup"><span data-stu-id="1af3f-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR\_WINHTTP\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-260">12167</span><span class="sxs-lookup"><span data-stu-id="1af3f-260">12167</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-261">Non è possibile scaricare il file PAC.</span><span class="sxs-lookup"><span data-stu-id="1af3f-261">The PAC file cannot be downloaded.</span></span> <span data-ttu-id="1af3f-262">Ad esempio, il server a cui fa riferimento l'URL PAC potrebbe non essere raggiungibile o il server ha restituito una risposta 404 non trovata.</span><span class="sxs-lookup"><span data-stu-id="1af3f-262">For example, the server referenced by the PAC URL may not have been reachable, or the server returned a 404 NOT FOUND response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERRORE \_ WinHTTP \_ tipo di script non gestito \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR\_WINHTTP\_UNHANDLED\_SCRIPT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-264">12176</span><span class="sxs-lookup"><span data-stu-id="1af3f-264">12176</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-265">Il tipo di script non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1af3f-265">The script type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**\_schema errore WinHTTP non \_ riconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR\_WINHTTP\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1af3f-267">12006</span><span class="sxs-lookup"><span data-stu-id="1af3f-267">12006</span></span>
</dt> <dt>



<span data-ttu-id="1af3f-268">L'URL ha specificato uno schema diverso da "http:" o "https:".</span><span class="sxs-lookup"><span data-stu-id="1af3f-268">The URL specified a scheme other than "http:" or "https:".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRORE \_ di \_ memoria insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1af3f-270">Memoria insufficiente per completare l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="1af3f-270">Not enough memory was available to complete the requested operation.</span></span>

<span data-ttu-id="1af3f-271">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="1af3f-271">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRORE \_ buffer insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1af3f-273">La dimensione, in byte, del buffer fornito a una funzione non è sufficiente per contenere i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="1af3f-273">The size, in bytes, of the buffer supplied to a function was insufficient to contain the returned data.</span></span> <span data-ttu-id="1af3f-274">Per ulteriori informazioni, vedere la funzione specifica.</span><span class="sxs-lookup"><span data-stu-id="1af3f-274">For more information, see the specific function.</span></span>

<span data-ttu-id="1af3f-275">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="1af3f-275">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERRORE \_ handle non valido \_**</span><span class="sxs-lookup"><span data-stu-id="1af3f-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1af3f-277">L'handle passato al Application Programming Interface (API) è stato invalidato o chiuso.</span><span class="sxs-lookup"><span data-stu-id="1af3f-277">The handle passed to the application programming interface (API) has been either invalidated or closed.</span></span>

<span data-ttu-id="1af3f-278">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="1af3f-278">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRORE \_ nessun \_ altro \_ file**</span><span class="sxs-lookup"><span data-stu-id="1af3f-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1af3f-280">Non sono stati trovati altri file.</span><span class="sxs-lookup"><span data-stu-id="1af3f-280">No more files have been found.</span></span>

<span data-ttu-id="1af3f-281">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="1af3f-281">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRORE \_ nessun \_ altro \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="1af3f-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1af3f-283">Non sono stati trovati altri elementi.</span><span class="sxs-lookup"><span data-stu-id="1af3f-283">No more items have been found.</span></span>

<span data-ttu-id="1af3f-284">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="1af3f-284">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1af3f-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRORE \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="1af3f-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1af3f-286">Lo stack di protocolli richiesto non è caricato e l'applicazione non può avviare WinSock.</span><span class="sxs-lookup"><span data-stu-id="1af3f-286">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>

<span data-ttu-id="1af3f-287">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="1af3f-287">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1af3f-288">Commenti</span><span class="sxs-lookup"><span data-stu-id="1af3f-288">Remarks</span></span>

<span data-ttu-id="1af3f-289">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1af3f-289">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

## <a name="requirements"></a><span data-ttu-id="1af3f-290">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1af3f-290">Requirements</span></span>



| <span data-ttu-id="1af3f-291">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af3f-291">Requirement</span></span> | <span data-ttu-id="1af3f-292">Valore</span><span class="sxs-lookup"><span data-stu-id="1af3f-292">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1af3f-293">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1af3f-293">Minimum supported client</span></span><br/> | <span data-ttu-id="1af3f-294">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="1af3f-294">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="1af3f-295">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1af3f-295">Minimum supported server</span></span><br/> | <span data-ttu-id="1af3f-296">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="1af3f-296">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="1af3f-297">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1af3f-297">Redistributable</span></span><br/>          | <span data-ttu-id="1af3f-298">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1af3f-298">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="1af3f-299">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1af3f-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="1af3f-300"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="1af3f-300"><dt>Winhttp.h</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1af3f-301">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1af3f-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af3f-302">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="1af3f-302">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

