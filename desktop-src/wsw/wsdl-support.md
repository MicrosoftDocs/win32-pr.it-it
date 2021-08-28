---
title: WSDL e contratti di servizio
description: L'utilità Wsutil.exe genera uno stub del linguaggio C in base ai metadati WSDL forniti, nonché le definizioni dei tipi di dati e le descrizioni per i tipi di dati descritti da XML Schema creati dall'utente.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- Supporto WSDL
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b273bd97d30aca185f35f31d385e6ab5a0bef4e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882283"
---
# <a name="wsdl-and-service-contracts"></a>WSDL e contratti di servizio

[L'utilitàWsutil.exe](web-service-compiler-tool.md) genera uno stub del linguaggio C in base ai metadati WSDL forniti, nonché le definizioni e le descrizioni dei tipi di dati per i tipi di dati descritti da XML Schema creati dall'utente.


Di seguito è riportato un documento WSDL di esempio e uno schema XML che funge da base per la discussione seguente:

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

Questo esempio fornisce un contratto, ISimpleService, con un singolo metodo, SimpleMethod. "SimpleMethod" ha due parametri di input di tipo **integer,** *a* *e b,* che vengono inviati dal client al servizio. Analogamente, SimpleMethod ha due parametri di output di tipo **integer**, *b* *e c*, che vengono restituiti al client dopo il completamento. Nella sintassi C con annotazioni SAL la definizione del metodo è la seguente:

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

In questa definizione, ISimpleService è un contratto di servizio con una singola operazione del servizio: SimpleMethod.

Il file di intestazione di output contiene definizioni e descrizioni per riferimento esterno. ad esempio:

-   Definizioni di struttura C per i tipi di elemento globali.
-   Prototipo di operazione definito nel file corrente.
-   Prototipo di tabella di funzioni per i contratti specificati nel file WSDL.
-   Prototipi di proxy client e stub del servizio per tutte le funzioni specificate nel file corrente.
-   Struttura [**di dati WS ELEMENT \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) per gli elementi dello schema globale definiti nel file corrente.
-   Struttura [**di dati WS MESSAGE \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) per tutti i messaggi specificati nel file corrente.
-   Struttura [**di dati WS CONTRACT \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) per tutti i contratti specificati nel file corrente.

Viene generata una struttura globale per incapsulare tutte le descrizioni globali per i tipi di schema e i tipi di modello di servizio a cui l'applicazione può fare riferimento. La struttura viene denominata usando un nome di file normalizzato. In questo esempio, Wsutil.exe una struttura di definizioni globali denominata "example \_ wsdl" che contiene tutte le descrizioni del servizio Web. La definizione della struttura viene generata nel file stub.

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

Per le definizioni di elementi globali nel documento XML Schema (XSD), per ogni elemento vengono generati un prototipo [**WS \_ ELEMENT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) e la definizione di tipo C corrispondente. I prototipi per le descrizioni degli elementi per SimpleMethod e SimpleMethodResponse vengono generati come membri nella struttura precedente. Le strutture C vengono generate come segue:

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

Analogamente per i tipi complessi globali, Wsutil.exe le definizioni di struttura C di tipo come sopra, senza descrizioni degli elementi corrispondenti.

Per l'input WSDL, Wsutil.exe genera i prototipi e le definizioni seguenti:

-   Per la descrizione del messaggio viene generato un prototipo [**WS \_ MESSAGE \_ DESCRIPTION.**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) Questa descrizione può essere utilizzata dal modello di servizio e dal livello messaggi. Le strutture di descrizione dei messaggi sono campi denominati "messagename" nella struttura globale. In questo esempio la descrizione del messaggio viene generata come campo ISimpleService SimpleMethod InputMessage nella struttura \_ \_ ISimpleService \_ SimpleMethod InputMessage come specificato nel \_ file WSDL.
-   [**WS \_ Il \_ prototipo CONTRACT DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) viene generato per la descrizione del contratto. Questa descrizione viene utilizzata dal modello di servizio. Le strutture di descrizione del contratto sono campi denominati "contractname" nella struttura globale. In questo esempio la descrizione del contratto viene generata come campo \_ DefaultBinding ISimpleService nella struttura \_ "example \_ wsdl".

Le specifiche di operazioni e tipi sono comuni sia al proxy che agli stub e vengono generate in entrambi i file. Wsutil.exe genera una copia solo se nello stesso file vengono generati sia il proxy che lo stub.

## <a name="identifier-generation"></a>Generazione di identificatori

Le strutture C rigenerate automaticamente elencate in precedenza vengono create in base al nome specificato nel file WSDL. Un NCName XML non viene in genere considerato un identificatore C valido e i nomi vengono normalizzati in base alle esigenze. I valori esadecimali non vengono convertiti e le lettere comuni come ':', '/' e '.' vengono convertite nel carattere di sottolineatura '' per migliorare \_ la leggibilità.

## <a name="header-for-the-stub"></a>Intestazione per lo stub

Per ogni operazione nel contratto di servizio, viene generata una routine di callback denominata &lt; "operationname &gt; Callback". Ad esempio, l'operazione "SimpleMethod" nel contratto di servizio di esempio ha un callback generato denominato "SimpleMethodCallback".

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

Per ogni **elemento portType** WSDL Wsutil.exe una tabella di funzioni che rappresenta **portType**. Ogni operazione su **portType ha** un puntatore a funzione corrispondente al callback presente nella tabella di funzioni.

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

I prototipi proxy vengono generati per tutte le operazioni. Il nome del prototipo è il nome dell'operazione ,in questo caso "SimpleMethod", specificato nel file WSDL per il contratto di servizio.

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a>Generazione prototipo di descrizione solo locale

I file proxy estub contengono la definizione per la struttura delle definizioni globali, inclusi prototipi e definizioni per le strutture contenenti descrizioni solo locali e implementazioni stub del proxy client/servizio.

Tutti i prototipi e le definizioni locali del file stub vengono generati come parte di una struttura di incapsulamento. Questa struttura di descrizione locale globale fornisce una gerarchia chiara delle descrizioni richieste dal livello di serializzazione e dal modello di servizio. La struttura della descrizione locale ha prototipi simili a quello illustrato di seguito:

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

Le definizioni locali possono fare riferimento a descrizioni generate in un altro file. Ad esempio, il messaggio può essere definito nel file di codice C generato dal file WSDL, ma l'elemento message può essere definito altrove nel file di codice C generato dal file XSD. In questo caso, Wsutil.exe genera un riferimento all'elemento globale dal file che contiene la definizione del messaggio, come illustrato di seguito:

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a>Descrizioni degli elementi globali

Per ogni elemento globale definito in un file wsdl:type o XSD, è presente un campo corrispondente denominato **elementName** all'interno **del campo GlobalElement.** In questo esempio viene generata una struttura denominata SimpleMethod:

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

Altre descrizioni richieste dalla descrizione dell'elemento vengono generate come parte della struttura contenitore. Se l'elemento è un elemento di tipo semplice, è presente un solo campo [**WS \_ ELEMENT \_ DESCRIPTION.**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Se il tipo di elemento è una struttura, tutti i campi e le descrizioni della struttura correlati vengono generati come parte della struttura dell'elemento. In questo esempio l'elemento SimpleMethod è una struttura contenente due campi, **a** e **b**. Wsutil.exe genera la struttura come segue:

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

Le strutture incorporate e gli elementi incorporati vengono generati come sotto-strutture in base alle esigenze.

## <a name="wsdl-related-definitions"></a>Definizioni correlate a WSDL

Wsutil.exe genera un campo nella sezione WSDL per ognuno dei valori **portType** definiti nel wsdl:service specificato.

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

Wsutil.exe genera un campo f che contiene tutte le descrizioni necessarie per l'operazione, una matrice di puntatori a ogni descrizione dell'operazione per ogni metodo e una [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) per il **portType specificato.**

Tutte le descrizioni necessarie per le operazioni vengono generate all'interno del **campo operationName** nell'elemento **portType specificato.** Sono inclusi il [**campo WS \_ ELEMENT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) e la sotto struttura per i parametri di input e output. Analogamente, i campi [**WS \_ MESSAGE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) per il messaggio di input e il messaggio di output facoltativo sono inclusi insieme a ; [**WS \_ Campo \_ dell'elenco PARAMETER DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) per tutti i parametri dell'operazione e campo [**WS OPERATION \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) per l'operazione stessa. In questo esempio la struttura del codice per la descrizione SimpleMethod viene generata come illustrato di seguito:

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

## <a name="xml-dictionary-related-definitions"></a>Definizioni correlate al dizionario XML

I nomi e gli spazi dei nomi utilizzati in varie descrizioni vengono generati come campi di tipo [**WS \_ XML \_ STRING.**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string) Tutte queste stringhe vengono generate come parte di un dizionario costante per file. L'elenco di stringhe e il campo [**WS \_ XML \_ DICTIONARY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (denominato **dict** nell'esempio seguente) vengono generati come parte del campo dizionario della **struttura fileNameLocal.**

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

La matrice di [**WS \_ XML \_ STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s viene generata come una serie di campi di tipo **WS \_ XML \_ STRING,** denominati con nomi descrittivi. Lo stub generato usa i nomi descrittivi in varie descrizioni per migliorare la leggibilità.

Proxy client per operazioni WSDL

Wsutil.exe genera un proxy client per tutte le operazioni. Le applicazioni possono sovrascrivere la firma del metodo usando un'opzione della riga di comando prefisso.

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

Il chiamante dell'operazione deve passare un parametro *heap* valido. I parametri di output vengono allocati utilizzando il valore heap WS \_ specificato nel *parametro heap.* La funzione chiamante può reimpostare o liberare l'heap per rilasciare la memoria per tutti i parametri di output. Se l'operazione non riesce, è possibile recuperare informazioni dettagliate aggiuntive sull'errore dall'oggetto errore facoltativo, se disponibile.

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

La sezione precedente descrive il prototipo della struttura locale contenente tutte le definizioni locali solo per il file stub. Le sezioni successive descrivono le definizioni delle descrizioni.

## <a name="wsdl-definition-generation"></a>Generazione di definizioni WSDL

Wsutil.exe genera una struttura statica costante (**const static**) denominata *<file name \_>* LocalDefinitions di tipo *<service name \_>* Local che contiene tutte le definizioni solo locali.

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

Sono supportate le descrizioni WSDL seguenti:

-   wsdl:service
-   wsdl:binding
-   wsdl:portType
-   wsdl:operation
-   wsdl:message

## <a name="processing-wsdloperation-and-wsdlmessage"></a>Elaborazione di wsdl:operation e wsdl:message

Ogni operazione specificata nel documento WSDL viene mappata a un'operazione del servizio [Wsutil.exe](web-service-compiler-tool.md). Lo strumento genera definizioni separate delle operazioni del servizio sia per il server che per il client.

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

Il layout degli elementi di dati di input e output del messaggio viene valutato dallo strumento per generare i metadati di serializzazione per l'infrastruttura insieme alla firma effettiva dell'operazione del servizio risultante a cui sono associati i messaggi di input e di output.

I metadati per ogni operazione all'interno di un **portType** specifico hanno input e, facoltativamente, un messaggio di output, ognuno di questi messaggi viene mappato a [**un messaggio WS \_ MESSAGE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description). In questo esempio l'input e il messaggio di output sull'operazione in portType sono mappati rispettivamente a inputMessageDescription e facoltativamente a outputMessageDescription in [**WS \_ OPERATION \_ DESCRIPTION.**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)

Per ogni messaggio WSDL, lo strumento genera [**WS \_ MESSAGE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) che fa riferimento alla [**definizione WS ELEMENT \_ \_ DESCRIPTION,**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) come illustrato di seguito:

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

La descrizione del messaggio fa riferimento alla descrizione dell'elemento di input. Poiché l'elemento è definito a livello globale, la descrizione del messaggio fa riferimento alla definizione globale anziché all'elemento statico locale. Analogamente, se l'elemento è definito in un altro file, Wsutil.exe genera un riferimento alla struttura definita a livello globale in tale file. Ad esempio, se SimpleMethodResponse è definito in un altro file example.xsd, Wsutil.exe genera quanto segue:

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Ogni descrizione del messaggio contiene l'azione e la descrizione dell'elemento specifica (un campo di tipo [**WS \_ ELEMENT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) per tutti gli elementi di dati del messaggio. Nel caso di un messaggio di tipo RPC o di un messaggio con più parti, viene creato un elemento wrapper per incapsulare le informazioni aggiuntive.

## <a name="rpc-style-support"></a>Supporto dello stile RPC

Wsutil.exe supporta operazioni di tipo documento e RPC in base all'estensione di associazione WSDL 1.1 per la specifica SOAP 1.2. Le operazioni rpc e di tipo letterale sono contrassegnate come WS \_ RPC \_ LITERAL \_ OPERATION. Il modello di servizio ignora il nome dell'elemento wrapper del corpo della risposta nelle operazioni RPC/letterali.

Wsutil.exe non supporta in modo nativo le operazioni di tipo codifica. Il parametro WS XML BUFFER viene generato per la codifica dei messaggi e gli sviluppatori devono popolare direttamente il \_ \_ buffer opaco.

## <a name="multiple-message-parts-support"></a>Supporto di più parti di messaggi

Wsutil.exe supporta più parti del messaggio in un unico messaggio. Un messaggio in più parti può essere specificato come segue:

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

Wsutil.exe genera un [**campo WS \_ STRUCT \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) per l'elemento message se il messaggio contiene più parti. Se il messaggio viene rappresentato usando lo stile del documento, Wsutil.exe genera un elemento wrapper con tipo struct. L'elemento wrapper non ha un nome o uno spazio dei nomi specifico e la struttura wrapper contiene tutti gli elementi in tutte le parti come campi. L'elemento wrapper è solo per uso interno e non verrà serializzato nel corpo del messaggio.

Se il messaggio usa una rappresentazione in stile RPC o letterale, Wsutil.exe crea un elemento wrapper con il nome dell'operazione come nome dell'elemento e lo spazio dei nomi specificato come spazio dei nomi del servizio in base alla specifica dell'estensione SOAP WSDL. La struttura dell'elemento contiene una matrice di campi che rappresentano i tipi specificati nelle parti del messaggio. L'elemento wrapper viene mappato all'elemento superiore effettivo nel corpo del messaggio, come indicato nella specifica SOAP.

Sul lato server, ogni operazione comporta un typedef dell'operazione del servizio server risultante. Questo typedef viene usato per fare riferimento all'operazione nella tabella delle funzioni come descritto in precedenza. Ogni operazione comporta anche la generazione di una funzione stub che nfrastructure chiama per conto del delegato al metodo effettivo.

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

Per l'operazione SimpleMethod, il typedef SimpleMethodOperation è definito in precedenza. Si noti che il metodo generato ha un elenco di argomenti espanso con la parte del messaggio per il messaggio di input e di output per l'operazione SimpleMethod come parametri denominati.

Sul lato client ogni operazione viene mappata a un'operazione del servizio proxy.

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

## <a name="processing-wsdlbinding"></a>Elaborazione di wsdl:binding

Il modello di servizio WWSAPI supporta l'estensione di associazione SOAP. Per ogni associazione è presente un **portType associato.**

Il trasporto specificato nell'estensione per l'associazione soap è solo consultivo. L'applicazione deve fornire informazioni sul trasporto durante la creazione di un canale. Attualmente sono supportate le associazioni WS HTTP BINDING e \_ \_ TCP BINDING \_ \_ WS.

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

Nel documento WSDL di esempio è presente un solo **portType** per ISimpleService. L'associazione SOAP fornita indica il trasporto HTTP, specificato come WS \_ HTTP \_ BINDING. Si noti che questa struttura non dispone di elementi decorativi statici perché questa struttura deve essere disponibile per l'applicazione.

Elaborazione di wsdl:portType

Ogni **portType** in WSDL è costituito da una o più operazioni. L'operazione deve essere coerente con l'estensione di associazione SOAP indicata in wsdl:binding.

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

In questo esempio il tipo  di porta ISimpleService contiene solo l'operazione SimpleMethod. Ciò è coerente con la sezione di associazione in cui è presente una sola operazione WSDL che esegue il mapping a un'azione SOAP.

Poiché il **portType** ISimpleService include una sola operazione, SimpleMethod, la tabella di funzione corrispondente contiene solo SimpleMethod come operazione del servizio.

In termini di metadati, **ogni portType** viene mappato Wsutil.exe a [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description). Ogni operazione all'interno **di un portType** viene mappata a [**WS OPERATION \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

In questo esempio **portType lo** strumento genera [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) per ISimpleService. Questa descrizione del contratto contiene il numero specifico di operazioni disponibili nel **portType** ISimpleService insieme a una matrice di [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) che rappresenta le singole operazioni definite in portType per ISimpleService. Poiché è presente una sola operazione su ISimpleService portType per ISimpleService, esiste anche una sola **definizione WS \_ OPERATION \_ DESCRIPTION.**

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

## <a name="processing-wsdlservice"></a>Elaborazione di wsdl:service

WsUtil.exe i servizi per trovare binding/porttypes e genera la struttura del contratto che descrive tipi, messaggi, definizioni di tipi di porta e così via. Le descrizioni dei contratti sono accessibili esternamente e vengono generate come parte della struttura di definizione globale specificata tramite l'intestazione generata.

WsUtil.exe supporta le estensioni EndpointReference definite in wsdl:port. Il riferimento all'endpoint è definito in WS-ADDRESSING come modo per descrivere le informazioni [sull'endpoint](endpoint-address.md) di un servizio. Il testo dell'estensione di riferimento dell'endpoint di input salvato come [**WS \_ XML \_ STRING,**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)insieme alla corrispondente [**WS \_ ENDPOINT ADDRESS \_ \_ DESCRIPTION,**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) vengono generati nella sezione endpointReferences della struttura globale.

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

Per creare [**WS \_ ENDPOINT \_ ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) usando i metadati generati da WsUtil:

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

Le stringhe costanti nello stub del servizio o del proxy client vengono generate come campi di tipo WS XML STRING ed è disponibile un dizionario costante per tutte le stringhe nel \_ \_ file proxy o stub. Ogni stringa nel dizionario viene generata come campo nella parte del dizionario della struttura locale per una migliore leggibilità.

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

## <a name="processing-wsdltype"></a>Elaborazione di wsdl:type

Wsutil.exe supporta solo documenti XML Schema (XSD) nella specifica wsdl:type. Un caso speciale è quando una porta del messaggio specifica una definizione di elemento globale. Vedere la sezione seguente per altri dettagli sull'euristica usata in questi casi.

## <a name="parameter-processing-heuristics"></a>Euristica dell'elaborazione dei parametri

Nel modello di servizio i messaggi WSDL vengono mappati a parametri specifici in un metodo. Wsutil.exe ha due stili di generazione dei parametri: nel primo stile, l'operazione ha un parametro per il messaggio di input e un parametro per il messaggio di output (se necessario); nel secondo stile, Wsutil.exe un'euristica per eseguire il mapping e l'espansione dei campi nelle strutture sia per i messaggi di input che per i messaggi di output a parametri diversi nell'operazione. Per generare questo secondo approccio, sia i messaggi di input che i messaggi di output devono avere elementi messaggio di tipo struttura.

Wsutil.exe le regole seguenti quando si generano i parametri dell'operazione dai messaggi di input e di output:

-   Per i messaggi di input e output con più parti del messaggio, ogni parte del messaggio è un parametro separato nell'operazione, con il nome della parte del messaggio come nome del parametro.
-   Per il messaggio in stile RPC con una parte del messaggio, la parte del messaggio è un parametro nell'operazione, con il nome della parte del messaggio come nome del parametro.
-   Per i messaggi di input e output in stile documento con una parte del messaggio:
    -   Se il nome di una parte del messaggio è "parameters" e il tipo di elemento è una struttura, ogni campo nella struttura viene considerato come un parametro separato con il nome del campo come nome del parametro.
    -   Se il nome della parte del messaggio non è "parameters", il messaggio è un parametro nell'operazione con il nome del messaggio usato come nome del parametro corrispondente.
-   Per il messaggio di input e output in stile documento con elemento nillable, il messaggio viene mappato a un parametro, con il nome della parte del messaggio come nome del parametro. Viene aggiunto un ulteriore livello di riferimento indiretto per indicare che il puntatore può essere **NULL.**
-   Se un campo viene visualizzato solo nell'elemento del messaggio di input, il campo viene considerato come \[ parametro \] in .
-   Se un campo viene visualizzato solo nell'elemento del messaggio di output, il campo viene considerato come \[ parametro \] out.
-   Se è presente un campo con lo stesso nome e lo stesso tipo visualizzato sia nel messaggio di input che nel messaggio di output, il campo viene considerato come \[ parametro in,out. \]

Per determinare la direzione dei parametri vengono usati gli strumenti seguenti:

-   Se un campo viene visualizzato solo nell'elemento del messaggio di input, il campo viene considerato come in un solo parametro.
-   Se un campo viene visualizzato solo nell'elemento del messaggio di output, il campo viene considerato come parametro out only.
-   Se è presente un campo con lo stesso nome e lo stesso tipo visualizzato sia nel messaggio di input che nel messaggio di output, il campo viene considerato come parametro in,out.

Wsutil.exe supporta solo elementi sequenziati. Rifiuta l'ordinamento non valido per quanto riguarda i parametri in,out Wsutil.exe non è possibile combinare i parametri in e \[ out in un singolo elenco di \] parametri. È possibile aggiungere suffissi ai nomi dei parametri per evitare conflitti di nomi.

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

Wsutil.exe considera i campi in tns:SimpleMethod e tns:SimpleMethodResponse come parametri, come illustrato nelle definizioni dei parametri seguenti:

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

Wsutil.exe l'elenco di parametri dai campi nell'elenco precedente e genera la struttura **ParamStruct** nell'esempio di codice seguente. Il run-time del modello di servizio può usare questa struttura per passare argomenti agli stub client e server.

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

Questa struttura viene usata solo per descrivere il stack frame sul lato client e sul lato server. Non sono presenti modifiche alla descrizione del messaggio o alle descrizioni degli elementi a cui fa riferimento la descrizione del messaggio.

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

Come regola generale, viene aggiunto un livello di riferimento indiretto per tutti i \[ parametri out \] e \[ in,out. \]

## <a name="parameterless-operation"></a>Operazione senza parametri

Per le operazioni documento e letterale, Wsutil.exe l'operazione viene trattata come con un parametro di input e un parametro di output se:

-   Il messaggio di input o di output ha più di una parte.
-   È presente una sola parte del messaggio e il nome della parte del messaggio non è "parameters".

.. Nell'esempio precedente, supponendo che le parti del messaggio siano denominate *ParamIn*" e *ParamOut*, la firma del metodo diventa il codice seguente:

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

Wsutil.exe genera una firma di versione per la descrizione dell'operazione in modo che il motore del modello di servizio sul lato server e WsCall possa verificare se la descrizione generata è applicabile per la piattaforma corrente.

Queste informazioni sulla versione vengono generate come parte della [**struttura WS \_ OPERATION \_ DESCRIPTION.**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) Il numero di versione può essere considerato come un selettore arm di unione per rendere estensibile la struttura. Attualmente **versionID è** impostato su 1 senza campi successivi. Versiosn futuro può incrementare il numero di versione e includere più campi in base alle esigenze. Ad esempio, Wsutil.exe attualmente genera il codice seguente in base all'ID versione:

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

In futuro, potrebbe essere espansa come segue:

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

Vedere la sezione relativa alla sicurezza [nell'argomento dello strumento del compilatore Wsutil.](wsutil-compiler-tool.md)

 

 




