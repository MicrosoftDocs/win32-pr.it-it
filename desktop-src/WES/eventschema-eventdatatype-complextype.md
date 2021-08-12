---
title: Tipo complesso EventDataType
description: Definisce gli elementi e le strutture dei dati dell'evento che contengono i dati dell'evento.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- EventDataType tipo complesso EventLog
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 424f7f5f6472859a06605467c427fc7b9f210a960f0920fb8593778bd757fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589024"
---
# <a name="eventdatatype-complex-type"></a>Tipo complesso EventDataType

Definisce gli elementi e le strutture dei dati dell'evento che contengono i dati dell'evento.

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
| [**Binario**](eventschema-binary-eventdatatype-element.md)           | Hexbinary                                                          | BLOB di dati binari per gli eventi scritti tramite [Registrazione eventi](/windows/desktop/EventLog/event-logging).<br/> |
| [**ComplexData**](eventschema-complexdata-eventdatatype-element.md) | [**ComplexDataType**](eventschema-complexdatatype-complextype.md) | Struttura definita nel modello per l'evento.<br/>                                |
| [**Dati**](eventschema-data-eventdatatype-element.md)               | [**Datatype**](eventschema-datafieldtype-complextype.md)          | Elemento di dati di primo livello definito nel modello per l'evento.<br/>                      |



## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                       |
|------|--------|-------------------------------------------------------------------|
| Nome | stringa | Nome del modello che contiene gli elementi di dati.<br/> |



## <a name="remarks"></a>Commenti

La [**funzione EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) esegue il rendering di matrici e strutture come BLOB binari.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

