---
description: Specifica se il dispositivo mobile broadband si connetterà automaticamente a una rete.
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
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226193"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>Elemento AutoConnectOnInternet (MBNProfile)

L'elemento **AutoConnectOnInternet (MBNProfile)** specifica se il dispositivo mobile broadband si connetterà automaticamente a una rete.

Se è impostato su **false**, la logica di connessione automatica del servizio Mobile Broadband non verrà usata se per il sistema sono disponibili altre connessioni di rete. Se è impostato su **true**, il servizio Mobile Broadband tenterà di connettere automaticamente il dispositivo alla rete in base all'impostazione di connessione automatica definita nell'elemento [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) .

**Windows 8 e versioni successive:** Questo elemento è deprecato. Usare invece il metodo [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) con il parametro *Property* impostato su **file WCM \_ Global \_ Property \_ minimizzi \_ policy** .

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

L'elemento **AutoConnectOnInternet** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

