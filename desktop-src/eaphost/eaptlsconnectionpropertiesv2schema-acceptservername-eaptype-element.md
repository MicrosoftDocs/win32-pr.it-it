---
title: AcceptServerName - elemento
description: Indica se il nome del server viene convalidato rispetto alla stringa del nome specificata nell'elemento ServerNames (ServerValidationParameters). | AcceptServerName - elemento
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- Elemento AcceptServerName EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69cb60d89824c4b6bf83f4903e96b1856433e367e647d19657b70888839595f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273703"
---
# <a name="acceptservername-element"></a>AcceptServerName - elemento

**L'elemento AcceptServerName (EapType)** indica se il nome del server viene convalidato rispetto alla stringa del nome specificata nell'elemento [**ServerNames (ServerValidationParameters).**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

**L'elemento AcceptServerName** è definito dall'elemento [**EapType.**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Commenti

**L'elemento AcceptServerName** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementi dello schema eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[**AcceptServerName (EapType)**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





