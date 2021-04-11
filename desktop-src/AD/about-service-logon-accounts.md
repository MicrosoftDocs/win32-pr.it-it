---
title: Informazioni sugli account di accesso al servizio
description: Quando un servizio basato su Win32 viene avviato, accede al computer locale.
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328b33d5dab36ccc5a803eb7c43ca3112e96ecf8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117514"
---
# <a name="about-service-logon-accounts"></a>Informazioni sugli account di accesso al servizio

Quando un servizio basato su Win32 viene avviato, accede al computer locale. Può accedere come:

-   Un account utente locale o di dominio.
-   Account LocalSystem.

L'account di accesso determina l'identità di sicurezza del servizio in fase di esecuzione, ovvero il contesto di sicurezza primario del servizio. Il contesto di sicurezza determina la capacità del servizio di accedere alle risorse locali e di rete. Ad esempio, un servizio in esecuzione nel contesto di sicurezza di un account utente locale non può accedere alle risorse di rete. Viceversa, un servizio in esecuzione nel contesto di sicurezza dell'account LocalSystem in un controller di dominio di Windows 2000 (DC) avrebbe accesso illimitato al controller di dominio. Per ulteriori informazioni e per una descrizione dei vantaggi e delle limitazioni tra gli account utente e LocalSystem, vedere [contesti di sicurezza e Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).

Infine, gli amministratori del sistema in cui è installato il servizio hanno il controllo dell'account di accesso del servizio. Per motivi di sicurezza, alcuni amministratori potrebbero non consentire l'installazione del servizio con l'account LocalSystem. Il servizio deve essere in grado di essere eseguito con un account utente di dominio. Il programmatore può esercitare un certo controllo sull'account di accesso del servizio. Il programma di installazione del servizio specifica l'account di accesso del servizio quando chiama la funzione [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) per installare il servizio in un computer host. Il programma di installazione può suggerire un account di accesso predefinito, ma deve consentire a un amministratore di specificare l'account effettivo.

Il programma di installazione può inoltre eseguire le attività seguenti relative all'account di accesso del servizio:

-   Installazione. Se si installa il servizio per l'esecuzione con un account utente, l'account deve esistere prima di chiamare [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea). È possibile usare un account esistente o crearne uno come parte del computer host installrt. Per ulteriori informazioni, vedere [configurazione di un account utente di un servizio](setting-up-a-serviceampaposs-user-account.md).
-   Autenticazione. Se si desidera che i client usino l'autenticazione reciproca Kerberos, registrare i nomi SPN nell'account di accesso del servizio. Se il servizio viene eseguito con l'account LocalSystem, l'account di accesso del servizio è l'account computer del computer host. Per altre informazioni vedere [Service Principal Names](service-principal-names.md) (Nomi di entità servizio).
-   Concessione dell'accesso. Verificare che il servizio in fase di esecuzione disponga dei diritti di accesso e dei privilegi necessari per eseguire le attività. Questa operazione può richiedere l'impostazione di voci di controllo di accesso (ACE) nei descrittori di sicurezza di varie risorse, ovvero oggetti directory, condivisioni file e così via, per consentire i diritti di accesso necessari per l'account utente o computer. Per ulteriori informazioni, vedere [concessione di diritti di accesso all'account di accesso al servizio](granting-access-rights-to-the-service-logon-account.md).
-   Impostare i privilegi. Assegnare privilegi all'account di accesso specificato, ad esempio il diritto di accedere come servizio al computer host. Per ulteriori informazioni, vedere [concessione dell'accesso come servizio direttamente nel computer host](granting-logon-as-service-right-on-the-host-computer.md).

Dopo l'installazione di un servizio, sono presenti attività di manutenzione correlate all'account di accesso al servizio. Per altre informazioni, vedere [attività di manutenzione degli account di accesso](logon-account-maintenance-tasks.md).

-   Manutenzione delle password. Per un servizio eseguito con un account utente, è necessario modificare periodicamente la password e mantenuta la password sincronizzata con la password utilizzata da uno o più gestori di controlli del servizio locali per avviare il servizio.
-   Manutenzione del nome SPN. Se viene modificato un account di accesso al servizio, rimuovere i nomi SPN registrati per l'account precedente e registrarli nel nuovo account. Tenere presente che quando viene installato un servizio, un amministratore di dominio può modificare l'account con cui viene eseguito il servizio. utilizzare le funzioni Win32 o l'interfaccia utente dello strumento di amministrazione Gestione computer.
-   Manutenzione ACE. Se un account di accesso al servizio viene modificato, è necessario aggiornare le voci ACE e l'appartenenza a gruppi per assicurarsi che il servizio possa comunque accedere alle risorse necessarie.

 

 