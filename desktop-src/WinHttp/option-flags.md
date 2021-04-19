---
Description: I flag di opzione seguenti sono supportati da WinHttpQueryOption e WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Flag di opzione (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 56eea8e528c445c5ce6f852ff8841073dd74d6a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332888"
---
# <a name="option-flags"></a><span data-ttu-id="32223-103">Flag di opzione</span><span class="sxs-lookup"><span data-stu-id="32223-103">Option Flags</span></span>

<span data-ttu-id="32223-104">I flag di opzione seguenti sono supportati da [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="32223-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="32223-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**l' \_ opzione WinHTTP ha \_ assicurato \_ \_ callback non bloccanti \_**</span><span class="sxs-lookup"><span data-stu-id="32223-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-106">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="32223-106">The default is FALSE.</span></span> <span data-ttu-id="32223-107">Se impostato su TRUE, WinHTTP non garantisce lo stato di avanzamento se i callback di stato sono bloccati dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="32223-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="32223-108">L'applicazione client deve prestare particolare attenzione a eseguire le operazioni minime all'interno del callback senza bloccarle, restituendo il più rapidamente possibile e in particolare non deve attendere le chiamate WinHTTP successive.</span><span class="sxs-lookup"><span data-stu-id="32223-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="32223-109">Se non segue queste linee guida, è probabile che si verifichi un impatto negativo sulle prestazioni o un potenziale blocco dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32223-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="32223-110">Se utilizzata nel modo prestabilito, questa opzione può migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="32223-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**criteri di accesso \_ automatico opzione WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="32223-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-112">Imposta un valore long integer senza segno che specifica i [criteri di accesso automatici](authentication-in-winhttp.md) con uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="32223-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="32223-113">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-113">Term</span></span> | <span data-ttu-id="32223-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-114">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>\_livello di sicurezza automatico WinHTTP- \_ \_ \_ alto</span><span class="sxs-lookup"><span data-stu-id="32223-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="32223-116">Le credenziali predefinite non vengono utilizzate.</span><span class="sxs-lookup"><span data-stu-id="32223-116">Default credentials are not used.</span></span> <span data-ttu-id="32223-117">Si noti che questo flag viene applicato solo se si specifica il server in base al nome del computer effettivo.</span><span class="sxs-lookup"><span data-stu-id="32223-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="32223-118">Non avrà effetto, se si specifica il server in base a "localhost" o indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="32223-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="32223-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>\_livello di sicurezza automatico WinHTTP- \_ \_ \_ basso</span><span class="sxs-lookup"><span data-stu-id="32223-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="32223-120">Per tutte le richieste viene eseguito un accesso autenticato con le credenziali predefinite.</span><span class="sxs-lookup"><span data-stu-id="32223-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="32223-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>\_supporto del livello di \_ sicurezza automatico WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="32223-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="32223-122">Un accesso autenticato con le credenziali predefinite viene eseguito solo per le richieste nella Intranet locale.</span><span class="sxs-lookup"><span data-stu-id="32223-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="32223-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_callback di opzioni WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-124">Recupera il puntatore al set di funzioni di callback con [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="32223-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contesto del \_ \_ certificato client dell'opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-126">Imposta il contesto del certificato client.</span><span class="sxs-lookup"><span data-stu-id="32223-126">Sets the client certificate context.</span></span> <span data-ttu-id="32223-127">Se un'applicazione riceve un errore per il certificato di [**\_ \_ autenticazione client WinHTTP \_ \_ \_ necessario**](error-messages.md), deve chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per fornire un certificato prima di ritentare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="32223-128">Nell'ambito dell'elaborazione di questa opzione, WinHttp chiama [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) nel contesto del certificato fornito dal chiamante, in modo che il contesto del certificato possa essere rilasciato in modo indipendente dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="32223-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="32223-129">L'applicazione non deve tentare di chiudere l'archivio certificati con il flag del flag di chiusura dell'archivio certificati per la \_ \_ \_ \_ chiamata a [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) nell'archivio certificati da cui è stato recuperato il contesto del certificato.</span><span class="sxs-lookup"><span data-stu-id="32223-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="32223-130">Potrebbe verificarsi una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="32223-130">An access violation may occur.</span></span>

<span data-ttu-id="32223-131">Quando il server richiede un certificato client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce un errore relativo al certificato di [**autenticazione del \_ \_ client WinHTTP \_ \_ \_ necessario**](error-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="32223-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="32223-132">Se il server richiede il certificato ma non lo richiede, l'applicazione può specificare questa opzione per indicare che non dispone di un certificato.</span><span class="sxs-lookup"><span data-stu-id="32223-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="32223-133">Il server può scegliere un altro schema di autenticazione o consentire l'accesso anonimo al server.</span><span class="sxs-lookup"><span data-stu-id="32223-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="32223-134">L'applicazione fornisce la macro del **contesto del certificato del \_ \_ client WinHTTP \_ \_ Nessuna** nel parametro *lpBuffer* di [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="32223-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="32223-135">Se il server richiede un certificato client, può inviare un codice di stato HTTP 403 in risposta.</span><span class="sxs-lookup"><span data-stu-id="32223-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="32223-136">Per ulteriori informazioni, vedere l'opzione **WinHTTP opzione \_ \_ client \_ CERT \_ Issuer \_ List** .</span><span class="sxs-lookup"><span data-stu-id="32223-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_elenco di \_ \_ \_ autorità emittenti del certificato client dell'opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-138">Recupera una [**struttura \_ IssuerListInfoEx di SecPkgContext**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) quando l'errore [**di WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) è errore il certificato di **autenticazione del \_ client WinHTTP \_ \_ \_ \_ necessario**.</span><span class="sxs-lookup"><span data-stu-id="32223-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="32223-139">L'elenco delle autorità emittenti nella struttura contiene un elenco di autorità di certificazione (CA) accettabili dal server.</span><span class="sxs-lookup"><span data-stu-id="32223-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="32223-140">L'applicazione client può filtrare l'elenco di CA per recuperare il certificato client per l'autenticazione SSL.</span><span class="sxs-lookup"><span data-stu-id="32223-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="32223-141">In alternativa, se il server richiede il certificato client, ma non lo richiede, l'applicazione può chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l'opzione del contesto del certificato **client dell' \_ opzione \_ \_ \_ WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="32223-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="32223-142">Per ulteriori informazioni, vedere l'opzione di **\_ \_ \_ \_ contesto certificato client opzione WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="32223-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**opzione WINHTTP-tabella \_ \_ codici**</span><span class="sxs-lookup"><span data-stu-id="32223-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-144">Imposta la [*tabella codici*](glossary.md) utilizzata per elaborare l'URL (ovvero la stringa di query).</span><span class="sxs-lookup"><span data-stu-id="32223-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="32223-145">Il valore predefinito è UTF8.</span><span class="sxs-lookup"><span data-stu-id="32223-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_opzione WinHTTP \_ Configure \_ Passport \_ AUTH**</span><span class="sxs-lookup"><span data-stu-id="32223-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-147">Imposta un valore long integer senza segno che specifica se [l'autenticazione Passport nell'autenticazione WinHTTP](passport-authentication-in-winhttp.md) è abilitata.</span><span class="sxs-lookup"><span data-stu-id="32223-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="32223-148">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="32223-148">The value can be one of the following:</span></span>

| <span data-ttu-id="32223-149">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-149">Term</span></span> | <span data-ttu-id="32223-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-150">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ disabilitare \_ l' \_ autenticazione Passport</span><span class="sxs-lookup"><span data-stu-id="32223-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="32223-152">L'autenticazione Microsoft Passport è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="32223-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="32223-153">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="32223-153">This is the default.</span></span> |
| <span data-ttu-id="32223-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ disabilitare \_ il \_ portachiavi Passport</span><span class="sxs-lookup"><span data-stu-id="32223-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="32223-155">Il portachiavi Passport è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="32223-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="32223-156">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="32223-156">This is the default.</span></span> |
| <span data-ttu-id="32223-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ Abilita \_ \_ autenticazione Passport</span><span class="sxs-lookup"><span data-stu-id="32223-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="32223-158">Autenticazione Passport abilitata.</span><span class="sxs-lookup"><span data-stu-id="32223-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="32223-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ Abilita \_ il \_ portachiavi Passport</span><span class="sxs-lookup"><span data-stu-id="32223-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="32223-160">Il portachiavi Passport è abilitato.</span><span class="sxs-lookup"><span data-stu-id="32223-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="32223-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_tentativi di \_ connessione dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-162">Imposta o recupera un valore long integer senza segno che contiene il numero di tentativi di timesWinHTTP per la connessione a un host.</span><span class="sxs-lookup"><span data-stu-id="32223-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="32223-163">I servizi HTTP di Microsoft Windows (WinHTTP) tentano una sola volta per ogni indirizzo IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="32223-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="32223-164">Se ad esempio si tenta di connettersi a un host multihomed con 10 indirizzi IP e i **tentativi di connessione dell' \_ opzione \_ \_ WinHTTP** sono impostati su 7, WinHTTP tenterà solo di connettersi ai primi sette indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="32223-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="32223-165">Dato lo stesso set di 10 indirizzi IP, se il tentativo di **\_ connessione dell'opzione \_ \_ WinHTTP** è impostato su 20, WinHTTP tenterà ogni 10 una sola volta.</span><span class="sxs-lookup"><span data-stu-id="32223-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="32223-166">Se un tentativo di connessione non riesce ancora dopo il numero di tentativi specificato o se il timeout di connessione è scaduto prima di, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="32223-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="32223-167">Il valore predefinito per **i \_ \_ \_ tentativi di connessione dell'opzione WinHTTP** è cinque tentativi.</span><span class="sxs-lookup"><span data-stu-id="32223-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_ \_ timeout connessione opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-169">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="32223-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="32223-170">Se si imposta questa opzione su infinito (0xFFFFFFFF), questo timer verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="32223-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="32223-171">Se una richiesta di connessione TCP impiega più tempo rispetto a questo valore di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="32223-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="32223-172">Il timeout predefinito è di 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="32223-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="32223-173">Quando si tenta di connettersi a più indirizzi IP per un singolo host (host multihomed), il limite di timeout è per ogni singola connessione.</span><span class="sxs-lookup"><span data-stu-id="32223-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_informazioni di \_ connessione dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-175">Recupera l'indirizzo IP di origine e di destinazione e la porta della richiesta che ha generato la risposta quando [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce.</span><span class="sxs-lookup"><span data-stu-id="32223-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="32223-176">L'applicazione chiama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con l'opzione di **\_ informazioni di \_ connessione \_ dell'opzione WinHTTP** e fornisce la struttura delle [**informazioni di \_ connessione \_ WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) nel parametro *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="32223-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="32223-177">Per ulteriori informazioni, vedere **le \_ \_ informazioni di connessione WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="32223-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="32223-178">**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="32223-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_Opzioni WinHTTP \_ connessione \_ statistiche \_ V0**</span><span class="sxs-lookup"><span data-stu-id="32223-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-180">Recupera lo struct [**TCP \_ info \_ V0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) per la connessione sottostante utilizzata dalla richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="32223-181">Lo struct restituito può contenere statistiche delle richieste precedenti inviate tramite la stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="32223-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="32223-182">Questa opzione è stata sostituita dall' **\_ opzione WinHTTP \_ Connection \_ Statistics \_ V1**.</span><span class="sxs-lookup"><span data-stu-id="32223-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Opzioni WinHTTP \_ connessione \_ statistiche \_ V1**</span><span class="sxs-lookup"><span data-stu-id="32223-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-184">Recupera lo struct [**TCP \_ info \_ V1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) per la connessione sottostante utilizzata dalla richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="32223-185">Lo struct restituito può contenere statistiche delle richieste precedenti inviate tramite la stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="32223-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_valore del \_ contesto dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-187">Imposta o recupera un **\_ ptr DWORD** che contiene un puntatore al valore di contesto associato a questo handle [HINTERNET](hinternet-handles-in-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="32223-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="32223-188">Viene utilizzato il valore archiviato nel buffer e al flag di opzione del **\_ valore del \_ contesto \_ dell'opzione WinHTTP** viene assegnato un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="32223-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**decompressione dell' \_ opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-190">Imposta un valore DWORD dei flag che determinano se WinHTTP decomprimerà automaticamente i corpi della risposta con codifiche di contenuto compresse.</span><span class="sxs-lookup"><span data-stu-id="32223-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="32223-191">In WinHTTP viene inoltre impostata un'intestazione Accept-Encoding appropriata, eseguendo l'override di qualsiasi oggetto fornito dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="32223-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="32223-192">I valori supportati sono:</span><span class="sxs-lookup"><span data-stu-id="32223-192">Supported values are:</span></span>

| <span data-ttu-id="32223-193">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-193">Term</span></span> | <span data-ttu-id="32223-194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-194">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_flag di decompressione WinHTTP ( \_ \_ gzip)</span><span class="sxs-lookup"><span data-stu-id="32223-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="32223-196">Decomprimi Content-Encoding: risposte gzip.</span><span class="sxs-lookup"><span data-stu-id="32223-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="32223-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_flag di decompressione WinHTTP \_ \_ deflate</span><span class="sxs-lookup"><span data-stu-id="32223-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="32223-198">Decomprimi Content-Encoding: Deflate risposte.</span><span class="sxs-lookup"><span data-stu-id="32223-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="32223-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_flag di decompressione WinHTTP \_ \_ tutti</span><span class="sxs-lookup"><span data-stu-id="32223-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="32223-200">Decomprimere le risposte con qualsiasi codifica di contenuto supportata.</span><span class="sxs-lookup"><span data-stu-id="32223-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="32223-201">Per impostazione predefinita, WinHTTP fornirà risposte compresse al chiamante senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="32223-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_funzionalità di \_ disabilitazione dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-203">Imposta un valore long integer senza segno che specifica quali funzionalità sono disabilitate con uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="32223-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="32223-204">Tenere presente che questa funzionalità deve essere passata solo a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) sugli handle di richiesta dopo la creazione dell'handle di richiesta con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)e prima che la richiesta venga inviata con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="32223-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="32223-205">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-205">Term</span></span> | <span data-ttu-id="32223-206">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-206">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ Disabilita \_ l'autenticazione</span><span class="sxs-lookup"><span data-stu-id="32223-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="32223-208">L'autenticazione automatica è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="32223-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="32223-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>\_disabilitare i \_ cookie in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="32223-210">L'aggiunta automatica delle intestazioni dei cookie alle richieste è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="32223-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="32223-211">Inoltre, i cookie restituiti non vengono aggiunti automaticamente al database dei cookie.</span><span class="sxs-lookup"><span data-stu-id="32223-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="32223-212">La disabilitazione dei cookie può comportare una riduzione delle prestazioni per l'autenticazione Passport.</span><span class="sxs-lookup"><span data-stu-id="32223-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="32223-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>\_disabilitazione WinHTTP \_ Keep- \_ Alive</span><span class="sxs-lookup"><span data-stu-id="32223-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="32223-214">Disabilita la semantica Keep-Alive per la connessione.</span><span class="sxs-lookup"><span data-stu-id="32223-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="32223-215">La semantica Keep-Alive è necessaria per MSN, NTLM e altri tipi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="32223-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="32223-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_REindirizzamenti disabilitati WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="32223-217">Il reindirizzamento automatico è disabilitato quando si inviano richieste con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="32223-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="32223-218">Se il reindirizzamento automatico è disabilitato, un'applicazione deve registrare una funzione di callback affinché l'autenticazione Passport abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="32223-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="32223-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_opzione WinHTTP \_ disabilitare \_ il \_ fallback del protocollo sicuro \_**</span><span class="sxs-lookup"><span data-stu-id="32223-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-220">Impedisce a WinHTTP di ritentare una connessione con una versione precedente del protocollo di sicurezza quando la negoziazione del protocollo iniziale ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="32223-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**\_opzione WinHTTP \_ disabilitare \_ la \_ coda di flusso**</span><span class="sxs-lookup"><span data-stu-id="32223-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-222">Consente alle nuove richieste di aprire una connessione HTTP/2 aggiuntiva quando viene raggiunto il limite massimo di flussi simultanei, anziché attendere il successivo flusso disponibile su una connessione esistente.</span><span class="sxs-lookup"><span data-stu-id="32223-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_funzionalità di \_ Abilitazione dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-224">Imposta un valore long integer senza segno che specifica le funzionalità attualmente abilitate.</span><span class="sxs-lookup"><span data-stu-id="32223-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="32223-225">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="32223-225">Can be one of the following values.</span></span>

| <span data-ttu-id="32223-226">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-226">Term</span></span> | <span data-ttu-id="32223-227">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-227">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ Abilita \_ la \_ rappresentazione del ripristino SSL \_</span><span class="sxs-lookup"><span data-stu-id="32223-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="32223-229">Se abilitata, WinHTTP Annulla temporaneamente la rappresentazione client per la durata delle operazioni di autenticazione del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="32223-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="32223-230">Questo valore può essere impostato solo nell'handle della sessione.</span><span class="sxs-lookup"><span data-stu-id="32223-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="32223-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ Abilita \_ \_ revoca SSL</span><span class="sxs-lookup"><span data-stu-id="32223-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="32223-232">Se abilitata, WinHTTP consente la revoca SSL.</span><span class="sxs-lookup"><span data-stu-id="32223-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="32223-233">Questo valore può essere impostato solo nell'handle della richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_opzione WinHTTP \_ Abilita \_ \_ protocollo http**</span><span class="sxs-lookup"><span data-stu-id="32223-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-235">Imposta una maschera di bit DWORD di versioni HTTP avanzate accettabili.</span><span class="sxs-lookup"><span data-stu-id="32223-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="32223-236">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="32223-236">Possible values are:</span></span>

| <span data-ttu-id="32223-237">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-237">Term</span></span> | <span data-ttu-id="32223-238">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-238">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_Flag di protocollo WinHTTP \_ \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="32223-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="32223-240">Abilita HTTP/2 per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="32223-241">Nessuno (0x0)</span><span class="sxs-lookup"><span data-stu-id="32223-241">None (0x0)</span></span> | <span data-ttu-id="32223-242">Limita la richiesta a HTTP/1.1 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="32223-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="32223-243">Non è possibile disabilitare le versioni legacy di HTTP (1,1 e precedenti) con questa opzione.</span><span class="sxs-lookup"><span data-stu-id="32223-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="32223-244">Il valore predefinito è 0x0.</span><span class="sxs-lookup"><span data-stu-id="32223-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_opzione WinHTTP \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="32223-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-246">Imposta un valore **bool** che specifica se la traccia è attualmente abilitata.</span><span class="sxs-lookup"><span data-stu-id="32223-246">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="32223-247">Per ulteriori informazioni sulla funzionalità di traccia in WinHTTP, vedere la pagina relativa alla [funzionalità di traccia WinHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="32223-247">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="32223-248">Questa opzione può essere impostata solo su un handle **HINTERNET** **null** .</span><span class="sxs-lookup"><span data-stu-id="32223-248">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="32223-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**\_opzione WinHTTP \_ Encode \_ extra**</span><span class="sxs-lookup"><span data-stu-id="32223-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-250">Abilita la codifica URL percentuale per percorso e stringa di query.</span><span class="sxs-lookup"><span data-stu-id="32223-250">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="32223-251">In alternativa, è possibile codificare la percentuale prima di chiamare WinHttp.</span><span class="sxs-lookup"><span data-stu-id="32223-251">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="32223-252"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ errore esteso dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-252"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-253">Recupera un valore unsigned long integer che contiene un codice di errore di Microsoft Windows Sockets di cui è stato eseguito il mapping ai \_ messaggi di errore WinHTTP di errore \_ \* restituiti per ultimi in questo contesto del thread.</span><span class="sxs-lookup"><span data-stu-id="32223-253">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="32223-254">È possibile passare **null** come valore dell'handle.</span><span class="sxs-lookup"><span data-stu-id="32223-254">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-255"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**\_opzione WinHTTP \_ \_ proxy globale \_ credenziali**</span><span class="sxs-lookup"><span data-stu-id="32223-255"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-256">Accetta un puntatore a una [**struttura \_ credenziali WinHTTP \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *HINTERNET* impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="32223-256">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="32223-257">Questa opzione richiede la chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings. ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="32223-257">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="32223-258">Se questa chiave del registro di sistema non è impostata, WinHTTP restituirà l' **errore errore \_ WinHTTP \_ non valido \_**.</span><span class="sxs-lookup"><span data-stu-id="32223-258">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="32223-259">Questa chiave del registro di sistema non è presente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="32223-259">This registry key is not present by default.</span></span> <span data-ttu-id="32223-260">Quando è impostato, WinINet invierà le credenziali a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="32223-260">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="32223-261">Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono state impostate credenziali sull'handle corrente, utilizzerà le credenziali fornite da WinINet.</span><span class="sxs-lookup"><span data-stu-id="32223-261">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="32223-262">Per condividere le credenziali del server oltre alle credenziali proxy, gli utenti devono impostare l' **opzione WinHTTP per l' \_ \_ utilizzo delle \_ \_ \_ credenziali globali del server** .</span><span class="sxs-lookup"><span data-stu-id="32223-262">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-263"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_opzione WinHTTP \_ \_ server globale \_ credenziali**</span><span class="sxs-lookup"><span data-stu-id="32223-263"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-264">Accetta un puntatore a una [**struttura \_ credenziali WinHTTP \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *HINTERNET* impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="32223-264">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="32223-265">Questa opzione richiede la chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings. ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="32223-265">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="32223-266">Se questa chiave del registro di sistema non è impostata, WinHTTP restituirà l' **errore errore \_ WinHTTP \_ non valido \_**.</span><span class="sxs-lookup"><span data-stu-id="32223-266">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="32223-267">Questa chiave del registro di sistema non è presente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="32223-267">This registry key is not present by default.</span></span> <span data-ttu-id="32223-268">Quando è impostato, WinINet invierà le credenziali a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="32223-268">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="32223-269">Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono state impostate credenziali sull'handle corrente, utilizzerà le credenziali fornite da WinINet.</span><span class="sxs-lookup"><span data-stu-id="32223-269">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="32223-270">Per condividere le credenziali del server oltre alle credenziali proxy, gli utenti devono impostare l' **opzione WinHTTP per l' \_ \_ utilizzo delle \_ \_ \_ credenziali globali del server** .</span><span class="sxs-lookup"><span data-stu-id="32223-270">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-271"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**\_tipo di \_ handle dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-271"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-272">Recupera un valore long integer senza segno che contiene il tipo dell'handle [HINTERNET](hinternet-handles-in-winhttp.md) passato.</span><span class="sxs-lookup"><span data-stu-id="32223-272">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="32223-273">Il valore restituito può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="32223-273">The return value can be one of the following:</span></span>

| <span data-ttu-id="32223-274">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-274">Term</span></span> | <span data-ttu-id="32223-275">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-275">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-276"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_connessione del \_ tipo di handle WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-276"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="32223-277">L'handle è un handle di connessione.</span><span class="sxs-lookup"><span data-stu-id="32223-277">The handle is a connection handle.</span></span> |
| <span data-ttu-id="32223-278"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_richiesta del \_ tipo di handle WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-278"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="32223-279">L'handle è un handle di richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-279">The handle is a request handle.</span></span> |
| <span data-ttu-id="32223-280"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_sessione del \_ tipo di handle WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-280"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="32223-281">L'handle è un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="32223-281">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="32223-282"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**il \_ protocollo HTTP dell'opzione WinHTTP è \_ \_ \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="32223-282"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-283">Impedisce che le versioni del protocollo diverse da quelle abilitate dall' **opzione WinHTTP abilitano l'uso del \_ \_ \_ \_ protocollo http** per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-283">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-284"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**\_opzione WinHTTP \_ \_ protocollo http \_ usato**</span><span class="sxs-lookup"><span data-stu-id="32223-284"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-285">Ottiene un valore DWORD che indica quale versione HTTP avanzata è stata utilizzata per una determinata richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-285">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="32223-286">Per un elenco di valori possibili, vedere **\_ opzione WinHTTP \_ Abilita \_ \_ protocollo http**.</span><span class="sxs-lookup"><span data-stu-id="32223-286">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-287"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_opzione WinHTTP \_ \_ versione http**</span><span class="sxs-lookup"><span data-stu-id="32223-287"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-288">Imposta o Recupera una struttura di [**\_ \_ informazioni sulla versione http**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) che contiene la versione http supportata.</span><span class="sxs-lookup"><span data-stu-id="32223-288">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="32223-289">Si tratta di un'opzione a livello di processo. utilizzare **null** per l'handle.</span><span class="sxs-lookup"><span data-stu-id="32223-289">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-290"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_opzione WinHTTP \_ ignorare la revoca del \_ certificato \_ \_ offline**</span><span class="sxs-lookup"><span data-stu-id="32223-290"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-291">Consente alle connessioni sicure di usare i certificati di sicurezza per i quali non è stato possibile scaricare l'elenco di revoche di certificati.</span><span class="sxs-lookup"><span data-stu-id="32223-291">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-292"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_Opzione WinHTTP \_ - \_ fallback rapido IPv6 \_**</span><span class="sxs-lookup"><span data-stu-id="32223-292"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-293">Abilita il fallback rapido IPv6 (più a occhi più contenti) per la connessione.</span><span class="sxs-lookup"><span data-stu-id="32223-293">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="32223-294">Questo comportamento è simile al comportamento degli occhi felici descritto in [RFC 6555](https://tools.ietf.org/html/rfc6555) per migliorare i tempi di connessione nelle reti in cui IPv6 non è affidabile.</span><span class="sxs-lookup"><span data-stu-id="32223-294">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="32223-295">Se gli indirizzi IPv6 e IPv4 vengono risolti per un determinato host, WinHttp inizierà con la connessione al primo indirizzo IPv6 risolto con un timeout breve (300 ms).</span><span class="sxs-lookup"><span data-stu-id="32223-295">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="32223-296">Se la connessione ha esito negativo, WinHttp tenterà di connettersi al primo indirizzo IPv4 risolto con il timeout standard.</span><span class="sxs-lookup"><span data-stu-id="32223-296">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="32223-297">Se la seconda connessione ha esito negativo, WinHttp tenterà di ritentare il primo indirizzo IPv6 risolto con il timeout standard.</span><span class="sxs-lookup"><span data-stu-id="32223-297">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="32223-298">Se la terza connessione ha esito negativo, WinHttp ripristinerà il comportamento predefinito per tutti gli indirizzi rimanenti, tentando di connettersi a ognuno con il timeout standard fino a quando non viene effettuata una connessione o non rimangono indirizzi.</span><span class="sxs-lookup"><span data-stu-id="32223-298">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-299"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**l' \_ opzione WinHTTP \_ è la \_ risposta di \_ connessione proxy \_**</span><span class="sxs-lookup"><span data-stu-id="32223-299"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-300">Ottiene un valore che indica se è possibile recuperare una risposta di connessione del proxy.</span><span class="sxs-lookup"><span data-stu-id="32223-300">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-301"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_Opzione WinHTTP \_ numero massimo di \_ conn \_ per \_ \_ Server 1 0 \_**</span><span class="sxs-lookup"><span data-stu-id="32223-301"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-302">Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="32223-302">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="32223-303">Il valore predefinito è **infinito**.</span><span class="sxs-lookup"><span data-stu-id="32223-303">The default value is **INFINITE**.</span></span>

<span data-ttu-id="32223-304">**Windows Vista con SP1 e Windows Server 2008:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="32223-304">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-305"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_opzione WinHTTP \_ numero massimo di \_ conn \_ per \_ Server**</span><span class="sxs-lookup"><span data-stu-id="32223-305"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-306">Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per server.</span><span class="sxs-lookup"><span data-stu-id="32223-306">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="32223-307">Il valore predefinito è **infinito**.</span><span class="sxs-lookup"><span data-stu-id="32223-307">The default value is **INFINITE**.</span></span>

<span data-ttu-id="32223-308">Quando questa opzione è impostata su zero, WinHTTP imposta il limite per il numero di connessioni a 2.</span><span class="sxs-lookup"><span data-stu-id="32223-308">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-309"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**\_opzione WinHTTP \_ numero massimo di \_ \_ \_ reindirizzamenti automatici http**</span><span class="sxs-lookup"><span data-stu-id="32223-309"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-310">Imposta il numero massimo di reindirizzamenti che WinHTTP segue; il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="32223-310">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="32223-311">Questo limite impedisce ai siti non autorizzati di far sospendere il client WinHTTP dopo un numero elevato di reindirizzamenti.</span><span class="sxs-lookup"><span data-stu-id="32223-311">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="32223-312">**Windows XP con SP1 e windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="32223-312">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-313"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_opzione WinHTTP \_ numero \_ massimo \_ stato http \_ continua**</span><span class="sxs-lookup"><span data-stu-id="32223-313"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-314">Il numero massimo di risposte del codice di stato 100-199 informativo ignorate prima di restituire il codice di stato finale al client WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="32223-314">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="32223-315">I codici di stato informativi 100-199 possono essere inviati dal server prima del codice di stato finale e sono descritti nella specifica per HTTP/1.1 (per ulteriori informazioni, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="32223-315">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="32223-316">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="32223-316">The default is 10.</span></span>

<span data-ttu-id="32223-317">**Windows XP con SP1 e windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="32223-317">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-318"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**\_ \_ dimensioni massime \_ \_ svuotamento risposta \_ opzione WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-318"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-319">Oggetto associato alla quantità di dati svuotati dalle risposte per riutilizzare una connessione, specificata in byte.</span><span class="sxs-lookup"><span data-stu-id="32223-319">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="32223-320">Il valore predefinito è 1 MB.</span><span class="sxs-lookup"><span data-stu-id="32223-320">The default is 1MB.</span></span>

<span data-ttu-id="32223-321">**Windows XP con SP1 e windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="32223-321">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-322"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_ \_ dimensioni massime \_ \_ intestazione risposta \_ opzione WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-322"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-323">Set associato alla dimensione massima della parte di intestazione della risposta del server, specificato in byte.</span><span class="sxs-lookup"><span data-stu-id="32223-323">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="32223-324">Questo limite protegge il client da un server non autorizzato che tenta di bloccare il client inviando una risposta con una quantità infinita di dati di intestazione.</span><span class="sxs-lookup"><span data-stu-id="32223-324">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="32223-325">Il valore predefinito è 64KB.</span><span class="sxs-lookup"><span data-stu-id="32223-325">The default value is 64KB.</span></span>

<span data-ttu-id="32223-326">**Windows XP con SP1 e windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="32223-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-327"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ handle padre dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-327"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-328">Recupera l'handle padre per questo handle.</span><span class="sxs-lookup"><span data-stu-id="32223-328">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-329"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**testo per la personalizzazione dell' \_ opzione WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="32223-329"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-330">Recupera una stringa che contiene il testo di [*cobranding*](glossary.md) fornito dal server di accesso Passport.</span><span class="sxs-lookup"><span data-stu-id="32223-330">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="32223-331">Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401.</span><span class="sxs-lookup"><span data-stu-id="32223-331">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="32223-332">Un'applicazione deve passare una dimensione del buffer, in byte, sufficientemente grande da mantenere la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="32223-332">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-333"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_URL di \_ \_ copersonalizzazione dell'opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-333"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-334">Recupera una stringa che contiene un URL per un'immagine di [*cobranding*](glossary.md) fornita dal server di accesso Passport.</span><span class="sxs-lookup"><span data-stu-id="32223-334">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="32223-335">Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401.</span><span class="sxs-lookup"><span data-stu-id="32223-335">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="32223-336">Un'applicazione deve passare una dimensione del buffer, in byte, sufficientemente grande da mantenere la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="32223-336">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-337"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_opzione WinHTTP \_ - \_ URL restituito Passport \_**</span><span class="sxs-lookup"><span data-stu-id="32223-337"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-338">Imposta un'opzione di sola lettura su un handle di richiesta che recupera l'URL di ritorno Passport.</span><span class="sxs-lookup"><span data-stu-id="32223-338">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-339"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_opzione WinHTTP \_ - \_ disconnessione Passport \_**</span><span class="sxs-lookup"><span data-stu-id="32223-339"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-340">Imposta l'opzione in un handle di sessione per disconnettersi da qualsiasi account di accesso Passport.</span><span class="sxs-lookup"><span data-stu-id="32223-340">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="32223-341">Un'applicazione deve passare l'URL di ritorno al passaporto recuperato con l' **\_ opzione WinHTTP \_ Passport \_ return \_ URL**.</span><span class="sxs-lookup"><span data-stu-id="32223-341">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="32223-342">Tutti i cookie correlati all'URL restituito vengono cancellati.</span><span class="sxs-lookup"><span data-stu-id="32223-342">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-343"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_password opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-343"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-344">Imposta o recupera un valore stringa che contiene la password associata a un handle di richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-344">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-345"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_proxy dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-345"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-346">Imposta o Recupera una struttura di [**\_ \_ informazioni proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) che contiene i dati del proxy su un handle di sessione o un handle di richiesta esistente.</span><span class="sxs-lookup"><span data-stu-id="32223-346">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="32223-347">Quando si recuperano i dati proxy, un'applicazione deve liberare le stringhe **lpszProxy** e **lpszProxyBypass** contenute in questa struttura (se sono non **null**) utilizzando la funzione [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="32223-347">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="32223-348">Un'applicazione può eseguire una query per i dati globali del proxy (proxy predefinito) passando un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="32223-348">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-349"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_ \_ password proxy opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-349"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-350">Imposta o recupera un valore stringa che contiene la password utilizzata per accedere al proxy.</span><span class="sxs-lookup"><span data-stu-id="32223-350">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-351"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**\_SPN del proxy dell'opzione WinHTTP \_ \_ \_ usato**</span><span class="sxs-lookup"><span data-stu-id="32223-351"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-352">Ottiene il nome dell'entità del server proxy fornito da WinHTTP a SSPI durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="32223-352">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="32223-353">Questo valore stringa è usefor passando a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) dopo un errore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="32223-353">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-354"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_ \_ nome utente proxy opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-354"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-355">Imposta o recupera un valore stringa che contiene il nome utente utilizzato per accedere al proxy.</span><span class="sxs-lookup"><span data-stu-id="32223-355">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-356"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_dimensioni del \_ buffer di lettura dell'opzione WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="32223-356"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-357">Questa opzione è stata deprecata. non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="32223-357">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-358"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**\_risposta di \_ \_ connessione proxy \_ di ricezione opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-358"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-359">Imposta un valore che indica se è possibile recuperare l'entità di risposta del proxy.</span><span class="sxs-lookup"><span data-stu-id="32223-359">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="32223-360">Questa opzione è disabilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="32223-360">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-361"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**\_timeout di \_ \_ risposta ricezione opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-361"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-362">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, di attesa per la ricezione di tutte le intestazioni di risposta a una richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-362">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="32223-363">Se WinHTTP non riesce a ricevere tutte le intestazioni entro questo periodo di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="32223-363">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="32223-364">Il valore di timeout predefinito è 90 secondi.</span><span class="sxs-lookup"><span data-stu-id="32223-364">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="32223-365">Questo timeout viene controllato solo quando i dati vengono ricevuti dal socket.</span><span class="sxs-lookup"><span data-stu-id="32223-365">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="32223-366">Di conseguenza, quando il timeout scade, l'applicazione client non riceve una notifica finché non arriva un numero maggiore di dati dal server.</span><span class="sxs-lookup"><span data-stu-id="32223-366">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="32223-367">Se non arrivano dati dal server, il ritardo tra la scadenza del timeout e la notifica dell'applicazione client potrebbe essere pari a quello del valore di timeout impostato utilizzando il parametro *dwReceiveTimeout* della funzione [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .</span><span class="sxs-lookup"><span data-stu-id="32223-367">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-368"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_timeout di \_ ricezione dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-368"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-369">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per ricevere una risposta parziale a una richiesta o leggere alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="32223-369">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="32223-370">Se la risposta richiede più tempo rispetto a questo valore di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="32223-370">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="32223-371">Il valore di timeout predefinito è di 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="32223-371">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-372"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_criteri di \_ Reindirizzamento \_ Opzioni WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-372"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-373">Imposta il comportamento di WinHTTP sulla gestione di un codice di stato di reindirizzamento HTTP di 30x.</span><span class="sxs-lookup"><span data-stu-id="32223-373">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="32223-374">Questa opzione può essere impostata su un handle di sessione o di richiesta su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="32223-374">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="32223-375">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-375">Term</span></span> | <span data-ttu-id="32223-376">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-376">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_criteri di \_ Reindirizzamento opzioni WinHTTP \_ \_ sempre</span><span class="sxs-lookup"><span data-stu-id="32223-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="32223-378">Tutti i reindirizzamenti vengono seguiti automaticamente.</span><span class="sxs-lookup"><span data-stu-id="32223-378">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="32223-379"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ criteri di reindirizzamento opzioni WinHTTP non \_ \_ consentono \_ https \_ per \_ http</span><span class="sxs-lookup"><span data-stu-id="32223-379"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="32223-380">Vengono seguiti tutti i reindirizzamenti, ad eccezione di quelli che hanno origine da un URL protetto (HTTPS) a un URL non sicuro (http).</span><span class="sxs-lookup"><span data-stu-id="32223-380">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="32223-381">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="32223-381">This is the default setting.</span></span> |
| <span data-ttu-id="32223-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_criteri di \_ Reindirizzamento opzioni WinHTTP \_ \_ mai</span><span class="sxs-lookup"><span data-stu-id="32223-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="32223-383">I reindirizzamenti non vengono mai seguiti.</span><span class="sxs-lookup"><span data-stu-id="32223-383">Redirects are never followed.</span></span> <span data-ttu-id="32223-384">Lo stato 30x viene restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32223-384">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-385"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_opzione WinHTTP \_ rifiutare \_ USERPWD \_ nell' \_ URL**</span><span class="sxs-lookup"><span data-stu-id="32223-385"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-386">Rifiuta gli URL contenenti un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="32223-386">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="32223-387">Questa opzione rifiuta anche gli URL che contengono la semantica *username: password* , anche se non è specificato alcun nome utente o password.</span><span class="sxs-lookup"><span data-stu-id="32223-387">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="32223-388">Ad esempio, " u:p@hostname ", " :@hostname ", " u:@hostname " e " :p@hostname " verrebbero tutti contrassegnati come non validi.</span><span class="sxs-lookup"><span data-stu-id="32223-388">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="32223-389">Se alla funzione viene passato un URL non valido, viene restituito [l' \_ errore \_ WinHTTP \_ non valido](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="32223-389">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="32223-390">Per impostazione predefinita, questa opzione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="32223-390">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-391"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_ \_ priorità richiesta opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-391"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-392">Questa opzione è stata deprecata. non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="32223-392">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-393"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_statistiche delle \_ richieste di opzioni WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-393"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-394">Statistiche recupera per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-394">Retreives statistics for the request.</span></span>  <span data-ttu-id="32223-395">Per un elenco delle statistiche disponibili, vedere [**WinHTTP \_ Request \_ Statistics**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="32223-395">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-396"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_tempi di \_ richiesta dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-396"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-397">Informazioni sull'intervallo di recupera per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-397">Retreives timing information for the request.</span></span> <span data-ttu-id="32223-398">Per un elenco degli intervalli disponibili, vedere [**\_ \_ tempi di richiesta WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="32223-398">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-399"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**\_ \_ timeout risoluzione opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-399"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-400">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per la risoluzione di un nome host.</span><span class="sxs-lookup"><span data-stu-id="32223-400">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="32223-401">Il valore di timeout predefinito è **infinito**.</span><span class="sxs-lookup"><span data-stu-id="32223-401">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="32223-402">Se viene specificato un valore non predefinito, si verifica un sovraccarico di una creazione di thread per risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32223-402">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-403"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**\_protocolli di \_ sicurezza delle opzioni WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-403"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-404">Imposta un valore long integer senza segno che specifica quali protocolli di sicurezza sono accettabili.</span><span class="sxs-lookup"><span data-stu-id="32223-404">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="32223-405">Per impostazione predefinita, solo SSL3 e TLS1 sono abilitati in Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="32223-405">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="32223-406">Per impostazione predefinita, solo SSL3, TLS 1.0, TLS 1.1 e TLS 1.2 sono abilitati in Windows 8.1 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="32223-406">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="32223-407">Il valore può essere una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="32223-407">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="32223-408">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-408">Term</span></span> | <span data-ttu-id="32223-409">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-409">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-410"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>FLAG WINHTTP- \_ \_ protocollo sicuro- \_ \_ tutto</span><span class="sxs-lookup"><span data-stu-id="32223-410"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="32223-411">È possibile usare i protocolli Secure Sockets Layer (SSL) 2,0, SSL 3,0 e Transport Layer Security (TLS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="32223-411">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="32223-412"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>FLAG WINHTTP- \_ \_ \_ protocollo protetto \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="32223-412"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="32223-413">Il protocollo SSL 2,0 può essere usato.</span><span class="sxs-lookup"><span data-stu-id="32223-413">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="32223-414"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>FLAG WINHTTP- \_ \_ \_ protocollo protetto \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="32223-414"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="32223-415">Il protocollo SSL 3,0 può essere usato.</span><span class="sxs-lookup"><span data-stu-id="32223-415">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="32223-416"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>FLAG WINHTTP- \_ \_ \_ protocollo protetto \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="32223-416"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="32223-417">Il protocollo TLS 1,0 può essere usato.</span><span class="sxs-lookup"><span data-stu-id="32223-417">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="32223-418"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_Protocollo WinHTTP \_ flag \_ Secure \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="32223-418"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="32223-419">Il protocollo TLS 1,1 può essere usato.</span><span class="sxs-lookup"><span data-stu-id="32223-419">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="32223-420"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_Protocollo WinHTTP \_ flag \_ Secure \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="32223-420"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="32223-421">Il protocollo TLS 1,2 può essere usato.</span><span class="sxs-lookup"><span data-stu-id="32223-421">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="32223-422"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_ \_ struct certificato di sicurezza opzione \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-422"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-423">Recupera il certificato per un server SSL/TLS nella struttura [**delle \_ \_ informazioni del certificato WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="32223-423">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="32223-424">L'applicazione deve liberare i membri **lpszSubjectInfo** e **lpszIssuerInfo** con [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span><span class="sxs-lookup"><span data-stu-id="32223-424">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-425"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_flag di \_ sicurezza delle opzioni WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-425"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-426">Imposta o recupera un valore long integer senza segno che contiene i flag di sicurezza per un handle.</span><span class="sxs-lookup"><span data-stu-id="32223-426">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="32223-427">Può essere una combinazione di questi valori:</span><span class="sxs-lookup"><span data-stu-id="32223-427">It can be a combination of these values:</span></span>

| <span data-ttu-id="32223-428">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-428">Term</span></span> | <span data-ttu-id="32223-429">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-429">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-430"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>FLAG di sicurezza \_ \_ Ignora \_ certificato \_ CN \_ non valido</span><span class="sxs-lookup"><span data-stu-id="32223-430"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="32223-431">Consente un nome comune non valido in un certificato; ovvero, il nome del server specificato dall'applicazione non corrisponde al nome comune nel certificato.</span><span class="sxs-lookup"><span data-stu-id="32223-431">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="32223-432">Se questo flag è impostato, l'applicazione non riceve un callback **del \_ certificato di stato di callback WinHTTP non \_ \_ \_ \_ \_ valido** .</span><span class="sxs-lookup"><span data-stu-id="32223-432">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="32223-433"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>FLAG di sicurezza \_ \_ Ignora \_ certificato \_ data \_ non valido</span><span class="sxs-lookup"><span data-stu-id="32223-433"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="32223-434">Consente la data di un certificato non valido, ovvero un certificato scaduto o non ancora valido.</span><span class="sxs-lookup"><span data-stu-id="32223-434">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="32223-435">Se questo flag è impostato, l'applicazione non riceve un callback **del \_ flag di stato del callback WinHTTP \_ data non \_ \_ \_ \_ valido** .</span><span class="sxs-lookup"><span data-stu-id="32223-435">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="32223-436"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ CA sconosciuta</span><span class="sxs-lookup"><span data-stu-id="32223-436"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="32223-437">Consente un'autorità di certificazione non valida.</span><span class="sxs-lookup"><span data-stu-id="32223-437">Allows an invalid certificate authority.</span></span> <span data-ttu-id="32223-438">Se questo flag è impostato, l'applicazione non riceve un callback **della \_ \_ CA non \_ \_ valido del \_ flag di stato di callback WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="32223-438">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="32223-439"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>il \_ flag di sicurezza \_ Ignora l' \_ utilizzo del certificato \_ non corretto \_</span><span class="sxs-lookup"><span data-stu-id="32223-439"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="32223-440">Consente di stabilire l'identità di un server con un certificato non server (ad esempio, un certificato client).</span><span class="sxs-lookup"><span data-stu-id="32223-440">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="32223-441"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ firma debole</span><span class="sxs-lookup"><span data-stu-id="32223-441"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="32223-442">Consente di ignorare una firma vulnerabile.</span><span class="sxs-lookup"><span data-stu-id="32223-442">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="32223-443">Questo flag è disponibile nell'aggiornamento cumulativo per ogni sistema operativo a partire da Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="32223-443">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="32223-444"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>FLAG di sicurezza \_ \_ sicuro</span><span class="sxs-lookup"><span data-stu-id="32223-444"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="32223-445">USA i trasferimenti sicuri.</span><span class="sxs-lookup"><span data-stu-id="32223-445">Uses secure transfers.</span></span> <span data-ttu-id="32223-446">Questa operazione viene restituita solo in una chiamata a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="32223-446">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="32223-447"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>livello \_ medio del flag di sicurezza \_ \_</span><span class="sxs-lookup"><span data-stu-id="32223-447"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="32223-448">Usa la crittografia media (a 56 bit).</span><span class="sxs-lookup"><span data-stu-id="32223-448">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="32223-449">Questa operazione viene restituita solo in una chiamata a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="32223-449">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="32223-450"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>sicurezza del flag di sicurezza \_ \_ \_ avanzata</span><span class="sxs-lookup"><span data-stu-id="32223-450"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="32223-451">Usa la crittografia complessa (a 128 bit).</span><span class="sxs-lookup"><span data-stu-id="32223-451">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="32223-452">Questa operazione viene restituita solo in una chiamata a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="32223-452">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="32223-453"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>resistenza al flag di sicurezza \_ \_ \_ debole</span><span class="sxs-lookup"><span data-stu-id="32223-453"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="32223-454">Usa la crittografia debole (a 40 bit).</span><span class="sxs-lookup"><span data-stu-id="32223-454">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="32223-455">Questa operazione viene restituita solo in una chiamata a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="32223-455">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="32223-456"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**\_informazioni di \_ sicurezza sull'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-456"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-457">Recupera la connessione SChannel e le informazioni di crittografia per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="32223-457">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-458"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**\_chiave di sicurezza dell'opzione WinHTTP \_ \_ \_ bit**</span><span class="sxs-lookup"><span data-stu-id="32223-458"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-459">Recupera un valore long integer senza segno che contiene il livello di codifica della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="32223-459">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="32223-460">Un numero maggiore indica una crittografia più avanzata del livello di crittografia.</span><span class="sxs-lookup"><span data-stu-id="32223-460">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-461"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ timeout invio opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-461"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-462">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per inviare una richiesta o scrivere alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="32223-462">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="32223-463">Se l'invio della richiesta richiede più tempo del timeout, l'operazione di invio viene annullata.</span><span class="sxs-lookup"><span data-stu-id="32223-463">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="32223-464">Il timeout predefinito è 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="32223-464">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-465"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_Server opzioni \_ WinHTTP \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="32223-465"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-466">Ottiene un puntatore alla struttura di [**\_ Binding SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) che specifica un token di associazione di canale (CBT).</span><span class="sxs-lookup"><span data-stu-id="32223-466">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="32223-467">Un token di associazione di canale è una proprietà di un canale di trasporto sicuro e viene utilizzato per associare un canale di autenticazione al canale di trasporto protetto.</span><span class="sxs-lookup"><span data-stu-id="32223-467">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="32223-468">Questo token può essere ottenuto solo tramite questa opzione dopo che è stata stabilita una connessione SSL.</span><span class="sxs-lookup"><span data-stu-id="32223-468">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="32223-469">Se si passa questa opzione e un valore **null** per *lpBuffer* a [**WINHTTPQUERYOPTION**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) , viene restituito l'errore \_ buffer insufficiente \_ e le dimensioni di byte richieste per il buffer nel parametro *lpdwBufferLength* .</span><span class="sxs-lookup"><span data-stu-id="32223-469">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="32223-470">Il valore della dimensione del buffer restituito può essere passato in una chiamata successiva a query per il token di associazione del canale.</span><span class="sxs-lookup"><span data-stu-id="32223-470">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="32223-471">Questi passaggi sono necessari \_ \_ \_ per la gestione della richiesta di stato di callback WinHTTP se si desidera modificare le intestazioni della richiesta in base al token di associazione del canale.</span><span class="sxs-lookup"><span data-stu-id="32223-471">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="32223-472">Si noti che Windows XP e vista non supportano la modifica delle intestazioni delle richieste durante questo callback.</span><span class="sxs-lookup"><span data-stu-id="32223-472">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-473"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_ \_ \_ contesto catena di certificati \_ server \_ Opzioni WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-473"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-474">Recupera il contesto della catena di certificazione server.</span><span class="sxs-lookup"><span data-stu-id="32223-474">Retrieves the server certification chain context.</span></span> <span data-ttu-id="32223-475">**WinHTTP \_ È possibile passare il \_ \_ \_ \_ contesto della catena** di certificati del server di opzione per ottenere un puntatore duplicato al **\_ \_ contesto della catena** di certificati per una catena di certificati server ricevuta durante una connessione SSL negoziata.</span><span class="sxs-lookup"><span data-stu-id="32223-475">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="32223-476">Il client deve chiamare [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sul puntatore di contesto PCCERT restituito \_ che viene inserito nel buffer.</span><span class="sxs-lookup"><span data-stu-id="32223-476">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-477"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_ \_ \_ contesto certificato server opzioni \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-477"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-478">Recupera il contesto di certificazione del server.</span><span class="sxs-lookup"><span data-stu-id="32223-478">Retrieves the server certification context.</span></span> <span data-ttu-id="32223-479">**WinHTTP \_ È possibile passare il \_ \_ \_ contesto** del certificato del server per ottenere un puntatore duplicato al [**contesto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) del certificato per un certificato del server ricevuto durante una connessione SSL negoziata.</span><span class="sxs-lookup"><span data-stu-id="32223-479">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="32223-480">Il client deve chiamare [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sul puntatore di contesto PCCERT restituito \_ che viene inserito nel buffer.</span><span class="sxs-lookup"><span data-stu-id="32223-480">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-481"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**\_ \_ nome SPN Server opzioni WinHTTP \_ \_ usato**</span><span class="sxs-lookup"><span data-stu-id="32223-481"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-482">Ottiene il nome dell'entità server server fornito da WinHTTP a SSPI durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="32223-482">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="32223-483">Questo valore stringa può essere passato a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) dopo un errore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="32223-483">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-484"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_ \_ nome SPN opzione WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-484"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-485">Include o rimuove il numero di porta del server quando il nome SPN (nome dell'entità servizio) viene compilato per Kerberos o negozia l'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="32223-485">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="32223-486">Questo flag è uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="32223-486">This flag is one of the following values:</span></span>

| <span data-ttu-id="32223-487">Termine</span><span class="sxs-lookup"><span data-stu-id="32223-487">Term</span></span> | <span data-ttu-id="32223-488">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32223-488">Description</span></span> |
|-|-|
| <span data-ttu-id="32223-489"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>\_disabilitare la \_ \_ porta del server SPN \_</span><span class="sxs-lookup"><span data-stu-id="32223-489"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="32223-490">Rimuove il numero di porta del server.</span><span class="sxs-lookup"><span data-stu-id="32223-490">Removes the server port number.</span></span> |
| <span data-ttu-id="32223-491"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_Abilita WinHTTP \_ \_ porta server \_ SPN</span><span class="sxs-lookup"><span data-stu-id="32223-491"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="32223-492">Include il numero di porta del server.</span><span class="sxs-lookup"><span data-stu-id="32223-492">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="32223-493"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_opzione WinHTTP \_ - \_ apertura rapida TCP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-493"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-494">Consente l'apertura rapida di TCP per la connessione.</span><span class="sxs-lookup"><span data-stu-id="32223-494">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-495"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**opzione WINHTTP ( \_ \_ avvio) TLS \_ false \_**</span><span class="sxs-lookup"><span data-stu-id="32223-495"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-496">Abilita l'avvio di TLS false per la connessione.</span><span class="sxs-lookup"><span data-stu-id="32223-496">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-497"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_evento di \_ scaricamento dell'opzione WinHTTP \_ Notify \_**</span><span class="sxs-lookup"><span data-stu-id="32223-497"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-498">Accetta un evento che verrà impostato al completamento dell'ultimo callback per una determinata sessione.</span><span class="sxs-lookup"><span data-stu-id="32223-498">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="32223-499">Questo flag deve essere utilizzato in un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="32223-499">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="32223-500">Non è possibile chiudere l'evento finché non è stato impostato da WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="32223-500">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-501"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**opzione WINHTTP- \_ \_ analisi dell'intestazione non sicura \_ \_**</span><span class="sxs-lookup"><span data-stu-id="32223-501"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-502">Questa opzione è riservata per uso interno e non deve essere chiamata.</span><span class="sxs-lookup"><span data-stu-id="32223-502">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-503"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_aggiornamento dell'opzione WinHTTP \_ \_ a \_ Web \_ socket**</span><span class="sxs-lookup"><span data-stu-id="32223-503"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-504">Indica allo stack di avviare un processo di handshake WebSocket con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="32223-504">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="32223-505">Questa opzione non accetta parametri.</span><span class="sxs-lookup"><span data-stu-id="32223-505">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-506"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_URL opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-506"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-507">Recupera un valore stringa che contiene l'URL completo di una risorsa scaricata.</span><span class="sxs-lookup"><span data-stu-id="32223-507">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="32223-508">Se l'URL originale contiene dati aggiuntivi, ad esempio stringhe di ricerca o ancoraggi, oppure se la chiamata è stata reindirizzata, l'URL restituito è diverso dall'originale.</span><span class="sxs-lookup"><span data-stu-id="32223-508">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="32223-509">L'applicazione deve passare un buffer, ridimensionato in byte, sufficientemente grande da mantenere l'URL restituito in caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="32223-509">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-510"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_opzione WinHTTP \_ usare \_ le \_ credenziali del server globale \_**</span><span class="sxs-lookup"><span data-stu-id="32223-510"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-511">Accetta un **bool** e può essere impostato solo un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="32223-511">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="32223-512">Si propagherà solo fino a handle creati dall'handle di sessione dopo che l'opzione è stata impostata.</span><span class="sxs-lookup"><span data-stu-id="32223-512">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="32223-513">Se **true**, questa opzione determina come ultima risorsa l'uso delle credenziali del server globale da WinInet.</span><span class="sxs-lookup"><span data-stu-id="32223-513">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="32223-514">Il valore predefinito per questa opzione è **false**.</span><span class="sxs-lookup"><span data-stu-id="32223-514">The default for this option is **FALSE**.</span></span> <span data-ttu-id="32223-515">Questa opzione richiede la chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings. ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="32223-515">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="32223-516">Questa chiave del registro di sistema non è presente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="32223-516">This registry key is not present by default.</span></span> <span data-ttu-id="32223-517">Quando è impostato, WinINet invierà le credenziali a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="32223-517">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="32223-518">Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono state impostate credenziali sull'handle corrente, utilizzerà le credenziali fornite da WinINet.</span><span class="sxs-lookup"><span data-stu-id="32223-518">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-519"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_ \_ agente utente opzione \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-519"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-520">Imposta o recupera la stringa dell' [*agente utente*](glossary.md) negli handle forniti da [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) e usata nelle funzioni [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) successive, purché non venga sottoposta a override da un'intestazione aggiunta da [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) o **WinHttpSendRequest**.</span><span class="sxs-lookup"><span data-stu-id="32223-520">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="32223-521">Quando si recupera un agente utente, l'applicazione deve passare un buffer, ridimensionato in byte, che è sufficientemente grande da mantenere l'URL restituito in caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="32223-521">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="32223-522">Quando si imposta l'agente utente, le dimensioni del buffer corrispondono alla lunghezza della stringa, in caratteri, e al carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="32223-522">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-523"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_ \_ nome utente opzione WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-523"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-524">Imposta o Recupera una stringa che contiene il nome utente.</span><span class="sxs-lookup"><span data-stu-id="32223-524">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-525"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_timeout di \_ chiusura di Web \_ socket \_ \_ per l'opzione WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-525"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-526">Imposta il tempo, in millisecondi, che [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) deve attendere per completare l'handshake di chiusura.</span><span class="sxs-lookup"><span data-stu-id="32223-526">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="32223-527">Il valore predefinito è 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="32223-527">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-528"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_ \_ \_ \_ intervallo KeepAlive di Web socket per l'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-528"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-529">Imposta l'intervallo, in millisecondi, per l'invio di un pacchetto Keep-Alive sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="32223-529">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="32223-530">L'intervallo predefinito è 30000 (30 secondi).</span><span class="sxs-lookup"><span data-stu-id="32223-530">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="32223-531">L'intervallo minimo è 15000 (15 secondi).</span><span class="sxs-lookup"><span data-stu-id="32223-531">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="32223-532">Se si utilizza [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per impostare un valore inferiore a 15000, verrà restituito con **errore \_ \_ parametro non valido**.</span><span class="sxs-lookup"><span data-stu-id="32223-532">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="32223-533">Il valore predefinito per **l' \_ \_ intervallo di Web \_ socket \_ KeepAlive \_ dell'opzione WinHTTP** viene letto da **HKLM: \\ software \\ Microsoft \\ WebSocket \\ keepAliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="32223-533">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="32223-534">Se non è impostato alcun valore, verrà utilizzato il valore predefinito 30000.</span><span class="sxs-lookup"><span data-stu-id="32223-534">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="32223-535">Non è possibile avere un intervallo di KeepAlive inferiore a 15000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="32223-535">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-536"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**\_dimensioni del \_ \_ buffer di \_ ricezione \_ dell' \_ opzione WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-536"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-537">Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di ricezione da usare nelle connessioni WebSocket.</span><span class="sxs-lookup"><span data-stu-id="32223-537">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-538"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**\_dimensioni del \_ \_ buffer di invio del socket Web \_ \_ dell'opzione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-538"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-539">Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di invio da usare nelle connessioni WebSocket.</span><span class="sxs-lookup"><span data-stu-id="32223-539">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-540"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_ \_ conteggio thread di lavoro opzione \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-540"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-541">Imposta un valore long integer senza segno che specifica il numero di thread di lavoro che il pool di thread deve usare per i completamenti asincroni.</span><span class="sxs-lookup"><span data-stu-id="32223-541">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="32223-542">Il valore predefinito di questa opzione è zero, che specifica che il numero di thread di lavoro è uguale al numero di CPU nel sistema.</span><span class="sxs-lookup"><span data-stu-id="32223-542">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="32223-543">Questa opzione può essere impostata solo su un handle [HINTERNET](hinternet-handles-in-winhttp.md) **null** prima che si verifichi un'operazione asincrona.  </span><span class="sxs-lookup"><span data-stu-id="32223-543">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="32223-544">Questa opzione può essere impostata solo una volta.</span><span class="sxs-lookup"><span data-stu-id="32223-544">This option can only be set once.</span></span>

<span data-ttu-id="32223-545">**Windows Server 2008 R2 e Windows 7:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="32223-545">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32223-546"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_dimensioni del \_ buffer di scrittura dell'opzione WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="32223-546"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="32223-547">Questa opzione è stata deprecata. non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="32223-547">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32223-548">Commenti</span><span class="sxs-lookup"><span data-stu-id="32223-548">Remarks</span></span>

<span data-ttu-id="32223-549">Nella tabella seguente sono elencati i flag di opzione specificando gli handle su cui possono agire, se è possibile eseguire query e impostare e il tipo di dati utilizzato.</span><span class="sxs-lookup"><span data-stu-id="32223-549">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="32223-550">Una "X" indica che il flag di opzione è valido per l'uso con la funzione o l'handle, mentre un "-" specifica che il flag di opzione non è valido.</span><span class="sxs-lookup"><span data-stu-id="32223-550">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="32223-551">Se si tenta di impostare o eseguire una query su un flag di opzione in una versione di Windows in cui non è supportata, l' **\_ \_ \_ opzione errore WinHTTP non sarà valida**.</span><span class="sxs-lookup"><span data-stu-id="32223-551">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="32223-552">Flag di opzione e tipo di dati</span><span class="sxs-lookup"><span data-stu-id="32223-552">Option flag, and data type</span></span> | <span data-ttu-id="32223-553">Handle di sessione</span><span class="sxs-lookup"><span data-stu-id="32223-553">Session handle</span></span> | <span data-ttu-id="32223-554">Handle di richiesta</span><span class="sxs-lookup"><span data-stu-id="32223-554">Request handle</span></span> | <span data-ttu-id="32223-555">Opzione di query</span><span class="sxs-lookup"><span data-stu-id="32223-555">Query option</span></span> | <span data-ttu-id="32223-556">Opzione SET</span><span class="sxs-lookup"><span data-stu-id="32223-556">Set option</span></span> | <span data-ttu-id="32223-557">Versione minima di Windows</span><span class="sxs-lookup"><span data-stu-id="32223-557">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="32223-558">l' \_ opzione WinHTTP ha \_ assicurato \_ \_ callback non bloccanti \_</span><span class="sxs-lookup"><span data-stu-id="32223-558">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="32223-559">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-559">**BOOL**</span></span> | <span data-ttu-id="32223-560">X</span><span class="sxs-lookup"><span data-stu-id="32223-560">X</span></span> | \- | \- | <span data-ttu-id="32223-561">X</span><span class="sxs-lookup"><span data-stu-id="32223-561">X</span></span> | \- |
| <span data-ttu-id="32223-562">criteri di accesso \_ automatico opzione WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="32223-562">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="32223-563">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-563">**DWORD**</span></span> | \- | <span data-ttu-id="32223-564">X</span><span class="sxs-lookup"><span data-stu-id="32223-564">X</span></span> | \- | <span data-ttu-id="32223-565">X</span><span class="sxs-lookup"><span data-stu-id="32223-565">X</span></span> | \- |
| <span data-ttu-id="32223-566">\_callback di opzioni WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-566">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="32223-567">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="32223-567">**LPVOID**</span></span> | <span data-ttu-id="32223-568">X</span><span class="sxs-lookup"><span data-stu-id="32223-568">X</span></span> | <span data-ttu-id="32223-569">X</span><span class="sxs-lookup"><span data-stu-id="32223-569">X</span></span> | <span data-ttu-id="32223-570">X</span><span class="sxs-lookup"><span data-stu-id="32223-570">X</span></span> | <span data-ttu-id="32223-571">X</span><span class="sxs-lookup"><span data-stu-id="32223-571">X</span></span> | \- |
| <span data-ttu-id="32223-572">\_contesto del \_ \_ certificato client dell'opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-572">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="32223-573">**contesto del certificato \_**</span><span class="sxs-lookup"><span data-stu-id="32223-573">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="32223-574">X</span><span class="sxs-lookup"><span data-stu-id="32223-574">X</span></span> | \- | <span data-ttu-id="32223-575">X</span><span class="sxs-lookup"><span data-stu-id="32223-575">X</span></span> | <span data-ttu-id="32223-576">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32223-576">Windows Vista</span></span> |
| <span data-ttu-id="32223-577">\_elenco di \_ \_ \_ autorità emittenti del certificato client dell'opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-577">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="32223-578">**\_IssuerListInfoEx SecPkgContext**</span><span class="sxs-lookup"><span data-stu-id="32223-578">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="32223-579">X</span><span class="sxs-lookup"><span data-stu-id="32223-579">X</span></span> | <span data-ttu-id="32223-580">X</span><span class="sxs-lookup"><span data-stu-id="32223-580">X</span></span> | \- | <span data-ttu-id="32223-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32223-581">Windows Vista</span></span> |
| <span data-ttu-id="32223-582">opzione WINHTTP-tabella \_ \_ codici</span><span class="sxs-lookup"><span data-stu-id="32223-582">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="32223-583">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-583">**DWORD**</span></span> | <span data-ttu-id="32223-584">X</span><span class="sxs-lookup"><span data-stu-id="32223-584">X</span></span> | \- | \- | <span data-ttu-id="32223-585">X</span><span class="sxs-lookup"><span data-stu-id="32223-585">X</span></span> | \- |
| <span data-ttu-id="32223-586">\_opzione WinHTTP \_ Configure \_ Passport \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="32223-586">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="32223-587">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-587">**DWORD**</span></span> | <span data-ttu-id="32223-588">X</span><span class="sxs-lookup"><span data-stu-id="32223-588">X</span></span> | \- | \- | <span data-ttu-id="32223-589">X</span><span class="sxs-lookup"><span data-stu-id="32223-589">X</span></span> | \- |
| <span data-ttu-id="32223-590">\_tentativi di \_ connessione dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-590">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="32223-591">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-591">**DWORD**</span></span> | <span data-ttu-id="32223-592">X</span><span class="sxs-lookup"><span data-stu-id="32223-592">X</span></span> | <span data-ttu-id="32223-593">X</span><span class="sxs-lookup"><span data-stu-id="32223-593">X</span></span> | <span data-ttu-id="32223-594">X</span><span class="sxs-lookup"><span data-stu-id="32223-594">X</span></span> | <span data-ttu-id="32223-595">X</span><span class="sxs-lookup"><span data-stu-id="32223-595">X</span></span> | \- |
| <span data-ttu-id="32223-596">\_ \_ timeout connessione opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-596">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="32223-597">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-597">**DWORD**</span></span> | <span data-ttu-id="32223-598">X</span><span class="sxs-lookup"><span data-stu-id="32223-598">X</span></span> | <span data-ttu-id="32223-599">X</span><span class="sxs-lookup"><span data-stu-id="32223-599">X</span></span> | <span data-ttu-id="32223-600">X</span><span class="sxs-lookup"><span data-stu-id="32223-600">X</span></span> | <span data-ttu-id="32223-601">X</span><span class="sxs-lookup"><span data-stu-id="32223-601">X</span></span> | \- |
| <span data-ttu-id="32223-602">\_informazioni di \_ connessione dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-602">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="32223-603">**\_informazioni di connessione WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-603">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="32223-604">X</span><span class="sxs-lookup"><span data-stu-id="32223-604">X</span></span> | <span data-ttu-id="32223-605">X</span><span class="sxs-lookup"><span data-stu-id="32223-605">X</span></span> | \- | \- |
| <span data-ttu-id="32223-606">\_Opzioni WinHTTP \_ connessione \_ statistiche \_ V0</span><span class="sxs-lookup"><span data-stu-id="32223-606">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="32223-607">**\_Informazioni TCP \_ V0**</span><span class="sxs-lookup"><span data-stu-id="32223-607">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="32223-608">X</span><span class="sxs-lookup"><span data-stu-id="32223-608">X</span></span> | <span data-ttu-id="32223-609">X</span><span class="sxs-lookup"><span data-stu-id="32223-609">X</span></span> | \- | <span data-ttu-id="32223-610">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="32223-610">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="32223-611">\_Opzioni WinHTTP \_ connessione \_ statistiche \_ V1</span><span class="sxs-lookup"><span data-stu-id="32223-611">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="32223-612">**\_Informazioni TCP \_ V1**</span><span class="sxs-lookup"><span data-stu-id="32223-612">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="32223-613">X</span><span class="sxs-lookup"><span data-stu-id="32223-613">X</span></span> | <span data-ttu-id="32223-614">X</span><span class="sxs-lookup"><span data-stu-id="32223-614">X</span></span> | \- | <span data-ttu-id="32223-615">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="32223-615">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="32223-616">\_valore del \_ contesto dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-616">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="32223-617">**\_ptr DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-617">**DWORD\_PTR**</span></span> | <span data-ttu-id="32223-618">X</span><span class="sxs-lookup"><span data-stu-id="32223-618">X</span></span> | <span data-ttu-id="32223-619">X</span><span class="sxs-lookup"><span data-stu-id="32223-619">X</span></span> | <span data-ttu-id="32223-620">X</span><span class="sxs-lookup"><span data-stu-id="32223-620">X</span></span> | <span data-ttu-id="32223-621">X</span><span class="sxs-lookup"><span data-stu-id="32223-621">X</span></span> | \- |
| <span data-ttu-id="32223-622">decompressione dell' \_ opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-622">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="32223-623">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-623">**DWORD**</span></span> | <span data-ttu-id="32223-624">X</span><span class="sxs-lookup"><span data-stu-id="32223-624">X</span></span> | <span data-ttu-id="32223-625">X</span><span class="sxs-lookup"><span data-stu-id="32223-625">X</span></span> | \- | <span data-ttu-id="32223-626">X</span><span class="sxs-lookup"><span data-stu-id="32223-626">X</span></span> | <span data-ttu-id="32223-627">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="32223-627">Windows 8.1</span></span> |
| <span data-ttu-id="32223-628">\_funzionalità di \_ disabilitazione dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-628">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="32223-629">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-629">**DWORD**</span></span> | \- | <span data-ttu-id="32223-630">X</span><span class="sxs-lookup"><span data-stu-id="32223-630">X</span></span> | \- | <span data-ttu-id="32223-631">X</span><span class="sxs-lookup"><span data-stu-id="32223-631">X</span></span> | \- |
| <span data-ttu-id="32223-632">\_opzione WinHTTP \_ disabilitare \_ il \_ fallback del protocollo sicuro \_</span><span class="sxs-lookup"><span data-stu-id="32223-632">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="32223-633">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-633">**BOOL**</span></span> | <span data-ttu-id="32223-634">X</span><span class="sxs-lookup"><span data-stu-id="32223-634">X</span></span> | \- | \- | <span data-ttu-id="32223-635">X</span><span class="sxs-lookup"><span data-stu-id="32223-635">X</span></span> | <span data-ttu-id="32223-636">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="32223-636">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="32223-637">\_opzione WinHTTP \_ disabilitare \_ la \_ coda di flusso</span><span class="sxs-lookup"><span data-stu-id="32223-637">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="32223-638">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-638">**BOOL**</span></span> | <span data-ttu-id="32223-639">X</span><span class="sxs-lookup"><span data-stu-id="32223-639">X</span></span> | <span data-ttu-id="32223-640">X</span><span class="sxs-lookup"><span data-stu-id="32223-640">X</span></span> | \- | <span data-ttu-id="32223-641">X</span><span class="sxs-lookup"><span data-stu-id="32223-641">X</span></span> | <span data-ttu-id="32223-642">Windows 10 versione 1809</span><span class="sxs-lookup"><span data-stu-id="32223-642">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="32223-643">\_funzionalità di \_ Abilitazione dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-643">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="32223-644">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-644">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="32223-645">X</span><span class="sxs-lookup"><span data-stu-id="32223-645">X</span></span> | \- |
| <span data-ttu-id="32223-646">\_opzione WinHTTP \_ Abilita \_ \_ protocollo http</span><span class="sxs-lookup"><span data-stu-id="32223-646">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="32223-647">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-647">**DWORD**</span></span> | <span data-ttu-id="32223-648">X</span><span class="sxs-lookup"><span data-stu-id="32223-648">X</span></span> | <span data-ttu-id="32223-649">X</span><span class="sxs-lookup"><span data-stu-id="32223-649">X</span></span> | \- | <span data-ttu-id="32223-650">X</span><span class="sxs-lookup"><span data-stu-id="32223-650">X</span></span> | <span data-ttu-id="32223-651">Windows 10 versione 1607</span><span class="sxs-lookup"><span data-stu-id="32223-651">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="32223-652">\_opzione WinHTTP \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="32223-652">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="32223-653">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-653">**DWORD**</span></span> | \- | \- | <span data-ttu-id="32223-654">X</span><span class="sxs-lookup"><span data-stu-id="32223-654">X</span></span> | <span data-ttu-id="32223-655">X</span><span class="sxs-lookup"><span data-stu-id="32223-655">X</span></span> | \- |
| <span data-ttu-id="32223-656">\_opzione WinHTTP \_ Encode \_ extra</span><span class="sxs-lookup"><span data-stu-id="32223-656">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="32223-657">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-657">**BOOL**</span></span> | <span data-ttu-id="32223-658">X</span><span class="sxs-lookup"><span data-stu-id="32223-658">X</span></span> | <span data-ttu-id="32223-659">X</span><span class="sxs-lookup"><span data-stu-id="32223-659">X</span></span> | \- | <span data-ttu-id="32223-660">X</span><span class="sxs-lookup"><span data-stu-id="32223-660">X</span></span> | <span data-ttu-id="32223-661">Windows 10 versione 1803</span><span class="sxs-lookup"><span data-stu-id="32223-661">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="32223-662">\_ \_ errore esteso dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-662">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="32223-663">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-663">**DWORD**</span></span> | <span data-ttu-id="32223-664">X</span><span class="sxs-lookup"><span data-stu-id="32223-664">X</span></span> | <span data-ttu-id="32223-665">X</span><span class="sxs-lookup"><span data-stu-id="32223-665">X</span></span> | <span data-ttu-id="32223-666">X</span><span class="sxs-lookup"><span data-stu-id="32223-666">X</span></span> | \- | \- |
| <span data-ttu-id="32223-667">\_opzione WinHTTP \_ \_ proxy globale \_ credenziali</span><span class="sxs-lookup"><span data-stu-id="32223-667">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="32223-668">**\_credenziali WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-668">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="32223-669">X</span><span class="sxs-lookup"><span data-stu-id="32223-669">X</span></span> | <span data-ttu-id="32223-670">X</span><span class="sxs-lookup"><span data-stu-id="32223-670">X</span></span> | \- | <span data-ttu-id="32223-671">X</span><span class="sxs-lookup"><span data-stu-id="32223-671">X</span></span> | \- |
| <span data-ttu-id="32223-672">\_opzione WinHTTP \_ \_ server globale \_ credenziali</span><span class="sxs-lookup"><span data-stu-id="32223-672">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="32223-673">**WINHTTP \_ credenziali \_ ex**</span><span class="sxs-lookup"><span data-stu-id="32223-673">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="32223-674">X</span><span class="sxs-lookup"><span data-stu-id="32223-674">X</span></span> | <span data-ttu-id="32223-675">X</span><span class="sxs-lookup"><span data-stu-id="32223-675">X</span></span> | \- | <span data-ttu-id="32223-676">X</span><span class="sxs-lookup"><span data-stu-id="32223-676">X</span></span> | \- |
| <span data-ttu-id="32223-677">\_tipo di \_ handle dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-677">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="32223-678">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-678">**DWORD**</span></span> | <span data-ttu-id="32223-679">X</span><span class="sxs-lookup"><span data-stu-id="32223-679">X</span></span> | <span data-ttu-id="32223-680">X</span><span class="sxs-lookup"><span data-stu-id="32223-680">X</span></span> | <span data-ttu-id="32223-681">X</span><span class="sxs-lookup"><span data-stu-id="32223-681">X</span></span> | \- | \- |
| <span data-ttu-id="32223-682">il \_ protocollo HTTP dell'opzione WinHTTP è \_ \_ \_ obbligatorio</span><span class="sxs-lookup"><span data-stu-id="32223-682">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="32223-683">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-683">**BOOL**</span></span> | <span data-ttu-id="32223-684">X</span><span class="sxs-lookup"><span data-stu-id="32223-684">X</span></span> | <span data-ttu-id="32223-685">X</span><span class="sxs-lookup"><span data-stu-id="32223-685">X</span></span> | \- | <span data-ttu-id="32223-686">X</span><span class="sxs-lookup"><span data-stu-id="32223-686">X</span></span> | <span data-ttu-id="32223-687">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="32223-687">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="32223-688">\_opzione WinHTTP \_ \_ protocollo http \_ usato</span><span class="sxs-lookup"><span data-stu-id="32223-688">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="32223-689">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-689">**DWORD**</span></span> | \- | <span data-ttu-id="32223-690">X</span><span class="sxs-lookup"><span data-stu-id="32223-690">X</span></span> | <span data-ttu-id="32223-691">X</span><span class="sxs-lookup"><span data-stu-id="32223-691">X</span></span> | \- | <span data-ttu-id="32223-692">Windows 10 versione 1607</span><span class="sxs-lookup"><span data-stu-id="32223-692">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="32223-693">\_opzione WinHTTP \_ \_ versione http</span><span class="sxs-lookup"><span data-stu-id="32223-693">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="32223-694">**\_informazioni sulla versione http \_**</span><span class="sxs-lookup"><span data-stu-id="32223-694">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="32223-695">X</span><span class="sxs-lookup"><span data-stu-id="32223-695">X</span></span> | <span data-ttu-id="32223-696">X</span><span class="sxs-lookup"><span data-stu-id="32223-696">X</span></span> | <span data-ttu-id="32223-697">X</span><span class="sxs-lookup"><span data-stu-id="32223-697">X</span></span> | <span data-ttu-id="32223-698">X</span><span class="sxs-lookup"><span data-stu-id="32223-698">X</span></span> | \- |
| <span data-ttu-id="32223-699">\_opzione WinHTTP \_ ignorare la revoca del \_ certificato \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="32223-699">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="32223-700">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-700">**BOOL**</span></span> | \- | <span data-ttu-id="32223-701">X</span><span class="sxs-lookup"><span data-stu-id="32223-701">X</span></span> | \- | <span data-ttu-id="32223-702">X</span><span class="sxs-lookup"><span data-stu-id="32223-702">X</span></span> | <span data-ttu-id="32223-703">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="32223-703">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="32223-704">\_Opzione WinHTTP \_ - \_ fallback rapido IPv6 \_</span><span class="sxs-lookup"><span data-stu-id="32223-704">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="32223-705">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-705">**BOOL**</span></span> | <span data-ttu-id="32223-706">X</span><span class="sxs-lookup"><span data-stu-id="32223-706">X</span></span> | \- | \- | <span data-ttu-id="32223-707">X</span><span class="sxs-lookup"><span data-stu-id="32223-707">X</span></span> | <span data-ttu-id="32223-708">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="32223-708">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="32223-709">l' \_ opzione WinHTTP \_ è la \_ risposta di \_ connessione proxy \_</span><span class="sxs-lookup"><span data-stu-id="32223-709">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="32223-710">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-710">**BOOL**</span></span> | <span data-ttu-id="32223-711">X</span><span class="sxs-lookup"><span data-stu-id="32223-711">X</span></span> | <span data-ttu-id="32223-712">X</span><span class="sxs-lookup"><span data-stu-id="32223-712">X</span></span> | <span data-ttu-id="32223-713">X</span><span class="sxs-lookup"><span data-stu-id="32223-713">X</span></span> | \- | \- |
| <span data-ttu-id="32223-714">\_Opzione WinHTTP \_ numero massimo di \_ conn \_ per \_ \_ Server 1 0 \_</span><span class="sxs-lookup"><span data-stu-id="32223-714">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="32223-715">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-715">**DWORD**</span></span> | <span data-ttu-id="32223-716">X</span><span class="sxs-lookup"><span data-stu-id="32223-716">X</span></span> | \- | <span data-ttu-id="32223-717">X</span><span class="sxs-lookup"><span data-stu-id="32223-717">X</span></span> | <span data-ttu-id="32223-718">X</span><span class="sxs-lookup"><span data-stu-id="32223-718">X</span></span> | \- |
| <span data-ttu-id="32223-719">\_opzione WinHTTP \_ numero massimo di \_ conn \_ per \_ Server</span><span class="sxs-lookup"><span data-stu-id="32223-719">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="32223-720">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-720">**DWORD**</span></span> | <span data-ttu-id="32223-721">X</span><span class="sxs-lookup"><span data-stu-id="32223-721">X</span></span> | \- | <span data-ttu-id="32223-722">X</span><span class="sxs-lookup"><span data-stu-id="32223-722">X</span></span> | <span data-ttu-id="32223-723">X</span><span class="sxs-lookup"><span data-stu-id="32223-723">X</span></span> | \- |
| <span data-ttu-id="32223-724">\_opzione WinHTTP \_ numero massimo di \_ \_ \_ reindirizzamenti automatici http</span><span class="sxs-lookup"><span data-stu-id="32223-724">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="32223-725">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-725">**DWORD**</span></span> | <span data-ttu-id="32223-726">X</span><span class="sxs-lookup"><span data-stu-id="32223-726">X</span></span> | <span data-ttu-id="32223-727">X</span><span class="sxs-lookup"><span data-stu-id="32223-727">X</span></span> | <span data-ttu-id="32223-728">X</span><span class="sxs-lookup"><span data-stu-id="32223-728">X</span></span> | <span data-ttu-id="32223-729">X</span><span class="sxs-lookup"><span data-stu-id="32223-729">X</span></span> | \- |
| <span data-ttu-id="32223-730">\_opzione WinHTTP \_ numero \_ massimo \_ stato http \_ continua</span><span class="sxs-lookup"><span data-stu-id="32223-730">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="32223-731">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-731">**DWORD**</span></span> | <span data-ttu-id="32223-732">X</span><span class="sxs-lookup"><span data-stu-id="32223-732">X</span></span> | <span data-ttu-id="32223-733">X</span><span class="sxs-lookup"><span data-stu-id="32223-733">X</span></span> | <span data-ttu-id="32223-734">X</span><span class="sxs-lookup"><span data-stu-id="32223-734">X</span></span> | <span data-ttu-id="32223-735">X</span><span class="sxs-lookup"><span data-stu-id="32223-735">X</span></span> | \- |
| <span data-ttu-id="32223-736">\_ \_ dimensioni massime \_ \_ svuotamento risposta \_ opzione WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-736">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="32223-737">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-737">**DWORD**</span></span> | <span data-ttu-id="32223-738">X</span><span class="sxs-lookup"><span data-stu-id="32223-738">X</span></span> | <span data-ttu-id="32223-739">X</span><span class="sxs-lookup"><span data-stu-id="32223-739">X</span></span> | <span data-ttu-id="32223-740">X</span><span class="sxs-lookup"><span data-stu-id="32223-740">X</span></span> | <span data-ttu-id="32223-741">X</span><span class="sxs-lookup"><span data-stu-id="32223-741">X</span></span> | \- |
| <span data-ttu-id="32223-742">\_ \_ dimensioni massime \_ \_ intestazione risposta \_ opzione WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-742">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="32223-743">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-743">**DWORD**</span></span> | <span data-ttu-id="32223-744">X</span><span class="sxs-lookup"><span data-stu-id="32223-744">X</span></span> | <span data-ttu-id="32223-745">X</span><span class="sxs-lookup"><span data-stu-id="32223-745">X</span></span> | <span data-ttu-id="32223-746">X</span><span class="sxs-lookup"><span data-stu-id="32223-746">X</span></span> | <span data-ttu-id="32223-747">X</span><span class="sxs-lookup"><span data-stu-id="32223-747">X</span></span> | \- |
| <span data-ttu-id="32223-748">\_ \_ handle padre dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-748">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="32223-749">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="32223-749">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="32223-750">X</span><span class="sxs-lookup"><span data-stu-id="32223-750">X</span></span> | <span data-ttu-id="32223-751">X</span><span class="sxs-lookup"><span data-stu-id="32223-751">X</span></span> | <span data-ttu-id="32223-752">X</span><span class="sxs-lookup"><span data-stu-id="32223-752">X</span></span> | \- | \- |
| <span data-ttu-id="32223-753">testo per la personalizzazione dell' \_ opzione WinHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="32223-753">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="32223-754">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-754">**LPWSTR**</span></span> | \- | <span data-ttu-id="32223-755">X</span><span class="sxs-lookup"><span data-stu-id="32223-755">X</span></span> | <span data-ttu-id="32223-756">X</span><span class="sxs-lookup"><span data-stu-id="32223-756">X</span></span> | \- | \- |
| <span data-ttu-id="32223-757">\_URL di \_ \_ copersonalizzazione dell'opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-757">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="32223-758">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-758">**LPWSTR**</span></span> | \- | <span data-ttu-id="32223-759">X</span><span class="sxs-lookup"><span data-stu-id="32223-759">X</span></span> | <span data-ttu-id="32223-760">X</span><span class="sxs-lookup"><span data-stu-id="32223-760">X</span></span> | \- | \- |
| <span data-ttu-id="32223-761">\_opzione WinHTTP \_ - \_ URL restituito Passport \_</span><span class="sxs-lookup"><span data-stu-id="32223-761">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="32223-762">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="32223-762">**LPVOID**</span></span> | \- | <span data-ttu-id="32223-763">X</span><span class="sxs-lookup"><span data-stu-id="32223-763">X</span></span> | <span data-ttu-id="32223-764">X</span><span class="sxs-lookup"><span data-stu-id="32223-764">X</span></span> | \- | \- |
| <span data-ttu-id="32223-765">\_opzione WinHTTP \_ - \_ disconnessione Passport \_</span><span class="sxs-lookup"><span data-stu-id="32223-765">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="32223-766">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="32223-766">**LPVOID**</span></span> | <span data-ttu-id="32223-767">X</span><span class="sxs-lookup"><span data-stu-id="32223-767">X</span></span> | \- | \- | <span data-ttu-id="32223-768">X</span><span class="sxs-lookup"><span data-stu-id="32223-768">X</span></span> | \- |
| <span data-ttu-id="32223-769">\_password opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-769">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="32223-770">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-770">**LPWSTR**</span></span> | \- | <span data-ttu-id="32223-771">X</span><span class="sxs-lookup"><span data-stu-id="32223-771">X</span></span> | <span data-ttu-id="32223-772">X</span><span class="sxs-lookup"><span data-stu-id="32223-772">X</span></span> | <span data-ttu-id="32223-773">X</span><span class="sxs-lookup"><span data-stu-id="32223-773">X</span></span> | \- |
| <span data-ttu-id="32223-774">\_proxy dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-774">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="32223-775">**\_informazioni proxy \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="32223-775">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="32223-776">X</span><span class="sxs-lookup"><span data-stu-id="32223-776">X</span></span> | <span data-ttu-id="32223-777">X</span><span class="sxs-lookup"><span data-stu-id="32223-777">X</span></span> | <span data-ttu-id="32223-778">X</span><span class="sxs-lookup"><span data-stu-id="32223-778">X</span></span> | <span data-ttu-id="32223-779">X</span><span class="sxs-lookup"><span data-stu-id="32223-779">X</span></span> | \- |
| <span data-ttu-id="32223-780">\_ \_ password proxy opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-780">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="32223-781">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-781">**LPWSTR**</span></span> | \- | <span data-ttu-id="32223-782">X</span><span class="sxs-lookup"><span data-stu-id="32223-782">X</span></span> | <span data-ttu-id="32223-783">X</span><span class="sxs-lookup"><span data-stu-id="32223-783">X</span></span> | <span data-ttu-id="32223-784">X</span><span class="sxs-lookup"><span data-stu-id="32223-784">X</span></span> | \- |
| <span data-ttu-id="32223-785">\_SPN del proxy dell'opzione WinHTTP \_ \_ \_ usato</span><span class="sxs-lookup"><span data-stu-id="32223-785">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="32223-786">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-786">**LPWSTR**</span></span> | \- | <span data-ttu-id="32223-787">X</span><span class="sxs-lookup"><span data-stu-id="32223-787">X</span></span> | <span data-ttu-id="32223-788">X</span><span class="sxs-lookup"><span data-stu-id="32223-788">X</span></span> | \- | \- |
| <span data-ttu-id="32223-789">\_ \_ nome utente proxy opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-789">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="32223-790">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-790">**LPWSTR**</span></span> | \- | <span data-ttu-id="32223-791">X</span><span class="sxs-lookup"><span data-stu-id="32223-791">X</span></span> | <span data-ttu-id="32223-792">X</span><span class="sxs-lookup"><span data-stu-id="32223-792">X</span></span> | <span data-ttu-id="32223-793">X</span><span class="sxs-lookup"><span data-stu-id="32223-793">X</span></span> | \- |
| <span data-ttu-id="32223-794">\_dimensioni del \_ buffer di lettura dell'opzione WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="32223-794">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="32223-795">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-795">**DWORD**</span></span> | \- | <span data-ttu-id="32223-796">X</span><span class="sxs-lookup"><span data-stu-id="32223-796">X</span></span> | <span data-ttu-id="32223-797">X</span><span class="sxs-lookup"><span data-stu-id="32223-797">X</span></span> | <span data-ttu-id="32223-798">X</span><span class="sxs-lookup"><span data-stu-id="32223-798">X</span></span> | \- |
| <span data-ttu-id="32223-799">\_risposta di \_ \_ connessione proxy \_ di ricezione opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-799">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="32223-800">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-800">**BOOL**</span></span> | <span data-ttu-id="32223-801">X</span><span class="sxs-lookup"><span data-stu-id="32223-801">X</span></span> | <span data-ttu-id="32223-802">X</span><span class="sxs-lookup"><span data-stu-id="32223-802">X</span></span> | \- | <span data-ttu-id="32223-803">X</span><span class="sxs-lookup"><span data-stu-id="32223-803">X</span></span> | \- |
| <span data-ttu-id="32223-804">\_timeout di \_ \_ risposta ricezione opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-804">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="32223-805">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-805">**DWORD**</span></span> | <span data-ttu-id="32223-806">X</span><span class="sxs-lookup"><span data-stu-id="32223-806">X</span></span> | <span data-ttu-id="32223-807">X</span><span class="sxs-lookup"><span data-stu-id="32223-807">X</span></span> | <span data-ttu-id="32223-808">X</span><span class="sxs-lookup"><span data-stu-id="32223-808">X</span></span> | <span data-ttu-id="32223-809">X</span><span class="sxs-lookup"><span data-stu-id="32223-809">X</span></span> | \- |
| <span data-ttu-id="32223-810">\_timeout di \_ ricezione dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-810">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="32223-811">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-811">**DWORD**</span></span> | <span data-ttu-id="32223-812">X</span><span class="sxs-lookup"><span data-stu-id="32223-812">X</span></span> | <span data-ttu-id="32223-813">X</span><span class="sxs-lookup"><span data-stu-id="32223-813">X</span></span> | <span data-ttu-id="32223-814">X</span><span class="sxs-lookup"><span data-stu-id="32223-814">X</span></span> | <span data-ttu-id="32223-815">X</span><span class="sxs-lookup"><span data-stu-id="32223-815">X</span></span> | \- |
| <span data-ttu-id="32223-816">\_criteri di \_ Reindirizzamento \_ Opzioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-816">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="32223-817">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-817">**DWORD**</span></span> | <span data-ttu-id="32223-818">X</span><span class="sxs-lookup"><span data-stu-id="32223-818">X</span></span> | <span data-ttu-id="32223-819">X</span><span class="sxs-lookup"><span data-stu-id="32223-819">X</span></span> | <span data-ttu-id="32223-820">X</span><span class="sxs-lookup"><span data-stu-id="32223-820">X</span></span> | <span data-ttu-id="32223-821">X</span><span class="sxs-lookup"><span data-stu-id="32223-821">X</span></span> | \- |
| <span data-ttu-id="32223-822">\_opzione WinHTTP \_ rifiutare \_ USERPWD \_ nell' \_ URL</span><span class="sxs-lookup"><span data-stu-id="32223-822">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="32223-823">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-823">**BOOL**</span></span> | \- | <span data-ttu-id="32223-824">X</span><span class="sxs-lookup"><span data-stu-id="32223-824">X</span></span> | \- | <span data-ttu-id="32223-825">X</span><span class="sxs-lookup"><span data-stu-id="32223-825">X</span></span> | \- |
| <span data-ttu-id="32223-826">\_ \_ priorità richiesta opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-826">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="32223-827">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-827">**DWORD**</span></span> | \- | <span data-ttu-id="32223-828">X</span><span class="sxs-lookup"><span data-stu-id="32223-828">X</span></span> | <span data-ttu-id="32223-829">X</span><span class="sxs-lookup"><span data-stu-id="32223-829">X</span></span> | <span data-ttu-id="32223-830">X</span><span class="sxs-lookup"><span data-stu-id="32223-830">X</span></span> | \- |
| <span data-ttu-id="32223-831">\_statistiche delle \_ richieste di opzioni WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-831">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="32223-832">**\_statistiche della richiesta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-832">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="32223-833">X</span><span class="sxs-lookup"><span data-stu-id="32223-833">X</span></span> | <span data-ttu-id="32223-834">X</span><span class="sxs-lookup"><span data-stu-id="32223-834">X</span></span> | \- | <span data-ttu-id="32223-835">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="32223-835">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="32223-836">\_tempi di \_ richiesta dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-836">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="32223-837">**\_tempi di richiesta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-837">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="32223-838">X</span><span class="sxs-lookup"><span data-stu-id="32223-838">X</span></span> | <span data-ttu-id="32223-839">X</span><span class="sxs-lookup"><span data-stu-id="32223-839">X</span></span> | \- | <span data-ttu-id="32223-840">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="32223-840">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="32223-841">\_ \_ timeout risoluzione opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-841">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="32223-842">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-842">**DWORD**</span></span> | <span data-ttu-id="32223-843">X</span><span class="sxs-lookup"><span data-stu-id="32223-843">X</span></span> | <span data-ttu-id="32223-844">X</span><span class="sxs-lookup"><span data-stu-id="32223-844">X</span></span> | <span data-ttu-id="32223-845">X</span><span class="sxs-lookup"><span data-stu-id="32223-845">X</span></span> | <span data-ttu-id="32223-846">X</span><span class="sxs-lookup"><span data-stu-id="32223-846">X</span></span> | \- |
| <span data-ttu-id="32223-847">\_protocolli di \_ sicurezza delle opzioni WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-847">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="32223-848">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-848">**DWORD**</span></span> | <span data-ttu-id="32223-849">X</span><span class="sxs-lookup"><span data-stu-id="32223-849">X</span></span> | \- | \- | <span data-ttu-id="32223-850">X</span><span class="sxs-lookup"><span data-stu-id="32223-850">X</span></span> | \- |
| <span data-ttu-id="32223-851">\_ \_ struct certificato di sicurezza opzione \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-851">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="32223-852">**\_informazioni sul certificato WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="32223-852">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="32223-853">X</span><span class="sxs-lookup"><span data-stu-id="32223-853">X</span></span> | <span data-ttu-id="32223-854">X</span><span class="sxs-lookup"><span data-stu-id="32223-854">X</span></span> | \- | \- |
| <span data-ttu-id="32223-855">\_flag di \_ sicurezza delle opzioni WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-855">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="32223-856">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-856">**DWORD**</span></span> | \- | <span data-ttu-id="32223-857">X</span><span class="sxs-lookup"><span data-stu-id="32223-857">X</span></span> | <span data-ttu-id="32223-858">X</span><span class="sxs-lookup"><span data-stu-id="32223-858">X</span></span> | <span data-ttu-id="32223-859">X</span><span class="sxs-lookup"><span data-stu-id="32223-859">X</span></span> | \- |
| <span data-ttu-id="32223-860">\_informazioni di \_ sicurezza sull'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-860">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="32223-861">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="32223-861">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="32223-862">X</span><span class="sxs-lookup"><span data-stu-id="32223-862">X</span></span> | <span data-ttu-id="32223-863">X</span><span class="sxs-lookup"><span data-stu-id="32223-863">X</span></span> | \- | <span data-ttu-id="32223-864">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="32223-864">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="32223-865">\_chiave di sicurezza dell'opzione WinHTTP \_ \_ \_ bit</span><span class="sxs-lookup"><span data-stu-id="32223-865">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="32223-866">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-866">**DWORD**</span></span> | \- | <span data-ttu-id="32223-867">X</span><span class="sxs-lookup"><span data-stu-id="32223-867">X</span></span> | <span data-ttu-id="32223-868">X</span><span class="sxs-lookup"><span data-stu-id="32223-868">X</span></span> | \- | \- |
| <span data-ttu-id="32223-869">\_ \_ timeout invio opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-869">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="32223-870">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-870">**DWORD**</span></span> | <span data-ttu-id="32223-871">X</span><span class="sxs-lookup"><span data-stu-id="32223-871">X</span></span> | <span data-ttu-id="32223-872">X</span><span class="sxs-lookup"><span data-stu-id="32223-872">X</span></span> | <span data-ttu-id="32223-873">X</span><span class="sxs-lookup"><span data-stu-id="32223-873">X</span></span> | <span data-ttu-id="32223-874">X</span><span class="sxs-lookup"><span data-stu-id="32223-874">X</span></span> | \- |
| <span data-ttu-id="32223-875">\_Server opzioni \_ WinHTTP \_ CBT</span><span class="sxs-lookup"><span data-stu-id="32223-875">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="32223-876">[**\_Binding SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="32223-876">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="32223-877">X</span><span class="sxs-lookup"><span data-stu-id="32223-877">X</span></span> | <span data-ttu-id="32223-878">X</span><span class="sxs-lookup"><span data-stu-id="32223-878">X</span></span> | \- | \- |
| <span data-ttu-id="32223-879">\_ \_ \_ contesto catena di certificati \_ server \_ Opzioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-879">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="32223-880">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="32223-880">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="32223-881">X</span><span class="sxs-lookup"><span data-stu-id="32223-881">X</span></span> | <span data-ttu-id="32223-882">X</span><span class="sxs-lookup"><span data-stu-id="32223-882">X</span></span> | \- | <span data-ttu-id="32223-883">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="32223-883">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="32223-884">\_ \_ \_ contesto certificato server opzioni \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-884">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="32223-885">**CONTESTO DEL CERTIFICATO**</span><span class="sxs-lookup"><span data-stu-id="32223-885">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="32223-886">X</span><span class="sxs-lookup"><span data-stu-id="32223-886">X</span></span> | <span data-ttu-id="32223-887">X</span><span class="sxs-lookup"><span data-stu-id="32223-887">X</span></span> | \- | \- |
| <span data-ttu-id="32223-888">\_ \_ nome SPN Server opzioni WinHTTP \_ \_ usato</span><span class="sxs-lookup"><span data-stu-id="32223-888">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="32223-889">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-889">**LPWSTR**</span></span> | \- | <span data-ttu-id="32223-890">X</span><span class="sxs-lookup"><span data-stu-id="32223-890">X</span></span> | <span data-ttu-id="32223-891">X</span><span class="sxs-lookup"><span data-stu-id="32223-891">X</span></span> | \- | \- |
| <span data-ttu-id="32223-892">\_ \_ nome SPN opzione WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-892">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="32223-893">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-893">**DWORD**</span></span> | \- | <span data-ttu-id="32223-894">X</span><span class="sxs-lookup"><span data-stu-id="32223-894">X</span></span> | \- | <span data-ttu-id="32223-895">X</span><span class="sxs-lookup"><span data-stu-id="32223-895">X</span></span> | \- |
| <span data-ttu-id="32223-896">\_opzione WinHTTP \_ - \_ apertura rapida TCP \_</span><span class="sxs-lookup"><span data-stu-id="32223-896">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="32223-897">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-897">**BOOL**</span></span> | <span data-ttu-id="32223-898">X</span><span class="sxs-lookup"><span data-stu-id="32223-898">X</span></span> | \- | \- | <span data-ttu-id="32223-899">X</span><span class="sxs-lookup"><span data-stu-id="32223-899">X</span></span> | <span data-ttu-id="32223-900">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="32223-900">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="32223-901">opzione WINHTTP ( \_ \_ avvio) TLS \_ false \_</span><span class="sxs-lookup"><span data-stu-id="32223-901">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="32223-902">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-902">**BOOL**</span></span> | <span data-ttu-id="32223-903">X</span><span class="sxs-lookup"><span data-stu-id="32223-903">X</span></span> | \- | \- | <span data-ttu-id="32223-904">X</span><span class="sxs-lookup"><span data-stu-id="32223-904">X</span></span> | <span data-ttu-id="32223-905">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="32223-905">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="32223-906">\_evento di \_ scaricamento dell'opzione WinHTTP \_ Notify \_</span><span class="sxs-lookup"><span data-stu-id="32223-906">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="32223-907">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="32223-907">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="32223-908">X</span><span class="sxs-lookup"><span data-stu-id="32223-908">X</span></span> | \- | \- | <span data-ttu-id="32223-909">X</span><span class="sxs-lookup"><span data-stu-id="32223-909">X</span></span> | \- |
| <span data-ttu-id="32223-910">opzione WINHTTP- \_ \_ analisi dell'intestazione non sicura \_ \_</span><span class="sxs-lookup"><span data-stu-id="32223-910">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="32223-911">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-911">**DWORD**</span></span> | \- | <span data-ttu-id="32223-912">X</span><span class="sxs-lookup"><span data-stu-id="32223-912">X</span></span> | \- | <span data-ttu-id="32223-913">X</span><span class="sxs-lookup"><span data-stu-id="32223-913">X</span></span> | \- |
| <span data-ttu-id="32223-914">\_aggiornamento dell'opzione WinHTTP \_ \_ a \_ Web \_ socket</span><span class="sxs-lookup"><span data-stu-id="32223-914">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="32223-915">N/D</span><span class="sxs-lookup"><span data-stu-id="32223-915">N/A</span></span> | \- | <span data-ttu-id="32223-916">X</span><span class="sxs-lookup"><span data-stu-id="32223-916">X</span></span> | \- | <span data-ttu-id="32223-917">X</span><span class="sxs-lookup"><span data-stu-id="32223-917">X</span></span> | \- |
| <span data-ttu-id="32223-918">\_URL opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-918">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="32223-919">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-919">**LPWSTR**</span></span> | \- | <span data-ttu-id="32223-920">X</span><span class="sxs-lookup"><span data-stu-id="32223-920">X</span></span> | <span data-ttu-id="32223-921">X</span><span class="sxs-lookup"><span data-stu-id="32223-921">X</span></span> | \- | \- |
| <span data-ttu-id="32223-922">\_opzione WinHTTP \_ usare \_ le \_ credenziali del server globale \_</span><span class="sxs-lookup"><span data-stu-id="32223-922">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="32223-923">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="32223-923">**BOOL**</span></span> | <span data-ttu-id="32223-924">X</span><span class="sxs-lookup"><span data-stu-id="32223-924">X</span></span> | <span data-ttu-id="32223-925">X</span><span class="sxs-lookup"><span data-stu-id="32223-925">X</span></span> | \- | <span data-ttu-id="32223-926">X</span><span class="sxs-lookup"><span data-stu-id="32223-926">X</span></span> | \- |
| <span data-ttu-id="32223-927">\_ \_ agente utente opzione \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-927">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="32223-928">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-928">**LPWSTR**</span></span> | <span data-ttu-id="32223-929">X</span><span class="sxs-lookup"><span data-stu-id="32223-929">X</span></span> | \- | <span data-ttu-id="32223-930">X</span><span class="sxs-lookup"><span data-stu-id="32223-930">X</span></span> | <span data-ttu-id="32223-931">X</span><span class="sxs-lookup"><span data-stu-id="32223-931">X</span></span> | \- |
| <span data-ttu-id="32223-932">\_ \_ nome utente opzione WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-932">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="32223-933">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="32223-933">**LPWSTR**</span></span> | \- | <span data-ttu-id="32223-934">X</span><span class="sxs-lookup"><span data-stu-id="32223-934">X</span></span> | <span data-ttu-id="32223-935">X</span><span class="sxs-lookup"><span data-stu-id="32223-935">X</span></span> | <span data-ttu-id="32223-936">X</span><span class="sxs-lookup"><span data-stu-id="32223-936">X</span></span> | \- |
| <span data-ttu-id="32223-937">\_timeout di \_ chiusura di Web \_ socket \_ \_ per l'opzione WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-937">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="32223-938">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-938">**DWORD**</span></span> | \- | \- | <span data-ttu-id="32223-939">X</span><span class="sxs-lookup"><span data-stu-id="32223-939">X</span></span> | <span data-ttu-id="32223-940">X</span><span class="sxs-lookup"><span data-stu-id="32223-940">X</span></span> | \- |
| <span data-ttu-id="32223-941">\_ \_ \_ \_ intervallo KeepAlive di Web socket per l'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-941">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="32223-942">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-942">**DWORD**</span></span> | \- | \- | <span data-ttu-id="32223-943">X</span><span class="sxs-lookup"><span data-stu-id="32223-943">X</span></span> | <span data-ttu-id="32223-944">X</span><span class="sxs-lookup"><span data-stu-id="32223-944">X</span></span> | \- |
| <span data-ttu-id="32223-945">\_dimensioni del \_ \_ buffer di \_ ricezione \_ dell' \_ opzione WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-945">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="32223-946">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-946">**DWORD**</span></span> | <span data-ttu-id="32223-947">X</span><span class="sxs-lookup"><span data-stu-id="32223-947">X</span></span> | <span data-ttu-id="32223-948">X</span><span class="sxs-lookup"><span data-stu-id="32223-948">X</span></span> | <span data-ttu-id="32223-949">X</span><span class="sxs-lookup"><span data-stu-id="32223-949">X</span></span> | <span data-ttu-id="32223-950">X</span><span class="sxs-lookup"><span data-stu-id="32223-950">X</span></span> | <span data-ttu-id="32223-951">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="32223-951">Windows 8.1</span></span> |
| <span data-ttu-id="32223-952">\_dimensioni del \_ \_ buffer di invio del socket Web \_ \_ dell'opzione WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-952">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="32223-953">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-953">**DWORD**</span></span> | <span data-ttu-id="32223-954">X</span><span class="sxs-lookup"><span data-stu-id="32223-954">X</span></span> | <span data-ttu-id="32223-955">X</span><span class="sxs-lookup"><span data-stu-id="32223-955">X</span></span> | <span data-ttu-id="32223-956">X</span><span class="sxs-lookup"><span data-stu-id="32223-956">X</span></span> | <span data-ttu-id="32223-957">X</span><span class="sxs-lookup"><span data-stu-id="32223-957">X</span></span> | <span data-ttu-id="32223-958">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="32223-958">Windows 8.1</span></span> |
| <span data-ttu-id="32223-959">\_ \_ conteggio thread di lavoro opzione \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="32223-959">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="32223-960">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-960">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="32223-961">X</span><span class="sxs-lookup"><span data-stu-id="32223-961">X</span></span> | \- |
| <span data-ttu-id="32223-962">\_dimensioni del \_ buffer di scrittura dell'opzione WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="32223-962">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="32223-963">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32223-963">**DWORD**</span></span> | \- | <span data-ttu-id="32223-964">X</span><span class="sxs-lookup"><span data-stu-id="32223-964">X</span></span> | <span data-ttu-id="32223-965">X</span><span class="sxs-lookup"><span data-stu-id="32223-965">X</span></span> | <span data-ttu-id="32223-966">X</span><span class="sxs-lookup"><span data-stu-id="32223-966">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="32223-967">Per Windows XP e Windows 2000, vedere [requisiti di run-time](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="32223-967">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32223-968">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32223-968">Requirements</span></span>

| <span data-ttu-id="32223-969">Requisito</span><span class="sxs-lookup"><span data-stu-id="32223-969">Requirement</span></span> | <span data-ttu-id="32223-970">Valore</span><span class="sxs-lookup"><span data-stu-id="32223-970">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="32223-971">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32223-971">Minimum supported client</span></span> | <span data-ttu-id="32223-972">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="32223-972">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="32223-973">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32223-973">Minimum supported server</span></span> | <span data-ttu-id="32223-974">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="32223-974">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="32223-975">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="32223-975">Redistributable</span></span>          | <span data-ttu-id="32223-976">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="32223-976">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="32223-977">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32223-977">Header</span></span>                   | <span data-ttu-id="32223-978">WinHTTP. h</span><span class="sxs-lookup"><span data-stu-id="32223-978">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="32223-979">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32223-979">See also</span></span>

[<span data-ttu-id="32223-980">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="32223-980">WinHTTP Versions</span></span>](winhttp-versions.md)
