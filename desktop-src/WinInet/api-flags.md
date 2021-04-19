---
title: Flag API (WinInet. h)
description: Molte delle funzioni WinINet accettano una matrice di flag come parametro. Di seguito è riportata una breve descrizione dei flag definiti.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301958"
---
# <a name="api-flags"></a><span data-ttu-id="c78af-104">Flag API</span><span class="sxs-lookup"><span data-stu-id="c78af-104">API Flags</span></span>

<span data-ttu-id="c78af-105">Molte delle funzioni WinINet accettano una matrice di flag come parametro.</span><span class="sxs-lookup"><span data-stu-id="c78af-105">Many of the WinINet functions accept an array of flags as a parameter.</span></span> <span data-ttu-id="c78af-106">Di seguito è riportata una breve descrizione dei flag definiti.</span><span class="sxs-lookup"><span data-stu-id="c78af-106">The following is a brief description of the defined flags.</span></span>

<dl> <dt>

<span data-ttu-id="c78af-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**Il \_ cookie Internet \_ valuta \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="c78af-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**INTERNET\_COOKIE\_EVALUATE\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-108">0x80</span><span class="sxs-lookup"><span data-stu-id="c78af-108">0x80</span></span>
</dt> <dt>



<span data-ttu-id="c78af-109">Indica che un'intestazione della piattaforma per la protezione della privacy (P3P) deve essere associata a un cookie.</span><span class="sxs-lookup"><span data-stu-id="c78af-109">Indicates that a Platform for Privacy Protection (P3P) header is to be associated with a cookie.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**INTERNET \_ cookie di \_ terze \_ parti**</span><span class="sxs-lookup"><span data-stu-id="c78af-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**INTERNET\_COOKIE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-111">0x10</span><span class="sxs-lookup"><span data-stu-id="c78af-111">0x10</span></span>
</dt> <dt>



