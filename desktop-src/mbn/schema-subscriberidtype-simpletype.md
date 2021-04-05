---
description: Definisce un tipo per l'elemento SubscriberID del profilo Mobile Broadband.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Tipo semplice subscriberIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049463"
---
# <a name="subscriberidtype-simple-type"></a>Tipo semplice subscriberIdType

Il tipo semplice **subscriberIdType** definisce un tipo per l'elemento [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) del profilo Mobile Broadband. Questo tipo è una raccolta di uno o più caratteri.

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




