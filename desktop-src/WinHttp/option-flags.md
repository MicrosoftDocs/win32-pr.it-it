---
Description: I flag di opzione seguenti sono supportati da WinHttpQueryOption e WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Flag di opzione (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 91a9506225c53893990d4dcdc534293daa6c8e00
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262063"
---
# <a name="option-flags"></a><span data-ttu-id="a8706-103">Flag di opzione</span><span class="sxs-lookup"><span data-stu-id="a8706-103">Option Flags</span></span>

<span data-ttu-id="a8706-104">I flag di opzione seguenti sono supportati [**da WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)</span><span class="sxs-lookup"><span data-stu-id="a8706-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="a8706-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**OPZIONE WINHTTP \_ \_ GARANTITA \_ CALLBACK NON \_ \_ BLOCCANTI**</span><span class="sxs-lookup"><span data-stu-id="a8706-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-106">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="a8706-106">The default is FALSE.</span></span> <span data-ttu-id="a8706-107">Se impostato su TRUE, WinHTTP non garantisce lo stato di avanzamento se i callback di stato sono bloccati dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a8706-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="a8706-108">L'applicazione client deve fare particolare attenzione a eseguire operazioni minime all'interno del callback senza bloccarsi, per restituire il più rapidamente possibile e, in particolare, non deve attendere le chiamate WinHTTP successive.</span><span class="sxs-lookup"><span data-stu-id="a8706-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="a8706-109">Se non segue queste linee guida, è probabile che si sia verificata un'impatto negativo sulle prestazioni o un potenziale blocco dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a8706-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="a8706-110">Se usata nel modo prescritto, questa opzione può migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a8706-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**CRITERIO DI \_ ACCESSO \_ AUTOMATICO DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-112">Imposta un valore long integer senza segno che specifica i criteri [di accesso automatico](authentication-in-winhttp.md) con uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a8706-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="a8706-113">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-113">Term</span></span> | <span data-ttu-id="a8706-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-114">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>LIVELLO DI SICUREZZA ACCESSO AUTOMATICO WINHTTP \_ \_ \_ \_ ELEVATO</span><span class="sxs-lookup"><span data-stu-id="a8706-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="a8706-116">Le credenziali predefinite non vengono usate.</span><span class="sxs-lookup"><span data-stu-id="a8706-116">Default credentials are not used.</span></span> <span data-ttu-id="a8706-117">Si noti che questo flag ha effetto solo se si specifica il server in base al nome effettivo del computer.</span><span class="sxs-lookup"><span data-stu-id="a8706-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="a8706-118">Non avrà effetto se si specifica il server in base a "localhost" o all'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a8706-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="a8706-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>LIVELLO DI SICUREZZA ACCESSO AUTOMATICO WINHTTP \_ \_ \_ \_ BASSO</span><span class="sxs-lookup"><span data-stu-id="a8706-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="a8706-120">Per tutte le richieste viene eseguito un accesso autenticato con le credenziali predefinite.</span><span class="sxs-lookup"><span data-stu-id="a8706-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="a8706-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>LIVELLO DI SICUREZZA ACCESSO AUTOMATICO WINHTTP \_ \_ \_ \_ MEDIO</span><span class="sxs-lookup"><span data-stu-id="a8706-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="a8706-122">Un accesso autenticato con le credenziali predefinite viene eseguito solo per le richieste nella Intranet locale.</span><span class="sxs-lookup"><span data-stu-id="a8706-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a8706-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**CALLBACK \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-124">Recupera il puntatore al set di funzioni di callback [**con WinHttpSetStatusCallback.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)</span><span class="sxs-lookup"><span data-stu-id="a8706-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**CONTESTO DEL CERTIFICATO \_ \_ CLIENT \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-126">Imposta il contesto del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a8706-126">Sets the client certificate context.</span></span> <span data-ttu-id="a8706-127">Se un'applicazione riceve [**l'errore \_ ERRORE WINHTTP CLIENT \_ \_ \_ AUTH CERT \_ NEEDED**](error-messages.md), deve chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per fornire un certificato prima di ritentare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="a8706-128">Come parte dell'elaborazione di questa opzione, WinHttp chiama [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) nel contesto del certificato fornito dal chiamante in modo che il contesto del certificato possa essere rilasciato in modo indipendente dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="a8706-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="a8706-129">L'applicazione non deve tentare di chiudere l'archivio certificati con il flag CERT CLOSE STORE FORCE FLAG nella chiamata a \_ \_ \_ \_ [**CertCloseStore nell'archivio**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) certificati da cui è stato recuperato il contesto del certificato.</span><span class="sxs-lookup"><span data-stu-id="a8706-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="a8706-130">Può verificarsi una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="a8706-130">An access violation may occur.</span></span>

<span data-ttu-id="a8706-131">Quando il server richiede un certificato client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce un [**errore \_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED.**](error-messages.md)</span><span class="sxs-lookup"><span data-stu-id="a8706-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="a8706-132">Se il server richiede il certificato ma non lo richiede, l'applicazione può specificare questa opzione per indicare che non dispone di un certificato.</span><span class="sxs-lookup"><span data-stu-id="a8706-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="a8706-133">Il server può scegliere un altro schema di autenticazione o consentire l'accesso anonimo al server.</span><span class="sxs-lookup"><span data-stu-id="a8706-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="a8706-134">L'applicazione fornisce la macro **WINHTTP \_ NO CLIENT \_ \_ CERT \_ CONTEXT** nel parametro *lpBuffer* di [**WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="a8706-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="a8706-135">Se il server richiede un certificato client, può inviare un codice di stato HTTP 403 in risposta.</span><span class="sxs-lookup"><span data-stu-id="a8706-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="a8706-136">Per altre informazioni, vedere **l'opzione WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ ISSUER \_ LIST.**</span><span class="sxs-lookup"><span data-stu-id="a8706-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**ELENCO AUTORITÀ \_ DI CERTIFICAZIONE DEL CERTIFICATO CLIENT \_ \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-138">Recupera una struttura [**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) quando l'errore da [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) è **ERROR \_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED**.</span><span class="sxs-lookup"><span data-stu-id="a8706-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="a8706-139">L'elenco di autorità di certificazione nella struttura contiene un elenco di autorità di certificazione (CA) accettabili dal server.</span><span class="sxs-lookup"><span data-stu-id="a8706-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="a8706-140">L'applicazione client può filtrare l'elenco di autorità di certificazione per recuperare il certificato client per l'autenticazione SSL.</span><span class="sxs-lookup"><span data-stu-id="a8706-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="a8706-141">In alternativa, se il server richiede il certificato client, ma non lo richiede, l'applicazione può chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l'opzione **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="a8706-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="a8706-142">Per altre informazioni, vedere **l'opzione \_ WINHTTP OPTION \_ CLIENT \_ CERT \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="a8706-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**TABELLA CODICI \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-144">Imposta la [*tabella codici*](glossary.md) usata per elaborare l'URL, ovvero la stringa di query.</span><span class="sxs-lookup"><span data-stu-id="a8706-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="a8706-145">Il valore predefinito è UTF8.</span><span class="sxs-lookup"><span data-stu-id="a8706-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**OPZIONE WINHTTP \_ \_ - CONFIGURARE \_ \_ L'AUTENTICAZIONE PASSPORT**</span><span class="sxs-lookup"><span data-stu-id="a8706-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-147">Imposta un valore long integer senza segno che specifica se l'autenticazione [Passport nell'autenticazione WinHTTP](passport-authentication-in-winhttp.md) è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a8706-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="a8706-148">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8706-148">The value can be one of the following:</span></span>

| <span data-ttu-id="a8706-149">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-149">Term</span></span> | <span data-ttu-id="a8706-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-150">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="a8706-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="a8706-152">Microsoft Passport'autenticazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a8706-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="a8706-153">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a8706-153">This is the default.</span></span> |
| <span data-ttu-id="a8706-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="a8706-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="a8706-155">Il keyring Passport è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a8706-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="a8706-156">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a8706-156">This is the default.</span></span> |
| <span data-ttu-id="a8706-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="a8706-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="a8706-158">L'autenticazione Passport è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a8706-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="a8706-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="a8706-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="a8706-160">Il keyring Passport è abilitato.</span><span class="sxs-lookup"><span data-stu-id="a8706-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="a8706-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**TENTATIVI \_ DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-162">Imposta o recupera un valore long integer senza segno che contiene il numero di tentativi di connessione a un host da parte diWinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a8706-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="a8706-163">I servizi HTTP di Microsoft Windows (WinHTTP) eseguono un solo tentativo una volta per ogni indirizzo IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="a8706-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="a8706-164">Ad esempio, se si tenta di connettersi a un host multihomed con 10 indirizzi IP e **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** è impostato su 7, WinHTTP prova a connettersi solo ai primi sette indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="a8706-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="a8706-165">Dato lo stesso set di 10 indirizzi IP, se **l'opzione WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** è impostata su 20, WinHTTP tenta ognuno dei 10 una sola volta.</span><span class="sxs-lookup"><span data-stu-id="a8706-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="a8706-166">Se un tentativo di connessione ha ancora esito negativo dopo il numero specificato di tentativi o se il timeout di connessione è scaduto prima di allora, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="a8706-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="a8706-167">Il valore predefinito per **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** è cinque tentativi.</span><span class="sxs-lookup"><span data-stu-id="a8706-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**TIMEOUT DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-169">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, espresso in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a8706-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="a8706-170">L'impostazione di questa opzione su infinito (0xFFFFFFFF) disabiliterà questo timer.</span><span class="sxs-lookup"><span data-stu-id="a8706-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="a8706-171">Se una richiesta di connessione TCP richiede più tempo di questo valore di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="a8706-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="a8706-172">Il timeout predefinito è 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="a8706-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="a8706-173">Quando si tenta di connettersi a più indirizzi IP per un singolo host (un host multihomed), il limite di timeout è per ogni singola connessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**INFORMAZIONI DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-175">Recupera l'indirizzo IP di origine e di destinazione e la porta della richiesta che ha generato la risposta quando [**viene restituito WinHttpReceiveResponse.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)</span><span class="sxs-lookup"><span data-stu-id="a8706-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="a8706-176">L'applicazione [**chiama WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con l'opzione **WINHTTP OPTION CONNECTION \_ \_ \_ INFO** e fornisce la struttura [**WINHTTP CONNECTION \_ \_ INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) nel *parametro lpBuffer.*</span><span class="sxs-lookup"><span data-stu-id="a8706-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="a8706-177">Per altre informazioni, vedere **INFORMAZIONI SULLA \_ CONNESSIONE \_ WINHTTP.**</span><span class="sxs-lookup"><span data-stu-id="a8706-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="a8706-178">**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a8706-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V0**</span><span class="sxs-lookup"><span data-stu-id="a8706-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-180">Ricostruisce lo struct [**TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) per la connessione sottostante usata dalla richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="a8706-181">Lo struct restituito può contenere statistiche provenienti da richieste precedenti inviate sulla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="a8706-182">Questa opzione è stata sostituita da **WINHTTP \_ OPTION CONNECTION \_ \_ STATS \_ V1.**</span><span class="sxs-lookup"><span data-stu-id="a8706-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V1**</span><span class="sxs-lookup"><span data-stu-id="a8706-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-184">Ricostruisce lo struct [**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) per la connessione sottostante usata dalla richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="a8706-185">Lo struct restituito può contenere statistiche provenienti da richieste precedenti inviate sulla stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**VALORE DI CONTESTO \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-187">Imposta o recupera un **\_ PTR DWORD** che contiene un puntatore al valore di contesto associato a questo handle [HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="a8706-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="a8706-188">Viene usato il valore archiviato nel buffer e al flag di **opzione WINHTTP \_ OPTION CONTEXT \_ \_ VALUE** viene assegnato un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="a8706-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_DECOMPRESSIONE \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-190">Imposta un valore DWORD di flag che determina se WinHTTP decomprime automaticamente i corpi di risposta con codifiche di contenuto compresse.</span><span class="sxs-lookup"><span data-stu-id="a8706-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="a8706-191">WinHTTP imposta anche un'intestazione Accept-Encoding, eseguendo l'override di qualsiasi elemento fornito dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="a8706-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="a8706-192">I valori supportati sono:</span><span class="sxs-lookup"><span data-stu-id="a8706-192">Supported values are:</span></span>

| <span data-ttu-id="a8706-193">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-193">Term</span></span> | <span data-ttu-id="a8706-194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-194">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>FLAG \_ DI DECOMPRESSIONE \_ \_ WINHTTP GZIP</span><span class="sxs-lookup"><span data-stu-id="a8706-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="a8706-196">Decomprimere Content-Encoding: risposte gzip.</span><span class="sxs-lookup"><span data-stu-id="a8706-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="a8706-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>FLAG DI \_ DECOMPRESSIONE WINHTTP \_ \_ DEFLATE</span><span class="sxs-lookup"><span data-stu-id="a8706-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="a8706-198">Decomprimere Content-Encoding: deflare le risposte.</span><span class="sxs-lookup"><span data-stu-id="a8706-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="a8706-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>FLAG \_ DI DECOMPRESSIONE WINHTTP \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="a8706-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="a8706-200">Decomprimere le risposte con qualsiasi codifica contenuto supportata.</span><span class="sxs-lookup"><span data-stu-id="a8706-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="a8706-201">Per impostazione predefinita, WinHTTP recapita risposte compresse al chiamante senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="a8706-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**OPZIONE WINHTTP \_ \_ DISABILITA \_ FUNZIONALITÀ**</span><span class="sxs-lookup"><span data-stu-id="a8706-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-203">Imposta un valore long integer senza segno che specifica quali funzionalità sono disabilitate con uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="a8706-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="a8706-204">Tenere presente che questa funzionalità deve essere passata a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) solo in handle di richiesta dopo che l'handle della richiesta è stato creato con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)e prima che la richiesta venga inviata [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="a8706-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="a8706-205">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-205">Term</span></span> | <span data-ttu-id="a8706-206">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-206">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>DISABILITARE \_ L'AUTENTICAZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="a8706-208">L'autenticazione automatica è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a8706-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="a8706-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>DISABILITARE \_ I COOKIE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="a8706-210">L'aggiunta automatica di intestazioni di cookie alle richieste è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a8706-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="a8706-211">Inoltre, i cookie restituiti non vengono aggiunti automaticamente al database dei cookie.</span><span class="sxs-lookup"><span data-stu-id="a8706-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="a8706-212">La disabilitazione dei cookie può comportare prestazioni scarse per l'autenticazione Passport.</span><span class="sxs-lookup"><span data-stu-id="a8706-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="a8706-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="a8706-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="a8706-214">Disabilita la semantica keep-alive per la connessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="a8706-215">La semantica keep-alive è necessaria per MSN, NTLM e altri tipi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a8706-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="a8706-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>DISABILITARE \_ I REINDIRIZZAMENTI WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="a8706-217">Il reindirizzamento automatico è disabilitato quando si inviano richieste [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="a8706-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="a8706-218">Se il reindirizzamento automatico è disabilitato, un'applicazione deve registrare una funzione di callback perché l'autenticazione Passport riesca.</span><span class="sxs-lookup"><span data-stu-id="a8706-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a8706-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**OPZIONE WINHTTP \_ \_ DISABILITA IL \_ \_ FALLBACK DEL \_ PROTOCOLLO SICURO**</span><span class="sxs-lookup"><span data-stu-id="a8706-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-220">Impedisce a WinHTTP di ritentare una connessione con una versione precedente del protocollo di sicurezza quando la negoziazione iniziale del protocollo non riesce.</span><span class="sxs-lookup"><span data-stu-id="a8706-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPZIONE WINHTTP \_ DISABILITA \_ CODA DI \_ \_ FLUSSO**</span><span class="sxs-lookup"><span data-stu-id="a8706-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-222">Consente alle nuove richieste di aprire una connessione HTTP/2 aggiuntiva quando viene raggiunto il limite massimo di flussi simultanei, anziché attendere il successivo flusso disponibile in una connessione esistente.</span><span class="sxs-lookup"><span data-stu-id="a8706-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**OPZIONE WINHTTP \_ \_ - ABILITARE LA \_ FUNZIONALITÀ**</span><span class="sxs-lookup"><span data-stu-id="a8706-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-224">Imposta un valore di long integer senza segno che specifica le funzionalità attualmente abilitate.</span><span class="sxs-lookup"><span data-stu-id="a8706-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="a8706-225">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a8706-225">Can be one of the following values.</span></span>

| <span data-ttu-id="a8706-226">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-226">Term</span></span> | <span data-ttu-id="a8706-227">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-227">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="a8706-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="a8706-229">Se abilitata, WinHTTP ripristina temporaneamente la rappresentazione del client per la durata delle operazioni di autenticazione del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="a8706-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="a8706-230">Questo valore può essere impostato solo sull'handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="a8706-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>ABILITARE \_ LA \_ REVOCA SSL WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="a8706-232">Se abilitata, WinHTTP consente la revoca SSL.</span><span class="sxs-lookup"><span data-stu-id="a8706-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="a8706-233">Questo valore può essere impostato solo sull'handle della richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**OPZIONE WINHTTP \_ \_ ABILITA PROTOCOLLO \_ \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-235">Imposta una maschera di bit DWORD di versioni HTTP avanzate accettabili.</span><span class="sxs-lookup"><span data-stu-id="a8706-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="a8706-236">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="a8706-236">Possible values are:</span></span>

| <span data-ttu-id="a8706-237">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-237">Term</span></span> | <span data-ttu-id="a8706-238">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-238">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>FLAG \_ DEL PROTOCOLLO \_ \_ WINHTTP HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a8706-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="a8706-240">Abilita HTTP/2 per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="a8706-241">Nessuno (0x0)</span><span class="sxs-lookup"><span data-stu-id="a8706-241">None (0x0)</span></span> | <span data-ttu-id="a8706-242">Limita la richiesta a HTTP/1.1 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="a8706-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="a8706-243">Le versioni legacy di HTTP (1.1 e precedenti) non possono essere disabilitate usando questa opzione.</span><span class="sxs-lookup"><span data-stu-id="a8706-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="a8706-244">Il valore predefinito è 0x0.</span><span class="sxs-lookup"><span data-stu-id="a8706-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-245"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**OPZIONE WINHTTP \_ \_ ABILITA \_ HTTP2 PLUS CLIENT \_ \_ \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="a8706-245"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a8706-246">Questa opzione può essere impostata su un handle di sessione WinHttp per consentire a WinHttp di usare il contesto del certificato client fornito dal chiamante quando viene usato HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="a8706-246">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-247"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**OPZIONE WINHTTP \_ \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="a8706-247"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-248">Imposta un **valore BOOL** che specifica se la traccia è attualmente abilitata.</span><span class="sxs-lookup"><span data-stu-id="a8706-248">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="a8706-249">Per altre informazioni sulla funzionalità di traccia in WinHTTP, vedere [Funzionalità di traccia WinHTTP.](winhttptracecfg-exe--a-trace-configuration-tool.md)</span><span class="sxs-lookup"><span data-stu-id="a8706-249">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="a8706-250">Questa opzione può essere impostata solo su un handle **HINTERNET** **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8706-250">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="a8706-251"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**OPZIONE WINHTTP \_ \_ ENCODE \_ EXTRA**</span><span class="sxs-lookup"><span data-stu-id="a8706-251"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-252">Abilita la codifica della percentuale url per il percorso e la stringa di query.</span><span class="sxs-lookup"><span data-stu-id="a8706-252">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="a8706-253">In alternativa, è possibile eseguire la codifica percentuale prima di chiamare WinHttp.</span><span class="sxs-lookup"><span data-stu-id="a8706-253">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="a8706-254"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**OPZIONE WINHTTP \_ \_ SCADENZA \_ CONNESSIONE**</span><span class="sxs-lookup"><span data-stu-id="a8706-254"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-255">Questa opzione può essere impostata solo su un handle di richiesta ancora attivo (invio o ricezione).</span><span class="sxs-lookup"><span data-stu-id="a8706-255">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="a8706-256">L'impostazione di questa opzione consente a WinHttp di interrompere la gestione delle richieste sulla connessione associata all'handle di richiesta passato.</span><span class="sxs-lookup"><span data-stu-id="a8706-256">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="a8706-257">La connessione verrà chiusa dopo il completamento dell'handle della richiesta con cui viene chiamata questa opzione.</span><span class="sxs-lookup"><span data-stu-id="a8706-257">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="a8706-258">Questa opzione non accetta parametri.</span><span class="sxs-lookup"><span data-stu-id="a8706-258">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-259"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERRORE ESTESO \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-259"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-260">Recupera un valore long integer senza segno che contiene un codice di errore di Microsoft Windows Sockets mappato ai messaggi di errore ERROR WINHTTP restituiti per l'ultima volta \_ in questo contesto del \_ \* thread.</span><span class="sxs-lookup"><span data-stu-id="a8706-260">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="a8706-261">È possibile passare **NULL** come valore dell'handle.</span><span class="sxs-lookup"><span data-stu-id="a8706-261">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-262"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**CREDS \_ \_ PROXY GLOBALI \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-262"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-263">Accetta un puntatore a [**una struttura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *hInternet* impostato su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8706-263">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="a8706-264">Questa opzione richiede la chiave del Registro **di sistema HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Impostazioni \\ Internet. ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="a8706-264">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a8706-265">Se questa chiave del Registro di sistema non è impostata, WinHTTP restituirà **l'errore \_ ERROR WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="a8706-265">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="a8706-266">Questa chiave del Registro di sistema non è presente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a8706-266">This registry key is not present by default.</span></span> <span data-ttu-id="a8706-267">Quando è impostata, WinINet invierà le credenziali a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a8706-267">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a8706-268">Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono impostate credenziali nell'handle corrente, userà le credenziali fornite da WinINet.</span><span class="sxs-lookup"><span data-stu-id="a8706-268">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="a8706-269">Per condividere le credenziali del server oltre alle credenziali proxy, gli utenti devono impostare **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="a8706-269">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-270"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**CREDS \_ \_ GLOBALI DEL SERVER \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-270"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-271">Accetta un puntatore a [**una struttura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *hInternet* impostato su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8706-271">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="a8706-272">Questa opzione richiede la chiave del Registro **di sistema HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Impostazioni \\ Internet. ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="a8706-272">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a8706-273">Se questa chiave del Registro di sistema non è impostata, WinHTTP restituirà **l'errore \_ ERROR WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="a8706-273">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="a8706-274">Questa chiave del Registro di sistema non è presente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a8706-274">This registry key is not present by default.</span></span> <span data-ttu-id="a8706-275">Quando è impostata, WinINet invierà le credenziali a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a8706-275">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a8706-276">Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono impostate credenziali nell'handle corrente, userà le credenziali fornite da WinINet.</span><span class="sxs-lookup"><span data-stu-id="a8706-276">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="a8706-277">Per condividere le credenziali del server oltre alle credenziali proxy, gli utenti devono impostare **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="a8706-277">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-278"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TIPO DI \_ HANDLE DI \_ OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-278"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-279">Recupera un valore di long integer senza segno che contiene il tipo dell'handle [HINTERNET](hinternet-handles-in-winhttp.md) passato.</span><span class="sxs-lookup"><span data-stu-id="a8706-279">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="a8706-280">Il valore restituito può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8706-280">The return value can be one of the following:</span></span>

| <span data-ttu-id="a8706-281">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-281">Term</span></span> | <span data-ttu-id="a8706-282">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-282">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-283"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>CONNESSIONE DEL TIPO DI HANDLE WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8706-283"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="a8706-284">L'handle è un handle di connessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-284">The handle is a connection handle.</span></span> |
| <span data-ttu-id="a8706-285"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>RICHIESTA DI TIPO HANDLE WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8706-285"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="a8706-286">L'handle è un handle di richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-286">The handle is a request handle.</span></span> |
| <span data-ttu-id="a8706-287"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SESSIONE CON TIPO DI HANDLE WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8706-287"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="a8706-288">L'handle è un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-288">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a8706-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**OPZIONE \_ \_ HTTP \_ PROTOCOL REQUIRED DI WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-290">Impedisce l'uso di versioni del protocollo diverse da quelle abilitate da **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-290">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-291"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**PROTOCOLLO \_ \_ HTTP DELL'OPZIONE WINHTTP \_ \_ USATO**</span><span class="sxs-lookup"><span data-stu-id="a8706-291"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-292">Ottiene un valore DWORD che indica quale versione HTTP avanzata è stata utilizzata in una determinata richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-292">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="a8706-293">Per un elenco dei valori possibili, vedere **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.</span><span class="sxs-lookup"><span data-stu-id="a8706-293">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-294"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**VERSIONE \_ \_ HTTP DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-294"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-295">Imposta o recupera una [**struttura HTTP \_ VERSION \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) che contiene la versione HTTP supportata.</span><span class="sxs-lookup"><span data-stu-id="a8706-295">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="a8706-296">Si tratta di un'opzione a livello di processo. usare **NULL per** l'handle.</span><span class="sxs-lookup"><span data-stu-id="a8706-296">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-297"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**OPZIONE \_ \_ WINHTTP \_ KEEPALIVE HTTP2**</span><span class="sxs-lookup"><span data-stu-id="a8706-297"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a8706-298">Questa opzione può essere impostata su un handle di sessione per fare in modo che WinHttp usi i frame PING HTTP/2 come meccanismo keep-live.</span><span class="sxs-lookup"><span data-stu-id="a8706-298">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="a8706-299">I chiamanti specificano un timeout in millisecondi e, dopo che non è presente alcuna attività su una connessione per tale periodo di timeout, WinHttp inizierà a inviare frame PING HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="a8706-299">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="a8706-300">I chiamanti non possono impostare un valore di timeout inferiore a 5000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a8706-300">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-301"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**OPZIONE WINHTTP \_ \_ HTTP2 \_ PLUS TRANSFER \_ \_ ENCODING**</span><span class="sxs-lookup"><span data-stu-id="a8706-301"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a8706-302">Questa opzione può essere impostata su un handle di richiesta WinHttp per controllare il comportamento di WinHttp quando una risposta HTTP/2 contiene un'intestazione "Transfer-Encoding".</span><span class="sxs-lookup"><span data-stu-id="a8706-302">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="a8706-303">In tal caso, WinHttp restituirà un errore se questa opzione è impostata su **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a8706-303">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="a8706-304"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**OPZIONE WINHTTP \_ \_ IGNORA REVOCA CERTIFICATO \_ \_ \_ OFFLINE**</span><span class="sxs-lookup"><span data-stu-id="a8706-304"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-305">Consente alle connessioni protette di usare certificati di sicurezza per i quali non è stato possibile scaricare l'elenco di revoche di certificati.</span><span class="sxs-lookup"><span data-stu-id="a8706-305">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-306"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**OPZIONE \_ \_ WINHTTP \_ FALLBACK RAPIDO IPV6 \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-306"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-307">Abilita il fallback rapido IPv6 (bulbi oculare più accattivanti) per la connessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-307">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="a8706-308">Questo comportamento è simile al comportamento di Happy Eyeballs descritto in [RFC 6555](https://tools.ietf.org/html/rfc6555) per migliorare i tempi di connessione nelle reti in cui IPv6 non è affidabile.</span><span class="sxs-lookup"><span data-stu-id="a8706-308">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="a8706-309">Se entrambi gli indirizzi IPv6 e IPv4 vengono risolti per un determinato host, WinHttp inizierà connettendosi al primo indirizzo IPv6 risolto con un timeout breve (300 ms).</span><span class="sxs-lookup"><span data-stu-id="a8706-309">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="a8706-310">In caso di errore di connessione, WinHttp tenterà di connettersi al primo indirizzo IPv4 risolto con il timeout standard.</span><span class="sxs-lookup"><span data-stu-id="a8706-310">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="a8706-311">In caso di errore della seconda connessione, WinHttp ripeterà il primo indirizzo IPv6 risolto con il timeout standard.</span><span class="sxs-lookup"><span data-stu-id="a8706-311">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="a8706-312">In caso di errore della terza connessione, WinHttp ripristina il comportamento predefinito per tutti gli indirizzi rimanenti, provando una connessione a ognuno con il timeout standard fino a quando non viene stabilita una connessione o non rimane alcun indirizzo.</span><span class="sxs-lookup"><span data-stu-id="a8706-312">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-313"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**L'OPZIONE WINHTTP \_ \_ È PROXY CONNECT \_ \_ \_ RESPONSE**</span><span class="sxs-lookup"><span data-stu-id="a8706-313"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-314">Ottiene un valore che indica se è possibile recuperare o meno una risposta di connessione restituita dal proxy.</span><span class="sxs-lookup"><span data-stu-id="a8706-314">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-315"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ 1 \_ 0 \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="a8706-315"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-316">Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="a8706-316">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="a8706-317">Il valore predefinito è **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="a8706-317">The default value is **INFINITE**.</span></span>

<span data-ttu-id="a8706-318">**Windows Vista con SP1 e Windows Server 2008:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a8706-318">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-319"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="a8706-319"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-320">Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server.</span><span class="sxs-lookup"><span data-stu-id="a8706-320">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="a8706-321">Il valore predefinito è **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="a8706-321">The default value is **INFINITE**.</span></span>

<span data-ttu-id="a8706-322">Quando questa opzione è impostata su zero, WinHTTP imposta il limite per il numero di connessioni su 2.</span><span class="sxs-lookup"><span data-stu-id="a8706-322">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-323"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**OPZIONE WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS**</span><span class="sxs-lookup"><span data-stu-id="a8706-323"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-324">Imposta il numero massimo di reindirizzamenti seguito da WinHTTP. il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="a8706-324">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="a8706-325">Questo limite impedisce a siti non autorizzati di sospendere il client WinHTTP in seguito a un numero elevato di reindirizzamenti.</span><span class="sxs-lookup"><span data-stu-id="a8706-325">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="a8706-326">**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a8706-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-327"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**OPZIONE WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE**</span><span class="sxs-lookup"><span data-stu-id="a8706-327"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-328">Numero massimo di risposte del codice di stato Informational 100-199 ignorate prima di restituire il codice di stato finale al client WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a8706-328">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="a8706-329">I codici di stato in formato informativo 100-199 possono essere inviati dal server prima del codice di stato finale e sono descritti nella specifica per HTTP/1.1 (per altre informazioni, vedere [RFC 2616).](https://www.ietf.org/rfc/rfc2616.txt)</span><span class="sxs-lookup"><span data-stu-id="a8706-329">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="a8706-330">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="a8706-330">The default is 10.</span></span>

<span data-ttu-id="a8706-331">**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a8706-331">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-332"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**OPZIONE WINHTTP \_ \_ DIMENSIONE MASSIMA \_ \_ SVUOTAMENTO \_ RISPOSTA**</span><span class="sxs-lookup"><span data-stu-id="a8706-332"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-333">Limite alla quantità di dati svuotati dalle risposte per riutilizzare una connessione, specificata in byte.</span><span class="sxs-lookup"><span data-stu-id="a8706-333">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="a8706-334">Il valore predefinito è 1 MB.</span><span class="sxs-lookup"><span data-stu-id="a8706-334">The default is 1MB.</span></span>

<span data-ttu-id="a8706-335">**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a8706-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-336"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**DIMENSIONI MASSIME \_ INTESTAZIONE RISPOSTA \_ \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-336"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-337">Set associato alla dimensione massima della parte di intestazione della risposta del server, specificata in byte.</span><span class="sxs-lookup"><span data-stu-id="a8706-337">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="a8706-338">Questo limite protegge il client da un server non autorizzato che tenta di bloccare il client inviando una risposta con una quantità infinita di dati di intestazione.</span><span class="sxs-lookup"><span data-stu-id="a8706-338">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="a8706-339">Il valore predefinito è 64 KB.</span><span class="sxs-lookup"><span data-stu-id="a8706-339">The default value is 64KB.</span></span>

<span data-ttu-id="a8706-340">**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a8706-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-341"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**HANDLE PADRE \_ DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-341"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-342">Recupera l'handle padre per questo handle.</span><span class="sxs-lookup"><span data-stu-id="a8706-342">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-343"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**TESTO \_ \_ \_ COBRANDING DELL'OPZIONE WINHTTP PASSPORT \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-343"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-344">Recupera una stringa contenente il [*testo di cobranding*](glossary.md) fornito dal server di accesso Passport.</span><span class="sxs-lookup"><span data-stu-id="a8706-344">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="a8706-345">Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401.</span><span class="sxs-lookup"><span data-stu-id="a8706-345">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="a8706-346">Un'applicazione deve passare dimensioni del buffer, in byte, sufficientemente grandi da contenere la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="a8706-346">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-347"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**URL \_ \_ \_ COBRANDING DELL'OPZIONE WINHTTP PASSPORT \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-347"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-348">Recupera una stringa contenente un URL per un [*elemento grafico di cobranding*](glossary.md) fornito dal server di accesso Passport.</span><span class="sxs-lookup"><span data-stu-id="a8706-348">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="a8706-349">Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401.</span><span class="sxs-lookup"><span data-stu-id="a8706-349">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="a8706-350">Un'applicazione deve passare dimensioni del buffer, in byte, sufficientemente grandi da contenere la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="a8706-350">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-351"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**URL \_ RESTITUITO \_ PASSPORT DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-351"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-352">Imposta un'opzione di sola lettura su un handle di richiesta che recupera l'URL restituito di Passport.</span><span class="sxs-lookup"><span data-stu-id="a8706-352">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-353"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**OPZIONE WINHTTP \_ \_ \_ DISCONNESSIONE PASSPORT \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-353"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-354">Imposta l'opzione su un handle di sessione per disconnettersi da qualsiasi account di accesso Passport.</span><span class="sxs-lookup"><span data-stu-id="a8706-354">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="a8706-355">Un'applicazione deve passare l'URL restituito passport recuperato con **WINHTTP \_ OPTION PASSPORT RETURN \_ \_ \_ URL**.</span><span class="sxs-lookup"><span data-stu-id="a8706-355">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="a8706-356">Tutti i cookie correlati all'URL restituito vengono cancellati.</span><span class="sxs-lookup"><span data-stu-id="a8706-356">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-357"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**PASSWORD \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-357"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-358">Imposta o recupera un valore stringa contenente la password associata a un handle di richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-358">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-359"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**PROXY \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-359"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-360">Imposta o recupera una struttura [**WINHTTP \_ PROXY \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) che contiene i dati del proxy in un handle di sessione o in un handle di richiesta esistente.</span><span class="sxs-lookup"><span data-stu-id="a8706-360">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="a8706-361">Quando si recuperano dati proxy, un'applicazione deve liberare le stringhe **lpszProxy** e **lpszProxyBypass** contenute in questa struttura (se non **SONO NULL)** usando la funzione [**GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree)</span><span class="sxs-lookup"><span data-stu-id="a8706-361">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="a8706-362">Un'applicazione può eseguire una query per i dati proxy globali (proxy predefinito) passando un handle **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8706-362">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-363"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**PASSWORD PROXY \_ DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-363"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-364">Imposta o recupera un valore stringa contenente la password utilizzata per accedere al proxy.</span><span class="sxs-lookup"><span data-stu-id="a8706-364">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-365"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**NOME \_ \_ SPN PROXY \_ DELL'OPZIONE WINHTTP \_ USATO**</span><span class="sxs-lookup"><span data-stu-id="a8706-365"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-366">Ottiene il nome dell'entità server proxy fornito da WinHTTP a SSPI durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a8706-366">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="a8706-367">Questo valore stringa viene utilizzato per passare a [**SspiPromptForCredentials dopo**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) un errore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a8706-367">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-368"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**NOME UTENTE \_ \_ PROXY DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-368"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-369">Imposta o recupera un valore stringa contenente il nome utente utilizzato per accedere al proxy.</span><span class="sxs-lookup"><span data-stu-id="a8706-369">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-370"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**DIMENSIONI DEL \_ \_ BUFFER DI LETTURA \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-370"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-371">Questa opzione è stata deprecata. non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="a8706-371">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-372"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**L'OPZIONE WINHTTP \_ RICEVE LA RISPOSTA DI CONNESSIONE \_ \_ \_ \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="a8706-372"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-373">Imposta se è possibile recuperare o meno l'entità di risposta del proxy.</span><span class="sxs-lookup"><span data-stu-id="a8706-373">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="a8706-374">Questa opzione è disabilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a8706-374">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-375"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**L'OPZIONE WINHTTP \_ RICEVE IL TIMEOUT DI \_ \_ \_ RISPOSTA**</span><span class="sxs-lookup"><span data-stu-id="a8706-375"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-376">Imposta o recupera un valore di long integer senza segno che contiene il valore di timeout, in millisecondi, per attendere la ricezione di tutte le intestazioni di risposta a una richiesta.</span><span class="sxs-lookup"><span data-stu-id="a8706-376">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="a8706-377">Se WinHTTP non riceve tutte le intestazioni entro questo periodo di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="a8706-377">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="a8706-378">Il valore di timeout predefinito è 90 secondi.</span><span class="sxs-lookup"><span data-stu-id="a8706-378">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="a8706-379">Questo timeout viene controllato solo quando i dati vengono ricevuti dal socket.</span><span class="sxs-lookup"><span data-stu-id="a8706-379">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="a8706-380">Di conseguenza, alla scadenza del timeout, l'applicazione client non viene notificata fino all'arrivo di altri dati dal server.</span><span class="sxs-lookup"><span data-stu-id="a8706-380">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="a8706-381">Se non arrivano dati dal server, il ritardo tra la scadenza del timeout e la notifica dell'applicazione client potrebbe essere pari al valore di timeout impostato usando il *parametro dwReceiveTimeout* della [**funzione WinHttpSetTimeouts.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)</span><span class="sxs-lookup"><span data-stu-id="a8706-381">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-382"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**TIMEOUT DI \_ RICEZIONE \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-382"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-383">Imposta o recupera un valore di long integer senza segno che contiene il valore di timeout, in millisecondi, per ricevere una risposta parziale a una richiesta o leggere alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="a8706-383">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="a8706-384">Se la risposta richiede più tempo di questo valore di timeout, la richiesta viene annullata.</span><span class="sxs-lookup"><span data-stu-id="a8706-384">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="a8706-385">Il valore di timeout predefinito è di 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="a8706-385">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-386"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-386"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-387">Imposta il comportamento di WinHTTP relativo alla gestione di un codice di stato di reindirizzamento HTTP 30x.</span><span class="sxs-lookup"><span data-stu-id="a8706-387">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="a8706-388">Questa opzione può essere impostata in un handle di sessione o richiesta su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8706-388">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="a8706-389">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-389">Term</span></span> | <span data-ttu-id="a8706-390">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-390">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-391"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_ \_ SEMPRE</span><span class="sxs-lookup"><span data-stu-id="a8706-391"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="a8706-392">Tutti i reindirizzamenti vengono seguiti automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a8706-392">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="a8706-393"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_L'OPZIONE WINHTTP \_ \_ \_ REINDIRIZZA I CRITERI NON \_ CONSENTONO HTTPS A \_ \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-393"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="a8706-394">Vengono seguiti tutti i reindirizzamenti, ad eccezione di quelli originati da un URL sicuro (https) a un URL non sicuro (http).</span><span class="sxs-lookup"><span data-stu-id="a8706-394">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="a8706-395">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a8706-395">This is the default setting.</span></span> |
| <span data-ttu-id="a8706-396"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_ \_ MAI</span><span class="sxs-lookup"><span data-stu-id="a8706-396"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="a8706-397">I reindirizzamenti non vengono mai seguiti.</span><span class="sxs-lookup"><span data-stu-id="a8706-397">Redirects are never followed.</span></span> <span data-ttu-id="a8706-398">Lo stato 30x viene restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a8706-398">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-399"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**OPZIONE WINHTTP \_ \_ REJECT \_ USERPWD \_ \_ NELL'URL**</span><span class="sxs-lookup"><span data-stu-id="a8706-399"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-400">Rifiuta gli URL che contengono un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="a8706-400">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="a8706-401">Questa opzione rifiuta anche gli URL che contengono la semantica *nome utente:password,* anche se non è specificato alcun nome utente o password.</span><span class="sxs-lookup"><span data-stu-id="a8706-401">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="a8706-402">Ad esempio, " u:p@hostname ", " :@hostname ", " " e " " verrebbero tutti u:@hostname :p@hostname contrassegnati come non validi.</span><span class="sxs-lookup"><span data-stu-id="a8706-402">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="a8706-403">Se alla funzione viene passato un URL non valido, restituisce [ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a8706-403">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="a8706-404">Per impostazione predefinita, questa opzione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a8706-404">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-405"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**PRIORITÀ DI RICHIESTA \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-405"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-406">Questa opzione è stata deprecata. non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="a8706-406">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-407"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**STATISTICHE DI \_ RICHIESTA \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-407"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-408">Retreives statistics for the request.retreives statistics for the request.</span><span class="sxs-lookup"><span data-stu-id="a8706-408">Retreives statistics for the request.</span></span>  <span data-ttu-id="a8706-409">Per un elenco delle statistiche disponibili, vedere [**WINHTTP \_ REQUEST \_ STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="a8706-409">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-410"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**TEMPI DI RICHIESTA \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-410"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-411">Retreives timing information for the request.retreives timing information for the request.</span><span class="sxs-lookup"><span data-stu-id="a8706-411">Retreives timing information for the request.</span></span> <span data-ttu-id="a8706-412">Per un elenco degli intervalli disponibili, vedere [**TEMPI DI RICHIESTA \_ \_ WINHTTP.**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)</span><span class="sxs-lookup"><span data-stu-id="a8706-412">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-413"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**OPZIONE WINHTTP \_ \_ REQUIRE STREAM \_ \_ END**</span><span class="sxs-lookup"><span data-stu-id="a8706-413"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a8706-414">Questa opzione indica a WinHttp di ignorare le intestazioni di risposta "Content-Length" e di continuare a ricevere in un flusso fino a quando non viene ricevuto END_STREAM flag di contenuto.</span><span class="sxs-lookup"><span data-stu-id="a8706-414">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-415"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**NOME HOST \_ DI \_ RISOLUZIONE \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-415"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a8706-416">Questa opzione può essere impostata su un handle di richiesta WinHttp prima dell'invio.</span><span class="sxs-lookup"><span data-stu-id="a8706-416">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="a8706-417">Se impostata, WinHttp userà la stringa fornita dal chiamante come nome host per la risoluzione DNS.</span><span class="sxs-lookup"><span data-stu-id="a8706-417">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-418"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**TIMEOUT RISOLUZIONE \_ DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-418"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-419">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per risolvere un nome host.</span><span class="sxs-lookup"><span data-stu-id="a8706-419">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="a8706-420">Il valore di timeout predefinito è **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="a8706-420">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="a8706-421">Se viene specificato un valore non predefinito, si verifica un sovraccarico della creazione di un thread per ogni risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a8706-421">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-422"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**PROTOCOLLI SICURI \_ \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-422"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-423">Imposta un valore di long integer senza segno che specifica quali protocolli sicuri sono accettabili.</span><span class="sxs-lookup"><span data-stu-id="a8706-423">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="a8706-424">Per impostazione predefinita, solo SSL3 e TLS1 sono abilitati in Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a8706-424">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="a8706-425">Per impostazione predefinita, solo SSL3, TLS1.0, TLS1.1 e TLS1.2 sono abilitati in Windows 8.1 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a8706-425">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="a8706-426">Il valore può essere una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a8706-426">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="a8706-427">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-427">Term</span></span> | <span data-ttu-id="a8706-428">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-428">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-429"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ ALL</span><span class="sxs-lookup"><span data-stu-id="a8706-429"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="a8706-430">È possibile usare i protocolli Secure Sockets Layer (SSL) 2.0, SSL 3.0 e Transport Layer Security (TLS) 1.0.</span><span class="sxs-lookup"><span data-stu-id="a8706-430">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="a8706-431"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="a8706-431"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="a8706-432">È possibile usare il protocollo SSL 2.0.</span><span class="sxs-lookup"><span data-stu-id="a8706-432">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="a8706-433"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="a8706-433"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="a8706-434">È possibile usare il protocollo SSL 3.0.</span><span class="sxs-lookup"><span data-stu-id="a8706-434">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="a8706-435"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="a8706-435"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="a8706-436">È possibile usare il protocollo TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="a8706-436">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="a8706-437"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>FLAG \_ WINHTTP \_ SECURE \_ PROTOCOL \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a8706-437"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="a8706-438">È possibile usare il protocollo TLS 1.1.</span><span class="sxs-lookup"><span data-stu-id="a8706-438">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="a8706-439"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>FLAG \_ WINHTTP \_ SECURE \_ PROTOCOL \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="a8706-439"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="a8706-440">È possibile usare il protocollo TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="a8706-440">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a8706-441"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**STRUCT \_ DEL CERTIFICATO DI SICUREZZA \_ \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-441"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-442">Recupera il certificato per un server SSL/TLS nella struttura [**WINHTTP \_ CERTIFICATE \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)</span><span class="sxs-lookup"><span data-stu-id="a8706-442">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="a8706-443">L'applicazione deve liberare **i membri lpszSubjectInfo** e **lpszIssuerInfo** con [**LocalFree.**](/windows/desktop/api/winbase/nf-winbase-localfree)</span><span class="sxs-lookup"><span data-stu-id="a8706-443">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-444"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**FLAG DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-444"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-445">Imposta o recupera un valore long integer senza segno che contiene i flag di sicurezza per un handle.</span><span class="sxs-lookup"><span data-stu-id="a8706-445">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="a8706-446">Può essere una combinazione di questi valori:</span><span class="sxs-lookup"><span data-stu-id="a8706-446">It can be a combination of these values:</span></span>

| <span data-ttu-id="a8706-447">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-447">Term</span></span> | <span data-ttu-id="a8706-448">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-448">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-449"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>FLAG DI \_ SICUREZZA \_ IGNORA \_ CERT CN NON \_ \_ VALIDO</span><span class="sxs-lookup"><span data-stu-id="a8706-449"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="a8706-450">Consente un nome comune non valido in un certificato. ciò significa che il nome del server specificato dall'applicazione non corrisponde al nome comune nel certificato.</span><span class="sxs-lookup"><span data-stu-id="a8706-450">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="a8706-451">Se questo flag è impostato, l'applicazione non riceve un **callback WINHTTP \_ CALLBACK STATUS \_ FLAG \_ \_ CERT CN \_ \_ INVALID.**</span><span class="sxs-lookup"><span data-stu-id="a8706-451">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="a8706-452"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>FLAG DI \_ SICUREZZA IGNORA DATA CERTIFICATO NON \_ \_ \_ \_ VALIDA</span><span class="sxs-lookup"><span data-stu-id="a8706-452"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="a8706-453">Consente una data di certificato non valida, ad esempio un certificato scaduto o non ancora valido.</span><span class="sxs-lookup"><span data-stu-id="a8706-453">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="a8706-454">Se questo flag è impostato, l'applicazione non riceve un **callback WINHTTP \_ CALLBACK STATUS \_ FLAG \_ \_ CERT DATE \_ \_ INVALID.**</span><span class="sxs-lookup"><span data-stu-id="a8706-454">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="a8706-455"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>FLAG DI \_ SICUREZZA \_ IGNORA CA \_ \_ SCONOSCIUTA</span><span class="sxs-lookup"><span data-stu-id="a8706-455"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="a8706-456">Consente un'autorità di certificazione non valida.</span><span class="sxs-lookup"><span data-stu-id="a8706-456">Allows an invalid certificate authority.</span></span> <span data-ttu-id="a8706-457">Se questo flag è impostato, l'applicazione non riceve un callback DI STATO **CALLBACK WINHTTP \_ NON \_ \_ \_ \_ VALIDO.**</span><span class="sxs-lookup"><span data-stu-id="a8706-457">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="a8706-458"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>FLAG DI \_ SICUREZZA \_ IGNORA UTILIZZO \_ ERRATO DEL \_ \_ CERTIFICATO</span><span class="sxs-lookup"><span data-stu-id="a8706-458"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="a8706-459">Consente di stabilire l'identità di un server con un certificato non server, ad esempio un certificato client.</span><span class="sxs-lookup"><span data-stu-id="a8706-459">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="a8706-460"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>FLAG DI \_ SICUREZZA \_ IGNORA FIRMA \_ \_ DEBOLE</span><span class="sxs-lookup"><span data-stu-id="a8706-460"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="a8706-461">Consente di ignorare una firma debole.</span><span class="sxs-lookup"><span data-stu-id="a8706-461">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="a8706-462">Questo flag è disponibile nell'aggiornamento cumulativo per ogni sistema operativo a partire da Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a8706-462">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="a8706-463"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>FLAG \_ DI \_ SICUREZZA SICURO</span><span class="sxs-lookup"><span data-stu-id="a8706-463"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="a8706-464">Usa trasferimenti sicuri.</span><span class="sxs-lookup"><span data-stu-id="a8706-464">Uses secure transfers.</span></span> <span data-ttu-id="a8706-465">Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="a8706-465">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a8706-466"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>LIVELLO DI \_ ATTENDIBILITÀ DEL FLAG \_ DI SICUREZZA \_ MEDIO</span><span class="sxs-lookup"><span data-stu-id="a8706-466"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="a8706-467">Usa la crittografia media (56 bit).</span><span class="sxs-lookup"><span data-stu-id="a8706-467">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="a8706-468">Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="a8706-468">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a8706-469"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>LIVELLO DI \_ COMPLESSITÀ DEL FLAG DI \_ \_ SICUREZZA</span><span class="sxs-lookup"><span data-stu-id="a8706-469"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="a8706-470">Usa la crittografia avanzata (128 bit).</span><span class="sxs-lookup"><span data-stu-id="a8706-470">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="a8706-471">Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="a8706-471">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="a8706-472"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>LIVELLO DI \_ COMPLESSITÀ DEL FLAG DI SICUREZZA \_ \_ DEBOLE</span><span class="sxs-lookup"><span data-stu-id="a8706-472"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="a8706-473">Usa la crittografia debole (40 bit).</span><span class="sxs-lookup"><span data-stu-id="a8706-473">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="a8706-474">Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)</span><span class="sxs-lookup"><span data-stu-id="a8706-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a8706-475"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**INFORMAZIONI DI SICUREZZA \_ DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-475"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-476">Retreives the SChannel connection and cipher information for a request.</span><span class="sxs-lookup"><span data-stu-id="a8706-476">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-477"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**BITNESS \_ CHIAVE DI SICUREZZA \_ \_ \_ DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-477"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-478">Recupera un valore di long integer senza segno che contiene il livello di codifica della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="a8706-478">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="a8706-479">Un numero maggiore indica una crittografia più avanzata per la complessità della crittografia.</span><span class="sxs-lookup"><span data-stu-id="a8706-479">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-480"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**TIMEOUT INVIO OPZIONE WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-480"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-481">Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per inviare una richiesta o scrivere alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="a8706-481">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="a8706-482">Se l'invio della richiesta richiede più tempo del timeout, l'operazione di invio viene annullata.</span><span class="sxs-lookup"><span data-stu-id="a8706-482">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="a8706-483">Il timeout predefinito è 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="a8706-483">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-484"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**OPZIONE WINHTTP \_ \_ SERVER \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="a8706-484"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-485">Ottiene un puntatore [**alla struttura SecPkgContext \_ Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) che specifica un token di associazione di canale (CBT).</span><span class="sxs-lookup"><span data-stu-id="a8706-485">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="a8706-486">Un token di associazione di canale è una proprietà di un canale di trasporto protetto e viene utilizzato per associare un canale di autenticazione al canale di trasporto protetto.</span><span class="sxs-lookup"><span data-stu-id="a8706-486">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="a8706-487">Questo token può essere ottenuto da questa opzione solo dopo che è stata stabilita una connessione SSL.</span><span class="sxs-lookup"><span data-stu-id="a8706-487">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="a8706-488">Il passaggio di questa opzione e di un valore **Null** per *lpBuffer* a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) restituirà ERROR INSUFFICIENT BUFFER e le dimensioni in byte necessarie per il \_ buffer nel parametro \_ *lpdwBufferLength.*</span><span class="sxs-lookup"><span data-stu-id="a8706-488">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="a8706-489">Questo valore delle dimensioni del buffer restituito può essere passato in una chiamata successiva per eseguire una query per il token di associazione del canale.</span><span class="sxs-lookup"><span data-stu-id="a8706-489">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="a8706-490">Questi passaggi sono necessari quando si gestisce WINHTTP CALLBACK STATUS REQUEST se si desidera modificare le intestazioni della richiesta \_ in base al token di associazione del \_ \_ canale.</span><span class="sxs-lookup"><span data-stu-id="a8706-490">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="a8706-491">Si noti che Windows XP e Vista non supportano la modifica delle intestazioni delle richieste durante questo callback.</span><span class="sxs-lookup"><span data-stu-id="a8706-491">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-492"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**CONTESTO DELLA \_ CATENA DI CERTIFICATI DEL SERVER \_ \_ \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-492"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-493">Recupera il contesto della catena di certificazione del server.</span><span class="sxs-lookup"><span data-stu-id="a8706-493">Retrieves the server certification chain context.</span></span> <span data-ttu-id="a8706-494">**WINHTTP \_ OPTION \_ SERVER \_ CERT CHAIN \_ \_ CONTEXT** può essere passato per ottenere un puntatore duplicato a **CERT CHAIN \_ \_ CONTEXT** per una catena di certificati server ricevuta durante una connessione SSL negoziata.</span><span class="sxs-lookup"><span data-stu-id="a8706-494">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="a8706-495">Il client deve chiamare [**CertFreeCertificateContext sul**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) puntatore PCCERT CONTEXT restituito che \_ viene inserito nel buffer.</span><span class="sxs-lookup"><span data-stu-id="a8706-495">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-496"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**CONTESTO DEL CERTIFICATO \_ \_ DEL SERVER \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-496"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-497">Recupera il contesto di certificazione del server.</span><span class="sxs-lookup"><span data-stu-id="a8706-497">Retrieves the server certification context.</span></span> <span data-ttu-id="a8706-498">**WINHTTP \_ OPTION \_ SERVER \_ CERT CONTEXT \_ può** essere passato per ottenere un puntatore duplicato a [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) per un certificato del server ricevuto durante una connessione SSL negoziata.</span><span class="sxs-lookup"><span data-stu-id="a8706-498">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="a8706-499">Il client deve chiamare [**CertFreeCertificateContext sul**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) puntatore PCCERT CONTEXT restituito che \_ viene inserito nel buffer.</span><span class="sxs-lookup"><span data-stu-id="a8706-499">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-500"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**NOME \_ \_ SPN DEL SERVER \_ DELL'OPZIONE WINHTTP \_ USATO**</span><span class="sxs-lookup"><span data-stu-id="a8706-500"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-501">Ottiene il nome dell'entità server del server fornito da WinHTTP a SSPI durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a8706-501">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="a8706-502">Questo valore stringa può essere passato a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) dopo un errore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a8706-502">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-503"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**NOME \_ \_ SPN DELL'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-503"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-504">Include o rimuove il numero di porta del server quando il nome SPN (nome dell'entità servizio) viene compilato per l'autenticazione Kerberos o Negotiate Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a8706-504">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="a8706-505">Questo flag è uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8706-505">This flag is one of the following values:</span></span>

| <span data-ttu-id="a8706-506">Termine</span><span class="sxs-lookup"><span data-stu-id="a8706-506">Term</span></span> | <span data-ttu-id="a8706-507">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8706-507">Description</span></span> |
|-|-|
| <span data-ttu-id="a8706-508"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ DISABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="a8706-508"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="a8706-509">Rimuove il numero di porta del server.</span><span class="sxs-lookup"><span data-stu-id="a8706-509">Removes the server port number.</span></span> |
| <span data-ttu-id="a8706-510"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>PORTA DEL \_ \_ SERVER SPN ABILITATA \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-510"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="a8706-511">Include il numero di porta del server.</span><span class="sxs-lookup"><span data-stu-id="a8706-511">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="a8706-512"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**CODICE DI ERRORE \_ DEL \_ FLUSSO \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-512"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="a8706-513">Questa opzione può essere eseguita su un handle di richiesta WinHttp e restituirà il codice di errore indicato da un frame RST_STREAM ricevuto in un flusso HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8706-513">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-514"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**OPZIONE WINHTTP \_ \_ TCP FAST \_ \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="a8706-514"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-515">Abilita TCP Fast Open per la connessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-515">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-516"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**OPZIONE \_ \_ WINHTTP TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="a8706-516"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-517">Questa opzione può essere impostata su un handle di sessione WinHttp per abilitare il comportamento keep-alive TCP nel socket sottostante.</span><span class="sxs-lookup"><span data-stu-id="a8706-517">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="a8706-518">Accetta uno [**struct \_ tcp keepalive.**](/windows/win32/winsock/sio-keepalive-vals)</span><span class="sxs-lookup"><span data-stu-id="a8706-518">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-519"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**OPZIONE WINHTTP \_ \_ TLS FALSE \_ \_ START**</span><span class="sxs-lookup"><span data-stu-id="a8706-519"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-520">Abilita TLS False Start per la connessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-520">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-521"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**OPZIONE WINHTTP \_ \_ \_ \_ FALLBACK NON SICURO DEL PROTOCOLLO TLS \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-521"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-522">Questa opzione può essere impostata su un handle di sessione WinHttp per controllare se è consentito il fallback a TLS 1.0 se si verifica un errore di handshake TLS con una versione del protocollo più recente.</span><span class="sxs-lookup"><span data-stu-id="a8706-522">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-523"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**EVENTO NOTIFICA \_ \_ DI SCARICAMENTO \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-523"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-524">Accetta un evento che verrà impostato quando l'ultimo callback è stato completato per una sessione specifica.</span><span class="sxs-lookup"><span data-stu-id="a8706-524">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="a8706-525">Questo flag deve essere usato in un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-525">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="a8706-526">L'evento non può essere chiuso fino a quando non è stato impostato da WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a8706-526">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-527"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**ANALISI \_ \_ DELL'INTESTAZIONE NON SICURA \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-527"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-528">Questa opzione è riservata per uso interno e non deve essere chiamata.</span><span class="sxs-lookup"><span data-stu-id="a8706-528">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-529"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**AGGIORNAMENTO \_ DELL'OPZIONE WINHTTP \_ AL WEB \_ \_ \_ SOCKET**</span><span class="sxs-lookup"><span data-stu-id="a8706-529"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-530">Indica all'oggetto stack di avviare un processo di handshake WebSocket [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="a8706-530">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="a8706-531">Questa opzione non accetta parametri.</span><span class="sxs-lookup"><span data-stu-id="a8706-531">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-532"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL DELL'OPZIONE WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-532"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-533">Recupera un valore stringa che contiene l'URL completo di una risorsa scaricata.</span><span class="sxs-lookup"><span data-stu-id="a8706-533">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="a8706-534">Se l'URL originale contiene dati aggiuntivi, ad esempio stringhe di ricerca o ancoraggi, o se la chiamata è stata reindirizzata, l'URL restituito è diverso da quello originale.</span><span class="sxs-lookup"><span data-stu-id="a8706-534">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="a8706-535">L'applicazione deve passare un buffer, ridimensionato in byte, sufficientemente grande da contenere l'URL restituito in caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="a8706-535">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-536"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**L'OPZIONE WINHTTP \_ USA LE CREDENZIALI GLOBALI DEL \_ \_ \_ \_ SERVER**</span><span class="sxs-lookup"><span data-stu-id="a8706-536"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-537">Accetta un **bool e** può essere impostato solo un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-537">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="a8706-538">Verrà propagato solo agli handle creati dall'handle di sessione dopo l'impostazione dell'opzione .</span><span class="sxs-lookup"><span data-stu-id="a8706-538">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="a8706-539">Se **TRUE,** questa opzione fa in modo che come ultima risorsa l'uso di credenziali del server globali di cui è stato fatto il push da WinInet.</span><span class="sxs-lookup"><span data-stu-id="a8706-539">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="a8706-540">Il valore predefinito per questa opzione è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a8706-540">The default for this option is **FALSE**.</span></span> <span data-ttu-id="a8706-541">Questa opzione richiede la chiave del Registro **di sistema HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Impostazioni \\ Internet. ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="a8706-541">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="a8706-542">Questa chiave del Registro di sistema non è presente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a8706-542">This registry key is not present by default.</span></span> <span data-ttu-id="a8706-543">Quando è impostata, WinINet invierà le credenziali a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a8706-543">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="a8706-544">Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono impostate credenziali nell'handle corrente, userà le credenziali fornite da WinINet.</span><span class="sxs-lookup"><span data-stu-id="a8706-544">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-545"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**OPZIONE WINHTTP \_ \_ AGENTE \_ UTENTE**</span><span class="sxs-lookup"><span data-stu-id="a8706-545"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-546">Imposta o recupera [](glossary.md) la stringa dell'agente utente sugli handle forniti da [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) e usati nelle funzioni [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) successive, purché non venga sottoposto a override da un'intestazione aggiunta da [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) **o WinHttpSendRequest.**</span><span class="sxs-lookup"><span data-stu-id="a8706-546">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="a8706-547">Quando si recupera un agente utente, l'applicazione deve passare un buffer, ridimensionato in byte, sufficientemente grande da contenere l'URL restituito in caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="a8706-547">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="a8706-548">Quando si imposta l'agente utente, la dimensione del buffer è la lunghezza della stringa, in caratteri, più il carattere **di terminazione NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8706-548">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-549"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**NOME UTENTE \_ DELL'OPZIONE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-549"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-550">Imposta o recupera una stringa contenente il nome utente.</span><span class="sxs-lookup"><span data-stu-id="a8706-550">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-551"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**TIMEOUT CHIUSURA \_ \_ WEB SOCKET \_ DELL'OPZIONE \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-551"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-552">Imposta il tempo, in millisecondi, di attesa di [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) per completare l'handshake di chiusura.</span><span class="sxs-lookup"><span data-stu-id="a8706-552">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="a8706-553">Il valore predefinito è 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="a8706-553">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-554"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**OPZIONE WINHTTP \_ \_ INTERVALLO \_ \_ KEEPALIVE PER WEB \_ SOCKET**</span><span class="sxs-lookup"><span data-stu-id="a8706-554"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-555">Imposta l'intervallo, in millisecondi, per l'invio di un pacchetto keep-alive sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="a8706-555">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="a8706-556">L'intervallo predefinito è 30000 (30 secondi).</span><span class="sxs-lookup"><span data-stu-id="a8706-556">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="a8706-557">L'intervallo minimo è 15000 (15 secondi).</span><span class="sxs-lookup"><span data-stu-id="a8706-557">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="a8706-558">[**L'uso di WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per impostare un valore inferiore a 15000 restituirà con **ERROR INVALID \_ \_ PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="a8706-558">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="a8706-559">Il valore predefinito per **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** viene letto da **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="a8706-559">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="a8706-560">Se non è impostato un valore, verrà usato il valore predefinito 30000.</span><span class="sxs-lookup"><span data-stu-id="a8706-560">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="a8706-561">Non è possibile avere un intervallo keep-live inferiore a 15000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a8706-561">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-562"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**DIMENSIONI BUFFER \_ DI RICEZIONE WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-562"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-563">Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di ricezione da utilizzare nelle connessioni WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a8706-563">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-564"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**DIMENSIONI BUFFER \_ DI INVIO WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-564"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-565">Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di invio da usare nelle connessioni WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a8706-565">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-566"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**CONTEGGIO \_ THREAD DI LAVORO \_ \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-566"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-567">Imposta un valore long integer senza segno che specifica il numero di thread di lavoro che il pool di thread deve usare per i completamenti asincroni.</span><span class="sxs-lookup"><span data-stu-id="a8706-567">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="a8706-568">Il valore predefinito di questa opzione è zero, che specifica che il numero di thread di lavoro è uguale al numero di CPU nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a8706-568">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="a8706-569">Questa opzione può essere impostata solo su un handle **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) prima che si sia verificata un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="a8706-569">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="a8706-570">Questa opzione può essere impostata una sola volta.</span><span class="sxs-lookup"><span data-stu-id="a8706-570">This option can only be set once.</span></span>

<span data-ttu-id="a8706-571">**Windows Server 2008 R2 e Windows 7:** Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a8706-571">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8706-572"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**DIMENSIONI DEL \_ BUFFER DI \_ SCRITTURA \_ DELL'OPZIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-572"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8706-573">Questa opzione è stata deprecata. non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="a8706-573">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8706-574">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8706-574">Remarks</span></span>

<span data-ttu-id="a8706-575">Nella tabella seguente sono elencati i flag di opzione specificando gli handle su cui possono agire, se possono essere sottoposti a query e impostati e il tipo di dati utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a8706-575">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="a8706-576">Una "X" indica che il flag di opzione è valido per l'uso con la funzione o l'handle, mentre "-" specifica che il flag di opzione non è valido.</span><span class="sxs-lookup"><span data-stu-id="a8706-576">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="a8706-577">Se si tenta di impostare o eseguire una query su un flag di opzione in una versione di Windows in cui non è supportata, verrà generato **l'errore \_ WINHTTP \_ INVALID \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="a8706-577">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="a8706-578">Flag di opzione e tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a8706-578">Option flag, and data type</span></span> | <span data-ttu-id="a8706-579">Handle di sessione</span><span class="sxs-lookup"><span data-stu-id="a8706-579">Session handle</span></span> | <span data-ttu-id="a8706-580">Handle di richiesta</span><span class="sxs-lookup"><span data-stu-id="a8706-580">Request handle</span></span> | <span data-ttu-id="a8706-581">Opzione di query</span><span class="sxs-lookup"><span data-stu-id="a8706-581">Query option</span></span> | <span data-ttu-id="a8706-582">Opzione SET</span><span class="sxs-lookup"><span data-stu-id="a8706-582">Set option</span></span> | <span data-ttu-id="a8706-583">Versione minima di Windows</span><span class="sxs-lookup"><span data-stu-id="a8706-583">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="a8706-584">L'OPZIONE WINHTTP \_ \_ ASSICURA CALLBACK NON \_ \_ \_ BLOCCANTI</span><span class="sxs-lookup"><span data-stu-id="a8706-584">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="a8706-585">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-585">**BOOL**</span></span> | <span data-ttu-id="a8706-586">X</span><span class="sxs-lookup"><span data-stu-id="a8706-586">X</span></span> | \- | \- | <span data-ttu-id="a8706-587">X</span><span class="sxs-lookup"><span data-stu-id="a8706-587">X</span></span> | \- |
| <span data-ttu-id="a8706-588">CRITERIO DI \_ ACCESSO \_ AUTOMATICO DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-588">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="a8706-589">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-589">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-590">X</span><span class="sxs-lookup"><span data-stu-id="a8706-590">X</span></span> | \- | <span data-ttu-id="a8706-591">X</span><span class="sxs-lookup"><span data-stu-id="a8706-591">X</span></span> | \- |
| <span data-ttu-id="a8706-592">CALLBACK \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-592">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="a8706-593">**Lpvoid**</span><span class="sxs-lookup"><span data-stu-id="a8706-593">**LPVOID**</span></span> | <span data-ttu-id="a8706-594">X</span><span class="sxs-lookup"><span data-stu-id="a8706-594">X</span></span> | <span data-ttu-id="a8706-595">X</span><span class="sxs-lookup"><span data-stu-id="a8706-595">X</span></span> | <span data-ttu-id="a8706-596">X</span><span class="sxs-lookup"><span data-stu-id="a8706-596">X</span></span> | <span data-ttu-id="a8706-597">X</span><span class="sxs-lookup"><span data-stu-id="a8706-597">X</span></span> | \- |
| <span data-ttu-id="a8706-598">CONTESTO DEL CERTIFICATO \_ \_ CLIENT \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-598">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="a8706-599">**CONTESTO DEL \_ CERTIFICATO**</span><span class="sxs-lookup"><span data-stu-id="a8706-599">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="a8706-600">X</span><span class="sxs-lookup"><span data-stu-id="a8706-600">X</span></span> | \- | <span data-ttu-id="a8706-601">X</span><span class="sxs-lookup"><span data-stu-id="a8706-601">X</span></span> | <span data-ttu-id="a8706-602">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8706-602">Windows Vista</span></span> |
| <span data-ttu-id="a8706-603">ELENCO AUTORITÀ \_ DI CERTIFICAZIONE DEL CERTIFICATO CLIENT \_ \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-603">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="a8706-604">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="a8706-604">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="a8706-605">X</span><span class="sxs-lookup"><span data-stu-id="a8706-605">X</span></span> | <span data-ttu-id="a8706-606">X</span><span class="sxs-lookup"><span data-stu-id="a8706-606">X</span></span> | \- | <span data-ttu-id="a8706-607">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8706-607">Windows Vista</span></span> |
| <span data-ttu-id="a8706-608">TABELLA CODICI \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-608">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="a8706-609">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-609">**DWORD**</span></span> | <span data-ttu-id="a8706-610">X</span><span class="sxs-lookup"><span data-stu-id="a8706-610">X</span></span> | \- | \- | <span data-ttu-id="a8706-611">X</span><span class="sxs-lookup"><span data-stu-id="a8706-611">X</span></span> | \- |
| <span data-ttu-id="a8706-612">OPZIONE WINHTTP \_ \_ - CONFIGURARE \_ \_ L'AUTENTICAZIONE PASSPORT</span><span class="sxs-lookup"><span data-stu-id="a8706-612">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="a8706-613">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-613">**DWORD**</span></span> | <span data-ttu-id="a8706-614">X</span><span class="sxs-lookup"><span data-stu-id="a8706-614">X</span></span> | \- | \- | <span data-ttu-id="a8706-615">X</span><span class="sxs-lookup"><span data-stu-id="a8706-615">X</span></span> | \- |
| <span data-ttu-id="a8706-616">TENTATIVI \_ DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-616">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="a8706-617">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-617">**DWORD**</span></span> | <span data-ttu-id="a8706-618">X</span><span class="sxs-lookup"><span data-stu-id="a8706-618">X</span></span> | <span data-ttu-id="a8706-619">X</span><span class="sxs-lookup"><span data-stu-id="a8706-619">X</span></span> | <span data-ttu-id="a8706-620">X</span><span class="sxs-lookup"><span data-stu-id="a8706-620">X</span></span> | <span data-ttu-id="a8706-621">X</span><span class="sxs-lookup"><span data-stu-id="a8706-621">X</span></span> | \- |
| <span data-ttu-id="a8706-622">TIMEOUT DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-622">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="a8706-623">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-623">**DWORD**</span></span> | <span data-ttu-id="a8706-624">X</span><span class="sxs-lookup"><span data-stu-id="a8706-624">X</span></span> | <span data-ttu-id="a8706-625">X</span><span class="sxs-lookup"><span data-stu-id="a8706-625">X</span></span> | <span data-ttu-id="a8706-626">X</span><span class="sxs-lookup"><span data-stu-id="a8706-626">X</span></span> | <span data-ttu-id="a8706-627">X</span><span class="sxs-lookup"><span data-stu-id="a8706-627">X</span></span> | \- |
| <span data-ttu-id="a8706-628">INFORMAZIONI DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-628">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="a8706-629">**INFORMAZIONI DI \_ CONNESSIONE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-629">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="a8706-630">X</span><span class="sxs-lookup"><span data-stu-id="a8706-630">X</span></span> | <span data-ttu-id="a8706-631">X</span><span class="sxs-lookup"><span data-stu-id="a8706-631">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-632">STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V0</span><span class="sxs-lookup"><span data-stu-id="a8706-632">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="a8706-633">**TCP \_ INFO \_ v0**</span><span class="sxs-lookup"><span data-stu-id="a8706-633">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="a8706-634">X</span><span class="sxs-lookup"><span data-stu-id="a8706-634">X</span></span> | <span data-ttu-id="a8706-635">X</span><span class="sxs-lookup"><span data-stu-id="a8706-635">X</span></span> | \- | <span data-ttu-id="a8706-636">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="a8706-636">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a8706-637">STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V1</span><span class="sxs-lookup"><span data-stu-id="a8706-637">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="a8706-638">**TCP \_ INFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a8706-638">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="a8706-639">X</span><span class="sxs-lookup"><span data-stu-id="a8706-639">X</span></span> | <span data-ttu-id="a8706-640">X</span><span class="sxs-lookup"><span data-stu-id="a8706-640">X</span></span> | \- | <span data-ttu-id="a8706-641">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="a8706-641">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a8706-642">VALORE DI CONTESTO \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-642">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="a8706-643">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-643">**DWORD\_PTR**</span></span> | <span data-ttu-id="a8706-644">X</span><span class="sxs-lookup"><span data-stu-id="a8706-644">X</span></span> | <span data-ttu-id="a8706-645">X</span><span class="sxs-lookup"><span data-stu-id="a8706-645">X</span></span> | <span data-ttu-id="a8706-646">X</span><span class="sxs-lookup"><span data-stu-id="a8706-646">X</span></span> | <span data-ttu-id="a8706-647">X</span><span class="sxs-lookup"><span data-stu-id="a8706-647">X</span></span> | \- |
| <span data-ttu-id="a8706-648">\_ \_ DECOMPRESSIONE DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-648">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="a8706-649">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-649">**DWORD**</span></span> | <span data-ttu-id="a8706-650">X</span><span class="sxs-lookup"><span data-stu-id="a8706-650">X</span></span> | <span data-ttu-id="a8706-651">X</span><span class="sxs-lookup"><span data-stu-id="a8706-651">X</span></span> | \- | <span data-ttu-id="a8706-652">X</span><span class="sxs-lookup"><span data-stu-id="a8706-652">X</span></span> | <span data-ttu-id="a8706-653">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a8706-653">Windows 8.1</span></span> |
| <span data-ttu-id="a8706-654">OPZIONE WINHTTP \_ \_ DISABILITA \_ FUNZIONALITÀ</span><span class="sxs-lookup"><span data-stu-id="a8706-654">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="a8706-655">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-655">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-656">X</span><span class="sxs-lookup"><span data-stu-id="a8706-656">X</span></span> | \- | <span data-ttu-id="a8706-657">X</span><span class="sxs-lookup"><span data-stu-id="a8706-657">X</span></span> | \- |
| <span data-ttu-id="a8706-658">OPZIONE WINHTTP \_ \_ DISABILITA IL \_ \_ FALLBACK DEL \_ PROTOCOLLO SICURO</span><span class="sxs-lookup"><span data-stu-id="a8706-658">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="a8706-659">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-659">**BOOL**</span></span> | <span data-ttu-id="a8706-660">X</span><span class="sxs-lookup"><span data-stu-id="a8706-660">X</span></span> | \- | \- | <span data-ttu-id="a8706-661">X</span><span class="sxs-lookup"><span data-stu-id="a8706-661">X</span></span> | <span data-ttu-id="a8706-662">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="a8706-662">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a8706-663">OPZIONE WINHTTP \_ DISABILITA \_ CODA DI \_ \_ FLUSSO</span><span class="sxs-lookup"><span data-stu-id="a8706-663">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="a8706-664">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-664">**BOOL**</span></span> | <span data-ttu-id="a8706-665">X</span><span class="sxs-lookup"><span data-stu-id="a8706-665">X</span></span> | <span data-ttu-id="a8706-666">X</span><span class="sxs-lookup"><span data-stu-id="a8706-666">X</span></span> | \- | <span data-ttu-id="a8706-667">X</span><span class="sxs-lookup"><span data-stu-id="a8706-667">X</span></span> | <span data-ttu-id="a8706-668">Windows 10 versione 1809</span><span class="sxs-lookup"><span data-stu-id="a8706-668">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="a8706-669">OPZIONE WINHTTP \_ \_ - ABILITARE LA \_ FUNZIONALITÀ</span><span class="sxs-lookup"><span data-stu-id="a8706-669">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="a8706-670">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-670">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="a8706-671">X</span><span class="sxs-lookup"><span data-stu-id="a8706-671">X</span></span> | \- |
| <span data-ttu-id="a8706-672">OPZIONE WINHTTP \_ \_ ABILITA PROTOCOLLO \_ \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-672">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="a8706-673">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-673">**DWORD**</span></span> | <span data-ttu-id="a8706-674">X</span><span class="sxs-lookup"><span data-stu-id="a8706-674">X</span></span> | <span data-ttu-id="a8706-675">X</span><span class="sxs-lookup"><span data-stu-id="a8706-675">X</span></span> | \- | <span data-ttu-id="a8706-676">X</span><span class="sxs-lookup"><span data-stu-id="a8706-676">X</span></span> | <span data-ttu-id="a8706-677">Windows 10 versione 1607</span><span class="sxs-lookup"><span data-stu-id="a8706-677">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="a8706-678">OPZIONE WINHTTP \_ \_ ENABLE \_ HTTP2 PLUS CLIENT \_ \_ \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="a8706-678">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="a8706-679">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-679">**BOOL**</span></span> | <span data-ttu-id="a8706-680">X</span><span class="sxs-lookup"><span data-stu-id="a8706-680">X</span></span> | \- | \- | <span data-ttu-id="a8706-681">X</span><span class="sxs-lookup"><span data-stu-id="a8706-681">X</span></span> | <span data-ttu-id="a8706-682">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="a8706-682">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a8706-683">OPZIONE WINHTTP \_ \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="a8706-683">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="a8706-684">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-684">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a8706-685">X</span><span class="sxs-lookup"><span data-stu-id="a8706-685">X</span></span> | <span data-ttu-id="a8706-686">X</span><span class="sxs-lookup"><span data-stu-id="a8706-686">X</span></span> | \- |
| <span data-ttu-id="a8706-687">OPZIONE WINHTTP \_ \_ ENCODE \_ EXTRA</span><span class="sxs-lookup"><span data-stu-id="a8706-687">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="a8706-688">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-688">**BOOL**</span></span> | <span data-ttu-id="a8706-689">X</span><span class="sxs-lookup"><span data-stu-id="a8706-689">X</span></span> | <span data-ttu-id="a8706-690">X</span><span class="sxs-lookup"><span data-stu-id="a8706-690">X</span></span> | \- | <span data-ttu-id="a8706-691">X</span><span class="sxs-lookup"><span data-stu-id="a8706-691">X</span></span> | <span data-ttu-id="a8706-692">Windows 10 versione 1803</span><span class="sxs-lookup"><span data-stu-id="a8706-692">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="a8706-693">OPZIONE WINHTTP \_ \_ SCADENZA \_ CONNESSIONE</span><span class="sxs-lookup"><span data-stu-id="a8706-693">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="a8706-694">N/D</span><span class="sxs-lookup"><span data-stu-id="a8706-694">N/A</span></span> | \- | <span data-ttu-id="a8706-695">X</span><span class="sxs-lookup"><span data-stu-id="a8706-695">X</span></span> | \- | <span data-ttu-id="a8706-696">X</span><span class="sxs-lookup"><span data-stu-id="a8706-696">X</span></span> | <span data-ttu-id="a8706-697">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="a8706-697">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a8706-698">ERRORE ESTESO \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-698">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="a8706-699">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-699">**DWORD**</span></span> | <span data-ttu-id="a8706-700">X</span><span class="sxs-lookup"><span data-stu-id="a8706-700">X</span></span> | <span data-ttu-id="a8706-701">X</span><span class="sxs-lookup"><span data-stu-id="a8706-701">X</span></span> | <span data-ttu-id="a8706-702">X</span><span class="sxs-lookup"><span data-stu-id="a8706-702">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-703">CRED \_ \_ PROXY GLOBALI \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-703">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="a8706-704">**WINHTTP \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="a8706-704">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="a8706-705">X</span><span class="sxs-lookup"><span data-stu-id="a8706-705">X</span></span> | <span data-ttu-id="a8706-706">X</span><span class="sxs-lookup"><span data-stu-id="a8706-706">X</span></span> | \- | <span data-ttu-id="a8706-707">X</span><span class="sxs-lookup"><span data-stu-id="a8706-707">X</span></span> | \- |
| <span data-ttu-id="a8706-708">CRED \_ \_ SERVER GLOBALI \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-708">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="a8706-709">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="a8706-709">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="a8706-710">X</span><span class="sxs-lookup"><span data-stu-id="a8706-710">X</span></span> | <span data-ttu-id="a8706-711">X</span><span class="sxs-lookup"><span data-stu-id="a8706-711">X</span></span> | \- | <span data-ttu-id="a8706-712">X</span><span class="sxs-lookup"><span data-stu-id="a8706-712">X</span></span> | \- |
| <span data-ttu-id="a8706-713">TIPO DI \_ \_ HANDLE DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-713">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="a8706-714">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-714">**DWORD**</span></span> | <span data-ttu-id="a8706-715">X</span><span class="sxs-lookup"><span data-stu-id="a8706-715">X</span></span> | <span data-ttu-id="a8706-716">X</span><span class="sxs-lookup"><span data-stu-id="a8706-716">X</span></span> | <span data-ttu-id="a8706-717">X</span><span class="sxs-lookup"><span data-stu-id="a8706-717">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-718">PROTOCOLLO \_ \_ HTTP DELL'OPZIONE WINHTTP \_ \_ OBBLIGATORIO</span><span class="sxs-lookup"><span data-stu-id="a8706-718">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="a8706-719">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-719">**BOOL**</span></span> | <span data-ttu-id="a8706-720">X</span><span class="sxs-lookup"><span data-stu-id="a8706-720">X</span></span> | <span data-ttu-id="a8706-721">X</span><span class="sxs-lookup"><span data-stu-id="a8706-721">X</span></span> | \- | <span data-ttu-id="a8706-722">X</span><span class="sxs-lookup"><span data-stu-id="a8706-722">X</span></span> | <span data-ttu-id="a8706-723">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="a8706-723">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a8706-724">PROTOCOLLO \_ \_ HTTP DELL'OPZIONE WINHTTP \_ \_ USATO</span><span class="sxs-lookup"><span data-stu-id="a8706-724">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="a8706-725">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-725">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-726">X</span><span class="sxs-lookup"><span data-stu-id="a8706-726">X</span></span> | <span data-ttu-id="a8706-727">X</span><span class="sxs-lookup"><span data-stu-id="a8706-727">X</span></span> | \- | <span data-ttu-id="a8706-728">Windows 10 versione 1607</span><span class="sxs-lookup"><span data-stu-id="a8706-728">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="a8706-729">VERSIONE \_ \_ HTTP DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-729">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="a8706-730">**INFORMAZIONI \_ SULLA VERSIONE \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-730">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="a8706-731">X</span><span class="sxs-lookup"><span data-stu-id="a8706-731">X</span></span> | <span data-ttu-id="a8706-732">X</span><span class="sxs-lookup"><span data-stu-id="a8706-732">X</span></span> | <span data-ttu-id="a8706-733">X</span><span class="sxs-lookup"><span data-stu-id="a8706-733">X</span></span> | <span data-ttu-id="a8706-734">X</span><span class="sxs-lookup"><span data-stu-id="a8706-734">X</span></span> | \- |
| <span data-ttu-id="a8706-735">OPZIONE WINHTTP \_ \_ HTTP2 \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="a8706-735">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="a8706-736">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-736">**DWORD**</span></span> | <span data-ttu-id="a8706-737">X</span><span class="sxs-lookup"><span data-stu-id="a8706-737">X</span></span> | \- | \- | <span data-ttu-id="a8706-738">X</span><span class="sxs-lookup"><span data-stu-id="a8706-738">X</span></span> | <span data-ttu-id="a8706-739">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="a8706-739">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a8706-740">OPZIONE WINHTTP \_ \_ HTTP2 \_ PLUS TRANSFER \_ \_ ENCODING</span><span class="sxs-lookup"><span data-stu-id="a8706-740">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="a8706-741">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-741">**BOOL**</span></span> | <span data-ttu-id="a8706-742">X</span><span class="sxs-lookup"><span data-stu-id="a8706-742">X</span></span> | <span data-ttu-id="a8706-743">X</span><span class="sxs-lookup"><span data-stu-id="a8706-743">X</span></span> | \- | <span data-ttu-id="a8706-744">X</span><span class="sxs-lookup"><span data-stu-id="a8706-744">X</span></span> | <span data-ttu-id="a8706-745">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="a8706-745">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a8706-746">OPZIONE WINHTTP \_ \_ IGNORA REVOCA CERTIFICATO \_ \_ \_ OFFLINE</span><span class="sxs-lookup"><span data-stu-id="a8706-746">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="a8706-747">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-747">**BOOL**</span></span> | \- | <span data-ttu-id="a8706-748">X</span><span class="sxs-lookup"><span data-stu-id="a8706-748">X</span></span> | \- | <span data-ttu-id="a8706-749">X</span><span class="sxs-lookup"><span data-stu-id="a8706-749">X</span></span> | <span data-ttu-id="a8706-750">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="a8706-750">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a8706-751">OPZIONE \_ \_ WINHTTP \_ FALLBACK RAPIDO IPV6 \_</span><span class="sxs-lookup"><span data-stu-id="a8706-751">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="a8706-752">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-752">**BOOL**</span></span> | <span data-ttu-id="a8706-753">X</span><span class="sxs-lookup"><span data-stu-id="a8706-753">X</span></span> | \- | \- | <span data-ttu-id="a8706-754">X</span><span class="sxs-lookup"><span data-stu-id="a8706-754">X</span></span> | <span data-ttu-id="a8706-755">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="a8706-755">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a8706-756">L'OPZIONE WINHTTP \_ \_ È PROXY CONNECT \_ \_ \_ RESPONSE</span><span class="sxs-lookup"><span data-stu-id="a8706-756">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="a8706-757">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-757">**BOOL**</span></span> | <span data-ttu-id="a8706-758">X</span><span class="sxs-lookup"><span data-stu-id="a8706-758">X</span></span> | <span data-ttu-id="a8706-759">X</span><span class="sxs-lookup"><span data-stu-id="a8706-759">X</span></span> | <span data-ttu-id="a8706-760">X</span><span class="sxs-lookup"><span data-stu-id="a8706-760">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-761">OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ 1 \_ 0 \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="a8706-761">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="a8706-762">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-762">**DWORD**</span></span> | <span data-ttu-id="a8706-763">X</span><span class="sxs-lookup"><span data-stu-id="a8706-763">X</span></span> | \- | <span data-ttu-id="a8706-764">X</span><span class="sxs-lookup"><span data-stu-id="a8706-764">X</span></span> | <span data-ttu-id="a8706-765">X</span><span class="sxs-lookup"><span data-stu-id="a8706-765">X</span></span> | \- |
| <span data-ttu-id="a8706-766">OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="a8706-766">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="a8706-767">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-767">**DWORD**</span></span> | <span data-ttu-id="a8706-768">X</span><span class="sxs-lookup"><span data-stu-id="a8706-768">X</span></span> | \- | <span data-ttu-id="a8706-769">X</span><span class="sxs-lookup"><span data-stu-id="a8706-769">X</span></span> | <span data-ttu-id="a8706-770">X</span><span class="sxs-lookup"><span data-stu-id="a8706-770">X</span></span> | \- |
| <span data-ttu-id="a8706-771">OPZIONE WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS</span><span class="sxs-lookup"><span data-stu-id="a8706-771">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="a8706-772">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-772">**DWORD**</span></span> | <span data-ttu-id="a8706-773">X</span><span class="sxs-lookup"><span data-stu-id="a8706-773">X</span></span> | <span data-ttu-id="a8706-774">X</span><span class="sxs-lookup"><span data-stu-id="a8706-774">X</span></span> | <span data-ttu-id="a8706-775">X</span><span class="sxs-lookup"><span data-stu-id="a8706-775">X</span></span> | <span data-ttu-id="a8706-776">X</span><span class="sxs-lookup"><span data-stu-id="a8706-776">X</span></span> | \- |
| <span data-ttu-id="a8706-777">OPZIONE WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE</span><span class="sxs-lookup"><span data-stu-id="a8706-777">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="a8706-778">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-778">**DWORD**</span></span> | <span data-ttu-id="a8706-779">X</span><span class="sxs-lookup"><span data-stu-id="a8706-779">X</span></span> | <span data-ttu-id="a8706-780">X</span><span class="sxs-lookup"><span data-stu-id="a8706-780">X</span></span> | <span data-ttu-id="a8706-781">X</span><span class="sxs-lookup"><span data-stu-id="a8706-781">X</span></span> | <span data-ttu-id="a8706-782">X</span><span class="sxs-lookup"><span data-stu-id="a8706-782">X</span></span> | \- |
| <span data-ttu-id="a8706-783">OPZIONE WINHTTP \_ \_ DIMENSIONE MASSIMA \_ \_ SVUOTAMENTO \_ RISPOSTA</span><span class="sxs-lookup"><span data-stu-id="a8706-783">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="a8706-784">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-784">**DWORD**</span></span> | <span data-ttu-id="a8706-785">X</span><span class="sxs-lookup"><span data-stu-id="a8706-785">X</span></span> | <span data-ttu-id="a8706-786">X</span><span class="sxs-lookup"><span data-stu-id="a8706-786">X</span></span> | <span data-ttu-id="a8706-787">X</span><span class="sxs-lookup"><span data-stu-id="a8706-787">X</span></span> | <span data-ttu-id="a8706-788">X</span><span class="sxs-lookup"><span data-stu-id="a8706-788">X</span></span> | \- |
| <span data-ttu-id="a8706-789">DIMENSIONI MASSIME \_ INTESTAZIONE RISPOSTA \_ \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-789">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="a8706-790">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-790">**DWORD**</span></span> | <span data-ttu-id="a8706-791">X</span><span class="sxs-lookup"><span data-stu-id="a8706-791">X</span></span> | <span data-ttu-id="a8706-792">X</span><span class="sxs-lookup"><span data-stu-id="a8706-792">X</span></span> | <span data-ttu-id="a8706-793">X</span><span class="sxs-lookup"><span data-stu-id="a8706-793">X</span></span> | <span data-ttu-id="a8706-794">X</span><span class="sxs-lookup"><span data-stu-id="a8706-794">X</span></span> | \- |
| <span data-ttu-id="a8706-795">HANDLE PADRE \_ DELL'OPZIONE WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8706-795">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="a8706-796">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="a8706-796">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="a8706-797">X</span><span class="sxs-lookup"><span data-stu-id="a8706-797">X</span></span> | <span data-ttu-id="a8706-798">X</span><span class="sxs-lookup"><span data-stu-id="a8706-798">X</span></span> | <span data-ttu-id="a8706-799">X</span><span class="sxs-lookup"><span data-stu-id="a8706-799">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-800">TESTO \_ \_ COBRANDING DELL'OPZIONE WINHTTP PASSPORT \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8706-800">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="a8706-801">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-801">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-802">X</span><span class="sxs-lookup"><span data-stu-id="a8706-802">X</span></span> | <span data-ttu-id="a8706-803">X</span><span class="sxs-lookup"><span data-stu-id="a8706-803">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-804">URL \_ \_ \_ COBRANDING DELL'OPZIONE WINHTTP PASSPORT \_</span><span class="sxs-lookup"><span data-stu-id="a8706-804">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="a8706-805">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-805">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-806">X</span><span class="sxs-lookup"><span data-stu-id="a8706-806">X</span></span> | <span data-ttu-id="a8706-807">X</span><span class="sxs-lookup"><span data-stu-id="a8706-807">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-808">URL \_ RESTITUITO \_ PASSPORT DELL'OPZIONE WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8706-808">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="a8706-809">**Lpvoid**</span><span class="sxs-lookup"><span data-stu-id="a8706-809">**LPVOID**</span></span> | \- | <span data-ttu-id="a8706-810">X</span><span class="sxs-lookup"><span data-stu-id="a8706-810">X</span></span> | <span data-ttu-id="a8706-811">X</span><span class="sxs-lookup"><span data-stu-id="a8706-811">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-812">OPZIONE WINHTTP \_ \_ - \_ DISCONNESSIONE PASSPORT \_</span><span class="sxs-lookup"><span data-stu-id="a8706-812">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="a8706-813">**Lpvoid**</span><span class="sxs-lookup"><span data-stu-id="a8706-813">**LPVOID**</span></span> | <span data-ttu-id="a8706-814">X</span><span class="sxs-lookup"><span data-stu-id="a8706-814">X</span></span> | \- | \- | <span data-ttu-id="a8706-815">X</span><span class="sxs-lookup"><span data-stu-id="a8706-815">X</span></span> | \- |
| <span data-ttu-id="a8706-816">PASSWORD \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-816">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="a8706-817">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-817">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-818">X</span><span class="sxs-lookup"><span data-stu-id="a8706-818">X</span></span> | <span data-ttu-id="a8706-819">X</span><span class="sxs-lookup"><span data-stu-id="a8706-819">X</span></span> | <span data-ttu-id="a8706-820">X</span><span class="sxs-lookup"><span data-stu-id="a8706-820">X</span></span> | \- |
| <span data-ttu-id="a8706-821">PROXY \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-821">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="a8706-822">**INFORMAZIONI SUL PROXY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-822">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="a8706-823">X</span><span class="sxs-lookup"><span data-stu-id="a8706-823">X</span></span> | <span data-ttu-id="a8706-824">X</span><span class="sxs-lookup"><span data-stu-id="a8706-824">X</span></span> | <span data-ttu-id="a8706-825">X</span><span class="sxs-lookup"><span data-stu-id="a8706-825">X</span></span> | <span data-ttu-id="a8706-826">X</span><span class="sxs-lookup"><span data-stu-id="a8706-826">X</span></span> | \- |
| <span data-ttu-id="a8706-827">PASSWORD PROXY \_ DELL'OPZIONE WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8706-827">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="a8706-828">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-828">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-829">X</span><span class="sxs-lookup"><span data-stu-id="a8706-829">X</span></span> | <span data-ttu-id="a8706-830">X</span><span class="sxs-lookup"><span data-stu-id="a8706-830">X</span></span> | <span data-ttu-id="a8706-831">X</span><span class="sxs-lookup"><span data-stu-id="a8706-831">X</span></span> | \- |
| <span data-ttu-id="a8706-832">NOME \_ \_ SPN PROXY \_ DELL'OPZIONE WINHTTP \_ USATO</span><span class="sxs-lookup"><span data-stu-id="a8706-832">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="a8706-833">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-833">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-834">X</span><span class="sxs-lookup"><span data-stu-id="a8706-834">X</span></span> | <span data-ttu-id="a8706-835">X</span><span class="sxs-lookup"><span data-stu-id="a8706-835">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-836">NOME UTENTE \_ \_ PROXY DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-836">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="a8706-837">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-837">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-838">X</span><span class="sxs-lookup"><span data-stu-id="a8706-838">X</span></span> | <span data-ttu-id="a8706-839">X</span><span class="sxs-lookup"><span data-stu-id="a8706-839">X</span></span> | <span data-ttu-id="a8706-840">X</span><span class="sxs-lookup"><span data-stu-id="a8706-840">X</span></span> | \- |
| <span data-ttu-id="a8706-841">DIMENSIONI DEL \_ \_ BUFFER DI LETTURA \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-841">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a8706-842">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-842">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-843">X</span><span class="sxs-lookup"><span data-stu-id="a8706-843">X</span></span> | <span data-ttu-id="a8706-844">X</span><span class="sxs-lookup"><span data-stu-id="a8706-844">X</span></span> | <span data-ttu-id="a8706-845">X</span><span class="sxs-lookup"><span data-stu-id="a8706-845">X</span></span> | \- |
| <span data-ttu-id="a8706-846">L'OPZIONE WINHTTP \_ RICEVE LA RISPOSTA DI CONNESSIONE \_ \_ \_ \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="a8706-846">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="a8706-847">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-847">**BOOL**</span></span> | <span data-ttu-id="a8706-848">X</span><span class="sxs-lookup"><span data-stu-id="a8706-848">X</span></span> | <span data-ttu-id="a8706-849">X</span><span class="sxs-lookup"><span data-stu-id="a8706-849">X</span></span> | \- | <span data-ttu-id="a8706-850">X</span><span class="sxs-lookup"><span data-stu-id="a8706-850">X</span></span> | \- |
| <span data-ttu-id="a8706-851">L'OPZIONE WINHTTP \_ RICEVE IL TIMEOUT DI \_ \_ \_ RISPOSTA</span><span class="sxs-lookup"><span data-stu-id="a8706-851">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="a8706-852">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-852">**DWORD**</span></span> | <span data-ttu-id="a8706-853">X</span><span class="sxs-lookup"><span data-stu-id="a8706-853">X</span></span> | <span data-ttu-id="a8706-854">X</span><span class="sxs-lookup"><span data-stu-id="a8706-854">X</span></span> | <span data-ttu-id="a8706-855">X</span><span class="sxs-lookup"><span data-stu-id="a8706-855">X</span></span> | <span data-ttu-id="a8706-856">X</span><span class="sxs-lookup"><span data-stu-id="a8706-856">X</span></span> | \- |
| <span data-ttu-id="a8706-857">TIMEOUT DI \_ RICEZIONE \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-857">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="a8706-858">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-858">**DWORD**</span></span> | <span data-ttu-id="a8706-859">X</span><span class="sxs-lookup"><span data-stu-id="a8706-859">X</span></span> | <span data-ttu-id="a8706-860">X</span><span class="sxs-lookup"><span data-stu-id="a8706-860">X</span></span> | <span data-ttu-id="a8706-861">X</span><span class="sxs-lookup"><span data-stu-id="a8706-861">X</span></span> | <span data-ttu-id="a8706-862">X</span><span class="sxs-lookup"><span data-stu-id="a8706-862">X</span></span> | \- |
| <span data-ttu-id="a8706-863">CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-863">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="a8706-864">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-864">**DWORD**</span></span> | <span data-ttu-id="a8706-865">X</span><span class="sxs-lookup"><span data-stu-id="a8706-865">X</span></span> | <span data-ttu-id="a8706-866">X</span><span class="sxs-lookup"><span data-stu-id="a8706-866">X</span></span> | <span data-ttu-id="a8706-867">X</span><span class="sxs-lookup"><span data-stu-id="a8706-867">X</span></span> | <span data-ttu-id="a8706-868">X</span><span class="sxs-lookup"><span data-stu-id="a8706-868">X</span></span> | \- |
| <span data-ttu-id="a8706-869">OPZIONE WINHTTP \_ \_ REJECT \_ USERPWD \_ \_ NELL'URL</span><span class="sxs-lookup"><span data-stu-id="a8706-869">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="a8706-870">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-870">**BOOL**</span></span> | \- | <span data-ttu-id="a8706-871">X</span><span class="sxs-lookup"><span data-stu-id="a8706-871">X</span></span> | \- | <span data-ttu-id="a8706-872">X</span><span class="sxs-lookup"><span data-stu-id="a8706-872">X</span></span> | \- |
| <span data-ttu-id="a8706-873">PRIORITÀ RICHIESTA \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-873">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="a8706-874">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-874">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-875">X</span><span class="sxs-lookup"><span data-stu-id="a8706-875">X</span></span> | <span data-ttu-id="a8706-876">X</span><span class="sxs-lookup"><span data-stu-id="a8706-876">X</span></span> | <span data-ttu-id="a8706-877">X</span><span class="sxs-lookup"><span data-stu-id="a8706-877">X</span></span> | \- |
| <span data-ttu-id="a8706-878">STATISTICHE DI \_ RICHIESTA \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-878">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="a8706-879">**STATISTICHE DELLE \_ RICHIESTE \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="a8706-879">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="a8706-880">X</span><span class="sxs-lookup"><span data-stu-id="a8706-880">X</span></span> | <span data-ttu-id="a8706-881">X</span><span class="sxs-lookup"><span data-stu-id="a8706-881">X</span></span> | \- | <span data-ttu-id="a8706-882">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="a8706-882">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a8706-883">TEMPI DI RICHIESTA \_ \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-883">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="a8706-884">**TEMPI DI RICHIESTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-884">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="a8706-885">X</span><span class="sxs-lookup"><span data-stu-id="a8706-885">X</span></span> | <span data-ttu-id="a8706-886">X</span><span class="sxs-lookup"><span data-stu-id="a8706-886">X</span></span> | \- | <span data-ttu-id="a8706-887">Windows 10 versione 1903</span><span class="sxs-lookup"><span data-stu-id="a8706-887">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="a8706-888">OPZIONE WINHTTP \_ \_ REQUIRE STREAM \_ \_ END</span><span class="sxs-lookup"><span data-stu-id="a8706-888">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="a8706-889">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-889">**BOOL**</span></span> | <span data-ttu-id="a8706-890">X</span><span class="sxs-lookup"><span data-stu-id="a8706-890">X</span></span> | <span data-ttu-id="a8706-891">X</span><span class="sxs-lookup"><span data-stu-id="a8706-891">X</span></span> | \- | <span data-ttu-id="a8706-892">X</span><span class="sxs-lookup"><span data-stu-id="a8706-892">X</span></span> | <span data-ttu-id="a8706-893">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="a8706-893">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a8706-894">NOME HOST \_ PER \_ LA RISOLUZIONE \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-894">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="a8706-895">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-895">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-896">X</span><span class="sxs-lookup"><span data-stu-id="a8706-896">X</span></span> | \- | <span data-ttu-id="a8706-897">X</span><span class="sxs-lookup"><span data-stu-id="a8706-897">X</span></span> | <span data-ttu-id="a8706-898">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="a8706-898">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a8706-899">TIMEOUT DI \_ RISOLUZIONE \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-899">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="a8706-900">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-900">**DWORD**</span></span> | <span data-ttu-id="a8706-901">X</span><span class="sxs-lookup"><span data-stu-id="a8706-901">X</span></span> | <span data-ttu-id="a8706-902">X</span><span class="sxs-lookup"><span data-stu-id="a8706-902">X</span></span> | <span data-ttu-id="a8706-903">X</span><span class="sxs-lookup"><span data-stu-id="a8706-903">X</span></span> | <span data-ttu-id="a8706-904">X</span><span class="sxs-lookup"><span data-stu-id="a8706-904">X</span></span> | \- |
| <span data-ttu-id="a8706-905">PROTOCOLLI SICURI \_ \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-905">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="a8706-906">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-906">**DWORD**</span></span> | <span data-ttu-id="a8706-907">X</span><span class="sxs-lookup"><span data-stu-id="a8706-907">X</span></span> | \- | \- | <span data-ttu-id="a8706-908">X</span><span class="sxs-lookup"><span data-stu-id="a8706-908">X</span></span> | \- |
| <span data-ttu-id="a8706-909">STRUCT \_ DEL CERTIFICATO DI SICUREZZA \_ \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-909">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="a8706-910">**INFORMAZIONI SUL CERTIFICATO WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8706-910">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="a8706-911">X</span><span class="sxs-lookup"><span data-stu-id="a8706-911">X</span></span> | <span data-ttu-id="a8706-912">X</span><span class="sxs-lookup"><span data-stu-id="a8706-912">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-913">FLAG DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-913">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="a8706-914">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-914">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-915">X</span><span class="sxs-lookup"><span data-stu-id="a8706-915">X</span></span> | <span data-ttu-id="a8706-916">X</span><span class="sxs-lookup"><span data-stu-id="a8706-916">X</span></span> | <span data-ttu-id="a8706-917">X</span><span class="sxs-lookup"><span data-stu-id="a8706-917">X</span></span> | \- |
| <span data-ttu-id="a8706-918">INFORMAZIONI DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-918">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="a8706-919">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="a8706-919">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="a8706-920">X</span><span class="sxs-lookup"><span data-stu-id="a8706-920">X</span></span> | <span data-ttu-id="a8706-921">X</span><span class="sxs-lookup"><span data-stu-id="a8706-921">X</span></span> | \- | <span data-ttu-id="a8706-922">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="a8706-922">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a8706-923">BITNESS \_ CHIAVE DI SICUREZZA \_ \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-923">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="a8706-924">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-924">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-925">X</span><span class="sxs-lookup"><span data-stu-id="a8706-925">X</span></span> | <span data-ttu-id="a8706-926">X</span><span class="sxs-lookup"><span data-stu-id="a8706-926">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-927">TIMEOUT INVIO OPZIONE WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8706-927">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="a8706-928">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-928">**DWORD**</span></span> | <span data-ttu-id="a8706-929">X</span><span class="sxs-lookup"><span data-stu-id="a8706-929">X</span></span> | <span data-ttu-id="a8706-930">X</span><span class="sxs-lookup"><span data-stu-id="a8706-930">X</span></span> | <span data-ttu-id="a8706-931">X</span><span class="sxs-lookup"><span data-stu-id="a8706-931">X</span></span> | <span data-ttu-id="a8706-932">X</span><span class="sxs-lookup"><span data-stu-id="a8706-932">X</span></span> | \- |
| <span data-ttu-id="a8706-933">OPZIONE WINHTTP \_ \_ SERVER \_ CBT</span><span class="sxs-lookup"><span data-stu-id="a8706-933">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="a8706-934">[**Associazioni SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="a8706-934">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="a8706-935">X</span><span class="sxs-lookup"><span data-stu-id="a8706-935">X</span></span> | <span data-ttu-id="a8706-936">X</span><span class="sxs-lookup"><span data-stu-id="a8706-936">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-937">CONTESTO DELLA \_ CATENA DI CERTIFICATI DEL SERVER \_ \_ \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-937">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="a8706-938">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a8706-938">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="a8706-939">X</span><span class="sxs-lookup"><span data-stu-id="a8706-939">X</span></span> | <span data-ttu-id="a8706-940">X</span><span class="sxs-lookup"><span data-stu-id="a8706-940">X</span></span> | \- | <span data-ttu-id="a8706-941">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="a8706-941">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a8706-942">CONTESTO DEL CERTIFICATO \_ \_ DEL SERVER \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-942">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="a8706-943">**CONTESTO DEL CERTIFICATO**</span><span class="sxs-lookup"><span data-stu-id="a8706-943">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="a8706-944">X</span><span class="sxs-lookup"><span data-stu-id="a8706-944">X</span></span> | <span data-ttu-id="a8706-945">X</span><span class="sxs-lookup"><span data-stu-id="a8706-945">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-946">NOME \_ \_ SPN DEL SERVER \_ DELL'OPZIONE WINHTTP \_ USATO</span><span class="sxs-lookup"><span data-stu-id="a8706-946">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="a8706-947">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-947">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-948">X</span><span class="sxs-lookup"><span data-stu-id="a8706-948">X</span></span> | <span data-ttu-id="a8706-949">X</span><span class="sxs-lookup"><span data-stu-id="a8706-949">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-950">NOME \_ \_ SPN DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-950">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="a8706-951">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-951">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-952">X</span><span class="sxs-lookup"><span data-stu-id="a8706-952">X</span></span> | \- | <span data-ttu-id="a8706-953">X</span><span class="sxs-lookup"><span data-stu-id="a8706-953">X</span></span> | \- |
| <span data-ttu-id="a8706-954">CODICE DI ERRORE \_ DEL \_ FLUSSO \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-954">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="a8706-955">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-955">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-956">X</span><span class="sxs-lookup"><span data-stu-id="a8706-956">X</span></span> | <span data-ttu-id="a8706-957">X</span><span class="sxs-lookup"><span data-stu-id="a8706-957">X</span></span> | \- | <span data-ttu-id="a8706-958">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="a8706-958">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a8706-959">OPZIONE WINHTTP \_ \_ TCP FAST \_ \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="a8706-959">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="a8706-960">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-960">**BOOL**</span></span> | <span data-ttu-id="a8706-961">X</span><span class="sxs-lookup"><span data-stu-id="a8706-961">X</span></span> | \- | \- | <span data-ttu-id="a8706-962">X</span><span class="sxs-lookup"><span data-stu-id="a8706-962">X</span></span> | <span data-ttu-id="a8706-963">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="a8706-963">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a8706-964">OPZIONE \_ \_ WINHTTP TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="a8706-964">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="a8706-965">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="a8706-965">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="a8706-966">X</span><span class="sxs-lookup"><span data-stu-id="a8706-966">X</span></span> | \- | \- | <span data-ttu-id="a8706-967">X</span><span class="sxs-lookup"><span data-stu-id="a8706-967">X</span></span> | <span data-ttu-id="a8706-968">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="a8706-968">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a8706-969">OPZIONE WINHTTP \_ \_ TLS FALSE \_ \_ START</span><span class="sxs-lookup"><span data-stu-id="a8706-969">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="a8706-970">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-970">**BOOL**</span></span> | <span data-ttu-id="a8706-971">X</span><span class="sxs-lookup"><span data-stu-id="a8706-971">X</span></span> | \- | \- | <span data-ttu-id="a8706-972">X</span><span class="sxs-lookup"><span data-stu-id="a8706-972">X</span></span> | <span data-ttu-id="a8706-973">Windows 10 versione 2004</span><span class="sxs-lookup"><span data-stu-id="a8706-973">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="a8706-974">OPZIONE WINHTTP \_ \_ \_ \_ FALLBACK NON SICURO DEL PROTOCOLLO TLS \_</span><span class="sxs-lookup"><span data-stu-id="a8706-974">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="a8706-975">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-975">**BOOL**</span></span> | <span data-ttu-id="a8706-976">X</span><span class="sxs-lookup"><span data-stu-id="a8706-976">X</span></span> | \- | \- | <span data-ttu-id="a8706-977">X</span><span class="sxs-lookup"><span data-stu-id="a8706-977">X</span></span> | <span data-ttu-id="a8706-978">Windows 10 versione 21H1</span><span class="sxs-lookup"><span data-stu-id="a8706-978">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="a8706-979">EVENTO NOTIFICA \_ \_ DI SCARICAMENTO \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-979">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="a8706-980">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="a8706-980">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="a8706-981">X</span><span class="sxs-lookup"><span data-stu-id="a8706-981">X</span></span> | \- | \- | <span data-ttu-id="a8706-982">X</span><span class="sxs-lookup"><span data-stu-id="a8706-982">X</span></span> | \- |
| <span data-ttu-id="a8706-983">ANALISI \_ \_ DELL'INTESTAZIONE NON SICURA \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-983">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="a8706-984">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-984">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-985">X</span><span class="sxs-lookup"><span data-stu-id="a8706-985">X</span></span> | \- | <span data-ttu-id="a8706-986">X</span><span class="sxs-lookup"><span data-stu-id="a8706-986">X</span></span> | \- |
| <span data-ttu-id="a8706-987">AGGIORNAMENTO \_ DELL'OPZIONE WINHTTP \_ AL WEB \_ \_ \_ SOCKET</span><span class="sxs-lookup"><span data-stu-id="a8706-987">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="a8706-988">N/D</span><span class="sxs-lookup"><span data-stu-id="a8706-988">N/A</span></span> | \- | <span data-ttu-id="a8706-989">X</span><span class="sxs-lookup"><span data-stu-id="a8706-989">X</span></span> | \- | <span data-ttu-id="a8706-990">X</span><span class="sxs-lookup"><span data-stu-id="a8706-990">X</span></span> | \- |
| <span data-ttu-id="a8706-991">URL DELL'OPZIONE WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8706-991">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="a8706-992">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-992">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-993">X</span><span class="sxs-lookup"><span data-stu-id="a8706-993">X</span></span> | <span data-ttu-id="a8706-994">X</span><span class="sxs-lookup"><span data-stu-id="a8706-994">X</span></span> | \- | \- |
| <span data-ttu-id="a8706-995">L'OPZIONE WINHTTP \_ USA LE CREDENZIALI GLOBALI DEL \_ \_ \_ \_ SERVER</span><span class="sxs-lookup"><span data-stu-id="a8706-995">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="a8706-996">**Bool**</span><span class="sxs-lookup"><span data-stu-id="a8706-996">**BOOL**</span></span> | <span data-ttu-id="a8706-997">X</span><span class="sxs-lookup"><span data-stu-id="a8706-997">X</span></span> | <span data-ttu-id="a8706-998">X</span><span class="sxs-lookup"><span data-stu-id="a8706-998">X</span></span> | \- | <span data-ttu-id="a8706-999">X</span><span class="sxs-lookup"><span data-stu-id="a8706-999">X</span></span> | \- |
| <span data-ttu-id="a8706-1000">OPZIONE WINHTTP \_ \_ AGENTE \_ UTENTE</span><span class="sxs-lookup"><span data-stu-id="a8706-1000">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="a8706-1001">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-1001">**LPWSTR**</span></span> | <span data-ttu-id="a8706-1002">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1002">X</span></span> | \- | <span data-ttu-id="a8706-1003">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1003">X</span></span> | <span data-ttu-id="a8706-1004">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1004">X</span></span> | \- |
| <span data-ttu-id="a8706-1005">NOME UTENTE \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-1005">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="a8706-1006">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8706-1006">**LPWSTR**</span></span> | \- | <span data-ttu-id="a8706-1007">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1007">X</span></span> | <span data-ttu-id="a8706-1008">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1008">X</span></span> | <span data-ttu-id="a8706-1009">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1009">X</span></span> | \- |
| <span data-ttu-id="a8706-1010">TIMEOUT DI \_ CHIUSURA DEL SOCKET WEB \_ \_ \_ DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-1010">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="a8706-1011">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-1011">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a8706-1012">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1012">X</span></span> | <span data-ttu-id="a8706-1013">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1013">X</span></span> | \- |
| <span data-ttu-id="a8706-1014">INTERVALLO \_ \_ \_ \_ KEEPALIVE DEL WEB SOCKET DELL'OPZIONE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-1014">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="a8706-1015">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-1015">**DWORD**</span></span> | \- | \- | <span data-ttu-id="a8706-1016">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1016">X</span></span> | <span data-ttu-id="a8706-1017">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1017">X</span></span> | \- |
| <span data-ttu-id="a8706-1018">DIMENSIONI DEL \_ BUFFER DI RICEZIONE WEB SOCKET \_ \_ \_ \_ DELL'OPZIONE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-1018">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a8706-1019">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-1019">**DWORD**</span></span> | <span data-ttu-id="a8706-1020">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1020">X</span></span> | <span data-ttu-id="a8706-1021">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1021">X</span></span> | <span data-ttu-id="a8706-1022">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1022">X</span></span> | <span data-ttu-id="a8706-1023">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1023">X</span></span> | <span data-ttu-id="a8706-1024">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a8706-1024">Windows 8.1</span></span> |
| <span data-ttu-id="a8706-1025">DIMENSIONI DEL \_ BUFFER DI INVIO DEL SOCKET WEB \_ \_ \_ \_ \_ DELL'OPZIONE WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-1025">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a8706-1026">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-1026">**DWORD**</span></span> | <span data-ttu-id="a8706-1027">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1027">X</span></span> | <span data-ttu-id="a8706-1028">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1028">X</span></span> | <span data-ttu-id="a8706-1029">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1029">X</span></span> | <span data-ttu-id="a8706-1030">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1030">X</span></span> | <span data-ttu-id="a8706-1031">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a8706-1031">Windows 8.1</span></span> |
| <span data-ttu-id="a8706-1032">CONTEGGIO THREAD \_ \_ DI LAVORO DELL'OPZIONE \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="a8706-1032">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="a8706-1033">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-1033">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="a8706-1034">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1034">X</span></span> | \- |
| <span data-ttu-id="a8706-1035">DIMENSIONI DEL \_ \_ BUFFER DI SCRITTURA DELL'OPZIONE \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-1035">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="a8706-1036">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a8706-1036">**DWORD**</span></span> | \- | <span data-ttu-id="a8706-1037">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1037">X</span></span> | <span data-ttu-id="a8706-1038">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1038">X</span></span> | <span data-ttu-id="a8706-1039">X</span><span class="sxs-lookup"><span data-stu-id="a8706-1039">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="a8706-1040">Per Windows XP e Windows 2000, vedere [Requisiti di run-time](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="a8706-1040">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8706-1041">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8706-1041">Requirements</span></span>

| <span data-ttu-id="a8706-1042">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8706-1042">Requirement</span></span> | <span data-ttu-id="a8706-1043">Valore</span><span class="sxs-lookup"><span data-stu-id="a8706-1043">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a8706-1044">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8706-1044">Minimum supported client</span></span> | <span data-ttu-id="a8706-1045">Windows XP, Windows 2000 Professional con solo app desktop SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8706-1045">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="a8706-1046">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8706-1046">Minimum supported server</span></span> | <span data-ttu-id="a8706-1047">Windows Server 2003, Windows 2000 Server con solo app desktop SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8706-1047">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="a8706-1048">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a8706-1048">Redistributable</span></span>          | <span data-ttu-id="a8706-1049">WinHTTP 5.0 e Internet Explorer 5.01 o versione successiva in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a8706-1049">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="a8706-1050">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8706-1050">Header</span></span>                   | <span data-ttu-id="a8706-1051">Winhttp.h</span><span class="sxs-lookup"><span data-stu-id="a8706-1051">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="a8706-1052">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8706-1052">See also</span></span>

[<span data-ttu-id="a8706-1053">Versioni di WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a8706-1053">WinHTTP Versions</span></span>](winhttp-versions.md)
