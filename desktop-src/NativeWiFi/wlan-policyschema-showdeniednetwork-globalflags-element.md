---
description: Specifica se le reti negate vengono visualizzate nella Connessione a una procedura guidata di rete.
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
ms.openlocfilehash: 04c6c95f9c9db4c6b88a5258ced4b272947a932342a82d380be36210c3196521
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064711"
---
# <a name="showdeniednetwork-globalflags-element"></a>Elemento showDeniedNetwork (globalFlags)

**L'elemento showDeniedNetwork** (globalFlags) specifica se le reti negate vengono visualizzate nella procedura guidata Connessione **a una** rete. Le reti possono essere negate da Criteri di gruppo o dalle impostazioni utente. Quando **showDeniedNetwork** ha il valore TRUE, le reti negate vengono visualizzate nella procedura guidata Connessione **a una rete.** In caso contrario, le reti negate non vengono visualizzate nella procedura guidata.

Questo elemento è obbligatorio. Quando un profilo viene creato dal servizio AutoConfig, questo elemento avrà il valore predefinito FALSE.

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

**L'elemento showDeniedNetwork** è definito dall'elemento [**globalFlags.**](wlan-policyschema-globalflags-wlanpolicy-element.md)

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

 

 




