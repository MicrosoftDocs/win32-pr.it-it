---
description: Elenca le esportazioni di DLL che devono essere implementate per creare una gestione credenziali.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementazione di gestione credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884506"
---
# <a name="implementing-a-credential-manager"></a>Implementazione di gestione credenziali

Per creare una gestione credenziali, è necessario creare una DLL che esporti le funzioni seguenti:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Per ripristinare le notifiche per le funzioni [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) per l'accesso con smart card, creare una voce del registro di sistema denominata **SmartCardLogonNotify** come **DWORD** e impostarla su 1:

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

**Windows Server 2003 e Windows XP:** La voce del registro di sistema **SmartCardLogonNotify** non è obbligatoria.

Inoltre, i gestori delle credenziali devono supportare anche la funzione [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) per l'avvio di WNNC \_ (il supporto di altri indici non è necessario per i gestori delle credenziali). Ciò indica a MPR quando viene avviato un gestore delle credenziali. Chiamando **NPGetCaps** con il parametro *NINDEX* impostato su WNNC \_ Start, il MPR ottiene il tempo di attesa prima di chiamare le funzioni del punto di ingresso di gestione delle credenziali del provider. Se il server di gestione delle credenziali dispone di queste informazioni, è possibile inviarlo a gestione credenziali, impostando il timeout.

 

 



