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
ms.openlocfilehash: aac83be84ae313f572d82e6b4c9a2afb14beeb7e15c531eaae7efd67bcc90464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881365"
---
# <a name="subscriberidtype-simple-type"></a>Tipo semplice subscriberIdType

Il **tipo semplice subscriberIdType** definisce un tipo per l'elemento [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) del profilo Mobile Broadband. Questo tipo è una raccolta di uno o più caratteri.

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
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




