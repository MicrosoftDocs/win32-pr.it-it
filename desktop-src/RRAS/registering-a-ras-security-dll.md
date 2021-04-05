---
title: Registrazione di una DLL di sicurezza RAS
description: Il programma di installazione di una DLL di sicurezza RAS deve registrare la DLL con il server RAS Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709859"
---
# <a name="registering-a-ras-security-dll"></a>Registrazione di una DLL di sicurezza RAS

Il programma di installazione di una DLL di sicurezza RAS deve registrare la DLL con il server RAS Windows NT/Windows 2000. È possibile registrare solo una DLL di sicurezza RAS perché non è disponibile il supporto per più DLL di sicurezza. Per registrare una DLL di sicurezza RAS, impostare il valore *DllPath* nella chiave seguente del registro di sistema:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| Nome del valore | Dati del valore                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DLLPath*  | Stringa **reg \_ SZ** che contiene il percorso della dll. Questa stringa deve specificare il percorso completo, a meno che la DLL non si trovi in una directory elencata nel percorso di sistema. |



 

Anche il programma di installazione di una DLL di sicurezza RAS deve fornire la funzionalità di rimozione/disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare il valore *DllPath* dal registro di sistema. Il servizio RAS non viene avviato se il valore *DllPath* specifica una dll non trovata.

Una DLL di sicurezza RAS deve esportare le funzioni [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) e [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) .

 

 




