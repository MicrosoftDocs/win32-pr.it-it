---
Description: I flag di opzione seguenti sono supportati da WinHttpQueryOption e WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Flag di opzione (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 25049ee11c59c6b320b794c07bd65e5ec9b930c9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395416"
---
# <a name="option-flags"></a><span data-ttu-id="5829a-103">Flag di opzione</span><span class="sxs-lookup"><span data-stu-id="5829a-103">Option Flags</span></span>

<span data-ttu-id="5829a-104">I flag di opzione seguenti sono supportati [**da WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)</span><span class="sxs-lookup"><span data-stu-id="5829a-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="5829a-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**OPZIONE WINHTTP \_ \_ ASSICURATA \_ CALLBACK NON \_ \_ BLOCCANTI**</span><span class="sxs-lookup"><span data-stu-id="5829a-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-106">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="5829a-106">The default is FALSE.</span></span> <span data-ttu-id="5829a-107">Se impostato su TRUE, WinHTTP non garantisce lo stato di avanzamento se i callback di stato vengono bloccati dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="5829a-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="5829a-108">L'applicazione client deve eseguire operazioni minime all'interno del callback senza bloccarsi, restituire il più rapidamente possibile e, in particolare, non deve attendere le chiamate WinHTTP successive.</span><span class="sxs-lookup"><span data-stu-id="5829a-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="5829a-109">Se non segue queste linee guida, è probabile che si verifica un impatto negativo sulle prestazioni o un potenziale blocco dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5829a-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="5829a-110">Se usata nel modo prescritto, questa opzione può migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5829a-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**CRITERI DI \_ ACCESSO \_ AUTOMATICO DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-112">Imposta un valore long integer senza segno che specifica i criteri [di accesso automatico](authentication-in-winhttp.md) con uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5829a-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="5829a-113">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-113">Term</span></span> | <span data-ttu-id="5829a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-114">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>LIVELLO DI SICUREZZA DI ACCESSO AUTOMATICO WINHTTP \_ \_ \_ \_ ELEVATO</span><span class="sxs-lookup"><span data-stu-id="5829a-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="5829a-116">Le credenziali predefinite non vengono usate.</span><span class="sxs-lookup"><span data-stu-id="5829a-116">Default credentials are not used.</span></span> <span data-ttu-id="5829a-117">Si noti che questo flag ha effetto solo se si specifica il server in base al nome effettivo del computer.</span><span class="sxs-lookup"><span data-stu-id="5829a-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="5829a-118">Non avrà effetto se si specifica il server in base a "localhost" o all'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="5829a-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="5829a-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>LIVELLO DI \_ SICUREZZA WINHTTP AUTOLOGON \_ \_ \_ BASSO</span><span class="sxs-lookup"><span data-stu-id="5829a-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="5829a-120">Viene eseguito un accesso autenticato usando le credenziali predefinite per tutte le richieste.</span><span class="sxs-lookup"><span data-stu-id="5829a-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="5829a-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>LIVELLO DI SICUREZZA WINHTTP \_ AUTOLOGON \_ \_ \_ MEDIUM</span><span class="sxs-lookup"><span data-stu-id="5829a-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="5829a-122">Un accesso autenticato usando le credenziali predefinite viene eseguito solo per le richieste nella Intranet locale.</span><span class="sxs-lookup"><span data-stu-id="5829a-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="5829a-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**CONNESSIONI IN \_ BACKGROUND DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5829a-124">Quando si imposta questa opzione su un handle di sessione, è necessario passare il numero di connessioni da aprire.</span><span class="sxs-lookup"><span data-stu-id="5829a-124">When you set this option on a session handle, you must pass the number of connections you wish to open.</span></span> <span data-ttu-id="5829a-125">Quindi, al primo invio di una richiesta, anziché aprire una sola connessione, WinHttp apre una serie di connessioni in parallelo.</span><span class="sxs-lookup"><span data-stu-id="5829a-125">Then, upon first sending a request, rather than opening only a single connection, WinHttp opens a number of connections in parallel.</span></span> <span data-ttu-id="5829a-126">In questo modo è possibile migliorare le prestazioni delle richieste successive alla stessa destinazione, senza l'overhead della creazione della connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-126">This can improve the performance of subsequent requests to the same destination, which won't have the overhead of connection establishment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**CALLBACK \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-128">Recupera il puntatore al set di funzioni di callback [**con WinHttpSetStatusCallback.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)</span><span class="sxs-lookup"><span data-stu-id="5829a-128">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**CONTESTO CERTIFICATO \_ \_ CLIENT \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-130">Imposta il contesto del certificato client.</span><span class="sxs-lookup"><span data-stu-id="5829a-130">Sets the client certificate context.</span></span> <span data-ttu-id="5829a-131">Se un'applicazione riceve [**ERROR \_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED,**](error-messages.md)deve chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per fornire un certificato prima di ritentare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-131">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="5829a-132">Come parte dell'elaborazione di questa opzione, WinHttp chiama [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) nel contesto del certificato fornito dal chiamante in modo che il contesto del certificato possa essere rilasciato in modo indipendente dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="5829a-132">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="5829a-133">L'applicazione non deve tentare di chiudere l'archivio certificati con il flag CERT CLOSE STORE FORCE FLAG nella chiamata a \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) nell'archivio certificati da cui è stato recuperato il contesto del certificato.</span><span class="sxs-lookup"><span data-stu-id="5829a-133">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="5829a-134">Potrebbe verificarsi una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="5829a-134">An access violation may occur.</span></span>

<span data-ttu-id="5829a-135">Quando il server richiede un certificato client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce un errore [**\_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED.**](error-messages.md)</span><span class="sxs-lookup"><span data-stu-id="5829a-135">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="5829a-136">Se il server richiede il certificato ma non lo richiede, l'applicazione può specificare questa opzione per indicare che non dispone di un certificato.</span><span class="sxs-lookup"><span data-stu-id="5829a-136">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="5829a-137">Il server può scegliere un altro schema di autenticazione o consentire l'accesso anonimo al server.</span><span class="sxs-lookup"><span data-stu-id="5829a-137">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="5829a-138">L'applicazione fornisce la macro **\_ WINHTTP NO \_ CLIENT \_ CERT \_ CONTEXT** nel *parametro lpBuffer* di [**WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="5829a-138">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="5829a-139">Se il server richiede un certificato client, può inviare un codice di stato HTTP 403 in risposta.</span><span class="sxs-lookup"><span data-stu-id="5829a-139">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="5829a-140">Per altre informazioni, vedere **l'opzione WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ ISSUER \_ LIST.**</span><span class="sxs-lookup"><span data-stu-id="5829a-140">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**ELENCO AUTORITÀ DI CERTIFICAZIONE \_ \_ DEL CERTIFICATO CLIENT \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-142">Recupera una [**struttura SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) quando l'errore da [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) è **ERROR \_ WINHTTP CLIENT \_ \_ \_ AUTH CERT \_ NEEDED**.</span><span class="sxs-lookup"><span data-stu-id="5829a-142">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="5829a-143">L'elenco delle autorità di certificazione nella struttura contiene un elenco di autorità di certificazione (CA) accettabili dal server.</span><span class="sxs-lookup"><span data-stu-id="5829a-143">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="5829a-144">L'applicazione client può filtrare l'elenco di CA per recuperare il certificato client per l'autenticazione SSL.</span><span class="sxs-lookup"><span data-stu-id="5829a-144">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="5829a-145">In alternativa, se il server richiede il certificato client, ma non lo richiede, l'applicazione può chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l'opzione **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="5829a-145">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="5829a-146">Per altre informazioni, vedere **l'opzione \_ WINHTTP OPTION \_ CLIENT \_ CERT \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="5829a-146">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**TABELLA CODICI \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-148">Imposta la [*tabella codici*](glossary.md) utilizzata per elaborare l'URL, ovvero la stringa di query.</span><span class="sxs-lookup"><span data-stu-id="5829a-148">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="5829a-149">Il valore predefinito è UTF8.</span><span class="sxs-lookup"><span data-stu-id="5829a-149">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**OPZIONE WINHTTP \_ \_ CONFIGURARE \_ \_ L'AUTENTICAZIONE PASSPORT**</span><span class="sxs-lookup"><span data-stu-id="5829a-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-151">Imposta un valore long integer senza segno che specifica se [l'autenticazione Passport nell'autenticazione WinHTTP](passport-authentication-in-winhttp.md) è abilitata.</span><span class="sxs-lookup"><span data-stu-id="5829a-151">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="5829a-152">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5829a-152">The value can be one of the following:</span></span>

| <span data-ttu-id="5829a-153">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-153">Term</span></span> | <span data-ttu-id="5829a-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-154">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ DISABILITARE \_ \_ L'AUTENTICAZIONE PASSPORT</span><span class="sxs-lookup"><span data-stu-id="5829a-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="5829a-156">Microsoft Passport'autenticazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5829a-156">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="5829a-157">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5829a-157">This is the default.</span></span> |
| <span data-ttu-id="5829a-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ DISABILITA \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="5829a-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="5829a-159">Il keyring Passport è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5829a-159">The Passport keyring is disabled.</span></span> <span data-ttu-id="5829a-160">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5829a-160">This is the default.</span></span> |
| <span data-ttu-id="5829a-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ ABILITARE \_ L'AUTENTICAZIONE \_ PASSPORT</span><span class="sxs-lookup"><span data-stu-id="5829a-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="5829a-162">L'autenticazione Passport è abilitata.</span><span class="sxs-lookup"><span data-stu-id="5829a-162">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="5829a-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="5829a-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="5829a-164">Il keyring Passport è abilitato.</span><span class="sxs-lookup"><span data-stu-id="5829a-164">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="5829a-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**TENTATIVI \_ DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-166">Imposta o recupera un valore long integer senza segno che contiene il numero di tentativi di connessione diWinHTTP a un host.</span><span class="sxs-lookup"><span data-stu-id="5829a-166">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="5829a-167">I servizi HTTP di Microsoft Windows (WinHTTP) tentano una sola volta per ogni indirizzo IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="5829a-167">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="5829a-168">Ad esempio, se si tenta di connettersi a un host multihomed con 10 indirizzi IP e **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** è impostato su 7, WinHTTP tenta di connettersi solo al primo sette indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="5829a-168">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="5829a-169">Dato lo stesso set di 10 indirizzi IP, se **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** è impostato su 20, WinHTTP tenta ognuno dei 10 una sola volta.</span><span class="sxs-lookup"><span data-stu-id="5829a-169">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="5829a-170">Se un tentativo di connessione ha comunque esito negativo dopo il numero specificato di tentativi o se il timeout di connessione è scaduto prima di allora, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="5829a-170">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="5829a-171">Il valore predefinito per **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** è cinque tentativi.</span><span class="sxs-lookup"><span data-stu-id="5829a-171">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**TIMEOUT DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-173">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, espresso in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="5829a-173">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="5829a-174">L'impostazione di questa opzione su infinito (0xFFFFFFFF) disabilita questo timer.</span><span class="sxs-lookup"><span data-stu-id="5829a-174">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="5829a-175">Se una richiesta di connessione TCP richiede più tempo di questo valore di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="5829a-175">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="5829a-176">Il timeout predefinito è 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="5829a-176">The default timeout is 60 seconds.</span></span> <span data-ttu-id="5829a-177">Quando si tenta di connettersi a più indirizzi IP per un singolo host (un host multihomed), il limite di timeout è per ogni singola connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-177">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**INFORMAZIONI DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-179">Recupera l'indirizzo IP di origine e di destinazione e la porta della richiesta che ha generato la risposta quando viene restituito [**WinHttpReceiveResponse.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)</span><span class="sxs-lookup"><span data-stu-id="5829a-179">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="5829a-180">L'applicazione chiama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con l'opzione **WINHTTP \_ OPTION CONNECTION \_ \_ INFO** e fornisce la struttura [**WINHTTP CONNECTION \_ \_ INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) nel *parametro lpBuffer.*</span><span class="sxs-lookup"><span data-stu-id="5829a-180">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="5829a-181">Per altre informazioni, vedere **WINHTTP \_ CONNECTION \_ INFO**.</span><span class="sxs-lookup"><span data-stu-id="5829a-181">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="5829a-182">**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5829a-182">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**STATISTICHE DI \_ \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ V0**</span><span class="sxs-lookup"><span data-stu-id="5829a-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-184">Rieduca lo struct [**TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) per la connessione sottostante usata dalla richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-184">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="5829a-185">Lo struct restituito può contenere statistiche provenienti da richieste precedenti inviate sulla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="5829a-186">Questa opzione è stata sostituita da **WINHTTP \_ OPTION CONNECTION \_ \_ STATS \_ V1.**</span><span class="sxs-lookup"><span data-stu-id="5829a-186">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**STATISTICHE DI \_ \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ V1**</span><span class="sxs-lookup"><span data-stu-id="5829a-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-188">Rieduca lo struct [**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) per la connessione sottostante usata dalla richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-188">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="5829a-189">Lo struct restituito può contenere statistiche provenienti da richieste precedenti inviate sulla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-189">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**VALORE DI CONTESTO \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-191">Imposta o recupera un **\_ PTR DWORD** che contiene un puntatore al valore di contesto associato a questo handle [HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="5829a-191">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="5829a-192">Viene usato il valore archiviato nel buffer e al flag di opzione **WINHTTP \_ OPTION CONTEXT \_ \_ VALUE** viene assegnato un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="5829a-192">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_ \_ DECOMPRESSIONE DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-194">Imposta un valore DWORD di flag che determina se WinHTTP decomprime automaticamente i corpi di risposta con codifiche di contenuto compresse.</span><span class="sxs-lookup"><span data-stu-id="5829a-194">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="5829a-195">WinHTTP imposta anche un'intestazione Accept-Encoding appropriata, eseguendo l'override di qualsiasi elemento fornito dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="5829a-195">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="5829a-196">I valori supportati sono:</span><span class="sxs-lookup"><span data-stu-id="5829a-196">Supported values are:</span></span>

| <span data-ttu-id="5829a-197">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-197">Term</span></span> | <span data-ttu-id="5829a-198">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-198">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP \_ DECOMPRESSION \_ FLAG \_ GZIP</span><span class="sxs-lookup"><span data-stu-id="5829a-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="5829a-200">Decomprimere Content-Encoding: risposte gzip.</span><span class="sxs-lookup"><span data-stu-id="5829a-200">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="5829a-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>DEFLATE \_ IL FLAG DI DECOMPRESSIONE WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="5829a-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="5829a-202">Decompressione della codifica dei contenuti: deflare le risposte.</span><span class="sxs-lookup"><span data-stu-id="5829a-202">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="5829a-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>FLAG \_ DI DECOMPRESSIONE WINHTTP \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="5829a-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="5829a-204">Decomprimere le risposte con qualsiasi codifica di contenuto supportata.</span><span class="sxs-lookup"><span data-stu-id="5829a-204">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="5829a-205">Per impostazione predefinita, WinHTTP recapiterà le risposte compresse al chiamante senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="5829a-205">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**OPZIONE WINHTTP \_ DISABILITA LA COMPILAZIONE DELLA CATENA DI \_ \_ \_ \_ CERTIFICATI**</span><span class="sxs-lookup"><span data-stu-id="5829a-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="5829a-207">L'impostazione di questa opzione su un handle di sessione WinHttp consente di abilitare o disabilitare la creazione della catena di certificati del server.</span><span class="sxs-lookup"><span data-stu-id="5829a-207">Setting this option on a WinHttp session handle allows you to enable/disable whether the server certificate chain is built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**OPZIONE WINHTTP \_ \_ DISABILITA \_ FUNZIONALITÀ**</span><span class="sxs-lookup"><span data-stu-id="5829a-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-209">Imposta un valore long integer senza segno che specifica quali funzionalità sono disabilitate con uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="5829a-209">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="5829a-210">Tenere presente che questa funzionalità deve essere passata a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) solo su handle di richiesta dopo la creazione dell'handle della richiesta [**con WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)e prima che la richiesta venga inviata [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="5829a-210">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="5829a-211">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-211">Term</span></span> | <span data-ttu-id="5829a-212">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-212">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ DISABILITARE \_ L'AUTENTICAZIONE</span><span class="sxs-lookup"><span data-stu-id="5829a-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="5829a-214">L'autenticazione automatica è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5829a-214">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="5829a-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>DISABILITARE \_ I COOKIE IN WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="5829a-216">L'aggiunta automatica delle intestazioni dei cookie alle richieste è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5829a-216">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="5829a-217">Inoltre, i cookie restituiti non vengono aggiunti automaticamente al database dei cookie.</span><span class="sxs-lookup"><span data-stu-id="5829a-217">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="5829a-218">La disabilitazione dei cookie può comportare prestazioni scarse per l'autenticazione Passport.</span><span class="sxs-lookup"><span data-stu-id="5829a-218">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="5829a-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="5829a-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="5829a-220">Disabilita la semantica keep-alive per la connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-220">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="5829a-221">La semantica keep-alive è necessaria per MSN, NTLM e altri tipi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5829a-221">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="5829a-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP \_ DISABILITA \_ I REINDIRIZZAMENTI</span><span class="sxs-lookup"><span data-stu-id="5829a-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="5829a-223">Il reindirizzamento automatico è disabilitato quando si inviano richieste [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="5829a-223">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="5829a-224">Se il reindirizzamento automatico è disabilitato, un'applicazione deve registrare una funzione di callback perché l'autenticazione Passport riesca.</span><span class="sxs-lookup"><span data-stu-id="5829a-224">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="5829a-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**OPZIONE WINHTTP \_ \_ DISABILITA IL \_ \_ FALLBACK DEL \_ PROTOCOLLO SICURO**</span><span class="sxs-lookup"><span data-stu-id="5829a-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-226">Impedisce a WinHTTP di ritentare una connessione con una versione inferiore del protocollo di sicurezza quando la negoziazione iniziale del protocollo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5829a-226">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPZIONE WINHTTP \_ \_ DISABILITA CODA DI \_ \_ FLUSSO**</span><span class="sxs-lookup"><span data-stu-id="5829a-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-228">Consente alle nuove richieste di aprire una connessione HTTP/2 aggiuntiva quando viene raggiunto il limite massimo di flussi simultanei, anziché attendere il successivo flusso disponibile in una connessione esistente.</span><span class="sxs-lookup"><span data-stu-id="5829a-228">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**FUNZIONALITÀ DI \_ ABILITAZIONE \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-230">Imposta un valore long integer senza segno che specifica le funzionalità attualmente abilitate.</span><span class="sxs-lookup"><span data-stu-id="5829a-230">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="5829a-231">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5829a-231">Can be one of the following values.</span></span>

| <span data-ttu-id="5829a-232">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-232">Term</span></span> | <span data-ttu-id="5829a-233">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-233">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="5829a-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="5829a-235">Se abilitata, WinHTTP ripristina temporaneamente la rappresentazione del client per la durata delle operazioni di autenticazione del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="5829a-235">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="5829a-236">Questo valore può essere impostato solo nell'handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-236">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="5829a-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ ABILITARE LA REVOCA \_ \_ SSL</span><span class="sxs-lookup"><span data-stu-id="5829a-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="5829a-238">Se abilitata, WinHTTP consente la revoca SSL.</span><span class="sxs-lookup"><span data-stu-id="5829a-238">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="5829a-239">Questo valore può essere impostato solo nell'handle della richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-239">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**OPZIONE WINHTTP \_ \_ ABILITA PROTOCOLLO \_ \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-241">Imposta una maschera di bit DWORD di versioni HTTP avanzate accettabili.</span><span class="sxs-lookup"><span data-stu-id="5829a-241">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="5829a-242">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="5829a-242">Possible values are:</span></span>

| <span data-ttu-id="5829a-243">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-243">Term</span></span> | <span data-ttu-id="5829a-244">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-244">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>FLAG \_ DEL PROTOCOLLO \_ \_ WINHTTP HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5829a-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="5829a-246">Abilita HTTP/2 per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-246">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="5829a-247">Nessuno (0x0)</span><span class="sxs-lookup"><span data-stu-id="5829a-247">None (0x0)</span></span> | <span data-ttu-id="5829a-248">Limita la richiesta a HTTP/1.1 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="5829a-248">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="5829a-249">Le versioni legacy di HTTP (1.1 e precedenti) non possono essere disabilitate usando questa opzione.</span><span class="sxs-lookup"><span data-stu-id="5829a-249">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="5829a-250">Il valore predefinito è 0x0.</span><span class="sxs-lookup"><span data-stu-id="5829a-250">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**OPZIONE WINHTTP \_ \_ ABILITA \_ HTTP2 PLUS CLIENT \_ \_ \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="5829a-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="5829a-252">Questa opzione può essere impostata su un handle di sessione WinHttp per consentire a WinHttp di usare il contesto del certificato client fornito dal chiamante quando viene usato HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="5829a-252">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**OPZIONE WINHTTP \_ \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="5829a-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-254">Imposta un **valore BOOL** che specifica se la traccia è attualmente abilitata.</span><span class="sxs-lookup"><span data-stu-id="5829a-254">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="5829a-255">Per altre informazioni sulla funzionalità di traccia in WinHTTP, vedere [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="5829a-255">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="5829a-256">Questa opzione può essere impostata solo su un handle **HINTERNET** **NULL.**</span><span class="sxs-lookup"><span data-stu-id="5829a-256">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="5829a-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**OPZIONE WINHTTP \_ \_ ENCODE \_ EXTRA**</span><span class="sxs-lookup"><span data-stu-id="5829a-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-258">Abilita la codifica della percentuale dell'URL per il percorso e la stringa di query.</span><span class="sxs-lookup"><span data-stu-id="5829a-258">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="5829a-259">In alternativa, è possibile eseguire la codifica percentuale prima di chiamare WinHttp.</span><span class="sxs-lookup"><span data-stu-id="5829a-259">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="5829a-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**L'OPZIONE WINHTTP \_ \_ SCADE LA \_ CONNESSIONE**</span><span class="sxs-lookup"><span data-stu-id="5829a-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-261">Questa opzione può essere impostata solo su un handle di richiesta ancora attivo (invio o ricezione).</span><span class="sxs-lookup"><span data-stu-id="5829a-261">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="5829a-262">L'impostazione di questa opzione consente a WinHttp di interrompere la gestione delle richieste sulla connessione associata all'handle di richiesta passato.</span><span class="sxs-lookup"><span data-stu-id="5829a-262">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="5829a-263">La connessione verrà chiusa dopo il completamento dell'handle della richiesta con cui viene chiamata questa opzione.</span><span class="sxs-lookup"><span data-stu-id="5829a-263">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="5829a-264">Questa opzione non accetta parametri.</span><span class="sxs-lookup"><span data-stu-id="5829a-264">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERRORE ESTESO \_ \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-266">Recupera un valore di long integer senza segno che contiene un codice di errore di Microsoft Windows Sockets mappato all'ultimo messaggio di errore ERROR WINHTTP restituito \_ in questo contesto del \_ \* thread.</span><span class="sxs-lookup"><span data-stu-id="5829a-266">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="5829a-267">È possibile passare **NULL** come valore dell'handle.</span><span class="sxs-lookup"><span data-stu-id="5829a-267">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**OPZIONE WINHTTP \_ \_ PRIMA CONNESSIONE \_ \_ DISPONIBILE**</span><span class="sxs-lookup"><span data-stu-id="5829a-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="5829a-269">Per impostazione predefinita, quando WinHttp invia una richiesta, se non sono disponibili connessioni per gestire la richiesta, WinHttp tenterà di stabilire una nuova connessione e la richiesta verrà associata a questa nuova connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-269">By default, when WinHttp sends a request, if there are no available connections to serve the request, WinHttp will attempt to establish a new connection, and the request will be bound to this new connection.</span></span> <span data-ttu-id="5829a-270">Quando si imposta questa opzione, tale richiesta verrà invece servita alla prima connessione che diventa disponibile e non necessariamente a quella stabilita.</span><span class="sxs-lookup"><span data-stu-id="5829a-270">When you set this option, such a request will instead be served on the first connection that becomes available, and not necessarily the one being established.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**CRED \_ \_ PROXY GLOBALI \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-272">Accetta un puntatore a [**una struttura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *hInternet* impostato su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="5829a-272">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="5829a-273">Questa opzione richiede la chiave del Registro di sistema **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="5829a-273">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="5829a-274">Se questa chiave del Registro di sistema non è impostata, WinHTTP restituirà **l'errore ERRORE \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="5829a-274">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="5829a-275">Questa chiave del Registro di sistema non è presente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5829a-275">This registry key is not present by default.</span></span> <span data-ttu-id="5829a-276">Quando è impostato, WinINet invierà le credenziali a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5829a-276">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="5829a-277">Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono impostate credenziali nell'handle corrente, userà le credenziali fornite da WinINet.</span><span class="sxs-lookup"><span data-stu-id="5829a-277">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="5829a-278">Per condividere le credenziali del server oltre alle credenziali del proxy, gli utenti devono impostare **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="5829a-278">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**CRED SERVER \_ \_ GLOBALI \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-280">Accetta un puntatore a [**una struttura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *hInternet* impostato su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="5829a-280">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="5829a-281">Questa opzione richiede la chiave del Registro di sistema **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="5829a-281">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="5829a-282">Se questa chiave del Registro di sistema non è impostata, WinHTTP restituirà **l'errore ERRORE \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="5829a-282">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="5829a-283">Questa chiave del Registro di sistema non è presente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5829a-283">This registry key is not present by default.</span></span> <span data-ttu-id="5829a-284">Quando è impostato, WinINet invierà le credenziali a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5829a-284">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="5829a-285">Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono impostate credenziali nell'handle corrente, userà le credenziali fornite da WinINet.</span><span class="sxs-lookup"><span data-stu-id="5829a-285">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="5829a-286">Per condividere le credenziali del server oltre alle credenziali del proxy, gli utenti devono impostare **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="5829a-286">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TIPO DI \_ HANDLE DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-288">Recupera un valore long integer senza segno che contiene il tipo dell'handle [HINTERNET](hinternet-handles-in-winhttp.md) passato.</span><span class="sxs-lookup"><span data-stu-id="5829a-288">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="5829a-289">Il valore restituito può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="5829a-289">The return value can be one of the following:</span></span>

| <span data-ttu-id="5829a-290">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-290">Term</span></span> | <span data-ttu-id="5829a-291">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-291">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>TIPO DI HANDLE WINHTTP \_ \_ \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="5829a-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="5829a-293">L'handle è un handle di connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-293">The handle is a connection handle.</span></span> |
| <span data-ttu-id="5829a-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>RICHIESTA DI TIPO HANDLE WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5829a-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="5829a-295">L'handle è un handle di richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-295">The handle is a request handle.</span></span> |
| <span data-ttu-id="5829a-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SESSIONE DEL TIPO DI HANDLE WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5829a-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="5829a-297">L'handle è un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-297">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="5829a-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**PROTOCOLLO \_ \_ HTTP DELL'OPZIONE WINHTTP \_ \_ OBBLIGATORIO**</span><span class="sxs-lookup"><span data-stu-id="5829a-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-299">Impedisce l'uso di versioni del protocollo diverse da quelle abilitate da **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-299">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**PROTOCOLLO \_ \_ HTTP DELL'OPZIONE WINHTTP \_ \_ USATO**</span><span class="sxs-lookup"><span data-stu-id="5829a-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-301">Ottiene un valore DWORD che indica quale versione HTTP avanzata è stata usata in una determinata richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-301">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="5829a-302">Per un elenco dei valori possibili, vedere **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.</span><span class="sxs-lookup"><span data-stu-id="5829a-302">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**VERSIONE \_ \_ HTTP DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-304">Imposta o recupera una struttura [**HTTP \_ VERSION \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) che contiene la versione HTTP supportata.</span><span class="sxs-lookup"><span data-stu-id="5829a-304">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="5829a-305">Si tratta di un'opzione a livello di processo. usare **NULL per** l'handle.</span><span class="sxs-lookup"><span data-stu-id="5829a-305">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**OPZIONE WINHTTP \_ \_ HTTP2 \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="5829a-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="5829a-307">Questa opzione può essere impostata su un handle di sessione per fare in modo che WinHttp usi i frame PING HTTP/2 come meccanismo keepalive.</span><span class="sxs-lookup"><span data-stu-id="5829a-307">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="5829a-308">I chiamanti specificano un timeout in millisecondi e, dopo che non è presente alcuna attività su una connessione per tale periodo di timeout, WinHttp inizierà a inviare frame PING HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="5829a-308">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="5829a-309">I chiamanti non possono impostare un valore di timeout inferiore a 5000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="5829a-309">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**OPZIONE WINHTTP \_ \_ HTTP2 \_ PLUS TRANSFER \_ \_ ENCODING**</span><span class="sxs-lookup"><span data-stu-id="5829a-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="5829a-311">Questa opzione può essere impostata su un handle di richiesta WinHttp per controllare il comportamento di WinHttp quando una risposta HTTP/2 contiene un'intestazione "Transfer-Encoding".</span><span class="sxs-lookup"><span data-stu-id="5829a-311">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="5829a-312">In tal caso, WinHttp restituirà un errore se questa opzione è impostata su **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="5829a-312">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="5829a-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**OPZIONE WINHTTP \_ \_ IGNORA REVOCA CERTIFICATO \_ \_ \_ OFFLINE**</span><span class="sxs-lookup"><span data-stu-id="5829a-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-314">Consente alle connessioni protette di usare certificati di sicurezza per cui non è stato possibile scaricare l'elenco di revoche di certificati.</span><span class="sxs-lookup"><span data-stu-id="5829a-314">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**OPZIONE \_ \_ WINHTTP \_ FALLBACK RAPIDO IPV6 \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-316">Abilita il fallback rapido IPv6 (bulbi oculare più accattivanti) per la connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-316">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="5829a-317">Questo comportamento è simile al comportamento di Happy Eyeballs descritto in [RFC 6555](https://tools.ietf.org/html/rfc6555) per migliorare i tempi di connessione nelle reti in cui IPv6 non è affidabile.</span><span class="sxs-lookup"><span data-stu-id="5829a-317">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="5829a-318">Se entrambi gli indirizzi IPv6 e IPv4 vengono risolti per un determinato host, WinHttp inizierà connettendosi al primo indirizzo IPv6 risolto con un timeout breve (300 ms).</span><span class="sxs-lookup"><span data-stu-id="5829a-318">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="5829a-319">In caso di errore di connessione, WinHttp tenterà di connettersi al primo indirizzo IPv4 risolto con il timeout standard.</span><span class="sxs-lookup"><span data-stu-id="5829a-319">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="5829a-320">In caso di errore della seconda connessione, WinHttp ripeterà il primo indirizzo IPv6 risolto con il timeout standard.</span><span class="sxs-lookup"><span data-stu-id="5829a-320">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="5829a-321">In caso di errore della terza connessione, WinHttp ripristina il comportamento predefinito per tutti gli indirizzi rimanenti, provando una connessione a ognuno con il timeout standard fino a quando non viene stabilita una connessione o non rimane alcun indirizzo.</span><span class="sxs-lookup"><span data-stu-id="5829a-321">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**L'OPZIONE WINHTTP \_ \_ È PROXY CONNECT \_ \_ \_ RESPONSE**</span><span class="sxs-lookup"><span data-stu-id="5829a-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-323">Ottiene un valore che indica se è possibile recuperare o meno una risposta di connessione restituita dal proxy.</span><span class="sxs-lookup"><span data-stu-id="5829a-323">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ 1 \_ 0 \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="5829a-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-325">Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="5829a-325">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="5829a-326">Il valore predefinito è **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="5829a-326">The default value is **INFINITE**.</span></span>

<span data-ttu-id="5829a-327">**Windows Vista con SP1 e Windows Server 2008:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5829a-327">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="5829a-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-329">Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server.</span><span class="sxs-lookup"><span data-stu-id="5829a-329">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="5829a-330">Il valore predefinito è **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="5829a-330">The default value is **INFINITE**.</span></span>

<span data-ttu-id="5829a-331">Quando questa opzione è impostata su zero, WinHTTP imposta il limite per il numero di connessioni su 2.</span><span class="sxs-lookup"><span data-stu-id="5829a-331">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**OPZIONE WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS**</span><span class="sxs-lookup"><span data-stu-id="5829a-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-333">Imposta il numero massimo di reindirizzamenti seguito da WinHTTP. il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="5829a-333">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="5829a-334">Questo limite impedisce a siti non autorizzati di sospendere il client WinHTTP in seguito a un numero elevato di reindirizzamenti.</span><span class="sxs-lookup"><span data-stu-id="5829a-334">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="5829a-335">**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5829a-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**OPZIONE WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE**</span><span class="sxs-lookup"><span data-stu-id="5829a-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-337">Numero massimo di risposte del codice di stato Informational 100-199 ignorate prima di restituire il codice di stato finale al client WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5829a-337">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="5829a-338">I codici di stato in formato informativo 100-199 possono essere inviati dal server prima del codice di stato finale e sono descritti nella specifica per HTTP/1.1 (per altre informazioni, vedere [RFC 2616).](https://www.ietf.org/rfc/rfc2616.txt)</span><span class="sxs-lookup"><span data-stu-id="5829a-338">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="5829a-339">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="5829a-339">The default is 10.</span></span>

<span data-ttu-id="5829a-340">**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5829a-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**DIMENSIONI DI \_ \_ SVUOTAMENTO DELLE \_ RISPOSTE MASSIME \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-342">Limite alla quantità di dati svuotati dalle risposte per riutilizzare una connessione, specificata in byte.</span><span class="sxs-lookup"><span data-stu-id="5829a-342">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="5829a-343">Il valore predefinito è 1 MB.</span><span class="sxs-lookup"><span data-stu-id="5829a-343">The default is 1MB.</span></span>

<span data-ttu-id="5829a-344">**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5829a-344">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**DIMENSIONI MASSIME \_ INTESTAZIONE RISPOSTA \_ \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-346">Set associato alla dimensione massima della parte di intestazione della risposta del server, specificata in byte.</span><span class="sxs-lookup"><span data-stu-id="5829a-346">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="5829a-347">Questo limite protegge il client da un server non autorizzato che tenta di bloccare il client inviando una risposta con una quantità infinita di dati di intestazione.</span><span class="sxs-lookup"><span data-stu-id="5829a-347">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="5829a-348">Il valore predefinito è 64 KB.</span><span class="sxs-lookup"><span data-stu-id="5829a-348">The default value is 64KB.</span></span>

<span data-ttu-id="5829a-349">**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5829a-349">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**HANDLE PADRE \_ DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-351">Recupera l'handle padre per questo handle.</span><span class="sxs-lookup"><span data-stu-id="5829a-351">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**TESTO \_ \_ \_ COBRANDING DELL'OPZIONE WINHTTP PASSPORT \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-353">Recupera una stringa che contiene il [*testo di cobranding*](glossary.md) fornito dal server di accesso Passport.</span><span class="sxs-lookup"><span data-stu-id="5829a-353">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="5829a-354">Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401.</span><span class="sxs-lookup"><span data-stu-id="5829a-354">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="5829a-355">Un'applicazione deve passare dimensioni del buffer, in byte, sufficientemente grandi da contenere la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="5829a-355">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**URL \_ \_ \_ COBRANDING DELL'OPZIONE WINHTTP PASSPORT \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-357">Recupera una stringa contenente un URL per un [*elemento grafico di cobranding*](glossary.md) fornito dal server di accesso Passport.</span><span class="sxs-lookup"><span data-stu-id="5829a-357">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="5829a-358">Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401.</span><span class="sxs-lookup"><span data-stu-id="5829a-358">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="5829a-359">Un'applicazione deve passare dimensioni del buffer, in byte, sufficientemente grandi da contenere la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="5829a-359">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**URL \_ RESTITUITO \_ PASSPORT DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-361">Imposta un'opzione di sola lettura su un handle di richiesta che recupera l'URL restituito di Passport.</span><span class="sxs-lookup"><span data-stu-id="5829a-361">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**OPZIONE WINHTTP \_ \_ \_ DISCONNESSIONE PASSPORT \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-363">Imposta l'opzione su un handle di sessione per disconnettersi da qualsiasi account di accesso Passport.</span><span class="sxs-lookup"><span data-stu-id="5829a-363">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="5829a-364">Un'applicazione deve passare l'URL restituito passport recuperato con **WINHTTP \_ OPTION PASSPORT RETURN \_ \_ \_ URL**.</span><span class="sxs-lookup"><span data-stu-id="5829a-364">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="5829a-365">Tutti i cookie correlati all'URL restituito vengono cancellati.</span><span class="sxs-lookup"><span data-stu-id="5829a-365">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**PASSWORD \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-367">Imposta o recupera un valore stringa contenente la password associata a un handle di richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-367">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**PROXY \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-369">Imposta o recupera una struttura [**WINHTTP \_ PROXY \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) che contiene i dati del proxy in un handle di sessione o in un handle di richiesta esistente.</span><span class="sxs-lookup"><span data-stu-id="5829a-369">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="5829a-370">Quando si recuperano dati proxy, un'applicazione deve liberare le stringhe **lpszProxy** e **lpszProxyBypass** contenute in questa struttura (se non **sono NULL)** usando la [**funzione GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree)</span><span class="sxs-lookup"><span data-stu-id="5829a-370">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="5829a-371">Un'applicazione può eseguire una query per i dati proxy globali (proxy predefinito) passando un handle **NULL.**</span><span class="sxs-lookup"><span data-stu-id="5829a-371">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**PASSWORD PROXY \_ DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-373">Imposta o recupera un valore stringa contenente la password utilizzata per accedere al proxy.</span><span class="sxs-lookup"><span data-stu-id="5829a-373">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**NOME \_ \_ SPN PROXY \_ DELL'OPZIONE WINHTTP \_ USATO**</span><span class="sxs-lookup"><span data-stu-id="5829a-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-375">Ottiene il nome dell'entità server proxy fornito da WinHTTP a SSPI durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5829a-375">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="5829a-376">Questo valore stringa viene utilizzato per passare a [**SspiPromptForCredentials dopo**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) un errore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5829a-376">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**NOME UTENTE \_ PROXY DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-378">Imposta o recupera un valore stringa contenente il nome utente utilizzato per accedere al proxy.</span><span class="sxs-lookup"><span data-stu-id="5829a-378">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**DIMENSIONI DEL \_ \_ BUFFER DI LETTURA \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-380">Questa opzione è stata deprecata. non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="5829a-380">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**L'OPZIONE WINHTTP \_ RICEVE LA RISPOSTA DI CONNESSIONE \_ \_ \_ \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="5829a-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-382">Imposta se è possibile recuperare o meno l'entità di risposta del proxy.</span><span class="sxs-lookup"><span data-stu-id="5829a-382">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="5829a-383">Questa opzione è disabilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5829a-383">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**L'OPZIONE WINHTTP \_ RICEVE IL TIMEOUT DI \_ \_ \_ RISPOSTA**</span><span class="sxs-lookup"><span data-stu-id="5829a-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-385">Imposta o recupera un valore di long integer senza segno che contiene il valore di timeout, in millisecondi, per attendere la ricezione di tutte le intestazioni di risposta a una richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-385">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="5829a-386">Se WinHTTP non riceve tutte le intestazioni entro questo periodo di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="5829a-386">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="5829a-387">Il valore di timeout predefinito è 90 secondi.</span><span class="sxs-lookup"><span data-stu-id="5829a-387">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="5829a-388">Questo timeout viene controllato solo quando i dati vengono ricevuti dal socket.</span><span class="sxs-lookup"><span data-stu-id="5829a-388">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="5829a-389">Di conseguenza, alla scadenza del timeout l'applicazione client non viene notificata fino a quando non arrivano altri dati dal server.</span><span class="sxs-lookup"><span data-stu-id="5829a-389">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="5829a-390">Se non arrivano dati dal server, il ritardo tra la scadenza del timeout e la notifica dell'applicazione client potrebbe essere pari al valore di timeout impostato usando il *parametro dwReceiveTimeout* della [**funzione WinHttpSetTimeouts.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)</span><span class="sxs-lookup"><span data-stu-id="5829a-390">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**TIMEOUT DI \_ RICEZIONE \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-392">Imposta o recupera un valore di long integer senza segno che contiene il valore di timeout, in millisecondi, per ricevere una risposta parziale a una richiesta o leggere alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="5829a-392">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="5829a-393">Se la risposta richiede più tempo di questo valore di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="5829a-393">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="5829a-394">Il valore di timeout predefinito è di 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="5829a-394">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-396">Imposta il comportamento di WinHTTP relativo alla gestione di un codice di stato di reindirizzamento HTTP 30x.</span><span class="sxs-lookup"><span data-stu-id="5829a-396">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="5829a-397">Questa opzione può essere impostata in un handle di sessione o richiesta su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5829a-397">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="5829a-398">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-398">Term</span></span> | <span data-ttu-id="5829a-399">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-399">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_ \_ SEMPRE</span><span class="sxs-lookup"><span data-stu-id="5829a-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="5829a-401">Tutti i reindirizzamenti vengono seguiti automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5829a-401">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="5829a-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_L'OPZIONE WINHTTP \_ \_ REINDIRIZZA \_ I CRITERI NON CONSENTONO HTTPS A \_ \_ \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="5829a-403">Vengono seguiti tutti i reindirizzamenti, ad eccezione di quelli originati da un URL sicuro (https) a un URL non sicuro (http).</span><span class="sxs-lookup"><span data-stu-id="5829a-403">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="5829a-404">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5829a-404">This is the default setting.</span></span> |
| <span data-ttu-id="5829a-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_ \_ MAI</span><span class="sxs-lookup"><span data-stu-id="5829a-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="5829a-406">I reindirizzamenti non vengono mai seguiti.</span><span class="sxs-lookup"><span data-stu-id="5829a-406">Redirects are never followed.</span></span> <span data-ttu-id="5829a-407">Lo stato 30x viene restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5829a-407">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**OPZIONE WINHTTP \_ \_ REJECT \_ USERPWD \_ IN \_ URL**</span><span class="sxs-lookup"><span data-stu-id="5829a-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-409">Rifiuta gli URL che contengono un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="5829a-409">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="5829a-410">Questa opzione rifiuta anche gli URL che contengono la semantica *username:password,* anche se non viene specificato alcun nome utente o password.</span><span class="sxs-lookup"><span data-stu-id="5829a-410">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="5829a-411">Ad esempio, " u:p@hostname ", " ", " " e " " verrebbero contrassegnati :@hostname u:@hostname come non :p@hostname validi.</span><span class="sxs-lookup"><span data-stu-id="5829a-411">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="5829a-412">Se alla funzione viene passato un URL non valido, restituisce [ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="5829a-412">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="5829a-413">Per impostazione predefinita, questa opzione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5829a-413">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**PRIORITÀ RICHIESTA \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-415">Questa opzione è stata deprecata. non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="5829a-415">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**STATISTICHE DI \_ RICHIESTA \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-417">Rieduca le statistiche per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-417">Retreives statistics for the request.</span></span>  <span data-ttu-id="5829a-418">Per un elenco delle statistiche disponibili, vedere [**WINHTTP \_ REQUEST \_ STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="5829a-418">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**TEMPI DI RICHIESTA \_ \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-420">Retreives timing information for the request (Retreives timing information for the request).</span><span class="sxs-lookup"><span data-stu-id="5829a-420">Retreives timing information for the request.</span></span> <span data-ttu-id="5829a-421">Per un elenco degli intervalli disponibili, vedere [**WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="5829a-421">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**OPZIONE WINHTTP \_ \_ REQUIRE STREAM \_ \_ END**</span><span class="sxs-lookup"><span data-stu-id="5829a-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="5829a-423">Questa opzione indica a WinHttp di ignorare le intestazioni di risposta "Content-Length" e di continuare a ricevere in un flusso fino a quando non viene ricevuto END_STREAM flag di risposta.</span><span class="sxs-lookup"><span data-stu-id="5829a-423">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**NOME HOST \_ DELLA \_ RISOLUZIONE \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="5829a-425">Questa opzione può essere impostata su un handle di richiesta WinHttp prima dell'invio.</span><span class="sxs-lookup"><span data-stu-id="5829a-425">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="5829a-426">Se impostato, WinHttp userà la stringa fornita dal chiamante come nome host per la risoluzione DNS.</span><span class="sxs-lookup"><span data-stu-id="5829a-426">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**TIMEOUT DI \_ RISOLUZIONE \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-428">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, espresso in millisecondi, per risolvere un nome host.</span><span class="sxs-lookup"><span data-stu-id="5829a-428">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="5829a-429">Il valore di timeout predefinito è **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="5829a-429">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="5829a-430">Se viene specificato un valore non predefinito, si verifica un sovraccarico della creazione di un thread per ogni risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5829a-430">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**PROTOCOLLI SICURI \_ DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-432">Imposta un valore di long integer senza segno che specifica quali protocolli sicuri sono accettabili.</span><span class="sxs-lookup"><span data-stu-id="5829a-432">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="5829a-433">Per impostazione predefinita, solo SSL3 e TLS1 sono abilitati in Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5829a-433">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="5829a-434">Per impostazione predefinita, solo SSL3, TLS1.0, TLS1.1 e TLS1.2 sono abilitati in Windows 8.1 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5829a-434">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="5829a-435">Il valore può essere una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5829a-435">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="5829a-436">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-436">Term</span></span> | <span data-ttu-id="5829a-437">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-437">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ ALL</span><span class="sxs-lookup"><span data-stu-id="5829a-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="5829a-439">È possibile usare i protocolli Secure Sockets Layer (SSL) 2.0, SSL 3.0 e Transport Layer Security (TLS) 1.0.</span><span class="sxs-lookup"><span data-stu-id="5829a-439">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="5829a-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="5829a-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="5829a-441">È possibile usare il protocollo SSL 2.0.</span><span class="sxs-lookup"><span data-stu-id="5829a-441">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="5829a-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="5829a-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="5829a-443">È possibile usare il protocollo SSL 3.0.</span><span class="sxs-lookup"><span data-stu-id="5829a-443">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="5829a-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="5829a-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="5829a-445">È possibile usare il protocollo TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="5829a-445">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="5829a-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP \_ FLAG SECURE PROTOCOL \_ \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5829a-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="5829a-447">È possibile usare il protocollo TLS 1.1.</span><span class="sxs-lookup"><span data-stu-id="5829a-447">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="5829a-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP \_ FLAG SECURE PROTOCOL \_ \_ \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="5829a-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="5829a-449">È possibile usare il protocollo TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="5829a-449">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="5829a-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**STRUCT DEL CERTIFICATO \_ \_ DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-451">Recupera il certificato per un server SSL/TLS nella struttura [**WINHTTP \_ CERTIFICATE \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)</span><span class="sxs-lookup"><span data-stu-id="5829a-451">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="5829a-452">L'applicazione deve liberare **i membri lpszSubjectInfo** **e lpszIssuerInfo** con [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span><span class="sxs-lookup"><span data-stu-id="5829a-452">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**FLAG DI \_ SICUREZZA \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-454">Imposta o recupera un valore long integer senza segno che contiene i flag di sicurezza per un handle.</span><span class="sxs-lookup"><span data-stu-id="5829a-454">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="5829a-455">Può essere una combinazione di questi valori:</span><span class="sxs-lookup"><span data-stu-id="5829a-455">It can be a combination of these values:</span></span>

| <span data-ttu-id="5829a-456">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-456">Term</span></span> | <span data-ttu-id="5829a-457">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-457">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>FLAG \_ DI SICUREZZA IGNORE \_ \_ CERT CN \_ \_ INVALID</span><span class="sxs-lookup"><span data-stu-id="5829a-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="5829a-459">Consente un nome comune non valido in un certificato. in altri, il nome del server specificato dall'applicazione non corrisponde al nome comune nel certificato.</span><span class="sxs-lookup"><span data-stu-id="5829a-459">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="5829a-460">Se questo flag è impostato, l'applicazione non riceve un **callback WINHTTP \_ CALLBACK STATUS \_ FLAG \_ \_ CERT CN \_ \_ INVALID** callback.</span><span class="sxs-lookup"><span data-stu-id="5829a-460">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="5829a-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>IL \_ FLAG DI SICUREZZA IGNORA LA DATA DEL CERTIFICATO NON \_ \_ \_ \_ VALIDO</span><span class="sxs-lookup"><span data-stu-id="5829a-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="5829a-462">Consente una data di certificato non valida, ad esempio un certificato scaduto o non ancora valido.</span><span class="sxs-lookup"><span data-stu-id="5829a-462">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="5829a-463">Se questo flag è impostato, l'applicazione non riceve un **callback WINHTTP \_ CALLBACK STATUS \_ FLAG \_ \_ CERT DATE \_ \_ INVALID.**</span><span class="sxs-lookup"><span data-stu-id="5829a-463">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="5829a-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>FLAG \_ DI SICUREZZA IGNORA CA \_ \_ \_ SCONOSCIUTA</span><span class="sxs-lookup"><span data-stu-id="5829a-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="5829a-465">Consente un'autorità di certificazione non valida.</span><span class="sxs-lookup"><span data-stu-id="5829a-465">Allows an invalid certificate authority.</span></span> <span data-ttu-id="5829a-466">Se questo flag è impostato, l'applicazione non riceve un callback DI CALLBACK **DI WINHTTP \_ STATUS FLAG INVALID \_ \_ \_ \_ CA.**</span><span class="sxs-lookup"><span data-stu-id="5829a-466">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="5829a-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>FLAG DI \_ SICUREZZA \_ IGNORA \_ L'UTILIZZO ERRATO \_ DEL \_ CERTIFICATO</span><span class="sxs-lookup"><span data-stu-id="5829a-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="5829a-468">Consente di stabilire l'identità di un server con un certificato non server, ad esempio un certificato client.</span><span class="sxs-lookup"><span data-stu-id="5829a-468">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="5829a-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>FLAG \_ DI SICUREZZA IGNORA FIRMA \_ \_ \_ DEBOLE</span><span class="sxs-lookup"><span data-stu-id="5829a-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="5829a-470">Consente di ignorare una firma debole.</span><span class="sxs-lookup"><span data-stu-id="5829a-470">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="5829a-471">Questo flag è disponibile nell'aggiornamento cumulativo per ogni sistema operativo a partire da Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="5829a-471">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="5829a-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>FLAG \_ DI \_ SICUREZZA SICURO</span><span class="sxs-lookup"><span data-stu-id="5829a-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="5829a-473">Usa trasferimenti sicuri.</span><span class="sxs-lookup"><span data-stu-id="5829a-473">Uses secure transfers.</span></span> <span data-ttu-id="5829a-474">Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="5829a-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="5829a-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>LIVELLO \_ DI ATTENDIBILITÀ DEL FLAG \_ DI SICUREZZA \_ MEDIO</span><span class="sxs-lookup"><span data-stu-id="5829a-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="5829a-476">Usa la crittografia media (56 bit).</span><span class="sxs-lookup"><span data-stu-id="5829a-476">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="5829a-477">Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="5829a-477">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="5829a-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>LIVELLO \_ DI SICUREZZA DEL FLAG DI SICUREZZA \_ \_ SICURO</span><span class="sxs-lookup"><span data-stu-id="5829a-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="5829a-479">Usa una crittografia avanzata (a 128 bit).</span><span class="sxs-lookup"><span data-stu-id="5829a-479">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="5829a-480">Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="5829a-480">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="5829a-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>LIVELLO \_ DI SICUREZZA DEL FLAG \_ \_ DEBOLE</span><span class="sxs-lookup"><span data-stu-id="5829a-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="5829a-482">Usa la crittografia debole (a 40 bit).</span><span class="sxs-lookup"><span data-stu-id="5829a-482">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="5829a-483">Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="5829a-483">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="5829a-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**INFORMAZIONI DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-485">Rieduca la connessione SChannel e le informazioni di crittografia per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="5829a-485">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**BITNESS \_ CHIAVE DI SICUREZZA \_ \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-487">Recupera un valore long integer senza segno che contiene il livello di crittografia della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="5829a-487">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="5829a-488">Un numero maggiore indica una crittografia più avanzata.</span><span class="sxs-lookup"><span data-stu-id="5829a-488">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**TIMEOUT DI \_ INVIO \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-490">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per inviare una richiesta o scrivere alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="5829a-490">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="5829a-491">Se l'invio della richiesta richiede più tempo del timeout, l'operazione di invio viene annullata.</span><span class="sxs-lookup"><span data-stu-id="5829a-491">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="5829a-492">Il timeout predefinito è 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="5829a-492">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="5829a-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-494">Ottiene un puntatore [**alla struttura SecPkgContext \_ Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) che specifica un token di associazione di canale (CBT).</span><span class="sxs-lookup"><span data-stu-id="5829a-494">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="5829a-495">Un token di associazione del canale è una proprietà di un canale di trasporto sicuro e viene usato per associare un canale di autenticazione al canale di trasporto sicuro.</span><span class="sxs-lookup"><span data-stu-id="5829a-495">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="5829a-496">Questo token può essere ottenuto da questa opzione solo dopo che è stata stabilita una connessione SSL.</span><span class="sxs-lookup"><span data-stu-id="5829a-496">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="5829a-497">Il passaggio di questa opzione e di un valore **Null** per *lpBuffer* [**a WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) restituirà ERROR INSUFFICIENT BUFFER e le dimensioni in byte necessarie per il buffer nel \_ parametro \_ *lpdwBufferLength.*</span><span class="sxs-lookup"><span data-stu-id="5829a-497">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="5829a-498">Questo valore delle dimensioni del buffer restituito può essere passato in una chiamata successiva per eseguire una query per il token di associazione del canale.</span><span class="sxs-lookup"><span data-stu-id="5829a-498">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="5829a-499">Questi passaggi sono necessari quando si gestisce WINHTTP CALLBACK STATUS REQUEST se si vogliono modificare le intestazioni della richiesta \_ in base al token di associazione del \_ \_ canale.</span><span class="sxs-lookup"><span data-stu-id="5829a-499">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="5829a-500">Si noti che Windows XP e Vista non supportano la modifica delle intestazioni delle richieste durante questo callback.</span><span class="sxs-lookup"><span data-stu-id="5829a-500">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**CONTESTO DELLA \_ CATENA DI CERTIFICATI DEL SERVER \_ \_ \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-502">Recupera il contesto della catena di certificazione del server.</span><span class="sxs-lookup"><span data-stu-id="5829a-502">Retrieves the server certification chain context.</span></span> <span data-ttu-id="5829a-503">**WINHTTP \_ OPTION \_ SERVER \_ CERT CHAIN \_ \_ CONTEXT** può essere passato per ottenere un puntatore duplicato a **CERT CHAIN \_ \_ CONTEXT** per una catena di certificati server ricevuta durante una connessione SSL negoziata.</span><span class="sxs-lookup"><span data-stu-id="5829a-503">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="5829a-504">Il client deve chiamare [**CertFreeCertificateContext sul**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) puntatore PCCERT CONTEXT restituito che \_ viene inserito nel buffer.</span><span class="sxs-lookup"><span data-stu-id="5829a-504">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**CONTESTO DEL CERTIFICATO \_ \_ DEL SERVER \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-506">Recupera il contesto di certificazione del server.</span><span class="sxs-lookup"><span data-stu-id="5829a-506">Retrieves the server certification context.</span></span> <span data-ttu-id="5829a-507">**WINHTTP \_ OPTION \_ SERVER \_ CERT CONTEXT \_ può** essere passato per ottenere un puntatore duplicato a [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) per un certificato del server ricevuto durante una connessione SSL negoziata.</span><span class="sxs-lookup"><span data-stu-id="5829a-507">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="5829a-508">Il client deve chiamare [**CertFreeCertificateContext sul**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) puntatore PCCERT CONTEXT restituito che \_ viene inserito nel buffer.</span><span class="sxs-lookup"><span data-stu-id="5829a-508">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**NOME \_ \_ SPN DEL SERVER \_ DELL'OPZIONE WINHTTP \_ USATO**</span><span class="sxs-lookup"><span data-stu-id="5829a-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-510">Ottiene il nome dell'entità server del server fornito da WinHTTP a SSPI durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5829a-510">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="5829a-511">Questo valore stringa può essere passato a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) dopo un errore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5829a-511">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**NOME \_ \_ SPN DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-513">Include o rimuove il numero di porta del server quando il nome SPN (nome dell'entità servizio) viene compilato per l'autenticazione Kerberos o Negotiate Kerberos.</span><span class="sxs-lookup"><span data-stu-id="5829a-513">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="5829a-514">Questo flag è uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5829a-514">This flag is one of the following values:</span></span>

| <span data-ttu-id="5829a-515">Termine</span><span class="sxs-lookup"><span data-stu-id="5829a-515">Term</span></span> | <span data-ttu-id="5829a-516">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5829a-516">Description</span></span> |
|-|-|
| <span data-ttu-id="5829a-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ DISABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="5829a-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="5829a-518">Rimuove il numero di porta del server.</span><span class="sxs-lookup"><span data-stu-id="5829a-518">Removes the server port number.</span></span> |
| <span data-ttu-id="5829a-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>PORTA DEL \_ \_ SERVER SPN ABILITATA \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="5829a-520">Include il numero di porta del server.</span><span class="sxs-lookup"><span data-stu-id="5829a-520">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="5829a-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**CODICE DI ERRORE \_ DEL \_ FLUSSO \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="5829a-522">Questa opzione può essere eseguita su un handle di richiesta WinHttp e restituirà il codice di errore indicato da un frame RST_STREAM ricevuto in un flusso HTTP.</span><span class="sxs-lookup"><span data-stu-id="5829a-522">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**OPZIONE WINHTTP \_ \_ TCP FAST \_ \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="5829a-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-524">Abilita TCP Fast Open per la connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-524">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**OPZIONE \_ \_ WINHTTP TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="5829a-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-526">Questa opzione può essere impostata su un handle di sessione WinHttp per abilitare il comportamento keep-alive TCP nel socket sottostante.</span><span class="sxs-lookup"><span data-stu-id="5829a-526">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="5829a-527">Accetta uno [**struct \_ tcp keepalive.**](/windows/win32/winsock/sio-keepalive-vals)</span><span class="sxs-lookup"><span data-stu-id="5829a-527">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**OPZIONE WINHTTP \_ \_ TLS FALSE \_ \_ START**</span><span class="sxs-lookup"><span data-stu-id="5829a-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-529">Abilita TLS False Start per la connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-529">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**OPZIONE WINHTTP \_ \_ \_ \_ FALLBACK NON SICURO DEL PROTOCOLLO TLS \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-531">Questa opzione può essere impostata su un handle di sessione WinHttp per controllare se è consentito il fallback a TLS 1.0 se si verifica un errore di handshake TLS con una versione del protocollo più recente.</span><span class="sxs-lookup"><span data-stu-id="5829a-531">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**EVENTO NOTIFICA \_ \_ DI SCARICAMENTO \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-533">Accetta un evento che verrà impostato quando l'ultimo callback è stato completato per una sessione specifica.</span><span class="sxs-lookup"><span data-stu-id="5829a-533">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="5829a-534">Questo flag deve essere usato in un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-534">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="5829a-535">L'evento non può essere chiuso fino a quando non è stato impostato da WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5829a-535">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**ANALISI \_ \_ DELL'INTESTAZIONE NON SICURA \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-537">Questa opzione è riservata per uso interno e non deve essere chiamata.</span><span class="sxs-lookup"><span data-stu-id="5829a-537">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**AGGIORNAMENTO \_ DELL'OPZIONE WINHTTP \_ AL WEB \_ \_ \_ SOCKET**</span><span class="sxs-lookup"><span data-stu-id="5829a-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-539">Indica all'oggetto stack di avviare un processo di handshake WebSocket [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="5829a-539">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="5829a-540">Questa opzione non accetta parametri.</span><span class="sxs-lookup"><span data-stu-id="5829a-540">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-542">Recupera un valore stringa che contiene l'URL completo di una risorsa scaricata.</span><span class="sxs-lookup"><span data-stu-id="5829a-542">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="5829a-543">Se l'URL originale contiene dati aggiuntivi, ad esempio stringhe di ricerca o ancoraggi, o se la chiamata è stata reindirizzata, l'URL restituito è diverso da quello originale.</span><span class="sxs-lookup"><span data-stu-id="5829a-543">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="5829a-544">L'applicazione deve passare un buffer, ridimensionato in byte, sufficientemente grande da contenere l'URL restituito in caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="5829a-544">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**L'OPZIONE WINHTTP \_ USA LE CREDENZIALI GLOBALI DEL \_ \_ \_ \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="5829a-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-546">Accetta un **bool e** può essere impostato solo un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-546">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="5829a-547">Verrà propagato solo agli handle creati dall'handle di sessione dopo l'impostazione dell'opzione .</span><span class="sxs-lookup"><span data-stu-id="5829a-547">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="5829a-548">Se **TRUE,** questa opzione fa in modo che come ultima risorsa l'uso di credenziali del server globali di cui è stato fatto il push da WinInet.</span><span class="sxs-lookup"><span data-stu-id="5829a-548">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="5829a-549">Il valore predefinito per questa opzione è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="5829a-549">The default for this option is **FALSE**.</span></span> <span data-ttu-id="5829a-550">Questa opzione richiede la chiave del Registro **di sistema HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Impostazioni \\ Internet. ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="5829a-550">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="5829a-551">Questa chiave del Registro di sistema non è presente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5829a-551">This registry key is not present by default.</span></span> <span data-ttu-id="5829a-552">Quando è impostata, WinINet invierà le credenziali a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5829a-552">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="5829a-553">Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono impostate credenziali nell'handle corrente, userà le credenziali fornite da WinINet.</span><span class="sxs-lookup"><span data-stu-id="5829a-553">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**OPZIONE WINHTTP \_ \_ AGENTE \_ UTENTE**</span><span class="sxs-lookup"><span data-stu-id="5829a-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-555">Imposta o recupera [](glossary.md) la stringa dell'agente utente sugli handle forniti da [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) e usati nelle funzioni [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) successive, purché non venga sottoposto a override da un'intestazione aggiunta da [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) **o WinHttpSendRequest.**</span><span class="sxs-lookup"><span data-stu-id="5829a-555">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="5829a-556">Quando si recupera un agente utente, l'applicazione deve passare un buffer, ridimensionato in byte, sufficientemente grande da contenere l'URL restituito in caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="5829a-556">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="5829a-557">Quando si imposta l'agente utente, la dimensione del buffer è la lunghezza della stringa, in caratteri, più il carattere **di terminazione NULL.**</span><span class="sxs-lookup"><span data-stu-id="5829a-557">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**NOME UTENTE \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-559">Imposta o recupera una stringa contenente il nome utente.</span><span class="sxs-lookup"><span data-stu-id="5829a-559">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**TIMEOUT CHIUSURA \_ \_ WEB SOCKET \_ DELL'OPZIONE \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-561">Imposta il tempo, in millisecondi, di attesa di [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) per completare l'handshake di chiusura.</span><span class="sxs-lookup"><span data-stu-id="5829a-561">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="5829a-562">Il valore predefinito è 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="5829a-562">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**OPZIONE WINHTTP \_ \_ INTERVALLO \_ \_ KEEPALIVE PER WEB \_ SOCKET**</span><span class="sxs-lookup"><span data-stu-id="5829a-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-564">Imposta l'intervallo, in millisecondi, per l'invio di un pacchetto keep-alive sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="5829a-564">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="5829a-565">L'intervallo predefinito è 30000 (30 secondi).</span><span class="sxs-lookup"><span data-stu-id="5829a-565">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="5829a-566">L'intervallo minimo è 15000 (15 secondi).</span><span class="sxs-lookup"><span data-stu-id="5829a-566">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="5829a-567">[**L'uso di WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per impostare un valore inferiore a 15000 restituirà con **ERROR INVALID \_ \_ PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="5829a-567">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="5829a-568">Il valore predefinito per **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** viene letto da **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="5829a-568">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="5829a-569">Se non è impostato un valore, verrà usato il valore predefinito 30000.</span><span class="sxs-lookup"><span data-stu-id="5829a-569">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="5829a-570">Non è possibile avere un intervallo keep-live inferiore a 15000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="5829a-570">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**DIMENSIONI BUFFER \_ DI RICEZIONE WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-572">Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di ricezione da utilizzare nelle connessioni WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5829a-572">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**DIMENSIONI BUFFER \_ DI INVIO WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-574">Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di invio da usare nelle connessioni WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5829a-574">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**CONTEGGIO \_ THREAD DI LAVORO \_ \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-576">Imposta un valore long integer senza segno che specifica il numero di thread di lavoro che il pool di thread deve usare per i completamenti asincroni.</span><span class="sxs-lookup"><span data-stu-id="5829a-576">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="5829a-577">Il valore predefinito di questa opzione è zero, che specifica che il numero di thread di lavoro è uguale al numero di CPU nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5829a-577">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="5829a-578">Questa opzione può essere impostata solo su un handle **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) prima che si sia verificata un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="5829a-578">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="5829a-579">Questa opzione può essere impostata una sola volta.</span><span class="sxs-lookup"><span data-stu-id="5829a-579">This option can only be set once.</span></span>

<span data-ttu-id="5829a-580">**Windows Server 2008 R2 e Windows 7:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5829a-580">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5829a-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**DIMENSIONI DEL \_ BUFFER DI \_ SCRITTURA \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5829a-582">Questa opzione è stata deprecata. non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="5829a-582">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5829a-583">Commenti</span><span class="sxs-lookup"><span data-stu-id="5829a-583">Remarks</span></span>

<span data-ttu-id="5829a-584">Nella tabella seguente sono elencati i flag di opzione specificando gli handle su cui possono agire, se possono essere sottoposti a query e impostati e il tipo di dati utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5829a-584">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="5829a-585">Una "X" indica che il flag di opzione è valido per l'uso con la funzione o l'handle, mentre "-" specifica che il flag di opzione non è valido.</span><span class="sxs-lookup"><span data-stu-id="5829a-585">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="5829a-586">Se si tenta di impostare o eseguire una query su un flag di opzione in una versione di Windows in cui non è supportata, verrà generato **l'errore \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="5829a-586">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="5829a-587">Flag di opzione e tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5829a-587">Option flag, and data type</span></span> | <span data-ttu-id="5829a-588">Handle di sessione</span><span class="sxs-lookup"><span data-stu-id="5829a-588">Session handle</span></span> | <span data-ttu-id="5829a-589">Handle di richiesta</span><span class="sxs-lookup"><span data-stu-id="5829a-589">Request handle</span></span> | <span data-ttu-id="5829a-590">Opzione di query</span><span class="sxs-lookup"><span data-stu-id="5829a-590">Query option</span></span> | <span data-ttu-id="5829a-591">Opzione SET</span><span class="sxs-lookup"><span data-stu-id="5829a-591">Set option</span></span> | <span data-ttu-id="5829a-592">Versione minima di Windows</span><span class="sxs-lookup"><span data-stu-id="5829a-592">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="5829a-593">OPZIONE WINHTTP \_ \_ GARANTITA \_ CALLBACK NON \_ \_ BLOCCANTI</span><span class="sxs-lookup"><span data-stu-id="5829a-593">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="5829a-594">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-594">**BOOL**</span></span> | <span data-ttu-id="5829a-595">X</span><span class="sxs-lookup"><span data-stu-id="5829a-595">X</span></span> | \- | \- | <span data-ttu-id="5829a-596">X</span><span class="sxs-lookup"><span data-stu-id="5829a-596">X</span></span> | \- |
| <span data-ttu-id="5829a-597">CRITERIO DI \_ ACCESSO \_ AUTOMATICO DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-597">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="5829a-598">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-598">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-599">X</span><span class="sxs-lookup"><span data-stu-id="5829a-599">X</span></span> | \- | <span data-ttu-id="5829a-600">X</span><span class="sxs-lookup"><span data-stu-id="5829a-600">X</span></span> | \- |
| <span data-ttu-id="5829a-601">CONNESSIONI IN \_ BACKGROUND DELL'OPZIONE WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="5829a-601">WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS</span></span><br/><span data-ttu-id="5829a-602">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-602">**DWORD**</span></span> | <span data-ttu-id="5829a-603">X</span><span class="sxs-lookup"><span data-stu-id="5829a-603">X</span></span> | \- | \- | <span data-ttu-id="5829a-604">X</span><span class="sxs-lookup"><span data-stu-id="5829a-604">X</span></span> | <span data-ttu-id="5829a-605">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-605">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-606">CALLBACK \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-606">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="5829a-607">**Lpvoid**</span><span class="sxs-lookup"><span data-stu-id="5829a-607">**LPVOID**</span></span> | <span data-ttu-id="5829a-608">X</span><span class="sxs-lookup"><span data-stu-id="5829a-608">X</span></span> | <span data-ttu-id="5829a-609">X</span><span class="sxs-lookup"><span data-stu-id="5829a-609">X</span></span> | <span data-ttu-id="5829a-610">X</span><span class="sxs-lookup"><span data-stu-id="5829a-610">X</span></span> | <span data-ttu-id="5829a-611">X</span><span class="sxs-lookup"><span data-stu-id="5829a-611">X</span></span> | \- |
| <span data-ttu-id="5829a-612">CONTESTO DEL CERTIFICATO \_ \_ CLIENT \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-612">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="5829a-613">**CONTESTO DEL \_ CERTIFICATO**</span><span class="sxs-lookup"><span data-stu-id="5829a-613">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="5829a-614">X</span><span class="sxs-lookup"><span data-stu-id="5829a-614">X</span></span> | \- | <span data-ttu-id="5829a-615">X</span><span class="sxs-lookup"><span data-stu-id="5829a-615">X</span></span> | <span data-ttu-id="5829a-616">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5829a-616">Windows Vista</span></span> |
| <span data-ttu-id="5829a-617">ELENCO AUTORITÀ \_ DI CERTIFICAZIONE DEL CERTIFICATO CLIENT \_ \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-617">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="5829a-618">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="5829a-618">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="5829a-619">X</span><span class="sxs-lookup"><span data-stu-id="5829a-619">X</span></span> | <span data-ttu-id="5829a-620">X</span><span class="sxs-lookup"><span data-stu-id="5829a-620">X</span></span> | \- | <span data-ttu-id="5829a-621">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5829a-621">Windows Vista</span></span> |
| <span data-ttu-id="5829a-622">TABELLA CODICI \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-622">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="5829a-623">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-623">**DWORD**</span></span> | <span data-ttu-id="5829a-624">X</span><span class="sxs-lookup"><span data-stu-id="5829a-624">X</span></span> | \- | \- | <span data-ttu-id="5829a-625">X</span><span class="sxs-lookup"><span data-stu-id="5829a-625">X</span></span> | \- |
| <span data-ttu-id="5829a-626">OPZIONE WINHTTP \_ \_ - CONFIGURARE \_ \_ L'AUTENTICAZIONE PASSPORT</span><span class="sxs-lookup"><span data-stu-id="5829a-626">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="5829a-627">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-627">**DWORD**</span></span> | <span data-ttu-id="5829a-628">X</span><span class="sxs-lookup"><span data-stu-id="5829a-628">X</span></span> | \- | \- | <span data-ttu-id="5829a-629">X</span><span class="sxs-lookup"><span data-stu-id="5829a-629">X</span></span> | \- |
| <span data-ttu-id="5829a-630">TENTATIVI \_ DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-630">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="5829a-631">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-631">**DWORD**</span></span> | <span data-ttu-id="5829a-632">X</span><span class="sxs-lookup"><span data-stu-id="5829a-632">X</span></span> | <span data-ttu-id="5829a-633">X</span><span class="sxs-lookup"><span data-stu-id="5829a-633">X</span></span> | <span data-ttu-id="5829a-634">X</span><span class="sxs-lookup"><span data-stu-id="5829a-634">X</span></span> | <span data-ttu-id="5829a-635">X</span><span class="sxs-lookup"><span data-stu-id="5829a-635">X</span></span> | \- |
| <span data-ttu-id="5829a-636">TIMEOUT DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-636">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="5829a-637">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-637">**DWORD**</span></span> | <span data-ttu-id="5829a-638">X</span><span class="sxs-lookup"><span data-stu-id="5829a-638">X</span></span> | <span data-ttu-id="5829a-639">X</span><span class="sxs-lookup"><span data-stu-id="5829a-639">X</span></span> | <span data-ttu-id="5829a-640">X</span><span class="sxs-lookup"><span data-stu-id="5829a-640">X</span></span> | <span data-ttu-id="5829a-641">X</span><span class="sxs-lookup"><span data-stu-id="5829a-641">X</span></span> | \- |
| <span data-ttu-id="5829a-642">INFORMAZIONI DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-642">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="5829a-643">**INFORMAZIONI DI \_ CONNESSIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-643">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="5829a-644">X</span><span class="sxs-lookup"><span data-stu-id="5829a-644">X</span></span> | <span data-ttu-id="5829a-645">X</span><span class="sxs-lookup"><span data-stu-id="5829a-645">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-646">STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V0</span><span class="sxs-lookup"><span data-stu-id="5829a-646">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="5829a-647">**TCP \_ INFO \_ v0**</span><span class="sxs-lookup"><span data-stu-id="5829a-647">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="5829a-648">X</span><span class="sxs-lookup"><span data-stu-id="5829a-648">X</span></span> | <span data-ttu-id="5829a-649">X</span><span class="sxs-lookup"><span data-stu-id="5829a-649">X</span></span> | \- | <span data-ttu-id="5829a-650">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="5829a-650">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="5829a-651">STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V1</span><span class="sxs-lookup"><span data-stu-id="5829a-651">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="5829a-652">**TCP \_ INFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="5829a-652">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="5829a-653">X</span><span class="sxs-lookup"><span data-stu-id="5829a-653">X</span></span> | <span data-ttu-id="5829a-654">X</span><span class="sxs-lookup"><span data-stu-id="5829a-654">X</span></span> | \- | <span data-ttu-id="5829a-655">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="5829a-655">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="5829a-656">VALORE DI CONTESTO \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-656">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="5829a-657">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-657">**DWORD\_PTR**</span></span> | <span data-ttu-id="5829a-658">X</span><span class="sxs-lookup"><span data-stu-id="5829a-658">X</span></span> | <span data-ttu-id="5829a-659">X</span><span class="sxs-lookup"><span data-stu-id="5829a-659">X</span></span> | <span data-ttu-id="5829a-660">X</span><span class="sxs-lookup"><span data-stu-id="5829a-660">X</span></span> | <span data-ttu-id="5829a-661">X</span><span class="sxs-lookup"><span data-stu-id="5829a-661">X</span></span> | \- |
| <span data-ttu-id="5829a-662">\_ \_ DECOMPRESSIONE DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-662">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="5829a-663">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-663">**DWORD**</span></span> | <span data-ttu-id="5829a-664">X</span><span class="sxs-lookup"><span data-stu-id="5829a-664">X</span></span> | <span data-ttu-id="5829a-665">X</span><span class="sxs-lookup"><span data-stu-id="5829a-665">X</span></span> | \- | <span data-ttu-id="5829a-666">X</span><span class="sxs-lookup"><span data-stu-id="5829a-666">X</span></span> | <span data-ttu-id="5829a-667">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5829a-667">Windows 8.1</span></span> |
| <span data-ttu-id="5829a-668">OPZIONE WINHTTP \_ PER \_ DISABILITARE \_ LA COMPILAZIONE DELLA CATENA \_ DI \_ CERTIFICATI</span><span class="sxs-lookup"><span data-stu-id="5829a-668">WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING</span></span><br/><span data-ttu-id="5829a-669">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-669">**BOOL**</span></span> | <span data-ttu-id="5829a-670">X</span><span class="sxs-lookup"><span data-stu-id="5829a-670">X</span></span> | \- | \- | <span data-ttu-id="5829a-671">X</span><span class="sxs-lookup"><span data-stu-id="5829a-671">X</span></span> | <span data-ttu-id="5829a-672">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-672">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-673">OPZIONE WINHTTP \_ \_ DISABILITA \_ FUNZIONALITÀ</span><span class="sxs-lookup"><span data-stu-id="5829a-673">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="5829a-674">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-674">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-675">X</span><span class="sxs-lookup"><span data-stu-id="5829a-675">X</span></span> | \- | <span data-ttu-id="5829a-676">X</span><span class="sxs-lookup"><span data-stu-id="5829a-676">X</span></span> | \- |
| <span data-ttu-id="5829a-677">OPZIONE WINHTTP \_ \_ DISABILITA IL \_ \_ FALLBACK DEL \_ PROTOCOLLO SICURO</span><span class="sxs-lookup"><span data-stu-id="5829a-677">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="5829a-678">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-678">**BOOL**</span></span> | <span data-ttu-id="5829a-679">X</span><span class="sxs-lookup"><span data-stu-id="5829a-679">X</span></span> | \- | \- | <span data-ttu-id="5829a-680">X</span><span class="sxs-lookup"><span data-stu-id="5829a-680">X</span></span> | <span data-ttu-id="5829a-681">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="5829a-681">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="5829a-682">OPZIONE WINHTTP \_ DISABILITA \_ CODA DI \_ \_ FLUSSO</span><span class="sxs-lookup"><span data-stu-id="5829a-682">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="5829a-683">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-683">**BOOL**</span></span> | <span data-ttu-id="5829a-684">X</span><span class="sxs-lookup"><span data-stu-id="5829a-684">X</span></span> | <span data-ttu-id="5829a-685">X</span><span class="sxs-lookup"><span data-stu-id="5829a-685">X</span></span> | \- | <span data-ttu-id="5829a-686">X</span><span class="sxs-lookup"><span data-stu-id="5829a-686">X</span></span> | <span data-ttu-id="5829a-687">Windows 10 versione 1809</span><span class="sxs-lookup"><span data-stu-id="5829a-687">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="5829a-688">OPZIONE WINHTTP \_ \_ - ABILITARE LA \_ FUNZIONALITÀ</span><span class="sxs-lookup"><span data-stu-id="5829a-688">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="5829a-689">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-689">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="5829a-690">X</span><span class="sxs-lookup"><span data-stu-id="5829a-690">X</span></span> | \- |
| <span data-ttu-id="5829a-691">OPZIONE WINHTTP \_ \_ ABILITA PROTOCOLLO \_ \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-691">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="5829a-692">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-692">**DWORD**</span></span> | <span data-ttu-id="5829a-693">X</span><span class="sxs-lookup"><span data-stu-id="5829a-693">X</span></span> | <span data-ttu-id="5829a-694">X</span><span class="sxs-lookup"><span data-stu-id="5829a-694">X</span></span> | \- | <span data-ttu-id="5829a-695">X</span><span class="sxs-lookup"><span data-stu-id="5829a-695">X</span></span> | <span data-ttu-id="5829a-696">Windows 10 versione 1607</span><span class="sxs-lookup"><span data-stu-id="5829a-696">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="5829a-697">OPZIONE WINHTTP \_ \_ ENABLE \_ HTTP2 PLUS CLIENT \_ \_ \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="5829a-697">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="5829a-698">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-698">**BOOL**</span></span> | <span data-ttu-id="5829a-699">X</span><span class="sxs-lookup"><span data-stu-id="5829a-699">X</span></span> | \- | \- | <span data-ttu-id="5829a-700">X</span><span class="sxs-lookup"><span data-stu-id="5829a-700">X</span></span> | <span data-ttu-id="5829a-701">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-701">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-702">OPZIONE WINHTTP \_ \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="5829a-702">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="5829a-703">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-703">**DWORD**</span></span> | \- | \- | <span data-ttu-id="5829a-704">X</span><span class="sxs-lookup"><span data-stu-id="5829a-704">X</span></span> | <span data-ttu-id="5829a-705">X</span><span class="sxs-lookup"><span data-stu-id="5829a-705">X</span></span> | \- |
| <span data-ttu-id="5829a-706">OPZIONE WINHTTP \_ \_ ENCODE \_ EXTRA</span><span class="sxs-lookup"><span data-stu-id="5829a-706">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="5829a-707">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-707">**BOOL**</span></span> | <span data-ttu-id="5829a-708">X</span><span class="sxs-lookup"><span data-stu-id="5829a-708">X</span></span> | <span data-ttu-id="5829a-709">X</span><span class="sxs-lookup"><span data-stu-id="5829a-709">X</span></span> | \- | <span data-ttu-id="5829a-710">X</span><span class="sxs-lookup"><span data-stu-id="5829a-710">X</span></span> | <span data-ttu-id="5829a-711">Windows 10 versione 1803</span><span class="sxs-lookup"><span data-stu-id="5829a-711">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="5829a-712">OPZIONE WINHTTP \_ \_ SCADENZA \_ CONNESSIONE</span><span class="sxs-lookup"><span data-stu-id="5829a-712">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="5829a-713">N/D</span><span class="sxs-lookup"><span data-stu-id="5829a-713">N/A</span></span> | \- | <span data-ttu-id="5829a-714">X</span><span class="sxs-lookup"><span data-stu-id="5829a-714">X</span></span> | \- | <span data-ttu-id="5829a-715">X</span><span class="sxs-lookup"><span data-stu-id="5829a-715">X</span></span> | <span data-ttu-id="5829a-716">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="5829a-716">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="5829a-717">ERRORE ESTESO \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-717">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="5829a-718">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-718">**DWORD**</span></span> | <span data-ttu-id="5829a-719">X</span><span class="sxs-lookup"><span data-stu-id="5829a-719">X</span></span> | <span data-ttu-id="5829a-720">X</span><span class="sxs-lookup"><span data-stu-id="5829a-720">X</span></span> | <span data-ttu-id="5829a-721">X</span><span class="sxs-lookup"><span data-stu-id="5829a-721">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-722">OPZIONE WINHTTP \_ \_ PRIMA CONNESSIONE \_ \_ DISPONIBILE</span><span class="sxs-lookup"><span data-stu-id="5829a-722">WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION</span></span><br/><span data-ttu-id="5829a-723">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-723">**BOOL**</span></span> | <span data-ttu-id="5829a-724">X</span><span class="sxs-lookup"><span data-stu-id="5829a-724">X</span></span> | \- | \- | <span data-ttu-id="5829a-725">X</span><span class="sxs-lookup"><span data-stu-id="5829a-725">X</span></span> | <span data-ttu-id="5829a-726">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-726">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-727">CREDS \_ \_ PROXY GLOBALI \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-727">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="5829a-728">**WINHTTP \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="5829a-728">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="5829a-729">X</span><span class="sxs-lookup"><span data-stu-id="5829a-729">X</span></span> | <span data-ttu-id="5829a-730">X</span><span class="sxs-lookup"><span data-stu-id="5829a-730">X</span></span> | \- | <span data-ttu-id="5829a-731">X</span><span class="sxs-lookup"><span data-stu-id="5829a-731">X</span></span> | \- |
| <span data-ttu-id="5829a-732">CREDS \_ \_ GLOBALI DEL SERVER \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-732">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="5829a-733">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="5829a-733">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="5829a-734">X</span><span class="sxs-lookup"><span data-stu-id="5829a-734">X</span></span> | <span data-ttu-id="5829a-735">X</span><span class="sxs-lookup"><span data-stu-id="5829a-735">X</span></span> | \- | <span data-ttu-id="5829a-736">X</span><span class="sxs-lookup"><span data-stu-id="5829a-736">X</span></span> | \- |
| <span data-ttu-id="5829a-737">TIPO DI \_ HANDLE DI \_ OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-737">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="5829a-738">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-738">**DWORD**</span></span> | <span data-ttu-id="5829a-739">X</span><span class="sxs-lookup"><span data-stu-id="5829a-739">X</span></span> | <span data-ttu-id="5829a-740">X</span><span class="sxs-lookup"><span data-stu-id="5829a-740">X</span></span> | <span data-ttu-id="5829a-741">X</span><span class="sxs-lookup"><span data-stu-id="5829a-741">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-742">OPZIONE \_ \_ HTTP \_ PROTOCOL REQUIRED DI WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-742">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="5829a-743">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-743">**BOOL**</span></span> | <span data-ttu-id="5829a-744">X</span><span class="sxs-lookup"><span data-stu-id="5829a-744">X</span></span> | <span data-ttu-id="5829a-745">X</span><span class="sxs-lookup"><span data-stu-id="5829a-745">X</span></span> | \- | <span data-ttu-id="5829a-746">X</span><span class="sxs-lookup"><span data-stu-id="5829a-746">X</span></span> | <span data-ttu-id="5829a-747">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="5829a-747">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="5829a-748">PROTOCOLLO \_ \_ HTTP DELL'OPZIONE WINHTTP \_ \_ USATO</span><span class="sxs-lookup"><span data-stu-id="5829a-748">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="5829a-749">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-749">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-750">X</span><span class="sxs-lookup"><span data-stu-id="5829a-750">X</span></span> | <span data-ttu-id="5829a-751">X</span><span class="sxs-lookup"><span data-stu-id="5829a-751">X</span></span> | \- | <span data-ttu-id="5829a-752">Windows 10 versione 1607</span><span class="sxs-lookup"><span data-stu-id="5829a-752">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="5829a-753">VERSIONE \_ \_ HTTP DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-753">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="5829a-754">**INFORMAZIONI \_ SULLA VERSIONE \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-754">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="5829a-755">X</span><span class="sxs-lookup"><span data-stu-id="5829a-755">X</span></span> | <span data-ttu-id="5829a-756">X</span><span class="sxs-lookup"><span data-stu-id="5829a-756">X</span></span> | <span data-ttu-id="5829a-757">X</span><span class="sxs-lookup"><span data-stu-id="5829a-757">X</span></span> | <span data-ttu-id="5829a-758">X</span><span class="sxs-lookup"><span data-stu-id="5829a-758">X</span></span> | \- |
| <span data-ttu-id="5829a-759">OPZIONE \_ \_ WINHTTP \_ KEEPALIVE HTTP2</span><span class="sxs-lookup"><span data-stu-id="5829a-759">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="5829a-760">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-760">**DWORD**</span></span> | <span data-ttu-id="5829a-761">X</span><span class="sxs-lookup"><span data-stu-id="5829a-761">X</span></span> | \- | \- | <span data-ttu-id="5829a-762">X</span><span class="sxs-lookup"><span data-stu-id="5829a-762">X</span></span> | <span data-ttu-id="5829a-763">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-763">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-764">OPZIONE WINHTTP \_ \_ HTTP2 \_ PLUS TRANSFER \_ \_ ENCODING</span><span class="sxs-lookup"><span data-stu-id="5829a-764">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="5829a-765">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-765">**BOOL**</span></span> | <span data-ttu-id="5829a-766">X</span><span class="sxs-lookup"><span data-stu-id="5829a-766">X</span></span> | <span data-ttu-id="5829a-767">X</span><span class="sxs-lookup"><span data-stu-id="5829a-767">X</span></span> | \- | <span data-ttu-id="5829a-768">X</span><span class="sxs-lookup"><span data-stu-id="5829a-768">X</span></span> | <span data-ttu-id="5829a-769">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-769">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-770">OPZIONE WINHTTP \_ \_ IGNORA REVOCA CERTIFICATO \_ \_ \_ OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5829a-770">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="5829a-771">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-771">**BOOL**</span></span> | \- | <span data-ttu-id="5829a-772">X</span><span class="sxs-lookup"><span data-stu-id="5829a-772">X</span></span> | \- | <span data-ttu-id="5829a-773">X</span><span class="sxs-lookup"><span data-stu-id="5829a-773">X</span></span> | <span data-ttu-id="5829a-774">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="5829a-774">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="5829a-775">OPZIONE \_ \_ IPV6 \_ FAST \_ FALLBACK WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-775">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="5829a-776">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-776">**BOOL**</span></span> | <span data-ttu-id="5829a-777">X</span><span class="sxs-lookup"><span data-stu-id="5829a-777">X</span></span> | \- | \- | <span data-ttu-id="5829a-778">X</span><span class="sxs-lookup"><span data-stu-id="5829a-778">X</span></span> | <span data-ttu-id="5829a-779">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="5829a-779">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="5829a-780">L'OPZIONE WINHTTP \_ È LA RISPOSTA DI CONNESSIONE \_ \_ \_ \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="5829a-780">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="5829a-781">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-781">**BOOL**</span></span> | <span data-ttu-id="5829a-782">X</span><span class="sxs-lookup"><span data-stu-id="5829a-782">X</span></span> | <span data-ttu-id="5829a-783">X</span><span class="sxs-lookup"><span data-stu-id="5829a-783">X</span></span> | <span data-ttu-id="5829a-784">X</span><span class="sxs-lookup"><span data-stu-id="5829a-784">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-785">OPZIONE \_ WINHTTP \_ MAX \_ CONNS \_ PER \_ 1 \_ 0 \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="5829a-785">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="5829a-786">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-786">**DWORD**</span></span> | <span data-ttu-id="5829a-787">X</span><span class="sxs-lookup"><span data-stu-id="5829a-787">X</span></span> | \- | <span data-ttu-id="5829a-788">X</span><span class="sxs-lookup"><span data-stu-id="5829a-788">X</span></span> | <span data-ttu-id="5829a-789">X</span><span class="sxs-lookup"><span data-stu-id="5829a-789">X</span></span> | \- |
| <span data-ttu-id="5829a-790">OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="5829a-790">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="5829a-791">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-791">**DWORD**</span></span> | <span data-ttu-id="5829a-792">X</span><span class="sxs-lookup"><span data-stu-id="5829a-792">X</span></span> | \- | <span data-ttu-id="5829a-793">X</span><span class="sxs-lookup"><span data-stu-id="5829a-793">X</span></span> | <span data-ttu-id="5829a-794">X</span><span class="sxs-lookup"><span data-stu-id="5829a-794">X</span></span> | \- |
| <span data-ttu-id="5829a-795">OPZIONE WINHTTP \_ \_ NUMERO MASSIMO DI \_ \_ \_ REINDIRIZZAMENTI HTTP AUTOMATICI</span><span class="sxs-lookup"><span data-stu-id="5829a-795">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="5829a-796">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-796">**DWORD**</span></span> | <span data-ttu-id="5829a-797">X</span><span class="sxs-lookup"><span data-stu-id="5829a-797">X</span></span> | <span data-ttu-id="5829a-798">X</span><span class="sxs-lookup"><span data-stu-id="5829a-798">X</span></span> | <span data-ttu-id="5829a-799">X</span><span class="sxs-lookup"><span data-stu-id="5829a-799">X</span></span> | <span data-ttu-id="5829a-800">X</span><span class="sxs-lookup"><span data-stu-id="5829a-800">X</span></span> | \- |
| <span data-ttu-id="5829a-801">\_L'OPZIONE \_ WINHTTP MAX HTTP STATUS \_ \_ \_ CONTINUE</span><span class="sxs-lookup"><span data-stu-id="5829a-801">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="5829a-802">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-802">**DWORD**</span></span> | <span data-ttu-id="5829a-803">X</span><span class="sxs-lookup"><span data-stu-id="5829a-803">X</span></span> | <span data-ttu-id="5829a-804">X</span><span class="sxs-lookup"><span data-stu-id="5829a-804">X</span></span> | <span data-ttu-id="5829a-805">X</span><span class="sxs-lookup"><span data-stu-id="5829a-805">X</span></span> | <span data-ttu-id="5829a-806">X</span><span class="sxs-lookup"><span data-stu-id="5829a-806">X</span></span> | \- |
| <span data-ttu-id="5829a-807">OPZIONE WINHTTP \_ \_ MAX RESPONSE DRAIN \_ \_ \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="5829a-807">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="5829a-808">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-808">**DWORD**</span></span> | <span data-ttu-id="5829a-809">X</span><span class="sxs-lookup"><span data-stu-id="5829a-809">X</span></span> | <span data-ttu-id="5829a-810">X</span><span class="sxs-lookup"><span data-stu-id="5829a-810">X</span></span> | <span data-ttu-id="5829a-811">X</span><span class="sxs-lookup"><span data-stu-id="5829a-811">X</span></span> | <span data-ttu-id="5829a-812">X</span><span class="sxs-lookup"><span data-stu-id="5829a-812">X</span></span> | \- |
| <span data-ttu-id="5829a-813">DIMENSIONI MASSIME \_ INTESTAZIONE \_ RISPOSTA \_ \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-813">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="5829a-814">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-814">**DWORD**</span></span> | <span data-ttu-id="5829a-815">X</span><span class="sxs-lookup"><span data-stu-id="5829a-815">X</span></span> | <span data-ttu-id="5829a-816">X</span><span class="sxs-lookup"><span data-stu-id="5829a-816">X</span></span> | <span data-ttu-id="5829a-817">X</span><span class="sxs-lookup"><span data-stu-id="5829a-817">X</span></span> | <span data-ttu-id="5829a-818">X</span><span class="sxs-lookup"><span data-stu-id="5829a-818">X</span></span> | \- |
| <span data-ttu-id="5829a-819">HANDLE PADRE \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-819">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="5829a-820">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="5829a-820">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="5829a-821">X</span><span class="sxs-lookup"><span data-stu-id="5829a-821">X</span></span> | <span data-ttu-id="5829a-822">X</span><span class="sxs-lookup"><span data-stu-id="5829a-822">X</span></span> | <span data-ttu-id="5829a-823">X</span><span class="sxs-lookup"><span data-stu-id="5829a-823">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-824">TESTO \_ \_ \_ COBRANDING DELL'OPZIONE PASSPORT WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-824">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="5829a-825">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-825">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-826">X</span><span class="sxs-lookup"><span data-stu-id="5829a-826">X</span></span> | <span data-ttu-id="5829a-827">X</span><span class="sxs-lookup"><span data-stu-id="5829a-827">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-828">URL \_ \_ \_ COBRANDING DELL'OPZIONE PASSPORT WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-828">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="5829a-829">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-829">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-830">X</span><span class="sxs-lookup"><span data-stu-id="5829a-830">X</span></span> | <span data-ttu-id="5829a-831">X</span><span class="sxs-lookup"><span data-stu-id="5829a-831">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-832">URL \_ RESTITUITO \_ PASSPORT DELL'OPZIONE WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="5829a-832">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="5829a-833">**Lpvoid**</span><span class="sxs-lookup"><span data-stu-id="5829a-833">**LPVOID**</span></span> | \- | <span data-ttu-id="5829a-834">X</span><span class="sxs-lookup"><span data-stu-id="5829a-834">X</span></span> | <span data-ttu-id="5829a-835">X</span><span class="sxs-lookup"><span data-stu-id="5829a-835">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-836">OPZIONE \_ \_ WINHTTP - \_ DISCONNESSIONE PASSPORT \_</span><span class="sxs-lookup"><span data-stu-id="5829a-836">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="5829a-837">**Lpvoid**</span><span class="sxs-lookup"><span data-stu-id="5829a-837">**LPVOID**</span></span> | <span data-ttu-id="5829a-838">X</span><span class="sxs-lookup"><span data-stu-id="5829a-838">X</span></span> | \- | \- | <span data-ttu-id="5829a-839">X</span><span class="sxs-lookup"><span data-stu-id="5829a-839">X</span></span> | \- |
| <span data-ttu-id="5829a-840">PASSWORD \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-840">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="5829a-841">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-841">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-842">X</span><span class="sxs-lookup"><span data-stu-id="5829a-842">X</span></span> | <span data-ttu-id="5829a-843">X</span><span class="sxs-lookup"><span data-stu-id="5829a-843">X</span></span> | <span data-ttu-id="5829a-844">X</span><span class="sxs-lookup"><span data-stu-id="5829a-844">X</span></span> | \- |
| <span data-ttu-id="5829a-845">PROXY \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-845">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="5829a-846">**INFORMAZIONI SUL PROXY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-846">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="5829a-847">X</span><span class="sxs-lookup"><span data-stu-id="5829a-847">X</span></span> | <span data-ttu-id="5829a-848">X</span><span class="sxs-lookup"><span data-stu-id="5829a-848">X</span></span> | <span data-ttu-id="5829a-849">X</span><span class="sxs-lookup"><span data-stu-id="5829a-849">X</span></span> | <span data-ttu-id="5829a-850">X</span><span class="sxs-lookup"><span data-stu-id="5829a-850">X</span></span> | \- |
| <span data-ttu-id="5829a-851">PASSWORD PROXY \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-851">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="5829a-852">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-852">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-853">X</span><span class="sxs-lookup"><span data-stu-id="5829a-853">X</span></span> | <span data-ttu-id="5829a-854">X</span><span class="sxs-lookup"><span data-stu-id="5829a-854">X</span></span> | <span data-ttu-id="5829a-855">X</span><span class="sxs-lookup"><span data-stu-id="5829a-855">X</span></span> | \- |
| <span data-ttu-id="5829a-856">NOME \_ \_ SPN PROXY \_ DELL'OPZIONE WINHTTP \_ USATO</span><span class="sxs-lookup"><span data-stu-id="5829a-856">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="5829a-857">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-857">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-858">X</span><span class="sxs-lookup"><span data-stu-id="5829a-858">X</span></span> | <span data-ttu-id="5829a-859">X</span><span class="sxs-lookup"><span data-stu-id="5829a-859">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-860">NOME UTENTE \_ \_ PROXY DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-860">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="5829a-861">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-861">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-862">X</span><span class="sxs-lookup"><span data-stu-id="5829a-862">X</span></span> | <span data-ttu-id="5829a-863">X</span><span class="sxs-lookup"><span data-stu-id="5829a-863">X</span></span> | <span data-ttu-id="5829a-864">X</span><span class="sxs-lookup"><span data-stu-id="5829a-864">X</span></span> | \- |
| <span data-ttu-id="5829a-865">DIMENSIONI DEL \_ \_ BUFFER DI LETTURA \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-865">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="5829a-866">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-866">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-867">X</span><span class="sxs-lookup"><span data-stu-id="5829a-867">X</span></span> | <span data-ttu-id="5829a-868">X</span><span class="sxs-lookup"><span data-stu-id="5829a-868">X</span></span> | <span data-ttu-id="5829a-869">X</span><span class="sxs-lookup"><span data-stu-id="5829a-869">X</span></span> | \- |
| <span data-ttu-id="5829a-870">RISPOSTA DI CONNESSIONE \_ PROXY \_ DI RICEZIONE \_ \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-870">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="5829a-871">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-871">**BOOL**</span></span> | <span data-ttu-id="5829a-872">X</span><span class="sxs-lookup"><span data-stu-id="5829a-872">X</span></span> | <span data-ttu-id="5829a-873">X</span><span class="sxs-lookup"><span data-stu-id="5829a-873">X</span></span> | \- | <span data-ttu-id="5829a-874">X</span><span class="sxs-lookup"><span data-stu-id="5829a-874">X</span></span> | \- |
| <span data-ttu-id="5829a-875">TIMEOUT DI \_ RICEZIONE \_ RISPOSTA PER \_ L'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-875">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="5829a-876">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-876">**DWORD**</span></span> | <span data-ttu-id="5829a-877">X</span><span class="sxs-lookup"><span data-stu-id="5829a-877">X</span></span> | <span data-ttu-id="5829a-878">X</span><span class="sxs-lookup"><span data-stu-id="5829a-878">X</span></span> | <span data-ttu-id="5829a-879">X</span><span class="sxs-lookup"><span data-stu-id="5829a-879">X</span></span> | <span data-ttu-id="5829a-880">X</span><span class="sxs-lookup"><span data-stu-id="5829a-880">X</span></span> | \- |
| <span data-ttu-id="5829a-881">TIMEOUT RICEZIONE OPZIONE WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5829a-881">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="5829a-882">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-882">**DWORD**</span></span> | <span data-ttu-id="5829a-883">X</span><span class="sxs-lookup"><span data-stu-id="5829a-883">X</span></span> | <span data-ttu-id="5829a-884">X</span><span class="sxs-lookup"><span data-stu-id="5829a-884">X</span></span> | <span data-ttu-id="5829a-885">X</span><span class="sxs-lookup"><span data-stu-id="5829a-885">X</span></span> | <span data-ttu-id="5829a-886">X</span><span class="sxs-lookup"><span data-stu-id="5829a-886">X</span></span> | \- |
| <span data-ttu-id="5829a-887">CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-887">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="5829a-888">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-888">**DWORD**</span></span> | <span data-ttu-id="5829a-889">X</span><span class="sxs-lookup"><span data-stu-id="5829a-889">X</span></span> | <span data-ttu-id="5829a-890">X</span><span class="sxs-lookup"><span data-stu-id="5829a-890">X</span></span> | <span data-ttu-id="5829a-891">X</span><span class="sxs-lookup"><span data-stu-id="5829a-891">X</span></span> | <span data-ttu-id="5829a-892">X</span><span class="sxs-lookup"><span data-stu-id="5829a-892">X</span></span> | \- |
| <span data-ttu-id="5829a-893">OPZIONE WINHTTP \_ \_ RIFIUTA \_ USERPWD \_ \_ NELL'URL</span><span class="sxs-lookup"><span data-stu-id="5829a-893">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="5829a-894">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-894">**BOOL**</span></span> | \- | <span data-ttu-id="5829a-895">X</span><span class="sxs-lookup"><span data-stu-id="5829a-895">X</span></span> | \- | <span data-ttu-id="5829a-896">X</span><span class="sxs-lookup"><span data-stu-id="5829a-896">X</span></span> | \- |
| <span data-ttu-id="5829a-897">PRIORITÀ DI \_ RICHIESTA \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-897">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="5829a-898">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-898">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-899">X</span><span class="sxs-lookup"><span data-stu-id="5829a-899">X</span></span> | <span data-ttu-id="5829a-900">X</span><span class="sxs-lookup"><span data-stu-id="5829a-900">X</span></span> | <span data-ttu-id="5829a-901">X</span><span class="sxs-lookup"><span data-stu-id="5829a-901">X</span></span> | \- |
| <span data-ttu-id="5829a-902">STATISTICHE DI \_ RICHIESTA \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-902">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="5829a-903">**STATISTICHE DELLE \_ RICHIESTE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-903">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="5829a-904">X</span><span class="sxs-lookup"><span data-stu-id="5829a-904">X</span></span> | <span data-ttu-id="5829a-905">X</span><span class="sxs-lookup"><span data-stu-id="5829a-905">X</span></span> | \- | <span data-ttu-id="5829a-906">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="5829a-906">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="5829a-907">TEMPI DI RICHIESTA \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-907">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="5829a-908">**TEMPI DI RICHIESTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5829a-908">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="5829a-909">X</span><span class="sxs-lookup"><span data-stu-id="5829a-909">X</span></span> | <span data-ttu-id="5829a-910">X</span><span class="sxs-lookup"><span data-stu-id="5829a-910">X</span></span> | \- | <span data-ttu-id="5829a-911">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="5829a-911">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="5829a-912">OPZIONE WINHTTP \_ \_ REQUIRE STREAM \_ \_ END</span><span class="sxs-lookup"><span data-stu-id="5829a-912">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="5829a-913">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-913">**BOOL**</span></span> | <span data-ttu-id="5829a-914">X</span><span class="sxs-lookup"><span data-stu-id="5829a-914">X</span></span> | <span data-ttu-id="5829a-915">X</span><span class="sxs-lookup"><span data-stu-id="5829a-915">X</span></span> | \- | <span data-ttu-id="5829a-916">X</span><span class="sxs-lookup"><span data-stu-id="5829a-916">X</span></span> | <span data-ttu-id="5829a-917">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-917">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-918">NOME HOST \_ DI \_ RISOLUZIONE \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-918">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="5829a-919">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-919">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-920">X</span><span class="sxs-lookup"><span data-stu-id="5829a-920">X</span></span> | \- | <span data-ttu-id="5829a-921">X</span><span class="sxs-lookup"><span data-stu-id="5829a-921">X</span></span> | <span data-ttu-id="5829a-922">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-922">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-923">TIMEOUT RISOLUZIONE \_ DELL'OPZIONE WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="5829a-923">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="5829a-924">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-924">**DWORD**</span></span> | <span data-ttu-id="5829a-925">X</span><span class="sxs-lookup"><span data-stu-id="5829a-925">X</span></span> | <span data-ttu-id="5829a-926">X</span><span class="sxs-lookup"><span data-stu-id="5829a-926">X</span></span> | <span data-ttu-id="5829a-927">X</span><span class="sxs-lookup"><span data-stu-id="5829a-927">X</span></span> | <span data-ttu-id="5829a-928">X</span><span class="sxs-lookup"><span data-stu-id="5829a-928">X</span></span> | \- |
| <span data-ttu-id="5829a-929">PROTOCOLLI SICURI \_ \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-929">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="5829a-930">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-930">**DWORD**</span></span> | <span data-ttu-id="5829a-931">X</span><span class="sxs-lookup"><span data-stu-id="5829a-931">X</span></span> | \- | \- | <span data-ttu-id="5829a-932">X</span><span class="sxs-lookup"><span data-stu-id="5829a-932">X</span></span> | \- |
| <span data-ttu-id="5829a-933">STRUCT \_ DEL CERTIFICATO DI SICUREZZA \_ \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-933">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="5829a-934">**INFORMAZIONI SUL \_ CERTIFICATO \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="5829a-934">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="5829a-935">X</span><span class="sxs-lookup"><span data-stu-id="5829a-935">X</span></span> | <span data-ttu-id="5829a-936">X</span><span class="sxs-lookup"><span data-stu-id="5829a-936">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-937">FLAG DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-937">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="5829a-938">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-938">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-939">X</span><span class="sxs-lookup"><span data-stu-id="5829a-939">X</span></span> | <span data-ttu-id="5829a-940">X</span><span class="sxs-lookup"><span data-stu-id="5829a-940">X</span></span> | <span data-ttu-id="5829a-941">X</span><span class="sxs-lookup"><span data-stu-id="5829a-941">X</span></span> | \- |
| <span data-ttu-id="5829a-942">INFORMAZIONI DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-942">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="5829a-943">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="5829a-943">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="5829a-944">X</span><span class="sxs-lookup"><span data-stu-id="5829a-944">X</span></span> | <span data-ttu-id="5829a-945">X</span><span class="sxs-lookup"><span data-stu-id="5829a-945">X</span></span> | \- | <span data-ttu-id="5829a-946">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="5829a-946">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="5829a-947">BITNESS \_ CHIAVE DI SICUREZZA \_ \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-947">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="5829a-948">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-948">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-949">X</span><span class="sxs-lookup"><span data-stu-id="5829a-949">X</span></span> | <span data-ttu-id="5829a-950">X</span><span class="sxs-lookup"><span data-stu-id="5829a-950">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-951">TIMEOUT INVIO OPZIONE WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5829a-951">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="5829a-952">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-952">**DWORD**</span></span> | <span data-ttu-id="5829a-953">X</span><span class="sxs-lookup"><span data-stu-id="5829a-953">X</span></span> | <span data-ttu-id="5829a-954">X</span><span class="sxs-lookup"><span data-stu-id="5829a-954">X</span></span> | <span data-ttu-id="5829a-955">X</span><span class="sxs-lookup"><span data-stu-id="5829a-955">X</span></span> | <span data-ttu-id="5829a-956">X</span><span class="sxs-lookup"><span data-stu-id="5829a-956">X</span></span> | \- |
| <span data-ttu-id="5829a-957">OPZIONE WINHTTP \_ \_ SERVER \_ CBT</span><span class="sxs-lookup"><span data-stu-id="5829a-957">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="5829a-958">[**Associazioni SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="5829a-958">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="5829a-959">X</span><span class="sxs-lookup"><span data-stu-id="5829a-959">X</span></span> | <span data-ttu-id="5829a-960">X</span><span class="sxs-lookup"><span data-stu-id="5829a-960">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-961">CONTESTO CATENA \_ DI CERTIFICATI DEL SERVER \_ \_ \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-961">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="5829a-962">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="5829a-962">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="5829a-963">X</span><span class="sxs-lookup"><span data-stu-id="5829a-963">X</span></span> | <span data-ttu-id="5829a-964">X</span><span class="sxs-lookup"><span data-stu-id="5829a-964">X</span></span> | \- | <span data-ttu-id="5829a-965">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="5829a-965">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="5829a-966">CONTESTO DEL CERTIFICATO \_ \_ DEL SERVER \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-966">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="5829a-967">**CONTESTO DEL CERTIFICATO**</span><span class="sxs-lookup"><span data-stu-id="5829a-967">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="5829a-968">X</span><span class="sxs-lookup"><span data-stu-id="5829a-968">X</span></span> | <span data-ttu-id="5829a-969">X</span><span class="sxs-lookup"><span data-stu-id="5829a-969">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-970">NOME \_ \_ SPN DEL SERVER \_ DELL'OPZIONE WINHTTP \_ USATO</span><span class="sxs-lookup"><span data-stu-id="5829a-970">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="5829a-971">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-971">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-972">X</span><span class="sxs-lookup"><span data-stu-id="5829a-972">X</span></span> | <span data-ttu-id="5829a-973">X</span><span class="sxs-lookup"><span data-stu-id="5829a-973">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-974">NOME \_ \_ SPN DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-974">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="5829a-975">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-975">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-976">X</span><span class="sxs-lookup"><span data-stu-id="5829a-976">X</span></span> | \- | <span data-ttu-id="5829a-977">X</span><span class="sxs-lookup"><span data-stu-id="5829a-977">X</span></span> | \- |
| <span data-ttu-id="5829a-978">CODICE DI ERRORE \_ DEL \_ FLUSSO \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-978">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="5829a-979">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-979">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-980">X</span><span class="sxs-lookup"><span data-stu-id="5829a-980">X</span></span> | <span data-ttu-id="5829a-981">X</span><span class="sxs-lookup"><span data-stu-id="5829a-981">X</span></span> | \- | <span data-ttu-id="5829a-982">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-982">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-983">OPZIONE WINHTTP \_ \_ TCP FAST \_ \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="5829a-983">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="5829a-984">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-984">**BOOL**</span></span> | <span data-ttu-id="5829a-985">X</span><span class="sxs-lookup"><span data-stu-id="5829a-985">X</span></span> | \- | \- | <span data-ttu-id="5829a-986">X</span><span class="sxs-lookup"><span data-stu-id="5829a-986">X</span></span> | <span data-ttu-id="5829a-987">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="5829a-987">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="5829a-988">OPZIONE \_ \_ WINHTTP TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="5829a-988">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="5829a-989">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="5829a-989">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="5829a-990">X</span><span class="sxs-lookup"><span data-stu-id="5829a-990">X</span></span> | \- | \- | <span data-ttu-id="5829a-991">X</span><span class="sxs-lookup"><span data-stu-id="5829a-991">X</span></span> | <span data-ttu-id="5829a-992">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="5829a-992">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="5829a-993">OPZIONE WINHTTP \_ \_ TLS FALSE \_ \_ START</span><span class="sxs-lookup"><span data-stu-id="5829a-993">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="5829a-994">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-994">**BOOL**</span></span> | <span data-ttu-id="5829a-995">X</span><span class="sxs-lookup"><span data-stu-id="5829a-995">X</span></span> | \- | \- | <span data-ttu-id="5829a-996">X</span><span class="sxs-lookup"><span data-stu-id="5829a-996">X</span></span> | <span data-ttu-id="5829a-997">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="5829a-997">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="5829a-998">OPZIONE WINHTTP \_ \_ \_ \_ FALLBACK NON SICURO DEL PROTOCOLLO TLS \_</span><span class="sxs-lookup"><span data-stu-id="5829a-998">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="5829a-999">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-999">**BOOL**</span></span> | <span data-ttu-id="5829a-1000">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1000">X</span></span> | \- | \- | <span data-ttu-id="5829a-1001">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1001">X</span></span> | <span data-ttu-id="5829a-1002">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="5829a-1002">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="5829a-1003">EVENTO NOTIFICA \_ \_ DI SCARICAMENTO \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-1003">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="5829a-1004">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="5829a-1004">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="5829a-1005">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1005">X</span></span> | \- | \- | <span data-ttu-id="5829a-1006">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1006">X</span></span> | \- |
| <span data-ttu-id="5829a-1007">ANALISI \_ \_ DELL'INTESTAZIONE NON SICURA \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-1007">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="5829a-1008">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-1008">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-1009">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1009">X</span></span> | \- | <span data-ttu-id="5829a-1010">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1010">X</span></span> | \- |
| <span data-ttu-id="5829a-1011">AGGIORNAMENTO \_ DELL'OPZIONE WINHTTP \_ AL WEB \_ \_ \_ SOCKET</span><span class="sxs-lookup"><span data-stu-id="5829a-1011">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="5829a-1012">N/D</span><span class="sxs-lookup"><span data-stu-id="5829a-1012">N/A</span></span> | \- | <span data-ttu-id="5829a-1013">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1013">X</span></span> | \- | <span data-ttu-id="5829a-1014">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1014">X</span></span> | \- |
| <span data-ttu-id="5829a-1015">URL DELL'OPZIONE WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="5829a-1015">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="5829a-1016">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-1016">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-1017">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1017">X</span></span> | <span data-ttu-id="5829a-1018">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1018">X</span></span> | \- | \- |
| <span data-ttu-id="5829a-1019">L'OPZIONE WINHTTP \_ USA LE CREDENZIALI GLOBALI DEL \_ \_ \_ \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="5829a-1019">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="5829a-1020">**Bool**</span><span class="sxs-lookup"><span data-stu-id="5829a-1020">**BOOL**</span></span> | <span data-ttu-id="5829a-1021">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1021">X</span></span> | <span data-ttu-id="5829a-1022">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1022">X</span></span> | \- | <span data-ttu-id="5829a-1023">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1023">X</span></span> | \- |
| <span data-ttu-id="5829a-1024">OPZIONE WINHTTP \_ \_ AGENTE \_ UTENTE</span><span class="sxs-lookup"><span data-stu-id="5829a-1024">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="5829a-1025">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-1025">**LPWSTR**</span></span> | <span data-ttu-id="5829a-1026">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1026">X</span></span> | \- | <span data-ttu-id="5829a-1027">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1027">X</span></span> | <span data-ttu-id="5829a-1028">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1028">X</span></span> | \- |
| <span data-ttu-id="5829a-1029">NOME UTENTE \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="5829a-1029">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="5829a-1030">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5829a-1030">**LPWSTR**</span></span> | \- | <span data-ttu-id="5829a-1031">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1031">X</span></span> | <span data-ttu-id="5829a-1032">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1032">X</span></span> | <span data-ttu-id="5829a-1033">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1033">X</span></span> | \- |
| <span data-ttu-id="5829a-1034">TIMEOUT CHIUSURA \_ \_ WEB SOCKET \_ DELL'OPZIONE \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-1034">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="5829a-1035">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-1035">**DWORD**</span></span> | \- | \- | <span data-ttu-id="5829a-1036">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1036">X</span></span> | <span data-ttu-id="5829a-1037">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1037">X</span></span> | \- |
| <span data-ttu-id="5829a-1038">OPZIONE WINHTTP \_ \_ INTERVALLO \_ \_ KEEPALIVE DEL WEB \_ SOCKET</span><span class="sxs-lookup"><span data-stu-id="5829a-1038">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="5829a-1039">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-1039">**DWORD**</span></span> | \- | \- | <span data-ttu-id="5829a-1040">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1040">X</span></span> | <span data-ttu-id="5829a-1041">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1041">X</span></span> | \- |
| <span data-ttu-id="5829a-1042">DIMENSIONI BUFFER \_ DI RICEZIONE WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-1042">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="5829a-1043">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-1043">**DWORD**</span></span> | <span data-ttu-id="5829a-1044">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1044">X</span></span> | <span data-ttu-id="5829a-1045">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1045">X</span></span> | <span data-ttu-id="5829a-1046">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1046">X</span></span> | <span data-ttu-id="5829a-1047">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1047">X</span></span> | <span data-ttu-id="5829a-1048">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5829a-1048">Windows 8.1</span></span> |
| <span data-ttu-id="5829a-1049">DIMENSIONI BUFFER \_ DI INVIO WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-1049">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="5829a-1050">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-1050">**DWORD**</span></span> | <span data-ttu-id="5829a-1051">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1051">X</span></span> | <span data-ttu-id="5829a-1052">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1052">X</span></span> | <span data-ttu-id="5829a-1053">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1053">X</span></span> | <span data-ttu-id="5829a-1054">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1054">X</span></span> | <span data-ttu-id="5829a-1055">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5829a-1055">Windows 8.1</span></span> |
| <span data-ttu-id="5829a-1056">CONTEGGIO \_ THREAD DI LAVORO \_ \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-1056">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="5829a-1057">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-1057">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="5829a-1058">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1058">X</span></span> | \- |
| <span data-ttu-id="5829a-1059">DIMENSIONI DEL \_ BUFFER DI \_ SCRITTURA \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-1059">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="5829a-1060">**Dword**</span><span class="sxs-lookup"><span data-stu-id="5829a-1060">**DWORD**</span></span> | \- | <span data-ttu-id="5829a-1061">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1061">X</span></span> | <span data-ttu-id="5829a-1062">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1062">X</span></span> | <span data-ttu-id="5829a-1063">X</span><span class="sxs-lookup"><span data-stu-id="5829a-1063">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="5829a-1064">Per Windows XP e Windows 2000, vedere [Requisiti di run-time.](winhttp-start-page.md)</span><span class="sxs-lookup"><span data-stu-id="5829a-1064">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5829a-1065">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5829a-1065">Requirements</span></span>

| <span data-ttu-id="5829a-1066">Requisito</span><span class="sxs-lookup"><span data-stu-id="5829a-1066">Requirement</span></span> | <span data-ttu-id="5829a-1067">Valore</span><span class="sxs-lookup"><span data-stu-id="5829a-1067">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="5829a-1068">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5829a-1068">Minimum supported client</span></span> | <span data-ttu-id="5829a-1069">Windows XP, Windows 2000 Professional con solo app desktop SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="5829a-1069">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="5829a-1070">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5829a-1070">Minimum supported server</span></span> | <span data-ttu-id="5829a-1071">Solo Windows Server 2003, Windows 2000 Server con app desktop SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="5829a-1071">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="5829a-1072">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5829a-1072">Redistributable</span></span>          | <span data-ttu-id="5829a-1073">WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5829a-1073">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="5829a-1074">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5829a-1074">Header</span></span>                   | <span data-ttu-id="5829a-1075">Winhttp.h</span><span class="sxs-lookup"><span data-stu-id="5829a-1075">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="5829a-1076">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5829a-1076">See also</span></span>

[<span data-ttu-id="5829a-1077">Versioni di WinHTTP</span><span class="sxs-lookup"><span data-stu-id="5829a-1077">WinHTTP Versions</span></span>](winhttp-versions.md)
