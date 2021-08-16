---
description: Specifica se il dispositivo Mobile Broadband si connetterà automaticamente a una rete.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Elemento AutoConnectOnInternet (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: 3a10804e91ee34125c25c320a49b5f7251f720ed9ce6c770c2aa4af5167a8511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881476"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>Elemento AutoConnectOnInternet (MBNProfile)

**L'elemento AutoConnectOnInternet (MBNProfile)** specifica se il dispositivo Mobile Broadband si connetterà automaticamente a una rete.

Se impostato su **FALSE,** la logica di connessione automatica del servizio Mobile Broadband non verrà usata se è disponibile un'altra connettività di rete per il sistema. Se impostato su **TRUE,** il servizio Mobile Broadband tenterà di connettere automaticamente il dispositivo alla rete in base all'impostazione di connessione automatica definita [**nell'elemento ConnectionMode.**](schema-connectionmode-mbnprofile-element.md)

**Windows 8 e versioni successive:** Questo elemento è deprecato. Usare invece [**il metodo WcmSetProperty con**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) il parametro *Property* impostato su **wcm global property \_ minimize \_ \_ \_ policy.**

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

**L'elemento AutoConnectOnInternet** è definito dall'elemento [**MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

