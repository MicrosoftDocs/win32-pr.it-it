---
title: Tipo complesso PeapExtensionsType
description: Contiene miglioramenti dello schema apportati in Windows 7. I miglioramenti futuri dello schema verranno gestiti da PeapExtensionsTypeV2.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
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
ms.openlocfilehash: 212c8bf6b1421cfc461288e8f57258b40e11e9118c9ea2b2f620986e91d226f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984031"
---
# <a name="peapextensionstype-complex-type"></a>Tipo complesso PeapExtensionsType

Il **tipo complesso PeapExtensionsType** contiene miglioramenti dello schema apportati in Windows 7. I miglioramenti futuri dello schema verranno gestiti da [**PeapExtensionsTypeV2.**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md)

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                                               | Tipo | Descrizione                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [**extendedPeap:PerformServerValidation**](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | Windows 7 e versioni successive: indica se viene eseguita la convalida del server.<br/>                          |
| [**extendedPeap:AcceptServerName**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | Windows 7 e versioni successive: indica se il nome di un server è letto.<br/>                            |
| [**extendedPeap:IdentityPrivacy**](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | Windows 7 e versioni successive: indica se viene inviata l'identità vera o anonima di un utente.<br/> |
| [**extendedPeap:PeapExtensionsV2**](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | Windows 7 e versioni successive: abilita i miglioramenti futuri dello schema.<br/>                                 |



## <a name="remarks"></a>Commenti

**L'elemento PeapExtensionsType** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Mspeapconnectionpropertiesv1 Tipi complessi dello schema](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





