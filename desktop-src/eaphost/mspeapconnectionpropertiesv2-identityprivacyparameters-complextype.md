---
title: Tipo complesso IdentityPrivacyParameters
description: Contiene informazioni sull'utilizzo di identità anonime durante l'autenticazione PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 18bef3eb69ab2799f7139fe2886d89e996fb8fb47d178997694c568450fb8340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983901"
---
# <a name="identityprivacyparameters-complex-type"></a>Tipo complesso IdentityPrivacyParameters

Il **tipo complesso IdentityPrivacyParameters** contiene informazioni sull'utilizzo di identità anonime durante l'autenticazione PEAP.


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| Elemento                                                                                                               | Tipo    | Descrizione                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | boolean | Indica se viene inviata la vera identità di un utente o un'identità anonima.                                                                                                                                                                                                                                                                           |
| [**AnonymousUserName**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | string  | contiene un'identità anonima usata al posto dell'identificazione vera di un utente. Viene inviato durante la prima fase dell'autenticazione PEAP quando **l'identità** viene inviata come testo normale. L'utilizzo di identità anonime è determinato [**dall'elemento EnableIdentityPrivacy.**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) |



 

## <a name="remarks"></a>Commenti

L'elemento IdentityPrivacyParameters è facoltativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Mspeapconnectionpropertiesv2 Tipi complessi](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




