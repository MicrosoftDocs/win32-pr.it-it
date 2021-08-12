---
title: Tipo complesso showMessageType
description: Definisce gli elementi che rappresentano un'azione che mostra una finestra di messaggio.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- Tipo complesso showMessageType Utilità di pianificazione
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aeb2c0e1b3ac3e29502e7d998305674aaa283371be6a22324dde6d84c4330326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611243"
---
# <a name="showmessagetype-complex-type"></a>Tipo complesso showMessageType

Definisce gli elementi che rappresentano un'azione che mostra una finestra di messaggio.

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                            | Tipo           | Descrizione                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Corpo**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Specifica il testo da visualizzare nel corpo della finestra di messaggio. <br/> |
| [**Titolo**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Specifica il titolo della finestra di messaggio. <br/>                       |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





