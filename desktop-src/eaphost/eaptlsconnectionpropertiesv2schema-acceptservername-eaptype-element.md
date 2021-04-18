---
title: Elemento AcceptServerName
description: Indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento ServerNames (ServerValidationParameters). | Elemento AcceptServerName
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
ms.openlocfilehash: b48c43bce2bd71f4d761ea58fcdf5e0632107f87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321440"
---
# <a name="acceptservername-element"></a>Elemento AcceptServerName

L'elemento **AcceptServerName (EapType)** indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento [**serverNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

L'elemento **AcceptServerName** è definito dall'elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

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

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementi dello schema eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[**AcceptServerName (EapType)**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





