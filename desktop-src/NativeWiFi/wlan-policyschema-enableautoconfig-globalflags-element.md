---
description: Specifica se i computer utilizzano il servizio di configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: Elemento enableAutoConfig (globalFlags) (LAN_policy) per WLAN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 77b09bf046cdbadb58c888a3084d14ed14794064bf9f11c110ccecaff105fceb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684411"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy) per WLAN 

**L'elemento enableAutoConfig** (globalFlags) specifica se i computer usano il servizio di configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless. Quando **enableAutoConfig** ha il valore FALSE, i computer non devono usare AutoConfig per gestire le connessioni wireless e il servizio AutoConfig risponde solo alle richieste di abilitazione del servizio. Quando **enableAutoConfig ha** valore TRUE, i computer possono usare il servizio AutoConfig.

Questo elemento è obbligatorio. Quando un profilo viene creato dal servizio AutoConfig, questo elemento avrà il valore predefinito TRUE.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

**L'elemento enableAutoConfig** è definito dall'elemento [**globalFlags.**](wlan-policyschema-globalflags-wlanpolicy-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




