---
title: Mapping dei metadati
description: Il contenuto di un documento di metadati viene mappato all'API dei metadati nei modi illustrati nelle sezioni seguenti.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Servizi Web di mapping dei metadati per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e6577e05f1d51ec13cc917465c306b94c403827149b086f252a38964997ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841491"
---
# <a name="metadata-mapping"></a>Mapping dei metadati

Il contenuto di un documento di metadati viene mappato all'API dei metadati nei modi illustrati nelle sezioni seguenti.


In questa documentazione vengono usati i prefissi degli spazi dei nomi seguenti:

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

Le sezioni successive descrivono i costrutti API insieme ai costrutti di metadati (WSDL o Criteri) a cui corrispondono.

La familiarità con le specifiche dei metadati, ad esempio WSDL e Criteri, consente di comprendere questa sezione.

## <a name="endpoint-address"></a>Indirizzo dell'endpoint

L'indirizzo di un endpoint (vedere [**WS \_ ENDPOINT \_ ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) viene ottenuto da un elemento di estendibilità all'interno dell'elemento wsdl:port del documento WSDL. Per specificare l'indirizzo sono supportati gli elementi di estendibilità seguenti:

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

## <a name="ws_channel_binding"></a>BINDING DEL CANALE WS \_ \_

L'associazione di canale [**(vedere WS \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) è determinata dal trasporto usato dall'associazione soap, come indicato di seguito:

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>VERSIONE ENVELOPE \_ \_ DELLE PROPRIETÀ DEL \_ CANALE \_ WS

