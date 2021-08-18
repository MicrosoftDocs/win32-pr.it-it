---
title: Tipo complesso PeapExtensionsType (proprietà di connessione)
description: Informazioni sul tipo complesso PeapExtensionsType. Questo tipo consente miglioramenti futuri dello schema.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- Tipo complesso PeapExtensionsType EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a72fa87b3f1cf5ba4a65c179895c22e5a208616ed8c9b2ffb9f046e5de9b92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983921"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a>Tipo complesso PeapExtensionsType (proprietà di connessione)

Il **tipo complesso PeapExtensionsType** consente miglioramenti futuri dello schema.

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Commenti

Il **tipo complesso PeapExtensionsType** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





