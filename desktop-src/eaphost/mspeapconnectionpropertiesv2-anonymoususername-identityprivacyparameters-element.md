---
title: Elemento AnonymousUserName (IdentityPrivacyParameters)
description: Contiene un'identità anonima utilizzata al posto dell'identificazione true di un utente. Viene inviato durante la prima fase dell'autenticazione PEAP quando l'identità viene inviata come testo normale.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Elemento AnonymousUserName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400767"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a>Elemento AnonymousUserName (IdentityPrivacyParameters)

L'elemento **AnonymousUserName (IdentityPrivacyParameters)** contiene un'identità anonima usata al posto dell'identificazione true di un utente. Viene inviato durante la prima fase dell'autenticazione PEAP quando l' **identità** viene inviata come testo normale.

L'utilizzo dell'identità anonima è determinato dall'elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

L'elemento **AnonymousUserName** è definito da [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .

## <a name="remarks"></a>Commenti

L'elemento **AnonymousUserName** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





