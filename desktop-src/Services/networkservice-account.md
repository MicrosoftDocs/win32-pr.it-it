---
description: L'account NetworkService è un account locale predefinito usato da Gestione controllo servizi.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: NetworkService Account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f8256a15b43d9a9c0403067a61f9a7cbf6b9d2df0d78936c4d9c06f6dfd87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889395"
---
# <a name="networkservice-account"></a>NetworkService Account

L'account NetworkService è un account locale predefinito usato da Gestione controllo servizi. Questo account non è riconosciuto dal sottosistema di sicurezza, pertanto non è possibile specificarne il nome in una chiamata alla [**funzione LookupAccountName.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) Ha privilegi minimi sul computer locale e funge da computer in rete.

Questo account può essere specificato in una chiamata alle [**funzioni CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) Si noti che questo account non dispone di una password, pertanto le informazioni sulla password fornite in questa chiamata vengono ignorate. Anche se il sottosistema di sicurezza localizza questo nome di account, Gestione controllo servizi non supporta i nomi localizzati. Si riceverà quindi un nome localizzato per questo account dalla funzione [**LookupAccountSid,**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) ma il nome dell'account deve essere NT AUTHORITY NetworkService quando si chiama \\ **CreateService** o **ChangeServiceConfig**, indipendentemente dalle impostazioni locali o possono verificarsi risultati imprevisti.

Un servizio eseguito nel contesto dell'account NetworkService presenta le credenziali del computer ai server remoti. Per impostazione predefinita, il token remoto contiene SID per i gruppi Everyone e Authenticated Users. Il SID utente viene creato dal **valore SECURITY NETWORK SERVICE \_ \_ \_ RID.**

L'account NetworkService ha una propria sottochiave nella chiave del Registro di sistema **HKEY \_ USERS.** Pertanto, la **chiave del Registro di sistema HKEY CURRENT \_ \_ USER** è associata all'account NetworkService.

L'account NetworkService ha i privilegi seguenti:

-   **edizione Standard \_ ASSIGNPRIMARYTOKEN \_ NAME** (disabilitato)
-   **edizione Standard \_ AUDIT \_ NAME** (disabilitato)
-   **edizione Standard \_ CHANGE \_ NOTIFY \_ NAME** (abilitato)
-   **edizione Standard \_ CREATE \_ GLOBAL \_ NAME** (abilitato)
-   **edizione Standard \_ NOME \_ IMPERSONATE** (abilitato)
-   **edizione Standard \_ INCREASE \_ QUOTA \_ NAME** (disabled)
-   **edizione Standard \_ SHUTDOWN \_ NAME** (disabilitato)
-   **edizione Standard \_ UNDOCK \_ NAME** (disabilitato)
-   Tutti i privilegi assegnati agli utenti e agli utenti autenticati

Per altre informazioni, vedere [Sicurezza dei servizi e diritti di accesso.](service-security-and-access-rights.md)

 

 
