---
title: Elemento EapType (mschapv2userpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dello schema baseeapuserpropertiesv1. Per mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
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
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334320"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a>Elemento EapType (mschapv2userpropertiesv1schema)

L'elemento **EapType** è un tipo derivato dell'elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) dello schema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .

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
                    <xs:element
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Tipo   | Descrizione                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome utente**](mschapv2userpropertiesv1schema-username-element.md)               |        | Identifica l'utente autenticato. Se questo elemento non è presente, il nome utente viene ottenuto da Winlogon. L'elemento [**username**](mschapv2userpropertiesv1schema-username-element.md) è facoltativo.<br/>                                        |
| [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | string | Identifica il dominio dell'utente o del computer da autenticare. Se questo elemento non è presente, viene usato il dominio di Winlogon. L'elemento [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) è facoltativo.<br/>        |
| [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | string | Identifica la password dell'utente o del computer da autenticare. Se questo elemento non è presente, l'hash della password viene ottenuto da Winlogon. L'elemento [**password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) è facoltativo.<br/> |



## <a name="remarks"></a>Commenti

L'elemento **processContents** consente miglioramenti futuri allo schema. L'elemento **processContents** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





