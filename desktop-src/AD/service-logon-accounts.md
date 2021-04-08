---
title: Account di accesso al servizio
description: Un servizio, come qualsiasi processo, ha un'identità di sicurezza primaria che determina i diritti di accesso e i privilegi concessi per le risorse locali e di rete.
ms.assetid: c2345967-8415-4cc0-96d3-12c48e74028e
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, accesso al servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340fe7eebc95ec4c7ea3091c96a2539cb08dee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855382"
---
# <a name="service-logon-accounts"></a>Account di accesso al servizio

Un servizio, come qualsiasi processo, ha un'identità di sicurezza primaria che determina i diritti di accesso e i privilegi concessi per le risorse locali e di rete. Questa identità di sicurezza, o contesto di sicurezza, determina anche il potenziale del servizio per danneggiare le risorse locali e di rete.

Il contesto di sicurezza per un servizio Microsoft Win32 è determinato dall'account di accesso utilizzato per avviare il servizio. In questa sezione vengono illustrati i problemi di programmazione e le procedure consigliate relative all'account di accesso al servizio utilizzato dai servizi Win32, con particolare attenzione ai servizi abilitati per la directory. Questa sezione include gli argomenti seguenti:

-   [Informazioni sugli account di accesso](about-service-logon-accounts.md)al servizio: Panoramica degli account di accesso al servizio e problemi di programmazione del contesto di sicurezza per un servizio Win32.
-   [Linee guida per la selezione di un account di accesso al servizio](guidelines-for-selecting-a-service-logon-account.md) per un servizio Win32.
-   [Configurazione dell'account utente di un servizio](setting-up-a-serviceampaposs-user-account.md).
-   [Installare un servizio in un computer host](installing-a-service-on-a-host-computer.md) e specificare l'account di accesso al servizio.
-   [Concessione dell'accesso come servizio direttamente nel computer host](granting-logon-as-service-right-on-the-host-computer.md), concedendo all'account utente del servizio il diritto di accesso come servizio nel computer host.
-   [Verifica dell'esecuzione in un controller di dominio](testing-whether-running-on-a-domain-controller.md): rilevamento in fase di installazione se l'istanza del servizio viene installata in un controller di dominio.
-   [Concessione dei diritti di accesso all'account di accesso al servizio](granting-access-rights-to-the-service-logon-account.md): impostazione e gestione di Ace e appartenenze a gruppi per garantire che il sistema consentirà all'esecuzione del servizio di accedere alle risorse locali e di rete necessarie.
-   [Modifica della password nell'account utente di un servizio](changing-the-password-on-a-serviceampaposs-user-account.md): modifica della password dell'account utente di un servizio e aggiornamento della password registrata con Gestione controllo servizi in ogni server host in cui è installato il servizio.
-   [Autenticazione reciproca tramite Kerberos](mutual-authentication-using-kerberos.md): gestione della registrazione del nome dell'entità servizio (SPN) nell'oggetto directory associato all'account di accesso di ogni istanza del servizio. I nomi SPN consentono ai client di autenticare un servizio usando l'autenticazione reciproca Kerberos.
-   [Conversione dei formati dei nomi di account di dominio](converting-domain-account-name-formats.md), ad esempio la conversione di un nome distinto in formato *dominio ***\\*** nomeutente* e viceversa.

 

 




