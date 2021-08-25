---
description: L'account LocalService è un account locale predefinito usato da Gestione controllo servizi.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: LocalService Account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89878f39f78c384398a5971c7c9f290288fbf3fa87f2c8e55677309e27a6fa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967982"
---
# <a name="localservice-account"></a>LocalService Account

L'account LocalService è un account locale predefinito usato da Gestione controllo servizi. Ha privilegi minimi nel computer locale e presenta credenziali anonime nella rete.

Questo account può essere specificato in una chiamata alle [**funzioni CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) Si noti che questo account non ha una password, quindi le informazioni sulla password fornite in questa chiamata vengono ignorate. Anche se il sottosistema di sicurezza localizza il nome dell'account, Gestione controllo servizi non supporta i nomi localizzati. Si riceverà quindi un nome localizzato per questo account dalla funzione [**LookupAccountSid,**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) ma il nome dell'account deve essere NT AUTHORITY LocalService quando si chiama \\ **CreateService** o **ChangeServiceConfig**, indipendentemente dalle impostazioni locali o possono verificarsi risultati imprevisti.

Il SID utente viene creato dal **valore SECURITY LOCAL SERVICE \_ \_ \_ RID.**

L'account LocalService ha una propria sottochiave nella chiave del Registro **di sistema HKEY \_ USERS.** Di conseguenza, la chiave del Registro di sistema **\_ HKEY CURRENT \_ USER** è associata all'account LocalService.

L'account LocalService ha i privilegi seguenti:

-   **edizione Standard \_ ASSIGNPRIMARYTOKEN \_ NAME** (disabilitato)
-   **edizione Standard \_ AUDIT \_ NAME** (disabilitato)
-   **edizione Standard \_ CHANGE \_ NOTIFY \_ NAME** (abilitato)
-   **edizione Standard \_ CREATE \_ GLOBAL \_ NAME** (abilitato)
-   **edizione Standard \_ IMPERSONATE \_ NAME** (abilitato)
-   **edizione Standard \_ INCREASE \_ QUOTA \_ NAME** (disabilitato)
-   **edizione Standard \_ SHUTDOWN \_ NAME** (disabilitato)
-   **edizione Standard \_ ANNULLA IL \_ NOME** (disabilitato)
-   Tutti i privilegi assegnati a utenti e utenti autenticati

Per altre informazioni, vedere Sicurezza [del servizio e diritti di accesso.](service-security-and-access-rights.md)

 

 
