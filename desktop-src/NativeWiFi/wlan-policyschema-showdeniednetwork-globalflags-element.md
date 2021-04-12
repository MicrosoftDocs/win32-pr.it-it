---
description: Specifica se le reti negate vengono visualizzate nella procedura guidata Connetti a una rete.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Elemento showDeniedNetwork (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527799"
---
# <a name="showdeniednetwork-globalflags-element"></a>Elemento showDeniedNetwork (globalFlags)

L'elemento **showDeniedNetwork** (globalFlags) specifica se le reti negate vengono visualizzate nella procedura guidata **Connetti a una rete** . Le reti possono essere negate da criteri di gruppo o da impostazioni utente. Quando **showDeniedNetwork** ha il valore true, le reti negate vengono visualizzate nella procedura guidata **Connetti a rete** ; in caso contrario, le reti negate non vengono visualizzate nella procedura guidata.

Questo elemento è obbligatorio. Quando un profilo viene creato dal servizio di configurazione automatica, questo elemento prenderà il valore predefinito FALSE.

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

L'elemento **showDeniedNetwork** è definito dall'elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

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

 

 




