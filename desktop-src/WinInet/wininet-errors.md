---
title: Messaggi di errore (WinInet. h)
description: Le funzioni WinINet restituiscono i codici di errore laddove appropriato. Gli errori seguenti sono specifici delle funzioni WinINet.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121623"
---
# <a name="error-messages-winineth"></a><span data-ttu-id="81c2f-104">Messaggi di errore (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="81c2f-104">Error Messages (Wininet.h)</span></span>

<span data-ttu-id="81c2f-105">Le funzioni WinINet restituiscono i codici di errore laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="81c2f-105">The WinINet functions return error codes where appropriate.</span></span> <span data-ttu-id="81c2f-106">Gli errori seguenti sono specifici delle funzioni WinINet.</span><span class="sxs-lookup"><span data-stu-id="81c2f-106">The following errors are specific to the WinINet functions.</span></span>

<dl> <dt>

<span data-ttu-id="81c2f-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERRORE \_ FTP \_ eliminato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR\_FTP\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-108">12111</span><span class="sxs-lookup"><span data-stu-id="81c2f-108">12111</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-109">Operazione FTP non completata perché la sessione è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="81c2f-109">The FTP operation was not completed because the session was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERRORE \_ FTP \_ Nessuna \_ \_ modalità passiva**</span><span class="sxs-lookup"><span data-stu-id="81c2f-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR\_FTP\_NO\_PASSIVE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-111">12112</span><span class="sxs-lookup"><span data-stu-id="81c2f-111">12112</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-112">La modalità passiva non è disponibile nel server.</span><span class="sxs-lookup"><span data-stu-id="81c2f-112">Passive mode is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERRORE \_ \_ trasferimento FTP \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="81c2f-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR\_FTP\_TRANSFER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-114">12110</span><span class="sxs-lookup"><span data-stu-id="81c2f-114">12110</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-115">Impossibile eseguire l'operazione richiesta sull'handle della sessione FTP perché è già in corso un'operazione.</span><span class="sxs-lookup"><span data-stu-id="81c2f-115">The requested operation cannot be made on the FTP session handle because an operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERRORE \_ Gopher \_ attributo \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERROR\_GOPHER\_ATTRIBUTE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-117">12137</span><span class="sxs-lookup"><span data-stu-id="81c2f-117">12137</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-118">Impossibile trovare l'attributo richiesto.</span><span class="sxs-lookup"><span data-stu-id="81c2f-118">The requested attribute could not be located.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-119">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-119">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**errore \_ dati Gopher errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERROR\_GOPHER\_DATA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-121">12132</span><span class="sxs-lookup"><span data-stu-id="81c2f-121">12132</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-122">È stato rilevato un errore durante la ricezione di dati dal server gopher.</span><span class="sxs-lookup"><span data-stu-id="81c2f-122">An error was detected while receiving data from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-123">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-123">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERRORE \_ \_ di fine \_ dei \_ dati in Gopher**</span><span class="sxs-lookup"><span data-stu-id="81c2f-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR\_GOPHER\_END\_OF\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-125">12133</span><span class="sxs-lookup"><span data-stu-id="81c2f-125">12133</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-126">È stata raggiunta la fine dei dati.</span><span class="sxs-lookup"><span data-stu-id="81c2f-126">The end of the data has been reached.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-127">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-127">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**\_tipo di \_ \_ localizzatore errato Gopher \_ errore**</span><span class="sxs-lookup"><span data-stu-id="81c2f-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR\_GOPHER\_INCORRECT\_LOCATOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-129">12135</span><span class="sxs-lookup"><span data-stu-id="81c2f-129">12135</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-130">Il tipo di localizzatore non è corretto per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="81c2f-130">The type of the locator is not correct for this operation.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-131">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-131">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERRORE \_ Gopher \_ non valido del \_ localizzatore**</span><span class="sxs-lookup"><span data-stu-id="81c2f-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR\_GOPHER\_INVALID\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-133">12134</span><span class="sxs-lookup"><span data-stu-id="81c2f-133">12134</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-134">Il localizzatore specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="81c2f-134">The supplied locator is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-135">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-135">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERRORE \_ Gopher \_ non \_ file**</span><span class="sxs-lookup"><span data-stu-id="81c2f-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR\_GOPHER\_NOT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-137">12131</span><span class="sxs-lookup"><span data-stu-id="81c2f-137">12131</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-138">La richiesta deve essere eseguita per un localizzatore di file.</span><span class="sxs-lookup"><span data-stu-id="81c2f-138">The request must be made for a file locator.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-139">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-139">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERRORE \_ Gopher \_ non \_ Gopher \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="81c2f-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR\_GOPHER\_NOT\_GOPHER\_PLUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-141">12136</span><span class="sxs-lookup"><span data-stu-id="81c2f-141">12136</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-142">L'operazione richiesta può essere eseguita solo su un gopher + server o con un localizzatore che specifica un'operazione di gopher +.</span><span class="sxs-lookup"><span data-stu-id="81c2f-142">The requested operation can be made only against a Gopher+ server, or with a locator that specifies a Gopher+ operation.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-143">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-143">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**errore \_ del \_ protocollo Gopher errore \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERROR\_GOPHER\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-145">12130</span><span class="sxs-lookup"><span data-stu-id="81c2f-145">12130</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-146">È stato rilevato un errore durante l'analisi dei dati restituiti dal server gopher.</span><span class="sxs-lookup"><span data-stu-id="81c2f-146">An error was detected while parsing data returned from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-147">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-147">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERRORE \_ Gopher \_ Unknown \_ Locator**</span><span class="sxs-lookup"><span data-stu-id="81c2f-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERROR\_GOPHER\_UNKNOWN\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-149">12138</span><span class="sxs-lookup"><span data-stu-id="81c2f-149">12138</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-150">Il tipo di localizzatore è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="81c2f-150">The locator type is unknown.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-151">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-151">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERRORE \_ \_ cookie HTTP \_ rifiutato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR\_HTTP\_COOKIE\_DECLINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-153">12162</span><span class="sxs-lookup"><span data-stu-id="81c2f-153">12162</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-154">Il cookie HTTP è stato rifiutato dal server.</span><span class="sxs-lookup"><span data-stu-id="81c2f-154">The HTTP cookie was declined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERRORE \_ del \_ cookie HTTP necessario per la \_ \_ conferma**</span><span class="sxs-lookup"><span data-stu-id="81c2f-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR\_HTTP\_COOKIE\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-156">12161</span><span class="sxs-lookup"><span data-stu-id="81c2f-156">12161</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-157">Il cookie HTTP richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="81c2f-157">The HTTP cookie requires confirmation.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-158">Windows Vista e Windows Server 2008 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-158">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERRORE \_ http \_ server di livello inferiore \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR\_HTTP\_DOWNLEVEL\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-160">12151</span><span class="sxs-lookup"><span data-stu-id="81c2f-160">12151</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-161">Il server non ha restituito intestazioni.</span><span class="sxs-lookup"><span data-stu-id="81c2f-161">The server did not return any headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**l' \_ \_ intestazione HTTP \_ Error \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="81c2f-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**ERROR\_HTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-163">12155</span><span class="sxs-lookup"><span data-stu-id="81c2f-163">12155</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-164">Non è stato possibile aggiungere l'intestazione perché esiste già.</span><span class="sxs-lookup"><span data-stu-id="81c2f-164">The header could not be added because it already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_ \_ \_ Impossibile trovare l'intestazione HTTP dell'errore \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**ERROR\_HTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-166">12150</span><span class="sxs-lookup"><span data-stu-id="81c2f-166">12150</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-167">Non è stato possibile trovare l'intestazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="81c2f-167">The requested header could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERRORE \_ http \_ intestazione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR\_HTTP\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-169">12153</span><span class="sxs-lookup"><span data-stu-id="81c2f-169">12153</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-170">L'intestazione specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="81c2f-170">The supplied header is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERRORE \_ http \_ \_ richiesta di query non valida \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR\_HTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-172">12154</span><span class="sxs-lookup"><span data-stu-id="81c2f-172">12154</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-173">La richiesta effettuata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) non è valida.</span><span class="sxs-lookup"><span data-stu-id="81c2f-173">The request made to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERRORE \_ http \_ \_ risposta server non valida \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR\_HTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-175">12152</span><span class="sxs-lookup"><span data-stu-id="81c2f-175">12152</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-176">Non è stato possibile analizzare la risposta del server.</span><span class="sxs-lookup"><span data-stu-id="81c2f-176">The server response could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERRORE \_ http \_ non \_ reindirizzato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR\_HTTP\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-178">12160</span><span class="sxs-lookup"><span data-stu-id="81c2f-178">12160</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-179">La richiesta HTTP non è stata reindirizzata.</span><span class="sxs-lookup"><span data-stu-id="81c2f-179">The HTTP request was not redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERRORE \_ di \_ Reindirizzamento HTTP \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="81c2f-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR\_HTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-181">12156</span><span class="sxs-lookup"><span data-stu-id="81c2f-181">12156</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-182">Il reindirizzamento non è riuscito perché lo schema è stato modificato (ad esempio, da HTTP a FTP) o tutti i tentativi di reindirizzamento non sono riusciti (il valore predefinito è cinque tentativi).</span><span class="sxs-lookup"><span data-stu-id="81c2f-182">The redirection failed because either the scheme changed (for example, HTTP to FTP) or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERRORE \_ di \_ Reindirizzamento HTTP \_ necessario \_ conferma**</span><span class="sxs-lookup"><span data-stu-id="81c2f-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR\_HTTP\_REDIRECT\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-184">12168</span><span class="sxs-lookup"><span data-stu-id="81c2f-184">12168</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-185">Il reindirizzamento richiede la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="81c2f-185">The redirection requires user confirmation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERRORE \_ \_ thread asincrono \_ Internet \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="81c2f-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR\_INTERNET\_ASYNC\_THREAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-187">12047</span><span class="sxs-lookup"><span data-stu-id="81c2f-187">12047</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-188">L'applicazione non è in grado di avviare un thread asincrono.</span><span class="sxs-lookup"><span data-stu-id="81c2f-188">The application could not start an asynchronous thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERRORE \_ Internet \_ \_ \_ script proxy auto \_ errato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR\_INTERNET\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-190">12166</span><span class="sxs-lookup"><span data-stu-id="81c2f-190">12166</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-191">Si è verificato un errore nello script di configurazione automatica del proxy.</span><span class="sxs-lookup"><span data-stu-id="81c2f-191">There was an error in the automatic proxy configuration script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERRORE \_ di \_ \_ lunghezza dell'opzione Internet errato \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR\_INTERNET\_BAD\_OPTION\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-193">12010</span><span class="sxs-lookup"><span data-stu-id="81c2f-193">12010</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-194">La lunghezza di un'opzione fornita a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) non è corretta per il tipo di opzione specificata.</span><span class="sxs-lookup"><span data-stu-id="81c2f-194">The length of an option supplied to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) is incorrect for the type of option specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERRORE \_ Internet \_ \_ parametro registro di sistema non valido \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERROR\_INTERNET\_BAD\_REGISTRY\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-196">12022</span><span class="sxs-lookup"><span data-stu-id="81c2f-196">12022</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-197">È stato individuato un valore del registro di sistema obbligatorio, ma è un tipo errato o ha un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="81c2f-197">A required registry value was located but is an incorrect type or has an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERRORE \_ Internet \_ non in grado di \_ connettersi**</span><span class="sxs-lookup"><span data-stu-id="81c2f-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR\_INTERNET\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-199">12029</span><span class="sxs-lookup"><span data-stu-id="81c2f-199">12029</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-200">Tentativo di connessione al server non riuscito.</span><span class="sxs-lookup"><span data-stu-id="81c2f-200">The attempt to connect to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERRORE \_ Internet \_ CHG \_ Post \_ \_ non è \_ sicuro**</span><span class="sxs-lookup"><span data-stu-id="81c2f-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR\_INTERNET\_CHG\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-202">12042</span><span class="sxs-lookup"><span data-stu-id="81c2f-202">12042</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-203">L'applicazione sta inviando e tentando di modificare più righe di testo in un server non protetto.</span><span class="sxs-lookup"><span data-stu-id="81c2f-203">The application is posting and attempting to change multiple lines of text on a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERRORE \_ \_ \_ certificato autenticazione client \_ Internet \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="81c2f-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-205">12044</span><span class="sxs-lookup"><span data-stu-id="81c2f-205">12044</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-206">Il server richiede l'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="81c2f-206">The server is requesting client authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERRORE \_ di \_ autenticazione client Internet \_ \_ non \_ impostata**</span><span class="sxs-lookup"><span data-stu-id="81c2f-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_NOT\_SETUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-208">12046</span><span class="sxs-lookup"><span data-stu-id="81c2f-208">12046</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-209">L'autorizzazione client non è configurata nel computer.</span><span class="sxs-lookup"><span data-stu-id="81c2f-209">Client authorization is not set up on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERRORE \_ di \_ connessione Internet \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="81c2f-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR\_INTERNET\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-211">12030</span><span class="sxs-lookup"><span data-stu-id="81c2f-211">12030</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-212">La connessione al server è stata terminata.</span><span class="sxs-lookup"><span data-stu-id="81c2f-212">The connection with the server has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERRORE \_ di \_ reimpostazione della connessione Internet \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR\_INTERNET\_CONNECTION\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-214">12031</span><span class="sxs-lookup"><span data-stu-id="81c2f-214">12031</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-215">La connessione al server è stata reimpostata.</span><span class="sxs-lookup"><span data-stu-id="81c2f-215">The connection with the server has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERRORE \_ di \_ decodifica Internet \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="81c2f-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR\_INTERNET\_DECODING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-217">12175</span><span class="sxs-lookup"><span data-stu-id="81c2f-217">12175</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-218">WinINet non è riuscito a eseguire la decodifica del contenuto nella risposta.</span><span class="sxs-lookup"><span data-stu-id="81c2f-218">WinINet failed to perform content decoding on the response.</span></span> <span data-ttu-id="81c2f-219">Per ulteriori informazioni, vedere l'argomento relativo alla [**codifica del contenuto**](content-encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="81c2f-219">For more information, see the [**Content Encoding**](content-encoding.md) topic.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**\_finestra di dialogo errore Internet \_ \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="81c2f-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**ERROR\_INTERNET\_DIALOG\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-221">12049</span><span class="sxs-lookup"><span data-stu-id="81c2f-221">12049</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-222">Un altro thread ha una finestra di dialogo password in corso.</span><span class="sxs-lookup"><span data-stu-id="81c2f-222">Another thread has a password dialog box in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERRORE \_ Internet \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="81c2f-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR\_INTERNET\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-224">12163</span><span class="sxs-lookup"><span data-stu-id="81c2f-224">12163</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-225">La connessione Internet è stata persa.</span><span class="sxs-lookup"><span data-stu-id="81c2f-225">The Internet connection has been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**errore \_ Internet \_ esteso \_ errore**</span><span class="sxs-lookup"><span data-stu-id="81c2f-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**ERROR\_INTERNET\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-227">12003</span><span class="sxs-lookup"><span data-stu-id="81c2f-227">12003</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-228">Il server ha restituito un errore esteso.</span><span class="sxs-lookup"><span data-stu-id="81c2f-228">An extended error was returned from the server.</span></span> <span data-ttu-id="81c2f-229">Si tratta in genere di una stringa o di un buffer contenente un messaggio di errore dettagliato.</span><span class="sxs-lookup"><span data-stu-id="81c2f-229">This is typically a string or buffer containing a verbose error message.</span></span> <span data-ttu-id="81c2f-230">Chiamare [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) per recuperare il testo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="81c2f-230">Call [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) to retrieve the error text.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERRORE \_ Internet \_ DUETOSECURITYCHECK non riuscito \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR\_INTERNET\_FAILED\_DUETOSECURITYCHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-232">12171</span><span class="sxs-lookup"><span data-stu-id="81c2f-232">12171</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-233">La funzione non è riuscita a causa di un controllo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="81c2f-233">The function failed due to a security check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERRORE \_ Internet \_ Force \_ retry**</span><span class="sxs-lookup"><span data-stu-id="81c2f-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR\_INTERNET\_FORCE\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-235">12032</span><span class="sxs-lookup"><span data-stu-id="81c2f-235">12032</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-236">La funzione deve ripetere la richiesta.</span><span class="sxs-lookup"><span data-stu-id="81c2f-236">The function needs to redo the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERRORE \_ Internet \_ fortezza \_ login \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="81c2f-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR\_INTERNET\_FORTEZZA\_LOGIN\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-238">12054</span><span class="sxs-lookup"><span data-stu-id="81c2f-238">12054</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-239">La risorsa richiesta richiede l'autenticazione della fortezza.</span><span class="sxs-lookup"><span data-stu-id="81c2f-239">The requested resource requires Fortezza authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERRORE \_ \_ handle Internet \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="81c2f-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR\_INTERNET\_HANDLE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-241">12036</span><span class="sxs-lookup"><span data-stu-id="81c2f-241">12036</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-242">La richiesta non è riuscita perché l'handle esiste già.</span><span class="sxs-lookup"><span data-stu-id="81c2f-242">The request failed because the handle already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERRORE \_ \_ da http \_ a HTTPS da Internet a \_ \_ \_ redir**</span><span class="sxs-lookup"><span data-stu-id="81c2f-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-244">12039</span><span class="sxs-lookup"><span data-stu-id="81c2f-244">12039</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-245">L'applicazione sta migrando da un non SSL a una connessione SSL a causa di un reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="81c2f-245">The application is moving from a non-SSL to an SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERRORE \_ Internet \_ https \_ http \_ Submit \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR\_INTERNET\_HTTPS\_HTTP\_SUBMIT\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-247">12052</span><span class="sxs-lookup"><span data-stu-id="81c2f-247">12052</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-248">I dati inviati a una connessione SSL vengono reindirizzati a una connessione non SSL.</span><span class="sxs-lookup"><span data-stu-id="81c2f-248">The data being submitted to an SSL connection is being redirected to a non-SSL connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERRORE \_ \_ da Internet https \_ a \_ http \_ in \_ redir**</span><span class="sxs-lookup"><span data-stu-id="81c2f-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-250">12040</span><span class="sxs-lookup"><span data-stu-id="81c2f-250">12040</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-251">L'applicazione sta migrando da un SSL a una connessione non SSL a causa di un reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="81c2f-251">The application is moving from an SSL to an non-SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERRORE \_ nel \_ formato Internet errato \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR\_INTERNET\_INCORRECT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-253">12027</span><span class="sxs-lookup"><span data-stu-id="81c2f-253">12027</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-254">Il formato della richiesta non è valido.</span><span class="sxs-lookup"><span data-stu-id="81c2f-254">The format of the request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERRORE \_ Internet \_ \_ handle errato \_ stato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-256">12019</span><span class="sxs-lookup"><span data-stu-id="81c2f-256">12019</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-257">Non è possibile eseguire l'operazione richiesta perché l'handle specificato non è nello stato corretto.</span><span class="sxs-lookup"><span data-stu-id="81c2f-257">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERRORE \_ di \_ \_ tipo handle Internet errato \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-259">12018</span><span class="sxs-lookup"><span data-stu-id="81c2f-259">12018</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-260">Il tipo di handle fornito non è corretto per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="81c2f-260">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERRORE \_ di \_ Internet \_ password errata**</span><span class="sxs-lookup"><span data-stu-id="81c2f-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR\_INTERNET\_INCORRECT\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-262">12014</span><span class="sxs-lookup"><span data-stu-id="81c2f-262">12014</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-263">Non è stato possibile completare la richiesta di connessione e accesso a un server FTP perché la password specificata non è corretta.</span><span class="sxs-lookup"><span data-stu-id="81c2f-263">The request to connect and log on to an FTP server could not be completed because the supplied password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERRORE \_ \_ \_ nome utente Internet errato \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR\_INTERNET\_INCORRECT\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-265">12013</span><span class="sxs-lookup"><span data-stu-id="81c2f-265">12013</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-266">Non è stato possibile completare la richiesta di connessione e accesso a un server FTP perché il nome utente specificato non è corretto.</span><span class="sxs-lookup"><span data-stu-id="81c2f-266">The request to connect and log on to an FTP server could not be completed because the supplied user name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERRORE in \_ Internet \_ Insert \_ CDROM**</span><span class="sxs-lookup"><span data-stu-id="81c2f-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR\_INTERNET\_INSERT\_CDROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-268">12053</span><span class="sxs-lookup"><span data-stu-id="81c2f-268">12053</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-269">La richiesta richiede l'inserimento di un CD-ROM nell'unità CD-ROM per individuare la risorsa richiesta.</span><span class="sxs-lookup"><span data-stu-id="81c2f-269">The request requires a CD-ROM to be inserted in the CD-ROM drive to locate the resource requested.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-270">Windows Vista e Windows Server 2008 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-270">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**errore \_ \_ interno Internet \_ errore**</span><span class="sxs-lookup"><span data-stu-id="81c2f-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**ERROR\_INTERNET\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-272">12004</span><span class="sxs-lookup"><span data-stu-id="81c2f-272">12004</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-273">Si è verificato un errore interno.</span><span class="sxs-lookup"><span data-stu-id="81c2f-273">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERRORE \_ Internet \_ CA non valida \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR\_INTERNET\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-275">12045</span><span class="sxs-lookup"><span data-stu-id="81c2f-275">12045</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-276">La funzione non ha familiarità con l'autorità di certificazione che ha generato il certificato del server.</span><span class="sxs-lookup"><span data-stu-id="81c2f-276">The function is unfamiliar with the Certificate Authority that generated the server's certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERRORE \_ Internet \_ operazione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR\_INTERNET\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-278">12016</span><span class="sxs-lookup"><span data-stu-id="81c2f-278">12016</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-279">L'operazione richiesta non è valida.</span><span class="sxs-lookup"><span data-stu-id="81c2f-279">The requested operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERRORE \_ Internet \_ opzione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR\_INTERNET\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-281">12009</span><span class="sxs-lookup"><span data-stu-id="81c2f-281">12009</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-282">Una richiesta a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) ha specificato un valore di opzione non valido.</span><span class="sxs-lookup"><span data-stu-id="81c2f-282">A request to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERRORE \_ di \_ \_ richiesta proxy Internet non valida \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR\_INTERNET\_INVALID\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-284">12033</span><span class="sxs-lookup"><span data-stu-id="81c2f-284">12033</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-285">La richiesta al proxy non è valida.</span><span class="sxs-lookup"><span data-stu-id="81c2f-285">The request to the proxy was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERRORE \_ \_ URL Internet non valido \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR\_INTERNET\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-287">12005</span><span class="sxs-lookup"><span data-stu-id="81c2f-287">12005</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-288">L'URL non è valido.</span><span class="sxs-lookup"><span data-stu-id="81c2f-288">The URL is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERRORE \_ \_ elemento Internet \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR\_INTERNET\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-290">12028</span><span class="sxs-lookup"><span data-stu-id="81c2f-290">12028</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-291">Impossibile trovare l'elemento richiesto.</span><span class="sxs-lookup"><span data-stu-id="81c2f-291">The requested item could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**errore \_ di \_ accesso Internet errore \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-293">12015</span><span class="sxs-lookup"><span data-stu-id="81c2f-293">12015</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-294">La richiesta di connessione e accesso a un server FTP non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="81c2f-294">The request to connect and log on to an FTP server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**errore \_ di \_ accesso Internet errore \_ \_ visualizzazione \_ \_ corpo entità**</span><span class="sxs-lookup"><span data-stu-id="81c2f-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-296">12174</span><span class="sxs-lookup"><span data-stu-id="81c2f-296">12174</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-297">Il MS-Logoff intestazione digest è stato restituito dal sito Web.</span><span class="sxs-lookup"><span data-stu-id="81c2f-297">The MS-Logoff digest header has been returned from the website.</span></span> <span data-ttu-id="81c2f-298">Questa intestazione indica in modo specifico al pacchetto digest di ripulire le credenziali per l'area di autenticazione associata.</span><span class="sxs-lookup"><span data-stu-id="81c2f-298">This header specifically instructs the digest package to purge credentials for the associated realm.</span></span> <span data-ttu-id="81c2f-299">Questo errore viene restituito solo se è stata impostata l'opzione del [ \_ \_ \_ \_ \_ \_ \_ corpo dell'entità Visualizza errore di accesso alla maschera di errore Internet](option-flags.md) ; in caso contrario, viene restituito un errore di **\_ \_ accesso \_ a Internet** .</span><span class="sxs-lookup"><span data-stu-id="81c2f-299">This error will only be returned if [INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY](option-flags.md) option has been set; otherwise, **ERROR\_INTERNET\_LOGIN\_FAILURE** is returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERRORE di \_ sicurezza di Internet \_ mista \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR\_INTERNET\_MIXED\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-301">12041</span><span class="sxs-lookup"><span data-stu-id="81c2f-301">12041</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-302">Il contenuto non è interamente sicuro.</span><span class="sxs-lookup"><span data-stu-id="81c2f-302">The content is not entirely secure.</span></span> <span data-ttu-id="81c2f-303">Parte del contenuto visualizzato potrebbe provenire da server non protetti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-303">Some of the content being viewed may have come from unsecured servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERRORE \_ \_ nome Internet \_ non \_ risolto**</span><span class="sxs-lookup"><span data-stu-id="81c2f-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR\_INTERNET\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-305">12007</span><span class="sxs-lookup"><span data-stu-id="81c2f-305">12007</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-306">Non è stato possibile risolvere il nome del server.</span><span class="sxs-lookup"><span data-stu-id="81c2f-306">The server name could not be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERRORE \_ Internet \_ necessario \_ MSN \_ SSPI SSPI \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR\_INTERNET\_NEED\_MSN\_SSPI\_PKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-308">12173</span><span class="sxs-lookup"><span data-stu-id="81c2f-308">12173</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-309">Non implementato attualmente.</span><span class="sxs-lookup"><span data-stu-id="81c2f-309">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERRORE \_ Internet \_ richiesta \_ interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="81c2f-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR\_INTERNET\_NEED\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-311">12034</span><span class="sxs-lookup"><span data-stu-id="81c2f-311">12034</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-312">È stata richiesta un'interfaccia utente o un'altra operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="81c2f-312">A user interface or other blocking operation has been requested.</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-313">Windows Vista e Windows Server 2008 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="81c2f-313">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERRORE \_ Internet \_ senza \_ callback**</span><span class="sxs-lookup"><span data-stu-id="81c2f-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR\_INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-315">12025</span><span class="sxs-lookup"><span data-stu-id="81c2f-315">12025</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-316">Impossibile effettuare una richiesta asincrona perché una funzione di callback non è stata impostata.</span><span class="sxs-lookup"><span data-stu-id="81c2f-316">An asynchronous request could not be made because a callback function has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERRORE \_ Internet \_ senza \_ contesto**</span><span class="sxs-lookup"><span data-stu-id="81c2f-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR\_INTERNET\_NO\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-318">12024</span><span class="sxs-lookup"><span data-stu-id="81c2f-318">12024</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-319">Impossibile effettuare una richiesta asincrona perché è stato specificato un valore di contesto zero.</span><span class="sxs-lookup"><span data-stu-id="81c2f-319">An asynchronous request could not be made because a zero context value was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERRORE \_ Internet \_ senza \_ \_ accesso diretto**</span><span class="sxs-lookup"><span data-stu-id="81c2f-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR\_INTERNET\_NO\_DIRECT\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-321">12023</span><span class="sxs-lookup"><span data-stu-id="81c2f-321">12023</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-322">Non è possibile effettuare l'accesso diretto alla rete in questo momento.</span><span class="sxs-lookup"><span data-stu-id="81c2f-322">Direct network access cannot be made at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERRORE \_ Internet \_ non \_ inizializzato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR\_INTERNET\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-324">12172</span><span class="sxs-lookup"><span data-stu-id="81c2f-324">12172</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-325">Non è stata eseguita l'inizializzazione dell'API WinINet.</span><span class="sxs-lookup"><span data-stu-id="81c2f-325">Initialization of the WinINet API has not occurred.</span></span> <span data-ttu-id="81c2f-326">Indica che una funzione di livello superiore, ad esempio [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena), non è ancora stata chiamata.</span><span class="sxs-lookup"><span data-stu-id="81c2f-326">Indicates that a higher-level function, such as [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), has not been called yet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERRORE \_ Internet \_ non \_ \_ richiesta proxy**</span><span class="sxs-lookup"><span data-stu-id="81c2f-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR\_INTERNET\_NOT\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-328">12020</span><span class="sxs-lookup"><span data-stu-id="81c2f-328">12020</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-329">La richiesta non può essere effettuata tramite un proxy.</span><span class="sxs-lookup"><span data-stu-id="81c2f-329">The request cannot be made via a proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERRORE \_ \_ operazione Internet \_ annullata**</span><span class="sxs-lookup"><span data-stu-id="81c2f-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR\_INTERNET\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-331">12017</span><span class="sxs-lookup"><span data-stu-id="81c2f-331">12017</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-332">L'operazione è stata annullata, in genere perché l'handle su cui era in funzione la richiesta è stato chiuso prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="81c2f-332">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**\_opzione Internet di errore \_ \_ non \_ impostabile**</span><span class="sxs-lookup"><span data-stu-id="81c2f-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR\_INTERNET\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-334">12011</span><span class="sxs-lookup"><span data-stu-id="81c2f-334">12011</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-335">Impossibile impostare l'opzione richiesta, solo query.</span><span class="sxs-lookup"><span data-stu-id="81c2f-335">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERRORE \_ \_ di Internet \_ degli \_ handle**</span><span class="sxs-lookup"><span data-stu-id="81c2f-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR\_INTERNET\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-337">12001</span><span class="sxs-lookup"><span data-stu-id="81c2f-337">12001</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-338">Al momento non è stato possibile generare più handle.</span><span class="sxs-lookup"><span data-stu-id="81c2f-338">No more handles could be generated at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERRORE \_ Internet \_ Post \_ \_ non \_ sicuro**</span><span class="sxs-lookup"><span data-stu-id="81c2f-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-340">12043</span><span class="sxs-lookup"><span data-stu-id="81c2f-340">12043</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-341">L'applicazione sta inviando i dati a un server non protetto.</span><span class="sxs-lookup"><span data-stu-id="81c2f-341">The application is posting data to a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERRORE \_ \_ protocollo Internet \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR\_INTERNET\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-343">12008</span><span class="sxs-lookup"><span data-stu-id="81c2f-343">12008</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-344">Il protocollo richiesto non è stato individuato.</span><span class="sxs-lookup"><span data-stu-id="81c2f-344">The requested protocol could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERRORE \_ \_ server proxy Internet non \_ \_ raggiungibile**</span><span class="sxs-lookup"><span data-stu-id="81c2f-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR\_INTERNET\_PROXY\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-346">12165</span><span class="sxs-lookup"><span data-stu-id="81c2f-346">12165</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-347">Impossibile raggiungere il server proxy designato.</span><span class="sxs-lookup"><span data-stu-id="81c2f-347">The designated proxy server cannot be reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERRORE \_ di \_ \_ modifica dello schema di reindirizzamento Internet \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR\_INTERNET\_REDIRECT\_SCHEME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-349">12048</span><span class="sxs-lookup"><span data-stu-id="81c2f-349">12048</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-350">La funzione non è stata in grado di gestire il reindirizzamento perché lo schema è stato modificato (ad esempio, da HTTP ad FTP).</span><span class="sxs-lookup"><span data-stu-id="81c2f-350">The function could not handle the redirection, because the scheme changed (for example, HTTP to FTP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERRORE \_ \_ valore registro di sistema Internet \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR\_INTERNET\_REGISTRY\_VALUE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-352">12021</span><span class="sxs-lookup"><span data-stu-id="81c2f-352">12021</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-353">Impossibile trovare un valore obbligatorio del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="81c2f-353">A required registry value could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**\_richiesta Internet di errore \_ \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="81c2f-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERROR\_INTERNET\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-355">12026</span><span class="sxs-lookup"><span data-stu-id="81c2f-355">12026</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-356">Non è stato possibile completare l'operazione richiesta perché una o più richieste sono in sospeso.</span><span class="sxs-lookup"><span data-stu-id="81c2f-356">The required operation could not be completed because one or more requests are pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**\_finestra di \_ dialogo Riprova Internet errore \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**ERROR\_INTERNET\_RETRY\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-358">12050</span><span class="sxs-lookup"><span data-stu-id="81c2f-358">12050</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-359">È necessario ritentare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="81c2f-359">The dialog box should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERRORE per il \_ \_ certificato CN di Internet sec \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="81c2f-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-361">12038</span><span class="sxs-lookup"><span data-stu-id="81c2f-361">12038</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-362">Il nome comune del certificato SSL (campo nome host) non è corretto, ad esempio se è stato immesso www.server.com e il nome comune nel certificato è www.different.com.</span><span class="sxs-lookup"><span data-stu-id="81c2f-362">SSL certificate common name (host name field) is incorrect for example, if you entered www.server.com and the common name on the certificate says www.different.com.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERRORE in \_ Internet \_ sec \_ CERT \_ data \_ non valida**</span><span class="sxs-lookup"><span data-stu-id="81c2f-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-364">12037</span><span class="sxs-lookup"><span data-stu-id="81c2f-364">12037</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-365">La data del certificato SSL ricevuta dal server non è valida.</span><span class="sxs-lookup"><span data-stu-id="81c2f-365">SSL certificate date that was received from the server is bad.</span></span> <span data-ttu-id="81c2f-366">Il certificato è scaduto.</span><span class="sxs-lookup"><span data-stu-id="81c2f-366">The certificate is expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**\_errori del certificato di Internet \_ sec errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-368">12055</span><span class="sxs-lookup"><span data-stu-id="81c2f-368">12055</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-369">Il certificato SSL contiene errori.</span><span class="sxs-lookup"><span data-stu-id="81c2f-369">The SSL certificate contains errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERRORE \_ Internet \_ sec \_ CERT \_ No \_ REV**</span><span class="sxs-lookup"><span data-stu-id="81c2f-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR\_INTERNET\_SEC\_CERT\_NO\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-371">12056</span><span class="sxs-lookup"><span data-stu-id="81c2f-371">12056</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-372">Il certificato SSL non è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="81c2f-372">The SSL certificate was not revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERRORE di \_ Internet \_ sec \_ CERT \_ rev \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="81c2f-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR\_INTERNET\_SEC\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-374">12057</span><span class="sxs-lookup"><span data-stu-id="81c2f-374">12057</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-375">Revoca del certificato SSL non riuscita.</span><span class="sxs-lookup"><span data-stu-id="81c2f-375">Revocation of the SSL certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERRORE \_ \_ certificato Internet \_ sec \_ revocato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR\_INTERNET\_SEC\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-377">12170</span><span class="sxs-lookup"><span data-stu-id="81c2f-377">12170</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-378">Il certificato SSL è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="81c2f-378">The SSL certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERRORE \_ di \_ \_ certificato non valido per Internet sec \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR\_INTERNET\_SEC\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-380">12169</span><span class="sxs-lookup"><span data-stu-id="81c2f-380">12169</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-381">Il certificato SSL non è valido.</span><span class="sxs-lookup"><span data-stu-id="81c2f-381">The SSL certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**errore \_ \_ canale di sicurezza Internet \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**ERROR\_INTERNET\_SECURITY\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-383">12157</span><span class="sxs-lookup"><span data-stu-id="81c2f-383">12157</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-384">Si è verificato un errore interno durante il caricamento delle librerie SSL.</span><span class="sxs-lookup"><span data-stu-id="81c2f-384">The application experienced an internal error loading the SSL libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERRORE \_ server Internet non \_ \_ raggiungibile**</span><span class="sxs-lookup"><span data-stu-id="81c2f-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR\_INTERNET\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-386">12164</span><span class="sxs-lookup"><span data-stu-id="81c2f-386">12164</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-387">Il sito Web o il server indicato non è raggiungibile.</span><span class="sxs-lookup"><span data-stu-id="81c2f-387">The website or server indicated is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERRORE \_ di \_ arresto Internet**</span><span class="sxs-lookup"><span data-stu-id="81c2f-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR\_INTERNET\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-389">12012</span><span class="sxs-lookup"><span data-stu-id="81c2f-389">12012</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-390">È in corso l'arresto o lo scaricamento del supporto di WinINet.</span><span class="sxs-lookup"><span data-stu-id="81c2f-390">WinINet support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERRORE \_ Internet \_ TCPIP \_ non \_ installato**</span><span class="sxs-lookup"><span data-stu-id="81c2f-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR\_INTERNET\_TCPIP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-392">12159</span><span class="sxs-lookup"><span data-stu-id="81c2f-392">12159</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-393">Lo stack di protocolli richiesto non è caricato e l'applicazione non può avviare WinSock.</span><span class="sxs-lookup"><span data-stu-id="81c2f-393">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**\_timeout Internet \_ errore**</span><span class="sxs-lookup"><span data-stu-id="81c2f-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR\_INTERNET\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-395">12002</span><span class="sxs-lookup"><span data-stu-id="81c2f-395">12002</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-396">Timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="81c2f-396">The request has timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERRORE \_ Internet \_ non è possibile \_ \_ memorizzare nella cache il \_ file**</span><span class="sxs-lookup"><span data-stu-id="81c2f-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR\_INTERNET\_UNABLE\_TO\_CACHE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-398">12158</span><span class="sxs-lookup"><span data-stu-id="81c2f-398">12158</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-399">La funzione non è in grado di memorizzare il file nella cache.</span><span class="sxs-lookup"><span data-stu-id="81c2f-399">The function was unable to cache the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERRORE \_ Internet \_ non è possibile \_ \_ scaricare \_ lo script**</span><span class="sxs-lookup"><span data-stu-id="81c2f-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR\_INTERNET\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-401">12167</span><span class="sxs-lookup"><span data-stu-id="81c2f-401">12167</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-402">Non è stato possibile scaricare lo script di configurazione automatica del proxy.</span><span class="sxs-lookup"><span data-stu-id="81c2f-402">The automatic proxy configuration script could not be downloaded.</span></span> <span data-ttu-id="81c2f-403">Il \_ flag Internet \_ deve \_ \_ essere impostato come flag della richiesta della cache.</span><span class="sxs-lookup"><span data-stu-id="81c2f-403">The INTERNET\_FLAG\_MUST\_CACHE\_REQUEST flag was set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**schema di errore \_ Internet non \_ riconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR\_INTERNET\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81c2f-405">12006</span><span class="sxs-lookup"><span data-stu-id="81c2f-405">12006</span></span>
</dt> <dt>



