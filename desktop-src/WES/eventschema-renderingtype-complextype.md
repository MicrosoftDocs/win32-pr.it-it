---
title: Tipo complesso RenderingInfoType
description: Definisce i messaggi di cui è stato eseguito il rendering per l'evento.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Log eventi di tipo complesso RenderingInfoType
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478791"
---
# <a name="renderinginfotype-complex-type"></a>Tipo complesso RenderingInfoType

Definisce i messaggi di cui è stato eseguito il rendering per l'evento.

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
| [**Channel**](eventschema-task-renderingtype-element.md)           | string | Stringa del messaggio di cui è stato eseguito il rendering del canale specificato nell'evento.<br/> |
| [**Parola chiave**](eventschema-keyword-keywords-element.md)             | string | Stringa del messaggio di cui è stato eseguito il rendering di una parola chiave specificata nell'evento.<br/>   |
| [**Parole chiave**](eventschema-keywords-renderingtype-element.md)      |        | Elenco di parole chiave sottoposte a rendering.<br/>                                       |
| [**Livello**](eventschema-level-renderingtype-element.md)            | string | Stringa del messaggio di cui è stato eseguito il rendering del livello specificato nell'evento.<br/>   |
| [**Messaggio**](eventschema-message-renderingtype-element.md)        | string | Stringa del messaggio di cui è stato eseguito il rendering dell'evento.<br/>                          |
| [**Opcode**](eventschema-opcode-renderingtype-element.md)          | string | Stringa del messaggio di cui è stato eseguito il rendering del codice operativo specificato nell'evento.<br/>  |
| [**Provider**](eventschema-publisher-renderinginfotype-element.md) | string | Stringa di messaggio di cui è stato eseguito il rendering per il provider.<br/>                      |
| [**Attività**](eventschema-task-renderingtype-element.md)              | string | Stringa del messaggio di cui è stato eseguito il rendering dell'attività specificata nell'evento.<br/>    |



## <a name="attributes"></a>Attributi



| Nome    | Tipo     | Descrizione                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| culture | Linguaggio | Nome della lingua (ad esempio, en-US) che identifica le impostazioni locali utilizzate per il rendering delle stringhe di messaggio.<br/> |



## <a name="remarks"></a>Commenti

Questa sezione contiene solo gli eventi che sono stati raccolti tramite il servizio [raccolta eventi di Windows](/windows/desktop/WEC/windows-event-collector) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

