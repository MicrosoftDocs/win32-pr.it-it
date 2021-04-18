---
title: Elemento EapType (mspeapconnectionpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dello schema BaseEapConnectionProperties. Per mspeapconnectionpropertiesv1schema.
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
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334325"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a>Elemento EapType (mspeapconnectionpropertiesv1schema)

L'elemento **EapType** è un tipo derivato dell'elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) dello schema [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .

Questo elemento **EapType** derivato contiene gli elementi seguenti: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**per riconnessione rapida**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) e [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).

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
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | Descrive il metodo interno e la configurazione del metodo. Se l'elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è true, è necessario che l'elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) sia presente. Se l'elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è false, l'elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) deve essere assente.<br/>           |
| [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | boolean                                                                                                         | Indica se eseguire i controlli di protezione accesso alla rete (NAP). Se l'elemento [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) è true, PEAP eseguirà i controlli NAP; Se FALSE PEAP non eseguirà controlli NAP. L'elemento [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) è facoltativo.<br/>                                                                                |
| [**Per riconnessione rapida**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | boolean                                                                                                         | Indica se eseguire una riconnessione rapida. Se l'elemento [**per riconnessione rapida**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) è true, PEAP tenta di eseguire una riconnessione rapida. Se FALSE, PEAP esegue l'autenticazione completa. L'elemento [**per riconnessione rapida**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) è facoltativo.<br/>                                                                                                                       |
| [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [**IdentityPrivacyParameters**](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | Windows 7 o versioni successive: indica se viene inviata un'identità vera o anonima dell'utente. L'elemento [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                                                                 |
| [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | boolean                                                                                                         | Indica se eseguire l'accesso GUEST. Se l'elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è true, è necessario che l'elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) sia presente e descriva il metodo interno e la relativa configurazione. Se FALSE, PEAP eseguirà l'accesso GUEST. L'elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è facoltativo.<br/>            |
| [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | L'elemento [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) consente miglioramenti futuri allo schema. L'elemento [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                    |
| [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | boolean                                                                                                         | Indica se eseguire l'autenticazione con i server che supportano la crittografia. Se l'elemento [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) è true, PEAP eseguirà l'autenticazione con i server che non supportano Crypto; Se FALSE, PEAP eseguirà l'autenticazione solo con i server che supportano la crittografia. L'elemento [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) è facoltativo.<br/> |
| [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | Contiene informazioni su come eseguire la convalida del server. L'elemento [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





