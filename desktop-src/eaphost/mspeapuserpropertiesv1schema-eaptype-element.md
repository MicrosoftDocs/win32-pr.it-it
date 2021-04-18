---
title: Elemento EapType (mspeapuserpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dello schema baseeapuserpropertiesv1. Per mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
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
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334339"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a>Elemento EapType (mspeapuserpropertiesv1schema)

L'elemento **EapType** è un tipo derivato dell'elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) dello schema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .

``` syntax
<xs:element name="EapType
        "
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
                        maxOccurs="unbounded"
                        ref="Eap"
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



| Elemento                                                                               | Tipo                                                                                      | Descrizione                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | L'elemento [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) identifica il metodo interno e le credenziali da utilizzare con il metodo. Quando la configurazione PEAP è configurata per l'accesso Guest PEAP, questo elemento è assente.<br/>                                  |
| [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [**PeapExtensionsType**](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | L'elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) consente miglioramenti futuri allo schema. <br/> L'elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) è facoltativo.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





