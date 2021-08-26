---
title: Registrazione di una DLL di sicurezza RAS
description: Il programma di installazione per una DLL di sicurezza RAS deve registrare la DLL con il server RAS Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5ca32aa687649c80917f9a072b9d4cbeb0f1f4e8ba61ce090e7781bb04cdefd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028415"
---
# <a name="registering-a-ras-security-dll"></a>Registrazione di una DLL di sicurezza RAS

Il programma di installazione per una DLL di sicurezza RAS deve registrare la DLL con il server RAS Windows NT/Windows 2000. Non è possibile registrare una sola DLL di sicurezza RAS come supporto per più DLL di sicurezza. Per registrare una DLL di sicurezza RAS, impostare il *valore DLLPath* nella chiave seguente nel Registro di sistema:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| Nome del valore | Dati del valore                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DLLPath*  | Stringa **REG \_ SZ** che contiene il percorso della DLL. Questa stringa deve specificare il percorso completo a meno che la DLL non si trova in una directory elencata nel percorso di sistema. |



 

Anche il programma di installazione per una DLL di sicurezza RAS deve fornire funzionalità di rimozione/disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare il *valore DLLPath* dal Registro di sistema. Il servizio RAS non viene avviato se il *valore DLLPath* specifica una DLL che non è possibile trovare.

Una DLL di sicurezza RAS deve esportare [**le funzioni RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) e [**RasSecurityDialogEnd.**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend)

 

 




