---
title: Tipo complesso InstrumentationType
description: Definisce il contenuto della sezione di strumentazione del manifesto.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- EventLog di tipo complesso InstrumentationType
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21462782ad14dfd977c87ab0898b7b9d2211e730bae42ed6281207fc557a4101
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905001"
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
| [**Eventi**](eventmanifestschema-events-instrumentationtype-element.md) | [**EventsType**](eventmanifestschema-eventstype-complextype.md) | Contiene un elenco di provider definiti dal manifesto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





