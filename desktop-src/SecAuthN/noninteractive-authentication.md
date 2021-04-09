---
description: L'autenticazione non interattiva può essere utilizzata solo dopo che è stata eseguita un'autenticazione interattiva. Durante l'autenticazione non interattiva, l'utente non esegue l'input dei dati di accesso, bensì vengono utilizzate le credenziali stabilite in precedenza.
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: Autenticazione non interattiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658cba212403da2f970e056d7bacc1bc1bcaa559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966624"
---
# <a name="noninteractive-authentication"></a>Autenticazione non interattiva

L'autenticazione non interattiva può essere utilizzata solo dopo che è stata eseguita un' [autenticazione interattiva](interactive-authentication.md) . Durante l'autenticazione non interattiva, l'utente non esegue l'input [*dei dati di accesso*](../secgloss/l-gly.md), bensì vengono utilizzate le [*credenziali*](../secgloss/c-gly.md) stabilite in precedenza.

L'autenticazione non interattiva viene eseguita quando un'applicazione utilizza l'interfaccia SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) e un pacchetto di sicurezza per stabilire una connessione di rete sicura. L'autenticazione non interattiva è il meccanismo di lavoro quando un utente si connette a più computer in una rete senza dover immettere nuovamente le informazioni di accesso per ogni computer. Se, ad esempio, un'applicazione deve aprire una cartella protetta in un computer remoto e l'utente dell'applicazione è già connesso in modo interattivo a un account di dominio, l'applicazione non richiede che l'utente fornisca nuovamente i dati di accesso. L'applicazione può invece richiedere un'autenticazione non interattiva utilizzando SSPI per passare le informazioni di sicurezza precedentemente stabilite a un pacchetto di sicurezza. Il pacchetto di sicurezza usa quindi le funzioni LSA per verificare le [*credenziali*](../secgloss/c-gly.md). Nel diagramma seguente viene illustrata questa procedura.

![autenticazione non interattiva](images/lsasspi2.png)

Nel diagramma precedente, l'applicazione client avvia una chiamata a SSPI per richiedere una connessione di rete autenticata. SSPI passa la richiesta del client a un pacchetto di sicurezza per l'elaborazione. Il pacchetto di sicurezza autentica l'utente chiamando l' [*autorità di protezione locale*](../secgloss/l-gly.md) (LSA) e specificando un [*pacchetto di autenticazione*](../secgloss/a-gly.md) e fornendo le credenziali esistenti dell'utente.

Il risultato dell'autenticazione viene passato dal [*pacchetto di autenticazione*](../secgloss/a-gly.md), tramite LSA, al [*pacchetto di sicurezza*](../secgloss/s-gly.md)e infine a SSPI. SSPI notifica all'applicazione client il risultato della richiesta.

Per ulteriori informazioni su SSPI, vedere [Security Support Provider Interface](sspi.md).

 

 
