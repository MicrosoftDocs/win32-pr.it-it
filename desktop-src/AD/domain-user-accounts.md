---
title: Utilizzo di un account utente di dominio come account di accesso al servizio
description: Un account utente di dominio consente al servizio di sfruttare appieno le funzionalità di sicurezza dei servizi di Windows e Microsoft Active Directory Domain Services.
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: c8defc6cc3b35ca88038ca3818b56024dfb18699
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881449"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>Utilizzo di un account utente di dominio come account di accesso al servizio

Un account utente di dominio consente al servizio di sfruttare appieno le funzionalità di sicurezza dei servizi di Windows e Microsoft Active Directory Domain Services. Il servizio dispone di qualsiasi accesso locale e di rete concesso all'account o a tutti i gruppi di cui l'account è membro. Il servizio può supportare l'autenticazione reciproca Kerberos.

> [!Note]  
> La documentazione seguente è per gli sviluppatori. Gli utenti finali che cercano informazioni su un messaggio di errore che interessa gli account utente di dominio possono vedere i [forum della community Microsoft.](https://answers.microsoft.com) Per informazioni sulla gestione degli account utente di dominio, vedere [TechNet.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11))

Il vantaggio dell'uso di un account utente di dominio è che le azioni del servizio sono limitate dai diritti di accesso e dai privilegi associati all'account. A differenza `LocalSystem` di un servizio, i bug in un servizio con account utente non possono danneggiare il sistema. Se il servizio viene compromesso da un attacco alla sicurezza, il danno è isolato dalle operazioni che il sistema consente all'account utente di eseguire. Allo stesso tempo, i client in esecuzione a livelli di privilegi diversi possono connettersi al servizio, che consente al servizio di rappresentare un client per eseguire operazioni sensibili.

L'account utente di un servizio non deve essere membro di gruppi di amministratori locali, di dominio o aziendali. Se il servizio necessita di privilegi amministrativi locali, eseguirlo con `LocalSystem` l'account . Per le operazioni che richiedono privilegi amministrativi di dominio, eseguirle rappresentando il contesto di sicurezza di un'applicazione client.

Un'istanza del servizio che usa un account utente di dominio richiede un'azione amministrativa periodica per mantenere la password dell'account. Gestione controllo servizi nel computer host di un'istanza del servizio memorizza nella cache la password dell'account da utilizzare per la registrazione nel servizio. Quando si modifica la password dell'account, è necessario aggiornare anche la password memorizzata nella cache nel computer host in cui è installato il servizio. Per altre informazioni e un esempio di codice, vedere [Modifica della password nell'account](changing-the-password-on-a-serviceampaposs-user-account.md)utente di un servizio. È possibile evitare la manutenzione regolare lasciando invariata la password, ma ciò aumenta la probabilità di un attacco con password all'account del servizio. Tenere presente che anche se gestione controllo servizi archivia la password in una parte sicura del Registro di sistema, è comunque soggetta ad attacchi.

Un account utente di dominio ha due formati di nome: il nome distinto dell'oggetto utente nella directory e il formato " nome utente dominio " usato dal gestore &lt; &gt; \\ &lt; di controllo del &gt; servizio locale. Per altre informazioni e un esempio di codice che esegue la conversione da un formato all'altro, vedere [Conversione di formati di nomi di account di dominio.](converting-domain-account-name-formats.md)

 

 