La versione envelope (vedere [**WS \_ CHANNEL PROPERTY ENVELOPE \_ \_ \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) è determinata dall'associazione soap usata, come indicato di seguito:

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

## <a name="addressing-version"></a>Versione di indirizzamento

La versione di indirizzamento (vedere [**WS \_ CHANNEL PROPERTY \_ \_ ADDRESSING \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) è determinata dalle asserzioni seguenti nei criteri dell'endpoint:

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

Se non è presente un'asserzione di indirizzamento, si presuppone [**che WS \_ ADDRESSING \_ VERSION \_ TRANSPORT.**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)

## <a name="message-encoding"></a>Codifica dei messaggi

La codifica del messaggio (vedere [**WS \_ CHANNEL PROPERTY \_ \_ ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) è determinata dalle asserzioni seguenti nei criteri dell'endpoint:

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Si noti che l'asserzione dei criteri di codifica binaria non include informazioni sul fatto che la codifica binaria sia con sessione o senza sessione. Questo è determinato dal vincolo della proprietà di codifica (che deve essere appropriato a seconda che il tipo di canale [**WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) in uso sia con sessione o meno).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Se nessuna delle asserzioni precedenti è presente, viene usata una codifica di testo: [**WS \_ ENCODING XML \_ \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS ENCODING XML \_ \_ \_ UTF16LE**, **WS ENCODING XML \_ \_ \_ UTF16BE**.

Si noti che i criteri non includono informazioni sul set di caratteri per le codifiche MTOM o di testo (indipendentemente dal fatto che si tratta di UTF8, UTF16LE o UTF16BE). Il valore effettivo del set di caratteri usato è determinato dal vincolo della proprietà di codifica.

## <a name="constraints-with-http-header-authentication"></a>Vincoli con l'autenticazione dell'intestazione HTTP

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza [**WS \_ HTTP HEADER \_ \_ AUTH SECURITY BINDING \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

Questa associazione di sicurezza è indicata nei criteri da asserzioni diverse che indicano sia che deve essere usata l'autenticazione dell'intestazione HTTP sia che deve essere usato uno schema di autenticazione specifico. Le asserzioni dei criteri corrispondono ai valori di [**WS \_ SECURITY BINDING PROPERTY HTTP HEADER \_ \_ \_ \_ \_ AUTH \_ SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) come indicato di seguito:

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

## <a name="constraints-with-sll-transport-security"></a>Vincoli con la sicurezza del trasporto SLL

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza [**\_ WS SSL \_ TRANSPORT SECURITY \_ BINDING \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) In questo caso vengono usate le asserzioni di criteri seguenti:

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

## <a name="constraints-with-sspi-transport-security"></a>Vincoli con sicurezza del trasporto SSPI

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) In questo caso vengono usate le asserzioni di criteri seguenti:

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

## <a name="constrains-with-transport-security"></a>Vincola con la sicurezza dei trasporti

Il vincolo di proprietà [**WS \_ SECURITY PROPERTY TRANSPORT PROTECTION \_ \_ \_ \_ LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) può essere specificato se viene specificato uno dei vincoli di associazione di sicurezza:

-   [**VINCOLO DI \_ ASSOCIAZIONE DI SICUREZZA DEL \_ \_ TRASPORTO \_ SSL WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    Il valore dei criteri è sempre [**WS \_ PROTECTION LEVEL SIGN AND \_ \_ \_ \_ ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

-   [**VINCOLO DI \_ ASSOCIAZIONE DI SICUREZZA DEL TRASPORTO \_ SSPI TCP WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    Il valore dei criteri viene specificato come parte dell'asserzione WindowsTransportSecurity, come indicato di seguito:

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [**VINCOLO DI ASSOCIAZIONE DI SICUREZZA \_ \_ \_ DELL'AUTENTICAZIONE \_ DELL'INTESTAZIONE \_ HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    Il valore del criterio è sempre [**WS \_ PROTECTION LEVEL \_ \_ NONE.**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Vincoli con l'associazione di sicurezza APREQ Kerberos

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) In questo caso vengono usate le asserzioni di criteri seguenti:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a>Vincoli con l'associazione di sicurezza dei messaggi

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza [**\_ WS USERNAME \_ MESSAGE SECURITY \_ BINDING \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) In questo caso vengono usate le asserzioni di criteri seguenti:

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>VINCOLO DI ASSOCIAZIONE DI SICUREZZA DEI MESSAGGI WS \_ CERT \_ \_ \_ \_

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza [**WS \_ CERT \_ MESSAGE SECURITY \_ BINDING \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) In questo caso vengono usate le asserzioni di criteri seguenti:

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>VINCOLO DI ASSOCIAZIONE DI \_ SICUREZZA DEI MESSAGGI TOKEN \_ \_ \_ EMESSI DA \_ \_ WS

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza [**WS \_ ISSUED TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) In questo caso vengono usate le asserzioni di criteri seguenti:

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

Di seguito viene descritto il mapping dei campi di [**WS \_ ISSUED TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) al criterio precedente:

-   Il campo claimConstraints viene usato per verificare il set di URI del tipo di attestazione visualizzati all'interno dell'elemento wsi:ClaimType precedente.

-   Il campo issuerAddress corrisponde all'elemento wsp:Issuer precedente, ovvero l'INDIRIZZO [**ENDPOINT WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) del servizio che può rilasciare il token.

-   Il campo requestSecurityTokenTemplate corrisponde agli elementi figlio dell'elemento wsp:RequestSecurityTokenTemplate.

## <a name="ws_security_context_message_security_binding_constraint"></a>VINCOLO DI ASSOCIAZIONE DI SICUREZZA \_ DEI MESSAGGI DEL CONTESTO DI \_ \_ \_ \_ \_ SICUREZZA WS

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza [**\_ WS SECURITY \_ CONTEXT MESSAGE SECURITY BINDING \_ \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) In questo caso vengono usate le asserzioni di criteri seguenti:

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

La modalità entropia è determinata dall'asserzione <sp:Trust10>. <sp:RequireClientEntropy/> e <sp:RequireServerEntropy/> => [**WS \_ SECURITY KEY \_ \_ ENTROPY MODE \_ \_ COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS SECURITY KEY \_ \_ ENTROPY MODE CLIENT \_ \_ \_ \_ ONLY** <sp:RequireServerEntropy/> => **WS \_ SECURITY \_ KEY \_ ENTROPY \_ MODE SERVER \_ \_ ONLY**

## <a name="ws_request_security_token_property_trust_version"></a>VERSIONE DI ATTENDIBILITÀ \_ DELLE PROPRIETÀ DEL TOKEN DI SICUREZZA DELLA \_ \_ \_ \_ \_ RICHIESTA WS

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza [**WS \_ ISSUED TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) Le asserzioni di criteri seguenti vengono usate per identificare la [**versione di WS \_ TRUST \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) e le opzioni associate.

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

La versione di attendibilità può essere specificata usando [**WS \_ REQUEST SECURITY TOKEN PROPERTY \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) con ID di proprietà [**WS REQUEST SECURITY TOKEN \_ PROPERTY TRUST \_ \_ \_ \_ \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).

## <a name="ws_security_property_security_header_version"></a>VERSIONE \_ DELL'INTESTAZIONE DI \_ SICUREZZA DELLE PROPRIETÀ DI \_ \_ SICUREZZA DI \_ WS

Questa sezione si applica quando si usa uno dei vincoli di associazione seguenti:

-   [**VINCOLO DI ASSOCIAZIONE DI \_ \_ SICUREZZA DEI MESSAGGI APREQ KERBEROS \_ \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**VINCOLO DI ASSOCIAZIONE DI \_ SICUREZZA DEL MESSAGGIO DEL NOME \_ \_ UTENTE \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**VINCOLO DI ASSOCIAZIONE DI SICUREZZA DEI MESSAGGI WS \_ CERT \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**VINCOLO DI ASSOCIAZIONE DI \_ SICUREZZA DEI MESSAGGI TOKEN \_ \_ \_ EMESSI DA \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

La versione di sicurezza dell'intestazione (come specificato da [**WS \_ SECURITY PROPERTY SECURITY HEADER \_ \_ \_ \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) è determinata da una delle asserzioni di criteri seguenti:

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Vincoli con layout di sicurezza delle intestazioni

Questa sezione si applica quando si usa uno dei vincoli di associazione seguenti:

-   [**VINCOLO DI ASSOCIAZIONE DI \_ \_ SICUREZZA DEI MESSAGGI APREQ KERBEROS \_ \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**VINCOLO DI ASSOCIAZIONE DI \_ SICUREZZA DEL MESSAGGIO DEL NOME \_ \_ UTENTE \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**VINCOLO DI ASSOCIAZIONE DI SICUREZZA DEI MESSAGGI WS \_ CERT \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**VINCOLO DI ASSOCIAZIONE DI \_ SICUREZZA DEI MESSAGGI TOKEN \_ \_ \_ EMESSI DA \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Il layout dell'intestazione di sicurezza (come specificato da [**WS \_ SECURITY PROPERTY SECURITY HEADER \_ \_ \_ \_ LAYOUT)**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)è determinato da una delle asserzioni di criteri seguenti:

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

## <a name="constraints-with-timestamp-security"></a>Vincoli con sicurezza timestamp

Questa sezione si applica quando si usa uno dei vincoli di associazione seguenti:

-   [**VINCOLO DI ASSOCIAZIONE DI \_ \_ SICUREZZA DEI MESSAGGI APREQ KERBEROS \_ \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**VINCOLO DI ASSOCIAZIONE DI \_ SICUREZZA DEL MESSAGGIO DEL NOME \_ \_ UTENTE \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**VINCOLO DI ASSOCIAZIONE DI SICUREZZA DEI MESSAGGI WS \_ CERT \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**VINCOLO DI ASSOCIAZIONE DI \_ SICUREZZA DEI MESSAGGI TOKEN \_ \_ \_ EMESSI DA \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

L'inclusione o meno di un timestamp nell'intestazione di sicurezza (come specificato da [**WS \_ SECURITY PROPERTY \_ TIMESTAMP \_ \_ USAGE)**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)dipende dalla presenza di sp:IncludeTimestamp nel percorso seguente:

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

Se è presente l'asserzione sp:IncludeTimestamp, il valore dei criteri è [**WS \_ SECURITY TIMESTAMP USAGE \_ \_ \_ ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Se l'asserzione sp:IncludeTimestamp non è presente, il valore dei criteri è [**WS \_ SECURITY TIMESTAMP USAGE \_ \_ \_ NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

 

 




