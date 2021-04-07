---
description: Ogni server può impostare un valore della chiave del registro di sistema MachineID nel registro di sistema che viene impostato come parte fissa dell'ID di sessione.
ms.assetid: 1B373496-1C1B-4D4B-8CAC-B572C58E43A2
title: Bilanciamento del carico con Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce190d665f4cc41eb0615a2ddc83e0ee54798d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882373"
---
# <a name="load-balancing-using-schannel"></a>Bilanciamento del carico con Schannel

Ogni server può impostare un valore della chiave del registro di sistema MachineID nel registro di sistema che viene impostato come parte fissa dell'ID di sessione. La chiave del registro di sistema MachineID è un tipo di valore **reg \_ DWORD** . Il servizio di bilanciamento del carico può usare questa parte dell'ID di sessione per determinare quale server ha generato la sessione SSL e può gestire la mappa a tale server. L'ID sessione fa parte dell'handshake SSL/TLS inviato in rete. Il codice del servizio di bilanciamento del carico deve usare il secondo **valore DWORD** nell'ID sessione durante la ripresa o la riconnessione al client. Il secondo **valore DWORD** dell'ID di sessione casuale generato da un Server Schannel viene sostituito dal **valore DWORD** archiviato nel registro di sistema. Il valore del registro di sistema per **DWORD** non può essere 0xffffffff.

Il valore della chiave del registro di sistema è il seguente.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            SecurityProviders
               SCHANNEL
                  MachineID<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

 

 



