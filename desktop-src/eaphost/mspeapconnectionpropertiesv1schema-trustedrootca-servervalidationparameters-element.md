---
title: Elemento TrustedRootCA (ServerValidationParameters) (V1)
description: Acquisisce la stampa Thumb delle autorità di certificazione radice ritenute attendibili dal client. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
keywords:
- Elemento TrustedRootCA EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389078"
---
# <a name="trustedrootca-servervalidationparameters-element"></a>Elemento TrustedRootCA (ServerValidationParameters)

L'elemento **TrustedRootCA (ServerValidationParameters)** elemento acquisisce la stampa Thumb delle autorità di certificazione radice che sono considerate attendibili dal client.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

L'elemento **TrustedRootCA** è definito dal tipo complesso [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Commenti

La stampa Thumb è una stringa esadecimale che contiene l'hash SHA-1 del certificato. L'elemento **TrustedRootCA** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Possibili elementi padre immediati nell'istanza dello schema**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





