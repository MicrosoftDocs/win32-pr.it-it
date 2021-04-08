---
title: WSDL e contratti di servizio
description: L'utilità Wsutil.exe genera uno stub del linguaggio C in base ai metadati WSDL specificati, nonché le definizioni e le descrizioni dei tipi di dati per i tipi di dati descritti dagli schemi XML creati dall'utente.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- Supporto WSDL
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19661e487c1a0dde871333376336bede239f9825
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734839"
---
# <a name="wsdl-and-service-contracts"></a>WSDL e contratti di servizio

L'utilità [Wsutil.exe](web-service-compiler-tool.md) genera uno stub del linguaggio C in base ai metadati WSDL specificati, nonché le definizioni e le descrizioni dei tipi di dati per i tipi di dati descritti dagli schemi XML creati dall'utente.


Di seguito è riportato un documento WSDL di esempio e XML Schema che funge da base per la discussione seguente:

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:int" />
      <xs:element name="b" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:int" />
      <xs:element name="c" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

In questo esempio viene fornito un contratto, ISimpleService, con un solo metodo, SimpleMethod. "SimpleMethod" ha due parametri di input di tipo **Integer**, *a* e *b*, che vengono inviati dal client al servizio. Analogamente, SimpleMethod ha due parametri di output di tipo **Integer**, *b* e *c*, che vengono restituiti al client al termine del completamento. Nella sintassi C con annotazioni SAL la definizione del metodo viene visualizzata come segue:

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

In questa definizione, ISimpleService è un contratto di servizio con una singola operazione di servizio: SimpleMethod.

Il file di intestazione di output contiene definizioni e descrizioni per riferimento esterno. ad esempio:

-   Definizioni della struttura C per i tipi di elemento globali.
-   Un prototipo di operazione come definito nel file corrente.
-   Prototipo di tabella di funzione per i contratti specificati nel file WSDL.
-   Prototipi del proxy client e dello stub del servizio per tutte le funzioni specificate nel file corrente.
-   Struttura di dati di [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) per gli elementi dello schema globale definiti nel file corrente.
-   Struttura dei dati [**WS \_ message \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) per tutti i messaggi specificati nel file corrente.
-   Struttura di dati [**WS \_ Contract \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) per tutti i contratti specificati nel file corrente.

Viene generata una struttura globale per incapsulare tutte le descrizioni globali per i tipi di schema e i tipi di modello di servizio a cui l'applicazione può fare riferimento. La struttura viene denominata utilizzando un nome di file normalizzato. In questo esempio Wsutil.exe genera una struttura di definizioni globali denominata "example \_ WSDL" che contiene tutte le descrizioni dei servizi Web. La definizione della struttura viene generata nel file stub.

``` syntax
typedef struct _example_wsdl
{
  struct {
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    WS_ELEMENT_DESCRIPTION SimpleMethodResponse;
  } elements;
  struct {
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
  } messages;
  struct {
    WS_CONTRACT_DESCRIPTION DefaultBinding_ISimpleService;
  } contracts;
} _example_wsdl;

extern const _stockquote_wsdl stockquote_wsdl;
```