<span data-ttu-id="c78af-112">Indica che è in corso l'impostazione o il recupero di un cookie di terze parti.</span><span class="sxs-lookup"><span data-stu-id="c78af-112">Indicates that a third-party cookie is being set or retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**\_flag Internet \_ asincrono**</span><span class="sxs-lookup"><span data-stu-id="c78af-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**INTERNET\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-114">0x10000000</span><span class="sxs-lookup"><span data-stu-id="c78af-114">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-115">Esegue solo richieste asincrone sugli handle derivate dall'handle restituito da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="c78af-115">Makes only asynchronous requests on handles descended from the handle returned from this function.</span></span> <span data-ttu-id="c78af-116">Solo la funzione [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa questo flag.</span><span class="sxs-lookup"><span data-stu-id="c78af-116">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**\_ \_ Async della cache del flag Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-118">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c78af-118">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="c78af-119">Consente la scrittura di cache lazy.</span><span class="sxs-lookup"><span data-stu-id="c78af-119">Allows a lazy cache write.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**\_cache del flag Internet se la rete ha \_ \_ \_ \_ esito negativo**</span><span class="sxs-lookup"><span data-stu-id="c78af-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-121">0x00010000</span><span class="sxs-lookup"><span data-stu-id="c78af-121">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-122">Restituisce la risorsa dalla cache se la richiesta di rete per la risorsa ha esito negativo a causa di un [errore di \_ \_ \_ reimpostazione della connessione Internet](wininet-errors.md) o di [errore \_ Internet \_ non è in grado di \_ connettersi](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c78af-122">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="c78af-123">Questo flag viene usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="c78af-123">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**\_flag Internet \_ dont \_ cache**</span><span class="sxs-lookup"><span data-stu-id="c78af-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**INTERNET\_FLAG\_DONT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-125">0x04000000</span><span class="sxs-lookup"><span data-stu-id="c78af-125">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-126">Non aggiunge l'entità restituita alla cache.</span><span class="sxs-lookup"><span data-stu-id="c78af-126">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="c78af-127">Si tratta di un valore identico a quello preferito, ovvero [ \_ \_ Nessuna \_ \_ scrittura nella cache](/windows).</span><span class="sxs-lookup"><span data-stu-id="c78af-127">This is identical to the preferred value, [INTERNET\_FLAG\_NO\_CACHE\_WRITE](/windows).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**\_flag Internet \_ esistente \_ Connetti**</span><span class="sxs-lookup"><span data-stu-id="c78af-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**INTERNET\_FLAG\_EXISTING\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-129">0x20000000</span><span class="sxs-lookup"><span data-stu-id="c78af-129">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-130">Tenta di utilizzare un oggetto [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) esistente se ne esiste uno con gli stessi attributi necessari per effettuare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c78af-130">Attempts to use an existing [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) object if one exists with the same attributes required to make the request.</span></span> <span data-ttu-id="c78af-131">Questa operazione è utile solo con le operazioni FTP, poiché FTP è l'unico protocollo che in genere esegue più operazioni durante la stessa sessione.</span><span class="sxs-lookup"><span data-stu-id="c78af-131">This is useful only with FTP operations, since FTP is the only protocol that typically performs multiple operations during the same session.</span></span> <span data-ttu-id="c78af-132">WinINet memorizza nella cache un singolo handle di connessione per ogni handle [**HINTERNET**](appendix-a-hinternet-handles.md) generato da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="c78af-132">WinINet caches a single connection handle for each [**HINTERNET**](appendix-a-hinternet-handles.md) handle generated by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="c78af-133">Le funzioni [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e **InternetConnect** utilizzano questo flag per le connessioni HTTP e FTP.</span><span class="sxs-lookup"><span data-stu-id="c78af-133">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and **InternetConnect** functions use this flag for Http and Ftp connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_ \_ Invia form di flag Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**INTERNET\_FLAG\_FORMS\_SUBMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-135">0x00000040</span><span class="sxs-lookup"><span data-stu-id="c78af-135">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="c78af-136">Indica che si tratta di un invio di form.</span><span class="sxs-lookup"><span data-stu-id="c78af-136">Indicates that this is a Forms submission.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_flag Internet \_ dalla \_ cache**</span><span class="sxs-lookup"><span data-stu-id="c78af-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**INTERNET\_FLAG\_FROM\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-138">0x01000000</span><span class="sxs-lookup"><span data-stu-id="c78af-138">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-139">Non esegue richieste di rete.</span><span class="sxs-lookup"><span data-stu-id="c78af-139">Does not make network requests.</span></span> <span data-ttu-id="c78af-140">Tutte le entità vengono restituite dalla cache.</span><span class="sxs-lookup"><span data-stu-id="c78af-140">All entities are returned from the cache.</span></span> <span data-ttu-id="c78af-141">Se l'elemento richiesto non è presente nella cache, viene restituito un errore appropriato, ad esempio file di errore \_ \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="c78af-141">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="c78af-142">Solo la funzione [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa questo flag.</span><span class="sxs-lookup"><span data-stu-id="c78af-142">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**\_nuovo flag Internet \_ FWD \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**INTERNET\_FLAG\_FWD\_BACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-144">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c78af-144">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="c78af-145">Indica che la funzione deve utilizzare la copia della risorsa attualmente nella cache Internet.</span><span class="sxs-lookup"><span data-stu-id="c78af-145">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="c78af-146">La data di scadenza e altre informazioni sulla risorsa non sono controllate.</span><span class="sxs-lookup"><span data-stu-id="c78af-146">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="c78af-147">Se l'elemento richiesto non viene trovato nella cache Internet, il sistema tenta di individuare la risorsa nella rete.</span><span class="sxs-lookup"><span data-stu-id="c78af-147">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="c78af-148">Questo valore è stato introdotto in Microsoft Internet Explorer 5 ed è associato alle operazioni dei pulsanti **Avanti** e **indietro** di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c78af-148">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**\_ \_ collegamento ipertestuale flag Internet**</span><span class="sxs-lookup"><span data-stu-id="c78af-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**INTERNET\_FLAG\_HYPERLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-150">0x00000400</span><span class="sxs-lookup"><span data-stu-id="c78af-150">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="c78af-151">Impone un ricaricamento se non è presente alcuna scadenza e non viene restituito alcun tempo LastModified dal server per determinare se ricaricare l'elemento dalla rete.</span><span class="sxs-lookup"><span data-stu-id="c78af-151">Forces a reload if there is no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.</span></span> <span data-ttu-id="c78af-152">Questo flag può essere usato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="c78af-152">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="c78af-153">**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="c78af-153">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**\_flag Internet \_ Ignora \_ certificato \_ CN \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="c78af-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-155">0x00001000</span><span class="sxs-lookup"><span data-stu-id="c78af-155">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-156">Disabilita il controllo dei certificati basati su SSL/PCT restituiti dal server rispetto al nome host specificato nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="c78af-156">Disables checking of SSL/PCT-based certificates that are returned from the server against the host name given in the request.</span></span> <span data-ttu-id="c78af-157">WinINet utilizza un semplice controllo per i certificati confrontando i nomi host corrispondenti e le semplici regole con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="c78af-157">WinINet uses a simple check against certificates by comparing for matching host names and simple wildcarding rules.</span></span> <span data-ttu-id="c78af-158">Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).</span><span class="sxs-lookup"><span data-stu-id="c78af-158">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**il \_ flag Internet \_ Ignora la data del \_ certificato non è \_ \_ valida**</span><span class="sxs-lookup"><span data-stu-id="c78af-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="c78af-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-161">Disabilita il controllo dei certificati basati su SSL/PCT per le date di validità corrette.</span><span class="sxs-lookup"><span data-stu-id="c78af-161">Disables checking of SSL/PCT-based certificates for proper validity dates.</span></span> <span data-ttu-id="c78af-162">Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).</span><span class="sxs-lookup"><span data-stu-id="c78af-162">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**\_flag Internet \_ ignorare \_ Reindirizzamento \_ a \_ http**</span><span class="sxs-lookup"><span data-stu-id="c78af-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-164">0x00008000</span><span class="sxs-lookup"><span data-stu-id="c78af-164">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-165">Disabilita il rilevamento di questo tipo speciale di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="c78af-165">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="c78af-166">Quando si usa questo flag, WinINet consente i reindirizzamenti da HTTPS a URL HTTP in modo trasparente.</span><span class="sxs-lookup"><span data-stu-id="c78af-166">When this flag is used, WinINet transparently allows redirects from HTTPS to HTTP URLs.</span></span> <span data-ttu-id="c78af-167">Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).</span><span class="sxs-lookup"><span data-stu-id="c78af-167">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**\_flag Internet \_ ignorare \_ Reindirizzamento \_ a \_ https**</span><span class="sxs-lookup"><span data-stu-id="c78af-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-169">0x00004000</span><span class="sxs-lookup"><span data-stu-id="c78af-169">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-170">Disabilita il rilevamento di questo tipo speciale di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="c78af-170">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="c78af-171">Quando si usa questo flag, WinINet consente in modo trasparente i reindirizzamenti da HTTP a URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c78af-171">When this flag is used, WinINet transparently allow redirects from HTTP to HTTPS URLs.</span></span> <span data-ttu-id="c78af-172">Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).</span><span class="sxs-lookup"><span data-stu-id="c78af-172">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**\_flag Internet \_ Mantieni \_ connessione**</span><span class="sxs-lookup"><span data-stu-id="c78af-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**INTERNET\_FLAG\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-174">0x00400000</span><span class="sxs-lookup"><span data-stu-id="c78af-174">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-175">Usa la semantica Keep-Alive, se disponibile, per la connessione.</span><span class="sxs-lookup"><span data-stu-id="c78af-175">Uses keep-alive semantics, if available, for the connection.</span></span> <span data-ttu-id="c78af-176">Questo flag viene usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).</span><span class="sxs-lookup"><span data-stu-id="c78af-176">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span> <span data-ttu-id="c78af-177">Questo flag è obbligatorio per Microsoft Network (MSN), NTLM e altri tipi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c78af-177">This flag is required for Microsoft Network (MSN), NTLM, and other types of authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**FLAG INTERNET che \_ \_ rende \_ persistente**</span><span class="sxs-lookup"><span data-stu-id="c78af-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-179">0x02000000</span><span class="sxs-lookup"><span data-stu-id="c78af-179">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-180">Non più supportata.</span><span class="sxs-lookup"><span data-stu-id="c78af-180">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**il \_ flag Internet \_ deve \_ memorizzare nella cache la \_ richiesta**</span><span class="sxs-lookup"><span data-stu-id="c78af-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c78af-182">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="c78af-183">Identico al valore preferito, **il \_ \_ \_ file di richiesta del flag Internet**.</span><span class="sxs-lookup"><span data-stu-id="c78af-183">Identical to the preferred value, **INTERNET\_FLAG\_NEED\_FILE**.</span></span> <span data-ttu-id="c78af-184">Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="c78af-184">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="c78af-185">Questo flag può essere usato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="c78af-185">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="c78af-186">**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="c78af-186">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**\_file con flag Internet \_ necessario \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**INTERNET\_FLAG\_NEED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-188">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c78af-188">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="c78af-189">Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="c78af-189">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="c78af-190">Questo flag può essere usato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="c78af-190">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="c78af-191">**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="c78af-191">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**\_flag Internet \_ Nessuna \_ autenticazione**</span><span class="sxs-lookup"><span data-stu-id="c78af-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**INTERNET\_FLAG\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-193">0x00040000</span><span class="sxs-lookup"><span data-stu-id="c78af-193">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-194">Non tenta automaticamente l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c78af-194">Does not attempt authentication automatically.</span></span> <span data-ttu-id="c78af-195">Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).</span><span class="sxs-lookup"><span data-stu-id="c78af-195">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**\_flag Internet \_ senza \_ \_ Reindirizzamento automatico**</span><span class="sxs-lookup"><span data-stu-id="c78af-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**INTERNET\_FLAG\_NO\_AUTO\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-197">0x00200000</span><span class="sxs-lookup"><span data-stu-id="c78af-197">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-198">Non gestisce automaticamente il reindirizzamento in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="c78af-198">Does not automatically handle redirection in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="c78af-199">Questo flag può essere usato anche da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) per le richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="c78af-199">This flag can also be used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) for HTTP requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**\_flag Internet \_ senza \_ \_ scrittura cache**</span><span class="sxs-lookup"><span data-stu-id="c78af-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-201">0x04000000</span><span class="sxs-lookup"><span data-stu-id="c78af-201">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-202">Non aggiunge l'entità restituita alla cache.</span><span class="sxs-lookup"><span data-stu-id="c78af-202">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="c78af-203">Questo flag viene utilizzato da, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="c78af-203">This flag is used by , [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="c78af-204">**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="c78af-204">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**\_flag Internet \_ senza \_ cookie**</span><span class="sxs-lookup"><span data-stu-id="c78af-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**INTERNET\_FLAG\_NO\_COOKIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-206">0x00080000</span><span class="sxs-lookup"><span data-stu-id="c78af-206">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-207">Non aggiunge automaticamente le intestazioni dei cookie alle richieste e non aggiunge automaticamente i cookie restituiti al database dei cookie.</span><span class="sxs-lookup"><span data-stu-id="c78af-207">Does not automatically add cookie headers to requests, and does not automatically add returned cookies to the cookie database.</span></span> <span data-ttu-id="c78af-208">Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).</span><span class="sxs-lookup"><span data-stu-id="c78af-208">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**\_flag Internet \_ Nessuna \_ interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="c78af-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**INTERNET\_FLAG\_NO\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c78af-210">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="c78af-211">Disabilita la finestra di dialogo dei cookie.</span><span class="sxs-lookup"><span data-stu-id="c78af-211">Disables the cookie dialog box.</span></span> <span data-ttu-id="c78af-212">Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo richieste http).</span><span class="sxs-lookup"><span data-stu-id="c78af-212">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**\_flag Internet \_ offline**</span><span class="sxs-lookup"><span data-stu-id="c78af-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**INTERNET\_FLAG\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-214">0x01000000</span><span class="sxs-lookup"><span data-stu-id="c78af-214">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-215">Identico **al \_ flag Internet \_ dalla \_ cache**.</span><span class="sxs-lookup"><span data-stu-id="c78af-215">Identical to **INTERNET\_FLAG\_FROM\_CACHE**.</span></span> <span data-ttu-id="c78af-216">Non esegue richieste di rete.</span><span class="sxs-lookup"><span data-stu-id="c78af-216">Does not make network requests.</span></span> <span data-ttu-id="c78af-217">Tutte le entità vengono restituite dalla cache.</span><span class="sxs-lookup"><span data-stu-id="c78af-217">All entities are returned from the cache.</span></span> <span data-ttu-id="c78af-218">Se l'elemento richiesto non è presente nella cache, viene restituito un errore appropriato, ad esempio file di errore \_ \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="c78af-218">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="c78af-219">Solo la funzione [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa questo flag.</span><span class="sxs-lookup"><span data-stu-id="c78af-219">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**\_flag Internet \_ passivo**</span><span class="sxs-lookup"><span data-stu-id="c78af-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**INTERNET\_FLAG\_PASSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-221">0x08000000</span><span class="sxs-lookup"><span data-stu-id="c78af-221">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-222">Usa la semantica FTP passiva.</span><span class="sxs-lookup"><span data-stu-id="c78af-222">Uses passive FTP semantics.</span></span> <span data-ttu-id="c78af-223">Solo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usano questo flag.</span><span class="sxs-lookup"><span data-stu-id="c78af-223">Only [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) use this flag.</span></span> <span data-ttu-id="c78af-224">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilizza questo flag per le richieste FTP e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilizza questo flag per i file e le directory FTP.</span><span class="sxs-lookup"><span data-stu-id="c78af-224">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses this flag for FTP requests, and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses this flag for FTP files and directories.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**\_flag Internet \_ pragma \_ NoCache**</span><span class="sxs-lookup"><span data-stu-id="c78af-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-226">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c78af-226">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="c78af-227">Impone la risoluzione della richiesta da parte del server di origine, anche se nel proxy esiste una copia memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="c78af-227">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="c78af-228">La funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo per le richieste HTTP e HTTPS) e la funzione [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usano questo flag.</span><span class="sxs-lookup"><span data-stu-id="c78af-228">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_flag Internet \_ dati non elaborati \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**INTERNET\_FLAG\_RAW\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-230">0x40000000</span><span class="sxs-lookup"><span data-stu-id="c78af-230">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-231">Restituisce i dati come struttura [**di \_ \_ dati Find Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) durante il recupero delle informazioni sulla directory FTP.</span><span class="sxs-lookup"><span data-stu-id="c78af-231">Returns the data as a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure when retrieving FTP directory information.</span></span> <span data-ttu-id="c78af-232">Se questo flag non viene specificato o se la chiamata viene eseguita tramite un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) restituisce la versione HTML della directory.</span><span class="sxs-lookup"><span data-stu-id="c78af-232">If this flag is not specified or if the call is made through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) returns the HTML version of the directory.</span></span> <span data-ttu-id="c78af-233">Solo la funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa questo flag.</span><span class="sxs-lookup"><span data-stu-id="c78af-233">Only the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function uses this flag.</span></span>

<span data-ttu-id="c78af-234">**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Restituisce inoltre una struttura di [**\_ \_ dati Find di Gopher**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) durante il recupero delle informazioni sulla directory gopher.</span><span class="sxs-lookup"><span data-stu-id="c78af-234">**Windows XP and Windows Server 2003 R2 and earlier:** Also returns a [**GOPHER\_FIND\_DATA**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) structure when retrieving Gopher directory information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**prelettura flag INTERNET- \_ \_ lettura \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**INTERNET\_FLAG\_READ\_PREFETCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-236">0x00100000</span><span class="sxs-lookup"><span data-stu-id="c78af-236">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-237">Questo flag è attualmente disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c78af-237">This flag is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**\_ricarica del flag Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**INTERNET\_FLAG\_RELOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-239">0x80000000</span><span class="sxs-lookup"><span data-stu-id="c78af-239">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-240">Impone un download del file, dell'oggetto o dell'elenco di directory richiesto dal server di origine e non dalla cache.</span><span class="sxs-lookup"><span data-stu-id="c78af-240">Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.</span></span> <span data-ttu-id="c78af-241">Le funzioni [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usano questo flag.</span><span class="sxs-lookup"><span data-stu-id="c78af-241">The [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) functions use this flag.</span></span>

<span data-ttu-id="c78af-242">**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="c78af-242">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_area con \_ restrizioni del flag Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**INTERNET\_FLAG\_RESTRICTED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-244">0x00020000</span><span class="sxs-lookup"><span data-stu-id="c78af-244">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-245">Indica che il cookie da impostare è associato a un sito non attendibile.</span><span class="sxs-lookup"><span data-stu-id="c78af-245">Indicates that the cookie being set is associated with an untrusted site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**risincronizzazione del \_ flag Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-247">0x00000800</span><span class="sxs-lookup"><span data-stu-id="c78af-247">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="c78af-248">Ricarica le risorse HTTP se la risorsa è stata modificata dall'ultima volta in cui è stata scaricata.</span><span class="sxs-lookup"><span data-stu-id="c78af-248">Reloads HTTP resources if the resource has been modified since the last time it was downloaded.</span></span> <span data-ttu-id="c78af-249">Tutte le risorse FTP vengono ricaricate.</span><span class="sxs-lookup"><span data-stu-id="c78af-249">All FTP resources are reloaded.</span></span> <span data-ttu-id="c78af-250">Questo flag può essere usato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="c78af-250">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="c78af-251">**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)e le risorse Gopher vengono ricaricate.</span><span class="sxs-lookup"><span data-stu-id="c78af-251">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), and Gopher resources are reloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**\_flag Internet \_ sicuro**</span><span class="sxs-lookup"><span data-stu-id="c78af-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**INTERNET\_FLAG\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-253">0x00800000</span><span class="sxs-lookup"><span data-stu-id="c78af-253">0x00800000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-254">Utilizza semantica sicura delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="c78af-254">Uses secure transaction semantics.</span></span> <span data-ttu-id="c78af-255">Questo si traduce nell'utilizzo di Secure Sockets Layer/Private Communications Technology (SSL/PCT) ed è significativo solo nelle richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="c78af-255">This translates to using Secure Sockets Layer/Private Communications Technology (SSL/PCT) and is only meaningful in HTTP requests.</span></span> <span data-ttu-id="c78af-256">Questo flag viene usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), ma è ridondante se https://viene visualizzato nell'URL. La funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa questo flag per le connessioni HTTP. il flag verrà ereditato da tutti gli handle di richiesta creati in questa connessione.</span><span class="sxs-lookup"><span data-stu-id="c78af-256">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), but this is redundant if https:// appears in the URL.The [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function uses this flag for HTTP connections; all the request handles created under this connection will inherit this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**\_flag Internet \_ Transfer \_ ASCII**</span><span class="sxs-lookup"><span data-stu-id="c78af-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**INTERNET\_FLAG\_TRANSFER\_ASCII**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-258">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c78af-258">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="c78af-259">Trasferisce il file come ASCII (solo FTP).</span><span class="sxs-lookup"><span data-stu-id="c78af-259">Transfers file as ASCII (FTP only).</span></span> <span data-ttu-id="c78af-260">Questo flag può essere usato da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)e [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="c78af-260">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_binario di \_ trasferimento del flag Internet \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**INTERNET\_FLAG\_TRANSFER\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-262">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c78af-262">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="c78af-263">Trasferisce il file come binario (solo FTP).</span><span class="sxs-lookup"><span data-stu-id="c78af-263">Transfers file as binary (FTP only).</span></span> <span data-ttu-id="c78af-264">Questo flag può essere usato da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)e [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="c78af-264">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET \_ senza \_ callback**</span><span class="sxs-lookup"><span data-stu-id="c78af-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c78af-266">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="c78af-267">Indica che non deve essere eseguito alcun callback per l'API.</span><span class="sxs-lookup"><span data-stu-id="c78af-267">Indicates that no callbacks should be made for that API.</span></span> <span data-ttu-id="c78af-268">Viene usato per il parametro *dxContext* delle funzioni che consentono operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="c78af-268">This is used for the *dxContext* parameter of the functions that allow asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_opzione Internet \_ Disattiva \_ \_ autenticazione server**</span><span class="sxs-lookup"><span data-stu-id="c78af-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-270">104</span><span class="sxs-lookup"><span data-stu-id="c78af-270">104</span></span>
</dt> <dt>



<span data-ttu-id="c78af-271">Imposta un oggetto richiesta HTTP in modo che non effettuerà l'accesso ai server di origine, ma eseguirà l'accesso automatico ai server proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="c78af-271">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="c78af-272">Questa opzione è diversa dal flag di richiesta INTERNET \_ flag \_ No \_ AUTH, che impedisce l'autenticazione sia per i server proxy che per i server di origine.</span><span class="sxs-lookup"><span data-stu-id="c78af-272">This option differs from the Request flag INTERNET\_FLAG\_NO\_AUTH, which prevents authentication to both proxy servers and origin servers.</span></span> <span data-ttu-id="c78af-273">L'impostazione di questa modalità eliminerà l'utilizzo di qualsiasi materiale delle credenziali (in precedenza fornito nome utente/password o certificato SSL client) durante la comunicazione con un server di origine.</span><span class="sxs-lookup"><span data-stu-id="c78af-273">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="c78af-274">Tuttavia, se la richiesta deve transitare tramite un proxy di autenticazione, WinINet eseguirà comunque l'autenticazione automatica al proxy HTTP in base alle impostazioni dell'area Intranet per l'utente.</span><span class="sxs-lookup"><span data-stu-id="c78af-274">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="c78af-275">L'impostazione predefinita dell'area Intranet è consentire l'accesso automatico utilizzando le credenziali predefinite dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c78af-275">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span> <span data-ttu-id="c78af-276">Per garantire l'eliminazione di tutte le informazioni di identificazione, il chiamante deve combinare l' \_ opzione Internet \_ Elimina \_ \_ autenticazione server con il flag Internet \_ \_ nessun \_ cookie richiesta flag.</span><span class="sxs-lookup"><span data-stu-id="c78af-276">To ensure suppression of all identifying information, the caller should combine INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH with the INTERNET\_FLAG\_NO\_COOKIES request flag.</span></span> <span data-ttu-id="c78af-277">Questa opzione può essere impostata solo su oggetti richiesta prima dell'invio.</span><span class="sxs-lookup"><span data-stu-id="c78af-277">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="c78af-278">Se si tenta di impostare questa opzione dopo l'invio della richiesta, verrà \_ restituito \_ \_ lo stato dell'handle errato Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="c78af-278">Attempts to set this option after the request has been sent will return ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE.</span></span> <span data-ttu-id="c78af-279">Per questa opzione non è necessario alcun buffer.</span><span class="sxs-lookup"><span data-stu-id="c78af-279">No buffer is required for this option.</span></span> <span data-ttu-id="c78af-280">Viene usato da InternetSetOption per gli handle restituiti solo da HttpOpenRequest.</span><span class="sxs-lookup"><span data-stu-id="c78af-280">This is used by InternetSetOption on handles returned by HttpOpenRequest only.</span></span> <span data-ttu-id="c78af-281">Versione: richiede Internet Explorer 8,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c78af-281">Version: Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**\_flag API \_ WinInet \_ asincrono**</span><span class="sxs-lookup"><span data-stu-id="c78af-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WININET\_API\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c78af-283">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="c78af-284">Forza le operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="c78af-284">Forces asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**\_ \_ sincronizzazione flag API \_ WinInet**</span><span class="sxs-lookup"><span data-stu-id="c78af-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**WININET\_API\_FLAG\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-286">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c78af-286">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="c78af-287">Forza le operazioni sincrone.</span><span class="sxs-lookup"><span data-stu-id="c78af-287">Forces synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c78af-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**\_contesto di \_ utilizzo del flag API \_ WinInet \_**</span><span class="sxs-lookup"><span data-stu-id="c78af-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**WININET\_API\_FLAG\_USE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c78af-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c78af-289">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="c78af-290">Impone all'API di usare il valore di contesto, anche se è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="c78af-290">Forces the API to use the context value, even if it is set to zero.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c78af-291">Commenti</span><span class="sxs-lookup"><span data-stu-id="c78af-291">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c78af-292">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="c78af-292">WinINet does not support server implementations.</span></span> <span data-ttu-id="c78af-293">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="c78af-293">In addition, it should not be used from a service.</span></span> <span data-ttu-id="c78af-294">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="c78af-294">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c78af-295">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c78af-295">Requirements</span></span>



| <span data-ttu-id="c78af-296">Requisito</span><span class="sxs-lookup"><span data-stu-id="c78af-296">Requirement</span></span> | <span data-ttu-id="c78af-297">Valore</span><span class="sxs-lookup"><span data-stu-id="c78af-297">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c78af-298">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c78af-298">Minimum supported client</span></span><br/> | <span data-ttu-id="c78af-299">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c78af-299">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c78af-300">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c78af-300">Minimum supported server</span></span><br/> | <span data-ttu-id="c78af-301">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c78af-301">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c78af-302">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c78af-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="c78af-303"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="c78af-303"><dt>Wininet.h</dt></span></span> </dl> |



 

