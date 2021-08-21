---
description: COM+ offre diverse funzionalità di sicurezza che è possibile usare per proteggere le applicazioni COM+, dai servizi che si configurano a livello amministrativo alle API che è possibile chiamare all'interno del codice.
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: Concetti relativi alla sicurezza COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b93ac113cf4ff2b1c679936fd610c2d44f29689ff175930c6a67274002457d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047529"
---
# <a name="com-security-concepts"></a>Concetti relativi alla sicurezza COM+

COM+ offre diverse funzionalità di sicurezza che è possibile usare per proteggere le applicazioni COM+, dai servizi che si configurano a livello amministrativo alle API che è possibile chiamare all'interno del codice.

Quando possibile, per le applicazioni COM+, è meglio usare la sicurezza automatica, ad esempio la sicurezza dichiarativa basata sui ruoli e l'autenticazione, anziché configurare la sicurezza all'interno dei componenti. L'uso della sicurezza automatica semplifica la scrittura e la gestione dei componenti, semplifica la progettazione della sicurezza in un'intera applicazione e, poiché è configurata a livello amministrativo, è più semplice modificare i criteri di sicurezza di un'applicazione. Questi servizi di sicurezza automatici rendono possibile lasciare tutte le funzionalità correlate alla sicurezza fuori dei componenti. Quando è possibile attivare i servizi e configurarli in modo appropriato, COM+ gestirà i dettagli dell'applicazione dei criteri di sicurezza specificati.

Tuttavia, quando i servizi di sicurezza automatici in COM+ non esetendono esattamente ciò che è necessario fare, è possibile estenderli, sulla base della piattaforma di sicurezza automatica fornita da COM+. Nei casi in cui si sceglie di non usare la sicurezza automatica o in cui si vuole usarla, ma è necessario basarsi su di essa per soddisfare i requisiti di sicurezza dell'applicazione, sono disponibili le opzioni seguenti per la configurazione della sicurezza a livello di codice:

-   Sicurezza basata sui ruoli a livello di codice, ad esempio il controllo dei ruoli, che è disponibile quando la sicurezza basata sui ruoli è abilitata per l'applicazione.
-   Rappresentazione: per quando si vuole usare l'identità di un client per accedere a una risorsa protetta.
-   Funzionalità di controllo basate sulle informazioni sul contesto di chiamata di sicurezza, disponibili anche quando è abilitata la sicurezza basata sui ruoli.

I meccanismi utilizzati per proteggere una determinata applicazione dipendono dai requisiti specifici dell'applicazione. Alcune scelte di sicurezza possono influire sulla modalità di scrittura dei componenti e altre possono influire in modo significativo sulla progettazione dell'applicazione. Prima di prendere decisioni su come implementare una strategia di sicurezza per un'applicazione, è necessario prendere in considerazione i requisiti di sicurezza nel contesto della progettazione complessiva, ovvero requisiti di prestazioni, accesso ai dati, progettazione fisica, e scegliere la combinazione più adatta di funzionalità di sicurezza. Per altre informazioni sull'implementazione della sicurezza a livello di codice, vedere [Sicurezza dei componenti a livello di codice.](programmatic-component-security.md)

Di seguito vengono fornite brevi descrizioni di categorie di sicurezza, funzionalità e problemi COM+, con collegamenti agli argomenti di questa sezione che forniscono una descrizione dettagliata di ognuna delle aree importanti.

> [!Note]  
> Anche se non sono descritti in questa sezione, i componenti in coda hanno anche problemi specifici relativi alle funzionalità di sicurezza disponibili. Per informazioni dettagliate, vedere [Sicurezza dei componenti in coda](queued-components-security.md) e Sviluppo di componenti in [coda](developing-queued-components.md).

 

## <a name="role-based-security"></a>Sicurezza basata sui ruoli

La sicurezza basata sui ruoli è la funzionalità centrale della sicurezza delle applicazioni COM+. Usando i ruoli, è possibile costruire a livello amministrativo un criterio di autorizzazione per un'applicazione, scegliendo (fino al livello del metodo, se necessario) quali utenti possono accedere alle risorse. Inoltre, i ruoli forniscono un framework per l'applicazione del controllo di sicurezza all'interno del codice se l'applicazione richiede un controllo degli accessi con granularità più fine.

