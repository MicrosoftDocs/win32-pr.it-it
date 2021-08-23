---
title: Supporto dei criteri
description: Wsutil elabora i criteri specificati nei metadati di input e genera routine helper per il supporto del modello di servizio.
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Servizi Web di supporto criteri per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347265d4081216a227b5040fc73f272181bdccfe09ca7500b81078a6a57ed7bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838641"
---
# <a name="policy-support"></a>Supporto dei criteri

Wsutil elabora i criteri specificati nei metadati di input e genera routine helper per il supporto del modello di servizio.

## <a name="how-to-use-policy-support-in-wsutil"></a>Come usare il supporto dei criteri in wsutil

Gli sviluppatori devono seguire questa procedura per usare il supporto dei criteri nel compilatore wsutil:

-   Raccogliere tutti i file di metadati di input necessari per il servizio Web di destinazione.
-   Compilare tutti i file WSDL/XSD/policy raccolti usando wsutil.exe. Wsutil genera un set di file stub e file di intestazione per ogni file WSDL e XSD di input.
-   Esaminare il file di intestazione generato. Tutti i nomi delle routine helper dei criteri sono elencati nella sezione dei commenti all'inizio del file di intestazione.
-   Usare la routine helper bindingName \_ CreateServiceProxy per creare il proxy del servizio.
-   Usare la routine helper bindingName \_ CreateServiceEndpoint per creare l'endpoint di servizio.
-   Compilare la struttura WS \_ bindingTemplateType \_ BINDING TEMPLATE specificata nella firma del \_ metodo. Gli sviluppatori possono fornire proprietà aggiuntive del canale e/o proprietà di sicurezza in base alle esigenze.
-   Chiamare le routine helper, al completamento della creazione del proxy del servizio restituito o dell'endpoint del servizio.

Le sezioni seguenti descrivono in dettaglio gli argomenti correlati.

## <a name="handle-policy-input"></a>Gestire l'input dei criteri

Di seguito sono riportate [le opzioni del compilatore](web-service-compiler-tool.md) correlate all'elaborazione dei criteri.

Per impostazione predefinita, wsutil genererà sempre modelli di criteri a meno che non venga chiamato con l'opzione "/nopolicy". I criteri possono essere incorporati come parte di un file WSDL o possono essere creati separatamente come file di metadati dei criteri che wsutil accetta come input. L'opzione del compilatore "/wsp:" viene usata per indicare che i metadati di input specificati sono un file di criteri. Wsutil genera potenziali helper correlati ai criteri con la compilazione seguente:

**wsutil /wsdl:trusted.wsdl /wsdl:trusted1.wsdl**

**wstuil /wsdl:input.wsdl /wsp:policy.wsp**

Quando l'opzione "/nopolicy" viene usata come nell'esempio seguente, non viene generato alcun helper criteri.

**wsutil /nopolicy /wsdl:trusted.wsdl /wsdl:trusted1.wsdl**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Codice correlato ai criteri generato dal compilatore wsutil

[Nella pagina Mapping](metadata-mapping.md) dei metadati viene descritto in dettaglio il mapping tra costrutti di metadati con tipi di associazione diversi.

È possibile specificare tre categorie di impostazioni dei criteri nelle impostazioni dei criteri:

