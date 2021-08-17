---
description: In alcuni casi, un'applicazione server deve presentare un'identità client alle risorse a cui accede per conto dei client, in genere per fare in modo che i controlli di accesso o l'autenticazione siano eseguiti sull'identità client.
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: Rappresentazione e delega del client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b0262f3d8dd6736d183fa76eb5d3f0946d50b2724e76bcea73843644aaefb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129373"
---
# <a name="client-impersonation-and-delegation"></a>Rappresentazione e delega del client

In alcuni casi, un'applicazione server deve presentare l'identità di un client alle risorse a cui accede per conto del client, in genere per fare in modo che i controlli di accesso o l'autenticazione siano eseguiti sull'identità del client. In un certo senso, il server può agire con l'identità del client, ovvero un'azione definita rappresentazione del client.

*La rappresentazione* è la capacità di un thread di essere eseguito in un contesto di sicurezza diverso da quello del processo proprietario del thread. Il thread del server usa un token di accesso che rappresenta le credenziali del client e, con questa operazione, può accedere alle risorse a cui il client può accedere.

L'uso della rappresentazione garantisce che il server possa eseguire esattamente le operazione che il client può eseguire. L'accesso alle risorse può essere limitato o espanso, a seconda di ciò che il client ha l'autorizzazione per eseguire.

È possibile scegliere di fare in modo che un server rappresentazione di un client durante la connessione a un database in modo che il database possa autenticare e autorizzare il client per se stesso. In caso contrario, se l'applicazione accede a file protetti con un descrittore di sicurezza e per consentire al client di ottenere l'accesso autorizzato alle informazioni in questi file, l'applicazione può rappresentare il client prima di accedere ai file.

## <a name="how-to-implement-impersonation"></a>Come implementare la rappresentazione

La rappresentazione richiede la partecipazione sia del client che del server (e, in alcuni casi, degli amministratori di sistema). Il client deve indicare la disponibilità a consentire al server di usare la propria identità e il server deve presupporre in modo esplicito l'identità del client a livello di codice. Per informazioni dettagliate, vedere gli argomenti [Requisiti lato client per la](client-side-requirements-for-impersonation.md) rappresentazione e Requisiti lato server per la [rappresentazione](server-side-requirements-for-impersonation.md).

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Requisiti amministrativi per Delegate-Level rappresentazione

Per usare in modo efficace la forma più potente di rappresentazione, la delega , ovvero la rappresentazione dei client in rete, gli account utente client e server devono essere configurati correttamente nel servizio Active Directory per supportarlo (oltre all'autorità che concede il client per eseguire la rappresentazione a livello di delegato), come indicato di seguito:

-   L'identità del server deve essere contrassegnata come "Trusted for delegation" nel servizio Active Directory.
-   L'identità client non deve essere contrassegnata come "L'account è sensibile e non può essere delegato" nel servizio Active Directory.

Queste funzionalità di configurazione offrono all'amministratore di dominio un elevato livello di controllo sulla delega, che è auspicabile, in base alla quantità di attendibilità (e quindi al rischio per la sicurezza). Per altre informazioni sulla delega, vedere [Delega e rappresentazione.](/windows/desktop/com/delegation-and-impersonation)

## <a name="cloaking"></a>Cloaking

Insieme all'autorità che un client concede a un server tramite il livello di rappresentazione, la funzionalità di cloaking del server determina in gran parte il comportamento della rappresentazione. Il cloaking influisce sull'identità effettivamente presentata dal server quando effettua chiamate per conto del client, ovvero per conto del client. Per informazioni dettagliate, vedere [Cloaking](cloaking.md).

## <a name="performance-implications"></a>Implicazioni per le prestazioni

La rappresentazione può influire in modo significativo sulle prestazioni e sul ridimensionamento. In genere è più costoso rappresentare un client in una chiamata piuttosto che effettuare direttamente la chiamata. Di seguito sono riportati alcuni dei problemi da considerare:

-   Sovraccarico di calcolo dovuto al passaggio dell'identità in modelli complessi, in particolare se è abilitato il cloaking dinamico.
-   La complessità generale dell'applicazione del controllo di sicurezza ridondante in numerose posizioni, anziché solo a livello centrale nel livello intermedio.
-   Le risorse, ad esempio le connessioni di database, quando vengono aperte rappresentando un client, non possono essere riutilizzate tra più client, un ostacolo molto grande alla scalabilità.

A volte l'unica soluzione efficace a un problema consiste nell'usare la rappresentazione, ma questa decisione deve essere ponderata attentamente. Per altre informazioni su questi problemi, vedere [Sicurezza delle applicazioni multilivello.](multi-tier-application-security.md)

## <a name="queued-components"></a>Componenti in coda

[I componenti in coda](com--queued-components.md) non supportano la rappresentazione. Quando un client effettua una chiamata a un oggetto in coda, la chiamata viene effettivamente effettuata al registratore, che lo crea come parte di un messaggio al server. Il listener legge quindi il messaggio dalla coda e lo passa al lettore, che richiama il componente server effettivo ed esegue la stessa chiamata al metodo . Di conseguenza, quando il server riceve la chiamata, il token client originale non è disponibile tramite rappresentazione. La sicurezza basata sui ruoli si applica comunque, tuttavia, e la sicurezza a livello di codice che usa [**l'interfaccia ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) funzionerà. Per informazioni dettagliate, vedere [Sicurezza dei componenti in coda](queued-components-security.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Sicurezza delle applicazioni della libreria](library-application-security.md)
</dt> <dt>

[Sicurezza delle applicazioni multilivello](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza dei componenti a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[Uso dei criteri di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
