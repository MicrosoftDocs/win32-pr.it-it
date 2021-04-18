---
title: Flag di opzione (WinInet. h)
description: I flag di opzione seguenti vengono utilizzati con le funzioni InternetQueryOption e InternetSetOption. Tutti i flag di opzione validi hanno un valore maggiore o uguale a INTERNET \_ prima opzione \_ e minore o uguale a Internet \_ Ultima \_ opzione.
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302736"
---
# <a name="option-flags-winineth"></a><span data-ttu-id="c281b-104">Flag di opzione (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="c281b-104">Option Flags (Wininet.h)</span></span>

<span data-ttu-id="c281b-105">I flag di opzione seguenti vengono utilizzati con le funzioni [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) .</span><span class="sxs-lookup"><span data-stu-id="c281b-105">The following option flags are used with the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) functions.</span></span> <span data-ttu-id="c281b-106">Tutti i flag di opzione validi hanno un valore maggiore o uguale **a \_ Internet \_ prima** opzione e minore o uguale a **Internet \_ Ultima \_ opzione**.</span><span class="sxs-lookup"><span data-stu-id="c281b-106">All valid option flags have a value greater than or equal to **INTERNET\_FIRST\_OPTION** and less than or equal to **INTERNET\_LAST\_OPTION**.</span></span>

<dl> <dt>

<span data-ttu-id="c281b-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**\_opzione Internet \_ ALTER \_ Identity**</span><span class="sxs-lookup"><span data-stu-id="c281b-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**INTERNET\_OPTION\_ALTER\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-108">80</span><span class="sxs-lookup"><span data-stu-id="c281b-108">80</span></span>
</dt> <dt>



<span data-ttu-id="c281b-109">Non implementato</span><span class="sxs-lookup"><span data-stu-id="c281b-109">Not implemented</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**\_opzione Internet \_ Async**</span><span class="sxs-lookup"><span data-stu-id="c281b-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**INTERNET\_OPTION\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-111">30</span><span class="sxs-lookup"><span data-stu-id="c281b-111">30</span></span>
</dt> <dt>



<span data-ttu-id="c281b-112">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-112">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**\_ \_ ID async opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**INTERNET\_OPTION\_ASYNC\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-114">15</span><span class="sxs-lookup"><span data-stu-id="c281b-114">15</span></span>
</dt> <dt>



<span data-ttu-id="c281b-115">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-115">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**\_opzione Internet \_ - \_ priorità asincrona**</span><span class="sxs-lookup"><span data-stu-id="c281b-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**INTERNET\_OPTION\_ASYNC\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-117">16</span><span class="sxs-lookup"><span data-stu-id="c281b-117">16</span></span>
</dt> <dt>



<span data-ttu-id="c281b-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-118">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**\_opzione Internet \_ ignorare \_ \_ voce modificata**</span><span class="sxs-lookup"><span data-stu-id="c281b-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**INTERNET\_OPTION\_BYPASS\_EDITED\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-120">64</span><span class="sxs-lookup"><span data-stu-id="c281b-120">64</span></span>
</dt> <dt>



<span data-ttu-id="c281b-121">Imposta o Recupera il valore booleano che determina se il sistema deve controllare la rete per il contenuto più recente e sovrascrivere le voci della cache modificate se viene rilevata una versione più recente.</span><span class="sxs-lookup"><span data-stu-id="c281b-121">Sets or retrieves the Boolean value that determines if the system should check the network for newer content and overwrite edited cache entries if a newer version is found.</span></span> <span data-ttu-id="c281b-122">Se impostato su **true**, il sistema controlla la rete per il contenuto più recente e sovrascrive la voce della cache modificata con la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="c281b-122">If set to **True**, the system checks the network for newer content and overwrites the edited cache entry with the newer version.</span></span> <span data-ttu-id="c281b-123">Il valore predefinito è **false**, che indica che la voce della cache modificata deve essere utilizzata senza controllare la rete.</span><span class="sxs-lookup"><span data-stu-id="c281b-123">The default is **False**, which indicates that the edited cache entry should be used without checking the network.</span></span> <span data-ttu-id="c281b-124">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-124">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-125">È valido solo in Microsoft Internet Explorer 5 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-125">It is valid only in Microsoft Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**\_handle del \_ flusso della cache delle opzioni \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**INTERNET\_OPTION\_CACHE\_STREAM\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-127">27</span><span class="sxs-lookup"><span data-stu-id="c281b-127">27</span></span>
</dt> <dt>



<span data-ttu-id="c281b-128">Non più supportata.</span><span class="sxs-lookup"><span data-stu-id="c281b-128">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**\_ \_ timestamp della cache delle opzioni Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**INTERNET\_OPTION\_CACHE\_TIMESTAMPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-130">69</span><span class="sxs-lookup"><span data-stu-id="c281b-130">69</span></span>
</dt> <dt>



<span data-ttu-id="c281b-131">Recupera una struttura di [**\_ \_ timestamp della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) che contiene l'ora LastModified e scade l'ora dalla risorsa archiviata nella cache Internet.</span><span class="sxs-lookup"><span data-stu-id="c281b-131">Retrieves an [**INTERNET\_CACHE\_TIMESTAMPS**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) structure that contains the LastModified time and Expires time from the resource stored in the Internet cache.</span></span> <span data-ttu-id="c281b-132">Questo valore viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-132">This value is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**\_callback opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**INTERNET\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-134">1</span><span class="sxs-lookup"><span data-stu-id="c281b-134">1</span></span>
</dt> <dt>



<span data-ttu-id="c281b-135">Imposta o recupera l'indirizzo della funzione di callback definita per questo handle.</span><span class="sxs-lookup"><span data-stu-id="c281b-135">Sets or retrieves the address of the callback function defined for this handle.</span></span> <span data-ttu-id="c281b-136">Questa opzione può essere usata in tutti gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="c281b-136">This option can be used on all [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="c281b-137">Usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-137">Used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**\_filtro di \_ callback delle opzioni Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**INTERNET\_OPTION\_CALLBACK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-139">54</span><span class="sxs-lookup"><span data-stu-id="c281b-139">54</span></span>
</dt> <dt>



<span data-ttu-id="c281b-140">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-140">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**\_contesto del \_ \_ certificato client dell'opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**INTERNET\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-142">84</span><span class="sxs-lookup"><span data-stu-id="c281b-142">84</span></span>
</dt> <dt>



