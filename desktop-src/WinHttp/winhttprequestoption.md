---
description: Include le opzioni che è possibile impostare o recuperare per la sessione corrente dei servizi HTTP di Microsoft Windows (WinHTTP).
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: Enumerazione WinHttpRequestOption
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: 32ae65f43cd04027027e43d29c49ed0f68f29c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526238"
---
# <a name="winhttprequestoption-enumeration"></a><span data-ttu-id="f3cde-103">Enumerazione WinHttpRequestOption</span><span class="sxs-lookup"><span data-stu-id="f3cde-103">WinHttpRequestOption enumeration</span></span>

<span data-ttu-id="f3cde-104">L'enumerazione **WinHttpRequestOption** include opzioni che è possibile impostare o recuperare per la sessione corrente dei servizi HTTP di Microsoft Windows (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="f3cde-104">The **WinHttpRequestOption** enumeration includes options that can be set or retrieved for the current Microsoft Windows HTTP Services (WinHTTP) session.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3cde-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3cde-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a><span data-ttu-id="f3cde-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="f3cde-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f3cde-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**\_UserAgentString WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption\_UserAgentString**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-108">Imposta o Recupera una **variante** che contiene la stringa dell' [*agente utente*](glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="f3cde-108">Sets or retrieves a **VARIANT** that contains the [*user agent*](glossary.md) string.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**\_URL WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-110">Recupera una **variante** che contiene l'URL della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f3cde-110">Retrieves a **VARIANT** that contains the URL of the resource.</span></span> <span data-ttu-id="f3cde-111">Questo valore è di sola lettura. non è possibile impostare l'URL utilizzando questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="f3cde-111">This value is read-only; you cannot set the URL using this property.</span></span> <span data-ttu-id="f3cde-112">L'URL non può essere letto finché non viene chiamato il metodo [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="f3cde-112">The URL cannot be read until the [**Open**](iwinhttprequest-open.md) method is called.</span></span> <span data-ttu-id="f3cde-113">Questa opzione è utile per controllare l'URL dopo il completamento del metodo [**Send**](iwinhttprequest-send.md) per verificare che sia stato eseguito il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="f3cde-113">This option is useful for checking the URL after the [**Send**](iwinhttprequest-send.md) method is finished to verify that any redirection occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**\_URLCodePage WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption\_URLCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-115">Imposta o recupera un **Variant** che identifica la [*tabella codici*](glossary.md) per la stringa dell'URL.</span><span class="sxs-lookup"><span data-stu-id="f3cde-115">Sets or retrieves a **VARIANT** that identifies the [*code page*](glossary.md) for the URL string.</span></span> <span data-ttu-id="f3cde-116">Il valore predefinito è la tabella codici UTF-8.</span><span class="sxs-lookup"><span data-stu-id="f3cde-116">The default value is the UTF-8 code page.</span></span> <span data-ttu-id="f3cde-117">La tabella codici viene utilizzata per convertire la stringa dell'URL Unicode, passata nel metodo [**Open**](iwinhttprequest-open.md) , a una rappresentazione di stringa a byte singolo.</span><span class="sxs-lookup"><span data-stu-id="f3cde-117">The code page is used to convert the Unicode URL string, passed in the [**Open**](iwinhttprequest-open.md) method, to a single-byte string representation.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**\_EscapePercentInURL WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption\_EscapePercentInURL**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-119">Imposta o recupera un valore **Variant** che indica se la percentuale di caratteri nella stringa dell'URL viene convertita in una sequenza di escape.</span><span class="sxs-lookup"><span data-stu-id="f3cde-119">Sets or retrieves a **VARIANT** that indicates whether percent characters in the URL string are converted to an escape sequence.</span></span> <span data-ttu-id="f3cde-120">Il valore predefinito di questa opzione è **Variant \_ true** che specifica tutti i caratteri unsafe American National Standards Institute (ANSI) ad eccezione del fatto che il simbolo di percentuale viene convertito in una sequenza di escape.</span><span class="sxs-lookup"><span data-stu-id="f3cde-120">The default value of this option is **VARIANT\_TRUE** which specifies all unsafe American National Standards Institute (ANSI) characters except the percent symbol are converted to an escape sequence.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**\_SslErrorIgnoreFlags WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption\_SslErrorIgnoreFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-122">Imposta o recupera un valore **Variant** che indica quali errori del certificato del server devono essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="f3cde-122">Sets or retrieves a **VARIANT** that indicates which server certificate errors should be ignored.</span></span> <span data-ttu-id="f3cde-123">Può trattarsi di una combinazione di uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3cde-123">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="f3cde-124">Errore</span><span class="sxs-lookup"><span data-stu-id="f3cde-124">Error</span></span>                                                  | <span data-ttu-id="f3cde-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f3cde-125">Value</span></span>  |
|--------------------------------------------------------|--------|
| <span data-ttu-id="f3cde-126">Autorità di certificazione (CA) o radice non attendibile sconosciuta</span><span class="sxs-lookup"><span data-stu-id="f3cde-126">Unknown certification authority (CA) or untrusted root</span></span> | <span data-ttu-id="f3cde-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="f3cde-127">0x0100</span></span> |
| <span data-ttu-id="f3cde-128">Utilizzo errato</span><span class="sxs-lookup"><span data-stu-id="f3cde-128">Wrong usage</span></span>                                            | <span data-ttu-id="f3cde-129">0x0200</span><span class="sxs-lookup"><span data-stu-id="f3cde-129">0x0200</span></span> |
| <span data-ttu-id="f3cde-130">Nome comune non valido (CN)</span><span class="sxs-lookup"><span data-stu-id="f3cde-130">Invalid common name (CN)</span></span>                               | <span data-ttu-id="f3cde-131">0x1000</span><span class="sxs-lookup"><span data-stu-id="f3cde-131">0x1000</span></span> |
| <span data-ttu-id="f3cde-132">La data o il certificato non è scaduto</span><span class="sxs-lookup"><span data-stu-id="f3cde-132">Invalid date or certificate expired</span></span>                    | <span data-ttu-id="f3cde-133">0x2000</span><span class="sxs-lookup"><span data-stu-id="f3cde-133">0x2000</span></span> |



 

<span data-ttu-id="f3cde-134">Il valore predefinito di questa opzione nella versione 5,1 di WinHTTP è zero e pertanto non viene ignorato alcun errore.</span><span class="sxs-lookup"><span data-stu-id="f3cde-134">The default value of this option in Version 5.1 of WinHTTP is zero, which results in no errors being ignored.</span></span> <span data-ttu-id="f3cde-135">Nelle versioni precedenti di WinHTTP, l'impostazione predefinita era 0x3300, pertanto tutti gli errori del certificato del server venivano ignorati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f3cde-135">In earlier versions of WinHTTP, the default setting was 0x3300, which resulted in all server certificate errors being ignored by default.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**\_SelectCertificate WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption\_SelectCertificate**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-137">Imposta un **Variant** che specifica il certificato client inviato a un server per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f3cde-137">Sets a **VARIANT** that specifies the client certificate that is sent to a server for authentication.</span></span> <span data-ttu-id="f3cde-138">Questa opzione indica il percorso, l' [*archivio certificati*](glossary.md)e l'oggetto di un certificato client delimitato da barre rovesciate.</span><span class="sxs-lookup"><span data-stu-id="f3cde-138">This option indicates the location, [*certificate store*](glossary.md), and subject of a client certificate delimited with backslashes.</span></span> <span data-ttu-id="f3cde-139">Per ulteriori informazioni sulla selezione di un certificato client, vedere [SSL in WinHTTP](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="f3cde-139">For more information about selecting a client certificate, see [SSL in WinHTTP](ssl-in-winhttp.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**\_EnableRedirects WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption\_EnableRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-141">Imposta o recupera un valore **Variant** che indica se le richieste vengono reindirizzate automaticamente quando il server specifica un nuovo percorso per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f3cde-141">Sets or retrieves a **VARIANT** that indicates whether requests are automatically redirected when the server specifies a new location for the resource.</span></span> <span data-ttu-id="f3cde-142">Il valore predefinito di questa opzione è **Variant \_ true** per indicare che le richieste vengono reindirizzate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f3cde-142">The default value of this option is **VARIANT\_TRUE** to indicate that requests are automatically redirected.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**\_UrlEscapeDisable WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption\_UrlEscapeDisable**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-144">Imposta o recupera un valore **Variant** che indica se i caratteri unsafe nel percorso e i componenti della query di un URL vengono convertiti in sequenze di escape.</span><span class="sxs-lookup"><span data-stu-id="f3cde-144">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the path and query components of a URL are converted to escape sequences.</span></span> <span data-ttu-id="f3cde-145">Il valore predefinito di questa opzione è **Variant \_ true**, che specifica che i caratteri nel percorso e nella query vengono convertiti.</span><span class="sxs-lookup"><span data-stu-id="f3cde-145">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the path and query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**\_UrlEscapeDisableQuery WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption\_UrlEscapeDisableQuery**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-147">Imposta o recupera un valore **Variant** che indica se i caratteri unsafe nel componente di query dell'URL vengono convertiti in sequenze di escape.</span><span class="sxs-lookup"><span data-stu-id="f3cde-147">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the query component of the URL are converted to escape sequences.</span></span> <span data-ttu-id="f3cde-148">Il valore predefinito di questa opzione è **Variant \_ true**, che specifica che i caratteri nella query vengono convertiti.</span><span class="sxs-lookup"><span data-stu-id="f3cde-148">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**\_SecureProtocols WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption\_SecureProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-150">Imposta o recupera un **Variant** che indica i protocolli protetti che è possibile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f3cde-150">Sets or retrieves a **VARIANT** that indicates which secure protocols can be used.</span></span> <span data-ttu-id="f3cde-151">Questa opzione consente di selezionare i protocolli accettabili per il client.</span><span class="sxs-lookup"><span data-stu-id="f3cde-151">This option selects the protocols acceptable to the client.</span></span> <span data-ttu-id="f3cde-152">Il protocollo viene negoziato durante l'handshake di Secure Sockets Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="f3cde-152">The protocol is negotiated during the Secure Sockets Layer (SSL) handshake.</span></span> <span data-ttu-id="f3cde-153">Può trattarsi di una combinazione di uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3cde-153">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="f3cde-154">Protocollo</span><span class="sxs-lookup"><span data-stu-id="f3cde-154">Protocol</span></span>                           | <span data-ttu-id="f3cde-155">Valore</span><span class="sxs-lookup"><span data-stu-id="f3cde-155">Value</span></span>  |
|------------------------------------|--------|
| <span data-ttu-id="f3cde-156">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="f3cde-156">SSL 2.0</span></span>                            | <span data-ttu-id="f3cde-157">0x0008</span><span class="sxs-lookup"><span data-stu-id="f3cde-157">0x0008</span></span> |
| <span data-ttu-id="f3cde-158">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="f3cde-158">SSL 3.0</span></span>                            | <span data-ttu-id="f3cde-159">0x0020</span><span class="sxs-lookup"><span data-stu-id="f3cde-159">0x0020</span></span> |
| <span data-ttu-id="f3cde-160">Transport Layer Security (TLS) 1,0</span><span class="sxs-lookup"><span data-stu-id="f3cde-160">Transport Layer Security (TLS) 1.0</span></span> | <span data-ttu-id="f3cde-161">0x0080</span><span class="sxs-lookup"><span data-stu-id="f3cde-161">0x0080</span></span> |



 

<span data-ttu-id="f3cde-162">Il valore predefinito di questa opzione è 0x0028, che indica che è possibile utilizzare SSL 2,0 o SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="f3cde-162">The default value of this option is 0x0028, which indicates that SSL 2.0 or SSL 3.0 can be used.</span></span> <span data-ttu-id="f3cde-163">Se questa opzione è impostata su zero, il client e il server non sono in grado di determinare un protocollo di sicurezza accettabile e l' [**invio**](iwinhttprequest-send.md) successivo genera un errore.</span><span class="sxs-lookup"><span data-stu-id="f3cde-163">If this option is set to zero, the client and server are not able to determine an acceptable security protocol and the next [**Send**](iwinhttprequest-send.md) results in an error.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**\_EnableTracing WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption\_EnableTracing**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-165">Imposta o recupera un valore **Variant** che indica se la traccia è attualmente abilitata.</span><span class="sxs-lookup"><span data-stu-id="f3cde-165">Sets or retrieves a **VARIANT** that indicates whether tracing is currently enabled.</span></span> <span data-ttu-id="f3cde-166">Per ulteriori informazioni sulla funzionalità di traccia in servizi HTTP di Microsoft Windows (WinHTTP), vedere la pagina relativa alla [funzionalità di traccia WinHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="f3cde-166">For more information about the trace facility in Microsoft Windows HTTP Services (WinHTTP), see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**\_RevertImpersonationOverSsl WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption\_RevertImpersonationOverSsl**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-168">Controlla se l'oggetto [**WinHttpRequest**](winhttprequest.md) Annulla temporaneamente la rappresentazione client per la durata delle operazioni di autenticazione del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="f3cde-168">Controls whether the [**WinHttpRequest**](winhttprequest.md) object temporarily reverts client impersonation for the duration of the SSL certificate authentication operations.</span></span> <span data-ttu-id="f3cde-169">L'impostazione predefinita per l'oggetto **WinHttpRequest** è **true**.</span><span class="sxs-lookup"><span data-stu-id="f3cde-169">The default setting for the **WinHttpRequest** object is **TRUE**.</span></span> <span data-ttu-id="f3cde-170">Impostare questa opzione su **false** per evitare la rappresentazione durante l'esecuzione delle operazioni di autenticazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="f3cde-170">Set this option to **FALSE** to keep impersonation while performing certificate authentication operations.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**\_EnableHttpsToHttpRedirects WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption\_EnableHttpsToHttpRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-172">Controlla se WinHTTP consente i reindirizzamenti.</span><span class="sxs-lookup"><span data-stu-id="f3cde-172">Controls whether or not WinHTTP allows redirects.</span></span> <span data-ttu-id="f3cde-173">Per impostazione predefinita, tutti i reindirizzamenti vengono seguiti automaticamente, ad eccezione di quelli che trasferiscono da un URL protetto (HTTPS) a un URL non protetto (http).</span><span class="sxs-lookup"><span data-stu-id="f3cde-173">By default, all redirects are automatically followed, except those that transfer from a secure (https) URL to an non-secure (http) URL.</span></span> <span data-ttu-id="f3cde-174">Impostare questa opzione su **true** per abilitare i reindirizzamenti HTTPS ai reindirizzamenti HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3cde-174">Set this option to **TRUE** to enable HTTPS to HTTP redirects.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**\_EnablePassportAuthentication WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption\_EnablePassportAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-176">Abilita o Disabilita il supporto per l'autenticazione Passport.</span><span class="sxs-lookup"><span data-stu-id="f3cde-176">Enables or disables support for Passport authentication.</span></span> <span data-ttu-id="f3cde-177">Per impostazione predefinita, il supporto automatico per l'autenticazione Passport è disabilitato; impostare questa opzione su **true** per abilitare il supporto per l'autenticazione Passport.</span><span class="sxs-lookup"><span data-stu-id="f3cde-177">By default, automatic support for Passport authentication is disabled; set this option to **TRUE** to enable Passport authentication support.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**\_MaxAutomaticRedirects WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption\_MaxAutomaticRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-179">Imposta o Recupera il numero massimo di reindirizzamenti che WinHTTP segue; il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="f3cde-179">Sets or retrieves the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="f3cde-180">Questo limite impedisce ai siti non autorizzati di rendere il client WinHTTP bloccato in seguito a un numero elevato di reindirizzamenti.</span><span class="sxs-lookup"><span data-stu-id="f3cde-180">This limit prevents unauthorized sites from making the WinHTTP client stall following a large number of redirects.</span></span>

<span data-ttu-id="f3cde-181">**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3cde-181">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**\_MaxResponseHeaderSize WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption\_MaxResponseHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-183">Imposta o recupera un set associato sulla dimensione massima della parte di intestazione della risposta del server.</span><span class="sxs-lookup"><span data-stu-id="f3cde-183">Sets or retrieves a bound set on the maximum size of the header portion of the server's response.</span></span> <span data-ttu-id="f3cde-184">Questo limite protegge il client da un server dannoso che tenta di bloccare il client inviando una risposta con una quantità infinita di dati di intestazione.</span><span class="sxs-lookup"><span data-stu-id="f3cde-184">This bound protects the client from a malicious server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="f3cde-185">Il valore predefinito è 64 KB.</span><span class="sxs-lookup"><span data-stu-id="f3cde-185">The default value is 64 KB.</span></span>

<span data-ttu-id="f3cde-186">**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3cde-186">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**\_MaxResponseDrainSize WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption\_MaxResponseDrainSize**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-188">Imposta o recupera un limite sulla quantità di dati che verranno svuotati dalle risposte per riutilizzare una connessione.</span><span class="sxs-lookup"><span data-stu-id="f3cde-188">Sets or retrieves a bound on the amount of data that will be drained from responses in order to reuse a connection.</span></span> <span data-ttu-id="f3cde-189">Il valore predefinito è 1 MB.</span><span class="sxs-lookup"><span data-stu-id="f3cde-189">The default is 1 MB.</span></span>

<span data-ttu-id="f3cde-190">**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3cde-190">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f3cde-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption\_EnableHttp1\_1**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-192">Imposta o recupera un valore booleano che indica se è necessario utilizzare HTTP/1.1 o HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="f3cde-192">Sets or retrieves a boolean value that indicates whether HTTP/1.1 or HTTP/1.0 should be used.</span></span> <span data-ttu-id="f3cde-193">Il valore predefinito è **true**, in modo che http/1.1 venga usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f3cde-193">The default is **TRUE**, so that HTTP/1.1 is used by default.</span></span>

<span data-ttu-id="f3cde-194">**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3cde-194">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f3cde-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**\_EnableCertificateRevocationCheck WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="f3cde-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption\_EnableCertificateRevocationCheck**</span></span>
</dt> <dd>

<span data-ttu-id="f3cde-196">Abilita il controllo delle revoche di certificati del server durante la negoziazione SSL.</span><span class="sxs-lookup"><span data-stu-id="f3cde-196">Enables server certificate revocation checking during SSL negotiation.</span></span> <span data-ttu-id="f3cde-197">Quando il server presenta un certificato, viene eseguito un controllo per determinare se il certificato è stato revocato dall'emittente.</span><span class="sxs-lookup"><span data-stu-id="f3cde-197">When the server presents a certificate, a check is performed to determine whether the certificate has been revoked by its issuer.</span></span> <span data-ttu-id="f3cde-198">Se il certificato è stato effettivamente revocato oppure il controllo della revoca non riesce perché non è possibile scaricare l'elenco di revoche di certificati (CRL), la richiesta ha esito negativo. questi errori di revoca non possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="f3cde-198">If the certificate is indeed revoked, or the revocation check fails because the Certificate Revocation List (CRL) cannot be downloaded, the request fails; such revocation errors cannot be suppressed.</span></span>

<span data-ttu-id="f3cde-199">**Windows XP con SP1 e windows 2000 con SP3:** Questo valore di enumerazione non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3cde-199">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3cde-200">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3cde-200">Remarks</span></span>

<span data-ttu-id="f3cde-201">Impostare un'opzione specificando una delle costanti precedenti come parametro della proprietà [**Option**](iwinhttprequest-option.md) .</span><span class="sxs-lookup"><span data-stu-id="f3cde-201">Set an option by specifying one of the preceding constants as the parameter of the [**Option**](iwinhttprequest-option.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="f3cde-202">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f3cde-202">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3cde-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3cde-203">Requirements</span></span>



| <span data-ttu-id="f3cde-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3cde-204">Requirement</span></span> | <span data-ttu-id="f3cde-205">Valore</span><span class="sxs-lookup"><span data-stu-id="f3cde-205">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3cde-206">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3cde-206">Minimum supported client</span></span><br/> | <span data-ttu-id="f3cde-207">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="f3cde-207">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="f3cde-208">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3cde-208">Minimum supported server</span></span><br/> | <span data-ttu-id="f3cde-209">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="f3cde-209">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="f3cde-210">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f3cde-210">Redistributable</span></span><br/>          | <span data-ttu-id="f3cde-211">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f3cde-211">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="f3cde-212">IDL</span><span class="sxs-lookup"><span data-stu-id="f3cde-212">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3cde-213"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3cde-213"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3cde-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3cde-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3cde-215">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f3cde-215">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




