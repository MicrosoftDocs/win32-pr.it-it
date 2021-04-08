---
title: Tipo complesso TLSExtensionsType
description: Informazioni sul tipo complesso TLSExtensionsType. Questo tipo consente miglioramenti futuri allo schema.
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a93b9ecb0ba32a95e4c85856ac015f5135fb5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730330"
---
# <a name="tlsextensionstype-complex-type"></a>Tipo complesso TLSExtensionsType

Il tipo complesso **TLSExtensionsType** consente miglioramenti futuri allo schema.


```XML
<xs:complexType name="TLSExtensionsType">
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

L'elemento **TLSExtensionsType** è facoltativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Tipi complessi eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**TLSExtensions (TLSExtensionsType)**](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 




