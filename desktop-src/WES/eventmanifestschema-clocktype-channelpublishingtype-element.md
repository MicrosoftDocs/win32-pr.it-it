---
title: Elemento clockType (ChannelPublishingType)
description: Risoluzione del clock da usare quando si registra il timestamp per ogni evento.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- EventLog elemento clockType
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400309"
---
# <a name="clocktype-channelpublishingtype-element"></a>Elemento clockType (ChannelPublishingType)

Risoluzione del clock da usare quando si registra il timestamp per ogni evento.

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

L'elemento **clockType** è definito dal tipo complesso [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .

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

 

 





