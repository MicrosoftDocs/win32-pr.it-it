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
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306499"
---
# <a name="denyallibss-networkfilter-element"></a>Elemento denyAllIBSS (networkFilter)

L'elemento denyAllIBSS (networkFilter) specifica se l'accesso a tutte le reti ad hoc è bloccato. Quando **denyAllIBSS** ha il valore true, i computer non possono connettersi a una rete ad hoc; in caso contrario, è possibile che i computer si connettano alle reti ad hoc.

Il valore predefinito per questo elemento è FALSE. Se **denyAllIBSS** non è specificato in un profilo, per impostazione predefinita i computer possono connettersi alle reti ad hoc.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

L'elemento **denyAllIBSS** è definito dall'elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

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

 

 