<span data-ttu-id="81c2f-406">Non è stato possibile riconoscere lo schema URL oppure non è supportato.</span><span class="sxs-lookup"><span data-stu-id="81c2f-406">The URL scheme could not be recognized, or is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERRORE \_ handle non valido \_**</span><span class="sxs-lookup"><span data-stu-id="81c2f-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81c2f-408">L'handle passato all'API è stato invalidato o chiuso.</span><span class="sxs-lookup"><span data-stu-id="81c2f-408">The handle that was passed to the API has been either invalidated or closed.</span></span>

<span data-ttu-id="81c2f-409">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="81c2f-409">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERRORE di \_ più \_ dati**</span><span class="sxs-lookup"><span data-stu-id="81c2f-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81c2f-411">sono disponibili più dati.</span><span class="sxs-lookup"><span data-stu-id="81c2f-411">More data is available.</span></span>

<span data-ttu-id="81c2f-412">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="81c2f-412">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRORE \_ nessun \_ altro \_ file**</span><span class="sxs-lookup"><span data-stu-id="81c2f-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81c2f-414">Non sono stati trovati altri file.</span><span class="sxs-lookup"><span data-stu-id="81c2f-414">No more files have been found.</span></span>

<span data-ttu-id="81c2f-415">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="81c2f-415">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81c2f-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRORE \_ nessun \_ altro \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="81c2f-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81c2f-417">Non sono stati trovati altri elementi.</span><span class="sxs-lookup"><span data-stu-id="81c2f-417">No more items have been found.</span></span>

