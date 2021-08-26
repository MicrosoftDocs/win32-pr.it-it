---
title: Elemento EapType (eaptlsuserpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dallo schema baseeapuserpropertiesv1. Per lo schema eaptlsuserpropertiesv1schema.
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
ms.openlocfilehash: fbc58ab640b7993d274abdb134de4648d51c495c07f70a4468460de1d920bd76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021631"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>Elemento EapType (eaptlsuserpropertiesv1schema)

**L'elemento EapType** è un tipo derivato dell'elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) dallo schema [baseeapuserpropertiesv1.](baseeapuserpropertiesv1schema-schema.md)

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
| [**Nome utente**](eaptlsuserpropertiesv1schema-username-element.md)         |           | Acquisisce il nome utente da inviare nella EAP-Identity risposta. Se [**l'elemento Username**](eaptlsuserpropertiesv1schema-username-element.md) è assente, EAP-TLS usa il nome nel certificato a cui si fa riferimento [**nell'elemento UserCert.**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md)<br/> |
| [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | Hexbinary | Fa riferimento all'hash SHA-1 del certificato che deve essere usato per l'autenticazione.<br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a>Commenti

**L'elemento processContents** consente miglioramenti futuri allo schema. **L'elemento processContents** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





