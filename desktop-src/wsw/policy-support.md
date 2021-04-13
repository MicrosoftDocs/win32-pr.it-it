---
title: Supporto dei criteri
description: Wsutil elabora i criteri specificati nei metadati di input e genera routine di supporto per il supporto del modello di servizio.
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Servizi Web di supporto dei criteri per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aafcd481fd4ea8a8cc6782a5dc50655fb9255c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331068"
---
# <a name="policy-support"></a>Supporto dei criteri

Wsutil elabora i criteri specificati nei metadati di input e genera routine di supporto per il supporto del modello di servizio.

## <a name="how-to-use-policy-support-in-wsutil"></a>Come usare il supporto dei criteri in wsutil

Gli sviluppatori devono attenersi alla procedura seguente per usare il supporto dei criteri nel compilatore WSUTIL:

-   Raccogliere tutti i file di metadati di input necessari per il servizio Web di destinazione.
-   Compilare tutti i file WSDL/XSD/Policy raccolti utilizzando wsutil.exe. Wsutil genera un set di file stub e file di intestazione per ogni file WSDL e XSD di input.
-   Esaminare il file di intestazione generato. tutti i nomi di routine helper dei criteri sono elencati nella sezione commento all'inizio del file di intestazione.
-   Usare BindingName \_ CreateServiceProxy routine di supporto per creare il proxy del servizio.
-   Usare BindingName \_ CreateServiceEndpoint routine di supporto per creare un endpoint del servizio.
-   Compilare \_ \_ la struttura del modello di associazione WS bindingTemplateType \_ specificata nella firma del metodo. Gli sviluppatori possono fornire proprietà del canale aggiuntive e/o proprietà di sicurezza in base alle esigenze.
-   Chiamare le routine di supporto, in modo che venga creato un proxy del servizio restituito o un endpoint del servizio riuscito.

Le sezioni seguenti descrivono in dettaglio gli argomenti correlati.

## <a name="handle-policy-input"></a>Gestisci input dei criteri

Di seguito sono riportate le [Opzioni del compilatore](web-service-compiler-tool.md) correlate all'elaborazione dei criteri.

Per impostazione predefinita, WSUTIL genererà sempre modelli di criteri a meno che non venga chiamato con l'opzione "/nopolicy". I criteri possono essere incorporati come parte di un file WSDL oppure possono essere creati separatamente come file di metadati dei criteri che WSUTIL accetta come input. L'opzione del compilatore "/wsp:" viene usata per indicare che i metadati di input specificati sono un file di criteri. Wsutil genera gli helper potenziali correlati ai criteri con la compilazione seguente:

**wsutil/WSDL: trusted. WSDL/WSDL: trusted1. WSDL**

**wstuil/WSDL: input. WSDL/wsp: Policy. wsp**

Quando si usa l'opzione "/nopolicy", non viene generato alcun helper del criterio come nell'esempio seguente.

**wsutil/nopolicy/WSDL: trusted. WSDL/WSDL: trusted1. WSDL**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Codice correlato ai criteri generato dal compilatore wsutil

Pagina [mapping metadati](metadata-mapping.md) dettagli il mapping tra costrutti di metadati con tipi di associazione diversi.

Nelle impostazioni dei criteri è possibile specificare tre categorie di impostazioni dei criteri:

-   Proprietà del canale. Attualmente sono supportate solo le seguenti proprietà del canale: [**WS \_ Channel \_ Property \_ Encoding**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id), **WS \_ Channel \_ Property \_ Addressing \_ Version** e **WS \_ Channel \_ Property \_ Envelope \_ Version**.
-   Proprietà di sicurezza. Attualmente sono supportate solo le seguenti proprietà di sicurezza: [**WS \_ Security proprietà \_ \_ timestamp \_ Usage**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id), **WS \_ Security Property Security \_ \_ \_ header \_**, **WS \_ Security \_ Property \_ Transport \_ \_ Level** e WS Security Property Security **\_ \_ \_ \_ header \_ Version**.
-   Associazione di sicurezza. Attualmente sono supportate solo le seguenti associazioni di sicurezza: [**WS \_ http \_ header \_ auth \_ \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)di sicurezza [**, \_ WS \_ SSL \_ Transport Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)binding, [**WS \_ TCP \_ SSPI \_ Transport \_ Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)binding, [**WS \_ nomeutente \_ message \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding), [**WS \_ Kerberos \_ APREQ \_ message \_ Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)binding e [**WS \_ Security \_ Context \_ message \_ \_ Binding sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).

