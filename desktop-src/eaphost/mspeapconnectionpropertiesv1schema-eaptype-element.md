---
title: Elemento EapType (mspeapconnectionpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dallo schema BaseEapConnectionProperties. Per lo schema mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 47f3585f35b2e7ee7722cdd99c90605cdb7864b2211fcf28f7ec0ac662b5289b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719772"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a>Elemento EapType (mspeapconnectionpropertiesv1schema)

**L'elemento EapType** è un tipo derivato dell'elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) dallo schema [BaseEapConnectionProperties.](baseeapconnectionpropertiesv1schema-schema.md)

Questo elemento **EapType** derivato contiene gli elementi seguenti: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) e [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                     | Tipo                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | Descrive il metodo interno e la configurazione del metodo. Se [**l'elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è TRUE, [**l'elemento Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) deve essere presente. Se [**l'elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è FALSE, [**l'elemento Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) deve essere assente.<br/>           |
| [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | boolean                                                                                                         | Indica se eseguire i controlli di Protezione accesso alla rete. Se [**l'elemento EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) è TRUE, PEAP eseguirà i controlli di Protezione accesso alla rete. se FALSE PEAP non eseguirà i controlli di Protezione accesso alla rete. [**L'elemento EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) è facoltativo.<br/>                                                                                |
| [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | boolean                                                                                                         | Indica se eseguire una riconnessione rapida. Se [**l'elemento FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) è TRUE, PEAP tenta di eseguire una riconnessione rapida. se FALSE, PEAP esegue l'autenticazione completa. [**L'elemento FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) è facoltativo.<br/>                                                                                                                       |
| [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [**IdentityPrivacyParameters**](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | Windows 7 o versione successiva: indica se viene inviata la vera identità di un utente o un'identità anonima. [**L'elemento IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                                                                 |
| [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | boolean                                                                                                         | Indica se eseguire l'accesso GUEST. Se [**l'elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è TRUE, [**l'elemento Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) deve essere presente e descrivere il metodo interno e la relativa configurazione. se FALSE, PEAP eseguirà l'accesso GUEST. [**L'elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è facoltativo.<br/>            |
| [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | [**L'elemento PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) consente miglioramenti futuri dello schema. [**L'elemento PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                    |
| [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | boolean                                                                                                         | Indica se eseguire l'autenticazione con server che supportano la crittografia. Se [**l'elemento RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) è TRUE, PEAP eseguirà l'autenticazione con server che non supportano cryptobinding. se FALSE, PEAP eseguirà l'autenticazione solo con i server che supportano cryptobinding. [**L'elemento RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) è facoltativo.<br/> |
| [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [**Proprietà ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | Contiene informazioni su come eseguire la convalida del server. [**L'elemento ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





