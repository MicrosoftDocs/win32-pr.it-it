---
title: Tipo complesso PeapExtensionsTypeV2
description: Informazioni sul tipo complesso PeapExtensionsTypeV2. Questo tipo consente miglioramenti futuri allo schema.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baea42ec60fe84085ea5e4541848fd43b786419bedab17e938044ff0a713fa07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086030"
---
# <a name="peapextensionstypev2-complex-type"></a>Tipo complesso PeapExtensionsTypeV2

Il **tipo complesso PeapExtensionsTypeV2** consente miglioramenti futuri dello schema.


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

**L'elemento PeapExtensionsTypeV2** è facoltativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Mspeapconnectionpropertiesv2 Tipi complessi](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