Tipo di modello di associazione

In WSUTIL sono supportati numeri limitati di binding. Tutte le combinazioni supportate di queste associazioni sono elencate nella definizione [**del \_ \_ \_ tipo di modello di binding WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) . Ad esempio, per l'associazione seguente in WSDL

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Wsutil genera il tipo di modello di associazione [**WS \_ http \_ binding \_ \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) per questa associazione.

Descrizioni dei criteri

Con l'impostazione dei criteri di input, WSUTIL genera un set di descrizioni dei criteri che descrivono i criteri di input, inclusi il tipo di modello, nonché i valori specificati nei criteri. Ad esempio, per l'input

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

wsutil genera la descrizione della proprietà del canale, ad esempio:

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

Tutte le impostazioni dei criteri (proprietà del canale, proprietà di sicurezza e proprietà di associazione di sicurezza) in un'associazione vengono aggregate in una \_ struttura di descrizione dei criteri WS bindingTemplateType \_ \_ . [**WS \_ \_ \_ Tipo di modello di associazione**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) specifica le diverse combinazioni di criteri di associazione supportate da wsutil.

Struttura del modello da compilare per applicazione

La descrizione dei criteri contiene tutte le informazioni sui criteri specificate nei metadati di input per una determinata associazione, ma sono presenti informazioni che non possono essere rappresentate nei criteri, ma che richiedono l'input dell'utente quando si usano tali criteri per creare un proxy di servizio e/o un endpoint del servizio. Ad esempio, l'applicazione deve fornire le credenziali per l'autenticazione dell'intestazione HTTP.

L'applicazione deve compilare la struttura del modello, denominata WS \_ bindingTemplateType \_ binding \_ template per ogni tipo di modello di binding diverso, definito in WebServices. h:

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

L'elenco dei modelli di associazione di sicurezza è facoltativo a seconda dell'associazione di sicurezza corrispondente. Ad esempio, il campo [**modello di binding di sicurezza del trasporto di WS \_ SSL \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) viene presentato nel [**modello di associazione di WS \_ http \_ SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) per l'applicazione per fornire informazioni sul binding di sicurezza correlate a SSL, incluse le informazioni sulle credenziali.

L'applicazione deve compilare tutti i campi in questa struttura prima di chiamare le API del modello WebServices. Le proprietà di sicurezza aggiuntive, nonché le proprietà di associazione di sicurezza che non possono essere rappresentate nei criteri devono essere compilate e le API WebServices uniscono i due set di proprietà in fase di esecuzione. È possibile azzerare i campi se non sono applicabili. Ad esempio, securityProperties può essere azzerato se non sono necessarie proprietà di sicurezza aggiuntive.

Routine di supporto e dichiarazione della descrizione dei criteri nei file di intestazione

wsutil crea una routine di supporto per semplificare il supporto del livello del modello di servizio, in modo che l'applicazione possa creare più facilmente un proxy di servizio e un endpoint di servizio. La descrizione del criterio è esposta anche in modo che l'applicazione possa utilizzarle direttamente. Una routine della Guida CreateSerivceProxy è simile alla seguente:

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

Gli sviluppatori sono invitati a usare queste routine di supporto, anche se possono usare direttamente la routine di runtime sottostante fornita da webservices.dll. Gli sviluppatori non sono invitati a usare direttamente le descrizioni dei criteri durante la programmazione con il livello del [modello di servizio](service-model-layer-overview.md) .

I riferimenti alla descrizione dei criteri vengono generati anche nell'intestazione per utenti avanzati. Se gli sviluppatori non utilizzano le funzionalità del modello di servizio, possono utilizzare direttamente le descrizioni dei criteri.

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

Prototipi delle definizioni nei file stub

Una singola struttura di descrizione dei criteri per binding e le descrizioni Helper a cui viene fatto riferimento internamente vengono create nella struttura del prototipo locale. Le descrizioni dei criteri vengono generate nel file in cui viene generata la [**\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) . In genere, gli sviluppatori non devono esaminare il file stub durante lo sviluppo, ma il file stub contiene tutti i dettagli sulle specifiche dei criteri.

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

