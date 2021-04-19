---
description: L'account NetworkService è un account locale predefinito utilizzato da Gestione controllo servizi.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Account NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316614"
---
# <a name="networkservice-account"></a>Account NetworkService

L'account NetworkService è un account locale predefinito utilizzato da Gestione controllo servizi. Questo account non è riconosciuto dal sottosistema di sicurezza, pertanto non è possibile specificarne il nome in una chiamata alla funzione [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) . Dispone dei privilegi minimi nel computer locale e funge da computer in rete.

Questo account può essere specificato in una chiamata alle funzioni [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Si noti che questo account non dispone di una password, pertanto tutte le informazioni sulla password fornite in questa chiamata verranno ignorate. Mentre il sottosistema di sicurezza localizza il nome dell'account, SCM non supporta i nomi localizzati. Si riceverà pertanto un nome localizzato per questo account dalla funzione [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , ma il nome dell'account deve essere NT Authority \\ NetworkService quando si chiama **CreateService** o **ChangeServiceConfig**, indipendentemente dalle impostazioni locali, oppure possono verificarsi risultati imprevisti.

Un servizio eseguito nel contesto dell'account NetworkService presenta le credenziali del computer ai server remoti. Per impostazione predefinita, il token remoto contiene i SID per i gruppi Everyone e Authenticated Users. Il SID utente viene creato dal valore **\_ \_ \_ RID servizio di rete di sicurezza** .

L'account NetworkService ha una propria sottochiave sotto la chiave del registro di sistema **HKEY \_ Users** . La chiave del registro di sistema dell' **\_ \_ utente corrente di HKEY** è quindi associata all'account NetworkService.

L'account NetworkService dispone dei privilegi seguenti:

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

 

 
