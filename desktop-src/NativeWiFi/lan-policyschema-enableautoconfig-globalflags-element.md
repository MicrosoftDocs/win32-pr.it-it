---
description: Specifica se i computer usano il servizio di configurazione automatica incorporato per gestire le connessioni alle reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1X.
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: Elemento enableAutoConfig (globalFlags) (LAN_policy)
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
ms.openlocfilehash: 2842da69b07136df80d15ea84553aecdf2c62d417c73f7ec85d9c315b819a397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780201"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy)

**L'elemento enableAutoConfig** (globalFlags) specifica se i computer usano il servizio di configurazione automatica incorporato per gestire le connessioni alle reti cablate che richiedono l'autenticazione di livello 2 , ad esempio 802.1X.

Quando **enableAutoConfig ha** il valore FALSE, i computer non devono usare il servizio di configurazione automatica predefinito per gestire le connessioni che richiedono l'autenticazione di livello 2. La rete specificata nell'elemento [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) è invece l'unica rete disponibile per la connessione. Il servizio di configurazione automatica risponderà solo alle richieste di abilitazione del servizio.

Quando **enableAutoConfig ha** il valore TRUE, i computer possono usare il servizio di configurazione automatica predefinito per connettersi alle reti cablate che richiedono l'autenticazione di livello 2.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

**L'elemento enableAutoConfig** è definito dall'elemento [**globalFlags.**](lan-policyschema-globalflags-lanpolicy-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**globalFlags (LANPolicy)**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




