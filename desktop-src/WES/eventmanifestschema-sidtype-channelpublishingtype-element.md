---
title: Elemento sidType (ChannelPublishingType)
description: Determina se includere un ID di sicurezza (SID) dell'entità con ogni evento scritto nel canale.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- Elemento sidType EventLog
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41653a1fbda3400b74ca5302deb8075ae891e69f22ca0f0e88b6ec4dbb58dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589152"
---
# <a name="sidtype-channelpublishingtype-element"></a>Elemento sidType (ChannelPublishingType)

Determina se includere un ID di sicurezza (SID) dell'entità con ogni evento scritto nel canale.

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**L'elemento sidType** è definito dal tipo complesso [**ChannelPublishingType.**](eventmanifestschema-channelpublishingtype-complextype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**publishing (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





