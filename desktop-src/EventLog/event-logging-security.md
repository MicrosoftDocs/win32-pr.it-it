---
description: Il registro di sicurezza è progettato per essere utilizzato dal sistema. Tuttavia, gli utenti possono leggere e cancellare il registro di sicurezza se sono stati concessi \_ i \_ privilegi per il nome di sicurezza se (il &\# 0034, gestire il registro di controllo e di protezione&\# 0034; diritto utente). Per ulteriori informazioni, vedere privilegi.
ms.assetid: 861be39a-012e-473b-a2d3-2a8c7ba3adaa
title: Sicurezza registrazione eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4e2dce7318efeb6f26917bca1d6812eb32a343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310817"
---
# <a name="event-logging-security"></a>Sicurezza registrazione eventi

Il registro di **sicurezza** è progettato per essere utilizzato dal sistema. Tuttavia, gli utenti possono leggere e cancellare il registro di **sicurezza** se sono stati concessi i \_ privilegi per il nome di sicurezza se \_ ("Gestione registro di controllo e di protezione"). Per ulteriori informazioni, vedere [privilegi](/windows/desktop/SecAuthZ/privileges).

Solo l'autorità di sicurezza locale (Lsass.exe) dispone dell'autorizzazione di scrittura per il registro di **sicurezza** . Nessun altro account può richiedere questo privilegio. Per scrivere un evento nel registro di **sicurezza** , usare la funzione [**AuthzReportSecurityEvent**](/windows/desktop/api/authz/nf-authz-authzreportsecurityevent) .

L'accesso al registro **applicazioni** , al registro di **sistema** e ai log personalizzati è limitato. Il sistema concede l'accesso in base ai diritti di accesso concessi all'account con cui viene eseguito il thread. La tabella seguente illustra i tipi di accesso richiesti dalle funzioni di registrazione eventi.



| Diritto di accesso                 | Descrizione                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| \_Registro Elf \_ Clear (0x0004) | Obbligatorio per [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga).                                                    |
| \_Lettura file di log Elf \_ (0x0001)  | Richiesto da [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) e [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga). |
| \_Scrittura file di log Elf \_ (0x0002) | Obbligatorio per [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea).                                        |



 

Usare il valore del registro di sistema **CustomSD** per configurare la sicurezza del registro **applicazioni** , il registro di **sistema** e i log personalizzati. Per altre informazioni, vedere [EventLog Key](eventlog-key.md).

**Windows XP/2000:** La tabella seguente descrive i diritti di accesso concessi per ogni account in ogni log.

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



 

Per concedere l'accesso ai membri dell'account Guest, modificare il valore del registro di sistema seguente:

**HKEY \_ Registro eventi di sistema del \_ computer locale** \\  \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **RestrictGuestAccess**

 

 
