---
title: Tipo semplice emptyString
description: Informazioni sul tipo semplice emptyString, che non è in uso. Vedere i requisiti e visualizzare altre risorse disponibili.
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- EAPHost di tipo semplice emptyString
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
ms.openlocfilehash: 4f210fadeb0097ffd7a11d80dd47b252dbbfdc614950af0ac07d612b44edd0aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948211"
---
# <a name="emptystring-simple-type"></a>Tipo semplice emptyString

Il **tipo semplice emptyString** non è in uso.

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



| Ruolo | Versione minima supportata del sistema operativo |
|-------------------------------------|------------------------------------------------------|
| Client<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipi semplici dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 





