---
title: Tipo complesso PeapExtensionsType
description: Contiene miglioramenti allo schema apportati in Windows 7. I miglioramenti futuri dello schema verranno gestiti da PeapExtensionsTypeV2.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- PeapExtensionsType di tipo complesso EAPHost
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
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742842"
---
# <a name="peapextensionstype-complex-type"></a>Tipo complesso PeapExtensionsType

Il tipo complesso **PeapExtensionsType** contiene miglioramenti dello schema apportati in Windows 7. I miglioramenti futuri dello schema verranno gestiti da [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).

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
| [**extendedPeap:AcceptServerName**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | Windows 7 e versioni successive: indica se viene letto il nome di un server.<br/>                            |
| [**extendedPeap:IdentityPrivacy**](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | Windows 7 e versioni successive: indica se viene inviata un'identità vera o anonima dell'utente.<br/> |
| [**extendedPeap:PeapExtensionsV2**](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | Windows 7 e versioni successive: consente miglioramenti futuri allo schema.<br/>                                 |



## <a name="remarks"></a>Commenti

L'elemento **PeapExtensionsType** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipi complessi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





