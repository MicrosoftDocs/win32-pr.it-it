---
description: L'account LocalSystem è un account locale predefinito usato da Gestione controllo servizi.
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: LocalSystem Account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d4dca5655402b3b4f400d3c1941ccf3978a7d385363567fac01a1d3024f1dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889442"
---
# <a name="localsystem-account"></a>LocalSystem Account

L'account LocalSystem è un account locale predefinito usato da Gestione controllo servizi. Questo account non è riconosciuto dal sottosistema di sicurezza, pertanto non è possibile specificarne il nome in una chiamata alla [**funzione LookupAccountName.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) Dispone di privilegi estesi nel computer locale e funge da computer in rete. Il token include i SID NT AUTHORITY \\ SYSTEM e BUILTIN Administrators. Questi account hanno accesso alla maggior parte degli oggetti di \\ sistema. Il nome dell'account in tutte le impostazioni locali è . \\ Localsystem. È anche possibile usare il nome LocalSystem o *ComputerName* \\ LocalSystem. Questo account non dispone di una password. Se si specifica l'account LocalSystem in una chiamata alla [**funzione CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig,**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) le informazioni sulla password specificate vengono ignorate.

Un servizio eseguito nel contesto dell'account LocalSystem eredita il contesto di sicurezza di Gestione controllo servizi. Il SID utente viene creato dal **valore SECURITY LOCAL SYSTEM \_ \_ \_ RID.** L'account non è associato ad alcun account utente connesso. Questo ha diverse implicazioni:

-   La chiave del Registro **di sistema HKEY \_ CURRENT \_ USER** è associata all'utente predefinito, non all'utente corrente. Per accedere al profilo di un altro utente, rappresentare l'utente, quindi **accedere a HKEY \_ CURRENT \_ USER**.
-   Il servizio può aprire la chiave del Registro di **sistema HKEY \_ LOCAL MACHINE \_ \\ SECURITY**.
-   Il servizio presenta le credenziali del computer ai server remoti.
-   Se il servizio apre una finestra di comando ed esegue un file batch, l'utente potrebbe premere CTRL+C per terminare il file batch e ottenere l'accesso a una finestra di comando con autorizzazioni LocalSystem.

L'account LocalSystem dispone dei privilegi seguenti:

-   **edizione Standard \_ ASSIGNPRIMARYTOKEN \_ NAME** (disabilitato)
-   **edizione Standard \_ AUDIT \_ NAME** (abilitato)
-   **edizione Standard \_ BACKUP \_ NAME** (disabilitato)
-   **edizione Standard \_ CHANGE \_ NOTIFY \_ NAME** (abilitato)
-   **edizione Standard \_ CREATE \_ GLOBAL \_ NAME** (abilitato)
-   **edizione Standard \_ CREATE \_ PAGEFILE \_ NAME** (enabled)
-   **edizione Standard \_ CREATE \_ PERMANENT \_ NAME** (abilitato)
-   **edizione Standard \_ CREATE \_ TOKEN \_ NAME** (disabilitato)
-   **edizione Standard \_ DEBUG \_ NAME** (abilitato)
-   **edizione Standard \_ NOME \_ IMPERSONATE** (abilitato)
-   **edizione Standard \_ INC \_ BASE \_ PRIORITY \_ NAME** (enabled)
-   **edizione Standard \_ INCREASE \_ QUOTA \_ NAME** (disabled)
-   **edizione Standard \_ LOAD \_ DRIVER \_ NAME** (disabled)
-   **edizione Standard \_ LOCK \_ MEMORY \_ NAME** (abilitato)
-   **edizione Standard \_ GESTISCI \_ NOME \_ VOLUME** (disabilitato)
-   **edizione Standard \_ NOME \_ PROCESSO \_ SINGOLO \_ PROF** (abilitato)
-   **edizione Standard \_ RESTORE \_ NAME** (disabilitato)
-   **edizione Standard \_ NOME \_ SICUREZZA** (disabilitato)
-   **edizione Standard \_ SHUTDOWN \_ NAME** (disabilitato)
-   **edizione Standard \_ NOME \_ AMBIENTE \_ SISTEMA** (disabilitato)
-   **edizione Standard \_ SYSTEMTIME \_ NAME** (disabilitato)
-   **edizione Standard \_ TAKE \_ OWNERSHIP \_ NAME** (DISABILITATO)
-   **edizione Standard \_ TCB \_ NAME** (abilitato)
-   **edizione Standard \_ UNDOCK \_ NAME** (disabilitato)

Per la maggior parte dei servizi non è necessario un livello di privilegio così elevato. Se il servizio non richiede questi privilegi e non è un servizio interattivo, è consigliabile usare [l'account LocalService](localservice-account.md) o [l'account NetworkService](networkservice-account.md). Per altre informazioni, vedere [Sicurezza dei servizi e diritti di accesso.](service-security-and-access-rights.md)

 

 
