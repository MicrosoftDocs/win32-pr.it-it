---
title: Mapping dei metadati
description: Il contenuto di un documento di metadati viene mappato all'API dei metadati nei modi descritti nelle sezioni seguenti.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Mapping dei metadati per i servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9da067768569e78ba6bb98ee219e11917d3201
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300704"
---
# <a name="metadata-mapping"></a><span data-ttu-id="92d64-106">Mapping dei metadati</span><span class="sxs-lookup"><span data-stu-id="92d64-106">Metadata Mapping</span></span>

<span data-ttu-id="92d64-107">Il contenuto di un documento di metadati viene mappato all'API dei metadati nei modi descritti nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="92d64-107">The contents of a metadata document map to the metadata API in the ways explained in the following sections.</span></span>


<span data-ttu-id="92d64-108">In questa documentazione vengono usati i prefissi degli spazi dei nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-108">The following namespace prefixes are used throughout this documentation:</span></span>

``` syntax
wsdl   => http://schemas.xmlsoap.org/wsdl/
soap11 => http://schemas.xmlsoap.org/wsdl/soap/
soap12 => http://schemas.xmlsoap.org/wsdl/soap12/
wsa09  => http://schemas.xmlsoap.org/ws/2004/08/addressing
wsa10  => http://www.w3.org/2005/08/addressing
wsa09p => http://schemas.xmlsoap.org/ws/2004/08/addressing/policy
wsa10p => http://www.w3.org/2006/05/addressing/wsdl
binp   => http://schemas.microsoft.com/ws/06/2004/mspolicy/netbinary1
mtomp  => http://schemas.xmlsoap.org/ws/2004/09/policy/optimizedmimeserialization
sp     => http://schemas.xmlsoap.org/ws/2005/07/securitypolicy
wsp    => http://schemas.xmlsoap.org/ws/2004/09/policy
netf   => http://schemas.microsoft.com/ws/2006/05/framing/policy
httpp  => http://schemas.microsoft.com/ws/06/2004/policy/http
wst10  => http://schemas.xmlsoap.org/ws/2005/02/trust
wsi    => http://schemas.xmlsoap.org/ws/2005/05/identity
```

<span data-ttu-id="92d64-109">Nelle sezioni successive vengono descritti i costrutti delle API insieme ai costrutti di metadati (WSDL o Policy) a cui corrispondono.</span><span class="sxs-lookup"><span data-stu-id="92d64-109">The subsequent sections describe API constructs along with what metadata constructs (WSDL or Policy) they correspond to.</span></span>

<span data-ttu-id="92d64-110">Una certa familiarità con le specifiche dei metadati, come WSDL e Policy, aiuterà a comprendere questa sezione.</span><span class="sxs-lookup"><span data-stu-id="92d64-110">Familiarity with metadata specifications such as WSDL and Policy will aid in understanding this section.</span></span>

## <a name="endpoint-address"></a><span data-ttu-id="92d64-111">Indirizzo endpoint</span><span class="sxs-lookup"><span data-stu-id="92d64-111">Endpoint address</span></span>