<span data-ttu-id="81c2f-418">**Intestazione:** Dichiarata in Winerror. h</span><span class="sxs-lookup"><span data-stu-id="81c2f-418">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81c2f-419">Commenti</span><span class="sxs-lookup"><span data-stu-id="81c2f-419">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="81c2f-420">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="81c2f-420">WinINet does not support server implementations.</span></span> <span data-ttu-id="81c2f-421">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="81c2f-421">In addition, it should not be used from a service.</span></span> <span data-ttu-id="81c2f-422">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="81c2f-422">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81c2f-423">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81c2f-423">Requirements</span></span>



| <span data-ttu-id="81c2f-424">Requisito</span><span class="sxs-lookup"><span data-stu-id="81c2f-424">Requirement</span></span> | <span data-ttu-id="81c2f-425">Valore</span><span class="sxs-lookup"><span data-stu-id="81c2f-425">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81c2f-426">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81c2f-426">Minimum supported client</span></span><br/> | <span data-ttu-id="81c2f-427">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81c2f-427">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="81c2f-428">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81c2f-428">Minimum supported server</span></span><br/> | <span data-ttu-id="81c2f-429">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81c2f-429">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="81c2f-430">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81c2f-430">Header</span></span><br/>                   | <dl> <span data-ttu-id="81c2f-431"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="81c2f-431"><dt>Wininet.h</dt></span></span> </dl> |



 

