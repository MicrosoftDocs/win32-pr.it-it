---
title: Elemento RequireCryptoBinding (EapType)
description: Indica se eseguire l'autenticazione con server che supportano la crittografia.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Elemento RequireCryptoBinding EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c4f4169e6ac0af123085795374b06de854b261b5f22004bd726ad47488bc11d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067221"
---
# <a name="requirecryptobinding-eaptype-element"></a>Elemento RequireCryptoBinding (EapType)

**L'elemento RequireCryptoBinding (EapType)** indica se eseguire l'autenticazione con server che supportano cryptobinding.

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

**L'elemento RequireCryptoBinding** è definito dall'elemento [**EapType.**](mspeapconnectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Commenti

Se **l'elemento RequireCryptoBinding** è TRUE, PEAP eseguirà l'autenticazione con server che non supportano cryptobinding. se FALSE, PEAP eseguirà l'autenticazione solo con i server che supportano cryptobinding. **L'elemento RequireCryptoBinding** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





