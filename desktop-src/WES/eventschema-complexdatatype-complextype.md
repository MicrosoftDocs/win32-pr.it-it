---
title: Tipo complesso ComplexDataType
description: Definisce una struttura che contiene uno o più elementi di dati.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- EventLog di tipo complesso ComplexDataType
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f86b15defc32469dd1a4abd0f6366e1a93d4b83441b1e1518ff7ac999f30bd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055809"
---
# <a name="complexdatatype-complex-type"></a>Tipo complesso ComplexDataType

Definisce una struttura che contiene uno o più elementi di dati.

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                  | Tipo                                                      | Descrizione                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Dati**](eventschema-data-complexdatatype-element.md) | [**Datatype**](eventschema-datafieldtype-complextype.md) | Elenco di elementi di dati nella struttura . L'elenco di elementi è nello stesso ordine definito nel modello.<br/> |



## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome | stringa | Nome della struttura. Si tratta del nome specificato quando è stata definita la struttura nel modello (vedere il tipo complesso [**TemplateItemType).**](eventmanifestschema-templateitemtype-complextype.md)<br/> |



## <a name="remarks"></a>Commenti

La [**funzione EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) esegue il rendering del contenuto di una struttura come BLOB binario. la funzione non esegue il rendering dei singoli elementi di dati della struttura .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





