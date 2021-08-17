---
description: L'autenticazione non interattiva può essere usata solo dopo che è stata eseguita un'autenticazione interattiva. Durante l'autenticazione non interattiva, l'utente non specifica i dati di accesso, ma vengono usate le credenziali stabilite in precedenza.
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: Autenticazione non interattiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e259a2b14d48f4d7109966fa01f6fbd6a505a1343e90ea312c557ebfb9c84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786615"
---
# <a name="noninteractive-authentication"></a>Autenticazione non interattiva

L'autenticazione non interattiva può essere usata solo dopo che è [stata eseguita un'autenticazione](interactive-authentication.md) interattiva. Durante l'autenticazione non interattiva, l'utente non immettere i dati [*di*](../secgloss/l-gly.md)accesso , ma vengono utilizzate [*le credenziali stabilite*](../secgloss/c-gly.md) in precedenza.

L'autenticazione non interattiva viene eseguita quando un'applicazione usa [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) e un pacchetto di sicurezza per stabilire una connessione di rete protetta. L'autenticazione non interattiva è il meccanismo sul lavoro quando un utente si connette a più computer in una rete senza dover immettere nuovamente le informazioni di accesso per ogni computer. Ad esempio, se un'applicazione deve aprire una cartella sicura in un computer remoto e l'utente dell'applicazione è già connesso in modo interattivo a un account di dominio, l'applicazione non richiede all'utente di fornire nuovamente i dati di accesso. Al contrario, l'applicazione può richiedere un'autenticazione non interattiva usando SSPI per passare le informazioni di sicurezza stabilite in precedenza a un pacchetto di sicurezza. Il pacchetto di sicurezza usa quindi le funzioni LSA per controllare [*le credenziali*](../secgloss/c-gly.md). Nel diagramma seguente viene illustrata questa procedura.

![autenticazione non interattiva](images/lsasspi2.png)

Nel diagramma precedente l'applicazione client avvia una chiamata a SSPI per richiedere una connessione di rete autenticata. SSPI passa la richiesta del client a un pacchetto di sicurezza per l'elaborazione. Il pacchetto di sicurezza autentica l'utente chiamando l'autorità di [](../secgloss/a-gly.md) sicurezza locale [](../secgloss/l-gly.md) (LSA) e specificando un pacchetto di autenticazione e fornendo le credenziali esistenti dell'utente.

Il risultato dell'autenticazione viene passato [*dal*](../secgloss/a-gly.md)pacchetto di autenticazione , tramite LSA, al pacchetto di sicurezza [*e*](../secgloss/s-gly.md)infine a SSPI. SSPI notifica all'applicazione client il risultato della richiesta.

Per altre informazioni su SSPI, vedere [Security Support Provider Interface.](sspi.md)

 

 
