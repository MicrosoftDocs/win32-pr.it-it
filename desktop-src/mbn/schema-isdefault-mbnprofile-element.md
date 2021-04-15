---
description: Specifica se questo è il profilo predefinito per il dispositivo.
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
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484828"
---
# <a name="isdefault-mbnprofile-element"></a>Elemento IsDefault (MBNProfile)

L'elemento **IsDefault (MBNProfile)** specifica se questo è il profilo predefinito per il dispositivo.

Si tratta di un elemento facoltativo e, se non è specificato, il profilo non verrà impostato come profilo predefinito.

Il profilo predefinito viene usato dal servizio Mobile Broadband per gli scopi seguenti

-   Il servizio Mobile Broadband usa le impostazioni di connessione del profilo predefinito durante l'esecuzione di connessioni di rete automatiche. Queste impostazioni includono il nome del punto di accesso, il nome utente, la password e così via.
-   Il criterio di connessione automatica per un dispositivo mobile broadband viene tratto dal profilo predefinito.
-   L'interfaccia utente della connessione di rete del sistema operativo usa anche i dati di connessione del profilo predefinito per le operazioni di connessione.

I provider di servizi cellulari possono fornire i dettagli della connessione in un profilo e configurare tale profilo come profilo predefinito. Il servizio Mobile Broadband utilizzerà queste impostazioni di connessione senza richiedere informazioni all'utente.

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

L'elemento **IsDefault** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .

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

 

 




