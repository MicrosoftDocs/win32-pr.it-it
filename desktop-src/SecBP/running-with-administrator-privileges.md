---
description: Per evitare attacchi dannosi, determinare se l'applicazione richiede privilegi di amministratore. Per le funzioni che richiedono autorizzazioni di amministratore, creare un'applicazione separata e utilizzare il comando della riga di comando RunAs di Windows.
ms.assetid: afa520fc-c206-49de-8d73-8f6566ec4fb6
title: Esecuzione con privilegi di amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc28843195e9b5cabadc13aa2317b0bdd8058ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318250"
---
# <a name="running-with-administrator-privileges"></a>Esecuzione con privilegi di amministratore

Il primo passaggio per stabilire il tipo di account con cui deve essere eseguita l'applicazione consiste nell'esaminare le risorse che l'applicazione userà e le API con privilegi che chiamerà. È possibile che l'applicazione, o parti di grandi dimensioni, non richieda privilegi di amministratore. La *scrittura di codice sicuro*, di Michael Howard e David LeBlanc, offre un'ottima descrizione di come eseguire questa valutazione ed è altamente consigliata. Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.

È possibile fornire i privilegi necessari per l'applicazione, con minore esposizione ad attacchi dannosi usando uno degli approcci seguenti:

-   Eseguire con un account con meno privilegi. Un modo per eseguire questa operazione consiste nell'usare [**PrivilegeCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck) per determinare quali privilegi sono abilitati in un token. Se i privilegi disponibili non sono appropriati per l'operazione corrente, è possibile disabilitare tale codice e chiedere all'utente di accedere a un account con privilegi di amministratore.
-   Suddividere in una funzione di applicazione separata che richiede autorizzazioni di amministratore. È possibile fornire all'utente un collegamento che esegue il comando RunAs. Per istruzioni dettagliate su come configurare il collegamento, cercare "RunAs" nella Guida di. A livello di codice, è possibile configurare il comando [RunAs](/windows/desktop/com/runas) sotto la chiave del registro di sistema della [chiave AppID](/windows/desktop/com/appid-key) per l'applicazione.
-   Autenticare l'utente chiamando [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) (GUI) o [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa) (riga di comando) per ottenere il nome utente e la password. Per un esempio, vedere [richiesta di credenziali all'utente](asking-the-user-for-credentials.md).
-   Rappresenta l'utente. Un processo che inizia con un account con privilegi elevati, come System, può rappresentare un account utente chiamando [**ImpersonateLoggedOnUser**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) o funzioni Impersonate simili, riducendo così il livello di privilegio. Tuttavia, se una chiamata a [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) viene inserita nel thread, il processo torna ai privilegi di sistema originali.

Se è stato determinato che l'applicazione deve essere eseguita con un account con privilegi di amministratore e che è necessario archiviare una password di amministratore nel sistema software, vedere [gestione delle password](handling-passwords.md) per i metodi di esecuzione sicura.

 

 
