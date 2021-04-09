---
title: Tipo complesso PeapExtensionsTypeV2
description: Informazioni sul tipo complesso PeapExtensionsTypeV2. Questo tipo consente miglioramenti futuri allo schema.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869e67f16bc9b42929d227755e08bf6924dcc737
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963470"
---
# <a name="peapextensionstypev2-complex-type"></a>Tipo complesso PeapExtensionsTypeV2

Il tipo complesso **PeapExtensionsTypeV2** consente miglioramenti futuri allo schema.


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a>Commenti

L'elemento **PeapExtensionsTypeV2** è facoltativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Tipi complessi mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