La sicurezza basata sui ruoli si basa su un meccanismo generale che consente di recuperare informazioni di sicurezza relative a tutti i chiamanti upstream nella catena di chiamate al componente. Questa funzionalità è utile in particolare se si desidera eseguire operazioni di controllo e registrazione dettagliate. Per una descrizione delle funzionalità di controllo fornite da COM+, vedere Accesso alle informazioni sul contesto [delle chiamate di sicurezza](accessing-security-call-context-information.md).

Per una descrizione dei problemi di sicurezza e amministrazione basati sui ruoli che è necessario prendere in considerazione durante l'uso, vedere Amministrazione della sicurezza [basata sui ruoli](role-based-security-administration.md).

## <a name="client-authentication"></a>Client Authentication (Autenticazione client)

Prima di autorizzare i client ad accedere alle risorse, è necessario essere certi che siano quelli che affermano di essere. Per abilitare questa verifica dell'identità, COM+ fornisce servizi di autenticazione. Anche se questi servizi vengono effettivamente forniti a un livello più fondamentale da COM e Microsoft Windows, un'applicazione COM+ consente di attivare il servizio di autenticazione a livello amministrativo in modo che funzioni in modo trasparente per l'applicazione. Per una descrizione dei servizi di autenticazione, vedere [Autenticazione client](client-authentication.md).

## <a name="client-impersonation-and-delegation"></a>Rappresentazione e delega del client

In alcuni casi, l'applicazione deve eseguire operazioni per conto di un client usando l'identità del client, ad esempio quando si accede a un database che eseguirà l'autenticazione del client originale. A questo scopo, l'applicazione deve rappresentare il client. COM+ offre funzionalità per abilitare vari livelli di rappresentazione. La rappresentazione è configurata a livello amministrativo, ma è anche necessario fornire il supporto per la rappresentazione con il codice dei componenti dell'applicazione. Per una descrizione della rappresentazione e dei problemi relativi all'uso, vedere [Rappresentazione client e delega](client-impersonation-and-delegation.md).

## <a name="using-the-software-restriction-policy-in-com"></a>Uso dei criteri di restrizione software in COM+

I criteri di restrizione software forniscono un modo per eseguire codice non attendibile e quindi potenzialmente dannoso in un ambiente vincolato in modo che non possa utilizzare in modo improprio i privilegi dell'utente. Questa operazione viene eseguita assegnando livelli di attendibilità ai file che l'utente può eseguire. Ad esempio, alcuni file di sistema possono essere completamente attendibili e avere accesso senza restrizioni ai privilegi dell'utente, mentre un file scaricato da Internet potrebbe essere completamente non attendibile e pertanto può essere eseguito solo in un ambiente con restrizioni in cui non è consentito l'uso di privilegi utente sensibili alla sicurezza.

I criteri di restrizione software a livello di sistema vengono controllati tramite lo strumento amministrativo Criteri di sicurezza locali, che consente agli amministratori di configurare i livelli di attendibilità per singoli file. Tuttavia, tutte le applicazioni server COM+ vengono eseguite nel file dllhost.exe. COM+ consente quindi di specificare i criteri di restrizione software per ogni applicazione server in modo che non devono dipendere dai criteri di restrizione del file dllhost.exe. Per una discussione su come usare i criteri di restrizione software in COM+, vedere Uso dei criteri [di restrizione software in COM+](using-the-software-restriction-policy-in-com-.md).

## <a name="library-application-security"></a>Sicurezza delle applicazioni della libreria

Le applicazioni di libreria hanno considerazioni speciali sulla sicurezza. Poiché queste applicazioni vengono eseguite nel processo del client, sono interessate dalla sicurezza applicata dal processo di hosting e non sono in grado di controllare la sicurezza a livello di processo. Per una descrizione dei fattori da considerare per le applicazioni di libreria, vedere [Sicurezza delle applicazioni della libreria](library-application-security.md).

## <a name="multi-tier-application-security"></a>Sicurezza delle applicazioni multilivello

Le applicazioni COM+ sono in genere applicazioni di livello intermedio. in altre modo spostano le informazioni tra i client e le risorse back-end, ad esempio i database. Le scelte difficili possono essere coinvolte nella determinazione della posizione in cui applicare la sicurezza e in quale grado. La sicurezza implica intrinsecamente compromessi delle prestazioni. Alcuni dei casi più gravi si verificano quando è necessario applicare il controllo di sicurezza sia a livello dati che a livello intermedio. Per una descrizione dei problemi da considerare, vedere [Sicurezza delle applicazioni multilivello.](multi-tier-application-security.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega del client](client-impersonation-and-delegation.md)
</dt> <dt>

[Attività di sicurezza COM+](com--security-tasks.md)
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

 

 



