---
description: L'account LocalService è un account locale predefinito utilizzato da Gestione controllo servizi.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Account LocalService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529868"
---
# <a name="localservice-account"></a>Account LocalService

L'account LocalService è un account locale predefinito utilizzato da Gestione controllo servizi. Dispone dei privilegi minimi nel computer locale e presenta credenziali anonime sulla rete.

Questo account può essere specificato in una chiamata alle funzioni [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Si noti che questo account non dispone di una password, pertanto tutte le informazioni sulla password fornite in questa chiamata verranno ignorate. Mentre il sottosistema di sicurezza localizza il nome dell'account, SCM non supporta i nomi localizzati. Si riceverà pertanto un nome localizzato per questo account dalla funzione [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , ma il nome dell'account deve essere NT Authority \\ LocalService quando si chiama **CreateService** o **ChangeServiceConfig**, indipendentemente dalle impostazioni locali, oppure possono verificarsi risultati imprevisti.

Il SID utente viene creato dal valore **\_ \_ \_ RID servizio locale di sicurezza** .

L'account LocalService ha una propria sottochiave nella chiave del registro di sistema **\_ utenti di HKEY** . La chiave del registro di sistema dell' **\_ \_ utente corrente di HKEY** è quindi associata all'account LocalService.

L'account LocalService presenta i privilegi seguenti:

-   **Se \_ \_Nome ASSIGNPRIMARYTOKEN** (disabilitato)
-   **Se \_ \_Nome controllo** (disabilitato)
-   **Se \_ MODIFICA \_ \_ nome notifica** (abilitato)
-   **Se \_ Crea \_ \_ nome globale** (abilitato)
-   **Se \_ \_Nome rappresentazione** (abilitato)
-   **Se \_ AUMENTA \_ il \_ nome della quota** (disabilitato)
-   **Se \_ \_Nome arresto** (disabilitato)
-   **Se \_ Annulla ancoraggio \_ nome** (disabilitato)
-   Tutti i privilegi assegnati agli utenti e agli utenti autenticati

Per ulteriori informazioni, vedere [sicurezza del servizio e diritti di accesso](service-security-and-access-rights.md).

 

 
