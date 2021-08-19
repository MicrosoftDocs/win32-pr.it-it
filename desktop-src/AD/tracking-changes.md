---
title: Rilevamento delle modifiche
description: Alcune applicazioni devono mantenere la coerenza tra dati specifici archiviati nel servizio directory Active Directory e altri dati.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, rilevamento delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3d8521fbd7b04d2c317246d81e0b9af7bce888bcc8e78b7bc9fcbbdd05b0c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024569"
---
# <a name="tracking-changes"></a>Rilevamento delle modifiche

Alcune applicazioni devono mantenere la coerenza tra dati specifici archiviati nel servizio directory Active Directory e altri dati. Gli altri dati possono essere archiviati nella directory, in una SQL Server tabella, in un file o nel Registro di sistema. Quando i dati archiviati nella directory cambiano, potrebbe essere necessario modificare gli altri dati per rimanere coerenti. Le applicazioni che hanno questo requisito includono:

Questa sezione non tratta i meccanismi usati dalle applicazioni di monitoraggio. Si tratta di applicazioni che monitorano le modifiche della directory non allo scopo di mantenere dati coerenti tra archivi separati, ma come strumento di gestione del sistema. Anche se le applicazioni di monitoraggio possono usare gli stessi meccanismi che supportano le applicazioni di rilevamento delle modifiche, i meccanismi seguenti sono progettati specificamente per il monitoraggio delle applicazioni:

-   Controllo di sicurezza. Modificando la parte sacl (System Access Control List) di un descrittore di sicurezza degli oggetti, è possibile fare in modo che gli accessi all'oggetto in un determinato controller di dominio generino record di controllo nel registro eventi di sicurezza in tale controller di dominio. È possibile controllare le operazioni di lettura, scrittura o entrambe. è possibile controllare l'intero oggetto o attributi specifici. Per altre informazioni, vedere Recupero del [SACL](retrieving-an-objectampaposs-sacl.md) di un oggetto e [Generazione di controlli](/windows/desktop/SecAuthZ/audit-generation).
-   Registrazione eventi Modificando le impostazioni del Registro di sistema in un determinato controller di dominio, è possibile modificare i tipi di eventi registrati nel registro eventi del servizio directory. In particolare, per registrare tutte le modifiche, impostare **il valore 8 Accesso** alla directory nella chiave del Registro di sistema seguente su 4.

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    Per altre informazioni, vedere [Registrazione eventi](/windows/desktop/EventLog/event-logging).

-   Traccia eventi. Windows 2000 ha introdotto un'API Traccia eventi per tracciare e registrare eventi interessanti nel software o nell'hardware. Il Windows sistema operativo e in Active Directory Domain Services, in particolare, supportano l'uso della traccia degli eventi per la pianificazione della capacità e l'analisi dettagliata delle prestazioni. Per altre informazioni, vedere [Traccia eventi](/windows/desktop/ETW/event-tracing-portal) e [Traccia eventi in ADSI.](/windows/desktop/ADSI/adsi-and-etw)

Questa sezione include gli argomenti seguenti:

-   [Panoramica delle Rilevamento modifiche tecniche](overview-of-change-tracking-techniques.md)
-   [Modificare le notifiche in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md)
-   [Polling delle modifiche tramite il controllo DirSync](polling-for-changes-using-the-dirsync-control.md)
-   [Polling delle modifiche tramite USNChanged](polling-for-changes-using-usnchanged.md)

 

 