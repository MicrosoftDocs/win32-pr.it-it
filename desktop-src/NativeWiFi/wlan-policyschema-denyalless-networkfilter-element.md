---
description: Specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: Elemento denyAllESS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5057f94dd91e2d7090c4f147ba987324e369dda706031ecebb8a79b165214414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619866"
---
# <a name="denyalless-networkfilter-element"></a>Elemento denyAllESS (networkFilter)

L'elemento denyAllESS (networkFilter) specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato. Quando **denyAllESS ha** valore TRUE, i computer non possono connettersi a una rete di infrastruttura. in caso contrario, i computer possono connettersi alle reti dell'infrastruttura.

Il valore predefinito per questo elemento è FALSE. Se **denyAllESS** non è specificato in un profilo, per impostazione predefinita i computer possono connettersi alle reti dell'infrastruttura.

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

**L'elemento denyAllESS** è definito dall'elemento [**networkFilter.**](wlan-policyschema-networkfilter-wlanpolicy-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




