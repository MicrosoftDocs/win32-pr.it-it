---
title: Tipo semplice emptyString
description: Informazioni sul tipo semplice emptyString, che non è in uso. Vedere requisiti e visualizzare altre risorse disponibili.
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- emptyString di tipo semplice EAPHost
topic_type:
- apiref
api_name:
- emptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 756c8976c8b989cf77be921491770fcff9ea62d5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047383"
---
# <a name="emptystring-simple-type"></a>Tipo semplice emptyString

Il tipo semplice **EmptyString** non è in uso.

``` syntax
<xs:simpleType name="emptyString">
    <xs:restriction
        base="string"
    >
        <xs:maxLength
            value="0"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|-------------------------------------|------------------------------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipi semplici dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 





