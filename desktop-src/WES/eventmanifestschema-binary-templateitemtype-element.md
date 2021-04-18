---
title: Binary (TemplateItemType)-elemento
description: Contiene i dati binari forniti dall'API del registro eventi.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- EventLog elemento binario
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302336"
---
# <a name="binary-templateitemtype-element"></a>Binary (TemplateItemType)-elemento

Contiene i dati binari forniti dall'API del [registro eventi](/windows/desktop/EventLog/event-logging) .

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L'elemento **binario** è definito dal tipo complesso [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) .

## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                          |
|------|--------|------------------------------------------------------|
| name | string | Nome associato ai dati binari.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**modello (TemplateListType)**](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

