---
title: Elemento EapType (eaptlsconnectionpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dallo schema BaseEapConnectionProperties. Per eaptlsconnectionpropertiesv1schema.
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
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
ms.openlocfilehash: b7d448524c65e53ad9142d52786a651e085eddcfc7f3eb28bff558a38fc619fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785206"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a>Elemento EapType (eaptlsconnectionpropertiesv1schema)

**L'elemento EapType** è un tipo derivato dell'elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) dallo schema [BaseEapConnectionProperties.](baseeapconnectionpropertiesv1schema-schema.md)

Questo elemento **EapType derivato** contiene gli elementi seguenti: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)e [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).

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
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                                               | Tipo                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**extendedTLS: PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | Windows 7 e versioni successive: indica se viene eseguita la convalida del server.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**extendedTLS: AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | Windows 7 e versioni successive: indica se il nome di un server è letto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**extendedTLS: TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | Windows 7 e versioni successive: abilita i miglioramenti futuri dello schema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | Contiene informazioni sul percorso del certificato EAP Transport Level Security (EAP-TLS). <br/> [**L'elemento CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | boolean                                                                                                           | Determina il nome utente che EAP-TLS deve usare. <br/> Se [**l'elemento DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) **è TRUE,** EAP-TLS deve usare un nome utente diverso da quello visualizzato nel certificato. Se [**l'elemento DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) **è FALSE,** EAP-TLS usa il nome utente visualizzato nel certificato.<br/> [**L'elemento DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) è facoltativo. <br/> |
| [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [**Proprietà ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | Contiene informazioni su come eseguire la convalida del server. [**L'elemento ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) è facoltativo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





