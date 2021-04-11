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
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226013"
---
# <a name="denyalless-networkfilter-element"></a>Elemento denyAllESS (networkFilter)

L'elemento denyAllESS (networkFilter) specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato. Quando **denyAllESS** ha il valore true, i computer non possono connettersi a una rete dell'infrastruttura; in caso contrario, i computer possono connettersi alle reti dell'infrastruttura.

Il valore predefinito per questo elemento è FALSE. Se **denyAllESS** non è specificato in un profilo, per impostazione predefinita i computer possono connettersi alle reti dell'infrastruttura.

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

L'elemento **denyAllESS** è definito dall'elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 




