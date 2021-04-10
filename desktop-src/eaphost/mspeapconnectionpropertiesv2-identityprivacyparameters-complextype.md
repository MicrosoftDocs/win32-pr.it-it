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
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104117253"
---
# <a name="identityprivacyparameters-complex-type"></a>Tipo complesso IdentityPrivacyParameters

Il tipo complesso **IdentityPrivacyParameters** contiene informazioni sull'utilizzo di identità anonime durante l'autenticazione PEAP.


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
| [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | boolean | Indica se viene inviata un'identità vera o anonima dell'utente.                                                                                                                                                                                                                                                                           |
| [**AnonymousUserName**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | string  | contiene un'identità anonima utilizzata al posto dell'identificazione true di un utente. Viene inviato durante la prima fase dell'autenticazione PEAP quando l' **identità** viene inviata come testo normale. L'utilizzo dell'identità anonima è determinato dall'elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) . |



 

## <a name="remarks"></a>Commenti

L'elemento IdentityPrivacyParameters è facoltativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Tipi complessi mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




