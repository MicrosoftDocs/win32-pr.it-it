---
title: Rilevamento delle modifiche
description: Alcune applicazioni devono mantenere la coerenza tra dati specifici archiviati nel servizio directory Active Directory e altri dati.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, rilevamento delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956296"
---
# <a name="tracking-changes"></a>Rilevamento delle modifiche

Alcune applicazioni devono mantenere la coerenza tra dati specifici archiviati nel servizio directory Active Directory e altri dati. Gli altri dati potrebbero essere archiviati nella directory, in una tabella SQL Server, in un file o nel registro di sistema. Quando i dati archiviati nella directory cambiano, è possibile che gli altri dati vengano modificati per rimanere coerenti. Le applicazioni che presentano questo requisito includono:

Questa sezione non include i meccanismi usati per il monitoraggio delle applicazioni. Si tratta di applicazioni che eseguono il monitoraggio delle modifiche della directory non allo scopo di gestire dati coerenti tra archivi distinti, ma come strumento di gestione del sistema. Sebbene le applicazioni di monitoraggio possano utilizzare gli stessi meccanismi che supportano le applicazioni di rilevamento delle modifiche, i meccanismi seguenti sono appositamente progettati per il monitoraggio delle applicazioni:

-   Controllo di sicurezza. Modificando la parte dell'elenco di controllo di accesso di sistema (SACL) di un descrittore di sicurezza di un oggetto, è possibile fare in modo che gli accessi all'oggetto in un determinato controller di dominio creino record di controllo nel registro eventi di protezione. È possibile controllare le letture, le Scritture o entrambe le operazioni; è possibile controllare l'intero oggetto o attributi specifici. Per altre informazioni, vedere [recupero del SACL di un oggetto](retrieving-an-objectampaposs-sacl.md) e [generazione del controllo](/windows/desktop/SecAuthZ/audit-generation).
-   Registrazione eventi Modificando le impostazioni del registro di sistema in un controller di dominio specifico, è possibile modificare i tipi di eventi registrati nel registro eventi del servizio directory. In particolare, per registrare tutte le modifiche, impostare il valore di **accesso alla directory 8** sotto la chiave del registro di sistema seguente su 4.

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    Per ulteriori informazioni, vedere [registrazione degli eventi](/windows/desktop/EventLog/event-logging).

-   Traccia eventi. In Windows 2000 è stata introdotta un'API di traccia eventi per la traccia e la registrazione di eventi interessanti in software o hardware. Il sistema operativo Windows e Active Directory Domain Services in particolare supportano l'utilizzo di traccia eventi per la pianificazione della capacità e l'analisi dettagliata delle prestazioni. Per ulteriori informazioni, vedere [traccia eventi](/windows/desktop/ETW/event-tracing-portal) e [traccia eventi in ADSI](/windows/desktop/ADSI/adsi-and-etw).

Questa sezione include gli argomenti seguenti:

-   [Cenni preliminari sulle tecniche di Rilevamento modifiche](overview-of-change-tracking-techniques.md)
-   [Modificare le notifiche in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md)
-   [Polling delle modifiche tramite il controllo DirSync](polling-for-changes-using-the-dirsync-control.md)
-   [Polling delle modifiche tramite USNChanged](polling-for-changes-using-usnchanged.md)

 

 