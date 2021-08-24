---
description: Per evitare attacchi dannosi, determinare se l'applicazione richiede privilegi di amministratore. Per le funzioni che richiedono autorizzazioni di amministratore, creare un'applicazione separata e usare il Windows comando della riga di comando RunAs.
ms.assetid: afa520fc-c206-49de-8d73-8f6566ec4fb6
title: Esecuzione con privilegi di amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87533e71fbce613ff01ec2cf4670f1632d46786eb2a5b77900f950357a9eaa8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622721"
---
# <a name="running-with-administrator-privileges"></a>Esecuzione con privilegi di amministratore

Il primo passaggio per stabilire il tipo di account con cui deve essere eseguita l'applicazione consiste nell'esaminare le risorse che verranno usate dall'applicazione e le API con privilegi che chiamerà. È possibile che l'applicazione, o grandi parti di essa, non richieda privilegi di amministratore. *Scrittura di codice sicuro*, di Michael Howard e David LeBlanc offre un'ottima descrizione di come eseguire questa valutazione ed è altamente consigliata. Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.

È possibile fornire i privilegi necessari all'applicazione con una minore esposizione ad attacchi dannosi usando uno degli approcci seguenti:

-   Eseguire con un account con meno privilegi. Un modo per eseguire questa operazione è usare [**PrivilegeCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck) per determinare quali privilegi sono abilitati in un token. Se i privilegi disponibili non sono adeguati per l'operazione corrente, è possibile disabilitare il codice e chiedere all'utente di accedere a un account con privilegi di amministratore.
-   Suddividere in funzioni dell'applicazione separate che richiedono autorizzazioni di amministratore. È possibile fornire all'utente un collegamento che esegue il comando RunAs. Per istruzioni dettagliate su come configurare il collegamento, cercare "runas" nella Guida. A livello di codice, è possibile configurare il [comando RunAs](/windows/desktop/com/runas) nella chiave del Registro di sistema [AppId Key](/windows/desktop/com/appid-key) per l'applicazione.
-   Autenticare l'utente chiamando [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) (GUI) o [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa) (riga di comando) per ottenere il nome utente e la password. Per un esempio, vedere [Richiesta di credenziali all'utente.](asking-the-user-for-credentials.md)
-   Rappresentare l'utente. Un processo avviato con un account con privilegi elevati come System può rappresentare un account utente chiamando [**ImpersonateLoggedOnUser**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) o funzioni impersonate simili, riducendo così il livello di privilegio. Tuttavia, se una chiamata a [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) viene inserita nel thread, il processo torna ai privilegi di sistema originali.

Se si è determinato che l'applicazione deve essere eseguita con un account con privilegi di amministratore e che è necessario archiviare una password amministratore nel sistema software, vedere [Gestione](handling-passwords.md) delle password per i metodi per eseguire questa operazione in modo sicuro.

 

 
