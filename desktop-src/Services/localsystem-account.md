---
description: L'account LocalSystem è un account locale predefinito utilizzato da Gestione controllo servizi.
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: Account LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0132e70044aec7886ce6875239a6bedb502fec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966570"
---
# <a name="localsystem-account"></a>Account LocalSystem

L'account LocalSystem è un account locale predefinito utilizzato da Gestione controllo servizi. Questo account non è riconosciuto dal sottosistema di sicurezza, pertanto non è possibile specificarne il nome in una chiamata alla funzione [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) . Dispone di privilegi estesi sul computer locale e funge da computer in rete. Il token include il \\ sistema di autorità NT e i \\ SID degli amministratori predefiniti. questi account hanno accesso alla maggior parte degli oggetti di sistema. Il nome dell'account in tutte le impostazioni locali è. \\ LocalSystem. È anche possibile usare il nome LocalSystem o *nomecomputer* \\ LocalSystem. Questo account non dispone di una password. Se si specifica l'account LocalSystem in una chiamata alla funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) , tutte le informazioni sulla password fornite verranno ignorate.

Un servizio che viene eseguito nel contesto dell'account LocalSystem eredita il contesto di sicurezza di SCM. Il SID utente viene creato dal valore **\_ RID del \_ sistema \_ locale di sicurezza** . L'account non è associato ad alcun account utente connesso. Questo ha diverse implicazioni:

-   La chiave del registro di sistema **HKEY \_ \_ utente corrente** è associata all'utente predefinito, non all'utente corrente. Per accedere al profilo di un altro utente, rappresentare l'utente, quindi accedere **all' \_ \_ utente corrente di HKEY**.
-   Il servizio può aprire la chiave del registro di sistema **HKEY \_ Local \_ Machine \\ Security**.
-   Il servizio presenta le credenziali del computer ai server remoti.
-   Se il servizio apre una finestra di comando ed esegue un file batch, l'utente può premere CTRL + C per terminare il file batch e ottenere l'accesso a una finestra di comando con le autorizzazioni LocalSystem.

L'account LocalSystem presenta i privilegi seguenti:

-   **Se \_ \_Nome ASSIGNPRIMARYTOKEN** (disabilitato)
-   **Se \_ \_Nome controllo** (abilitato)
-   **Se \_ \_Nome backup** (disabilitato)
-   **Se \_ MODIFICA \_ \_ nome notifica** (abilitato)
-   **Se \_ Crea \_ \_ nome globale** (abilitato)
-   **Se \_ Crea \_ \_ nome del file di paging** (abilitato)
-   **Se \_ Crea \_ \_ nome permanente** (abilitato)
-   **Se \_ Crea \_ \_ nome token** (disabilitato)
-   **Se \_ \_Nome debug** (abilitato)
-   **Se \_ \_Nome rappresentazione** (abilitato)
-   **Se \_ \_Nome della \_ priorità \_ di base di Inc** (abilitato)
-   **Se \_ AUMENTA \_ il \_ nome della quota** (disabilitato)
-   **Se \_ CARICA \_ \_ nome driver** (disabilitato)
-   **Se \_ BLOCCA \_ \_ nome memoria** (abilitato)
-   **Se \_ GESTISCi \_ \_ nome volume** (disabilitato)
-   **Se \_ \_Nome singolo \_ processo \_ prof** (abilitato)
-   **Se \_ \_Nome ripristino** (disabilitato)
-   **Se \_ \_Nome sicurezza** (disabilitato)
-   **Se \_ \_Nome arresto** (disabilitato)
-   **Se \_ \_ \_ Nome dell'ambiente di sistema** (disabilitato)
-   **Se \_ \_Nome SYSTEMTIME** (disabilitato)
-   **Se \_ ASSUMERE \_ il \_ nome della proprietà** (disabilitato)
-   **Se \_ \_Nome TCB** (abilitato)
-   **Se \_ Annulla ancoraggio \_ nome** (disabilitato)

Per la maggior parte dei servizi non è necessario un livello di privilegio elevato. Se il servizio non necessita di questi privilegi e non è un servizio interattivo, è consigliabile usare l' [account LocalService](localservice-account.md) o l' [account NetworkService](networkservice-account.md). Per ulteriori informazioni, vedere [sicurezza del servizio e diritti di accesso](service-security-and-access-rights.md).

 

 
