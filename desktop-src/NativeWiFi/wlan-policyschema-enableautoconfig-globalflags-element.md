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
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334399"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy) per WLAN 

L'elemento **enableAutoConfig** (globalFlags) specifica se i computer utilizzano il servizio di configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless. Quando **enableAutoConfig** ha il valore false, i computer non devono usare la configurazione automatica per gestire le connessioni wireless e il servizio di configurazione automatica risponde solo alle richieste per abilitare il servizio. Quando **enableAutoConfig** ha il valore true, i computer possono usare il servizio di configurazione automatica.

Questo elemento è obbligatorio. Quando un profilo viene creato dal servizio di configurazione automatica, questo elemento avrà il valore predefinito TRUE.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

L'elemento **enableAutoConfig** è definito dall'elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




