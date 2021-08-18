---
title: Elemento InnerEapOptional (EapType)
description: Informazioni sull'elemento InnerEapOptional (EapType). Questo elemento indica se eseguire l'accesso GUEST.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Elemento InnerEapOptional EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 372163b39ea788b5c03bd25aedcc44aee172d58080fb94e3333a029a514962a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404591"
---
# <a name="innereapoptional-eaptype-element"></a>Elemento InnerEapOptional (EapType)

**L'elemento InnerEapOptional (EapType)** indica se eseguire l'accesso GUEST.

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

**L'elemento InnerEapOptional** è definito dall'elemento [**EapType.**](mspeapconnectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Commenti

Se **l'elemento InnerEapOptional** è TRUE, [**l'elemento Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) deve essere presente e descrivere il metodo interno e la configurazione. se FALSE, PEAP eseguirà l'accesso GUEST. **L'elemento InnerEapOptional** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





