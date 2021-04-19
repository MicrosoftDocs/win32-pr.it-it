---
title: Elemento EapType (eaptlsuserpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dello schema baseeapuserpropertiesv1. Per eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
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
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334319"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>Elemento EapType (eaptlsuserpropertiesv1schema)

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
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
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



| Elemento                                                                   | Tipo      | Descrizione                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome utente**](eaptlsuserpropertiesv1schema-username-element.md)         |           | Acquisisce il nome utente da inviare nella risposta EAP-Identity. Se l'elemento [**username**](eaptlsuserpropertiesv1schema-username-element.md) è assente, EAP-TLS usa il nome nel certificato a cui si fa riferimento nell'elemento [**userCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .<br/> |
| [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | hexBinary | Si riferisce all'hash SHA-1 del certificato che deve essere utilizzato per l'autenticazione.<br/>                                                                                                                                                                                                                             |



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

[Schema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





