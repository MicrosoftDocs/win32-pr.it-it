---
description: In alcune circostanze, un'applicazione server deve presentare un'identità dei client alle risorse a cui accede per conto dei client, in genere per consentire l'esecuzione di controlli di accesso o di autenticazione con l'identità dei client.
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: Rappresentazione e delega client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7557dcde4cadf559dd8e116cf4e7bece4221aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305018"
---
# <a name="client-impersonation-and-delegation"></a>Rappresentazione e delega client

In alcune circostanze, un'applicazione server deve presentare l'identità di un client alle risorse a cui accede per conto del client, in genere per eseguire verifiche di accesso o autenticazione per l'identità del client. In un certo senso, il server può agire sotto l'identità del client, un'azione detta rappresentazione del client.

La *rappresentazione* è la capacità di esecuzione di un thread in un contesto di sicurezza diverso da quello del processo proprietario del thread. Il thread del server utilizza un token di accesso che rappresenta le credenziali del client e, con questo, può accedere alle risorse a cui il client può accedere.

L'utilizzo della rappresentazione garantisce che il server sia in grado di eseguire esattamente le operazioni che il client può eseguire. L'accesso alle risorse può essere limitato o espanso, a seconda di ciò che il client è autorizzato a eseguire.

È possibile scegliere di fare in modo che un server rappresenti un client durante la connessione a un database in modo che il database possa autenticare e autorizzare il client per se stesso. In alternativa, se l'applicazione accede ai file protetti con un descrittore di sicurezza e per consentire al client di ottenere l'accesso autorizzato alle informazioni contenute in questi file, l'applicazione può rappresentare il client prima di accedere ai file.

## <a name="how-to-implement-impersonation"></a>Come implementare la rappresentazione

La rappresentazione richiede la partecipazione da parte del client e del server (e, in alcuni casi, degli amministratori di sistema). Il client deve indicare la volontà di consentire al server di usare la propria identità e il server deve presupporre in modo esplicito l'identità del client a livello di codice. Per informazioni dettagliate, vedere gli argomenti [requisiti lato client per la rappresentazione](client-side-requirements-for-impersonation.md) e [requisiti lato server per la rappresentazione](server-side-requirements-for-impersonation.md).

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Requisiti amministrativi per la rappresentazione Delegate-Level

Per utilizzare in modo efficace la forma di rappresentazione più potente, ovvero la *delega*, ovvero la rappresentazione dei client in rete, gli account utente client e server devono essere configurati correttamente nel servizio Active Directory per supportarlo (oltre all'autorità che concede l'autorizzazione per la rappresentazione a livello di delega), come indicato di seguito:

-   L'identità del server deve essere contrassegnata come "trusted per la delega" nel servizio Active Directory.
-   L'identità del client non deve essere contrassegnata come "l'account è sensibile e non può essere delegato" nel servizio Active Directory.

Queste funzionalità di configurazione offrono all'amministratore di dominio un elevato livello di controllo sulla delega, che è auspicabile, data la quantità di attendibilità (e di conseguenza il rischio per la sicurezza). Per ulteriori dettagli sulla delega, vedere [delega e rappresentazione](/windows/desktop/com/delegation-and-impersonation).

## <a name="cloaking"></a>Cloaking

Insieme all'autorità un client concede un server attraverso il livello di rappresentazione, la funzionalità di mascheramento del server determina in gran parte il comportamento della rappresentazione. Il cloaking influiscono sull'identità effettivamente presentata dal server quando effettua chiamate per conto dell'utente, ovvero il proprio o il client. Per informazioni dettagliate, vedere [mascheramento](cloaking.md).

## <a name="performance-implications"></a>Implicazioni per le prestazioni

La rappresentazione può influire in modo significativo sulle prestazioni e sulla scalabilità. È in genere più oneroso rappresentare un client in una chiamata anziché eseguire direttamente la chiamata. Di seguito sono riportati alcuni dei problemi da considerare:

-   Sovraccarico computazionale del passaggio dell'identità in modelli complicati, in particolare se è abilitato il mascheramento dinamico.
-   Complessità generale dell'applicazione del controllo di sicurezza ridondante in numerose posizioni, anziché solo centralmente nel livello intermedio.
-   Le risorse, ad esempio le connessioni al database, quando si apre la rappresentazione di un client, non possono essere riutilizzate in più client, un ostacolo molto grande per la scalabilità.

A volte l'unica soluzione efficace per un problema consiste nell'usare la rappresentazione, ma questa decisione deve essere ponderata con attenzione. Per ulteriori informazioni su questi problemi, vedere [sicurezza delle applicazioni](multi-tier-application-security.md)a più livelli.

## <a name="queued-components"></a>Componenti in coda

I [componenti in coda](com--queued-components.md) non supportano la rappresentazione. Quando un client effettua una chiamata a un oggetto in coda, la chiamata viene effettivamente effettuata al registratore, che lo inserisce come parte di un messaggio al server. Il listener legge quindi il messaggio dalla coda e lo passa al lettore, che richiama il componente server effettivo ed effettua la stessa chiamata al metodo. Di conseguenza, quando il server riceve la chiamata, il token client originale non è disponibile tramite la rappresentazione. La protezione basata sui ruoli si applica comunque e la sicurezza a livello di codice tramite l'interfaccia [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) funzionerà. Per informazioni dettagliate, vedere [sicurezza dei componenti in coda](queued-components-security.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Sicurezza delle applicazioni di libreria](library-application-security.md)
</dt> <dt>

[Sicurezza delle applicazioni a più livelli](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