<span data-ttu-id="92d64-112">L'indirizzo di un endpoint (vedere [**WS \_ endpoint \_ Address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) viene ottenuto da un elemento extensibility nell'elemento WSDL: Port del documento WSDL.</span><span class="sxs-lookup"><span data-stu-id="92d64-112">The address of an endpoint (see [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) is obtained from an extensibility element within the wsdl:port element of the WSDL document.</span></span> <span data-ttu-id="92d64-113">Per specificare l'indirizzo sono supportati gli elementi di estensibilità seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-113">The following extensibility elements are supported for specifying the address:</span></span>

``` syntax
<wsdl:port...>
    <soap11:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <soap12:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa09:EndpointReference.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa10:EndpointReference.../>
</wsdl:port>
```

## <a name="ws_channel_binding"></a><span data-ttu-id="92d64-114">\_binding di canale WS \_</span><span class="sxs-lookup"><span data-stu-id="92d64-114">WS\_CHANNEL\_BINDING</span></span>

<span data-ttu-id="92d64-115">L'associazione di canale (vedere [**WS \_ Channel \_ Binding**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) è determinata dal trasporto utilizzato dall'associazione SOAP, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="92d64-115">The channel binding (see [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) is determined by the transport the soap binding used, as follows:</span></span>

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a><span data-ttu-id="92d64-116">\_ \_ versione busta della proprietà del canale WS \_ \_</span><span class="sxs-lookup"><span data-stu-id="92d64-116">WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION</span></span>

<span data-ttu-id="92d64-117">La versione della busta ( [**vedere \_ \_ versione della \_ busta \_ della proprietà del canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) è determinata dall'associazione SOAP utilizzata, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="92d64-117">The envelope version (see [**WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by which soap binding is used, as follows:</span></span>

``` syntax
<wsdl:binding...>
    <soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

``` syntax
<wsdl:binding...>
    <soap12:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_2
</wsdl:binding>
```

## <a name="addressing-version"></a><span data-ttu-id="92d64-118">Versione Addressing</span><span class="sxs-lookup"><span data-stu-id="92d64-118">Addressing Version</span></span>

<span data-ttu-id="92d64-119">La versione di indirizzamento (vedere la pagina relativa alla [**\_ \_ \_ \_ versione di indirizzamento delle proprietà del canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) è determinata dalle asserzioni seguenti nei criteri dell'endpoint:</span><span class="sxs-lookup"><span data-stu-id="92d64-119">The addressing version (see [**WS\_CHANNEL\_PROPERTY\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <wsa09p:UsingAddressing.../> => WS_ADDRESSING_VERSION_0_9
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <wsa10p:UsingAddressing.../> => WS_ADDRESSING_VERSION_1_0
</wsp:Policy>
```

<span data-ttu-id="92d64-120">Se non è presente un'asserzione di indirizzamento, viene presupposto il [**trasporto della versione di WS \_ Addressing \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .</span><span class="sxs-lookup"><span data-stu-id="92d64-120">If an addressing assertion is not present, then [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) is assumed.</span></span>

## <a name="message-encoding"></a><span data-ttu-id="92d64-121">Codifica dei messaggi</span><span class="sxs-lookup"><span data-stu-id="92d64-121">Message Encoding</span></span>

<span data-ttu-id="92d64-122">La codifica del messaggio (vedere la [**\_ codifica della \_ proprietà \_ WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) è determinata dalle asserzioni seguenti nei criteri dell'endpoint:</span><span class="sxs-lookup"><span data-stu-id="92d64-122">The encoding of the message (see [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

<span data-ttu-id="92d64-123">Si noti che l'asserzione di criteri di codifica binaria non include informazioni sul fatto che la codifica binaria sia con sessione o senza sessione.</span><span class="sxs-lookup"><span data-stu-id="92d64-123">Note that the binary encoding policy assertion does not include information about whether the binary encoding is sessionful or sessionless.</span></span> <span data-ttu-id="92d64-124">Questa condizione è determinata dal vincolo della proprietà di codifica (che deve essere appropriato a seconda che il [**\_ \_ tipo di canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) utilizzato sia o meno sessione).</span><span class="sxs-lookup"><span data-stu-id="92d64-124">This is determined by the encoding property constraint (which should be appropriate according to whether or not the [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) being used is sessionful or not).</span></span>

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

<span data-ttu-id="92d64-125">Se nessuna delle asserzioni precedenti è presente, viene utilizzata una codifica del testo: [**WS Encoding \_ \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ Encoding \_ XML \_ UTF16LE**, **WS \_ Encoding \_ XML \_ UTF16BE**.</span><span class="sxs-lookup"><span data-stu-id="92d64-125">If neither of the above assertions are present, then a text encoding is used: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS\_ENCODING\_XML\_UTF16LE**, **WS\_ENCODING\_XML\_UTF16BE**.</span></span>

<span data-ttu-id="92d64-126">Si noti che i criteri non includono informazioni sul set di caratteri per MTOM o codifiche di testo (indipendentemente dal fatto che sia UTF8, UTF16LE o UTF16BE).</span><span class="sxs-lookup"><span data-stu-id="92d64-126">Note that policy does not include information about the character set for MTOM or text encodings (whether it is UTF8, UTF16LE or UTF16BE).</span></span> <span data-ttu-id="92d64-127">Il valore effettivo del set di caratteri utilizzato è determinato dal vincolo della proprietà Encoding.</span><span class="sxs-lookup"><span data-stu-id="92d64-127">The actual character set value used is determined by the encoding property constraint.</span></span>

## <a name="constraints-with-http-header-authentication"></a><span data-ttu-id="92d64-128">Vincoli con autenticazione dell'intestazione HTTP</span><span class="sxs-lookup"><span data-stu-id="92d64-128">Constraints with HTTP Header Authentication</span></span>

<span data-ttu-id="92d64-129">Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza per l' [**\_ autenticazione dell' \_ intestazione \_ \_ \_ \_ WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="92d64-129">This section applies when the [**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) security binding constraint is specified.</span></span>

<span data-ttu-id="92d64-130">Questa associazione di sicurezza è indicata nei criteri da diverse asserzioni che specificano l'autenticazione dell'intestazione HTTP e che deve essere utilizzato un particolare schema di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="92d64-130">This security binding is indicated in the policy by different assertions that states both that HTTP header authentication should be used, and that a particular authentication scheme should be used.</span></span> <span data-ttu-id="92d64-131">Le asserzioni di criteri corrispondono ai valori dello [**schema di \_ \_ autenticazione dell' \_ \_ \_ intestazione \_ \_ http della proprietà di associazione di sicurezza WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="92d64-131">The policy assertions correspond to the values of the [**WS\_SECURITY\_BINDING\_PROPERTY\_HTTP\_HEADER\_AUTH\_SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) as follows:</span></span>

``` syntax
<wsp:Policy...>
    <httpp:BasicAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_BASIC
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NegotiateAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NtlmAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NTLM
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:DigestAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_DIGEST
</wsp:Policy>
```

## <a name="constraints-with-sll-transport-security"></a><span data-ttu-id="92d64-132">Vincoli con la sicurezza del trasporto SLL</span><span class="sxs-lookup"><span data-stu-id="92d64-132">Constraints with SLL Transport Security</span></span>

<span data-ttu-id="92d64-133">Questa sezione si applica quando viene specificato il vincolo di binding di sicurezza del [**trasporto di WS \_ SSL \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="92d64-133">This section applies when the [**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="92d64-134">In questo caso vengono usate le asserzioni di criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-134">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <sp:HttpsToken.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constraints-with-sspi-transport-security"></a><span data-ttu-id="92d64-135">Vincoli con la sicurezza del trasporto SSPI</span><span class="sxs-lookup"><span data-stu-id="92d64-135">Constraints with SSPI Transport Security</span></span>

<span data-ttu-id="92d64-136">Questa sezione si applica quando si specifica il vincolo di binding di sicurezza del [**\_ \_ \_ \_ \_ \_ trasporto SSPI di WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="92d64-136">This section applies when the [**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="92d64-137">In questo caso vengono usate le asserzioni di criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-137">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <netf:WindowsTransportSecurity.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constrains-with-transport-security"></a><span data-ttu-id="92d64-138">Vincoli con la sicurezza del trasporto</span><span class="sxs-lookup"><span data-stu-id="92d64-138">Constrains with Transport Security</span></span>

<span data-ttu-id="92d64-139">È possibile specificare il vincolo della proprietà [**livello di protezione del trasporto delle \_ proprietà di sicurezza \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) se è stato specificato uno dei vincoli di associazione di sicurezza:</span><span class="sxs-lookup"><span data-stu-id="92d64-139">The [**WS\_SECURITY\_PROPERTY\_TRANSPORT\_PROTECTION\_LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) property constraint can be specified if any of the security binding constraints are specified:</span></span>

-   [<span data-ttu-id="92d64-140">**\_vincolo di \_ binding di sicurezza del trasporto \_ \_ di WS SSL \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-140">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    <span data-ttu-id="92d64-141">Il valore da policy è sempre [**il \_ segno di livello di protezione WS e la \_ \_ \_ \_ crittografia**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="92d64-141">The value from policy is always [**WS\_PROTECTION\_LEVEL\_SIGN\_AND\_ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

-   [<span data-ttu-id="92d64-142">**\_vincolo di \_ \_ binding di sicurezza del trasporto SSPI \_ \_ di WS TCP \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-142">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    <span data-ttu-id="92d64-143">Il valore dei criteri viene specificato come parte dell'asserzione WindowsTransportSecurity, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="92d64-143">The value from policy is specified as part of the WindowsTransportSecurity assertion, as follows:</span></span>

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [<span data-ttu-id="92d64-144">**\_vincolo di \_ \_ binding di \_ sicurezza \_ \_ per l'autenticazione dell'intestazione WS http**</span><span class="sxs-lookup"><span data-stu-id="92d64-144">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    <span data-ttu-id="92d64-145">Il valore dei criteri è sempre [**il \_ livello di protezione WS \_ \_ None**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="92d64-145">The value from policy is always [**WS\_PROTECTION\_LEVEL\_NONE**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

## <a name="constraints-with-kerberos-apreq-security-binding"></a><span data-ttu-id="92d64-146">Vincoli con l'associazione di sicurezza APREQ Kerberos</span><span class="sxs-lookup"><span data-stu-id="92d64-146">Constraints with Kerberos APREQ Security Binding</span></span>

<span data-ttu-id="92d64-147">Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza del [**\_ messaggio WS Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="92d64-147">This section applies when the [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="92d64-148">In questo caso vengono usate le asserzioni di criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-148">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a><span data-ttu-id="92d64-149">Vincoli con associazione di sicurezza dei messaggi</span><span class="sxs-lookup"><span data-stu-id="92d64-149">Constraints with Message Security Binding</span></span>

<span data-ttu-id="92d64-150">Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza del vincolo di sicurezza del [**\_ \_ messaggio \_ \_ \_ WS nomeutente**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="92d64-150">This section applies when the [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="92d64-151">In questo caso vengono usate le asserzioni di criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-151">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a><span data-ttu-id="92d64-152">\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="92d64-152">WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="92d64-153">Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza del [**\_ \_ \_ \_ \_ vincolo di sicurezza del messaggio WS CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="92d64-153">This section applies when the [**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="92d64-154">In questo caso vengono usate le asserzioni di criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-154">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a><span data-ttu-id="92d64-155">\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_</span><span class="sxs-lookup"><span data-stu-id="92d64-155">WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="92d64-156">Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza per il vincolo di sicurezza dei [**\_ \_ \_ messaggi del \_ \_ \_ token WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="92d64-156">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="92d64-157">In questo caso vengono usate le asserzioni di criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-157">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:IssuedToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:RequestSecurityTokenTemplate TrustVersion='xs:anyURI&quot;?>
                ...
                <wst10:Claims>
                    <wsi:ClaimType Optional='xs:boolean'?>xs:anyURI<wt:ClaimType>*
                </wst10:Claims>
                ...
            </wsp:RequestSecurityTokenTemplate>
            <wsp:Policy>
                <sp:RequireDerivedKeys/> ?
                <sp:RequireExternalReference/> ?
                <sp:RequireInternalReference/> ?
            </wsp:Policy> ?
        </sp:IssuedToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="92d64-158">Di seguito viene descritto il mapping dei campi del [**\_ vincolo di \_ \_ associazione di \_ sicurezza \_ \_ dei messaggi del token WS rilasciato**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) ai criteri sopra indicati:</span><span class="sxs-lookup"><span data-stu-id="92d64-158">The following describes the mapping of fields of the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) to the above policy:</span></span>

-   <span data-ttu-id="92d64-159">Il campo claimConstraints viene usato per verificare il set di URI del tipo di attestazione che vengono visualizzati all'interno dell'elemento WSI: ClaimType precedente.</span><span class="sxs-lookup"><span data-stu-id="92d64-159">The claimConstraints field is used to verify the set of claim type URIs that appear within the wsi:ClaimType element above.</span></span>

-   <span data-ttu-id="92d64-160">Il campo issuerAddress corrisponde all'elemento wsp: Issuer precedente, che è l' [**indirizzo dell' \_ endpoint \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) del servizio che può emettere il token.</span><span class="sxs-lookup"><span data-stu-id="92d64-160">The issuerAddress field corresponds to the wsp:Issuer element above, which is the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) of the service that can issue the token.</span></span>

-   <span data-ttu-id="92d64-161">Il campo requestSecurityTokenTemplate corrisponde agli elementi figlio dell'elemento wsp: RequestSecurityTokenTemplate.</span><span class="sxs-lookup"><span data-stu-id="92d64-161">The requestSecurityTokenTemplate field corresponds to the child elements of the wsp:RequestSecurityTokenTemplate element.</span></span>

## <a name="ws_security_context_message_security_binding_constraint"></a><span data-ttu-id="92d64-162">\_vincolo di \_ \_ associazione di sicurezza del messaggio del contesto \_ di \_ sicurezza WS \_</span><span class="sxs-lookup"><span data-stu-id="92d64-162">WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="92d64-163">Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza del [**\_ \_ \_ messaggio del \_ \_ \_ contesto**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) di sicurezza WS.</span><span class="sxs-lookup"><span data-stu-id="92d64-163">This section applies when the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="92d64-164">In questo caso vengono usate le asserzioni di criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-164">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:SecureConversationToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:Policy>
                <sp:RequireDerivedKeys.../>?
                <sp:RequireExternalUriReference.../>?
                <sp:SC10SecurityContextToken.../>? => WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005
                <sp:BootstrapPolicy... >?
                   <wsp:Policy> ...  </wsp:Policy> => WS_SECURITY_CONSTRAINTS
                </sp:BootstrapPolicy>
            </wsp:Policy>
        </wsp:SecureConversationToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="92d64-165">La modalità entropia è determinata dall'asserzione di> <SP: Trust10.</span><span class="sxs-lookup"><span data-stu-id="92d64-165">The entropy mode is determined by the <sp:Trust10> assertion.</span></span> <span data-ttu-id="92d64-166"><SP: RequireClientEntropy/> e <SP: RequireServerEntropy/> => [**ws \_ \_ modalità entropia della chiave di sicurezza \_ \_ \_ combinata**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: RequireClientEntropy/> => **ws \_ sicurezza \_ chiave \_ entropia in \_ modalità \_ \_ solo client** <SP: RequireServerEntropy/> => **WS \_ sicurezza \_ chiave \_ entropia \_ modalità \_ \_ solo server**</span><span class="sxs-lookup"><span data-stu-id="92d64-166"><sp:RequireClientEntropy/> and <sp:RequireServerEntropy/> => [**WS\_SECURITY\_KEY\_ENTROPY\_MODE\_COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_CLIENT\_ONLY** <sp:RequireServerEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_SERVER\_ONLY**</span></span>

## <a name="ws_request_security_token_property_trust_version"></a><span data-ttu-id="92d64-167">\_versione del \_ \_ trust della proprietà del token di sicurezza \_ WS \_ Request \_</span><span class="sxs-lookup"><span data-stu-id="92d64-167">WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION</span></span>

<span data-ttu-id="92d64-168">Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza per il vincolo di sicurezza dei [**\_ \_ \_ messaggi del \_ \_ \_ token WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .</span><span class="sxs-lookup"><span data-stu-id="92d64-168">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="92d64-169">Le asserzioni di criteri seguenti vengono utilizzate per identificare [**la \_ \_ versione di WS Trust**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) e le opzioni associate.</span><span class="sxs-lookup"><span data-stu-id="92d64-169">The following policy assertions are used to identify the [**WS\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) and associated options.</span></span>

``` syntax
<sp:Trust10> => WS_TRUST_VERSION_FEBRUARY_2005
    <sp:Policy>
        <sp:MustSupportClientChallenge/> ?
        <sp:MustSupportServerChallenge/> ?
        <sp:RequireClientEntropy/> ?
        <sp:RequireServerEntropy/> ?
        <sp:MustSupportIssuedTokens/> ?
    </sp:Policy>
</sp:Trust10>
```

<span data-ttu-id="92d64-170">È possibile specificare la versione del trust utilizzando [**il \_ \_ vincolo della \_ \_ proprietà del \_ token di sicurezza WS request**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) con un ID di proprietà della [**\_ \_ \_ \_ \_ \_ versione di trust della proprietà del token di sicurezza WS request**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span><span class="sxs-lookup"><span data-stu-id="92d64-170">The trust version can be specified using the [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) with a property id of [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span></span>

## <a name="ws_security_property_security_header_version"></a><span data-ttu-id="92d64-171">\_versione dell' \_ intestazione di sicurezza della proprietà WS Security \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="92d64-171">WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION</span></span>

<span data-ttu-id="92d64-172">Questa sezione si applica quando viene utilizzato uno dei seguenti vincoli di binding:</span><span class="sxs-lookup"><span data-stu-id="92d64-172">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="92d64-173">**\_vincolo di \_ \_ binding di \_ sicurezza del messaggio \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="92d64-173">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="92d64-174">**\_vincolo di \_ binding di sicurezza del messaggio WS nomeutente \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-174">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="92d64-175">**\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-175">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="92d64-176">**\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-176">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="92d64-177">La versione di sicurezza dell'intestazione (come specificato dalla [**versione dell'intestazione di \_ sicurezza della \_ proprietà \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) è determinata da una delle asserzioni di criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-177">The header security version (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a><span data-ttu-id="92d64-178">Vincoli con layout di sicurezza dell'intestazione</span><span class="sxs-lookup"><span data-stu-id="92d64-178">Constraints with Header Security Layout</span></span>

<span data-ttu-id="92d64-179">Questa sezione si applica quando viene utilizzato uno dei seguenti vincoli di binding:</span><span class="sxs-lookup"><span data-stu-id="92d64-179">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="92d64-180">**\_vincolo di \_ \_ binding di \_ sicurezza del messaggio \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="92d64-180">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="92d64-181">**\_vincolo di \_ binding di sicurezza del messaggio WS nomeutente \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-181">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="92d64-182">**\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-182">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="92d64-183">**\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-183">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="92d64-184">Il layout dell'intestazione di sicurezza (come specificato dal [**layout dell'intestazione di \_ sicurezza della \_ proprietà \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) viene determinato da una delle asserzioni di criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d64-184">The security header layout (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_LAYOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Lax.../> => WS_SECURITY_HEADER_LAYOUT_LAX
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Strict.../> => WS_SECURITY_HEADER_LAYOUT_STRICT
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsFirst.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsLast.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

## <a name="constraints-with-timestamp-security"></a><span data-ttu-id="92d64-185">Vincoli con sicurezza timestamp</span><span class="sxs-lookup"><span data-stu-id="92d64-185">Constraints with Timestamp Security</span></span>

<span data-ttu-id="92d64-186">Questa sezione si applica quando viene utilizzato uno dei seguenti vincoli di binding:</span><span class="sxs-lookup"><span data-stu-id="92d64-186">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="92d64-187">**\_vincolo di \_ \_ binding di \_ sicurezza del messaggio \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="92d64-187">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="92d64-188">**\_vincolo di \_ binding di sicurezza del messaggio WS nomeutente \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-188">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="92d64-189">**\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-189">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="92d64-190">**\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_**</span><span class="sxs-lookup"><span data-stu-id="92d64-190">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="92d64-191">Il fatto che un timestamp sia incluso nell'intestazione di sicurezza (come specificato dalla [**\_ Proprietà WS \_ Security \_ timestamp \_ Usage**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) sia determinato dalla presenza di SP: IncludeTimestamp nel percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="92d64-191">Whether or not a timestamp is included in the security header (as specified by [**WS\_SECURITY\_PROPERTY\_TIMESTAMP\_USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by the presence of the sp:IncludeTimestamp in the following location:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

<span data-ttu-id="92d64-192">Se l'asserzione sp: IncludeTimestamp è presente, il valore dei criteri [**è \_ sempre WS Security \_ timestamp \_ Usage \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="92d64-192">If the sp:IncludeTimestamp assertion is present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

<span data-ttu-id="92d64-193">Se l'asserzione sp: IncludeTimestamp non è presente, il valore dei criteri è [**WS \_ Security \_ timestamp \_ Usage \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="92d64-193">If the sp:IncludeTimestamp assertion is not present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

 

 




