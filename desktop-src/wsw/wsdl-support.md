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
# <a name="wsdl-and-service-contracts"></a><span data-ttu-id="6f5c2-106">WSDL e contratti di servizio</span><span class="sxs-lookup"><span data-stu-id="6f5c2-106">WSDL and Service Contracts</span></span>

<span data-ttu-id="6f5c2-107">L'utilità [Wsutil.exe](web-service-compiler-tool.md) genera uno stub del linguaggio C in base ai metadati WSDL specificati, nonché le definizioni e le descrizioni dei tipi di dati per i tipi di dati descritti dagli schemi XML creati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-107">The [Wsutil.exe](web-service-compiler-tool.md) utility generates a C language stub according to supplied WSDL metadata, as well as data type definitions and descriptions for data types described by user-authored XML schemas.</span></span>


<span data-ttu-id="6f5c2-108">Di seguito è riportato un documento WSDL di esempio e XML Schema che funge da base per la discussione seguente:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-108">The following is an example WSDL document and XML schema that serves as a basis for the discussion that follows:</span></span>

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

<span data-ttu-id="6f5c2-109">In questo esempio viene fornito un contratto, ISimpleService, con un solo metodo, SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-109">This example provides a contract, ISimpleService, with a single method, SimpleMethod.</span></span> <span data-ttu-id="6f5c2-110">"SimpleMethod" ha due parametri di input di tipo **Integer**, *a* e *b*, che vengono inviati dal client al servizio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-110">"SimpleMethod" has two input parameters of type **integer**, *a* and *b*, that are sent from the client to the service.</span></span> <span data-ttu-id="6f5c2-111">Analogamente, SimpleMethod ha due parametri di output di tipo **Integer**, *b* e *c*, che vengono restituiti al client al termine del completamento.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-111">Likewise, SimpleMethod has two output parameters of type **integer**, *b* and *c*, which are returned to the client after successful completion.</span></span> <span data-ttu-id="6f5c2-112">Nella sintassi C con annotazioni SAL la definizione del metodo viene visualizzata come segue:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-112">In SAL-annotated C syntax, the method definition appears as follows:</span></span>

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

<span data-ttu-id="6f5c2-113">In questa definizione, ISimpleService è un contratto di servizio con una singola operazione di servizio: SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-113">In this definition, ISimpleService is a service contract with a single service operation: SimpleMethod.</span></span>

<span data-ttu-id="6f5c2-114">Il file di intestazione di output contiene definizioni e descrizioni per riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-114">The output header file contains definitions and descriptions for external reference.</span></span> <span data-ttu-id="6f5c2-115">ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-115">This includes:</span></span>

-   <span data-ttu-id="6f5c2-116">Definizioni della struttura C per i tipi di elemento globali.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-116">C structure definitions for global element types.</span></span>
-   <span data-ttu-id="6f5c2-117">Un prototipo di operazione come definito nel file corrente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-117">An operation prototype as defined in current file.</span></span>
-   <span data-ttu-id="6f5c2-118">Prototipo di tabella di funzione per i contratti specificati nel file WSDL.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-118">A function table prototype for the contracts specified in the WSDL file.</span></span>
-   <span data-ttu-id="6f5c2-119">Prototipi del proxy client e dello stub del servizio per tutte le funzioni specificate nel file corrente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-119">Client proxy and service stub prototypes for all the functions specified in current file.</span></span>
-   <span data-ttu-id="6f5c2-120">Struttura di dati di [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) per gli elementi dello schema globale definiti nel file corrente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-120">A [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) data structure for the global schema elements defined in current file.</span></span>
-   <span data-ttu-id="6f5c2-121">Struttura dei dati [**WS \_ message \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) per tutti i messaggi specificati nel file corrente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-121">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) data structure for all the messages specified in current file.</span></span>
-   <span data-ttu-id="6f5c2-122">Struttura di dati [**WS \_ Contract \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) per tutti i contratti specificati nel file corrente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-122">A [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) data structure for all the contracts specified in current file.</span></span>

<span data-ttu-id="6f5c2-123">Viene generata una struttura globale per incapsulare tutte le descrizioni globali per i tipi di schema e i tipi di modello di servizio a cui l'applicazione può fare riferimento.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-123">One global structure is generated to encapsulate all the global descriptions for the schema types and service model types to which the application can refer.</span></span> <span data-ttu-id="6f5c2-124">La struttura viene denominata utilizzando un nome di file normalizzato.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-124">The structure is named using a normalized file name.</span></span> <span data-ttu-id="6f5c2-125">In questo esempio Wsutil.exe genera una struttura di definizioni globali denominata "example \_ WSDL" che contiene tutte le descrizioni dei servizi Web.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-125">In this example, Wsutil.exe generates a global definitions structure named "example\_wsdl" that contains all the web service descriptions.</span></span> <span data-ttu-id="6f5c2-126">La definizione della struttura viene generata nel file stub.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-126">The structure definition is generated in the stub file.</span></span>

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

