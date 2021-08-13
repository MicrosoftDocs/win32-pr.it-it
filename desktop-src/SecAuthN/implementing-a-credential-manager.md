---
description: Elenca le esportazioni DLL che devono essere implementate per creare un gestore di credenziali.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementazione di un Gestione credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a1787fcf72d88ad809f904f9f83179ac86631b83a23314f9d24ee31ce3dec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482661"
---
# <a name="implementing-a-credential-manager"></a>Implementazione di un Gestione credenziali

Per creare un gestore di credenziali, è necessario creare una DLL che esporta le funzioni seguenti:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Per ripristinare le notifiche alle funzioni [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) per l'accesso smart card, creare una voce del Registro di sistema denominata **SmartCardLogonNotify** come **DWORD** e impostarla su 1:

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

**Windows Server 2003 e Windows XP:** La voce del Registro di sistema **SmartCardLogonNotify** non è necessaria.

Inoltre, i gestori di credenziali devono supportare anche la funzione [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) per WNNC START (il supporto di altri indici non è necessario \_ per i gestori di credenziali). In questo modo viene indicato all'MPR quando verrà avviato un gestore di credenziali. Chiamando **NPGetCaps** con il parametro *nIndex* impostato su WNNC START, la MPR ottiene il tempo di attesa prima di chiamare le funzioni del punto di ingresso di gestione delle credenziali \_ del provider. E se la password mpr contiene queste informazioni, può inoltrarla al gestore di credenziali, impostando il timeout.

 

 



