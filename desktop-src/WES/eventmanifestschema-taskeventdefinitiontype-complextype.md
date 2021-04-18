---
title: Tipo complesso TaskEventDefinitionType
description: Definisce un evento specifico dell'attività che il provider è in grado di registrare. | Tipo complesso TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- Log eventi di tipo complesso TaskEventDefinitionType
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321706"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Tipo complesso TaskEventDefinitionType

\[A partire dal compilatore di messaggi fornito con la versione di Windows 7 del Windows SDK, il tipo complesso TaskEventDefinitionType non è più disponibile. Usare invece i codici operativi specifici delle attività per fornire la stessa funzionalità.\]

Definisce un evento specifico dell'attività che il provider è in grado di registrare.

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="event"
                        type="EventDefinitionType"
                        maxOccurs="unbounded"
                     />
                </xs:sequence>
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
            </xs:complexType>
        </xs:element>
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



| Elemento                                                                      | Tipo                                                                               | Descrizione                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| **event**                                                                    | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Evento specifico dell'attività pubblicato con un'attività.<br/> |
| [**codice operativo**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | Codice operativo specifico dell'attività per un evento. <br/>   |



## <a name="attributes"></a>Attributi



| Nome | Tipo      | Descrizione                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nome del codice operativo specifico dell'attività.<br/> |
| name | anyURI    | Nome dell'attività.<br/>                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





