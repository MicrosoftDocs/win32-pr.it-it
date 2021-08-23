---
title: Supporto degli schemi
description: WsUtil.exe supporta lo schema XSD specificato in XML Schema.
ms.assetid: 33096cda-9dbe-44d2-8d08-410bc33ae81c
keywords:
- Supporto dello schema dei servizi Web per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0f55c5ea3828c72456989f7053e2ff008e524e41552b281b88839653229863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962900"
---
# <a name="schema-support"></a>Supporto degli schemi

WsUtil.exe supporta lo schema XSD specificato in [XML Schema.](https://www.w3.org/XML/Schema) Il file xsd e wsdl:type devono essere trattati nella stessa categoria, con l'eccezione in wsdl:type quando un elemento globale può essere un elenco di parametri. Wsutil.exe genera descrizioni degli elementi per tutte le definizioni di elemento globali che possono essere utilizzate nel serializzatore, con output aggiuntivo per la struttura dei parametri specificata nel [supporto WSDL.](wsdl-support.md)

## <a name="xsd-schema-support-level"></a>Livello di supporto dello schema XSD

WsUtil.exe non supporta l'intero extent dello schema XSD. Il livello di supporto corrente è definito nel livello [di supporto dello schema](schema-support-level.md).

Generazione di identificatori

Il nome dell'elemento o il nome del tipo nello schema potrebbe non essere un identificatore C valido e i nomi vengono normalizzati in modo da generare nomi C validi. I caratteri identificatore C non validi vengono convertiti nel nome esadecimale e un carattere di sottolineatura ' ' potrebbe essere preceduto \_ dal nome, se necessario. I tipi anonimi sono denominati in base al nome dell'elemento contenitore, ma preceduti dal carattere di sottolineatura " \_ " per evitare conflitti di nome. I nomi dei tipi globali vengono mantenuti così come sono dopo la normalizzazione dei caratteri non validi. I tipi anonimi annidati sono preceduti dal nome del tipo padre.

Per ogni definizione di elemento globale, wsutil.exe genera una [**WS \_ ELEMENT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) nella struttura di descrizione globale. Per ogni definizione di tipo globale, wsutil.exe genera una descrizione del tipo nella struttura di descrizione globale a cui l'applicazione deve fare riferimento.

Per ogni campo della struttura, wsutil.exe genera una [**WS \_ FIELD \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) incorporata come parte della struttura dello chassis.

## <a name="simple-types"></a>Tipi semplici

I tipi valore, elencati in [**WS \_ VALUE \_ TYPE,**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)vengono considerati come tipi semplici. Si noti che WS \_ VALUE TYPE è in realtà un subset di \_ [**WS \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type). Include tipi di dati integrali e float di base, nonché DECIMAL, WS \_ DATETIME e UUID.

Nel modello di servizio, nei tipi semplici vengono passati per valore, mentre i tipi semplici out e in uscita vengono passati per riferimento.

Wsutil crea una descrizione di elemento semplice come quella riportata di seguito per l'elemento globale contenente tipi semplici.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

Wsutil genera la descrizione dell'elemento seguente:

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

Questa struttura viene generata come parte della struttura di descrizione globale generata nel file di intestazione:

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a>Matrici

L'elemento con maxOccurs maggiore di 1 o una sequenza con un solo elemento e l'elemento figlio con maxOccurs maggiore di 1 viene considerato come matrice. Per un elemento di matrice nello schema, wsutil.exe due campi: un campo di conteggio che non è in transito e un campo puntatore contenente il tipo di matrice.

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

Il file di intestazione contiene la definizione della struttura C per la matrice, con il campo aCount che specifica il conteggio della matrice.

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

Di seguito è riportato il prototipo LocalDefinition che descrive la matrice:

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

Di seguito sono riportate le definizioni generate delle descrizioni precedenti. Si noti il mapping WS REPEATING ELEMENT FIELD MAPPING che indica il campo \_ \_ come campo di \_ \_ matrice.

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

Se la matrice è un campo di parametro nel messaggio di input/output, per il metodo verranno generati due parametri effettivi. Se la matrice è un parametro out o in,out, esisterebbe un livello aggiuntivo di riferimento indiretto per entrambi i campi in paramStruct.

## <a name="range-on-array"></a>Intervallo nella matrice

È consigliabile non specificare maxOccur="unbounded" per le matrici. È invece necessario che sia specificato un numero intero fisso per impostare un limite superiore di conteggi di matrici consentiti. range è supportato per i tipi integrali, nonché per stringhe, matrici di byte e matrici generiche.

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a>Euristica per la matrice di cui è stato eseguito il wrapping anziché senza wrapping

In alcuni casi viene eseguito il wrapping delle matrici all'interno di un'altra struttura da incorporare in una struttura di primo livello. In tal caso, è necessario rimuovere il livello wrapper intermedio. WsUtil.exe genera lo stesso prototipo e le stesse descrizioni di SimpleArray descritte in precedenza.

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

Wsutil rileva che SimpleArrayWrapper è un wrapper per SimpleArray e genera solo le strutture seguenti, con struttura separata per SimpleArray

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

wsutil.exe genera le definizioni seguenti per il prototipo corrispondente precedente, si noti che nella descrizione del campo i campi del nome del wrapper e dello spazio dei nomi del wrapper vengono compilati

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

## <a name="structures"></a>Strutture

Un complexType con più elementi in una sequenza è una struttura . Ad esempio,

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

Wsutil.exe genera un prototipo di struttura come segue:

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

wsutil genera il prototipo seguente per LocalDefinition:

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

La definizione per la struttura è simile alla seguente, con due descrizioni di campo nella struttura.

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

Per supportare l'estendibilità, le strutture incorporate sono sempre definite passate per riferimento. Nel servizio tutte le strutture out o in,out vengono passate da un puntatore double per consentire l'estensione futura della struttura, oltre a consentire una struttura nillable.

## <a name="recursive-structures"></a>Strutture ricorsive

Le strutture ricorsive sono supportate e i tipi incorporati vengono passati per riferimento. Per il wsdl seguente:

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

Wsutil genera le definizioni di tipo seguenti, nonché le descrizioni dei tipi:

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

La definizione viene generata come indicato di seguito:

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

## <a name="structure-inheritence"></a>Ereditarietà della struttura

wsutil supporta l'estensione di tipo complesso in cui un tipo complesso è un'estensione di un altro tipo complesso.

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

Il frammento xsd precedente indica che DerivedLinkList deriva da LinkList.

Wsutil.exe genera routine helper per C e C++ per rendere più semplice per l'applicazione configurare le informazioni sul tipo di base e i tipi derivati. Nel codice seguente viene usata la macro WS CPLUSPLUS per distinguere la definizione per il \_ \_ linguaggio C e C++:

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

Nell'helper di stile C, prima della serializzazione, l'applicazione chiama la routine generata da wsutil LinkList Init per inizializzare la struttura e impostare la descrizione del tipo su \_ LinkList type description. Dopo la deserializzazione, l'applicazione può chiamare LinkList \_ as \_ DerivedLinkList per ottenere il tipo derivato.

Per recuperare informazioni sul tipo in fase di esecuzione, wsutil genera il primo campo del tipo di base con il tipo [**\_ WS STRUCT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) e il mapping dei campi WS TYPE ATTRIBUTE FIELD MAPPING per descrivere le informazioni \* xsi:type. [**\_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) L'applicazione può impostare o controllare direttamente il campo per determinare il tipo effettivo di strutture. Ad esempio, il codice seguente imposta il tipo della struttura su DrivedLinkList:

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

Dopo la deserializzazione della struttura, l'applicazione può confrontare direttamente la descrizione del tipo per determinare il tipo deserializzato:

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

wsutil genera la classe sia per la struttura di base che per la struttura derivata. Il costruttore predefinito inizializza il tipo e la descrizione del tipo corrispondente. La routine AsDerivedType consente di eseguire il cast di tipi sicuri tra tipi.

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

## <a name="nillable"></a>nillable

L'attributo nillable è supportato per stringhe, struct e matrici di byte. \_L'attributo WS FIELD \_ NILLABLE verrà aggiunto ai campi con attributo nillable. Il puntatore verrà impostato su **NULL se** un elemento è nillable. Un campo nillable in una struttura viene considerato come un puntatore. Una struttura di parametri con attributo nillable verrà passata per riferimento.

## <a name="pointers"></a>indicatori di misura

Il tipo di valore deve essere passato per valore o per riferimento per i parametri out. Il puntatore double non è consentito ad eccezione delle strutture out only.

## <a name="parameterless"></a>Senza parametri

Si ricordi la discussione precedente per il nome dei "parametri" per la parte del messaggio. Se viene specificato, si tenterà di generare un frame combinato per il messaggio di input e output per l'operazione del servizio risultante. Se non viene specificato, l'operazione del servizio risultante conterrà i messaggi di input e output come struct come parametri.

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

Pertanto, per l'operazione SimpleMethod la firma per il servizio e il client sarà simile.

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

## <a name="security"></a>Sicurezza

Vedere la sezione relativa alla sicurezza [nello strumento del compilatore Wsutil](wsutil-compiler-tool.md) e [serializzazione](serialization.md)

 

 




