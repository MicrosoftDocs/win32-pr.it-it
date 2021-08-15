---
title: Tipo complesso MetadataType
description: Definisce i tipi di metadati che è possibile definire nella sezione dei metadati del manifesto.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- EventLog di tipo complesso MetadataType
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 392e0bb2940c36b541f63f55dac418312489f231d785f82014ade82c20602fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343603"
---
# <a name="metadatatype-complex-type"></a>Tipo complesso MetadataType

Definisce i tipi di metadati che è possibile definire nella sezione dei metadati del manifesto.

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                       | Tipo                                                                       | Descrizione                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Canali**](eventmanifestschema-channels-metadatatype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md) | Definisce un elenco di canali in cui i provider possono registrare gli eventi. Un provider può quindi importare uno o più canali nel manifesto.<br/>               |
| [**keywords**](eventmanifestschema-keywords-metadatatype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) | Definisce un elenco di parole chiave che determinano la categoria di eventi scritti dal provider.<br/>                                                            |
| [**Livelli**](eventmanifestschema-levels-metadatatype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)     | Definisce un elenco di livelli che specificano la gravità di un evento.<br/>                                                                                       |
| **message**                                                                   |                                                                            | Definisce una stringa di messaggio.<br/>                                                                                                                             |
| **messageTable**                                                              |                                                                            | Definisce un elenco di stringhe di messaggio.<br/>                                                                                                                    |
| [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)   | Definisce un elenco di query denominate che usano espressioni regolari per eseguire azioni di ricerca e sostituzione sulla stringa di messaggio di un evento.<br/>                        |
| [**Opcodes**](eventmanifestschema-opcodes-metadatatype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)   | Definisce un elenco di codici operativo che è possibile usare per raggruppare gli eventi all'interno di un'attività.<br/>                                                                             |
| **Attività**                                                                     | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)       | Definisce un elenco di attività che un provider può usare per raggruppare gli eventi. In genere, si usano le attività per raggruppare gli eventi per una funzionalità o un componente del provider.<br/> |
| [**Tipi**](eventmanifestschema-types-metadatatype-element.md)               | [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)       | Definisce un elenco di tipi XML.<br/>                                                                                                                          |



## <a name="attributes"></a>Attributi



| Nome    | Tipo                                                              | Descrizione                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Riferimento alla stringa localizzata nella tabella delle stringhe.<br/>                                |
| mid     | xs:string                                                         | Non usato.<br/>                                                                               |
| name    | anyURI                                                            | URI del metafile. <br/>                                                              |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Nome simbolico che si desidera che il compilatore di messaggi crei per questa stringa di messaggio.<br/> |
| Valore   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Numero da utilizzare come identificatore del messaggio.<br/>                           |



## <a name="remarks"></a>Commenti

Anche se è possibile creare un manifesto che contiene una sezione di metadati, il servizio non lo userà. gli unici metadati che il servizio riconosce sono i metadati trovati nel file Winmeta.xml file.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





