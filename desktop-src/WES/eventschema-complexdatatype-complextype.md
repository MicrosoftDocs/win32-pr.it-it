---
title: Tipo complesso ComplexDataType
description: Definisce una struttura che contiene uno o più elementi di dati.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- Log eventi di tipo complesso ComplexDataType
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302156"
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
| [**Data**](eventschema-data-complexdatatype-element.md) | [**Tipo**](eventschema-datafieldtype-complextype.md) | Elenco di elementi di dati nella struttura. L'elenco di elementi è nello stesso ordine definito nel modello.<br/> |



## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome | stringa | Nome della struttura. Si tratta del nome specificato quando è stata definita la struttura nel modello (vedere il tipo complesso [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |



## <a name="remarks"></a>Commenti

La funzione [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) esegue il rendering del contenuto di una struttura come BLOB binario; la funzione non esegue il rendering dei singoli elementi di dati della struttura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





