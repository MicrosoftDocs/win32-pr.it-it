---
title: Elemento sidType (ChannelPublishingType)
description: Determina se includere un ID di sicurezza (SID) dell'entità con ogni evento scritto nel canale.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- EventLog elemento sidType
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301842"
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

L'elemento **SIDType** è definito dal tipo complesso [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**pubblicazione (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





