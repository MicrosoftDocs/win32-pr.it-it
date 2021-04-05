---
title: Elemento AcceptServerName (PeapExtensionsType)
description: Indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento ServerNames (ServerValidationParameters). | Elemento AcceptServerName (PeapExtensionsType)
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- elemento EAPHost
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
ms.openlocfilehash: 1c877819fd559cb26cd93c5d5456631a93a49545
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058530"
---
# <a name="acceptservername-peapextensionstype-element"></a>Elemento AcceptServerName (PeapExtensionsType)

L'elemento **AcceptServerName (PeapExtensionsType)** indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento [**serverNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

L'elemento è definito dall'elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

## <a name="remarks"></a>Commenti

L'elemento **AcceptServerName** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



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

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**AcceptServerName**](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