<span data-ttu-id="6f5c2-127">Per le definizioni di elementi globali nel documento di XML Schema (XSD), viene generato un prototipo di [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , oltre alla definizione del tipo C corrispondente, per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-127">For global element definitions in the XML schema document (XSD), one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) prototype, as well as the corresponding C type definition, are generated for each of the elements.</span></span> <span data-ttu-id="6f5c2-128">I prototipi per le descrizioni degli elementi per SimpleMethod e SimpleMethodResponse vengono generati come membri nella struttura precedente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-128">The prototypes for the element descriptions for SimpleMethod and SimpleMethodResponse are generated as members in the structure above.</span></span> <span data-ttu-id="6f5c2-129">Le strutture C vengono generate nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-129">The C structures are generated as follows:</span></span>

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

<span data-ttu-id="6f5c2-130">Analogamente, per i tipi complessi globali, Wsutil.exe genera definizioni di struttura di tipo C come sopra, senza le descrizioni degli elementi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-130">Similarly for global complex types, Wsutil.exe generates type C structure definitions like above, without matching element descriptions.</span></span>

<span data-ttu-id="6f5c2-131">Per l'input WSDL, Wsutil.exe genera le definizioni e i prototipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-131">For WSDL input, Wsutil.exe generates the following prototypes and definitions:</span></span>

-   <span data-ttu-id="6f5c2-132">Per la descrizione del messaggio viene generato un prototipo [**WS \_ message \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-132">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) prototype is generated for the message description.</span></span> <span data-ttu-id="6f5c2-133">Questa descrizione può essere utilizzata dal modello del servizio e dal livello del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-133">This description can be used by the service model as well as the message layer.</span></span> <span data-ttu-id="6f5c2-134">Le strutture di descrizione del messaggio sono campi denominati "MessageName" nella struttura globale.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-134">Message description structures are fields named "messagename" in the global structure.</span></span> <span data-ttu-id="6f5c2-135">In questo esempio la descrizione del messaggio viene generata come campo ISimpleService \_ SimpleMethod \_ InputMessage nella \_ struttura ISimpleService SimpleMethod \_ InputMessage, come specificato nel file WSDL.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-135">In this example, the message description is generated as the ISimpleService\_SimpleMethod\_InputMessage field in the ISimpleService\_SimpleMethod\_InputMessage structure as specified in the WSDL file.</span></span>
-   <span data-ttu-id="6f5c2-136">[**WS \_ Il \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototipo della descrizione del contratto viene generato per la descrizione del contratto.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-136">[**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototype is generated for the contract description.</span></span> <span data-ttu-id="6f5c2-137">Questa descrizione viene utilizzata dal modello di servizio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-137">This description is used by service model.</span></span> <span data-ttu-id="6f5c2-138">Le strutture di descrizione del contratto sono campi denominati "ContractName" nella struttura globale.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-138">Contract description structures are fields named "contractname" in the global structure.</span></span> <span data-ttu-id="6f5c2-139">In questo esempio la descrizione del contratto viene generata come \_ campo Default ISimpleService nella struttura " \_ example \_ WSDL".</span><span class="sxs-lookup"><span data-stu-id="6f5c2-139">In this example, the contract description is generated as the DefaultBinding\_ISimpleService field in the structure "\_example\_wsdl".</span></span>

<span data-ttu-id="6f5c2-140">Le specifiche delle operazioni e dei tipi sono comuni sia al proxy che allo stub e vengono generate in entrambi i file.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-140">Operation and type specifications are common to both proxy and stub and they are generated in both files.</span></span> <span data-ttu-id="6f5c2-141">Wsutil.exe genera una copia solo se il proxy e lo stub vengono generati nello stesso file.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-141">Wsutil.exe generates one copy only if both the proxy and stub are generated in the same file.</span></span>

## <a name="identifier-generation"></a><span data-ttu-id="6f5c2-142">Generazione di identificatori</span><span class="sxs-lookup"><span data-stu-id="6f5c2-142">Identifier generation</span></span>

<span data-ttu-id="6f5c2-143">Le strutture C generate automaticamente sopra elencate vengono create in base al nome specificato nel file WSDL.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-143">The autogenerated C structures listed above are created based on the name specified in WSDL file.</span></span> <span data-ttu-id="6f5c2-144">Un NCName XML non è comunemente considerato un identificatore C valido e i nomi vengono normalizzati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-144">An XML NCName is not commonly considered a valid C identifier, and the names are normalized as needed.</span></span> <span data-ttu-id="6f5c2-145">I valori esadecimali non vengono convertiti e le lettere comuni come ':','/' è .' vengono convertite nel carattere di sottolineatura ' \_ ' per migliorare la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-145">Hex values are not converted, and common letters like ':', '/' and '.' are converted to the underscore '\_' character to improve readability.</span></span>

## <a name="header-for-the-stub"></a><span data-ttu-id="6f5c2-146">Intestazione per lo stub</span><span class="sxs-lookup"><span data-stu-id="6f5c2-146">Header for the stub</span></span>

<span data-ttu-id="6f5c2-147">Per ogni operazione nel contratto di servizio, viene generata una routine di callback denominata " <operationname> callback".</span><span class="sxs-lookup"><span data-stu-id="6f5c2-147">For each operation in the service contract, one callback routine named "<operationname>Callback" is generated.</span></span> <span data-ttu-id="6f5c2-148">Ad esempio, l'operazione "SimpleMethod" nel contratto di servizio di esempio ha un callback generato denominato "SimpleMethodCallback".</span><span class="sxs-lookup"><span data-stu-id="6f5c2-148">(For example, the operation "SimpleMethod" in the example service contract has a generated callback named "SimpleMethodCallback".)</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

<span data-ttu-id="6f5c2-149">Per ogni **PORTTYPE** WSDL Wsutil.exe genera una tabella di funzioni che rappresenta **portType**.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-149">For each WSDL **portType** Wsutil.exe generates a function table representing **portType**.</span></span> <span data-ttu-id="6f5c2-150">Ogni operazione su **portType** dispone di un puntatore a funzione corrispondente al callback presente nella tabella function.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-150">Each operation on the **portType** has a corresponding function pointer to the callback present in the function table.</span></span>

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

<span data-ttu-id="6f5c2-151">I prototipi proxy vengono generati per tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-151">Proxy prototypes are generated for all operations.</span></span> <span data-ttu-id="6f5c2-152">Il nome del prototipo è il nome dell'operazione (in questo caso, "SimpleMethod") specificato nel file WSDL per il contratto di servizio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-152">The prototype name is the operation name (in this case, "SimpleMethod") specified in WSDL file for the service contract.</span></span>

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a><span data-ttu-id="6f5c2-153">Generazione del prototipo di descrizione solo locale</span><span class="sxs-lookup"><span data-stu-id="6f5c2-153">Local-only Description Prototype Generation</span></span>

<span data-ttu-id="6f5c2-154">I file andstub del proxy contengono la definizione per la struttura delle definizioni globali, inclusi i prototipi e le definizioni per le strutture contenenti le descrizioni solo locali e le implementazioni del proxy client/servizio dello stub del servizio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-154">The proxy andstub files contain the definition for the global definitions structure, including prototypes and definitions for the structures containing local-only descriptions and client proxy/service stub implementations.</span></span>

<span data-ttu-id="6f5c2-155">Tutti i prototipi e le definizioni locali per il file stub vengono generati come parte di una struttura di incapsulamento.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-155">All prototypes and definitions that are local to the stub file are generated as part of an encapsulating structure.</span></span> <span data-ttu-id="6f5c2-156">Questa struttura di descrizione locale che include una chiara gerarchia delle descrizioni richieste dal livello di serializzazione e dal modello del servizio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-156">This overarching local description structure provides a clear hierarchy of the descriptions required by the serialization layer and the service model.</span></span> <span data-ttu-id="6f5c2-157">La struttura di descrizione locale presenta prototipi simili a quelli illustrati di seguito:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-157">The local description structure has prototypes similar to the one shown below:</span></span>

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

## <a name="referencing-definitions-from-other-files"></a><span data-ttu-id="6f5c2-158">Riferimento a definizioni da altri file</span><span class="sxs-lookup"><span data-stu-id="6f5c2-158">Referencing definitions from other files</span></span>

<span data-ttu-id="6f5c2-159">Le definizioni locali possono fare riferimento a descrizioni generate in un altro file.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-159">Local definitions can reference descriptions generated in another file.</span></span> <span data-ttu-id="6f5c2-160">Il messaggio, ad esempio, può essere definito nel file di codice C generato dal file WSDL, ma l'elemento Message può essere definito altrove nel file di codice C generato dal file XSD.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-160">For example, the message may be defined in the C code file generated from the WSDL file but the message element may be defined elsewhere in the C code file generated from the XSD file.</span></span> <span data-ttu-id="6f5c2-161">In questo caso, Wsutil.exe genera un riferimento all'elemento globale dal file che contiene la definizione del messaggio, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-161">In this case, Wsutil.exe generates reference to the global element from the file that contains the message definition, as demonstrated below:</span></span>

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a><span data-ttu-id="6f5c2-162">Descrizioni degli elementi globali</span><span class="sxs-lookup"><span data-stu-id="6f5c2-162">Global element descriptions</span></span>

<span data-ttu-id="6f5c2-163">Per ogni elemento globale definito in un file WSDL: Type o XSD, esiste un campo corrispondente denominato **ElementName** nel campo **globalelement** .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-163">For each global element defined in a wsdl:type or XSD file, there is a matching field named **elementName** inside the **GlobalElement** field.</span></span> <span data-ttu-id="6f5c2-164">In questo esempio viene generata una struttura denominata SimpleMethod:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-164">In this example, a structure named SimpleMethod is generated:</span></span>

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

<span data-ttu-id="6f5c2-165">Altre descrizioni richieste dalla descrizione dell'elemento vengono generate come parte della struttura che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-165">Other descriptions required by the element description are generated as part of the containing structure.</span></span> <span data-ttu-id="6f5c2-166">Se l'elemento è un elemento di tipo semplice, è presente un solo campo di [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-166">If the element is a simple type element, there is only one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field.</span></span> <span data-ttu-id="6f5c2-167">Se il tipo di elemento è una struttura, tutti i campi correlati e le descrizioni della struttura vengono generati come parte della struttura dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-167">If the element type is a structure, all of the related fields and structure descriptions are generated as part of the element structure.</span></span> <span data-ttu-id="6f5c2-168">In questo esempio, l'elemento SimpleMethod è una struttura che contiene due campi, **a** e **b**.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-168">In this example, SimpleMethod element is a structure containing two fields, **a** and **b**.</span></span> <span data-ttu-id="6f5c2-169">Wsutil.exe genera la struttura come segue:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-169">Wsutil.exe generates the structure as follows:</span></span>

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

<span data-ttu-id="6f5c2-170">Le strutture incorporate e gli elementi incorporati vengono generati come sottostrutture in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-170">Embedded structures and embedded elements are generated as sub-structures as needed.</span></span>

## <a name="wsdl-related-definitions"></a><span data-ttu-id="6f5c2-171">Definizioni correlate a WSDL</span><span class="sxs-lookup"><span data-stu-id="6f5c2-171">WSDL related definitions</span></span>

<span data-ttu-id="6f5c2-172">Wsutil.exe genera un campo sotto la sezione WSDL per ogni valore **portType** definito nel servizio WSDL: specificato.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-172">Wsutil.exe generates a field under WSDL section for each of the **portType** values defined under the specified wsdl:service.</span></span>

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

<span data-ttu-id="6f5c2-173">Wsutil.exe genera un campo f che contiene tutte le descrizioni necessarie per l'operazione, una matrice signle di puntatori a ognuna delle descrizioni delle operazioni per ogni metodo e una [**Descrizione del \_ contratto \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) per l'oggetto **portType** specificato.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-173">Wsutil.exe generates one field f that contains all the descriptions needed for the operation, a signle array of pointers to each of the operation descriptions for each method, and one [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for the specified **portType**.</span></span>

<span data-ttu-id="6f5c2-174">Tutte le descrizioni richieste dalle operazioni vengono generate all'interno del campo **OperationName** nell'oggetto **portType** specificato.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-174">All the descriptions needed by operations are generated inside the **operationName** field under the specified **portType**.</span></span> <span data-ttu-id="6f5c2-175">Sono inclusi il [**campo \_ \_ Description dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) e la sottostruttura per i parametri di input e di output.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-175">These include the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field as well as the sub-structure for input and output parameter s.</span></span> <span data-ttu-id="6f5c2-176">Analogamente, i campi di [**\_ \_ Descrizione del messaggio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) per il messaggio di input e il messaggio di output facoltativo vengono inclusi insieme a; [**WS \_ Campo elenco \_ Descrizione parametro**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) per tutti i parametri dell'operazione e il [**campo \_ \_ Descrizione operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) per l'operazione stessa.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-176">Likewise, the [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) fields for the input message and the optional output message are included along with the; [**WS\_PARAMETER\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) list field for all of the operation parameters and the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) field for the operation itself.</span></span> <span data-ttu-id="6f5c2-177">In questo esempio, la struttura del codice per la descrizione di SimpleMethod viene generata come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-177">In this example, the code structure for the SimpleMethod description is generated as seen below:</span></span>

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

## <a name="xml-dictionary-related-definitions"></a><span data-ttu-id="6f5c2-178">Definizioni correlate ai dizionari XML</span><span class="sxs-lookup"><span data-stu-id="6f5c2-178">XML dictionary related definitions</span></span>

<span data-ttu-id="6f5c2-179">I nomi e gli spazi dei nomi utilizzati in diverse descrizioni vengono generati come campi di tipo [**\_ \_ stringa WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span><span class="sxs-lookup"><span data-stu-id="6f5c2-179">Names and namespaces used in various descriptions are generated as fields of type [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span></span> <span data-ttu-id="6f5c2-180">Tutte queste stringhe vengono generate come parte di un dizionario di costanti per file.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-180">All of these strings are generated as part a per-file constant dictionary.</span></span> <span data-ttu-id="6f5c2-181">L'elenco di stringhe e il campo del [**\_ \_ dizionario di WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (denominato **dict** nell'esempio riportato di seguito) vengono generati come parte del campo Dictionary della struttura **fileNameLocal** .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-181">The list of strings and the [**WS\_XML\_DICTIONARY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) field (named **dict** in the example below) are generated as part of the dictionary field of the **fileNameLocal** structure.</span></span>

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

<span data-ttu-id="6f5c2-182">La matrice di [**\_ \_ stringhe WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)viene generata come una serie di campi di tipo **stringa WS \_ XML \_**, denominata con nomi descrittivi.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-182">The array of [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s are generated as a series of fields of type **WS\_XML\_STRING**, named with with user-friendly names.</span></span> <span data-ttu-id="6f5c2-183">Lo stub generato usa i nomi descrittivi in diverse descrizioni per migliorare la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-183">The generated stub uses the user-friendly names in various descriptions for better readability.</span></span>

<span data-ttu-id="6f5c2-184">Proxy client per le operazioni WSDL</span><span class="sxs-lookup"><span data-stu-id="6f5c2-184">Client proxy for WSDL operations</span></span>

<span data-ttu-id="6f5c2-185">Wsutil.exe genera un proxy client per tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-185">Wsutil.exe generates a client proxy for all of the operations.</span></span> <span data-ttu-id="6f5c2-186">Le applicazioni possono sovrascrivere la firma del metodo usando un'opzione della riga di comando prefix.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-186">Applications can overwrite the method signature using a prefix command-line option.</span></span>

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

<span data-ttu-id="6f5c2-187">Il chiamante dell'operazione deve passare un parametro dell' *heap* valido.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-187">The operation caller must pass in a valid *heap* parameter.</span></span> <span data-ttu-id="6f5c2-188">I parametri di output vengono allocati usando il \_ valore dell'heap WS specificato nel parametro dell' *heap* .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-188">Output parameters are allocated using the WS\_HEAP value specified in the *heap* parameter.</span></span> <span data-ttu-id="6f5c2-189">La funzione chiamante può reimpostare o liberare l'heap per rilasciare la memoria per tutti i parametri di output.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-189">The calling function can reset or free the heap to release memory for all of the output parameters.</span></span> <span data-ttu-id="6f5c2-190">Se l'operazione ha esito negativo, è possibile recuperare informazioni aggiuntive sull'errore di dettaglio dall'oggetto facoltativo error se disponibile.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-190">If the operation fails, additional detail error information can be retrieved from the optional error object if it is available.</span></span>

<span data-ttu-id="6f5c2-191">Wsutil.exe genera uno stub del servizio per tutte le operazioni descritte nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-191">Wsutil.exe generates a service stub for all of the operations described in binding.</span></span>

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

<span data-ttu-id="6f5c2-192">Nella sezione precedente viene descritto il prototipo della struttura locale contenente tutte le definizioni locali solo per il file stub.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-192">The above section describes the prototype of the local structure containing all of the definitions local to the stub file only.</span></span> <span data-ttu-id="6f5c2-193">Nelle sezioni successive vengono descritte le definizioni delle descrizioni.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-193">Subsequent sections describe the definitions of the descriptions.</span></span>

## <a name="wsdl-definition-generation"></a><span data-ttu-id="6f5c2-194">Generazione definizione WSDL</span><span class="sxs-lookup"><span data-stu-id="6f5c2-194">WSDL Definition Generation</span></span>

<span data-ttu-id="6f5c2-195">Wsutil.exe genera una struttura costante statica (**const static**) denominata *<\_ nome file>* LocalDefinitions di tipo *<\_ nome servizio>* locale che contiene tutte le definizioni solo locali.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-195">Wsutil.exe generates a constant static (**const static**) structure named *<file\_name>* LocalDefinitions of type *<service\_name>* Local that contains all the local only definitions.</span></span>

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

<span data-ttu-id="6f5c2-196">Sono supportate le seguenti descrizioni WSDL:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-196">The following WSDL descriptions are supported:</span></span>

-   <span data-ttu-id="6f5c2-197">WSDL: servizio</span><span class="sxs-lookup"><span data-stu-id="6f5c2-197">wsdl:service</span></span>
-   <span data-ttu-id="6f5c2-198">WSDL: binding</span><span class="sxs-lookup"><span data-stu-id="6f5c2-198">wsdl:binding</span></span>
-   <span data-ttu-id="6f5c2-199">WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="6f5c2-199">wsdl:portType</span></span>
-   <span data-ttu-id="6f5c2-200">WSDL: Operation</span><span class="sxs-lookup"><span data-stu-id="6f5c2-200">wsdl:operation</span></span>
-   <span data-ttu-id="6f5c2-201">WSDL: Message</span><span class="sxs-lookup"><span data-stu-id="6f5c2-201">wsdl:message</span></span>

## <a name="processing-wsdloperation-and-wsdlmessage"></a><span data-ttu-id="6f5c2-202">Elaborazione di WSDL: Operation e WSDL: Message</span><span class="sxs-lookup"><span data-stu-id="6f5c2-202">Processing wsdl:operation and wsdl:message</span></span>

<span data-ttu-id="6f5c2-203">Ogni operazione specificata nel documento WSDL viene mappata a un'operazione del servizio da [Wsutil.exe](web-service-compiler-tool.md).</span><span class="sxs-lookup"><span data-stu-id="6f5c2-203">Each operation specified in the WSDL document is mapped to a service operation by [Wsutil.exe](web-service-compiler-tool.md).</span></span> <span data-ttu-id="6f5c2-204">Lo strumento genera definizioni separate delle operazioni del servizio sia per il server che per il client.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-204">The tool generates separate definitions of the service operations for both the server and the client.</span></span>

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

<span data-ttu-id="6f5c2-205">Il layout degli elementi dati del messaggio andOutput di input viene valutato dallo strumento per generare i metadati di serializzazione per l'infrastruttura insieme alla firma effettiva dell'operazione di servizio risultante a cui sono associati i messaggi di input e di output.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-205">The layout of the input andoutput message data elements is evaluated by the tool to generate the serialization metadata for the infrastructure along with the actual signature of the resulting service operation to which the input and output messages are associated.</span></span>

<span data-ttu-id="6f5c2-206">I metadati per ogni operazione all'interno di un **portType** specifico hanno un input e, facoltativamente, un messaggio di output, ognuno di questi messaggi viene mappato a una [**\_ \_ Descrizione del messaggio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span><span class="sxs-lookup"><span data-stu-id="6f5c2-206">The metadata for each operation within a specific **portType** has input and optionally an output message, each of these messages is mapped to a [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span></span> <span data-ttu-id="6f5c2-207">In questo esempio, l'input e il messaggio di output sull'operazione nell'oggetto portType mappato a inputMessageDescription e facoltativamente outputMessageDescription nella [**Descrizione dell' \_ operazione \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-207">In this example, the input and the output message on the operation in the portType mapped to inputMessageDescription and optionally the outputMessageDescription on the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) respectively.</span></span>

<span data-ttu-id="6f5c2-208">Per ogni messaggio WSDL lo strumento genera [**la \_ \_ Descrizione del messaggio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) che fa riferimento alla definizione della [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-208">For each WSDL message the tool generates [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) that references the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) definition, as demonstrated below:</span></span>

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="6f5c2-209">La descrizione del messaggio si riferisce alla descrizione dell'elemento di input.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-209">The message description refers to the input element description.</span></span> <span data-ttu-id="6f5c2-210">Poiché l'elemento è definito globalmente, la descrizione del messaggio fa riferimento alla definizione globale anziché all'elemento statico locale.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-210">Because the element is globally defined, the message description references the global definition instead of the local static element.</span></span> <span data-ttu-id="6f5c2-211">Analogamente, se l'elemento è definito in un altro file, Wsutil.exe genera un riferimento alla struttura definita globalmente in tale file.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-211">Similarly, if the element is defined in another file, Wsutil.exe generates a reference to the globally-defined structure in that file.</span></span> <span data-ttu-id="6f5c2-212">Se, ad esempio, SimpleMethodResponse è definito in un altro file XSD di esempio, Wsutil.exe genera invece quanto segue:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-212">For example, if SimpleMethodResponse is defined in another example.xsd file, Wsutil.exe generates the following instead:</span></span>

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="6f5c2-213">Ogni descrizione del messaggio contiene l'azione e la descrizione dell'elemento specifico (un campo di tipo [**\_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) per tutti gli elementi dati del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-213">Each message description contains the action and the specific element description (a field of type [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) for all the message data elements.</span></span> <span data-ttu-id="6f5c2-214">Nel caso di un messaggio di tipo RPC o di un messaggio con più parti, viene creato un elemento wrapper per incapsulare le informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-214">In the case of an RPC-style message or a message with multiple parts, a wrapper element is created to encapsulate the additional information.</span></span>

## <a name="rpc-style-support"></a><span data-ttu-id="6f5c2-215">Supporto dello stile RPC</span><span class="sxs-lookup"><span data-stu-id="6f5c2-215">RPC style support</span></span>

<span data-ttu-id="6f5c2-216">Wsutil.exe supporta operazioni di tipo Document e RPC in base all'estensione di binding WSDL 1,1 per la specifica SOAP 1,2.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-216">Wsutil.exe supports document-style as well as RPC-style operations according to the WSDL 1.1 Binding Extension for SOAP 1.2 specification.</span></span> <span data-ttu-id="6f5c2-217">Le operazioni RPC e di tipo letterale sono contrassegnate \_ come \_ operazione WS RPC Literal \_ .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-217">RPC- and literal-style operations are marked as WS\_RPC\_LITERAL\_OPERATION.</span></span> <span data-ttu-id="6f5c2-218">Il modello di servizio ignora il nome dell'elemento wrapper del corpo della risposta nelle operazioni RPC/Literal.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-218">The service model ignores the name for the response body wrapper element in RPC/literal operations.</span></span>

<span data-ttu-id="6f5c2-219">Wsutil.exe non supporta in modo nativo operazioni di tipo codifica.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-219">Wsutil.exe does not natively support encoding-style operations.</span></span> <span data-ttu-id="6f5c2-220">Il \_ parametro del buffer WS XML \_ viene generato per i messaggi di codifica e gli sviluppatori devono popolare direttamente il buffer opaco.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-220">The WS\_XML\_BUFFER parameter is generated for encoding messages, and developers must populate the opaque buffer directly.</span></span>

## <a name="multiple-message-parts-support"></a><span data-ttu-id="6f5c2-221">Supporto per più parti del messaggio</span><span class="sxs-lookup"><span data-stu-id="6f5c2-221">Multiple message parts support</span></span>

<span data-ttu-id="6f5c2-222">Wsutil.exe supporta più parti del messaggio in un messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-222">Wsutil.exe supports multiple message parts in one message.</span></span> <span data-ttu-id="6f5c2-223">Un messaggio multiparte può essere specificato come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-223">A multi-part message can be specified as follows:</span></span>

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

<span data-ttu-id="6f5c2-224">Wsutil.exe genera un campo di [**\_ \_ tipo struct WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) per l'elemento Message se il messaggio contiene più parti.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-224">Wsutil.exe generates a [**WS\_STRUCT\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) field for the message element if the message contains multiple parts.</span></span> <span data-ttu-id="6f5c2-225">Se il messaggio viene rappresentato utilizzando lo stile del documento, Wsutil.exe genera un elemento wrapper con tipo struct.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-225">If the message is represented using the document style, Wsutil.exe generates a wrapper element with struct type.</span></span> <span data-ttu-id="6f5c2-226">L'elemento wrapper non ha un nome o uno spazio dei nomi specifico e la struttura wrapper contiene tutti gli elementi in tutte le parti come campi.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-226">The wrapper element does not have a name or a specific namespace, and the wrapper structure contains all of the elements in all of the parts as fields.</span></span> <span data-ttu-id="6f5c2-227">L'elemento wrapper è solo per uso interno e non verrà serializzato nel corpo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-227">The wrapper element is for internal use only and it will not be serialized in the message body.</span></span>

<span data-ttu-id="6f5c2-228">Se il messaggio utilizza la rappresentazione di stile RPC o Literal, Wsutil.exe crea un elemento wrapper con il nome dell'operazione come nome dell'elemento e lo spazio dei nomi specificato come spazio dei nomi del servizio in base alla specifica dell'estensione SOAP WSDL.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-228">If the message is using RPC or literal style representation , Wsutil.exe creates a wrapper element with the operation name as the element name and the specified namespace as service namespace according to WSDL SOAP extension specification.</span></span> <span data-ttu-id="6f5c2-229">La struttura dell'elemento contiene una matrice di campi che rappresentano i tipi specificati nelle parti del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-229">The structure of the element contains an array of fields representing the types specified in the message parts.</span></span> <span data-ttu-id="6f5c2-230">L'elemento wrapper viene mappato all'elemento superiore effettivo nel corpo del messaggio, come indicato nella specifica SOAP.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-230">The wrapper element is mapped to the actual top element in message body as indicated in the SOAP specification.</span></span>

<span data-ttu-id="6f5c2-231">Sul lato server, ogni operazione genera un typedef dell'operazione del servizio server risultante.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-231">On the server side, each operation results in a typedef of the resulting server service operation.</span></span> <span data-ttu-id="6f5c2-232">Questo typedef viene usato per fare riferimento all'operazione nella tabella Function come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-232">This typedef is used to refer to the operation in the function table as described previously.</span></span> <span data-ttu-id="6f5c2-233">Ogni operazione comporta inoltre la generazione di una funzione stub che nfrastructure chiamate per conto del delegato al metodo effettivo.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-233">Every operation also results in the generation of a stub function which nfrastructure calls on behalf of the delegate to the actual method.</span></span>

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

<span data-ttu-id="6f5c2-234">Per l'operazione SimpleMethod, il typedef SimpleMethodOperation è definito sopra.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-234">For the SimpleMethod operation, the SimpleMethodOperation typedef is defined above.</span></span> <span data-ttu-id="6f5c2-235">Si noti che il metodo generato presenta un argomento espanso listwith la parte del messaggio per il messaggio di input e di output per l'operazione SimpleMethod come parametri denominati.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-235">Note that the generated method has an expanded argument listwith the message part for the input and output message for SimpleMethod operation as named parameters.</span></span>

<span data-ttu-id="6f5c2-236">Sul lato client viene eseguito il mapping di ogni operazione a un'operazione del servizio proxy.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-236">On the client side each operation is mapped to a proxy service operation.</span></span>

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

## <a name="processing-wsdlbinding"></a><span data-ttu-id="6f5c2-237">Elaborazione di WSDL: binding</span><span class="sxs-lookup"><span data-stu-id="6f5c2-237">Processing wsdl:binding</span></span>

<span data-ttu-id="6f5c2-238">Il modello di servizio WWSAPI supporta l'estensione di binding II saponeho.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-238">The WWSAPI service model supports theSOAP binding extension.</span></span> <span data-ttu-id="6f5c2-239">Per ogni binding è presente un **portType** associato.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-239">For each binding there is an associated **portType**.</span></span>

<span data-ttu-id="6f5c2-240">Il trasporto specificato nell'estensione di binding SOAP è solo consultivo.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-240">The transport specified in soap binding extension is advisory only.</span></span> <span data-ttu-id="6f5c2-241">Quando si crea un canale, l'applicazione deve fornire informazioni sul trasporto.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-241">Application needs to provide transport information when creating a channel.</span></span> <span data-ttu-id="6f5c2-242">Attualmente sono supportate le associazioni WS \_ http \_ Binding e WS \_ TCP binding \_ .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-242">Currently we support the WS\_HTTP\_BINDING and WS\_TCP\_BINDING bindings.</span></span>

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

<span data-ttu-id="6f5c2-243">Nel documento WSDL di esempio è presente un solo **portType** per ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-243">In our example WSDL document we only have one **portType** for ISimpleService.</span></span> <span data-ttu-id="6f5c2-244">L'associazione SOAP fornita indica il trasporto HTTP, specificato come \_ binding WS http \_ .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-244">The provided SOAP binding indicates the HTTP transport, which is specified as WS\_HTTP\_BINDING.</span></span> <span data-ttu-id="6f5c2-245">Si noti che questa struttura non ha un effetto statico perché questa struttura deve essere disponibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-245">Notice that this structure does not have static decoration as this structure needs to be available to the application.</span></span>

<span data-ttu-id="6f5c2-246">Elaborazione di WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="6f5c2-246">Processing wsdl:portType</span></span>

<span data-ttu-id="6f5c2-247">Ogni **portType** in WSDL è costituito da una o più operazioni.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-247">Each **portType** in WSDL is made up of one or more operations.</span></span> <span data-ttu-id="6f5c2-248">L'operazione deve essere coerente con l'estensione di binding SOAP indicata in WSDL: binding.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-248">The operation should be consistent with the SOAP binding extension indicated in wsdl:binding.</span></span>

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

<span data-ttu-id="6f5c2-249">In questo esempio, l'oggetto **portType** ISimpleService contiene solo l'operazione SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-249">In this example, the ISimpleService **portType** only contains the SimpleMethod operation.</span></span> <span data-ttu-id="6f5c2-250">Questo comportamento è coerente con la sezione dell'associazione in cui è presente una sola operazione WSDL mappata a un'azione SOAP.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-250">This is consistent with the binding section where there is only one WSDL operation that maps to a SOAP action.</span></span>

<span data-ttu-id="6f5c2-251">Poiché l'oggetto **portType** ISimpleService dispone solo di un'operazione--SimpleMethod, la tabella di funzioni corrispondente contiene solo SimpleMethod come operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-251">Since the ISimpleService **portType** only has one operation -- SimpleMethod -- the corresponding function table only contains SimpleMethod as a service operation.</span></span>

<span data-ttu-id="6f5c2-252">In termini di metadati, ogni **portType** viene mappato da Wsutil.exe a una [**\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span><span class="sxs-lookup"><span data-stu-id="6f5c2-252">In terms of metadata each **portType** is mapped by Wsutil.exe to a [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span></span> <span data-ttu-id="6f5c2-253">Ogni operazione all'interno di **portType** viene mappata a una [**\_ \_ Descrizione dell'operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span><span class="sxs-lookup"><span data-stu-id="6f5c2-253">Each operation within a **portType** is mapped to a [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span></span>

<span data-ttu-id="6f5c2-254">In questo esempio **portType** lo strumento genera la [**\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) per ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-254">In this example, **portType** the tool generates [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for ISimpleService.</span></span> <span data-ttu-id="6f5c2-255">Questa descrizione del contratto contiene il numero specifico di operazioni disponibili nell' **portType** ISimpleService insieme a una matrice di [**\_ \_ Descrizione dell'operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) che rappresenta le singole operazioni definite nell'PortType per ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-255">This contract description contains the specific number of operations available on the ISimpleService **portType** along with an array of [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) representing the individual operations defined on the portType for ISimpleService.</span></span> <span data-ttu-id="6f5c2-256">Poiché è presente una sola operazione in ISimpleService portType for ISimpleService, è presente anche una sola definizione di **\_ \_ Descrizione dell'operazione WS** .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-256">Since there is only one operation on ISimpleService portType for ISimpleService, there is also only one **WS\_OPERATION\_DESCRIPTION** definition.</span></span>

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

## <a name="processing-wsdlservice"></a><span data-ttu-id="6f5c2-257">Elaborazione di WSDL: Service</span><span class="sxs-lookup"><span data-stu-id="6f5c2-257">Processing wsdl:service</span></span>

<span data-ttu-id="6f5c2-258">WsUtil.exe usa i servizi per trovare binding/PortTypes e genera la struttura del contratto che descrive i tipi, i messaggi, le definizioni PortType e così via.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-258">WsUtil.exe uses the services to find binding/porttypes, and generates contract structure that describes types, message, porttype definitions, and so on.</span></span> <span data-ttu-id="6f5c2-259">Le descrizioni dei contratti sono accessibili esternamente e vengono generate come parte della struttura di definizione globale specificata tramite l'intestazione generata.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-259">Contract descriptions are externally accessible, and they are generated as part of the global definition structure specified through generated header.</span></span>

<span data-ttu-id="6f5c2-260">WsUtil.exe supporta le estensioni EndpointReference definite in WSDL: Port.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-260">WsUtil.exe supports EndpointReference extensions defined in wsdl:port.</span></span> <span data-ttu-id="6f5c2-261">Il riferimento all'endpoint è definito in WS-Addressing come modo per descrivere le informazioni sugli [endpoint](endpoint-address.md) di un servizio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-261">Endpoint reference is defined in WS-ADDRESSING as a way to describe [endpoint](endpoint-address.md) information of a service.</span></span> <span data-ttu-id="6f5c2-262">Il testo dell'estensione di riferimento dell'endpoint di input salvato come [**\_ \_ stringa WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), insieme alla [**Descrizione dell' \_ \_ indirizzo \_ WS endpoint**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) corrispondente viene generato nella sezione endpointReferences della struttura globale.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-262">The input endpoint reference extension text saved as [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), together with matching [**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) are generated in endpointReferences section in the global structure.</span></span>

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

<span data-ttu-id="6f5c2-263">Per creare [**l' \_ \_ indirizzo dell'endpoint WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) usando i metadati generati da WsUtil:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-263">To Create [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) using the WsUtil generated metadata:</span></span>

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

<span data-ttu-id="6f5c2-264">Le stringhe costanti nel proxy client o nello stub del servizio vengono generate come campi di tipo \_ stringa WS XML \_ ed è presente un dizionario costante per tutte le stringhe nel file di proxy o stub.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-264">Constant strings in the client proxy or service stub are generated as fields of type WS\_XML\_STRING, and there is a constant dictionary for all the strings in the proxy or stub file.</span></span> <span data-ttu-id="6f5c2-265">Ogni stringa nel dizionario viene generata come campo nella parte del dizionario della struttura locale per una migliore leggibilità.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-265">Each string in the dictionary is generated as a field in the dictionary part of the local structure for better readability.</span></span>

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

## <a name="processing-wsdltype"></a><span data-ttu-id="6f5c2-266">Elaborazione di WSDL: Type</span><span class="sxs-lookup"><span data-stu-id="6f5c2-266">Processing wsdl:type</span></span>

<span data-ttu-id="6f5c2-267">Wsutil.exe supporta solo documenti XML Schema (XSD) nella specifica WSDL: Type.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-267">Wsutil.exe only supports XML schema (XSD) documents in wsdl:type specification.</span></span> <span data-ttu-id="6f5c2-268">Un caso speciale è quando una porta del messaggio specifica una definizione di elemento globale.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-268">One special case is when a message port specifies a global element definition.</span></span> <span data-ttu-id="6f5c2-269">Vedere la sezione seguente per altri dettagli sull'euristica usata in questi casi.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-269">See the following section for more details of the heuristics used in these cases.</span></span>

## <a name="parameter-processing-heuristics"></a><span data-ttu-id="6f5c2-270">Euristica di elaborazione dei parametri</span><span class="sxs-lookup"><span data-stu-id="6f5c2-270">Parameter Processing Heuristics</span></span>

<span data-ttu-id="6f5c2-271">Nel modello del servizio, viene eseguito il mapping dei messaggi WSDL a parametri specifici in un metodo.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-271">In the service model, WSDL messages are mapped to specific parameters in a method.</span></span> <span data-ttu-id="6f5c2-272">Wsutil.exe dispone di due stili di generazione del parametro: nel primo stile, l'operazione include un parametro per il messaggio di input e un parametro per il messaggio di output (se necessario); nel secondo stile, Wsutil.exe usa un approccio euristico per eseguire il mapping e l'espansione dei campi nelle strutture sia per i messaggi di input che per quelli di output a parametri diversi dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-272">Wsutil.exe has two styles of parameter generation: in first style, the operation has one parameter for input message, and one parameter for output message (if necessary); in the second style, Wsutil.exe uses a heuristic to map and expand fields in the structures for both input messages and output messages to different parameters in the operation.</span></span> <span data-ttu-id="6f5c2-273">I messaggi di input e di output devono avere elementi del messaggio di tipo struttura per generare questo secondo approccio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-273">Both input and output messages need to have structure type message elements to generate this second approach.</span></span>

<span data-ttu-id="6f5c2-274">Wsutil.exe usa le regole seguenti per la generazione di parametri dell'operazione dai messaggi di input e di output:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-274">Wsutil.exe uses the following rules when generating operation parameters from the input and output messages:</span></span>

-   <span data-ttu-id="6f5c2-275">Per i messaggi di input e di output con più parti del messaggio, ogni parte del messaggio è un parametro separato nell'operazione con il nome della parte del messaggio come nome di parametro.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-275">For input and output messages with multiple message parts, each message part is a separate parameter in the operation, with the message part name as parameter name.</span></span>
-   <span data-ttu-id="6f5c2-276">Per il messaggio di tipo RPC con una parte del messaggio, la parte del messaggio è un parametro dell'operazione, con il nome della parte del messaggio come nome di parametro.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-276">For RPC style message with one message part, the message part is a parameter in the operation, with message part name as parameter name.</span></span>
-   <span data-ttu-id="6f5c2-277">Per i messaggi di input e di output di tipo documento con una parte del messaggio:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-277">For document-style input and output messages with one message part:</span></span>
    -   <span data-ttu-id="6f5c2-278">Se il nome di una parte del messaggio è "Parameters" e il tipo di elemento è una struttura, ogni campo nella struttura viene considerato come un parametro separato con il nome del campo che corrisponde al nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-278">If the name of a message part is "parameters" and the element type is a structure, each field in the structure is treated as a separate parameter with the field name being the parameter name.</span></span>
    -   <span data-ttu-id="6f5c2-279">Se il nome della parte del messaggio non è "Parameters", il messaggio è un parametro dell'operazione con il nome del messaggio utilizzato come nome di parametro corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-279">If the message part name is not "parameters", the message is a parameter in the operation with the message name used as the corresponding parameter name.</span></span>
-   <span data-ttu-id="6f5c2-280">Per il messaggio di input e output di stile del documento con l'elemento nillable, il messaggio viene mappato a un parametro, con il nome della parte del messaggio come nome di parametro.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-280">For document style input and output message with nillable element, the message is mapped to one parameter, with message part name as parameter name.</span></span> <span data-ttu-id="6f5c2-281">Viene aggiunto un ulteriore livello di riferimento indiretto per indicare che il puntatore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-281">One additional level of indirection is added to indicate the pointer can be **NULL**.</span></span>
-   <span data-ttu-id="6f5c2-282">Se un campo viene visualizzato solo nell'elemento del messaggio di input, il campo viene considerato come un \[ \] parametro in.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-282">If a field appears in the input message element only, the field is treated as an \[in\] parameter.</span></span>
-   <span data-ttu-id="6f5c2-283">Se un campo viene visualizzato solo nell'elemento del messaggio di output, il campo viene considerato come un \[ \] parametro out.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-283">If a field appears in the output message element only, the field is treated as an \[out\] parameter.</span></span>
-   <span data-ttu-id="6f5c2-284">Se è presente un campo con lo stesso nome e lo stesso tipo visualizzato sia nel messaggio di input che nel messaggio di output, il campo viene considerato come un \[ parametro in, out \] .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-284">If there is a field with the same name and same type that appears in both the input message and the output message, the field is treated as an \[in,out\] parameter.</span></span>

<span data-ttu-id="6f5c2-285">Per determinare la direzione dei parametri vengono usati gli strumenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-285">Following tools are used to determine the direction of parameters:</span></span>

-   <span data-ttu-id="6f5c2-286">Se un campo viene visualizzato solo nell'elemento input Message, il campo viene considerato come solo parametro.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-286">If a field appears in input message element only, the field is treated as in only parameter.</span></span>
-   <span data-ttu-id="6f5c2-287">Se un campo viene visualizzato solo nell'elemento del messaggio di output, il campo viene considerato solo come parametro out.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-287">If a field appears in output message element only, the field is treated as out only parameter.</span></span>
-   <span data-ttu-id="6f5c2-288">Se è presente un campo con lo stesso nome e lo stesso tipo visualizzato nel messaggio di input e di output, il campo viene considerato come un parametro in, out.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-288">If there is a field with the same name and same type that appears in both input message and output message, the field is treated as an in,out parameter.</span></span>

<span data-ttu-id="6f5c2-289">Wsutil.exe supporta solo gli elementi in sequenza.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-289">Wsutil.exe only supports sequenced elements.</span></span> <span data-ttu-id="6f5c2-290">Rifiuta l'ordinamento non valido per quanto riguarda \[ i parametri in, out \] se Wsutil.exe non è in grado di combinare i parametri in e out in un unico elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-290">It rejects invalid ordering with regard to \[in,out\] parameters if Wsutil.exe cannot combine the in parameters and out parameters into a single parameter list.</span></span> <span data-ttu-id="6f5c2-291">I suffissi possono essere aggiunti ai nomi dei parametri per evitare conflitti di nomi.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-291">Suffixes might be added to parameter names to avoid name collision.</span></span>

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

<span data-ttu-id="6f5c2-292">Wsutil.exe considera i campi in TNS: SimpleMethod e TNS: SimpleMethodResponse ato be Parameters, come illustrato nelle definizioni dei parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-292">Wsutil.exe considers fields in tns:SimpleMethod and tns:SimpleMethodResponse ato be parameters, as seen in the parameter definitions below:</span></span>

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

<span data-ttu-id="6f5c2-293">Wsutil.exe espande l'elenco dei parametri dai campi nell'elenco precedente e genera la struttura **ParamStruct** nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-293">Wsutil.exe expands the parameter list from the fields in the list above, and generates the **ParamStruct** structure in the following code example.</span></span> <span data-ttu-id="6f5c2-294">Il modello di servizio in fase di esecuzione può utilizzare questa struttura per passare argomenti agli stub client e server.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-294">The service model run-time can use this structure to pass arguments to the client and server stubs.</span></span>

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

<span data-ttu-id="6f5c2-295">Questa struttura viene utilizzata solo per descrivere il stack frame sul lato client e server.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-295">This structure is only used to describe the stack frame on the client and server side.</span></span> <span data-ttu-id="6f5c2-296">Non viene apportata alcuna modifica alla descrizione del messaggio o alle descrizioni degli elementi a cui fa riferimento la descrizione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-296">There is no change to the message description, or to the element descriptions referenced by the message description.</span></span>

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

<span data-ttu-id="6f5c2-297">Come regola generale, viene aggiunto un livello di riferimento indiretto per tutti i \[ parametri out \] e \[ in out \] .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-297">As a general rule, one level of indirection is added for all the \[out\] and \[in,out\] parameters.</span></span>

## <a name="parameterless-operation"></a><span data-ttu-id="6f5c2-298">Operazione senza parametri</span><span class="sxs-lookup"><span data-stu-id="6f5c2-298">Parameterless operation</span></span>

<span data-ttu-id="6f5c2-299">Per le operazioni di documenti e valori letterali, Wsutil.exe considera l'operazione come un parametro di input e un parametro di output se:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-299">For document and literal operations, Wsutil.exe treats the operation as having one input parameter and one output parameter if:</span></span>

-   <span data-ttu-id="6f5c2-300">Il messaggio di input o di output ha più di una parte.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-300">The input or output message has more than one part.</span></span>
-   <span data-ttu-id="6f5c2-301">Esiste solo una parte del messaggio e il nome della parte del messaggio non è "Parameters".</span><span class="sxs-lookup"><span data-stu-id="6f5c2-301">There is only one message part and the message part name is not "parameters".</span></span>

<span data-ttu-id="6f5c2-302">..</span><span class="sxs-lookup"><span data-stu-id="6f5c2-302">..</span></span> <span data-ttu-id="6f5c2-303">Nell'esempio precedente, supponendo che le parti del messaggio siano denominate *Paramin*"e *param* out, la firma del metodo diventa il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-303">In the example above, assuming the message parts are named *ParamIn*" and *ParamOut*, the method signature becomes the following code:</span></span>

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

<span data-ttu-id="6f5c2-304">Wsutil.exe genera una firma di versione per la descrizione dell'operazione in modo che il motore del modello di servizio WsCall e lato server possa verificare se la descrizione generata è applicabile per la piattaforma corrente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-304">Wsutil.exe generates a version signature for the operation description such that the WsCall and server-side service model engine can check if the generated description is applicable for the current platform.</span></span>

<span data-ttu-id="6f5c2-305">Queste informazioni sulla versione vengono generate come parte della struttura della [**\_ \_ Descrizione dell'operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-305">This version info is generated as part of the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) structure.</span></span> <span data-ttu-id="6f5c2-306">Il numero di versione può essere considerato come un selettore ARM Unione per rendere estendibile la struttura.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-306">The version number can be treated as a union arm selector to make the structure extensible.</span></span> <span data-ttu-id="6f5c2-307">Attualmente, il **VersionId** è impostato su TO1 senza campi successivi.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-307">Currently, the **versionID** is set to1 with no subsequent fields.</span></span> <span data-ttu-id="6f5c2-308">I versiosn futuri possono incrementare il numero di versione e includere più campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-308">Future versiosn may increment the version number and include more fields as needed.</span></span> <span data-ttu-id="6f5c2-309">Ad esempio, Wsutil.exe genera attualmente il codice seguente in base all'ID versione:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-309">For example, Wsutil.exe currently generates the following code based on the version ID:</span></span>

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

<span data-ttu-id="6f5c2-310">In futuro, potrebbe essere espansa come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6f5c2-310">In the future, it could be expanded as follows:</span></span>

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

## <a name="security"></a><span data-ttu-id="6f5c2-311">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="6f5c2-311">Security</span></span>

<span data-ttu-id="6f5c2-312">Vedere la sezione sicurezza nell'argomento [dello strumento del compilatore WSUTIL](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-312">See the security section in the [Wsutil Compiler tool](wsutil-compiler-tool.md) topic.</span></span>

 

 




