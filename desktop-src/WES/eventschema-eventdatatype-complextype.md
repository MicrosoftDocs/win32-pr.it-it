---
title: Tipo complesso EventDataType
description: Definisce gli elementi e le strutture dei dati dell'evento che contiene i dati dell'evento.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- Log eventi di tipo complesso EventDataType
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740375"
---
# <a name="eventdatatype-complex-type"></a>Tipo complesso EventDataType

Definisce gli elementi e le strutture dei dati dell'evento che contiene i dati dell'evento.

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                              | Tipo                                                               | Descrizione                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Binary**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | BLOB di dati binari per gli eventi scritti mediante la [registrazione degli eventi](/windows/desktop/EventLog/event-logging).<br/> |
| [**ComplexData**](eventschema-complexdata-eventdatatype-element.md) | [**ComplexDataType**](eventschema-complexdatatype-complextype.md) | Struttura definita nel modello per l'evento.<br/>                                |
| [**Data**](eventschema-data-eventdatatype-element.md)               | [**Tipo**](eventschema-datafieldtype-complextype.md)          | Elemento di dati di primo livello definito nel modello per l'evento.<br/>                      |



## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                       |
|------|--------|-------------------------------------------------------------------|
| Nome | stringa | Nome del modello che contiene gli elementi di dati.<br/> |



## <a name="remarks"></a>Commenti

La funzione [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) esegue il rendering di matrici e strutture come BLOB binari.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

