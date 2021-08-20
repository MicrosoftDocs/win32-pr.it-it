---
description: Specifica un tipo di rete.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Elemento networkType (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 57616d6701ab4663fa6757ddec5df4886ec02faaf5088f61b6cb466ca834ec81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684391"
---
# <a name="networktype-networkitemtype-element"></a>Elemento networkType (networkItemType)

L'elemento networkType (networkItemType) specifica un tipo di rete. Esistono due tipi di reti: reti di infrastruttura (ESS) e reti ad hoc (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

**L'elemento networkType** è definito dal tipo complesso [**networkItemType.**](wlan-policyschema-networkitemtype-complextype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Possibili elementi padre immediati nell'istanza dello schema**
</dt> <dt>

[**network (allowList)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**network (blockList)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




