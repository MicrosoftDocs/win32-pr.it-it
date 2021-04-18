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
# <a name="metadata-mapping"></a>Mapping dei metadati

Il contenuto di un documento di metadati viene mappato all'API dei metadati nei modi descritti nelle sezioni seguenti.


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

Nelle sezioni successive vengono descritti i costrutti delle API insieme ai costrutti di metadati (WSDL o Policy) a cui corrispondono.

Una certa familiarità con le specifiche dei metadati, come WSDL e Policy, aiuterà a comprendere questa sezione.

## <a name="endpoint-address"></a>Indirizzo endpoint

L'indirizzo di un endpoint (vedere [**WS \_ endpoint \_ Address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) viene ottenuto da un elemento extensibility nell'elemento WSDL: Port del documento WSDL. Per specificare l'indirizzo sono supportati gli elementi di estensibilità seguenti:

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

## <a name="ws_channel_binding"></a>\_binding di canale WS \_

L'associazione di canale (vedere [**WS \_ Channel \_ Binding**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) è determinata dal trasporto utilizzato dall'associazione SOAP, come indicato di seguito:

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>\_ \_ versione busta della proprietà del canale WS \_ \_

La versione della busta ( [**vedere \_ \_ versione della \_ busta \_ della proprietà del canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) è determinata dall'associazione SOAP utilizzata, come indicato di seguito:

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

## <a name="addressing-version"></a>Versione Addressing

La versione di indirizzamento (vedere la pagina relativa alla [**\_ \_ \_ \_ versione di indirizzamento delle proprietà del canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) è determinata dalle asserzioni seguenti nei criteri dell'endpoint:

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

Se non è presente un'asserzione di indirizzamento, viene presupposto il [**trasporto della versione di WS \_ Addressing \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .

## <a name="message-encoding"></a>Codifica dei messaggi

La codifica del messaggio (vedere la [**\_ codifica della \_ proprietà \_ WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) è determinata dalle asserzioni seguenti nei criteri dell'endpoint:

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Si noti che l'asserzione di criteri di codifica binaria non include informazioni sul fatto che la codifica binaria sia con sessione o senza sessione. Questa condizione è determinata dal vincolo della proprietà di codifica (che deve essere appropriato a seconda che il [**\_ \_ tipo di canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) utilizzato sia o meno sessione).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Se nessuna delle asserzioni precedenti è presente, viene utilizzata una codifica del testo: [**WS Encoding \_ \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ Encoding \_ XML \_ UTF16LE**, **WS \_ Encoding \_ XML \_ UTF16BE**.

Si noti che i criteri non includono informazioni sul set di caratteri per MTOM o codifiche di testo (indipendentemente dal fatto che sia UTF8, UTF16LE o UTF16BE). Il valore effettivo del set di caratteri utilizzato è determinato dal vincolo della proprietà Encoding.

## <a name="constraints-with-http-header-authentication"></a>Vincoli con autenticazione dell'intestazione HTTP

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza per l' [**\_ autenticazione dell' \_ intestazione \_ \_ \_ \_ WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) .

Questa associazione di sicurezza è indicata nei criteri da diverse asserzioni che specificano l'autenticazione dell'intestazione HTTP e che deve essere utilizzato un particolare schema di autenticazione. Le asserzioni di criteri corrispondono ai valori dello [**schema di \_ \_ autenticazione dell' \_ \_ \_ intestazione \_ \_ http della proprietà di associazione di sicurezza WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) come indicato di seguito:

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

Questa sezione si applica quando viene specificato il vincolo di binding di sicurezza del [**trasporto di WS \_ SSL \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) . In questo caso vengono usate le asserzioni di criteri seguenti:

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

## <a name="constraints-with-sspi-transport-security"></a>Vincoli con la sicurezza del trasporto SSPI

Questa sezione si applica quando si specifica il vincolo di binding di sicurezza del [**\_ \_ \_ \_ \_ \_ trasporto SSPI di WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) . In questo caso vengono usate le asserzioni di criteri seguenti:

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

## <a name="constrains-with-transport-security"></a>Vincoli con la sicurezza del trasporto

È possibile specificare il vincolo della proprietà [**livello di protezione del trasporto delle \_ proprietà di sicurezza \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) se è stato specificato uno dei vincoli di associazione di sicurezza:

-   [**\_vincolo di \_ binding di sicurezza del trasporto \_ \_ di WS SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    Il valore da policy è sempre [**il \_ segno di livello di protezione WS e la \_ \_ \_ \_ crittografia**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

-   [**\_vincolo di \_ \_ binding di sicurezza del trasporto SSPI \_ \_ di WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

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

-   [**\_vincolo di \_ \_ binding di \_ sicurezza \_ \_ per l'autenticazione dell'intestazione WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    Il valore dei criteri è sempre [**il \_ livello di protezione WS \_ \_ None**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Vincoli con l'associazione di sicurezza APREQ Kerberos

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza del [**\_ messaggio WS Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) . In questo caso vengono usate le asserzioni di criteri seguenti:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a>Vincoli con associazione di sicurezza dei messaggi

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza del vincolo di sicurezza del [**\_ \_ messaggio \_ \_ \_ WS nomeutente**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) . In questo caso vengono usate le asserzioni di criteri seguenti:

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza del [**\_ \_ \_ \_ \_ vincolo di sicurezza del messaggio WS CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) . In questo caso vengono usate le asserzioni di criteri seguenti:

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza per il vincolo di sicurezza dei [**\_ \_ \_ messaggi del \_ \_ \_ token WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) . In questo caso vengono usate le asserzioni di criteri seguenti:

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

Di seguito viene descritto il mapping dei campi del [**\_ vincolo di \_ \_ associazione di \_ sicurezza \_ \_ dei messaggi del token WS rilasciato**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) ai criteri sopra indicati:

-   Il campo claimConstraints viene usato per verificare il set di URI del tipo di attestazione che vengono visualizzati all'interno dell'elemento WSI: ClaimType precedente.

-   Il campo issuerAddress corrisponde all'elemento wsp: Issuer precedente, che è l' [**indirizzo dell' \_ endpoint \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) del servizio che può emettere il token.

-   Il campo requestSecurityTokenTemplate corrisponde agli elementi figlio dell'elemento wsp: RequestSecurityTokenTemplate.

## <a name="ws_security_context_message_security_binding_constraint"></a>\_vincolo di \_ \_ associazione di sicurezza del messaggio del contesto \_ di \_ sicurezza WS \_

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza del [**\_ \_ \_ messaggio del \_ \_ \_ contesto**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) di sicurezza WS. In questo caso vengono usate le asserzioni di criteri seguenti:

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

La modalità entropia è determinata dall'asserzione di> <SP: Trust10. <SP: RequireClientEntropy/> e <SP: RequireServerEntropy/> => [**ws \_ \_ modalità entropia della chiave di sicurezza \_ \_ \_ combinata**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: RequireClientEntropy/> => **ws \_ sicurezza \_ chiave \_ entropia in \_ modalità \_ \_ solo client** <SP: RequireServerEntropy/> => **WS \_ sicurezza \_ chiave \_ entropia \_ modalità \_ \_ solo server**

## <a name="ws_request_security_token_property_trust_version"></a>\_versione del \_ \_ trust della proprietà del token di sicurezza \_ WS \_ Request \_

Questa sezione si applica quando viene specificato il vincolo di associazione di sicurezza per il vincolo di sicurezza dei [**\_ \_ \_ messaggi del \_ \_ \_ token WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) . Le asserzioni di criteri seguenti vengono utilizzate per identificare [**la \_ \_ versione di WS Trust**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) e le opzioni associate.

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

È possibile specificare la versione del trust utilizzando [**il \_ \_ vincolo della \_ \_ proprietà del \_ token di sicurezza WS request**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) con un ID di proprietà della [**\_ \_ \_ \_ \_ \_ versione di trust della proprietà del token di sicurezza WS request**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).

## <a name="ws_security_property_security_header_version"></a>\_versione dell' \_ intestazione di sicurezza della proprietà WS Security \_ \_ \_

Questa sezione si applica quando viene utilizzato uno dei seguenti vincoli di binding:

-   [**\_vincolo di \_ \_ binding di \_ sicurezza del messaggio \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_vincolo di \_ binding di sicurezza del messaggio WS nomeutente \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

La versione di sicurezza dell'intestazione (come specificato dalla [**versione dell'intestazione di \_ sicurezza della \_ proprietà \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) è determinata da una delle asserzioni di criteri seguenti:

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Vincoli con layout di sicurezza dell'intestazione

Questa sezione si applica quando viene utilizzato uno dei seguenti vincoli di binding:

-   [**\_vincolo di \_ \_ binding di \_ sicurezza del messaggio \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_vincolo di \_ binding di sicurezza del messaggio WS nomeutente \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Il layout dell'intestazione di sicurezza (come specificato dal [**layout dell'intestazione di \_ sicurezza della \_ proprietà \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) viene determinato da una delle asserzioni di criteri seguenti:

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

Questa sezione si applica quando viene utilizzato uno dei seguenti vincoli di binding:

-   [**\_vincolo di \_ \_ binding di \_ sicurezza del messaggio \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_vincolo di \_ binding di sicurezza del messaggio WS nomeutente \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Il fatto che un timestamp sia incluso nell'intestazione di sicurezza (come specificato dalla [**\_ Proprietà WS \_ Security \_ timestamp \_ Usage**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) sia determinato dalla presenza di SP: IncludeTimestamp nel percorso seguente:

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

Se l'asserzione sp: IncludeTimestamp è presente, il valore dei criteri [**è \_ sempre WS Security \_ timestamp \_ Usage \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Se l'asserzione sp: IncludeTimestamp non è presente, il valore dei criteri è [**WS \_ Security \_ timestamp \_ Usage \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

 

 