<span data-ttu-id="c281b-143">Questo flag non è supportato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-143">This flag is not supported by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="c281b-144">Il parametro *lpBuffer* deve essere un puntatore a una struttura del [**\_ contesto del certificato**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) e non un puntatore a un puntatore di **\_ contesto del certificato** .</span><span class="sxs-lookup"><span data-stu-id="c281b-144">The *lpBuffer* parameter must be a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure and not a pointer to a **CERT\_CONTEXT** pointer.</span></span> <span data-ttu-id="c281b-145">Se un'applicazione riceve l'errore certificato di **\_ \_ autenticazione client Internet \_ \_ \_ necessario**, deve chiamare [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o usare [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per fornire un certificato prima di ritentare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c281b-145">If an application receives **ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**, it must call [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or use [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="c281b-146">[**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) viene quindi chiamato in modo che il contesto del certificato passato possa essere rilasciato in modo indipendente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c281b-146">[**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) is then called so that the certificate context passed can be independently released by the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**opzione INTERNET (tabella \_ \_ codici)**</span><span class="sxs-lookup"><span data-stu-id="c281b-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**INTERNET\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-148">68</span><span class="sxs-lookup"><span data-stu-id="c281b-148">68</span></span>
</dt> <dt>



<span data-ttu-id="c281b-149">Per impostazione predefinita, la parte relativa all'host o all'autorità dell'URL Unicode viene codificata in base alla specifica IDN.</span><span class="sxs-lookup"><span data-stu-id="c281b-149">By default, the host or authority portion of the Unicode URL is encoded according to the IDN specification.</span></span> <span data-ttu-id="c281b-150">Impostando questa opzione sulla richiesta o sull'handle di connessione, quando IDN è disabilitato, viene specificato uno schema di codifica della tabella codici per la parte host dell'URL.</span><span class="sxs-lookup"><span data-stu-id="c281b-150">Setting this option on the request, or connection handle, when IDN is disabled, specifies a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="c281b-151">Il parametro *lpBuffer* nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la tabella codici DBCS desiderata.</span><span class="sxs-lookup"><span data-stu-id="c281b-151">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS code page.</span></span> <span data-ttu-id="c281b-152">Se in *lpBuffer* non è specificata alcuna tabella codici, WinInet usa la tabella codici di sistema predefinita (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="c281b-152">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span> <span data-ttu-id="c281b-153">Nota: questa opzione viene ignorata se IDN non è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c281b-153">Note: This option is ignored if IDN is not disabled.</span></span> <span data-ttu-id="c281b-154">Per ulteriori informazioni su come disabilitare IDN, vedere l'opzione **Internet \_ option \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="c281b-154">For more information about how to disable IDN, see the **INTERNET\_OPTION\_IDN** option.</span></span>

<span data-ttu-id="c281b-155">**Windows XP con SP2 e Windows Server 2003 con SP1:** Questo flag non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c281b-155">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="c281b-156">**Versione:** Richiede Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="c281b-156">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**\_opzione Internet \_ percorso tabella codici \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**INTERNET\_OPTION\_CODEPAGE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-158">100</span><span class="sxs-lookup"><span data-stu-id="c281b-158">100</span></span>
</dt> <dt>



<span data-ttu-id="c281b-159">Per impostazione predefinita, la parte del percorso dell'URL è con codifica UTF8.</span><span class="sxs-lookup"><span data-stu-id="c281b-159">By default, the path portion of the URL is UTF8 encoded.</span></span> <span data-ttu-id="c281b-160">L'API WinINet esegue il carattere di escape (%) codifica dei caratteri a bit significativo.</span><span class="sxs-lookup"><span data-stu-id="c281b-160">The WinINet API performs escape character (%) encoding on the high-bit characters.</span></span> <span data-ttu-id="c281b-161">Impostando questa opzione sulla richiesta o sull'handle di connessione, viene disabilitata la codifica UTF8 e viene impostata una tabella codici specifica.</span><span class="sxs-lookup"><span data-stu-id="c281b-161">Setting this option on the request, or connection handle, disables the UTF8 encoding and sets a specific code page.</span></span> <span data-ttu-id="c281b-162">Il parametro *lpBuffer* nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la tabella codici DBCS desiderata per il percorso.</span><span class="sxs-lookup"><span data-stu-id="c281b-162">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the path.</span></span> <span data-ttu-id="c281b-163">Se non viene specificata alcuna tabella codici in *lpBuffer*, WinInet usa il CP \_ UTF8 predefinito.</span><span class="sxs-lookup"><span data-stu-id="c281b-163">If no code page is specified in *lpBuffer*, WinINet uses the default CP\_UTF8.</span></span>

<span data-ttu-id="c281b-164">**Windows XP con SP2 e Windows Server 2003 con SP1:** Questo flag non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c281b-164">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="c281b-165">**Versione:** Richiede Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="c281b-165">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**opzione INTERNET-tabella \_ \_ codici \_ aggiuntivi**</span><span class="sxs-lookup"><span data-stu-id="c281b-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**INTERNET\_OPTION\_CODEPAGE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-167">101</span><span class="sxs-lookup"><span data-stu-id="c281b-167">101</span></span>
</dt> <dt>



<span data-ttu-id="c281b-168">Per impostazione predefinita, la parte del percorso dell'URL è la tabella codici di sistema predefinita (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="c281b-168">By default, the path portion of the URL is the default system code page (CP\_ACP).</span></span> <span data-ttu-id="c281b-169">Carattere di escape (%) le conversioni non vengono eseguite sulla parte aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="c281b-169">The escape character (%) conversions are not performed on the extra portion.</span></span> <span data-ttu-id="c281b-170">L'impostazione di questa opzione sulla richiesta o sull'handle di connessione Disabilita la \_ codifica CP ACP.</span><span class="sxs-lookup"><span data-stu-id="c281b-170">Setting this option on the request, or connection handle disables the CP\_ACP encoding.</span></span> <span data-ttu-id="c281b-171">Il parametro *lpBuffer* nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la tabella codici DBCS desiderata per la parte aggiuntiva dell'URL.</span><span class="sxs-lookup"><span data-stu-id="c281b-171">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the extra portion of the URL.</span></span> <span data-ttu-id="c281b-172">Se in *lpBuffer* non è specificata alcuna tabella codici, WinInet usa la tabella codici di sistema predefinita (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="c281b-172">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="c281b-173">**Windows XP con SP2 e Windows Server 2003 con SP1:** Questo flag non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c281b-173">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="c281b-174">**Versione:** Richiede Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="c281b-174">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**\_opzione Internet \_ - \_ lunghezza contenuto compresso \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**INTERNET\_OPTION\_COMPRESSED\_CONTENT\_LENGTH**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-176">147</span><span class="sxs-lookup"><span data-stu-id="c281b-176">147</span></span>
</dt> <dt>



<span data-ttu-id="c281b-177">Per una richiesta in cui WinInet decompressi la codifica del contenuto fornita dal server, recupera la lunghezza del contenuto segnalata dal server del corpo della risposta come ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="c281b-177">For a request where WinInet decompressed the server s supplied Content-Encoding, retrieves the server-reported Content-Length of the response body as a ULONGLONG.</span></span> <span data-ttu-id="c281b-178">Supportato in Windows 10, versione 1507 e successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-178">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**\_opzione Internet \_ Connect \_ BACKOFF**</span><span class="sxs-lookup"><span data-stu-id="c281b-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**INTERNET\_OPTION\_CONNECT\_BACKOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-180">4</span><span class="sxs-lookup"><span data-stu-id="c281b-180">4</span></span>
</dt> <dt>



<span data-ttu-id="c281b-181">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-181">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**opzioni INTERNET- \_ \_ tentativi di connessione \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**INTERNET\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-183">3</span><span class="sxs-lookup"><span data-stu-id="c281b-183">3</span></span>
</dt> <dt>



<span data-ttu-id="c281b-184">Imposta o recupera un valore long integer senza segno che contiene il numero di tentativi di WinINet per la risoluzione e la connessione a un host.</span><span class="sxs-lookup"><span data-stu-id="c281b-184">Sets or retrieves an unsigned long integer value that contains the number of times WinINet attempts to resolve and connect to a host.</span></span> <span data-ttu-id="c281b-185">Tenta solo una volta per ogni indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="c281b-185">It only attempts once per IP address.</span></span> <span data-ttu-id="c281b-186">Se ad esempio si tenta di connettersi a un host multihome con dieci indirizzi IP e l'opzione INTERNET \_ \_ tentativi di connessione \_ è impostata su sette, WinInet tenterà solo di risolvere e connettersi ai primi sette indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="c281b-186">For example, if you attempt to connect to a multihome host that has ten IP addresses and INTERNET\_OPTION\_CONNECT\_RETRIES is set to seven, WinINet only attempts to resolve and connect to the first seven IP addresses.</span></span> <span data-ttu-id="c281b-187">Viceversa, dato lo stesso set di dieci indirizzi IP, se l'opzione INTERNET \_ \_ tentativi di connessione \_ è impostata su 20, WinInet tenta ognuno dei dieci una sola volta.</span><span class="sxs-lookup"><span data-stu-id="c281b-187">Conversely, given the same set of ten IP addresses, if INTERNET\_OPTION\_CONNECT\_RETRIES is set to 20, WinINet attempts each of the ten only once.</span></span> <span data-ttu-id="c281b-188">Se un host dispone di un solo indirizzo IP e il primo tentativo di connessione ha esito negativo, non vengono eseguiti altri tentativi.</span><span class="sxs-lookup"><span data-stu-id="c281b-188">If a host has only one IP address and the first connection attempt fails, there are no further attempts.</span></span> <span data-ttu-id="c281b-189">Se un tentativo di connessione non riesce ancora dopo il numero di tentativi specificato, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="c281b-189">If a connection attempt still fails after the specified number of attempts, the request is canceled.</span></span> <span data-ttu-id="c281b-190">Il valore predefinito per i \_ tentativi di connessione all'opzione Internet \_ \_ è cinque tentativi.</span><span class="sxs-lookup"><span data-stu-id="c281b-190">The default value for INTERNET\_OPTION\_CONNECT\_RETRIES is five attempts.</span></span> <span data-ttu-id="c281b-191">Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="c281b-191">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="c281b-192">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-192">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**\_tempo di \_ connessione \_ opzione Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**INTERNET\_OPTION\_CONNECT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-194">55</span><span class="sxs-lookup"><span data-stu-id="c281b-194">55</span></span>
</dt> <dt>



<span data-ttu-id="c281b-195">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-195">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**\_opzione Internet \_ \_ timeout connessione**</span><span class="sxs-lookup"><span data-stu-id="c281b-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**INTERNET\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-197">2</span><span class="sxs-lookup"><span data-stu-id="c281b-197">2</span></span>
</dt> <dt>



<span data-ttu-id="c281b-198">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, da utilizzare per le richieste di connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="c281b-198">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to use for Internet connection requests.</span></span> <span data-ttu-id="c281b-199">Se si imposta questa opzione su infinito (0xFFFFFFFF), questo timer verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c281b-199">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="c281b-200">Se una richiesta di connessione richiede più tempo rispetto a questo valore di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="c281b-200">If a connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="c281b-201">Quando si tenta di connettersi a più indirizzi IP per un singolo host (host multihomed), il limite di timeout è cumulativo per tutti gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="c281b-201">When attempting to connect to multiple IP addresses for a single host (a multihome host), the timeout limit is cumulative for all of the IP addresses.</span></span> <span data-ttu-id="c281b-202">Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="c281b-202">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="c281b-203">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-203">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**\_opzione Internet \_ - \_ stato connesso**</span><span class="sxs-lookup"><span data-stu-id="c281b-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**INTERNET\_OPTION\_CONNECTED\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-205">50</span><span class="sxs-lookup"><span data-stu-id="c281b-205">50</span></span>
</dt> <dt>



<span data-ttu-id="c281b-206">Imposta o recupera un valore long integer senza segno che contiene lo stato connesso.</span><span class="sxs-lookup"><span data-stu-id="c281b-206">Sets or retrieves an unsigned long integer value that contains the connected state.</span></span> <span data-ttu-id="c281b-207">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-207">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**\_valore del \_ contesto dell'opzione Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**INTERNET\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-209">45</span><span class="sxs-lookup"><span data-stu-id="c281b-209">45</span></span>
</dt> <dt>



<span data-ttu-id="c281b-210">Imposta o recupera un \_ ptr DWORD che contiene l'indirizzo del valore di contesto associato a questo handle [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="c281b-210">Sets or retrieves a DWORD\_PTR that contains the address of the context value associated with this [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="c281b-211">Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="c281b-211">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="c281b-212">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-212">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-213">In precedenza, il valore del contesto veniva impostato sull'indirizzo archiviato nel puntatore **lpBuffer** .</span><span class="sxs-lookup"><span data-stu-id="c281b-213">Previously, this set the context value to the address stored in the **lpBuffer** pointer.</span></span> <span data-ttu-id="c281b-214">Questo problema è stato corretto in modo da usare il valore archiviato nel buffer e al flag del [ \_ valore del \_ contesto \_ dell'opzione Internet](/windows) viene assegnato un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="c281b-214">This has been corrected so that the value stored in the buffer is used and the [INTERNET\_OPTION\_CONTEXT\_VALUE](/windows) flag is assigned a new value.</span></span> <span data-ttu-id="c281b-215">Il valore precedente, 10, è stato mantenuto in modo che le applicazioni scritte per il comportamento precedente siano ancora supportate.</span><span class="sxs-lookup"><span data-stu-id="c281b-215">The old value, 10, has been preserved so that applications written for the old behavior are still supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**\_timeout di \_ \_ ricezione controllo opzione Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**INTERNET\_OPTION\_CONTROL\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-217">6</span><span class="sxs-lookup"><span data-stu-id="c281b-217">6</span></span>
</dt> <dt>



<span data-ttu-id="c281b-218">Il [ \_ \_ \_ timeout di ricezione](/windows)è identico a Internet.</span><span class="sxs-lookup"><span data-stu-id="c281b-218">Identical to [INTERNET\_OPTION\_RECEIVE\_TIMEOUT](/windows).</span></span> <span data-ttu-id="c281b-219">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-219">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**\_timeout di \_ invio del controllo opzioni \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**INTERNET\_OPTION\_CONTROL\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-221">5</span><span class="sxs-lookup"><span data-stu-id="c281b-221">5</span></span>
</dt> <dt>



<span data-ttu-id="c281b-222">Il [ \_ \_ \_ timeout di invio](/windows)è identico a Internet.</span><span class="sxs-lookup"><span data-stu-id="c281b-222">Identical to [INTERNET\_OPTION\_SEND\_TIMEOUT](/windows).</span></span> <span data-ttu-id="c281b-223">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-223">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**\_ \_ \_ timeout ricezione dati opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**INTERNET\_OPTION\_DATA\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-225">8</span><span class="sxs-lookup"><span data-stu-id="c281b-225">8</span></span>
</dt> <dt>



<span data-ttu-id="c281b-226">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per ricevere una risposta a una richiesta per il canale dati di una transazione FTP.</span><span class="sxs-lookup"><span data-stu-id="c281b-226">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="c281b-227">Se la risposta richiede più tempo rispetto a questo valore di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="c281b-227">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="c281b-228">Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="c281b-228">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="c281b-229">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-229">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="c281b-230">Questo flag non ha alcun effetto sulla funzionalità HTTP.</span><span class="sxs-lookup"><span data-stu-id="c281b-230">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**\_ \_ \_ timeout invio dati opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**INTERNET\_OPTION\_DATA\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-232">7</span><span class="sxs-lookup"><span data-stu-id="c281b-232">7</span></span>
</dt> <dt>



<span data-ttu-id="c281b-233">Imposta o recupera un valore long integer senza segno, in millisecondi, che contiene il valore di timeout per inviare una richiesta per il canale dati di una transazione FTP.</span><span class="sxs-lookup"><span data-stu-id="c281b-233">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="c281b-234">Se l'invio richiede più tempo rispetto a questo valore di timeout, l'invio viene annullato.</span><span class="sxs-lookup"><span data-stu-id="c281b-234">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="c281b-235">Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="c281b-235">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="c281b-236">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-236">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="c281b-237">Questo flag non ha alcun effetto sulla funzionalità HTTP.</span><span class="sxs-lookup"><span data-stu-id="c281b-237">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**\_nome dell'opzione Internet \_ DataFile \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**INTERNET\_OPTION\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-239">33</span><span class="sxs-lookup"><span data-stu-id="c281b-239">33</span></span>
</dt> <dt>



<span data-ttu-id="c281b-240">Recupera un valore stringa che contiene il nome del file che esegue il backup di un'entità scaricata.</span><span class="sxs-lookup"><span data-stu-id="c281b-240">Retrieves a string value that contains the name of the file backing a downloaded entity.</span></span> <span data-ttu-id="c281b-241">Questo flag è valido dopo il completamento di [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="c281b-241">This flag is valid after [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) has completed.</span></span> <span data-ttu-id="c281b-242">È possibile eseguire query su questa opzione solo con [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-242">This option can only be queried by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**\_opzione Internet \_ filedatafile \_ ext**</span><span class="sxs-lookup"><span data-stu-id="c281b-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**INTERNET\_OPTION\_DATAFILE\_EXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-244">96</span><span class="sxs-lookup"><span data-stu-id="c281b-244">96</span></span>
</dt> <dt>



<span data-ttu-id="c281b-245">Imposta un valore stringa che contiene l'estensione del file che esegue il backup di un'entità scaricata.</span><span class="sxs-lookup"><span data-stu-id="c281b-245">Sets a string value that contains the extension of the file backing a downloaded entity.</span></span> <span data-ttu-id="c281b-246">Questo flag deve essere impostato prima di chiamare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="c281b-246">This flag should be set before calling [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="c281b-247">Questa opzione può essere impostata solo da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-247">This option can only be set by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**\_informazioni sul \_ socket di diagnostica dell'opzione Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**INTERNET\_OPTION\_DIAGNOSTIC\_SOCKET\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-249">67</span><span class="sxs-lookup"><span data-stu-id="c281b-249">67</span></span>
</dt> <dt>



<span data-ttu-id="c281b-250">Recupera una struttura di [**\_ informazioni del \_ socket \_ di diagnostica Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) che contiene i dati relativi a una richiesta HTTP specificata.</span><span class="sxs-lookup"><span data-stu-id="c281b-250">Retrieves an [**INTERNET\_DIAGNOSTIC\_SOCKET\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) structure that contains data about a specified HTTP Request.</span></span> <span data-ttu-id="c281b-251">Questo flag viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-251">This flag is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

<span data-ttu-id="c281b-252">**Windows 7:** Questa opzione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="c281b-252">**Windows 7:** This option is no longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**\_ \_ Scarica autenticazione del digest dell'opzione Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**INTERNET\_OPTION\_DIGEST\_AUTH\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-254">76</span><span class="sxs-lookup"><span data-stu-id="c281b-254">76</span></span>
</dt> <dt>



<span data-ttu-id="c281b-255">Causa la disconnessione del pacchetto SSPI di autenticazione del digest da parte del sistema, con l'eliminazione di tutte le credenziali create per il processo.</span><span class="sxs-lookup"><span data-stu-id="c281b-255">Causes the system to log off the Digest authentication SSPI package, purging all of the credentials created for the process.</span></span> <span data-ttu-id="c281b-256">Per questa opzione non è necessario alcun buffer.</span><span class="sxs-lookup"><span data-stu-id="c281b-256">No buffer is required for this option.</span></span> <span data-ttu-id="c281b-257">Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-257">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**\_opzione Internet \_ Disabilita \_ Autodial**</span><span class="sxs-lookup"><span data-stu-id="c281b-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**INTERNET\_OPTION\_DISABLE\_AUTODIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-259">70</span><span class="sxs-lookup"><span data-stu-id="c281b-259">70</span></span>
</dt> <dt>



<span data-ttu-id="c281b-260">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-260">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**opzione INTERNET- \_ \_ timeout disconnesso \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**INTERNET\_OPTION\_DISCONNECTED\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-262">49</span><span class="sxs-lookup"><span data-stu-id="c281b-262">49</span></span>
</dt> <dt>



<span data-ttu-id="c281b-263">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-263">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**\_opzione Internet \_ Abilita \_ \_ protocollo http**</span><span class="sxs-lookup"><span data-stu-id="c281b-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**INTERNET\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-265">148</span><span class="sxs-lookup"><span data-stu-id="c281b-265">148</span></span>
</dt> <dt>



<span data-ttu-id="c281b-266">Imposta una maschera di bit DWORD di versioni HTTP avanzate accettabili.</span><span class="sxs-lookup"><span data-stu-id="c281b-266">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="c281b-267">Può essere impostato su qualsiasi tipo di handle.</span><span class="sxs-lookup"><span data-stu-id="c281b-267">May be set on any handle type.</span></span> <span data-ttu-id="c281b-268">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="c281b-268">Possible values are:</span></span>

-   <span data-ttu-id="c281b-269">\_Flag di protocollo http \_ \_ HTTP2 (0x2).</span><span class="sxs-lookup"><span data-stu-id="c281b-269">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="c281b-270">Supportato in Windows 10, versione 1507 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-270">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="c281b-271">Non è possibile disabilitare le versioni legacy di HTTP (1,1 e precedenti) con questa opzione.</span><span class="sxs-lookup"><span data-stu-id="c281b-271">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="c281b-272">Il valore predefinito è 0x0.</span><span class="sxs-lookup"><span data-stu-id="c281b-272">The default is 0x0.</span></span> <span data-ttu-id="c281b-273">Supportato in Windows 10, versione 1507 e successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-273">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**\_opzione Internet \_ Abilita \_ la \_ lettura della cache di Reindirizzamento \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**INTERNET\_OPTION\_ENABLE\_REDIRECT\_CACHE\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-275">122</span><span class="sxs-lookup"><span data-stu-id="c281b-275">122</span></span>
</dt> <dt>



<span data-ttu-id="c281b-276">In un handle di richiesta, imposta un valore booleano che controlla se i reindirizzamenti verranno restituiti dalla cache WinInet per una determinata richiesta.</span><span class="sxs-lookup"><span data-stu-id="c281b-276">On a request handle, sets a Boolean controlling whether redirects will be returned from the WinInet cache for a given request.</span></span> <span data-ttu-id="c281b-277">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="c281b-277">The default is FALSE.</span></span> <span data-ttu-id="c281b-278">Supportato in Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-278">Supported in Windows 8 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**\_opzione Internet \_ Encode \_ extra**</span><span class="sxs-lookup"><span data-stu-id="c281b-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**INTERNET\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-280">155</span><span class="sxs-lookup"><span data-stu-id="c281b-280">155</span></span>
</dt> <dt>



<span data-ttu-id="c281b-281">Ottiene o imposta un valore BOOL che indica se i caratteri non ASCII nella stringa di query devono essere codificati in percentuale.</span><span class="sxs-lookup"><span data-stu-id="c281b-281">Gets/sets a BOOL indicating whether non-ASCII characters in the query string should be percent-encoded.</span></span> <span data-ttu-id="c281b-282">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="c281b-282">The default is FALSE.</span></span> <span data-ttu-id="c281b-283">Supportato in Windows 8.1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-283">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**\_opzione Internet \_ End \_ browser \_ Session**</span><span class="sxs-lookup"><span data-stu-id="c281b-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**INTERNET\_OPTION\_END\_BROWSER\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-285">42</span><span class="sxs-lookup"><span data-stu-id="c281b-285">42</span></span>
</dt> <dt>



<span data-ttu-id="c281b-286">Scarica le voci non utilizzate dalla cache delle password sull'unità disco rigido.</span><span class="sxs-lookup"><span data-stu-id="c281b-286">Flushes entries not in use from the password cache on the hard disk drive.</span></span> <span data-ttu-id="c281b-287">Reimposta inoltre il tempo di memorizzazione nella cache utilizzato quando la modalità di sincronizzazione è una volta per sessione.</span><span class="sxs-lookup"><span data-stu-id="c281b-287">Also resets the cache time used when the synchronization mode is once-per-session.</span></span> <span data-ttu-id="c281b-288">Per questa opzione non è necessario alcun buffer.</span><span class="sxs-lookup"><span data-stu-id="c281b-288">No buffer is required for this option.</span></span> <span data-ttu-id="c281b-289">Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-289">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**\_maschera di \_ errore \_ opzione Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**INTERNET\_OPTION\_ERROR\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-291">62</span><span class="sxs-lookup"><span data-stu-id="c281b-291">62</span></span>
</dt> <dt>



<span data-ttu-id="c281b-292">Imposta un valore long integer senza segno che contiene le maschere di errore che possono essere gestite dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="c281b-292">Sets an unsigned long integer value that contains the error masks that can be handled by the client application.</span></span> <span data-ttu-id="c281b-293">Può trattarsi di una combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c281b-293">This can be a combination of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c281b-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>\_maschera di errore Internet \_ \_ combinazione \_ sec \_ certificato</span><span class="sxs-lookup"><span data-stu-id="c281b-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>INTERNET\_ERROR\_MASK\_COMBINED\_SEC\_CERT</span></span>
</dt> <dd>

<span data-ttu-id="c281b-295">0x2</span><span class="sxs-lookup"><span data-stu-id="c281b-295">0x2</span></span>

<span data-ttu-id="c281b-296">Indica che tutti gli errori del certificato devono essere segnalati utilizzando la stessa restituzione dell'errore, ovvero errori del certificato di **\_ Internet \_ sec \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="c281b-296">Indicates that all certificate errors are to be reported using the same error return, namely **ERROR\_INTERNET\_SEC\_CERT\_ERRORS**.</span></span> <span data-ttu-id="c281b-297">Se questo flag è impostato, chiamare **InternetErrorDlg** al momento della ricezione dell'errore **errore \_ \_ \_ certificato \_ Internet sec** , in modo che l'utente possa rispondere a una finestra di dialogo familiare che descrive il problema.</span><span class="sxs-lookup"><span data-stu-id="c281b-297">If this flag is set, call **InternetErrorDlg** upon receiving the **ERROR\_INTERNET\_SEC\_CERT\_ERRORS** error, so that the user can respond to a familiar dialog describing the problem.</span></span>

> [!Caution]  
> <span data-ttu-id="c281b-298">La mancata notifica all'utente di questo errore espone l'utente a potenziali attacchi di spoofing.</span><span class="sxs-lookup"><span data-stu-id="c281b-298">Failing to inform the user of this error exposes the user to potential spoofing attacks.</span></span>

 

</dd> <dt>

<span data-ttu-id="c281b-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>maschera di errore INTERNET- \_ \_ \_ Inserisci \_ CDROM</span><span class="sxs-lookup"><span data-stu-id="c281b-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>INTERNET\_ERROR\_MASK\_INSERT\_CDROM</span></span>
</dt> <dd>

<span data-ttu-id="c281b-300">0x1</span><span class="sxs-lookup"><span data-stu-id="c281b-300">0x1</span></span>

<span data-ttu-id="c281b-301">Indica che l'applicazione client è in grado di gestire l' **errore \_ Internet \_ inserire \_** codice errore cdrom.</span><span class="sxs-lookup"><span data-stu-id="c281b-301">Indicates that the client application can handle the **ERROR\_INTERNET\_INSERT\_CDROM** error code.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>errore di accesso della maschera di errore di INTERNET \_ visualizzazione del \_ corpo dell' \_ \_ \_ \_ entità \_</span><span class="sxs-lookup"><span data-stu-id="c281b-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY</span></span>
</dt> <dd>

<span data-ttu-id="c281b-303">0x8</span><span class="sxs-lookup"><span data-stu-id="c281b-303">0x8</span></span>

<span data-ttu-id="c281b-304">Indica che l'applicazione client è in grado di gestire l' **errore di \_ accesso Internet errore Visualizza codice errore \_ \_ \_ \_ \_ corpo entità** .</span><span class="sxs-lookup"><span data-stu-id="c281b-304">Indicates that the client application can handle the **ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY** error code.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>la \_ maschera di errore Internet \_ necessita di \_ \_ MSN \_ SSPI \_ pkg</span><span class="sxs-lookup"><span data-stu-id="c281b-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>INTERNET\_ERROR\_MASK\_NEED\_MSN\_SSPI\_PKG</span></span>
</dt> <dd>

<span data-ttu-id="c281b-306">0x4</span><span class="sxs-lookup"><span data-stu-id="c281b-306">0x4</span></span>

<span data-ttu-id="c281b-307">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-307">Not implemented.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="c281b-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**\_opzione Internet \_ \_ contesto aziendale**</span><span class="sxs-lookup"><span data-stu-id="c281b-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**INTERNET\_OPTION\_ENTERPRISE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-309">159</span><span class="sxs-lookup"><span data-stu-id="c281b-309">159</span></span>
</dt> <dt>



<span data-ttu-id="c281b-310">Imposta un PWSTR contenente l'ID Enterprise (vedere https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) che si applica alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="c281b-310">Sets a PWSTR containing the Enterprise ID (see https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) which applies to the request.</span></span> <span data-ttu-id="c281b-311">Supportato in Windows 10, versione 1507 e successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-311">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**\_opzione Internet \_ - \_ errore esteso**</span><span class="sxs-lookup"><span data-stu-id="c281b-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**INTERNET\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-313">24</span><span class="sxs-lookup"><span data-stu-id="c281b-313">24</span></span>
</dt> <dt>



<span data-ttu-id="c281b-314">Recupera un valore long integer senza segno che contiene un codice di errore Winsock mappato ai messaggi di errore **\_ Internet \_** restituiti per ultimi in questo contesto di thread.</span><span class="sxs-lookup"><span data-stu-id="c281b-314">Retrieves an unsigned long integer value that contains a Winsock error code mapped to the **ERROR\_INTERNET\_** error messages last returned in this thread context.</span></span> <span data-ttu-id="c281b-315">Questa opzione viene usata in un handle [**HINTERNET**](appendix-a-hinternet-handles.md) **null** da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-315">This option is used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**\_opzione Internet \_ da \_ \_ timeout cache**</span><span class="sxs-lookup"><span data-stu-id="c281b-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**INTERNET\_OPTION\_FROM\_CACHE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-317">63</span><span class="sxs-lookup"><span data-stu-id="c281b-317">63</span></span>
</dt> <dt>



<span data-ttu-id="c281b-318">Imposta o Recupera il valore long integer senza segno A1n che contiene la quantità di tempo durante la quale il sistema deve attendere una risposta a una richiesta di rete prima di controllare la cache per una copia della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c281b-318">Sets or retrieves a1n unsigned long integer value that contains the amount of time the system should wait for a response to a network request before checking the cache for a copy of the resource.</span></span> <span data-ttu-id="c281b-319">Se una richiesta di rete richiede più tempo del tempo specificato e la risorsa richiesta è disponibile nella cache, la risorsa viene recuperata dalla cache.</span><span class="sxs-lookup"><span data-stu-id="c281b-319">If a network request takes longer than the time specified and the requested resource is available in the cache, the resource is retrieved from the cache.</span></span> <span data-ttu-id="c281b-320">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-320">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**\_tipo di \_ handle di opzione Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**INTERNET\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-322">9</span><span class="sxs-lookup"><span data-stu-id="c281b-322">9</span></span>
</dt> <dt>



<span data-ttu-id="c281b-323">Recupera un valore long integer senza segno che contiene il tipo di handle [**HINTERNET**](appendix-a-hinternet-handles.md) passati.</span><span class="sxs-lookup"><span data-stu-id="c281b-323">Retrieves an unsigned long integer value that contains the type of the [**HINTERNET**](appendix-a-hinternet-handles.md) handles passed in.</span></span> <span data-ttu-id="c281b-324">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) per qualsiasi handle [HINTERNET](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="c281b-324">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) on any [HINTERNET](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="c281b-325">Tra i possibili valori restituiti sono inclusi i seguenti.</span><span class="sxs-lookup"><span data-stu-id="c281b-325">Possible return values include the following.</span></span>

<dl> <dt>

<span data-ttu-id="c281b-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>\_tipo di handle Internet \_ \_ connessione \_ FTP</span><span class="sxs-lookup"><span data-stu-id="c281b-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_FTP</span></span>
</dt> <dd>

<span data-ttu-id="c281b-327">2</span><span class="sxs-lookup"><span data-stu-id="c281b-327">2</span></span>

</dd> <dt>

<span data-ttu-id="c281b-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>\_tipo di handle Internet \_ \_ Connetti \_ Gopher</span><span class="sxs-lookup"><span data-stu-id="c281b-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_GOPHER</span></span>
</dt> <dd>

<span data-ttu-id="c281b-329">3</span><span class="sxs-lookup"><span data-stu-id="c281b-329">3</span></span>

</dd> <dt>

<span data-ttu-id="c281b-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>\_tipo di handle Internet \_ \_ Connect \_ http</span><span class="sxs-lookup"><span data-stu-id="c281b-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="c281b-331">4</span><span class="sxs-lookup"><span data-stu-id="c281b-331">4</span></span>

</dd> <dt>

<span data-ttu-id="c281b-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>\_richiesta di \_ file di tipo handle \_ Internet \_</span><span class="sxs-lookup"><span data-stu-id="c281b-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>INTERNET\_HANDLE\_TYPE\_FILE\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="c281b-333">14</span><span class="sxs-lookup"><span data-stu-id="c281b-333">14</span></span>

</dd> <dt>

<span data-ttu-id="c281b-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>\_tipo di handle Internet \_ \_ \_ file FTP</span><span class="sxs-lookup"><span data-stu-id="c281b-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="c281b-335">7</span><span class="sxs-lookup"><span data-stu-id="c281b-335">7</span></span>

</dd> <dt>

<span data-ttu-id="c281b-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>\_tipo di handle Internet \_ \_ \_ HTML file FTP \_</span><span class="sxs-lookup"><span data-stu-id="c281b-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="c281b-337">8</span><span class="sxs-lookup"><span data-stu-id="c281b-337">8</span></span>

</dd> <dt>

<span data-ttu-id="c281b-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>tipo di handle INTERNET- \_ \_ \_ \_ ricerca FTP</span><span class="sxs-lookup"><span data-stu-id="c281b-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="c281b-339">5</span><span class="sxs-lookup"><span data-stu-id="c281b-339">5</span></span>

</dd> <dt>

<span data-ttu-id="c281b-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>\_tipo di handle Internet \_ \_ FTP \_ trova \_ HTML</span><span class="sxs-lookup"><span data-stu-id="c281b-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="c281b-341">6</span><span class="sxs-lookup"><span data-stu-id="c281b-341">6</span></span>

</dd> <dt>

<span data-ttu-id="c281b-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>\_ \_ file Gopher del tipo di handle Internet \_ \_</span><span class="sxs-lookup"><span data-stu-id="c281b-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="c281b-343">11</span><span class="sxs-lookup"><span data-stu-id="c281b-343">11</span></span>

</dd> <dt>

<span data-ttu-id="c281b-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>\_tipo di handle Internet \_ \_ \_ HTML file Gopher \_</span><span class="sxs-lookup"><span data-stu-id="c281b-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="c281b-345">12</span><span class="sxs-lookup"><span data-stu-id="c281b-345">12</span></span>

</dd> <dt>

<span data-ttu-id="c281b-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>tipo di handle INTERNET- \_ \_ \_ \_ trova Gopher</span><span class="sxs-lookup"><span data-stu-id="c281b-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="c281b-347">9</span><span class="sxs-lookup"><span data-stu-id="c281b-347">9</span></span>

</dd> <dt>

<span data-ttu-id="c281b-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>\_tipo di handle Internet \_ \_ Gopher \_ Find \_ HTML</span><span class="sxs-lookup"><span data-stu-id="c281b-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="c281b-349">10</span><span class="sxs-lookup"><span data-stu-id="c281b-349">10</span></span>

</dd> <dt>

<span data-ttu-id="c281b-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>\_ \_ richiesta HTTP di tipo handle \_ Internet \_</span><span class="sxs-lookup"><span data-stu-id="c281b-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>INTERNET\_HANDLE\_TYPE\_HTTP\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="c281b-351">13</span><span class="sxs-lookup"><span data-stu-id="c281b-351">13</span></span>

</dd> <dt>

<span data-ttu-id="c281b-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>\_tipo di handle Internet \_ \_ Internet</span><span class="sxs-lookup"><span data-stu-id="c281b-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>INTERNET\_HANDLE\_TYPE\_INTERNET</span></span>
</dt> <dd>

<span data-ttu-id="c281b-353">1</span><span class="sxs-lookup"><span data-stu-id="c281b-353">1</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="c281b-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**\_opzione Internet \_ HSTS**</span><span class="sxs-lookup"><span data-stu-id="c281b-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**INTERNET\_OPTION\_HSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-355">157</span><span class="sxs-lookup"><span data-stu-id="c281b-355">157</span></span>
</dt> <dt>



<span data-ttu-id="c281b-356">Ottiene o imposta un valore BOOL che indica se WinInet deve seguire le direttive HTTP Strict Transport Security (HSTS) dai server.</span><span class="sxs-lookup"><span data-stu-id="c281b-356">Gets/sets a BOOL indicating whether WinInet should follow HTTP Strict Transport Security (HSTS) directives from servers.</span></span> <span data-ttu-id="c281b-357">Se abilitate, le richieste con schema https://a domini che hanno un criterio HSTS memorizzato nella cache da WinInet verranno reindirizzate agli URL https://corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="c281b-357">If enabled, https:// schemed requests to domains which have an HSTS policy cached by WinInet will be redirected to matching https:// URLs.</span></span> <span data-ttu-id="c281b-358">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="c281b-358">The default is FALSE.</span></span> <span data-ttu-id="c281b-359">Supportato in Windows 8.1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-359">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**\_opzione Internet \_ \_ decodifica http**</span><span class="sxs-lookup"><span data-stu-id="c281b-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**INTERNET\_OPTION\_HTTP\_DECODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-361">65</span><span class="sxs-lookup"><span data-stu-id="c281b-361">65</span></span>
</dt> <dt>



<span data-ttu-id="c281b-362">Consente a WinINet di eseguire la decodifica per gli schemi di codifica gzip e Deflate.</span><span class="sxs-lookup"><span data-stu-id="c281b-362">Enables WinINet to perform decoding for the gzip and deflate encoding schemes.</span></span> <span data-ttu-id="c281b-363">Per ulteriori informazioni, vedere [**codifica del contenuto**](content-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="c281b-363">For more information, see [**Content Encoding**](content-encoding.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**\_ \_ protocollo http opzione \_ Internet \_ usato**</span><span class="sxs-lookup"><span data-stu-id="c281b-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**INTERNET\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-365">149</span><span class="sxs-lookup"><span data-stu-id="c281b-365">149</span></span>
</dt> <dt>



<span data-ttu-id="c281b-366">Ottiene un valore DWORD che indica quale versione HTTP avanzata è stata utilizzata per una determinata richiesta.</span><span class="sxs-lookup"><span data-stu-id="c281b-366">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="c281b-367">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="c281b-367">Possible values are:</span></span>

-   <span data-ttu-id="c281b-368">\_Flag di protocollo http \_ \_ HTTP2 (0x2).</span><span class="sxs-lookup"><span data-stu-id="c281b-368">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="c281b-369">Supportato in Windows 10, versione 1507 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-369">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="c281b-370">0x0 indica HTTP/1.1 o versione precedente; vedere l' \_ opzione \_ Internet \_ versione http se è necessaria una maggiore precisione su quale versione legacy è stata usata.</span><span class="sxs-lookup"><span data-stu-id="c281b-370">0x0 indicates HTTP/1.1 or earlier; see INTERNET\_OPTION\_HTTP\_VERSION if more precision is needed about which legacy version was used.</span></span> <span data-ttu-id="c281b-371">Supportato in Windows 10, versione 1507 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-371">Supported on Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**\_opzione Internet \_ \_ versione http**</span><span class="sxs-lookup"><span data-stu-id="c281b-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**INTERNET\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-373">59</span><span class="sxs-lookup"><span data-stu-id="c281b-373">59</span></span>
</dt> <dt>



<span data-ttu-id="c281b-374">Imposta o Recupera una struttura di [**\_ \_ informazioni sulla versione http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) che contiene la versione http supportata.</span><span class="sxs-lookup"><span data-stu-id="c281b-374">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure that contains the supported HTTP version.</span></span> <span data-ttu-id="c281b-375">Questa operazione deve essere utilizzata su un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="c281b-375">This must be used on a **NULL** handle.</span></span> <span data-ttu-id="c281b-376">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-376">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="c281b-377">In Windows 7, Windows Server 2008 R2 e versioni successive, il valore del membro **dwMinorVersion** nella struttura delle [**\_ \_ informazioni sulla versione http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) viene sostituito dalle impostazioni di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c281b-377">On Windows 7, Windows Server 2008 R2, and later, the value of the **dwMinorVersion** member in the [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure is overridden by Internet Explorer settings.</span></span> <span data-ttu-id="c281b-378">**EnableHttp1 \_ 1** è un valore del registro di sistema in **HKLM \\ software \\ Microsoft \\ InternetExplorer \\ AdvacnedOptions \\ http \\ GENABLE** controllato dalle opzioni Internet impostate in Internet Explorer per il sistema.</span><span class="sxs-lookup"><span data-stu-id="c281b-378">**EnableHttp1\_1** is a registry value under **HKLM\\Software\\Microsoft\\InternetExplorer\\AdvacnedOptions\\HTTP\\GENABLE** controlled by Internet Options set in Internet Explorer for the system.</span></span> <span data-ttu-id="c281b-379">Il valore predefinito di **EnableHttp1 \_ 1** è 1.</span><span class="sxs-lookup"><span data-stu-id="c281b-379">The **EnableHttp1\_1** value defaults to 1.</span></span> <span data-ttu-id="c281b-380">La struttura delle **\_ \_ informazioni sulla versione http** viene ignorata per qualsiasi versione http inferiore a 1,1 se **EnableHttp1 \_ 1** è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="c281b-380">The **HTTP\_VERSION\_INFO** structure is ignored for any HTTP version less than 1.1 if **EnableHttp1\_1** is set to 1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**\_identità opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**INTERNET\_OPTION\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-382">78</span><span class="sxs-lookup"><span data-stu-id="c281b-382">78</span></span>
</dt> <dt>



<span data-ttu-id="c281b-383">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-383">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**opzione INTERNET- \_ \_ stato di inattività \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**INTERNET\_OPTION\_IDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-385">51</span><span class="sxs-lookup"><span data-stu-id="c281b-385">51</span></span>
</dt> <dt>



<span data-ttu-id="c281b-386">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-386">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**\_opzione Internet \_ IDN**</span><span class="sxs-lookup"><span data-stu-id="c281b-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**INTERNET\_OPTION\_IDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-388">102</span><span class="sxs-lookup"><span data-stu-id="c281b-388">102</span></span>
</dt> <dt>



<span data-ttu-id="c281b-389">Per impostazione predefinita, la parte relativa all'host o all'autorità dell'URL è codificata in base alla specifica IDN per le connessioni dirette e proxy.</span><span class="sxs-lookup"><span data-stu-id="c281b-389">By default, the host or authority portion of the URL is encoded according to the IDN specification for both direct and proxy connections.</span></span> <span data-ttu-id="c281b-390">Questa opzione può essere utilizzata nella richiesta o nell'handle di connessione per abilitare o disabilitare IDN.</span><span class="sxs-lookup"><span data-stu-id="c281b-390">This option can be used on the request, or connection handle to enable or disable IDN.</span></span> <span data-ttu-id="c281b-391">Quando IDN è disabilitato, WinINet usa la tabella codici di sistema per codificare la porzione host o Authority dell'URL.</span><span class="sxs-lookup"><span data-stu-id="c281b-391">When IDN is disabled, WinINet uses the system codepage to encode the host or authority portion of the URL.</span></span> <span data-ttu-id="c281b-392">Per disabilitare la conversione dell'host IDN, impostare il parametro *lpBuffer* nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) su zero.</span><span class="sxs-lookup"><span data-stu-id="c281b-392">To disable IDN host conversion, set the *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to zero.</span></span> <span data-ttu-id="c281b-393">Per abilitare la conversione IDN solo sulla connessione diretta, specificare **il \_ flag Internet \_ IDN \_ Direct** nel parametro *lpBuffer* nella chiamata a **InternetSetOption**.</span><span class="sxs-lookup"><span data-stu-id="c281b-393">To enable IDN conversion on only the direct connection, specify **INTERNET\_FLAG\_IDN\_DIRECT** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span> <span data-ttu-id="c281b-394">Per abilitare la conversione IDN solo sulla connessione proxy, specificare **il \_ \_ \_ proxy IDN del flag Internet** nel parametro *lpBuffer* nella chiamata a **InternetSetOption**.</span><span class="sxs-lookup"><span data-stu-id="c281b-394">To enable IDN conversion on only the proxy connection, specify **INTERNET\_FLAG\_IDN\_PROXY** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span>

<span data-ttu-id="c281b-395">**Windows XP con SP2 e Windows Server 2003 con SP1:** Questo flag non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c281b-395">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="c281b-396">**Versione:** Richiede Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="c281b-396">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**\_opzione Internet \_ Ignore \_ offline**</span><span class="sxs-lookup"><span data-stu-id="c281b-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**INTERNET\_OPTION\_IGNORE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-398">77</span><span class="sxs-lookup"><span data-stu-id="c281b-398">77</span></span>
</dt> <dt>



<span data-ttu-id="c281b-399">Imposta o recupera un valore che indica se il flag globale offline deve essere ignorato per l'handle di richiesta specificato.</span><span class="sxs-lookup"><span data-stu-id="c281b-399">Sets or retrieves whether the global offline flag should be ignored for the specified request handle.</span></span> <span data-ttu-id="c281b-400">Per questa opzione non è necessario alcun buffer.</span><span class="sxs-lookup"><span data-stu-id="c281b-400">No buffer is required for this option.</span></span> <span data-ttu-id="c281b-401">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con un handle di richiesta.</span><span class="sxs-lookup"><span data-stu-id="c281b-401">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with a request handle.</span></span> <span data-ttu-id="c281b-402">Questa opzione è valida solo in Internet Explorer 5 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-402">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**\_opzione Internet \_ Mantieni \_ connessione**</span><span class="sxs-lookup"><span data-stu-id="c281b-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**INTERNET\_OPTION\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-404">22</span><span class="sxs-lookup"><span data-stu-id="c281b-404">22</span></span>
</dt> <dt>



<span data-ttu-id="c281b-405">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-405">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**\_ \_ timeout ascolto opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**INTERNET\_OPTION\_LISTEN\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-407">11</span><span class="sxs-lookup"><span data-stu-id="c281b-407">11</span></span>
</dt> <dt>



<span data-ttu-id="c281b-408">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-408">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**\_Opzione Internet \_ Max \_ Conns \_ per \_ 1 \_ 0 \_ Server**</span><span class="sxs-lookup"><span data-stu-id="c281b-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-410">74</span><span class="sxs-lookup"><span data-stu-id="c281b-410">74</span></span>
</dt> <dt>



<span data-ttu-id="c281b-411">Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="c281b-411">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="c281b-412">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-412">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-413">Questa opzione è valida solo in Internet Explorer 5 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-413">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**\_opzione Internet \_ Max \_ connes \_ per \_ proxy**</span><span class="sxs-lookup"><span data-stu-id="c281b-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-415">103</span><span class="sxs-lookup"><span data-stu-id="c281b-415">103</span></span>
</dt> <dt>



<span data-ttu-id="c281b-416">Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni proxy CERN.</span><span class="sxs-lookup"><span data-stu-id="c281b-416">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per CERN proxy.</span></span> <span data-ttu-id="c281b-417">Quando questa opzione è impostata o recuperata, il parametro *HINTERNET* deve essere impostato su un valore di handle **null** .</span><span class="sxs-lookup"><span data-stu-id="c281b-417">When this option is set or retrieved, the *hInternet* parameter must set to a **null** handle value.</span></span> <span data-ttu-id="c281b-418">Un valore di handle **null** indica che l'opzione deve essere impostata o sottoposta a query per il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="c281b-418">A **null** handle value indicates that the option should be set or queried for the current process.</span></span> <span data-ttu-id="c281b-419">Quando si chiama [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con questa opzione, tutti gli oggetti proxy esistenti riceveranno il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="c281b-419">When calling [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with this option, all existing proxy objects will receive the new value.</span></span> <span data-ttu-id="c281b-420">Questo valore è limitato a un intervallo compreso tra 2 e 128, inclusi.</span><span class="sxs-lookup"><span data-stu-id="c281b-420">This value is limited to a range of 2 to 128, inclusive.</span></span>

<span data-ttu-id="c281b-421">**Versione:** Richiede Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="c281b-421">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**\_opzione Internet \_ Max \_ connes \_ per \_ Server**</span><span class="sxs-lookup"><span data-stu-id="c281b-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-423">73</span><span class="sxs-lookup"><span data-stu-id="c281b-423">73</span></span>
</dt> <dt>



<span data-ttu-id="c281b-424">Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per server.</span><span class="sxs-lookup"><span data-stu-id="c281b-424">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="c281b-425">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-425">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-426">Questa opzione è valida solo in Internet Explorer 5 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-426">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**\_opzione Internet \_ \_ modalità offline**</span><span class="sxs-lookup"><span data-stu-id="c281b-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**INTERNET\_OPTION\_OFFLINE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-428">26</span><span class="sxs-lookup"><span data-stu-id="c281b-428">26</span></span>
</dt> <dt>



<span data-ttu-id="c281b-429">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-429">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**\_ \_ semantica offline opzione Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**INTERNET\_OPTION\_OFFLINE\_SEMANTICS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-431">52</span><span class="sxs-lookup"><span data-stu-id="c281b-431">52</span></span>
</dt> <dt>



<span data-ttu-id="c281b-432">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-432">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**\_opzione Internet \_ scegliere \_ la \_ \_ firma debole**</span><span class="sxs-lookup"><span data-stu-id="c281b-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**INTERNET\_OPTION\_OPT\_IN\_WEAK\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-434">176</span><span class="sxs-lookup"><span data-stu-id="c281b-434">176</span></span>
</dt> <dt>



<span data-ttu-id="c281b-435">Acconsentire esplicitamente alle firme deboli (ad esempio, SHA-1) per essere considerate non sicure.</span><span class="sxs-lookup"><span data-stu-id="c281b-435">Opt-in for weak signatures (e.g. SHA-1) to be treated as insecure.</span></span> <span data-ttu-id="c281b-436">In questo modo, WinInet chiamerà [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) utilizzando il **parametro \_ \_ \_ di \_ \_ firma esplicito della catena di certificati** .</span><span class="sxs-lookup"><span data-stu-id="c281b-436">This will instruct WinInet to call [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) using the **CERT\_CHAIN\_OPT\_IN\_WEAK\_SIGNATURE** parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**\_ \_ handle padre opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**INTERNET\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-438">21</span><span class="sxs-lookup"><span data-stu-id="c281b-438">21</span></span>
</dt> <dt>



<span data-ttu-id="c281b-439">Recupera l'handle padre per questo handle.</span><span class="sxs-lookup"><span data-stu-id="c281b-439">Retrieves the parent handle to this handle.</span></span> <span data-ttu-id="c281b-440">Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-440">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**\_password opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**INTERNET\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-442">29</span><span class="sxs-lookup"><span data-stu-id="c281b-442">29</span></span>
</dt> <dt>



<span data-ttu-id="c281b-443">Imposta o recupera un valore stringa che contiene la password associata a un handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c281b-443">Sets or retrieves a string value that contains the password associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="c281b-444">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-444">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**opzione \_ Internet \_ per \_ ogni \_ opzione di connessione**</span><span class="sxs-lookup"><span data-stu-id="c281b-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-446">75</span><span class="sxs-lookup"><span data-stu-id="c281b-446">75</span></span>
</dt> <dt>



<span data-ttu-id="c281b-447">Imposta o Recupera una struttura [**Internet \_ per ogni \_ \_ \_ elenco**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) di opzioni conn che specifica un elenco di opzioni per una determinata connessione.</span><span class="sxs-lookup"><span data-stu-id="c281b-447">Sets or retrieves an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure that specifies a list of options for a particular connection.</span></span> <span data-ttu-id="c281b-448">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-448">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-449">Questa opzione è valida solo in Internet Explorer 5 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c281b-449">This option is only valid in Internet Explorer 5 and later.</span></span>

> [!Note]  
> <span data-ttu-id="c281b-450">**Internet \_ L' \_ opzione \_ per \_ connessione** consente di modificare le impostazioni a livello di sistema quando si utilizza un handle **null** nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-450">**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION** causes the settings to be changed on a system-wide basis when a **NULL** handle is used in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-451">Per aggiornare le impostazioni del proxy globale, è necessario chiamare **InternetSetOption** con il flag dell'opzione di **\_ \_ aggiornamento Internet Option** .</span><span class="sxs-lookup"><span data-stu-id="c281b-451">To refresh the global proxy settings, you must call **InternetSetOption** with the **INTERNET\_OPTION\_REFRESH** option flag.</span></span>

 

> [!Note]  
> <span data-ttu-id="c281b-452">Per modificare le informazioni sul proxy per l'intero processo senza influire sulle impostazioni globali in Internet Explorer 5 e versioni successive, usare questa opzione nell'handle restituito da [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="c281b-452">To change proxy information for the entire process without affecting the global settings in Internet Explorer 5 and later, use this option on the handle that is returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="c281b-453">Nell'esempio di codice seguente viene modificato il proxy per l'intero processo anche se l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) è chiuso e non viene utilizzato da alcuna richiesta.</span><span class="sxs-lookup"><span data-stu-id="c281b-453">The following code example changes the proxy for the whole process even though the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is closed and is not used by any requests.</span></span>

 

<span data-ttu-id="c281b-454">Per ulteriori informazioni ed esempi di codice, vedere l' [articolo della Knowledge base 226473](https://support.microsoft.com/kb/226473).</span><span class="sxs-lookup"><span data-stu-id="c281b-454">For more information and code examples, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**\_criteri opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**INTERNET\_OPTION\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-456">48</span><span class="sxs-lookup"><span data-stu-id="c281b-456">48</span></span>
</dt> <dt>



<span data-ttu-id="c281b-457">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-457">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**\_proxy opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**INTERNET\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-459">38</span><span class="sxs-lookup"><span data-stu-id="c281b-459">38</span></span>
</dt> <dt>



<span data-ttu-id="c281b-460">Imposta o Recupera una struttura di [**\_ \_ informazioni sul proxy Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) che contiene i dati del proxy per un handle [**internetopt**](/windows/desktop/api/Wininet/nf-wininet-internetopena) esistente quando l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) non è **null**.</span><span class="sxs-lookup"><span data-stu-id="c281b-460">Sets or retrieves an [**INTERNET\_PROXY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) structure that contains the proxy data for an existing [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) handle when the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is not **NULL**.</span></span> <span data-ttu-id="c281b-461">Se l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) è **null**, la funzione imposta o esegue una query sui dati proxy globali.</span><span class="sxs-lookup"><span data-stu-id="c281b-461">If the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is **NULL**, the function sets or queries the global proxy data.</span></span> <span data-ttu-id="c281b-462">Questa opzione può essere usata sull'handle restituito da **InternetOpen**.</span><span class="sxs-lookup"><span data-stu-id="c281b-462">This option can be used on the handle returned by **InternetOpen**.</span></span> <span data-ttu-id="c281b-463">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-463">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

> [!Note]  
> <span data-ttu-id="c281b-464">È consigliabile usare l'opzione \_ opzione Internet \_ per \_ connessione anziché il \_ \_ proxy di opzione Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="c281b-464">It is recommended that INTERNET\_OPTION\_PER\_CONNECTION\_OPTION be used instead of INTERNET\_OPTION\_PROXY.</span></span> <span data-ttu-id="c281b-465">Per ulteriori informazioni, vedere l' [articolo KB 226473](https://support.microsoft.com/kb/226473).</span><span class="sxs-lookup"><span data-stu-id="c281b-465">For more information, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**\_ \_ password proxy opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**INTERNET\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-467">44</span><span class="sxs-lookup"><span data-stu-id="c281b-467">44</span></span>
</dt> <dt>



<span data-ttu-id="c281b-468">Imposta o recupera un valore stringa che contiene la password utilizzata per accedere al proxy.</span><span class="sxs-lookup"><span data-stu-id="c281b-468">Sets or retrieves a string value that contains the password used to access the proxy.</span></span> <span data-ttu-id="c281b-469">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-469">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-470">Questa opzione può essere impostata sull'handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="c281b-470">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**\_ \_ impostazioni proxy opzioni \_ Internet \_ modificate**</span><span class="sxs-lookup"><span data-stu-id="c281b-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**INTERNET\_OPTION\_PROXY\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-472">95</span><span class="sxs-lookup"><span data-stu-id="c281b-472">95</span></span> 
</dt> <dt>



<span data-ttu-id="c281b-473">Avvisa l'istanza di WinInet corrente che le impostazioni proxy sono state modificate e che devono essere aggiornate con le nuove impostazioni.</span><span class="sxs-lookup"><span data-stu-id="c281b-473">Alerts the current WinInet instance that proxy settings have changed and that they must update with the new settings.</span></span> <span data-ttu-id="c281b-474">Per avvisare tutte le istanze di WinInet disponibili, impostare il parametro *buffer* di [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) su **null** e *bufferLength* su 0 quando si passa questa opzione.</span><span class="sxs-lookup"><span data-stu-id="c281b-474">To alert all available WinInet instances, set the *Buffer* parameter of [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to **NULL** and *BufferLength* to 0 when passing this option.</span></span> <span data-ttu-id="c281b-475">Questa opzione può essere impostata sull'handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="c281b-475">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**\_ \_ nome utente proxy opzione Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**INTERNET\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-477">43</span><span class="sxs-lookup"><span data-stu-id="c281b-477">43</span></span>
</dt> <dt>



<span data-ttu-id="c281b-478">Imposta o recupera un valore stringa che contiene il nome utente utilizzato per accedere al proxy.</span><span class="sxs-lookup"><span data-stu-id="c281b-478">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span> <span data-ttu-id="c281b-479">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-479">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-480">Questa opzione può essere impostata sull'handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="c281b-480">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**\_dimensioni del \_ buffer di lettura opzione \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**INTERNET\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-482">12</span><span class="sxs-lookup"><span data-stu-id="c281b-482">12</span></span>
</dt> <dt>



<span data-ttu-id="c281b-483">Imposta o recupera un valore long integer senza segno che contiene la dimensione del buffer di lettura.</span><span class="sxs-lookup"><span data-stu-id="c281b-483">Sets or retrieves an unsigned long integer value that contains the size of the read buffer.</span></span> <span data-ttu-id="c281b-484">Questa opzione può essere utilizzata per gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituiti da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)e [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (solo sessione FTP).</span><span class="sxs-lookup"><span data-stu-id="c281b-484">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="c281b-485">Questa opzione viene usata da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-485">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**\_ \_ velocità effettiva ricezione opzione Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**INTERNET\_OPTION\_RECEIVE\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-487">57</span><span class="sxs-lookup"><span data-stu-id="c281b-487">57</span></span>
</dt> <dt>



<span data-ttu-id="c281b-488">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-488">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**\_timeout di \_ ricezione \_ opzione Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**INTERNET\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-490">6</span><span class="sxs-lookup"><span data-stu-id="c281b-490">6</span></span>
</dt> <dt>



<span data-ttu-id="c281b-491">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per ricevere una risposta a una richiesta.</span><span class="sxs-lookup"><span data-stu-id="c281b-491">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request.</span></span> <span data-ttu-id="c281b-492">Se la risposta richiede più tempo rispetto a questo valore di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="c281b-492">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="c281b-493">Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="c281b-493">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="c281b-494">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-494">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="c281b-495">Questa opzione non è destinata a rappresentare un timeout immediato e con granularità fine.</span><span class="sxs-lookup"><span data-stu-id="c281b-495">This option is not intended to represent a fine-grained, immediate timeout.</span></span> <span data-ttu-id="c281b-496">È possibile prevedere che il timeout venga eseguito fino a sei secondi dopo il valore di timeout set.</span><span class="sxs-lookup"><span data-stu-id="c281b-496">You can expect the timeout to occur up to six seconds after the set timeout value.</span></span>

<span data-ttu-id="c281b-497">Se utilizzata in riferimento a una transazione FTP, questa opzione si riferisce al canale di controllo.</span><span class="sxs-lookup"><span data-stu-id="c281b-497">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**\_aggiornamento opzioni \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**INTERNET\_OPTION\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-499">37</span><span class="sxs-lookup"><span data-stu-id="c281b-499">37</span></span>
</dt> <dt>



<span data-ttu-id="c281b-500">Consente di rileggere i dati del proxy dal registro di sistema per un handle.</span><span class="sxs-lookup"><span data-stu-id="c281b-500">Causes the proxy data to be reread from the registry for a handle.</span></span> <span data-ttu-id="c281b-501">Non è necessario alcun buffer.</span><span class="sxs-lookup"><span data-stu-id="c281b-501">No buffer is required.</span></span> <span data-ttu-id="c281b-502">Questa opzione può essere usata nell'handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituito da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="c281b-502">This option can be used on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="c281b-503">Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-503">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**\_opzione Internet \_ Rimuovi \_ identità**</span><span class="sxs-lookup"><span data-stu-id="c281b-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**INTERNET\_OPTION\_REMOVE\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-505">79</span><span class="sxs-lookup"><span data-stu-id="c281b-505">79</span></span>
</dt> <dt>



<span data-ttu-id="c281b-506">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-506">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**\_flag di \_ richiesta di opzione Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**INTERNET\_OPTION\_REQUEST\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-508">23</span><span class="sxs-lookup"><span data-stu-id="c281b-508">23</span></span>
</dt> <dt>



<span data-ttu-id="c281b-509">Recupera un valore long integer senza segno che contiene i flag di stato speciali che indicano lo stato del download in corso.</span><span class="sxs-lookup"><span data-stu-id="c281b-509">Retrieves an unsigned long integer value that contains the special status flags that indicate the status of the download in progress.</span></span> <span data-ttu-id="c281b-510">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-510">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="c281b-511">L' [opzione \_ Internet \_ Request \_ Flags](/windows) può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c281b-511">The [INTERNET\_OPTION\_REQUEST\_FLAGS](/windows) option can be one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c281b-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET \_ REQFLAG \_ Async</span><span class="sxs-lookup"><span data-stu-id="c281b-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET\_REQFLAG\_ASYNC</span></span>
</dt> <dd>

<span data-ttu-id="c281b-513">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c281b-513">0x00000002</span></span>

<span data-ttu-id="c281b-514">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-514">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>\_ \_ scrittura cache REQFLAG \_ Internet \_ disabilitata</span><span class="sxs-lookup"><span data-stu-id="c281b-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>INTERNET\_REQFLAG\_CACHE\_WRITE\_DISABLED</span></span>
</dt> <dd>

<span data-ttu-id="c281b-516">0x00000040</span><span class="sxs-lookup"><span data-stu-id="c281b-516">0x00000040</span></span>

<span data-ttu-id="c281b-517">La richiesta Internet non può essere memorizzata nella cache (ad esempio, una richiesta HTTPS).</span><span class="sxs-lookup"><span data-stu-id="c281b-517">Internet request cannot be cached (an HTTPS request, for example).</span></span>

</dd> <dt>

<span data-ttu-id="c281b-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET \_ REQFLAG \_ dalla \_ cache</span><span class="sxs-lookup"><span data-stu-id="c281b-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET\_REQFLAG\_FROM\_CACHE</span></span>
</dt> <dd>

<span data-ttu-id="c281b-519">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c281b-519">0x00000001</span></span>

<span data-ttu-id="c281b-520">La risposta proviene dalla cache.</span><span class="sxs-lookup"><span data-stu-id="c281b-520">Response came from the cache.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>\_ \_ timeout rete REQFLAG \_ Internet</span><span class="sxs-lookup"><span data-stu-id="c281b-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>INTERNET\_REQFLAG\_NET\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="c281b-522">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c281b-522">0x00000080</span></span>

<span data-ttu-id="c281b-523">Timeout della richiesta Internet.</span><span class="sxs-lookup"><span data-stu-id="c281b-523">Internet request timed out.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET \_ REQFLAG \_ senza \_ intestazioni</span><span class="sxs-lookup"><span data-stu-id="c281b-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET\_REQFLAG\_NO\_HEADERS</span></span>
</dt> <dd>

<span data-ttu-id="c281b-525">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c281b-525">0x00000008</span></span>

<span data-ttu-id="c281b-526">La risposta originale non conteneva intestazioni.</span><span class="sxs-lookup"><span data-stu-id="c281b-526">Original response contained no headers.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET \_ REQFLAG \_ passivo</span><span class="sxs-lookup"><span data-stu-id="c281b-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET\_REQFLAG\_PASSIVE</span></span>
</dt> <dd>

<span data-ttu-id="c281b-528">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c281b-528">0x00000010</span></span>

<span data-ttu-id="c281b-529">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-529">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET \_ REQFLAG \_ tramite \_ proxy</span><span class="sxs-lookup"><span data-stu-id="c281b-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET\_REQFLAG\_VIA\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="c281b-531">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c281b-531">0x00000004</span></span>

<span data-ttu-id="c281b-532">La richiesta è stata effettuata tramite un proxy.</span><span class="sxs-lookup"><span data-stu-id="c281b-532">Request was made through a proxy.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="c281b-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**\_ \_ priorità richiesta opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**INTERNET\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-534">58</span><span class="sxs-lookup"><span data-stu-id="c281b-534">58</span></span>
</dt> <dt>



<span data-ttu-id="c281b-535">Imposta o recupera un valore long integer senza segno che contiene la priorità delle richieste che competono per una connessione su un handle HTTP.</span><span class="sxs-lookup"><span data-stu-id="c281b-535">Sets or retrieves an unsigned long integer value that contains the priority of requests that compete for a connection on an HTTP handle.</span></span> <span data-ttu-id="c281b-536">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-536">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**\_opzione Internet \_ Reimposta \_ \_ sessione Urlcache**</span><span class="sxs-lookup"><span data-stu-id="c281b-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**INTERNET\_OPTION\_RESET\_URLCACHE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-538">60</span><span class="sxs-lookup"><span data-stu-id="c281b-538">60</span></span>
</dt> <dt>



<span data-ttu-id="c281b-539">Avvia una nuova sessione della cache per il processo.</span><span class="sxs-lookup"><span data-stu-id="c281b-539">Starts a new cache session for the process.</span></span> <span data-ttu-id="c281b-540">Non è necessario alcun buffer.</span><span class="sxs-lookup"><span data-stu-id="c281b-540">No buffer is required.</span></span> <span data-ttu-id="c281b-541">Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-541">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-542">Questa opzione è riservata solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="c281b-542">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**\_opzione Internet \_ \_ chiave di cache secondaria \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**INTERNET\_OPTION\_SECONDARY\_CACHE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-544">53</span><span class="sxs-lookup"><span data-stu-id="c281b-544">53</span></span>
</dt> <dt>



<span data-ttu-id="c281b-545">Imposta o recupera un valore stringa che contiene la chiave di cache secondaria.</span><span class="sxs-lookup"><span data-stu-id="c281b-545">Sets or retrieves a string value that contains the secondary cache key.</span></span> <span data-ttu-id="c281b-546">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-546">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="c281b-547">Questa opzione è riservata solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="c281b-547">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**\_certificato di \_ sicurezza delle opzioni Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-549">35</span><span class="sxs-lookup"><span data-stu-id="c281b-549">35</span></span>
</dt> <dt>



<span data-ttu-id="c281b-550">Recupera il certificato per un server SSL/PCT (Secure Sockets Layer/tecnologia di comunicazione privata) in una stringa formattata.</span><span class="sxs-lookup"><span data-stu-id="c281b-550">Retrieves the certificate for an SSL/PCT (Secure Sockets Layer/Private Communications Technology) server into a formatted string.</span></span> <span data-ttu-id="c281b-551">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-551">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**\_ \_ struct certificato di sicurezza opzione \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-553">32</span><span class="sxs-lookup"><span data-stu-id="c281b-553">32</span></span>
</dt> <dt>



<span data-ttu-id="c281b-554">Recupera il certificato per un server SSL/PCT nella struttura delle \_ informazioni del certificato Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="c281b-554">Retrieves the certificate for an SSL/PCT server into the INTERNET\_CERTIFICATE\_INFO structure.</span></span> <span data-ttu-id="c281b-555">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-555">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**\_flag di \_ sicurezza delle opzioni Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**INTERNET\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-557">31</span><span class="sxs-lookup"><span data-stu-id="c281b-557">31</span></span>
</dt> <dt>



<span data-ttu-id="c281b-558">Recupera un valore long integer senza segno che contiene i flag di sicurezza per un handle.</span><span class="sxs-lookup"><span data-stu-id="c281b-558">Retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="c281b-559">Questa opzione viene utilizzata da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-559">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="c281b-560">Può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c281b-560">It can be a combination of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c281b-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>FLAG di sicurezza \_ \_ 128bit</span><span class="sxs-lookup"><span data-stu-id="c281b-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>SECURITY\_FLAG\_128BIT</span></span>
</dt> <dd>

<span data-ttu-id="c281b-562">0x20000000</span><span class="sxs-lookup"><span data-stu-id="c281b-562">0x20000000</span></span>

<span data-ttu-id="c281b-563">Identico al flag di sicurezza del valore preferito [ \_ \_ \_ Strong](/windows).</span><span class="sxs-lookup"><span data-stu-id="c281b-563">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_STRONG](/windows).</span></span> <span data-ttu-id="c281b-564">Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-564">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="c281b-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>FLAG di sicurezza \_ \_ 40BIT</span><span class="sxs-lookup"><span data-stu-id="c281b-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>SECURITY\_FLAG\_40BIT</span></span>
</dt> <dd>

<span data-ttu-id="c281b-566">0x10000000</span><span class="sxs-lookup"><span data-stu-id="c281b-566">0x10000000</span></span>

<span data-ttu-id="c281b-567">Identico al flag di sicurezza del valore preferito [ \_ \_ \_ debole](/windows).</span><span class="sxs-lookup"><span data-stu-id="c281b-567">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="c281b-568">Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-568">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="c281b-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>FLAG di sicurezza \_ \_ 56BIT</span><span class="sxs-lookup"><span data-stu-id="c281b-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>SECURITY\_FLAG\_56BIT</span></span>
</dt> <dd>

<span data-ttu-id="c281b-570">0x40000000</span><span class="sxs-lookup"><span data-stu-id="c281b-570">0x40000000</span></span>

<span data-ttu-id="c281b-571">Identico al flag di sicurezza del valore preferito [ \_ \_ \_ medio](/windows).</span><span class="sxs-lookup"><span data-stu-id="c281b-571">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_MEDIUM](/windows).</span></span> <span data-ttu-id="c281b-572">Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-572">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="c281b-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>FLAG di sicurezza \_ \_ fortezza</span><span class="sxs-lookup"><span data-stu-id="c281b-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>SECURITY\_FLAG\_FORTEZZA</span></span>
</dt> <dd>

<span data-ttu-id="c281b-574">0x08000000</span><span class="sxs-lookup"><span data-stu-id="c281b-574">0x08000000</span></span>

<span data-ttu-id="c281b-575">Indica che la fortezza è stata utilizzata per fornire riservatezza, autenticazione e/o integrità per la connessione specificata.</span><span class="sxs-lookup"><span data-stu-id="c281b-575">Indicates Fortezza has been used to provide secrecy, authentication, and/or integrity for the specified connection.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>FLAG di sicurezza \_ \_ IETFSSL4</span><span class="sxs-lookup"><span data-stu-id="c281b-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>SECURITY\_FLAG\_IETFSSL4</span></span>
</dt> <dd>

<span data-ttu-id="c281b-577">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c281b-577">0x00000020</span></span>

<span data-ttu-id="c281b-578">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-578">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>FLAG di sicurezza \_ \_ Ignora \_ certificato \_ CN \_ non valido</span><span class="sxs-lookup"><span data-stu-id="c281b-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="c281b-580">0x00001000</span><span class="sxs-lookup"><span data-stu-id="c281b-580">0x00001000</span></span>

<span data-ttu-id="c281b-581">Ignora il messaggio di errore [ \_ \_ \_ \_ \_ non valido della CN del certificato di errore di Internet sec](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c281b-581">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>FLAG di sicurezza \_ \_ Ignora \_ certificato \_ data \_ non valido</span><span class="sxs-lookup"><span data-stu-id="c281b-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="c281b-583">0x00002000</span><span class="sxs-lookup"><span data-stu-id="c281b-583">0x00002000</span></span>

<span data-ttu-id="c281b-584">Ignora il messaggio di errore [ \_ \_ \_ \_ \_ non valido relativo alla data del certificato di Internet sec](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c281b-584">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>\_flag \_ di sicurezza ignora \_ Reindirizzamento \_ a \_ http</span><span class="sxs-lookup"><span data-stu-id="c281b-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="c281b-586">0x00008000</span><span class="sxs-lookup"><span data-stu-id="c281b-586">0x00008000</span></span>

<span data-ttu-id="c281b-587">Ignora il messaggio [ \_ di errore Internet \_ https \_ per \_ http \_ su \_ redir](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c281b-587">Ignores the [ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>\_flag \_ di sicurezza ignora \_ Reindirizzamento \_ a \_ https</span><span class="sxs-lookup"><span data-stu-id="c281b-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS</span></span>
</dt> <dd>

<span data-ttu-id="c281b-589">0x00004000</span><span class="sxs-lookup"><span data-stu-id="c281b-589">0x00004000</span></span>

<span data-ttu-id="c281b-590">Ignora l' [errore \_ \_ \_ da http a HTTPS per il messaggio di errore di \_ \_ \_ redir](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c281b-590">Ignores the [ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>il \_ flag di sicurezza \_ Ignora la \_ revoca</span><span class="sxs-lookup"><span data-stu-id="c281b-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>SECURITY\_FLAG\_IGNORE\_REVOCATION</span></span>
</dt> <dd>

<span data-ttu-id="c281b-592">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c281b-592">0x00000080</span></span>

<span data-ttu-id="c281b-593">Ignora i problemi di revoca dei certificati.</span><span class="sxs-lookup"><span data-stu-id="c281b-593">Ignores certificate revocation problems.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ CA sconosciuta</span><span class="sxs-lookup"><span data-stu-id="c281b-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span>
</dt> <dd>

<span data-ttu-id="c281b-595">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c281b-595">0x00000100</span></span>

<span data-ttu-id="c281b-596">Ignora i problemi di autorità di certificazione sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="c281b-596">Ignores unknown certificate authority problems.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ firma debole</span><span class="sxs-lookup"><span data-stu-id="c281b-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span>
</dt> <dd>

<span data-ttu-id="c281b-598">0x00010000</span><span class="sxs-lookup"><span data-stu-id="c281b-598">0x00010000</span></span>

<span data-ttu-id="c281b-599">Ignora i problemi di firma del certificato vulnerabili.</span><span class="sxs-lookup"><span data-stu-id="c281b-599">Ignores weak certificate signature problems.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ utilizzo errato</span><span class="sxs-lookup"><span data-stu-id="c281b-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_WRONG\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="c281b-601">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c281b-601">0x00000200</span></span>

<span data-ttu-id="c281b-602">Ignora problemi di utilizzo non corretti.</span><span class="sxs-lookup"><span data-stu-id="c281b-602">Ignores incorrect usage problems.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>FLAG di sicurezza \_ \_ NORMALBITNESS</span><span class="sxs-lookup"><span data-stu-id="c281b-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>SECURITY\_FLAG\_NORMALBITNESS</span></span>
</dt> <dd>

<span data-ttu-id="c281b-604">0x10000000</span><span class="sxs-lookup"><span data-stu-id="c281b-604">0x10000000</span></span>

<span data-ttu-id="c281b-605">Identico al flag di sicurezza del valore [ \_ \_ \_ debole](/windows).</span><span class="sxs-lookup"><span data-stu-id="c281b-605">Identical to the value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="c281b-606">Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-606">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="c281b-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>FLAG di sicurezza \_ \_ PCT</span><span class="sxs-lookup"><span data-stu-id="c281b-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>SECURITY\_FLAG\_PCT</span></span>
</dt> <dd>

<span data-ttu-id="c281b-608">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c281b-608">0x00000008</span></span>

<span data-ttu-id="c281b-609">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-609">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>FLAG di sicurezza \_ \_ PCT4</span><span class="sxs-lookup"><span data-stu-id="c281b-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>SECURITY\_FLAG\_PCT4</span></span>
</dt> <dd>

<span data-ttu-id="c281b-611">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c281b-611">0x00000010</span></span>

<span data-ttu-id="c281b-612">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-612">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>FLAG di sicurezza \_ \_ sicuro</span><span class="sxs-lookup"><span data-stu-id="c281b-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span>
</dt> <dd>

<span data-ttu-id="c281b-614">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c281b-614">0x00000001</span></span>

<span data-ttu-id="c281b-615">USA i trasferimenti sicuri.</span><span class="sxs-lookup"><span data-stu-id="c281b-615">Uses secure transfers.</span></span> <span data-ttu-id="c281b-616">Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-616">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="c281b-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>\_SSL del flag di sicurezza \_</span><span class="sxs-lookup"><span data-stu-id="c281b-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>SECURITY\_FLAG\_SSL</span></span>
</dt> <dd>

<span data-ttu-id="c281b-618">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c281b-618">0x00000002</span></span>

<span data-ttu-id="c281b-619">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-619">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>FLAG di sicurezza \_ \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="c281b-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>SECURITY\_FLAG\_SSL3</span></span>
</dt> <dd>

<span data-ttu-id="c281b-621">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c281b-621">0x00000004</span></span>

<span data-ttu-id="c281b-622">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-622">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>livello \_ medio del flag di sicurezza \_ \_</span><span class="sxs-lookup"><span data-stu-id="c281b-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span>
</dt> <dd>

<span data-ttu-id="c281b-624">0x40000000</span><span class="sxs-lookup"><span data-stu-id="c281b-624">0x40000000</span></span>

<span data-ttu-id="c281b-625">Usa la crittografia media (a 56 bit).</span><span class="sxs-lookup"><span data-stu-id="c281b-625">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="c281b-626">Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-626">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="c281b-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>sicurezza del flag di sicurezza \_ \_ \_ avanzata</span><span class="sxs-lookup"><span data-stu-id="c281b-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span>
</dt> <dd>

<span data-ttu-id="c281b-628">0x20000000</span><span class="sxs-lookup"><span data-stu-id="c281b-628">0x20000000</span></span>

<span data-ttu-id="c281b-629">Usa la crittografia complessa (a 128 bit).</span><span class="sxs-lookup"><span data-stu-id="c281b-629">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="c281b-630">Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-630">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="c281b-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>resistenza al flag di sicurezza \_ \_ \_ debole</span><span class="sxs-lookup"><span data-stu-id="c281b-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span>
</dt> <dd>

<span data-ttu-id="c281b-632">0x10000000</span><span class="sxs-lookup"><span data-stu-id="c281b-632">0x10000000</span></span>

<span data-ttu-id="c281b-633">Usa la crittografia debole (a 40 bit).</span><span class="sxs-lookup"><span data-stu-id="c281b-633">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="c281b-634">Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-634">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="c281b-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>FLAG di sicurezza \_ \_ UNKNOWNBIT</span><span class="sxs-lookup"><span data-stu-id="c281b-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>SECURITY\_FLAG\_UNKNOWNBIT</span></span>
</dt> <dd>

<span data-ttu-id="c281b-636">0x80000000</span><span class="sxs-lookup"><span data-stu-id="c281b-636">0x80000000</span></span>

<span data-ttu-id="c281b-637">Le dimensioni del bit utilizzate nella crittografia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="c281b-637">The bit size used in the encryption is unknown.</span></span> <span data-ttu-id="c281b-638">Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-638">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> </dl>

<span data-ttu-id="c281b-639">Tenere presente che i dati recuperati in questo modo si riferiscono a una transazione che si è verificata, il cui livello di sicurezza non può più essere modificato.</span><span class="sxs-lookup"><span data-stu-id="c281b-639">Be aware that the data retrieved this way relates to a transaction that has occurred, whose security level can no longer be changed.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="c281b-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**\_opzione Internet \_ chiave di sicurezza \_ \_ bit**</span><span class="sxs-lookup"><span data-stu-id="c281b-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**INTERNET\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-641">36</span><span class="sxs-lookup"><span data-stu-id="c281b-641">36</span></span>
</dt> <dt>



<span data-ttu-id="c281b-642">Recupera un valore long integer senza segno che contiene la dimensione in bit della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="c281b-642">Retrieves an unsigned long integer value that contains the bit size of the encryption key.</span></span> <span data-ttu-id="c281b-643">Maggiore è il numero, maggiore è il livello di crittografia utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c281b-643">The larger the number, the greater the encryption strength used.</span></span> <span data-ttu-id="c281b-644">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-644">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="c281b-645">Tenere presente che i dati recuperati in questo modo si riferiscono a una transazione che si è già verificata, il cui livello di sicurezza non può più essere modificato.</span><span class="sxs-lookup"><span data-stu-id="c281b-645">Be aware that the data retrieved this way relates to a transaction that has already occurred, whose security level can no longer be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**\_ \_ velocità effettiva di invio dell'opzione Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**INTERNET\_OPTION\_SEND\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-647">56</span><span class="sxs-lookup"><span data-stu-id="c281b-647">56</span></span>
</dt> <dt>



<span data-ttu-id="c281b-648">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c281b-648">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**\_timeout di \_ INVIO \_ opzione Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**INTERNET\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-650">5</span><span class="sxs-lookup"><span data-stu-id="c281b-650">5</span></span>
</dt> <dt>



<span data-ttu-id="c281b-651">Imposta o recupera un valore long integer senza segno, in millisecondi, che contiene il valore di timeout per l'invio di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="c281b-651">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request.</span></span> <span data-ttu-id="c281b-652">Se l'invio richiede più tempo rispetto a questo valore di timeout, l'invio viene annullato.</span><span class="sxs-lookup"><span data-stu-id="c281b-652">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="c281b-653">Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="c281b-653">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="c281b-654">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-654">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="c281b-655">Se utilizzata in riferimento a una transazione FTP, questa opzione si riferisce al canale di controllo.</span><span class="sxs-lookup"><span data-stu-id="c281b-655">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**\_contesto della \_ \_ catena di certificati del server opzioni \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**INTERNET\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-657">105</span><span class="sxs-lookup"><span data-stu-id="c281b-657">105</span></span>
</dt> <dt>



<span data-ttu-id="c281b-658">Recupera il contesto della catena di certificati del server come [ \_ \_ contesto di catena PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)duplicato.</span><span class="sxs-lookup"><span data-stu-id="c281b-658">Retrieves the server s certificate-chain context as a duplicated [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="c281b-659">Questo contesto duplicato può essere passato a qualsiasi funzione API di crittografia che accetta [un \_ \_ contesto della catena PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span><span class="sxs-lookup"><span data-stu-id="c281b-659">You may pass this duplicated context to any Crypto API function which takes a [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="c281b-660">È necessario chiamare [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) nel [ \_ \_ contesto della catena PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) restituito al termine del contesto della catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="c281b-660">You must call [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) on the returned [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) when you are done with the certificate-chain context.</span></span>

<span data-ttu-id="c281b-661">**Versione:** Richiede Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="c281b-661">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**\_Impostazioni opzioni \_ Internet \_ modificate**</span><span class="sxs-lookup"><span data-stu-id="c281b-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**INTERNET\_OPTION\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-663">39</span><span class="sxs-lookup"><span data-stu-id="c281b-663">39</span></span>
</dt> <dt>



<span data-ttu-id="c281b-664">Notifica al sistema che le impostazioni del registro di sistema sono state modificate in modo da verificare le impostazioni alla successiva chiamata a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c281b-664">Notifies the system that the registry settings have been changed so that it verifies the settings on the next call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="c281b-665">Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-665">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_opzione Internet \_ Disattiva \_ \_ autenticazione server**</span><span class="sxs-lookup"><span data-stu-id="c281b-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-667">104</span><span class="sxs-lookup"><span data-stu-id="c281b-667">104</span></span>
</dt> <dt>



<span data-ttu-id="c281b-668">Imposta un oggetto richiesta HTTP in modo che non effettuerà l'accesso ai server di origine, ma eseguirà l'accesso automatico ai server proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="c281b-668">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="c281b-669">Questa opzione è diversa dal flag di richiesta **Internet \_ flag \_ No \_ AUTH**, che impedisce l'autenticazione sia per i server proxy che per i server di origine.</span><span class="sxs-lookup"><span data-stu-id="c281b-669">This option differs from the Request flag **INTERNET\_FLAG\_NO\_AUTH**, which prevents authentication to both proxy servers and origin servers.</span></span>

<span data-ttu-id="c281b-670">L'impostazione di questa modalità eliminerà l'utilizzo di qualsiasi materiale delle credenziali (in precedenza fornito nome utente/password o certificato SSL client) durante la comunicazione con un server di origine.</span><span class="sxs-lookup"><span data-stu-id="c281b-670">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="c281b-671">Tuttavia, se la richiesta deve transitare tramite un proxy di autenticazione, WinINet eseguirà comunque l'autenticazione automatica al proxy HTTP in base alle impostazioni dell'area Intranet per l'utente.</span><span class="sxs-lookup"><span data-stu-id="c281b-671">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="c281b-672">L'impostazione predefinita dell'area Intranet è consentire l'accesso automatico utilizzando le credenziali predefinite dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c281b-672">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span>

<span data-ttu-id="c281b-673">Per garantire l'eliminazione di tutte le informazioni di identificazione, il chiamante deve combinare l' **\_ opzione Internet \_ Elimina \_ \_ autenticazione server** con il flag **Internet \_ \_ nessun \_ cookie** richiesta flag.</span><span class="sxs-lookup"><span data-stu-id="c281b-673">To ensure suppression of all identifying information, the caller should combine **INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH** with the **INTERNET\_FLAG\_NO\_COOKIES** request flag.</span></span>

<span data-ttu-id="c281b-674">Questa opzione può essere impostata solo su oggetti richiesta prima dell'invio.</span><span class="sxs-lookup"><span data-stu-id="c281b-674">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="c281b-675">Se si tenta di impostare questa opzione dopo l'invio della richiesta, verrà restituito **\_ \_ \_ \_ lo stato dell'handle errato Internet**.</span><span class="sxs-lookup"><span data-stu-id="c281b-675">Attempts to set this option after the request has been sent will return **ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**.</span></span>

<span data-ttu-id="c281b-676">Per questa opzione non è necessario alcun buffer.</span><span class="sxs-lookup"><span data-stu-id="c281b-676">No buffer is required for this option.</span></span> <span data-ttu-id="c281b-677">Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per gli handle restituiti solo da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="c281b-677">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) on handles returned by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) only.</span></span>

<span data-ttu-id="c281b-678">**Versione:** Richiede Internet Explorer 8,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c281b-678">**Version:** Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**\_opzione Internet \_ Disattiva \_ comportamento**</span><span class="sxs-lookup"><span data-stu-id="c281b-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**INTERNET\_OPTION\_SUPPRESS\_BEHAVIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-680">81</span><span class="sxs-lookup"><span data-stu-id="c281b-680">81</span></span>
</dt> <dt>



<span data-ttu-id="c281b-681">Opzione per utilizzo generico utilizzata per escludere i comportamenti a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="c281b-681">A general purpose option that is used to suppress behaviors on a process-wide basis.</span></span> <span data-ttu-id="c281b-682">Il parametro *lpBuffer* della funzione deve essere un puntatore a un valore DWORD contenente il comportamento specifico da escludere.</span><span class="sxs-lookup"><span data-stu-id="c281b-682">The *lpBuffer* parameter of the function must be a pointer to a DWORD containing the specific behavior to suppress.</span></span> <span data-ttu-id="c281b-683">Non è possibile eseguire query su questa opzione con [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-683">This option cannot be queried with [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="c281b-684">I valori consentiti sono:</span><span class="sxs-lookup"><span data-stu-id="c281b-684">The permitted values are:</span></span>

<dl> <dt>

<span data-ttu-id="c281b-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET non \_ visualizzare \_ Reimposta \_ tutti</span><span class="sxs-lookup"><span data-stu-id="c281b-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET\_SUPPRESS\_RESET\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="c281b-686">0</span><span class="sxs-lookup"><span data-stu-id="c281b-686">0</span></span>

<span data-ttu-id="c281b-687">Disabilita tutte le evitazioni, riattivando il comportamento predefinito e configurato.</span><span class="sxs-lookup"><span data-stu-id="c281b-687">Disables all suppressions, re-enabling default and configured behavior.</span></span> <span data-ttu-id="c281b-688">Questa opzione equivale a impostare Internet per la cancellazione dei **\_ \_ \_ criteri \_ di cookie** e per l'eliminazione dei cookie in modo **\_ \_ \_ permanente \_** .</span><span class="sxs-lookup"><span data-stu-id="c281b-688">This option is the equivalent of setting **INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET** and **INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET** individually.</span></span>

<span data-ttu-id="c281b-689">**Versione:** Richiede Internet Explorer 6,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c281b-689">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>INTERNET non \_ visualizzare i \_ criteri dei cookie \_</span><span class="sxs-lookup"><span data-stu-id="c281b-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY</span></span> 
</dt> <dd>

<span data-ttu-id="c281b-691">1</span><span class="sxs-lookup"><span data-stu-id="c281b-691">1</span></span>

<span data-ttu-id="c281b-692">Ignora tutti i criteri cookie configurati e consente l'impostazione dei cookie.</span><span class="sxs-lookup"><span data-stu-id="c281b-692">Ignores any configured cookie policies and allows cookies to be set.</span></span>

<span data-ttu-id="c281b-693">**Versione:** Richiede Internet Explorer 6,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c281b-693">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET per \_ disattivare la \_ \_ reimpostazione dei criteri cookie \_</span><span class="sxs-lookup"><span data-stu-id="c281b-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET</span></span> 
</dt> <dd>

<span data-ttu-id="c281b-695">2</span><span class="sxs-lookup"><span data-stu-id="c281b-695">2</span></span>

<span data-ttu-id="c281b-696">Disabilita la soppressione **dei \_ \_ \_ criteri dei cookie in Internet** , consentendo la valutazione dei cookie in base ai criteri cookie configurati.</span><span class="sxs-lookup"><span data-stu-id="c281b-696">Disables the **INTERNET\_SUPPRESS\_COOKIE\_POLICY** suppression, permitting the evaluation of cookies according to the configured cookie policy.</span></span>

<span data-ttu-id="c281b-697">**Versione:** Richiede Internet Explorer 6,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c281b-697">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> INTERNET non \_ visualizzare \_ cookie \_ permanente</span><span class="sxs-lookup"><span data-stu-id="c281b-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> INTERNET\_SUPPRESS\_COOKIE\_PERSIST</span></span>
</dt> <dd>

<span data-ttu-id="c281b-699">3</span><span class="sxs-lookup"><span data-stu-id="c281b-699">3</span></span>

<span data-ttu-id="c281b-700">Elimina la persistenza dei cookie, anche se il server li ha specificati come permanenti.</span><span class="sxs-lookup"><span data-stu-id="c281b-700">Suppresses the persistence of cookies, even if the server has specified them as persistent.</span></span>

<span data-ttu-id="c281b-701">**Versione:** Richiede Internet Explorer 8,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c281b-701">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="c281b-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET non \_ visualizzare il \_ cookie \_ Mantieni \_ reimpostato</span><span class="sxs-lookup"><span data-stu-id="c281b-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="c281b-703">4</span><span class="sxs-lookup"><span data-stu-id="c281b-703">4</span></span>

<span data-ttu-id="c281b-704">Disabilita l'eliminazione di **\_ \_ \_ persistenza dei cookie in Internet** , riabilitando la persistenza dei cookie.</span><span class="sxs-lookup"><span data-stu-id="c281b-704">Disables the **INTERNET\_SUPPRESS\_COOKIE\_PERSIST** suppression, re-enabling the persistence of cookies.</span></span> <span data-ttu-id="c281b-705">Eventuali cookie eliminati in precedenza non diventeranno permanenti.</span><span class="sxs-lookup"><span data-stu-id="c281b-705">Any previously suppressed cookies will not become persistent.</span></span>

<span data-ttu-id="c281b-706">**Versione:** Richiede Internet Explorer 8,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c281b-706">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="c281b-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**\_URL opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**INTERNET\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-708">34</span><span class="sxs-lookup"><span data-stu-id="c281b-708">34</span></span>
</dt> <dt>



<span data-ttu-id="c281b-709">Recupera un valore stringa che contiene l'URL completo di una risorsa scaricata.</span><span class="sxs-lookup"><span data-stu-id="c281b-709">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="c281b-710">Se l'URL originale contiene dati aggiuntivi, ad esempio stringhe di ricerca o ancoraggi, oppure se la chiamata è stata reindirizzata, l'URL restituito è diverso dall'originale.</span><span class="sxs-lookup"><span data-stu-id="c281b-710">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="c281b-711">Questa opzione è valida per gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituiti da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="c281b-711">This option is valid on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="c281b-712">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-712">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**\_ \_ agente utente opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**INTERNET\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-714">41</span><span class="sxs-lookup"><span data-stu-id="c281b-714">41</span></span>
</dt> <dt>



<span data-ttu-id="c281b-715">Imposta o recupera la stringa dell'agente utente negli handle forniti da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) e usata nelle funzioni [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) successive, purché non venga sottoposta a override da un'intestazione aggiunta da [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) o [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="c281b-715">Sets or retrieves the user agent string on handles supplied by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) and used in subsequent [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions, as long as it is not overridden by a header added by [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) or [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="c281b-716">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-716">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**\_ \_ nome utente opzione Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**INTERNET\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-718">28</span><span class="sxs-lookup"><span data-stu-id="c281b-718">28</span></span>
</dt> <dt>



<span data-ttu-id="c281b-719">Imposta o Recupera una stringa che contiene il nome utente associato a un handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c281b-719">Sets or retrieves a string that contains the user name associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="c281b-720">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-720">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**\_versione opzione \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="c281b-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**INTERNET\_OPTION\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-722">40</span><span class="sxs-lookup"><span data-stu-id="c281b-722">40</span></span>
</dt> <dt>



<span data-ttu-id="c281b-723">Recupera una struttura di **\_ \_ informazioni sulla versione di Internet** che contiene il numero di versione di Wininet.dll.</span><span class="sxs-lookup"><span data-stu-id="c281b-723">Retrieves an **INTERNET\_VERSION\_INFO** structure that contains the version number of Wininet.dll.</span></span> <span data-ttu-id="c281b-724">Questa opzione può essere usata in un handle [**HINTERNET**](appendix-a-hinternet-handles.md) **null** da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-724">This option can be used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c281b-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**\_dimensioni del \_ buffer di scrittura delle opzioni Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c281b-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**INTERNET\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281b-726">13</span><span class="sxs-lookup"><span data-stu-id="c281b-726">13</span></span>
</dt> <dt>



<span data-ttu-id="c281b-727">Imposta o recupera un valore long integer senza segno che contiene la dimensione, in byte, del buffer di scrittura.</span><span class="sxs-lookup"><span data-stu-id="c281b-727">Sets or retrieves an unsigned long integer value that contains the size, in bytes, of the write buffer.</span></span> <span data-ttu-id="c281b-728">Questa opzione può essere utilizzata per gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituiti da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (solo sessione FTP).</span><span class="sxs-lookup"><span data-stu-id="c281b-728">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="c281b-729">Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="c281b-729">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c281b-730">Commenti</span><span class="sxs-lookup"><span data-stu-id="c281b-730">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c281b-731">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="c281b-731">WinINet does not support server implementations.</span></span> <span data-ttu-id="c281b-732">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="c281b-732">In addition, it should not be used from a service.</span></span> <span data-ttu-id="c281b-733">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="c281b-733">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c281b-734">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c281b-734">Requirements</span></span>



| <span data-ttu-id="c281b-735">Requisito</span><span class="sxs-lookup"><span data-stu-id="c281b-735">Requirement</span></span> | <span data-ttu-id="c281b-736">Valore</span><span class="sxs-lookup"><span data-stu-id="c281b-736">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c281b-737">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c281b-737">Minimum supported client</span></span><br/> | <span data-ttu-id="c281b-738">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c281b-738">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="c281b-739">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c281b-739">Minimum supported server</span></span><br/> | <span data-ttu-id="c281b-740">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c281b-740">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                   |
| <span data-ttu-id="c281b-741">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c281b-741">Header</span></span><br/>                   | <dl> <span data-ttu-id="c281b-742"><dt>WinInet. h; </dt> <dt>Winineti. h</dt></span><span class="sxs-lookup"><span data-stu-id="c281b-742"><dt>Wininet.h; </dt> <dt>Winineti.h</dt></span></span> </dl> |



 

