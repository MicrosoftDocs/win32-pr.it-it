---
title: Tipo complesso InstrumentationType
description: Definisce il contenuto della sezione di strumentazione del manifesto.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Log eventi di tipo complesso InstrumentationType
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302546"
---
# <a name="instrumentationtype-complex-type"></a>Tipo complesso InstrumentationType

Definisce il contenuto della sezione di strumentazione del manifesto.

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                  | Tipo                                                             | Descrizione                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**eventi**](eventmanifestschema-events-instrumentationtype-element.md) | [**EventsType**](eventmanifestschema-eventstype-complextype.md) | Contiene un elenco di provider definiti dal manifesto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





