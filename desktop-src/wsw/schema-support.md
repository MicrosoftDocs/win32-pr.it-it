---
title: Supporto degli schemi
description: WsUtil.exe supporta lo schema XSD specificato in XML Schema.
ms.assetid: 33096cda-9dbe-44d2-8d08-410bc33ae81c
keywords:
- Servizi Web di supporto dello schema per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dcf9d192c999333ee8b4e341e7722cd6bd59ff5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103956223"
---
# <a name="schema-support"></a><span data-ttu-id="00dd9-106">Supporto degli schemi</span><span class="sxs-lookup"><span data-stu-id="00dd9-106">Schema support</span></span>

<span data-ttu-id="00dd9-107">WsUtil.exe supporta lo schema XSD specificato in [XML Schema](https://www.w3.org/XML/Schema).</span><span class="sxs-lookup"><span data-stu-id="00dd9-107">WsUtil.exe supports the XSD schema specified at [XML Schema](https://www.w3.org/XML/Schema).</span></span> <span data-ttu-id="00dd9-108">il file XSD e WSDL: Type devono essere trattati nella stessa categoria, con l'eccezione in WSDL: Type quando un elemento globale può essere un elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="00dd9-108">xsd file and wsdl:type should be treated in the same category, with the exception in wsdl:type when a global element could be a parameter list.</span></span> <span data-ttu-id="00dd9-109">Wsutil.exe genera descrizioni di elementi per tutte le definizioni di elemento globali che possono essere utilizzate nel serializzatore, con output aggiuntivo per la struttura di parametri specificata nel [supporto WSDL](wsdl-support.md).</span><span class="sxs-lookup"><span data-stu-id="00dd9-109">Wsutil.exe generates element descriptions for all global element definitions that can be used in serializer, with additional output for parameter structure specified in [WSDL support](wsdl-support.md).</span></span>

## <a name="xsd-schema-support-level"></a><span data-ttu-id="00dd9-110">Livello di supporto dello schema XSD</span><span class="sxs-lookup"><span data-stu-id="00dd9-110">XSD Schema Support Level</span></span>

<span data-ttu-id="00dd9-111">WsUtil.exe non supporta l'intera estensione dello schema XSD.</span><span class="sxs-lookup"><span data-stu-id="00dd9-111">WsUtil.exe does not support the full extent of XSD schema.</span></span> <span data-ttu-id="00dd9-112">Il livello di supporto corrente viene definito nel [livello di supporto dello schema](schema-support-level.md).</span><span class="sxs-lookup"><span data-stu-id="00dd9-112">The current support level is defined in [Schema support level](schema-support-level.md).</span></span>

<span data-ttu-id="00dd9-113">Generazione di identificatori</span><span class="sxs-lookup"><span data-stu-id="00dd9-113">Identifier generation</span></span>

<span data-ttu-id="00dd9-114">Il nome dell'elemento o il nome del tipo nello schema potrebbe non essere un identificatore C valido e i nomi vengono normalizzati in nomi C validi generati.</span><span class="sxs-lookup"><span data-stu-id="00dd9-114">Element name or type name in the schema might not be valid C identifier, and the names are normalized to generated valid C names.</span></span> <span data-ttu-id="00dd9-115">I caratteri dell'identificatore C non validi vengono convertiti nel nome esadecimale e il carattere di sottolineatura ' \_ ' potrebbe essere preceduto dal nome, se necessario.</span><span class="sxs-lookup"><span data-stu-id="00dd9-115">Invalid C identifier characters are converted to the hex name, and a underscore '\_' might be prefixed to the name if necessary.</span></span> <span data-ttu-id="00dd9-116">I tipi anonimi vengono denominati dopo il nome dell'elemento di inclusione, ma con il carattere di sottolineatura " \_ " per evitare conflitti di nomi.</span><span class="sxs-lookup"><span data-stu-id="00dd9-116">Anonymous types are named after the enclosing element name but prefixed with underscore "\_" to avoid name collision.</span></span> <span data-ttu-id="00dd9-117">I nomi dei tipi globali vengono conservati così come sono dopo la normalizzazione di caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="00dd9-117">Global type names are preserved as it is after invalid characters are normalized.</span></span> <span data-ttu-id="00dd9-118">I tipi anonimi annidati sono preceduti dal nome del tipo padre.</span><span class="sxs-lookup"><span data-stu-id="00dd9-118">Nested anonymous types are prefixed with the parent type name.</span></span>

<span data-ttu-id="00dd9-119">Per ogni definizione di elemento globale, wsutil.exe genera [**una \_ \_ Descrizione dell'elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) nella struttura di descrizione globale.</span><span class="sxs-lookup"><span data-stu-id="00dd9-119">For every global element definition, wsutil.exe generates a [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) in the global description structure.</span></span> <span data-ttu-id="00dd9-120">Per ogni definizione di tipo globale, wsutil.exe genera una descrizione del tipo nella struttura di descrizione globale a cui fa riferimento l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="00dd9-120">For every global type definition, wsutil.exe generates a type description in the global description structure to be referenced by application.</span></span>

<span data-ttu-id="00dd9-121">Per ogni campo nella struttura, wsutil.exe genera una [**Descrizione del \_ campo \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) incorporata come parte della struttura dell'enclosure.</span><span class="sxs-lookup"><span data-stu-id="00dd9-121">For each field in the structure, wsutil.exe generates a [**WS\_FIELD\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) embedded as part of the enclosure structure.</span></span>

## <a name="simple-types"></a><span data-ttu-id="00dd9-122">Tipi semplici</span><span class="sxs-lookup"><span data-stu-id="00dd9-122">Simple Types</span></span>

<span data-ttu-id="00dd9-123">I tipi di valore, elencati [**nel \_ \_ tipo di valore WS**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), vengono considerati tipi semplici.</span><span class="sxs-lookup"><span data-stu-id="00dd9-123">Value types, as listed in [**WS\_VALUE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), are treated as simple types.</span></span> <span data-ttu-id="00dd9-124">Si noti che \_ \_ il tipo di valore WS è effettivamente un subset di [**WS \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span><span class="sxs-lookup"><span data-stu-id="00dd9-124">Notice that WS\_VALUE\_TYPE is really a subset of [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="00dd9-125">Sono inclusi i tipi di dati integrali e float di base, nonché decimali, WS \_ DateTime e UUID.</span><span class="sxs-lookup"><span data-stu-id="00dd9-125">It includes basic integral and float data types, as well as DECIMAL, WS\_DATETIME, and UUID.</span></span>

<span data-ttu-id="00dd9-126">Nel modello di servizio, nei tipi semplici vengono passati per valore, mentre in uscita e in i tipi semplici vengono passati per riferimento.</span><span class="sxs-lookup"><span data-stu-id="00dd9-126">In service model, in simple types are passed by value, while out and in,out simple types are passed by reference.</span></span>

<span data-ttu-id="00dd9-127">Wsutil creare una descrizione semplice dell'elemento come la seguente per l'elemento globale contenente tipi semplici.</span><span class="sxs-lookup"><span data-stu-id="00dd9-127">Wsutil create simple element description like below for global element containing simple types.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

<span data-ttu-id="00dd9-128">Wsutil genera la descrizione dell'elemento seguente:</span><span class="sxs-lookup"><span data-stu-id="00dd9-128">Wsutil generates the element description below:</span></span>

``` syntax
...  // global elements
{ // helloworld
{
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeNamespace,
WS_INT32_TYPE,
0,
},
}, // helloworld
... 
```

<span data-ttu-id="00dd9-129">Questa struttura viene generata come parte della struttura di descrizione globale generata nel file di intestazione:</span><span class="sxs-lookup"><span data-stu-id="00dd9-129">This structure is generated as part of the global description structure generated in header file:</span></span>

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a><span data-ttu-id="00dd9-130">Matrici</span><span class="sxs-lookup"><span data-stu-id="00dd9-130">Arrays</span></span>

<span data-ttu-id="00dd9-131">L'elemento con maxOccurs maggiore di 1 o una sequenza con un solo elemento e l'elemento figlio ha un maxOccurs maggiore di 1, viene trattato come matrice.</span><span class="sxs-lookup"><span data-stu-id="00dd9-131">Element with maxOccurs larger than 1, or sequence with only one item, and the child element has maxOccurs larger than 1, is treated as array.</span></span> <span data-ttu-id="00dd9-132">Per un elemento di matrice nello schema, wsutil.exe genera due campi: un campo di conteggio che non è in transito e un campo del puntatore che contiene il tipo di matrice.</span><span class="sxs-lookup"><span data-stu-id="00dd9-132">For an array element in schema, wsutil.exe generates two fields: one count field that does not go on wire, and one pointer field containing the array type.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleArray">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" maxOccurs="50" name="a" nillable="true" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="00dd9-133">Il file di intestazione contiene la definizione della struttura C per la matrice, con l'account di campo che specifica il numero della matrice.</span><span class="sxs-lookup"><span data-stu-id="00dd9-133">Header file contains the C structure definition for the array, with field aCount specifying the count of the array.</span></span>

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

<span data-ttu-id="00dd9-134">Il codice seguente fa parte del prototipo LocalDefinition che descrive la matrice:</span><span class="sxs-lookup"><span data-stu-id="00dd9-134">Following is part of the LocalDefinition prototype describing the array:</span></span>

``` syntax
... // globalElement part of the LocalDefinitions.
struct // SimpleArray
{
  struct // SimpleArray
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION * SimpleArrayFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArraydescs; // SimpleArray
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArray;

// Method with array parameters.
  typedef HRESULT (CALLBACK *SimpleMethodCallback)(
    const WS_OPERATION_CONTEXT* context,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);

  HRESULT CALLBACK SimpleMethod (
    WS_SERVICE_PROXY* serviceProxy,
    WS_HEAP* heap,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);
```

<span data-ttu-id="00dd9-135">Di seguito sono riportate le definizioni generate delle descrizioni precedenti. si noti il \_ mapping del campo dell'elemento ripetuto WS \_ \_ \_ che indica il campo come campo di matrice.</span><span class="sxs-lookup"><span data-stu-id="00dd9-135">Following is the generated definitions of the above descriptions, notice the WS\_REPEATING\_ELEMENT\_FIELD\_MAPPING which indicates the field as an array field.</span></span>

``` syntax
...
{ // SimpleArray
  {   // SimpleArray
    { // field description for a
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      0,
      0,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArray, a),
      0,
      0,
      WsOffsetOf(SimpleArray, aCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },    // end of field description for a
    {    // fields description for SimpleArray
      (WS_FIELD_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.a,
    },
    {
      sizeof(SimpleArray),
      __alignof(SimpleArray),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.
      SimpleArrayFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.SimpleArrayFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },   // struct description for SimpleArray
  },    // SimpleArray
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.structDesc,
  },
}, // SimpleArray
...
```

<span data-ttu-id="00dd9-136">Se la matrice è un campo di parametri nel messaggio di input/output, verranno generati due parametri effettivi per il metodo.</span><span class="sxs-lookup"><span data-stu-id="00dd9-136">If the array is a parameter field in input/output message, there would be two actual parameters generated for the method.</span></span> <span data-ttu-id="00dd9-137">Se la matrice è un parametro out o in, out, esiste un ulteriore livello di riferimento indiretto per entrambi i campi in paramStruct.</span><span class="sxs-lookup"><span data-stu-id="00dd9-137">If the array is an out or in,out parameter, there would be one additional level of indirection for both fields in paramStruct.</span></span>

## <a name="range-on-array"></a><span data-ttu-id="00dd9-138">Intervallo sulla matrice</span><span class="sxs-lookup"><span data-stu-id="00dd9-138">Range on Array</span></span>

<span data-ttu-id="00dd9-139">Si consiglia di non specificare maxOccur = "unbounded" per le matrici.</span><span class="sxs-lookup"><span data-stu-id="00dd9-139">We recommend the best practice of not specifying maxOccur="unbounded" for arrays.</span></span> <span data-ttu-id="00dd9-140">È invece necessario specificare un numero intero fisso per impostare un limite superiore del numero di matrici consentito.</span><span class="sxs-lookup"><span data-stu-id="00dd9-140">Instead, a fixed integer number should be specified to set a upper bound of array counts allowed.</span></span> <span data-ttu-id="00dd9-141">l'intervallo è supportato per i tipi integrali, nonché per stringhe, matrici di byte e matrici generiche.</span><span class="sxs-lookup"><span data-stu-id="00dd9-141">range is supported for integral types, as well as strings, byte arrays, and generic arrays.</span></span>

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a><span data-ttu-id="00dd9-142">Euristica per cui è stato eseguito il wrapped anziché la matrice</span><span class="sxs-lookup"><span data-stu-id="00dd9-142">Heuristic for Wrapped as Opposed to Unwrapped array</span></span>

<span data-ttu-id="00dd9-143">A volte le matrici vengono incapsulate all'interno di un'altra struttura per essere incorporate in una struttura di primo livello.</span><span class="sxs-lookup"><span data-stu-id="00dd9-143">Sometimes arrays are wrapped inside another structure to be embedded in a top level structure.</span></span> <span data-ttu-id="00dd9-144">In tal caso, è necessario rimuovere il livello wrapper intermedio.</span><span class="sxs-lookup"><span data-stu-id="00dd9-144">In that case, we should remove the intermediate wrapper layer.</span></span> <span data-ttu-id="00dd9-145">WsUtil.exe genera lo stesso prototipo e le stesse descrizioni di SimpleArray descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="00dd9-145">WsUtil.exe generates the same prototype and descriptions as SimpleArray described above.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="SimpleArray">
  <xs:sequence>
   <xs:element minOccurs="0" maxOccurs="50" name="aa" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="SimpleArrayWrapper">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="SimpleArray" type="tns:SimpleArray" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="00dd9-146">Wsutil rileva che SimpleArrayWrapper è un wrapper per SimpleArray e genera solo le strutture seguenti, con una struttura separata per SimpleArray</span><span class="sxs-lookup"><span data-stu-id="00dd9-146">Wsutil detects that SimpleArrayWrapper is a wrapper around SimpleArray, and generates following structures only, with separate structure for SimpleArray</span></span>

``` syntax
typedef struct SimpleArrayWrapper
{
  unsigned int  SimpleArrayCount ;
  int  * SimpleArray;
} SimpleArrayWrapper;

.. // global element inside the LocalDefinitions prototype
struct // SimpleArrayWrapper
{
  struct // SimpleArrayWrapper
  {
    WS_FIELD_DESCRIPTION SimpleArray;
    WS_FIELD_DESCRIPTION * SimpleArrayWrapperFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArrayWrapperdescs; // SimpleArrayWrapper
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArrayWrapper;
...
```

<span data-ttu-id="00dd9-147">wsutil.exe genera le seguenti definizioni per il prototipo corrispondente riportato sopra. si noti che nella descrizione del campo i campi nome wrapper e spazio dei nomi wrapper sono compilati</span><span class="sxs-lookup"><span data-stu-id="00dd9-147">wsutil.exe generates the following definitions for the matching prototype above, notices that in the field description, the wrapper name and wrapper namespace fields are filled in</span></span>

``` syntax
... // global element part of the LocalDefinitions structure:
{ // SimpleArrayWrapper
  {   // SimpleArrayWrapper
    { // WS_FIELD_DESCRIPTION  for SimpleArray
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArray),
      0,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArrayCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },    // end of field description for SimpleArray
    {    // array of field descriptions for SimpleArrayWrapper
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArray,
    },
    {  // WS_STRUCT_DESCRIPTION for SimpleArrayWrapper
      sizeof(SimpleArrayWrapper),
      __alignof(SimpleArrayWrapper),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },   // struct description for SimpleArrayWrapper
    },    // SimpleArrayWrapper
  {  // WS_ELEMENT_DESCRIPTION for SimpleArrayWrapper
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.structDesc,
  },
}, // SimpleArrayWrapper
```

## <a name="structures"></a><span data-ttu-id="00dd9-148">Strutture</span><span class="sxs-lookup"><span data-stu-id="00dd9-148">Structures</span></span>

<span data-ttu-id="00dd9-149">Un complexType con più elementi in una sequenza è una struttura.</span><span class="sxs-lookup"><span data-stu-id="00dd9-149">A complexType with multiple elements in a sequence is a structure.</span></span> <span data-ttu-id="00dd9-150">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="00dd9-150">For example,</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="StructType">
  <xs:sequence>
   <xs:element minOccurs="0" name="FirstName" nillable="true" type="xs:string" />
   <xs:element minOccurs="0" name="LastName" nillable="true" type="xs:string" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="StructType" nillable="true" type="tns:StructType" />
</xs:schema>
```

<span data-ttu-id="00dd9-151">Wsutil.exe genera un prototipo di struttura come:</span><span class="sxs-lookup"><span data-stu-id="00dd9-151">Wsutil.exe generates a structure prototype as:</span></span>

``` syntax
struct StructType
{
  WS_STRING FirstName;
  WS_STRING LastName;
};

// methods using structure parameters.
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

<span data-ttu-id="00dd9-152">wsutil genera il seguente prototipo per LocalDefinition:</span><span class="sxs-lookup"><span data-stu-id="00dd9-152">wsutil generates the following prototype for LocalDefinition:</span></span>

``` syntax
struct // StructType
{
  struct // StructType
  {
    WS_FIELD_DESCRIPTION FirstName;
    WS_FIELD_DESCRIPTION LastName;
    WS_FIELD_DESCRIPTION * StructTypeFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } StructTypedescs; // StructType
WS_ELEMENT_DESCRIPTION elementDesc;
}
```

<span data-ttu-id="00dd9-153">La definizione della struttura è simile alla seguente, con due descrizioni dei campi nella struttura.</span><span class="sxs-lookup"><span data-stu-id="00dd9-153">The definition for the structure looks like below, with two field descriptions in the structure.</span></span>

``` syntax
// global element inside LocalDefinitions.
{ // StructType
  {   // StructType
    { // field description for FirstName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, FirstName),
      0,
      0,
    },    // end of field description for FirstName
    { // field description for LastName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.LastNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, LastName),
      0,
      0,
    },    // end of field description for LastName
    {    // fields description for StructType
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.FirstName,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.LastName,
    },
    { // WS_STRUCT_DESCRIPTION for StructType
      sizeof(StructType),
      __alignof(StructType),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    },   // struct description for StructType
  },    // StructType
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.structDesc,
  },
}, // StructType
```

<span data-ttu-id="00dd9-154">Per supportare l'estendibilità, le strutture incorporate vengono sempre definite passate per riferimento.</span><span class="sxs-lookup"><span data-stu-id="00dd9-154">To support extensibility, embedded structures are always defined passed by reference.</span></span> <span data-ttu-id="00dd9-155">In Service, all out o in, le strutture out vengono passate da un puntatore doppio per consentire l'estensione futura della struttura, oltre a consentire la struttura nillable.</span><span class="sxs-lookup"><span data-stu-id="00dd9-155">In service, all out or in,out structures are passed by double pointer to allow future extension of the structure, as well as allowing nillable structure.</span></span>

## <a name="recursive-structures"></a><span data-ttu-id="00dd9-156">Strutture ricorsive</span><span class="sxs-lookup"><span data-stu-id="00dd9-156">Recursive Structures</span></span>

<span data-ttu-id="00dd9-157">Sono supportate le strutture ricorsive e i tipi incorporati vengono passati per riferimento.</span><span class="sxs-lookup"><span data-stu-id="00dd9-157">Recursive structures are supported, and the embedded types is passed by reference.</span></span> <span data-ttu-id="00dd9-158">Per il WSDL seguente:</span><span class="sxs-lookup"><span data-stu-id="00dd9-158">For the following wsdl:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleMethod">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="tns:example" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:complexType name="example">
  <xs:sequence>
   <xs:element minOccurs="0" name="d" type="tns:example" />
   <xs:element minOccurs="0" name="c" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
</xs:schema>
```

<span data-ttu-id="00dd9-159">Wsutil genera le definizioni dei tipi seguenti, nonché le descrizioni dei tipi:</span><span class="sxs-lookup"><span data-stu-id="00dd9-159">Wsutil generates the follow type definitions, as well as the type descriptions:</span></span>

``` syntax
typedef struct example
{
  struct example  * d;
  int32   c;
} example;

typedef struct SimpleMethod
{
  unsigned __int32   a;
  struct example  * b;
} SimpleMethod;

// global element part of the LocalDefinitions.
...
struct // SimpleMethod
{
  struct // SimpleMethod
  {
    WS_FIELD_DESCRIPTION a;
    struct // example
    {
      WS_FIELD_DESCRIPTION d;
      WS_FIELD_DESCRIPTION c;
      WS_FIELD_DESCRIPTION * exampleFields [2];
      WS_STRUCT_DESCRIPTION structDesc;
    } exampledescs; // example
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

<span data-ttu-id="00dd9-160">La definizione viene generata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="00dd9-160">The definition is generated as below:</span></span>

``` syntax
{   // SimpleMethod
  { // field description for a
    WS_ELEMENT_FIELD_MAPPING,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_INT32_TYPE,
    0,
    WsOffsetOf(SimpleMethod, a),
    0,
    0,
  },    // end of field description for a
  {   // example
    { // field description for d
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.dLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_STRUCT_TYPE,
      (WS_STRUCT_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.structDesc,
      WsOffsetOf(example, d),
      WS_FIELD_POINTER,
      0,
    },    // end of field description for d
    { // field description for c
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.cLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(example, c),
      0,
      0,
    },    // end of field description for c
    {    // fields description for example
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.d,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.c,
    },
  {
    sizeof(example),
    __alignof(example),
    (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields,
    WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields),
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.exampleTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  },   // struct description for example
}
```

## <a name="structure-inheritence"></a><span data-ttu-id="00dd9-161">Struttura eredità</span><span class="sxs-lookup"><span data-stu-id="00dd9-161">Structure inheritence</span></span>

<span data-ttu-id="00dd9-162">wsutil supporta un'estensione di tipo complesso in cui un tipo complesso è un'estensione di un altro tipo complesso.</span><span class="sxs-lookup"><span data-stu-id="00dd9-162">wsutil supports complex type extension where one complex type is an extension to another complex type.</span></span>

``` syntax
<s:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:s="http://www.w3.org/2001/XMLSchema">
 <s:complexType name="LinkList">
  <s:sequence>
   <s:element minOccurs="0" name="d" type="tns:LinkList" />
   <s:element minOccurs="0" name="c" type="s:int" />
  </s:sequence>
 </s:complexType> 
 <s:element name="DerivedLinkList">
  <s:complexType>
   <s:complexContent>
    <s:extension base="tns:LinkList">
     <s:sequence>
      <s:element name="derive1" type="s:int" />
     </s:sequence>
    </s:extension>
   </s:complexContent>
  </s:complexType>
 </s:element>
</s:schema>
```

<span data-ttu-id="00dd9-163">Il frammento XSD sopra riportato indica che DerivedLinkList deriva da linker.</span><span class="sxs-lookup"><span data-stu-id="00dd9-163">The above xsd fragment indicates that DerivedLinkList derives from LinkList.</span></span>

<span data-ttu-id="00dd9-164">Wsutil.exe genera routine di supporto sia per C che per C++, in modo da consentire all'applicazione di impostare in modo più semplice le informazioni sul tipo del tipo di base e dei tipi derivati.</span><span class="sxs-lookup"><span data-stu-id="00dd9-164">Wsutil.exe generates helper routines for both C and C++ to make it easier for application to set up the type information of base type and derived types.</span></span> <span data-ttu-id="00dd9-165">Nel codice seguente \_ \_ viene usata la macro WS CPLUSPLUS per distinguere la definizione per il linguaggio C e C++:</span><span class="sxs-lookup"><span data-stu-id="00dd9-165">In the following code, \_WS\_CPLUSPLUS macro is used to differentiate definition for C and C++ language:</span></span>

``` syntax
#if defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  LinkList();
  LinkList(WS_STRUCT_DESCRIPTION*);
  struct _DerivedLinkList* WINAPI As_DerivedLinkList();
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;

void WINAPI LinkList_Init(LinkList*);
#endif

#if defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList:LinkList
{
  _DerivedLinkList();
  int  derive1;
} _DerivedLinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList
{
  struct LinkList _base;
  int  derive1;
} _DerivedLinkList;

struct _DerivedLinkList* WINAPI LinkList_As_DerivedLinkList(LinkList*);
#endif
```

<span data-ttu-id="00dd9-166">Nell'helper di stile C, prima di serialiation, l'applicazione chiama WSUTIL generate routine linking \_ init per inizializzare la struttura e impostare la descrizione del tipo sulla descrizione del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="00dd9-166">In C style helper, before serialiation, application calls wsutil generated routine LinkList\_Init to initialize the structure and set the type description to LinkList type description.</span></span> <span data-ttu-id="00dd9-167">Dopo la deserializzazione, l'applicazione può chiamare Linked \_ come \_ DerivedLinkList per ottenere il tipo derivato.</span><span class="sxs-lookup"><span data-stu-id="00dd9-167">After deserialization, application can call LinkList\_As\_DerivedLinkList to get the derived type.</span></span>

<span data-ttu-id="00dd9-168">Per recuperare le informazioni sul tipo in fase di esecuzione, WSUTIL genera il primo campo del tipo di base con il mapping del campo del tipo di [**\_ \_ Descrizione di WS struct**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) \* e il mapping dei campi dell' [**\_ \_ attributo \_ \_ WS Type**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) per descrivere le informazioni xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="00dd9-168">To retrieve type information in runtime, wsutil generates the first field of base type with [**WS\_STRUCT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)\* type and [**WS\_TYPE\_ATTRIBUTE\_FIELD\_MAPPING**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) field mapping to describe the xsi:type information.</span></span> <span data-ttu-id="00dd9-169">L'applicazione può impostare o controllare direttamente il campo per determinare il tipo effettivo di strutture.</span><span class="sxs-lookup"><span data-stu-id="00dd9-169">Application can directly set or check the field to determine the actual type of structures.</span></span> <span data-ttu-id="00dd9-170">Il codice seguente, ad esempio, imposta il tipo della struttura come DrivedLinkList:</span><span class="sxs-lookup"><span data-stu-id="00dd9-170">For example, the following code set the type of the structure to be DrivedLinkList:</span></span>

``` syntax
_DerivedLinkList derivedLinkList;
derivedLinkList._base._type = (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription;
WsWriteType(
    writer,
    WS_ELEMENT_TYPE_MAPPING,
    WS_STRUCT_TYPE,
    (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription,
    ...);
```

<span data-ttu-id="00dd9-171">Dopo la deserializzazione della struttura, l'applicazione può confrontare direttamente la descrizione del tipo per determinare il tipo deserializzato:</span><span class="sxs-lookup"><span data-stu-id="00dd9-171">After the structure is deserialized, application can directly compares the type description to determine the deserialized type:</span></span>

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

<span data-ttu-id="00dd9-172">wsutil genera la classe sia per la struttura di base che per la struttura derivata.</span><span class="sxs-lookup"><span data-stu-id="00dd9-172">wsutil generate class for both base structure and derived structure.</span></span> <span data-ttu-id="00dd9-173">Il costruttore predefinito inizializza il tipo e la descrizione del tipo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="00dd9-173">The default constructor initialize the type and matching type description.</span></span> <span data-ttu-id="00dd9-174">La routine AsDerivedType consente di eseguire il cast di tipo sicuro tra i tipi.</span><span class="sxs-lookup"><span data-stu-id="00dd9-174">The AsDerivedType routine helps to do safe type casting between types.</span></span>

``` syntax
  { // field description for typeOfLinkList
  WS_TYPE_ATTRIBUTE_FIELD_MAPPING,
  0,
  0,
  WS_DESCRIPTION_TYPE,
  0,
  WsOffsetOf(LinkList, typeOfLinkList),
  0,
  0,
  },    // end of field description for typeOfLinkList        ...
  {
  sizeof(LinkList),
  __alignof(LinkList),
  (WS_FIELD_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields,
WsCountOf(test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields),
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeName,
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeNamespace,
0,
(WS_STRUCT_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.SubTypes,
  1,
  },   // struct description for LinkList
```

## <a name="nillable"></a><span data-ttu-id="00dd9-175">nillable</span><span class="sxs-lookup"><span data-stu-id="00dd9-175">nillable</span></span>

<span data-ttu-id="00dd9-176">l'attributo nillable è supportato per stringhe, struct e matrici di byte.</span><span class="sxs-lookup"><span data-stu-id="00dd9-176">nillable attribute is supported for strings, structs, and byte arrays.</span></span> <span data-ttu-id="00dd9-177">L' \_ attributo WS Field \_ NILLABLE verrà aggiunto ai campi con l'attributo NILLABLE.</span><span class="sxs-lookup"><span data-stu-id="00dd9-177">WS\_FIELD\_NILLABLE attribute will be added to fields with nillable attribute.</span></span> <span data-ttu-id="00dd9-178">Se un elemento è nillable, il puntatore verrà impostato su **null** .</span><span class="sxs-lookup"><span data-stu-id="00dd9-178">The pointer will be set to **NULL** if an element is nillable.</span></span> <span data-ttu-id="00dd9-179">Un campo nillable in una struttura viene considerato come un puntatore.</span><span class="sxs-lookup"><span data-stu-id="00dd9-179">A nillable field in a structure is treated as a pointer.</span></span> <span data-ttu-id="00dd9-180">Una struttura di parametri con attributo nillable verrà passata per riferimento.</span><span class="sxs-lookup"><span data-stu-id="00dd9-180">A parameter structure with nillable attribute will be passed by reference.</span></span>

## <a name="pointers"></a><span data-ttu-id="00dd9-181">indicatori di misura</span><span class="sxs-lookup"><span data-stu-id="00dd9-181">pointers</span></span>

<span data-ttu-id="00dd9-182">Il tipo di valore deve essere passato per valore o per riferimento per i parametri out.</span><span class="sxs-lookup"><span data-stu-id="00dd9-182">Value type must be passed by value or by reference for out parameters.</span></span> <span data-ttu-id="00dd9-183">Il puntatore doppio non è consentito tranne che per le strutture out only.</span><span class="sxs-lookup"><span data-stu-id="00dd9-183">Double pointer is not allowed except for out only structures.</span></span>

## <a name="parameterless"></a><span data-ttu-id="00dd9-184">Senza parametri</span><span class="sxs-lookup"><span data-stu-id="00dd9-184">Parameterless</span></span>

<span data-ttu-id="00dd9-185">Ricordare la discussione precedente per il nome "Parameters" per la parte del messaggio.</span><span class="sxs-lookup"><span data-stu-id="00dd9-185">Recall our prior discussion for the "parameters" name for the message part.</span></span> <span data-ttu-id="00dd9-186">Se si specifica questo valore, si tenterà di generare un frame combinato per il messaggio di input e di output per l'operazione del servizio risultante.</span><span class="sxs-lookup"><span data-stu-id="00dd9-186">If this is specified we will attempt to generate a combined frame for input and output message for the resulting service operation.</span></span> <span data-ttu-id="00dd9-187">Se non viene specificata, l'operazione del servizio risultante conterrà i messaggi di input e output come struct come parametri.</span><span class="sxs-lookup"><span data-stu-id="00dd9-187">If this is not specified the resulting service operation would then contain input and output messages as structs as parameters.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Sapphire.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Sapphire.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="00dd9-188">Quindi, per l'operazione SimpleMethod la firma per il servizio e il client sarà simile a.</span><span class="sxs-lookup"><span data-stu-id="00dd9-188">Thus for our SimpleMethod operation the signature for the service and the client will look like.</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback)
  (const WS_OPERATION_CONTEXT* context,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="security"></a><span data-ttu-id="00dd9-189">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="00dd9-189">Security</span></span>

<span data-ttu-id="00dd9-190">Vedere la sezione sicurezza nello [strumento del compilatore WSUTIL](wsutil-compiler-tool.md) e la [serializzazione](serialization.md)</span><span class="sxs-lookup"><span data-stu-id="00dd9-190">See security section in [Wsutil Compiler tool](wsutil-compiler-tool.md) as well as [Serialization](serialization.md)</span></span>

 

 




