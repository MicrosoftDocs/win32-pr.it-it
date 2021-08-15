---
title: Tipo complesso RenderingInfoType
description: Definisce i messaggi sottoposti a rendering per l'evento.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- EventLog di tipo complesso RenderingInfoType
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d4a70c8bc97abc3dea7cd04e9ce491b64cb62dcc892fcde318d69dcdc996e2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588464"
---
# <a name="renderinginfotype-complex-type"></a>Tipo complesso RenderingInfoType

Definisce i messaggi sottoposti a rendering per l'evento.

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                             | Tipo   | Descrizione                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [**Channel**](eventschema-task-renderingtype-element.md)           | string | Stringa di messaggio sottoposta a rendering del canale specificato nell'evento.<br/> |
| [**Parola chiave**](eventschema-keyword-keywords-element.md)             | string | Stringa di messaggio sottoposta a rendering di una parola chiave specificata nell'evento.<br/>   |
| [**Parole chiavi**](eventschema-keywords-renderingtype-element.md)      |        | Elenco di parole chiave sottoposte a rendering.<br/>                                       |
| [**Livello**](eventschema-level-renderingtype-element.md)            | string | Stringa di messaggio sottoposta a rendering del livello specificato nell'evento.<br/>   |
| [**Messaggio**](eventschema-message-renderingtype-element.md)        | string | Stringa di messaggio sottoposta a rendering dell'evento.<br/>                          |
| [**Opcode**](eventschema-opcode-renderingtype-element.md)          | string | Stringa di messaggio sottoposta a rendering del codice operativo specificato nell'evento .<br/>  |
| [**Provider**](eventschema-publisher-renderinginfotype-element.md) | string | Stringa di messaggio sottoposta a rendering per il provider.<br/>                      |
| [**Attività**](eventschema-task-renderingtype-element.md)              | string | Stringa di messaggio sottoposta a rendering dell'attività specificata nell'evento .<br/>    |



## <a name="attributes"></a>Attributi



| Nome    | Tipo     | Descrizione                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| culture | Linguaggio | Nome della lingua, ad esempio en-US, che identifica le impostazioni locali usate per il rendering delle stringhe di messaggio.<br/> |



## <a name="remarks"></a>Commenti

Questa sezione contiene solo gli eventi raccolti [usando Windows agente](/windows/desktop/WEC/windows-event-collector) di raccolta eventi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

