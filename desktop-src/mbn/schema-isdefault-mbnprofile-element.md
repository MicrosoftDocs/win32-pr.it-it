---
description: Specifica se si tratta del profilo predefinito per il dispositivo.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: Elemento IsDefault (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: 7dada4789b0a1c1f11676359972eeff074928ca064c04679e35fb7e83132ef53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065905"
---
# <a name="isdefault-mbnprofile-element"></a>Elemento IsDefault (MBNProfile)

**L'elemento IsDefault (MBNProfile)** specifica se si tratta del profilo predefinito per il dispositivo.

Si tratta di un elemento facoltativo e, se non viene specificato, il profilo non verrà impostato come profilo predefinito.

Il profilo predefinito viene usato dal servizio Mobile Broadband per gli scopi seguenti

-   Il servizio Mobile Broadband usa le impostazioni di connessione del profilo predefinito quando si eseguono connessioni di rete automatiche. Queste impostazioni includono il nome del punto di accesso, il nome utente, la password e così via.
-   I criteri di connessione automatica per un dispositivo Mobile Broadband derivano dal profilo predefinito.
-   L'interfaccia utente di connessione di rete del sistema operativo usa anche i dati di connessione del profilo predefinito per le operazioni di connessione.

I provider di servizi cellulare possono fornire i dettagli di connessione in un profilo e configurare tale profilo come profilo predefinito. Il servizio Mobile Broadband userà queste impostazioni di connessione senza richiedere dettagli all'utente.

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

**L'elemento IsDefault** è definito dall'elemento [**MBNProfile.**](schema-mbnprofile-element.md)

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

 

 