Implementazione delle routine di supporto nei file stub

Wsutil genera routine di supporto per semplificare le chiamate dell'applicazione a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) e la creazione di [**endpoint di WS \_ Service \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) in base alle informazioni fornite nelle impostazioni dei criteri.

Dipende dai vincoli di binding specificati per la porta specificata, il primo argomento è diverso in base alla struttura del modello. Nell'esempio seguente si presuppone il trasporto HTTP, la firma per la creazione del proxy di servizio è simile a un parametro di tipo di canale aggiuntivo.

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

Nella tabella seguente sono elencati tutti i tipi di modello di associazione supportati, le associazioni di sicurezza corrispondenti necessarie nel tipo, la struttura del modello da compilare per applicazione per il tipo e il tipo di descrizione corrispondente. L'applicazione deve compilare la struttura del modello, mentre lo sviluppatore di applicazioni deve comprendere quali sono le associazioni di sicurezza necessarie per i criteri specificati.



| [**\_tipo di \_ modello di binding WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | Combinazioni di associazioni di sicurezza                                                                                                                                                                                                                                                                                                               | struttura del modello da compilare per applicazione                                                                                            | Descrizione dei criteri                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo di \_ modello di associazione WS http \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**\_modello di \_ associazione WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**\_Descrizione dei \_ criteri WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**\_tipo di \_ \_ modello di associazione SSL HTTP \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_binding di \_ sicurezza del trasporto \_ \_ di WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**\_modello di \_ \_ associazione SSL http ws \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**Descrizione dei criteri di WS \_ http \_ SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**\_tipo di \_ \_ modello di binding di autenticazione dell'intestazione \_ http \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**\_binding di \_ sicurezza di autenticazione dell'intestazione WS http \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**\_modello di \_ \_ binding di autenticazione dell'intestazione HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**\_Descrizione dei \_ criteri di autenticazione dell'intestazione WS http \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**\_tipo di \_ \_ modello di \_ binding di autenticazione dell'intestazione WS \_ \_ http SSL \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**WS \_ Binding \_ di \_ sicurezza \_ del trasporto SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e [ **binding di sicurezza di \_ autenticazione dell' \_ intestazione \_ \_ \_ http ws**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**\_modello di \_ \_ binding di \_ autenticazione dell'intestazione \_ \_ WS HTTP SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**\_Descrizione dei \_ \_ criteri di \_ autenticazione dell'intestazione \_ \_ WS HTTP SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**\_tipo di \_ \_ modello di binding del nome utente SSL HTTP \_ \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ Binding \_ di \_ sicurezza \_ del trasporto SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e [ **associazione di sicurezza dei \_ \_ messaggi \_ \_ WS nomeutente**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**\_modello di \_ \_ binding del nome utente SSL HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**\_ \_ \_ Descrizione criterio nome utente \_ SSL \_ http ws**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**\_tipo di \_ \_ modello di \_ \_ Binding APREQ \_ \_ di WS HTTP SSL Kerberos**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ Binding \_ di \_ sicurezza \_ del trasporto SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e [ **associazione di sicurezza del \_ messaggio WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**\_modello di \_ \_ \_ \_ Binding APREQ \_ di WS HTTP SSL Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**\_Descrizione del \_ \_ \_ \_ criterio APREQ \_ di WS HTTP SSL Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**\_tipo di \_ modello di associazione WS TCP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**\_modello di \_ associazione WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**\_Descrizione dei \_ criteri WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**\_tipo di \_ \_ modello di binding SSPI WS TCP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_binding di \_ \_ sicurezza del trasporto SSPI \_ \_ di WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**\_modello di \_ \_ binding SSPI WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**\_Descrizione del \_ \_ criterio SSPI WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**\_tipo di \_ \_ modello di \_ Binding nome utente \_ WS TCP SSPI \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ Binding \_ di \_ \_ \_ sicurezza del trasporto SSPI TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e [ **\_ \_ \_ \_ associazione di sicurezza dei messaggi WS nomeutente**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**\_modello di \_ \_ Binding nome \_ utente \_ di WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**\_Descrizione del \_ \_ criterio nomeutente \_ \_ di WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**\_tipo di \_ \_ modello di \_ \_ Binding APREQ \_ \_ di WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ Binding di sicurezza del \_ \_ trasporto \_ \_ SSPI TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e [ **\_ associazione di sicurezza del messaggio WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**\_modello di \_ \_ \_ \_ Binding APREQ \_ di WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**\_Descrizione del \_ \_ \_ \_ criterio APREQ \_ WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**\_tipo di \_ \_ modello di \_ \_ binding del contesto di sicurezza \_ \_ WS HTTP SSL nomeutente \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ Binding di sicurezza del \_ trasporto \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e binding di sicurezza del [**\_ messaggio del \_ contesto \_ \_ \_ di sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS \_ nome utente \_ \_ \_ associazione di sicurezza messaggi**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) nel canale bootstrap                         | [**\_modello di \_ \_ associazione del \_ contesto di sicurezza del nome utente SSL \_ \_ http ws \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**\_Descrizione del criterio del contesto di sicurezza WS http \_ SSL \_ nomeutente \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**\_tipo di \_ \_ modello di \_ \_ associazione del \_ contesto di sicurezza \_ \_ \_ WS HTTP SSL APREQ**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ Binding di sicurezza del \_ trasporto \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e associazione di sicurezza del [**\_ messaggio del \_ contesto \_ \_ \_ di sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS \_ Kerberos \_ APREQ \_ \_ \_ associazione di sicurezza dei messaggi**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) nel canale bootstrap            | [**\_modello di associazione del contesto di sicurezza WS http \_ SSL \_ \_ APREQ Kerberos \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**\_Descrizione dei criteri di contesto di sicurezza WS http \_ SSL \_ \_ APREQ Kerberos \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**\_tipo di \_ \_ modello di \_ \_ associazione del contesto di sicurezza \_ \_ del nome utente di \_ WS TCP SSPI**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ Binding di sicurezza del \_ \_ trasporto \_ \_ SSPI TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e binding di sicurezza del [**messaggio del contesto di sicurezza di WS \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**binding di \_ sicurezza del \_ messaggio \_ \_ WS nomeutente**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) nel canale bootstrap              | [**\_modello di \_ \_ associazione del \_ contesto di sicurezza del nome utente \_ \_ di WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**\_Descrizione del criterio del contesto di sicurezza WS TCP \_ SSPI \_ nomeutente \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**\_tipo di \_ modello di binding del contesto di sicurezza WS TCP SSPI \_ Kerberos \_ APREQ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ Binding di sicurezza del \_ \_ trasporto SSPI \_ \_ TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e associazione di sicurezza del [**\_ messaggio del \_ contesto \_ \_ \_ di sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) con [**WS \_ Kerberos APREQ il binding di \_ \_ \_ sicurezza \_ dei messaggi**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) nel canale bootstrap | [**\_modello di \_ \_ associazione del \_ \_ contesto di sicurezza APREQ \_ \_ \_ di WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**\_Descrizione dei \_ \_ criteri di \_ \_ contesto di sicurezza APREQ \_ \_ \_ WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

Ad esempio, [**il \_ \_ tipo di \_ \_ modello di \_ binding SSL di WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) indica che i criteri di input per l'associazione specificano il trasporto HTTP e il binding di [**sicurezza del trasporto di WS \_ SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). L'applicazione deve compilare la struttura del [**\_ modello di associazione WS http \_ \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) prima di chiamare le routine di supporto e la descrizione dei criteri di corrispondenza è [**WS \_ http \_ SSL \_ policy \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description). In particolare, la sezione Binding in WSDL contiene i segmenti seguenti:

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

Nel [contesto di sicurezza](security-context.md), il canale bootstrap viene creato per stabilire la conversazione sicura nel canale del servizio. Wsutil supporta solo lo scenario in cui il canale bootstrap è lo stesso del canale del servizio, con le stesse proprietà del canale e le stesse proprietà di sicurezza. La sicurezza del trasporto è necessaria per l'associazione dei messaggi del contesto di sicurezza. wsutil supporta i canali bootstrap con altre associazioni di sicurezza dei messaggi, ma supporta solo il contesto di sicurezza come unico binding di sicurezza del messaggio nel canale del servizio, senza combinazione con altre associazioni di sicurezza dei messaggi. Gli sviluppatori possono supportare tali combinazioni al di fuori del supporto dei modelli di criteri.

L'enumerazione seguente fa parte del supporto dei criteri:

-   [**\_tipo di \_ modello di binding WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

Le funzioni seguenti fanno parte del supporto dei criteri:

-   [**WsCreateServiceEndpointFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**WsCreateServiceProxyFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

Le strutture seguenti fanno parte del supporto dei criteri:

-   [**\_modello di \_ associazione WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**\_modello di \_ \_ binding di autenticazione dell'intestazione HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**\_Descrizione dei \_ criteri di autenticazione dell'intestazione WS http \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**\_Descrizione dei \_ \_ criteri di \_ \_ associazione di \_ sicurezza \_ dell'intestazione WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**\_modello di \_ \_ associazione di \_ sicurezza \_ \_ per l'autenticazione dell'intestazione WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**\_Descrizione dei \_ criteri WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**\_modello di \_ \_ associazione SSL http ws \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**\_modello di \_ \_ binding di \_ autenticazione dell'intestazione \_ \_ WS HTTP SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**\_Descrizione dei \_ \_ criteri di \_ autenticazione dell'intestazione \_ \_ WS HTTP SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**\_modello di \_ \_ \_ \_ Binding APREQ \_ di WS HTTP SSL Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**\_Descrizione del \_ \_ \_ \_ criterio APREQ \_ di WS HTTP SSL Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**\_modello di associazione del contesto di sicurezza WS http \_ SSL \_ \_ APREQ Kerberos \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**\_Descrizione dei criteri di contesto di sicurezza WS http \_ SSL \_ \_ APREQ Kerberos \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**Descrizione dei criteri di WS \_ http \_ SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**\_modello di \_ \_ binding del nome utente SSL HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**\_ \_ \_ Descrizione criterio nome utente \_ SSL \_ http ws**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**\_modello di \_ \_ associazione del \_ contesto di sicurezza del nome utente SSL \_ \_ http ws \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**\_Descrizione del criterio del contesto di sicurezza WS http \_ SSL \_ nomeutente \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**\_Descrizione dei \_ \_ criteri di \_ associazione di sicurezza del messaggio WS \_ \_ Kerberos APREQ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**\_modello di \_ \_ associazione di \_ sicurezza del messaggio \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**\_Descrizione dei \_ \_ criteri di \_ associazione di sicurezza del messaggio del \_ \_ contesto di \_ sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**\_modello di \_ \_ associazione di sicurezza del messaggio del contesto \_ di \_ sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**\_Descrizione dei \_ \_ criteri di associazione di sicurezza del contesto \_ di \_ sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**\_modello di \_ associazione di sicurezza del contesto di sicurezza di \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**\_Descrizione dei \_ \_ criteri di associazione di sicurezza del trasporto \_ WS \_ SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**\_modello di \_ binding di sicurezza del trasporto \_ \_ di WS SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**\_Descrizione dei \_ \_ criteri di associazione di sicurezza del trasporto \_ di \_ WS SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**\_modello di \_ associazione WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**\_Descrizione dei \_ criteri WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**\_modello di \_ \_ binding SSPI WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**\_modello di \_ \_ \_ \_ Binding APREQ \_ di WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**\_Descrizione del \_ \_ \_ \_ criterio APREQ \_ WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**\_modello di \_ \_ associazione del \_ \_ contesto di sicurezza APREQ \_ \_ \_ di WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**\_Descrizione dei \_ \_ criteri di \_ \_ contesto di sicurezza APREQ \_ \_ \_ WS TCP SSPI Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**\_Descrizione del \_ \_ criterio SSPI WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**\_modello di \_ \_ associazione di sicurezza del trasporto SSPI \_ \_ di WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**\_modello di \_ \_ Binding nome \_ utente \_ di WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**\_Descrizione del \_ \_ criterio nomeutente \_ \_ di WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**\_modello di \_ \_ associazione del \_ contesto di sicurezza del nome utente \_ \_ di WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**\_Descrizione del criterio del contesto di sicurezza WS TCP \_ SSPI \_ nomeutente \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**\_Descrizione dei \_ \_ criteri di associazione di sicurezza del messaggio \_ WS \_ nomeutente \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**\_modello di \_ associazione di sicurezza del messaggio WS nomeutente \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




