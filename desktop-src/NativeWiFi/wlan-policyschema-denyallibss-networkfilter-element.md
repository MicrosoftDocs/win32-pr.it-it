---
description: Specifica se l'accesso a tutte le reti ad hoc è bloccato.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Elemento denyAllIBSS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9f34a45a0fc527c4c27e24ad3137dfe49438f9255baf1893e1090137bfb40a3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619536"
---
# <a name="denyallibss-networkfilter-element"></a>Elemento denyAllIBSS (networkFilter)

L'elemento denyAllIBSS (networkFilter) specifica se l'accesso a tutte le reti ad hoc è bloccato. Quando **denyAllIBSS ha** valore TRUE, i computer non possono connettersi a una rete ad hoc. in caso contrario, i computer possono connettersi a reti ad hoc.

Il valore predefinito per questo elemento è FALSE. Se **denyAllIBSS** non è specificato in un profilo, per impostazione predefinita i computer possono connettersi a reti ad hoc.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

**L'elemento denyAllIBSS** è definito dall'elemento [**networkFilter.**](wlan-policyschema-networkfilter-wlanpolicy-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




