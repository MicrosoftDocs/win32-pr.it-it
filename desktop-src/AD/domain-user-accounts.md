---
title: Uso di un account utente di dominio come account di accesso al servizio
description: Un account utente di dominio consente al servizio di sfruttare al meglio le funzionalità di sicurezza del servizio di Windows e Microsoft Active Directory Domain Services.
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: f482359eb8445cacef12c46716ecde662a95d46d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323820"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>Uso di un account utente di dominio come account di accesso al servizio

Un account utente di dominio consente al servizio di sfruttare al meglio le funzionalità di sicurezza del servizio di Windows e Microsoft Active Directory Domain Services. Il servizio ha tutti gli accessi locali e di rete concessi all'account o a tutti i gruppi di cui l'account è membro. Il servizio può supportare l'autenticazione reciproca Kerberos.

> [!Note]  
> La documentazione seguente è destinata agli sviluppatori. Se si è un utente finale che cerca informazioni su un messaggio di errore che interessa gli account utente di dominio, vedere i [Forum della community Microsoft](https://answers.microsoft.com). Per informazioni sulla gestione degli account utente di dominio, vedere [TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11)).

Il vantaggio dell'utilizzo di un account utente di dominio è che le azioni del servizio sono limitate dai diritti di accesso e dai privilegi associati all'account. A differenza di un `LocalSystem` servizio, i bug in un servizio account utente non possono danneggiare il sistema. Se il servizio viene compromesso da un attacco alla sicurezza, il danno viene isolato in base alle operazioni che il sistema consente all'account utente di eseguire. Allo stesso tempo, i client in esecuzione con diversi livelli di privilegio possono connettersi al servizio, consentendo al servizio di rappresentare un client per eseguire operazioni sensibili.

L'account utente di un servizio non deve essere un membro di tutti i gruppi di amministratori locali, di dominio o aziendali. Se il servizio richiede privilegi amministrativi locali, eseguirlo con l' `LocalSystem` account. Per le operazioni che richiedono privilegi amministrativi di dominio, eseguirle rappresentando il contesto di sicurezza di un'applicazione client.

Un'istanza del servizio che usa un account utente di dominio richiede un'azione amministrativa periodica per gestire la password dell'account. Gestione controllo servizi (SCM) nel computer host di un'istanza del servizio memorizza nella cache la password dell'account da utilizzare per la registrazione nel servizio. Quando si modifica la password dell'account, è necessario aggiornare anche la password memorizzata nella cache nel computer host in cui è installato il servizio. Per ulteriori informazioni e un esempio di codice, vedere [la pagina relativa alla modifica della password nell'account utente di un servizio](changing-the-password-on-a-serviceampaposs-user-account.md). È possibile evitare la manutenzione regolare lasciando invariata la password, ma ciò aumenta la probabilità di un attacco con password per l'account del servizio. Tenere presente che anche se SCM archivia la password in una parte sicura del registro di sistema, è comunque soggetta ad attacchi.

Un account utente di dominio dispone di due formati di nome: il nome distinto dell'oggetto utente nella directory e il <domain> \\ <username> formato "" utilizzato da Gestione controllo servizi locale. Per ulteriori informazioni e un esempio di codice che converte da un formato all'altro, vedere [conversione dei formati di nome dell'account di dominio](converting-domain-account-name-formats.md).

 

 
