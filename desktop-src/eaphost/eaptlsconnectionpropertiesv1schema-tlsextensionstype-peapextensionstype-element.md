---
title: AcceptServerName
description: Indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento ServerNames (ServerValidationParameters). | AcceptServerName
ms.assetid: 440a46ae-7fef-4e97-9fd7-cbd20143597b
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
ms.openlocfilehash: beb12da9897cc0e77480f609edee632c135b5c5d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234768"
---
# <a name="acceptservername"></a>AcceptServerName

L'elemento **AcceptServerName (EapType)** indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento [**serverNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: AcceptServerName"
 />
```

L'elemento è definito dall'elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

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

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**AcceptServerName (EapType)**](eaptlsconnectionpropertiesv2schema-acceptservername-eaptype-element.md)
</dt> </dl>

 

 





