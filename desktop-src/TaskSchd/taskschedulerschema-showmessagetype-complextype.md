---
title: Tipo complesso showMessageType
description: Definisce gli elementi che rappresentano un'azione che visualizza una finestra di messaggio.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- Utilità di pianificazione di tipo complesso showMessageType
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964512"
---
# <a name="showmessagetype-complex-type"></a>Tipo complesso showMessageType

Definisce gli elementi che rappresentano un'azione che visualizza una finestra di messaggio.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