-   Proprietà del canale. Attualmente sono supportate solo le proprietà del canale seguenti: [**WS \_ CHANNEL PROPERTY \_ \_ ENCODING,**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) **WS CHANNEL PROPERTY \_ \_ \_ ADDRESSING \_ VERSION** e **WS CHANNEL PROPERTY ENVELOPE \_ \_ \_ \_ VERSION**.
-   Proprietà di sicurezza. Attualmente sono supportate solo le proprietà di sicurezza seguenti: [**WS \_ SECURITY PROPERTY TIMESTAMP \_ \_ \_ USAGE,**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) **WS SECURITY PROPERTY SECURITY \_ \_ HEADER \_ \_ \_ LAYOUT,** **WS SECURITY PROPERTY TRANSPORT \_ \_ PROTECTION \_ \_ \_ LEVEL** e **WS SECURITY PROPERTY SECURITY \_ \_ HEADER \_ \_ \_ VERSION**.
-   Associazione di sicurezza. Attualmente sono supportate solo le associazioni di sicurezza seguenti: [**WS \_ HTTP HEADER \_ \_ AUTH SECURITY \_ \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [**WS \_ TCP \_ SSPI TRANSPORT SECURITY \_ \_ \_ BINDING, WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) [**USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) [**WS KERBEROS \_ \_ APREQ MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)e [**WS SECURITY MESSAGE SECURITY \_ \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).

Tipo di modello di associazione

In wsutil sono supportati un numero limitato di associazioni. Tutte le combinazioni supportate di queste associazioni sono elencate nella [**definizione WS \_ BINDING TEMPLATE \_ \_ TYPE.**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) Ad esempio, per l'associazione seguente in wsdl

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Wsutil genera il [**tipo di modello di associazione WS HTTP BINDING TEMPLATE \_ \_ \_ \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) per questa associazione.

Descrizioni dei criteri

Con l'impostazione dei criteri di input, wsutil genera un set di descrizioni dei criteri che descrivono i criteri di input, incluso il tipo di modello, nonché i valori specificati nei criteri. Ad esempio, per l'input

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

wsutil genera una descrizione della proprietà del canale, ad esempio:

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

Tutte le impostazioni dei criteri (proprietà del canale, proprietà di sicurezza e proprietà di associazione di sicurezza) in un'associazione vengono aggregate in un'unica struttura WS \_ bindingTemplateType \_ POLICY \_ DESCRIPTION. [**WS \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) specifica le diverse combinazioni di criteri di associazione supportate da wsutil.

Struttura del modello che deve essere compilata dall'applicazione

La descrizione dei criteri contiene tutte le informazioni sui criteri specificate nei metadati di input per una determinata associazione, ma sono presenti informazioni che non possono essere rappresentate nei criteri ma che richiedono l'input dell'utente quando si usa l'impostazione di tali criteri per creare il proxy del servizio e/o l'endpoint del servizio. Ad esempio, l'applicazione deve fornire le credenziali per l'autenticazione dell'intestazione HTTP.

L'applicazione deve compilare la struttura del modello, denominata WS bindingTemplateType BINDING TEMPLATE per ogni tipo di modello di associazione diverso, definito \_ \_ in \_ webservices.h:

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

L'elenco dei modelli di associazione di sicurezza è facoltativo dipende dall'associazione di sicurezza corrispondente. Ad esempio, il campo [**WS \_ SSL TRANSPORT SECURITY BINDING \_ \_ \_ \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) viene presentato in [**WS HTTP SSL BINDING \_ \_ \_ \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) per l'applicazione per fornire informazioni sull'associazione di sicurezza ssl, incluse le informazioni sulle credenziali.

L'applicazione deve compilare tutti i campi di questa struttura prima di chiamare le API del modello di servizi Web. Le proprietà di sicurezza aggiuntive, nonché le proprietà di associazione di sicurezza non rappresentabili nei criteri devono essere compilate e le API dei servizi Web uniscono i due set di proprietà in fase di esecuzione. Se non applicabile, è possibile azzerare i campi. Ad esempio, securityProperties può essere azzerato se non sono necessarie proprietà di sicurezza aggiuntive.

Routine helper e dichiarazione di descrizione dei criteri nei file di intestazione

wsutil crea una routine helper per semplificare il supporto nel livello del modello di servizio, in modo che l'applicazione possa creare più facilmente il proxy del servizio e l'endpoint di servizio. La descrizione dei criteri viene esposta in modo che l'applicazione possa usarli direttamente. Una routine della Guida CreateSerivceProxy è simile alla seguente:

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

Gli sviluppatori sono invitati a usare queste routine helper, anche se possono anche usare direttamente la routine di runtime sottostante fornita da webservices.dll. Gli sviluppatori non sono invitati a usare direttamente le descrizioni dei criteri durante la programmazione con il [livello del modello di](service-model-layer-overview.md) servizio.

I riferimenti alla descrizione dei criteri vengono generati anche nell'intestazione per l'utente avanzato. Se gli sviluppatori non usano le funzionalità del modello di servizio, possono usare direttamente le descrizioni dei criteri.

``` syntax
struct {
  ...
  struct {
    ...
    } contracts;
  struct {
    WS_bindingTemplateType_POLICY_DESCRIPTION bindingName;
    ...
    } policies;
  }
```

Prototipi di definizione nei file stub

Nella struttura del prototipo locale viene creato un singolo campo della struttura di descrizione dei criteri per ogni associazione e le relative descrizioni dell'helper a cui si fa riferimento internamente. Le descrizioni dei criteri vengono generate nel file in cui viene generata la DESCRIZIONE DEL CONTRATTO [**WS. \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) In genere gli sviluppatori non devono esaminare il file stub durante lo sviluppo, anche se il file stub contiene tutti i dettagli sulle specifiche dei criteri.

``` syntax
struct {
  ...
  struct {
  ... } contracts;
  ...
 struct {
      struct {
        hierarchy of policy template descriptions;
        } bindingName;
      ...
      list of bindings in the input wsdl file.
  } policies;
} fileNameLocalDefinitions;
```

Implementazione di routine helper nei file stub

Wsutil genera routine helper per semplificare le chiamate dell'applicazione a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) e la creazione di [**WS \_ SERVICE \_ ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) in base alle informazioni fornite nelle impostazioni dei criteri.

A seconda dei vincoli di associazione specificati per la porta specificata, il primo argomento è diverso in base alla struttura del modello. Nell'esempio seguente si presuppone il trasporto HTTP, la firma per la creazione del proxy di servizio è simile a un parametro di tipo di canale aggiuntivo.

``` syntax
HRESULT bindingName_CreateServiceProxy(
    __in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
    __in const ULONG propertyCount,
    __deref_out WS_SERVICE_PROXY** serviceProxy,
    __in_opt WS_ERROR* error)
{
    return WsCreateServiceProxyFromTemplate(
      WS_CHANNEL_TYPE_REQUEST,    // this is fixed for http, requires input for TCP
      properties,     
      propertyCount, 
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),  
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_constraintName_POLICY_DESCRIPTION),
      serviceProxy,     
      error);     
}
```

``` syntax
HRESULT bindingName_CreateServiceEndpoint(
__in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
__in_opt const WS_STRING* addressUrl,
__in bindingNameFunctionTable* functionTable,
__in WS_SERVICE_SECURITY_CALLBACK authorizationCallback,
__in const WS_SERVICE_ENDPOINT_PROPERTY* properties,
__in ULONG propertyCount,
__in WS_HEAP* heap,
  __deref_out WS_SERVICE_ENDPOINT** serviceEndpoint,
  __in_opt WS_ERROR* error)
{
  WS_SERVICE_CONTRACT serviceContract;
  serviceContract.contractDescription = &fileName.contracts.bindingName;
  serviceContract.defaultMessageHandlerCallback = NULL;
  serviceContract.methodTable = (const void *)functionTable;

  return WsCreateServiceEndpointFromTemplate(
      properties,
      propertyCount,
      addressUrl,    // service endpoint address
      WS_CHANNEL_TYPE_RESPONSE,    // this is fixed for http, requires input for TCP
      &serviceContract,
      authorizationCallback,
      heap,
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_bindingTemplateType_POLICY_DESCRIPTION),
      serviceEndpoint,
      error);
}
```

## <a name="supported-policy-settings"></a>Impostazioni dei criteri supportate

Nella tabella seguente sono elencati tutti i tipi di modello di associazione supportati, le associazioni di sicurezza corrispondenti necessarie nel tipo, la struttura del modello da riempire dall'applicazione per il tipo e il tipo di descrizione corrispondente. L'applicazione deve compilare la struttura del modello, mentre lo sviluppatore dell'applicazione deve comprendere quali sono le associazioni di sicurezza necessarie nei criteri.



| [**TIPO DI \_ MODELLO DI \_ BINDING WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | Combinazioni di associazioni di sicurezza                                                                                                                                                                                                                                                                                                               | struttura del modello da riempita dall'applicazione                                                                                            | Descrizione dei criteri                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DI \_ MODELLO DI BINDING HTTP WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**MODELLO DI BINDING HTTP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**DESCRIZIONE DEI \_ CRITERI HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**TIPO DI \_ MODELLO DI BINDING SSL HTTP \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**ASSOCIAZIONE DI \_ SICUREZZA DEL TRASPORTO SSL WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**MODELLO DI \_ \_ BINDING SSL HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**DESCRIZIONE DEI \_ \_ CRITERI SSL HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**WS \_ HTTP \_ HEADER \_ AUTH \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**WS \_ HTTP \_ HEADER \_ AUTH \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**WS \_ HTTP \_ HEADER \_ AUTH \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**DESCRIZIONE DEI \_ CRITERI DI \_ AUTENTICAZIONE \_ DELL'INTESTAZIONE \_ HTTP WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**WS \_ HTTP \_ SSL \_ HEADER \_ AUTH \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**WS \_ ASSOCIAZIONE DI SICUREZZA DEL TRASPORTO SSL \_ \_ \_ E**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [ **BINDING DI SICUREZZA DELL'AUTENTICAZIONE \_ \_ \_ DELL'INTESTAZIONE \_ \_ HTTP WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**MODELLO DI \_ ASSOCIAZIONE \_ DI AUTENTICAZIONE \_ \_ DELL'INTESTAZIONE \_ SSL HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**DESCRIZIONE DEI CRITERI \_ \_ DI AUTENTICAZIONE \_ DELL'INTESTAZIONE SSL HTTP \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**TIPO DI MODELLO \_ DI ASSOCIAZIONE DEL NOME \_ UTENTE SSL \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ ASSOCIAZIONE DI SICUREZZA DEL TRASPORTO SSL \_ \_ E \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) [ **DI SICUREZZA DEI MESSAGGI DEL \_ NOME \_ \_ UTENTE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**MODELLO DI \_ ASSOCIAZIONE DEL NOME UTENTE SSL HTTP \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**DESCRIZIONE DEI \_ CRITERI DEL NOME UTENTE SSL \_ HTTP \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ ASSOCIAZIONE \_ DI SICUREZZA DEL \_ TRASPORTO \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) E BINDING DI SICUREZZA DEI MESSAGGI [ **\_ \_ APREQ \_ \_ \_ KERBEROS WS**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**TIPO DI \_ MODELLO DI BINDING TCP WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**MODELLO DI \_ BINDING TCP WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**DESCRIZIONE DEI \_ CRITERI TCP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**TIPO DI MODELLO \_ DI BINDING SSPI TCP \_ WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**BINDING DI SICUREZZA \_ \_ DEL TRASPORTO SSPI TCP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**MODELLO DI \_ ASSOCIAZIONE SSPI TCP \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**DESCRIZIONE DEI \_ CRITERI \_ SSPI TCP WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**TIPO DI MODELLO DI ASSOCIAZIONE \_ \_ NOME UTENTE SSPI TCP WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e [ **WS \_ USERNAME MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**MODELLO DI \_ ASSOCIAZIONE DEL NOME \_ UTENTE SSPI TCP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**DESCRIZIONE DEI \_ CRITERI DEL NOME \_ UTENTE SSPI TCP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**TIPO DI MODELLO DI ASSOCIAZIONE \_ \_ KERBEROS \_ \_ APREQ DI \_ \_ \_ WS TCP SSPI**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e [ **WS \_ KERBEROS \_ APREQ MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**DESCRIZIONE DEI CRITERI DI \_ \_ APREQ KERBEROS SSPI \_ TCP \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**TIPO DI MODELLO \_ DI ASSOCIAZIONE DEL CONTESTO DI SICUREZZA DEL NOME \_ \_ \_ \_ UTENTE \_ \_ \_ SSL WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ SSL \_ TRANSPORT \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e [**WS SECURITY CONTEXT MESSAGE \_ \_ SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) nel canale bootstrap                         | [**MODELLO DI ASSOCIAZIONE DEL CONTESTO \_ DI SICUREZZA DEL NOME \_ \_ \_ UTENTE \_ \_ SSL WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**DESCRIZIONE DEI CRITERI DEL \_ CONTESTO DI SICUREZZA DEL NOME \_ \_ \_ UTENTE \_ \_ SSL HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ SSL \_ TRANSPORT \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e [**WS SECURITY CONTEXT MESSAGE \_ \_ SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS KERBEROS \_ \_ APREQ MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) nel canale bootstrap            | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**TIPO DI MODELLO DI ASSOCIAZIONE DEL CONTESTO DI SICUREZZA DEL NOME \_ \_ UTENTE SSPI TCP \_ \_ \_ \_ \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e [**WS SECURITY CONTEXT MESSAGE \_ SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) nel canale bootstrap              | [**MODELLO DI ASSOCIAZIONE DEL \_ CONTESTO DI SICUREZZA DEL NOME \_ \_ \_ UTENTE \_ \_ SSPI TCP WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**DESCRIZIONE DEI CRITERI DEL CONTESTO DI SICUREZZA \_ \_ DEL NOME \_ \_ UTENTE \_ \_ SSPI TCP WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e [**WS SECURITY CONTEXT MESSAGE \_ SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS KERBEROS \_ \_ APREQ MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) nel canale bootstrap | [**MODELLO DI ASSOCIAZIONE DEL CONTESTO DI SICUREZZA \_ \_ KERBEROS \_ \_ APREQ DI \_ \_ \_ \_ WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

Ad esempio, [**WS \_ HTTP SSL BINDING \_ TEMPLATE \_ \_ \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) indica i criteri di input per l'associazione che specifica il trasporto HTTP e [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). L'applicazione deve compilare la struttura [**WS \_ HTTP SSL BINDING \_ \_ \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) prima di chiamare le routine helper e la descrizione dei criteri di corrispondenza è [**WS HTTP SSL POLICY \_ \_ \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description). In particolare, la sezione relativa all'associazione in WSDL contiene i segmenti seguenti:

``` syntax
<wsp:Policy...>
  <sp:TransportBinding...>
    <wsp:Policy...>
      <sp:TransportToken...>
        <wsp:Policy...>
          <sp:HttpsToken.../>
        </wsp:Policy...>
      </sp:TransportToken...>
    </wsp:Policy>
  </sp:TransportBinding...>
</wsp:Policy>
```

``` syntax
<wsdl:binding...>
<soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

## <a name="security-context-support"></a>Supporto del contesto di sicurezza

In [Contesto di sicurezza](security-context.md)viene creato il canale bootstrap per stabilire la conversazione protetta nel canale del servizio. Wsutil supporta solo lo scenario in cui il canale bootstrap è lo stesso del canale del servizio, con le stesse proprietà del canale e le stesse proprietà di sicurezza. La sicurezza del trasporto è necessaria per l'associazione di messaggi del contesto di sicurezza. wsutil supporta i canali bootstrap con altre associazioni di sicurezza dei messaggi, ma supporta solo il contesto di sicurezza come unica associazione di sicurezza dei messaggi nel canale del servizio, senza combinazione con altre associazioni di sicurezza dei messaggi. Gli sviluppatori possono supportare queste combinazioni al di fuori del supporto del modello di criteri.

L'enumerazione seguente fa parte del supporto dei criteri:

-   [**TIPO DI \_ MODELLO DI \_ BINDING WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

Le funzioni seguenti fanno parte del supporto dei criteri:

-   [**WsCreateServiceEndpointFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**WsCreateServiceProxyFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

Le strutture seguenti fanno parte del supporto dei criteri:

-   [**MODELLO DI BINDING HTTP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**MODELLO DI \_ ASSOCIAZIONE DI \_ AUTENTICAZIONE \_ DELL'INTESTAZIONE \_ HTTP WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**DESCRIZIONE DEI \_ CRITERI DI \_ AUTENTICAZIONE \_ DELL'INTESTAZIONE \_ HTTP WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**WS \_ HTTP \_ HEADER \_ AUTH \_ SECURITY \_ BINDING \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**MODELLO DI ASSOCIAZIONE DI SICUREZZA \_ \_ \_ DELL'AUTENTICAZIONE \_ DELL'INTESTAZIONE \_ HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**DESCRIZIONE DEI \_ CRITERI HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**MODELLO DI \_ \_ BINDING SSL HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**MODELLO DI \_ BINDING \_ DI AUTENTICAZIONE \_ \_ DELL'INTESTAZIONE \_ SSL HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**DESCRIZIONE DEI CRITERI \_ \_ DI AUTENTICAZIONE \_ DELL'INTESTAZIONE SSL HTTP \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**DESCRIZIONE DEI \_ \_ CRITERI SSL HTTP WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**MODELLO DI \_ ASSOCIAZIONE DEL NOME UTENTE SSL HTTP \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**DESCRIZIONE DEI \_ CRITERI DEL NOME UTENTE SSL \_ HTTP \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**MODELLO DI ASSOCIAZIONE DEL CONTESTO \_ DI SICUREZZA DEL NOME \_ \_ \_ UTENTE \_ \_ SSL WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**DESCRIZIONE DEI CRITERI DEL \_ CONTESTO DI SICUREZZA DEL NOME \_ \_ \_ UTENTE \_ \_ SSL HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**MODELLO DI ASSOCIAZIONE DI SICUREZZA DEI \_ \_ MESSAGGI APREQ KERBEROS \_ \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**WS \_ SECURITY \_ CONTEXT \_ MESSAGE \_ SECURITY \_ BINDING \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**MODELLO DI \_ ASSOCIAZIONE DI SICUREZZA DEI MESSAGGI DEL CONTESTO DI SICUREZZA \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**DESCRIZIONE DEI \_ CRITERI DI ASSOCIAZIONE DI SICUREZZA DEL CONTESTO DI SICUREZZA \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**MODELLO DI \_ ASSOCIAZIONE DI SICUREZZA DEL CONTESTO DI SICUREZZA \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**DESCRIZIONE DEI \_ CRITERI DI ASSOCIAZIONE DI SICUREZZA DEL \_ \_ TRASPORTO \_ \_ SSL WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**MODELLO DI \_ ASSOCIAZIONE DI SICUREZZA DEL TRASPORTO SSL \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**DESCRIZIONE DEI \_ CRITERI DI ASSOCIAZIONE DI SICUREZZA \_ \_ DEL \_ \_ \_ TRASPORTO SSPI WS**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**MODELLO DI \_ BINDING TCP WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**DESCRIZIONE DEI \_ CRITERI TCP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**MODELLO DI \_ ASSOCIAZIONE SSPI TCP \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ BINDING \_ TEMPLATE**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**DESCRIZIONE DEI CRITERI DI \_ \_ APREQ KERBEROS SSPI \_ TCP \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**MODELLO DI ASSOCIAZIONE DEL CONTESTO DI SICUREZZA \_ \_ KERBEROS \_ \_ APREQ DI \_ \_ \_ \_ WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**DESCRIZIONE DEI \_ CRITERI \_ SSPI TCP WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**MODELLO DI ASSOCIAZIONE DI \_ \_ SICUREZZA DEL TRASPORTO SSPI TCP WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**MODELLO DI \_ ASSOCIAZIONE DEL NOME \_ UTENTE SSPI TCP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**DESCRIZIONE DEI \_ CRITERI DEL NOME \_ UTENTE SSPI TCP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**MODELLO DI ASSOCIAZIONE DEL \_ CONTESTO DI SICUREZZA DEL NOME \_ \_ \_ UTENTE \_ \_ SSPI TCP WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**DESCRIZIONE DEI CRITERI DEL CONTESTO DI SICUREZZA \_ \_ DEL NOME \_ \_ UTENTE \_ \_ SSPI TCP WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**DESCRIZIONE DEI CRITERI \_ DI ASSOCIAZIONE DI SICUREZZA DEL MESSAGGIO DEL \_ \_ \_ \_ NOME \_ UTENTE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**MODELLO DI ASSOCIAZIONE DI \_ SICUREZZA DEI MESSAGGI DEL NOME \_ \_ UTENTE \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




