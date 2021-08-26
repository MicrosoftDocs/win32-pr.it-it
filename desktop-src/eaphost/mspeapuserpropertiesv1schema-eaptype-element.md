---
title: Elemento EapType (mspeapuserpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dallo schema baseeapuserpropertiesv1. Per lo schema mspeapuserpropertiesv1schema.
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
ms.openlocfilehash: e27923d77a36b917b3356b7c5c79d408bc0a99d49d70967677b56a9047ed0b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067181"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a>Elemento EapType (mspeapuserpropertiesv1schema)

**L'elemento EapType** è un tipo derivato dell'elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) dallo schema [baseeapuserpropertiesv1.](baseeapuserpropertiesv1schema-schema.md)

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
| [**Eap**](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | [**L'elemento Eap**](baseeapuserpropertiesv1schema-eap-element.md) identifica il metodo interno e le credenziali da usare con tale metodo. Quando la configurazione PEAP è configurata per l'accesso guest PEAP, questo elemento è assente.<br/>                                  |
| [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [**PeapExtensionsType**](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | [**L'elemento PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) consente miglioramenti futuri dello schema. <br/> [**L'elemento PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) è facoltativo.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





