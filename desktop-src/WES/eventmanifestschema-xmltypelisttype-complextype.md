---
title: Tipo complesso XmlTypeListType
description: Definisce un elenco di tipi di output utilizzati dal servizio per determinare come eseguire il rendering di un tipo di dati di input.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Log eventi di tipo complesso XmlTypeListType
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340793"
---
# <a name="xmltypelisttype-complex-type"></a>Tipo complesso XmlTypeListType

Definisce un elenco di tipi di output utilizzati dal servizio per determinare come eseguire il rendering di un tipo di dati di input.

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension
                        base="XmlType"
                    >
                        <xs:attribute name="name"
                            type="QName"
                            use="required"
                         />
                        <xs:attribute name="value"
                            type="string"
                            use="required"
                         />
                        <xs:attribute name="symbol"
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                | Tipo | Descrizione                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [**xmlType**](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | Definisce un tipo XML. <br/> |



## <a name="attributes"></a>Attributi



| Nome   | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName**                                                         | Nome del tipo di output.<br/>                                                                                                                                                                                                                    |
| simbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento al tipo di output nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il tipo di output nel file di intestazione generato dal compilatore.<br/> |
| Valore  | string                                                            | Valore intero che identifica in modo univoco il tipo di output nell'elenco dei tipi di output definiti.<br/>                                                                                                                                          |



## <a name="remarks"></a>Commenti

Il \\ \\ file di inclusioneWinmeta.xml, incluso nella Windows SDK, contiene un elenco di tipi di output predefiniti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





