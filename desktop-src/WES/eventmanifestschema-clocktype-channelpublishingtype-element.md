---
title: Elemento clockType (ChannelPublishingType)
description: Risoluzione dell'orologio da utilizzare per la registrazione del timestamp per ogni evento.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- Elemento clockType EventLog
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fde3b263c2a190e91fdd2ddde8f05a40e9026486195ca9ae95b5f98cdcf7733d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590032"
---
# <a name="clocktype-channelpublishingtype-element"></a>Elemento clockType (ChannelPublishingType)

Risoluzione dell'orologio da utilizzare per la registrazione del timestamp per ogni evento.

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**L'elemento clockType** è definito dal tipo complesso [**ChannelPublishingType.**](eventmanifestschema-channelpublishingtype-complextype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**pubblicazione (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