Per le definizioni di elementi globali nel documento di XML Schema (XSD), viene generato un prototipo di [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , oltre alla definizione del tipo C corrispondente, per ogni elemento. I prototipi per le descrizioni degli elementi per SimpleMethod e SimpleMethodResponse vengono generati come membri nella struttura precedente. Le strutture C vengono generate nel modo seguente:

``` syntax
typedef struct SimpleMethod
{
  int   a;
  int   b;
} SimpleMethod;

typedef struct SimpleMethodResponse
{
  int   b;
  int   c;
} SimpleMethodResponse;
```

Analogamente, per i tipi complessi globali, Wsutil.exe genera definizioni di struttura di tipo C come sopra, senza le descrizioni degli elementi corrispondenti.

Per l'input WSDL, Wsutil.exe genera le definizioni e i prototipi seguenti:

-   Per la descrizione del messaggio viene generato un prototipo [**WS \_ message \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) . Questa descrizione può essere utilizzata dal modello del servizio e dal livello del messaggio. Le strutture di descrizione del messaggio sono campi denominati "MessageName" nella struttura globale. In questo esempio la descrizione del messaggio viene generata come campo ISimpleService \_ SimpleMethod \_ InputMessage nella \_ struttura ISimpleService SimpleMethod \_ InputMessage, come specificato nel file WSDL.
-   [**WS \_ Il \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototipo della descrizione del contratto viene generato per la descrizione del contratto. Questa descrizione viene utilizzata dal modello di servizio. Le strutture di descrizione del contratto sono campi denominati "ContractName" nella struttura globale. In questo esempio la descrizione del contratto viene generata come \_ campo Default ISimpleService nella struttura " \_ example \_ WSDL".

Le specifiche delle operazioni e dei tipi sono comuni sia al proxy che allo stub e vengono generate in entrambi i file. Wsutil.exe genera una copia solo se il proxy e lo stub vengono generati nello stesso file.

## <a name="identifier-generation"></a>Generazione di identificatori

Le strutture C generate automaticamente sopra elencate vengono create in base al nome specificato nel file WSDL. Un NCName XML non è comunemente considerato un identificatore C valido e i nomi vengono normalizzati in base alle esigenze. I valori esadecimali non vengono convertiti e le lettere comuni come ':','/' è .' vengono convertite nel carattere di sottolineatura ' \_ ' per migliorare la leggibilità.

## <a name="header-for-the-stub"></a>Intestazione per lo stub

Per ogni operazione nel contratto di servizio, viene generata una routine di callback denominata " <operationname> callback". Ad esempio, l'operazione "SimpleMethod" nel contratto di servizio di esempio ha un callback generato denominato "SimpleMethodCallback".

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

Per ogni **PORTTYPE** WSDL Wsutil.exe genera una tabella di funzioni che rappresenta **portType**. Ogni operazione su **portType** dispone di un puntatore a funzione corrispondente al callback presente nella tabella function.

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

I prototipi proxy vengono generati per tutte le operazioni. Il nome del prototipo è il nome dell'operazione (in questo caso, "SimpleMethod") specificato nel file WSDL per il contratto di servizio.

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a>Generazione del prototipo di descrizione solo locale

I file andstub del proxy contengono la definizione per la struttura delle definizioni globali, inclusi i prototipi e le definizioni per le strutture contenenti le descrizioni solo locali e le implementazioni del proxy client/servizio dello stub del servizio.

Tutti i prototipi e le definizioni locali per il file stub vengono generati come parte di una struttura di incapsulamento. Questa struttura di descrizione locale che include una chiara gerarchia delle descrizioni richieste dal livello di serializzazione e dal modello del servizio. La struttura di descrizione locale presenta prototipi simili a quelli illustrati di seguito:

``` syntax
struct _filenameLocalDefinitions
{
  struct {
  // schema related output for all the embedded 
  // descriptions that needs to describe global complex types.
  } globalTypes;
  // global elements.
  struct {
  // schema related output, like field description
  // structure description, element description etc.
  ...
  } globalElements;
  struct {
  // messages and related descriptions
  } messages;
  struct {
  // contract and related descriptions.
  } contracts;
  struct {
  // XML dictionary entries.
  } dictionary;
} _filenameLocalDefinitions;
```

## <a name="referencing-definitions-from-other-files"></a>Riferimento a definizioni da altri file

Le definizioni locali possono fare riferimento a descrizioni generate in un altro file. Il messaggio, ad esempio, può essere definito nel file di codice C generato dal file WSDL, ma l'elemento Message può essere definito altrove nel file di codice C generato dal file XSD. In questo caso, Wsutil.exe genera un riferimento all'elemento globale dal file che contiene la definizione del messaggio, come illustrato di seguito:

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a>Descrizioni degli elementi globali

Per ogni elemento globale definito in un file WSDL: Type o XSD, esiste un campo corrispondente denominato **ElementName** nel campo **globalelement** . In questo esempio viene generata una struttura denominata SimpleMethod:

``` syntax
typedef struct _SimpleServiceLocal
{
  struct  // global elements
  {
    struct // SimpleMethod
    {
    ...
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    ...
  } globalElements;
}
```

Altre descrizioni richieste dalla descrizione dell'elemento vengono generate come parte della struttura che lo contiene. Se l'elemento è un elemento di tipo semplice, è presente un solo campo di [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) . Se il tipo di elemento è una struttura, tutti i campi correlati e le descrizioni della struttura vengono generati come parte della struttura dell'elemento. In questo esempio, l'elemento SimpleMethod è una struttura che contiene due campi, **a** e **b**. Wsutil.exe genera la struttura come segue:

``` syntax
...
struct // SimpleMethod
{
  struct // SimpleMethod structure
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

Le strutture incorporate e gli elementi incorporati vengono generati come sottostrutture in base alle esigenze.

## <a name="wsdl-related-definitions"></a>Definizioni correlate a WSDL

Wsutil.exe genera un campo sotto la sezione WSDL per ogni valore **portType** definito nel servizio WSDL: specificato.

``` syntax
...
struct { // WSDL
    struct { // portTypeName
        struct { // operationName
        } operationName;
    ...
    WS_OPERATION_DESCRIPTION* operations[numOperations];
    WS_CONTRACT_DESCRIPTION contractDesc;
    } portTypeName;
}
...
```

Wsutil.exe genera un campo f che contiene tutte le descrizioni necessarie per l'operazione, una matrice signle di puntatori a ognuna delle descrizioni delle operazioni per ogni metodo e una [**Descrizione del \_ contratto \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) per l'oggetto **portType** specificato.

Tutte le descrizioni richieste dalle operazioni vengono generate all'interno del campo **OperationName** nell'oggetto **portType** specificato. Sono inclusi il [**campo \_ \_ Description dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) e la sottostruttura per i parametri di input e di output. Analogamente, i campi di [**\_ \_ Descrizione del messaggio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) per il messaggio di input e il messaggio di output facoltativo vengono inclusi insieme a; [**WS \_ Campo elenco \_ Descrizione parametro**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) per tutti i parametri dell'operazione e il [**campo \_ \_ Descrizione operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) per l'operazione stessa. In questo esempio, la struttura del codice per la descrizione di SimpleMethod viene generata come illustrato di seguito:

``` syntax
...
struct // messages
{
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
} messages;
struct // contracts
{
  struct // DefaultBinding_ISimpleService
  {
    struct // SimpleMethod
    {
      WS_PARAMETER_DESCRIPTION params[3];
      WS_OPERATION_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    WS_OPERATION_DESCRIPTION* operations[1];
    WS_CONTRACT_DESCRIPTION contractDesc;
  } DefaultBinding_ISimpleService;
} contracts;
...
```

## <a name="xml-dictionary-related-definitions"></a>Definizioni correlate ai dizionari XML

I nomi e gli spazi dei nomi utilizzati in diverse descrizioni vengono generati come campi di tipo [**\_ \_ stringa WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string). Tutte queste stringhe vengono generate come parte di un dizionario di costanti per file. L'elenco di stringhe e il campo del [**\_ \_ dizionario di WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (denominato **dict** nell'esempio riportato di seguito) vengono generati come parte del campo Dictionary della struttura **fileNameLocal** .

``` syntax
struct { // fileNameLocal
...
  struct { // dictionary
    struct { // XML string list
      WS_XML_STRING firstFieldName;
      WS_XML_STRING firstFieldNS;
      ...
    } xmlStrings;
  WS_XML_DICTIONARY dict;
  } dictionary;
}; // fileNameLocal;
```

La matrice di [**\_ \_ stringhe WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)viene generata come una serie di campi di tipo **stringa WS \_ XML \_**, denominata con nomi descrittivi. Lo stub generato usa i nomi descrittivi in diverse descrizioni per migliorare la leggibilità.

Proxy client per le operazioni WSDL

Wsutil.exe genera un proxy client per tutte le operazioni. Le applicazioni possono sovrascrivere la firma del metodo usando un'opzione della riga di comando prefix.

``` syntax
HRESULT WINAPI bindingName_SimpleMethod(WS_SERVICE_PROXY *serviceProxy,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_CALL_PROPERTY* callProperties,
  ULONG callPropertyCount,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error )
{
  void* argList[] = {&a, &b, &c};
  return WsCall(_serviceProxy,
    (WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
    (void **)&_argList,
    callProperties,
    callPropertyCount,
    heap,
    asyncContext,
    error
  );      
}
```

Il chiamante dell'operazione deve passare un parametro dell' *heap* valido. I parametri di output vengono allocati usando il \_ valore dell'heap WS specificato nel parametro dell' *heap* . La funzione chiamante può reimpostare o liberare l'heap per rilasciare la memoria per tutti i parametri di output. Se l'operazione ha esito negativo, è possibile recuperare informazioni aggiuntive sull'errore di dettaglio dall'oggetto facoltativo error se disponibile.

Wsutil.exe genera uno stub del servizio per tutte le operazioni descritte nell'associazione.

``` syntax
HRESULT CALLBACK ISimpleService_SimpleMethodStub(
  const WS_OPERATION_CONTEXT *context,
  void * stackStruct,
  void * callback,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR *error )
{
  SimpleMethodParamStruct *pstack = (SimpleMethodParamStruct *) stackstruct;
  SimpleMethodOperation operation = (SimpleMethodOperation)callback;
  return operation(context, pstack->a, &(pstack->b), &(pstack->c ), asyncContext, error );
}
```

Nella sezione precedente viene descritto il prototipo della struttura locale contenente tutte le definizioni locali solo per il file stub. Nelle sezioni successive vengono descritte le definizioni delle descrizioni.

## <a name="wsdl-definition-generation"></a>Generazione definizione WSDL

Wsutil.exe genera una struttura costante statica (**const static**) denominata *<\_ nome file>* LocalDefinitions di tipo *<\_ nome servizio>* locale che contiene tutte le definizioni solo locali.

``` syntax
const static _SimpleServiceLocal example_wsdlLocalDefinitions =
{
  {  // global types
  ...
  }, // global types
  {  // global elements
  ...
  }, // global elements
  {  // messages
  ...
  }, //messages
  ...
  {  // dictionary
  ...
  }, // dictionary
},
```

Sono supportate le seguenti descrizioni WSDL:

-   WSDL: servizio
-   WSDL: binding
-   WSDL: portType
-   WSDL: Operation
-   WSDL: Message

## <a name="processing-wsdloperation-and-wsdlmessage"></a>Elaborazione di WSDL: Operation e WSDL: Message

Ogni operazione specificata nel documento WSDL viene mappata a un'operazione del servizio da [Wsutil.exe](web-service-compiler-tool.md). Lo strumento genera definizioni separate delle operazioni del servizio sia per il server che per il client.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

Il layout degli elementi dati del messaggio andOutput di input viene valutato dallo strumento per generare i metadati di serializzazione per l'infrastruttura insieme alla firma effettiva dell'operazione di servizio risultante a cui sono associati i messaggi di input e di output.

I metadati per ogni operazione all'interno di un **portType** specifico hanno un input e, facoltativamente, un messaggio di output, ognuno di questi messaggi viene mappato a una [**\_ \_ Descrizione del messaggio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description). In questo esempio, l'input e il messaggio di output sull'operazione nell'oggetto portType mappato a inputMessageDescription e facoltativamente outputMessageDescription nella [**Descrizione dell' \_ operazione \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) rispettivamente.

Per ogni messaggio WSDL lo strumento genera [**la \_ \_ Descrizione del messaggio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) che fa riferimento alla definizione della [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , come illustrato di seguito:

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

La descrizione del messaggio si riferisce alla descrizione dell'elemento di input. Poiché l'elemento è definito globalmente, la descrizione del messaggio fa riferimento alla definizione globale anziché all'elemento statico locale. Analogamente, se l'elemento è definito in un altro file, Wsutil.exe genera un riferimento alla struttura definita globalmente in tale file. Se, ad esempio, SimpleMethodResponse è definito in un altro file XSD di esempio, Wsutil.exe genera invece quanto segue:

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Ogni descrizione del messaggio contiene l'azione e la descrizione dell'elemento specifico (un campo di tipo [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) per tutti gli elementi dati del messaggio. Nel caso di un messaggio di tipo RPC o di un messaggio con più parti, viene creato un elemento wrapper per incapsulare le informazioni aggiuntive.

## <a name="rpc-style-support"></a>Supporto dello stile RPC

Wsutil.exe supporta operazioni di tipo Document e RPC in base all'estensione di binding WSDL 1,1 per la specifica SOAP 1,2. Le operazioni RPC e di tipo letterale sono contrassegnate \_ come \_ operazione WS RPC Literal \_ . Il modello di servizio ignora il nome dell'elemento wrapper del corpo della risposta nelle operazioni RPC/Literal.

Wsutil.exe non supporta in modo nativo operazioni di tipo codifica. Il \_ parametro del buffer WS XML \_ viene generato per i messaggi di codifica e gli sviluppatori devono popolare direttamente il buffer opaco.

## <a name="multiple-message-parts-support"></a>Supporto per più parti del messaggio

Wsutil.exe supporta più parti del messaggio in un messaggio. Un messaggio multiparte può essere specificato come indicato di seguito:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_MutipleParts_InputMessage">
  <wsdl:part name="part1" element="tns:SimpleElement1" />
  <wsdl:part name="part2" element="tns:SimpleElement2" />
 </wsdl:message>
</wsdl:definitions>
```

Wsutil.exe genera un campo di [**\_ \_ tipo struct WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) per l'elemento Message se il messaggio contiene più parti. Se il messaggio viene rappresentato utilizzando lo stile del documento, Wsutil.exe genera un elemento wrapper con tipo struct. L'elemento wrapper non ha un nome o uno spazio dei nomi specifico e la struttura wrapper contiene tutti gli elementi in tutte le parti come campi. L'elemento wrapper è solo per uso interno e non verrà serializzato nel corpo del messaggio.

Se il messaggio utilizza la rappresentazione di stile RPC o Literal, Wsutil.exe crea un elemento wrapper con il nome dell'operazione come nome dell'elemento e lo spazio dei nomi specificato come spazio dei nomi del servizio in base alla specifica dell'estensione SOAP WSDL. La struttura dell'elemento contiene una matrice di campi che rappresentano i tipi specificati nelle parti del messaggio. L'elemento wrapper viene mappato all'elemento superiore effettivo nel corpo del messaggio, come indicato nella specifica SOAP.

Sul lato server, ogni operazione genera un typedef dell'operazione del servizio server risultante. Questo typedef viene usato per fare riferimento all'operazione nella tabella Function come descritto in precedenza. Ogni operazione comporta inoltre la generazione di una funzione stub che nfrastructure chiamate per conto del delegato al metodo effettivo.

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error
  );
```

Per l'operazione SimpleMethod, il typedef SimpleMethodOperation è definito sopra. Si noti che il metodo generato presenta un argomento espanso listwith la parte del messaggio per il messaggio di input e di output per l'operazione SimpleMethod come parametri denominati.

Sul lato client viene eseguito il mapping di ogni operazione a un'operazione del servizio proxy.

``` syntax
HRESULT WINAPI SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  ws_heap *heap,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="processing-wsdlbinding"></a>Elaborazione di WSDL: binding

Il modello di servizio WWSAPI supporta l'estensione di binding II saponeho. Per ogni binding è presente un **portType** associato.

Il trasporto specificato nell'estensione di binding SOAP è solo consultivo. Quando si crea un canale, l'applicazione deve fornire informazioni sul trasporto. Attualmente sono supportate le associazioni WS \_ http \_ Binding e WS \_ TCP binding \_ .

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
</wsdl:definitions>
```

Nel documento WSDL di esempio è presente un solo **portType** per ISimpleService. L'associazione SOAP fornita indica il trasporto HTTP, specificato come \_ binding WS http \_ . Si noti che questa struttura non ha un effetto statico perché questa struttura deve essere disponibile per l'applicazione.

Elaborazione di WSDL: portType

Ogni **portType** in WSDL è costituito da una o più operazioni. L'operazione deve essere coerente con l'estensione di binding SOAP indicata in WSDL: binding.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   ...
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

In questo esempio, l'oggetto **portType** ISimpleService contiene solo l'operazione SimpleMethod. Questo comportamento è coerente con la sezione dell'associazione in cui è presente una sola operazione WSDL mappata a un'azione SOAP.

Poiché l'oggetto **portType** ISimpleService dispone solo di un'operazione--SimpleMethod, la tabella di funzioni corrispondente contiene solo SimpleMethod come operazione del servizio.

In termini di metadati, ogni **portType** viene mappato da Wsutil.exe a una [**\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description). Ogni operazione all'interno di **portType** viene mappata a una [**\_ \_ Descrizione dell'operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

In questo esempio **portType** lo strumento genera la [**\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) per ISimpleService. Questa descrizione del contratto contiene il numero specifico di operazioni disponibili nell' **portType** ISimpleService insieme a una matrice di [**\_ \_ Descrizione dell'operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) che rappresenta le singole operazioni definite nell'PortType per ISimpleService. Poiché è presente una sola operazione in ISimpleService portType for ISimpleService, è presente anche una sola definizione di **\_ \_ Descrizione dell'operazione WS** .

``` syntax
...  part of LocalDefinitions structure
{    // array of operations for DefaultBinding_ISimpleService
(WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
},    // array of operations for DefaultBinding_ISimpleService
{    // contract description for DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},  // end of contract description for DefaultBinding_ISimpleService
},    // DefaultBinding_ISimpleService       ...
```

## <a name="processing-wsdlservice"></a>Elaborazione di WSDL: Service

WsUtil.exe usa i servizi per trovare binding/PortTypes e genera la struttura del contratto che descrive i tipi, i messaggi, le definizioni PortType e così via. Le descrizioni dei contratti sono accessibili esternamente e vengono generate come parte della struttura di definizione globale specificata tramite l'intestazione generata.

WsUtil.exe supporta le estensioni EndpointReference definite in WSDL: Port. Il riferimento all'endpoint è definito in WS-Addressing come modo per descrivere le informazioni sugli [endpoint](endpoint-address.md) di un servizio. Il testo dell'estensione di riferimento dell'endpoint di input salvato come [**\_ \_ stringa WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), insieme alla [**Descrizione dell' \_ \_ indirizzo \_ WS endpoint**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) corrispondente viene generato nella sezione endpointReferences della struttura globale.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
   <wsa:EndpointReference>
    <wsa:Address>http://example.org/wcfmetadata/WSHttpNon</wsa:Address>
   </wsa:EndpointReference> 
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

``` syntax
  const _example_wsdl example_wsdl =
  {
  ... // global element description
  {// messages
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
},    // message description for ISimpleService_SimpleMethod_InputMessage
{    // message description for ISimpleService_SimpleMethod_OutputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_OutputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodResponse,
},    // message description for ISimpleService_SimpleMethod_OutputMessage
}, // messages
{// contracts
{   // DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},    // end of DefaultBinding_ISimpleService
    }, // contracts
    {
        {
            {   // endpointAddressDescription
                WS_ADDRESSING_VERSION_0_9,
            },                    
            (WS_XML_STRING*)&xml_string_generated_in_stub // endpointReferenceString
        }, //DefaultBinding_ISimpleService
    }, // endpointReferences
}
```

Per creare [**l' \_ \_ indirizzo dell'endpoint WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) usando i metadati generati da WsUtil:

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

Le stringhe costanti nel proxy client o nello stub del servizio vengono generate come campi di tipo \_ stringa WS XML \_ ed è presente un dizionario costante per tutte le stringhe nel file di proxy o stub. Ogni stringa nel dizionario viene generata come campo nella parte del dizionario della struttura locale per una migliore leggibilità.

``` syntax
... // dictionary part of LocalDefinitions structure
{    // xmlStrings
  { // xmlStrings
    WS_XML_STRING_DICTIONARY_VALUE("a",&example_wsdlLocalDefinitions.dictionary.dict, 0), 
    WS_XML_STRING_DICTIONARY_VALUE("http://Sapphire.org",&example_wsdlLocalDefinitions.dictionary.dict, 1), 
    WS_XML_STRING_DICTIONARY_VALUE("b",&example_wsdlLocalDefinitions.dictionary.dict, 2), 
    WS_XML_STRING_DICTIONARY_VALUE("SimpleMethod",&example_wsdlLocalDefinitions.dictionary.dict, 3),
    ...
  },  // end of xmlStrings
  {   // SimpleServicedictionary
    // 45026280-d5dc-4570-8195-4d66d13bfa34
    { 0x45026280, 0xd5dc, 0x4570, { 0x81, 0x95, 0x4d,0x66, 0xd1, 0x3b, 0xfa, 0x34 } },
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings,
    stringCount,
    TRUE,
  },
}
...
```

## <a name="processing-wsdltype"></a>Elaborazione di WSDL: Type

Wsutil.exe supporta solo documenti XML Schema (XSD) nella specifica WSDL: Type. Un caso speciale è quando una porta del messaggio specifica una definizione di elemento globale. Vedere la sezione seguente per altri dettagli sull'euristica usata in questi casi.

## <a name="parameter-processing-heuristics"></a>Euristica di elaborazione dei parametri

Nel modello del servizio, viene eseguito il mapping dei messaggi WSDL a parametri specifici in un metodo. Wsutil.exe dispone di due stili di generazione del parametro: nel primo stile, l'operazione include un parametro per il messaggio di input e un parametro per il messaggio di output (se necessario); nel secondo stile, Wsutil.exe usa un approccio euristico per eseguire il mapping e l'espansione dei campi nelle strutture sia per i messaggi di input che per quelli di output a parametri diversi dell'operazione. I messaggi di input e di output devono avere elementi del messaggio di tipo struttura per generare questo secondo approccio.

Wsutil.exe usa le regole seguenti per la generazione di parametri dell'operazione dai messaggi di input e di output:

-   Per i messaggi di input e di output con più parti del messaggio, ogni parte del messaggio è un parametro separato nell'operazione con il nome della parte del messaggio come nome di parametro.
-   Per il messaggio di tipo RPC con una parte del messaggio, la parte del messaggio è un parametro dell'operazione, con il nome della parte del messaggio come nome di parametro.
-   Per i messaggi di input e di output di tipo documento con una parte del messaggio:
    -   Se il nome di una parte del messaggio è "Parameters" e il tipo di elemento è una struttura, ogni campo nella struttura viene considerato come un parametro separato con il nome del campo che corrisponde al nome del parametro.
    -   Se il nome della parte del messaggio non è "Parameters", il messaggio è un parametro dell'operazione con il nome del messaggio utilizzato come nome di parametro corrispondente.
-   Per il messaggio di input e output di stile del documento con l'elemento nillable, il messaggio viene mappato a un parametro, con il nome della parte del messaggio come nome di parametro. Viene aggiunto un ulteriore livello di riferimento indiretto per indicare che il puntatore può essere **null**.
-   Se un campo viene visualizzato solo nell'elemento del messaggio di input, il campo viene considerato come un \[ \] parametro in.
-   Se un campo viene visualizzato solo nell'elemento del messaggio di output, il campo viene considerato come un \[ \] parametro out.
-   Se è presente un campo con lo stesso nome e lo stesso tipo visualizzato sia nel messaggio di input che nel messaggio di output, il campo viene considerato come un \[ parametro in, out \] .

Per determinare la direzione dei parametri vengono usati gli strumenti seguenti:

-   Se un campo viene visualizzato solo nell'elemento input Message, il campo viene considerato come solo parametro.
-   Se un campo viene visualizzato solo nell'elemento del messaggio di output, il campo viene considerato solo come parametro out.
-   Se è presente un campo con lo stesso nome e lo stesso tipo visualizzato nel messaggio di input e di output, il campo viene considerato come un parametro in, out.

Wsutil.exe supporta solo gli elementi in sequenza. Rifiuta l'ordinamento non valido per quanto riguarda \[ i parametri in, out \] se Wsutil.exe non è in grado di combinare i parametri in e out in un unico elenco di parametri. I suffissi possono essere aggiunti ai nomi dei parametri per evitare conflitti di nomi.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

Wsutil.exe considera i campi in TNS: SimpleMethod e TNS: SimpleMethodResponse ato be Parameters, come illustrato nelle definizioni dei parametri seguenti:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:import namespace="http://Example.org" />
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:unsignedInt" />
      <xs:element name="b" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:unsignedInt" />
      <xs:element name="c" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
</wsdl:definitions>
```

Wsutil.exe espande l'elenco dei parametri dai campi nell'elenco precedente e genera la struttura **ParamStruct** nell'esempio di codice seguente. Il modello di servizio in fase di esecuzione può utilizzare questa struttura per passare argomenti agli stub client e server.

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

Questa struttura viene utilizzata solo per descrivere il stack frame sul lato client e server. Non viene apportata alcuna modifica alla descrizione del messaggio o alle descrizioni degli elementi a cui fa riferimento la descrizione del messaggio.

``` syntax
  // following are local definitions for the complex type
  { // field description for a
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, a),
  0,
  0,
  },    // end of field description for a
  { // field description for b
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.bLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, b),
  0,
  0,
  },    // end of field description for b
  {    // fields description for _SimpleMethod
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.a,
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.b,
  },
  {  // structure definition
  sizeof(_SimpleMethod),
  __alignof(_SimpleMethod),
  (WS_FIELD_DESCRIPTION**)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields,
  WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields),
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  0,
  },   // struct description for _SimpleMethod
  // following are global definitions for the out parameter
  ...
  {  // element description
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_STRUCT_TYPE,
  (void *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.structDesc,
  },
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
  },    // message description for ISimpleService_SimpleMethod_InputMessage
```

Come regola generale, viene aggiunto un livello di riferimento indiretto per tutti i \[ parametri out \] e \[ in out \] .

## <a name="parameterless-operation"></a>Operazione senza parametri

Per le operazioni di documenti e valori letterali, Wsutil.exe considera l'operazione come un parametro di input e un parametro di output se:

-   Il messaggio di input o di output ha più di una parte.
-   Esiste solo una parte del messaggio e il nome della parte del messaggio non è "Parameters".

.. Nell'esempio precedente, supponendo che le parti del messaggio siano denominate *Paramin*"e *param* out, la firma del metodo diventa il codice seguente:

``` syntax
typedef struct SimpleMethod{
unsigned int a;
unsigned int b;
};

typedef struct SimpleMethodResponse {
unsigned int b;
unsigned int c;
};

typedef  struct ISimpleService_SimpleMethodParamStruct
{
SimpleMethod  * SimpleMethod;
SimpleMethodResponse  * SimpleMethodResponse;
} ISimpleService_SimpleMethodParamStruct;
```

Wsutil.exe genera una firma di versione per la descrizione dell'operazione in modo che il motore del modello di servizio WsCall e lato server possa verificare se la descrizione generata è applicabile per la piattaforma corrente.

Queste informazioni sulla versione vengono generate come parte della struttura della [**\_ \_ Descrizione dell'operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) . Il numero di versione può essere considerato come un selettore ARM Unione per rendere estendibile la struttura. Attualmente, il **VersionId** è impostato su TO1 senza campi successivi. I versiosn futuri possono incrementare il numero di versione e includere più campi in base alle esigenze. Ad esempio, Wsutil.exe genera attualmente il codice seguente in base all'ID versione:

``` syntax
{ // SimpleMethod
{ // parameter descriptions for SimpleMethod
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)0, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)1, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)-1, (USHORT)1 },
},    // parameter descriptions for SimpleMethod
{    // operation description for SimpleMethod
1,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_InputMessage,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_OutputMessage,
3,
(WS_PARAMETER_DESCRIPTION*)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.params,
SimpleMethodOperationStub
}, //operation description for SimpleMethod
},  // SimpleMethod
```

In futuro, potrebbe essere espansa come indicato di seguito:

``` syntax
WS_OPERATION_DESCRIPTION simpleMethodOperationDesc =
{
  2,
  &ISimpleService_SimpleMethod_InputputMessageDesc,
  &ISimpleService_SimpleMethod_OutputMessageDesc,
  WsCountOf(SimpleMethodParameters),
  SimpleMethodParameters,
  ISimpleService_SimpleMethod_Stub,
  &forwardToString;   // just as an example.
};
```

## <a name="security"></a>Sicurezza

Vedere la sezione sicurezza nell'argomento [dello strumento del compilatore WSUTIL](wsutil-compiler-tool.md) .

 

 




