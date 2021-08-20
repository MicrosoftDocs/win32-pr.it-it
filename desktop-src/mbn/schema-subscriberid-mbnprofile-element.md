---
description: Identifica l'identificatore univoco del profilo.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Elemento SubscriberID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: 42290b0a80e85b2fdd1c794aced78571e939010b0e260bf1bdeba15f221cc103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065885"
---
# <a name="subscriberid-mbnprofile-element"></a>Elemento SubscriberID (MBNProfile)

**L'elemento SubscriberID (MBNProfile)** identifica l'identificatore univoco del profilo.

Per una rete GSM deve contenere l'IMSI (International Mobile Subscriber Identity) della SIM e per i dispositivi CDMA deve contenere il MIN (Numero di identificazione mobile) del dispositivo.

L'elemento è una stringa numerica con una lunghezza massima di 15 cifre.

L'elemento è obbligatorio.

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

**L'elemento SubscriberID** è definito dall'elemento [**MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop \| app UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




