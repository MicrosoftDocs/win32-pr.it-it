---
description: Il registro di sicurezza è progettato per l'uso da parte del sistema. Tuttavia, gli utenti possono leggere e cancellare il registro di sicurezza se è stato concesso il privilegio edizione Standard \_ SECURITY NAME (il &0034; gestire il controllo e il registro di sicurezza \_ \#&\# 0034; diritto utente). Per altre informazioni, vedere Privilegi.
ms.assetid: 861be39a-012e-473b-a2d3-2a8c7ba3adaa
title: Sicurezza della registrazione eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52f6c801b061290ebb4d6f47fe78efebc09e1b2d23dc4a598dc9f97c1b3a46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151551"
---
# <a name="event-logging-security"></a>Sicurezza della registrazione eventi

Il **registro** di sicurezza è progettato per l'uso da parte del sistema. Tuttavia, gli utenti possono leggere e cancellare il **registro** di sicurezza se gli è stato concesso il privilegio edizione Standard SECURITY NAME (diritto utente "gestione del log di controllo e \_ di \_ sicurezza"). Per altre informazioni, vedere [Privilegi](/windows/desktop/SecAuthZ/privileges).

Solo l'autorità di sicurezza locale (Lsass.exe) dispone dell'autorizzazione di scrittura per il **registro di** sicurezza. Nessun altro account può richiedere questo privilegio. Per scrivere un evento nel log **di** sicurezza, usare la [**funzione AuthzReportSecurityEvent.**](/windows/desktop/api/authz/nf-authz-authzreportsecurityevent)

L'accesso **al** registro applicazioni, al log **di** sistema e ai log personalizzati è limitato. Il sistema concede l'accesso in base ai diritti di accesso concessi all'account con cui è in esecuzione il thread. La tabella seguente illustra i tipi di accesso richiesti dalle funzioni di registrazione eventi.



| Diritto di accesso                 | Descrizione                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| ELF \_ LOGFILE \_ CLEAR (0x0004) | Richiesto da [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga).                                                    |
| ELF \_ LOGFILE \_ READ (0x0001)  | Obbligatorio [**per OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) e [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga). |
| ELF \_ LOGFILE \_ WRITE (0x0002) | Richiesto da [**RegisterEventSource.**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)                                        |



 

Usare il valore del Registro di sistema **CustomSD** per configurare la sicurezza del **registro** applicazioni, del log **di** sistema e dei log personalizzati. Per altre informazioni, vedere [Eventlog Key](eventlog-key.md).

**Windows XP/2000:** Nella tabella seguente vengono descritti i diritti di accesso concessi per ogni account in ogni log.

| Log             | Account                 | Lettura | Scrittura | Cancella |
|-----------------|-------------------------|------|-------|-------|
| **Applicazione** | Amministratori (sistema) | X    | X     | X     |
|                 | Amministratori (dominio) | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Utente interattivo        | X    | X     |       |
| **Sistema**      | Amministratori (sistema) | X    | X     | X     |
|                 | Amministratori (dominio) | X    |       | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Utente interattivo        | X    |       |       |
| *Impostazione personalizzata*        | Amministratori (sistema) | X    | X     | X     |
|                 | Amministratori (dominio) | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Utente interattivo        | X    | X     |       |



 

Per concedere l'accesso ai membri dell'account Guest, modificare il valore del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **EventLog** \\ *Log* \\ **RestrictGuestAccess**

 

 
