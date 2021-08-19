---
title: Informazioni sugli account di accesso al servizio
description: Quando un servizio basato su Win32 viene avviato, accede al computer locale.
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ba72ffca4362f42c6a5ad6ee494e36e9698d7883c19e3fe2a157e153ce556b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841021"
---
# <a name="about-service-logon-accounts"></a>Informazioni sugli account di accesso al servizio

Quando un servizio basato su Win32 viene avviato, accede al computer locale. Può accedere come:

-   Un account utente locale o di dominio.
-   Account LocalSystem.

L'account di accesso determina l'identità di sicurezza del servizio in fase di esecuzione, ad esempio il contesto di sicurezza primario del servizio. Il contesto di sicurezza determina la capacità del servizio di accedere alle risorse locali e di rete. Ad esempio, un servizio in esecuzione nel contesto di sicurezza di un account utente locale non può accedere alle risorse di rete. Al contrario, un servizio in esecuzione nel contesto di sicurezza dell'account LocalSystem in un controller di dominio Windows 2000 avrebbe accesso senza restrizioni al controller di dominio. Per altre informazioni e una descrizione dei vantaggi e delle limitazioni tra gli account utente e LocalSystem, vedere Contesti di sicurezza [e](security-contexts-and-active-directory-domain-services.md)Active Directory Domain Services .

In definitiva, gli amministratori del sistema in cui è installato il servizio hanno il controllo sull'account di accesso del servizio. Per motivi di sicurezza, alcuni amministratori potrebbero non consentire l'installazione del servizio con l'account LocalSystem. Il servizio deve essere in grado di essere eseguito con un account utente di dominio. I programmatori possono esercitare un certo controllo sull'account di accesso del servizio. Il programma di installazione del servizio specifica l'account di accesso del servizio quando chiama la [**funzione CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) per installare il servizio in un computer host. Il programma di installazione può suggerire un account di accesso predefinito, ma deve consentire a un amministratore di specificare l'account effettivo.

Il programma di installazione può anche eseguire le attività seguenti relative all'account di accesso del servizio:

-   Installazione. Se si installa il servizio per l'esecuzione con un account utente, l'account deve esistere prima di chiamare [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea). È possibile usare un account esistente o crearne uno come parte dell'installazione del computer host. Per altre informazioni, vedere [Configurazione dell'account utente di un servizio.](setting-up-a-serviceampaposs-user-account.md)
-   Autenticazione. Se si vuole che i client usino l'autenticazione reciproca Kerberos, registrare i nomi SPN nell'account di accesso del servizio. Se il servizio viene eseguito con l'account LocalSystem, l'account di accesso del servizio è l'account computer del computer host. Per altre informazioni vedere [Service Principal Names](service-principal-names.md) (Nomi di entità servizio).
-   Concedere l'accesso. Assicurarsi che il servizio in fase di esecuzione abbia i diritti di accesso e i privilegi necessari per eseguire le attività. Ciò può richiedere l'impostazione di voci di controllo di accesso (ACE) nei descrittori di sicurezza di varie risorse, ovvero oggetti directory, condivisioni file e così via, per consentire i diritti di accesso necessari all'account utente o computer. Per altre informazioni, vedere [Concessione dei diritti di accesso all'account di accesso al servizio](granting-access-rights-to-the-service-logon-account.md).
-   Impostare Privilegi. Assegnare privilegi all'account di accesso specificato, ad esempio il diritto di accesso come servizio al computer host. Per altre informazioni, vedere [Concessione del diritto Accesso come servizio nel computer host.](granting-logon-as-service-right-on-the-host-computer.md)

Dopo l'installazione di un servizio, sono presenti attività di manutenzione correlate all'account di accesso del servizio. Per altre informazioni, vedere [Attività di manutenzione dell'account di accesso](logon-account-maintenance-tasks.md).

-   Manutenzione delle password. Per un servizio eseguito con un account utente, è necessario modificare periodicamente la password e mantenere la password sincronizzata con la password usata da uno o più responsabili del controllo del servizio locale per avviare il servizio.
-   Manutenzione del nome SPN. Se un account di accesso al servizio cambia, rimuovere i nomi SPN registrati nell'account precedente e registrarli nel nuovo account. Tenere presente che quando viene installato un servizio, un amministratore di dominio può modificare l'account con cui viene eseguito il servizio. usare le funzioni Win32 o l'interfaccia utente dello strumento amministrativo Gestione computer.
-   Manutenzione ACE. Se un account di accesso al servizio cambia, è necessario aggiornare le voci di controllo di accesso e le appartenenze ai gruppi per assicurarsi che il servizio possa comunque accedere alle risorse necessarie.

 

 