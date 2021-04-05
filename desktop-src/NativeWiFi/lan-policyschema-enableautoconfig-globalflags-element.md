---
description: Specifica se i computer utilizzano il servizio di configurazione automatica incorporato per gestire le connessioni a reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1 X.
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
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757799"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy)

L'elemento **enableAutoConfig** (globalFlags) specifica se i computer utilizzano il servizio di configurazione automatica incorporato per gestire le connessioni a reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1 x.

Se il valore di **enableAutoConfig** è false, i computer non devono usare il servizio di configurazione automatica incorporato per gestire le connessioni che richiedono l'autenticazione di livello 2. La rete specificata nell'elemento [**Profiler**](lan-policyschema-profilelist-lanpolicy-element.md) è invece l'unica rete disponibile per la connessione. Il servizio di configurazione automatica risponderà solo alle richieste di abilitazione del servizio.

Quando **enableAutoConfig** ha il valore true, i computer possono usare il servizio di configurazione automatica incorporato per connettersi alle reti cablate che richiedono l'autenticazione di livello 2.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

L'elemento **enableAutoConfig** è definito dall'elemento [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**globalFlags (LANPolicy)**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




