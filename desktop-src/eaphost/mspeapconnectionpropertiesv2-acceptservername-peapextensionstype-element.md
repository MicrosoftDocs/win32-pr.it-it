---
title: Elemento AcceptServerName (PeapExtensionsType)
description: L'elemento AcceptServerName (PeapExtensionsType) indica se il nome del server viene convalidato rispetto alla stringa del nome specificata in ServerNames nello schema mspeapconnectionpropertiesv2.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Elemento AcceptServerName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b608629c9eb9d3e3fb592ead73ddc0ba9545e6b92a642adf4ce76bb0524b57ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086040"
---
# <a name="acceptservername-peapextensionstype-element"></a>Elemento AcceptServerName (PeapExtensionsType)

**L'elemento AcceptServerName (PeapExtensionsType)** indica se il nome del server viene convalidato rispetto alla stringa del nome specificata nell'elemento [**ServerNames (ServerValidationParameters).**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

**L'elemento AcceptServerName** è definito dall'elemento [**PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)

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

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





