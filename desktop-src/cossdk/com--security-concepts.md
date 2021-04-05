---
description: COM+ offre diverse funzionalità di sicurezza che è possibile usare per proteggere le applicazioni COM+, a partire dai servizi configurati in modo amministrativo per le API che è possibile chiamare all'interno del codice.
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: Concetti sulla sicurezza COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca5126f4b715f84c2b8801c8ec1adc29b3cbb83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049264"
---
# <a name="com-security-concepts"></a>Concetti sulla sicurezza COM+

COM+ offre diverse funzionalità di sicurezza che è possibile usare per proteggere le applicazioni COM+, a partire dai servizi configurati in modo amministrativo per le API che è possibile chiamare all'interno del codice.

Laddove possibile, per le applicazioni COM+ è preferibile usare la sicurezza automatica, ad esempio la sicurezza e l'autenticazione dichiarative basate sui ruoli, invece di configurare la sicurezza all'interno dei componenti. L'uso della sicurezza automatica semplifica la scrittura e la gestione dei componenti, semplifica la progettazione della sicurezza in un'intera applicazione e, poiché è configurata in modo amministrativo, più semplice da modificare i criteri di sicurezza di un'applicazione. Questi servizi di sicurezza automatici permettono di lasciare tutte le funzionalità relative alla sicurezza dai componenti di. Quando è possibile attivare i servizi e configurarli in modo appropriato, COM+ gestirà i dettagli dell'applicazione dei criteri di sicurezza specificati.

Tuttavia, quando i servizi di sicurezza automatici in COM+ non eseguono esattamente le operazioni necessarie, è possibile estenderli, basandosi sulla piattaforma di sicurezza automatica fornita da COM+. Nei casi in cui si sceglie di non usare la sicurezza automatica o la posizione in cui si vuole usarla, ma è necessario basarsi su di essa per soddisfare i requisiti di sicurezza dell'applicazione, sono disponibili le opzioni seguenti per la configurazione della sicurezza a livello di programmazione:

-   Sicurezza basata sui ruoli a livello di codice, ad esempio il controllo dei ruoli, disponibile quando è abilitata la sicurezza basata sui ruoli per l'applicazione.
-   Rappresentazione: quando si vuole usare l'identità di un client per accedere a una risorsa protetta.
-   Funzionalità di controllo basate sulle informazioni sul contesto delle chiamate di sicurezza, disponibili anche quando è abilitata la sicurezza basata sui ruoli.

I meccanismi usati per proteggere una determinata applicazione dipendono dai requisiti specifici dell'applicazione. Alcune opzioni di sicurezza possono influire sulla modalità di scrittura dei componenti e alcune possono influire significativamente sulla progettazione dell'applicazione. Prima di prendere decisioni su come implementare una strategia di sicurezza per un'applicazione, è necessario considerare i requisiti di sicurezza nel contesto della progettazione complessiva, ovvero i requisiti di prestazioni, l'accesso ai dati, la progettazione fisica, e scegliere la combinazione più adatta di funzionalità di sicurezza. Per ulteriori informazioni sull'implementazione della sicurezza a livello di codice, vedere [sicurezza dei componenti programmatici](programmatic-component-security.md).

Di seguito sono riportate brevi descrizioni delle categorie, delle funzionalità e dei problemi relativi alla sicurezza COM+, con collegamenti agli argomenti di questa sezione che forniscono una descrizione dettagliata di ogni area importante.

> [!Note]  
> Anche se non illustrata in questa sezione, i componenti in coda presentano problemi specifici relativi alle funzionalità di sicurezza disponibili. Per informazioni dettagliate, vedere [sicurezza dei componenti in coda](queued-components-security.md) e sviluppo di componenti in [coda](developing-queued-components.md).

 

## <a name="role-based-security"></a>Sicurezza basata sui ruoli

La protezione basata sui ruoli è la funzionalità centralizzata della sicurezza delle applicazioni COM+. Utilizzando i ruoli, è possibile costruire in modo amministrativo un criterio di autorizzazione per un'applicazione, scegliendo (fino al livello del metodo, se necessario) quali utenti possono accedere alle risorse. Inoltre, i ruoli forniscono un Framework per applicare il controllo della sicurezza all'interno del codice se l'applicazione richiede un controllo di accesso con granularità fine.

La protezione basata sui ruoli si basa su un meccanismo generale che consente di recuperare le informazioni di sicurezza relative a tutti i chiamanti upstream nella catena di chiamate al componente. Questa funzionalità è particolarmente utile se si desidera eseguire operazioni di controllo e registrazione dettagliate. Per una descrizione delle funzionalità di controllo fornite da COM+, vedere [accesso alle informazioni sul contesto delle chiamate di sicurezza](accessing-security-call-context-information.md).

Per una descrizione della sicurezza basata sui ruoli e dei problemi amministrativi che è necessario prendere in considerazione quando si usa, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).

## <a name="client-authentication"></a>Client Authentication (Autenticazione client)

Prima di autorizzare i client a poter accedere alle risorse, è necessario essere certi che siano quelli che affermano di essere. Per abilitare questa verifica dell'identità, COM+ fornisce servizi di autenticazione. Sebbene questi servizi siano effettivamente forniti a un livello più fondamentale da parte di COM e Microsoft Windows, un'applicazione COM+ consente di attivare il servizio di autenticazione in modo amministrativo, in modo che funzioni sotto le quinte, trasparenti per l'applicazione. Per una descrizione dei servizi di autenticazione, vedere [autenticazione client](client-authentication.md).

## <a name="client-impersonation-and-delegation"></a>Rappresentazione e delega client

In alcuni casi, l'applicazione deve lavorare per conto di un client usando l'identità del client, ad esempio quando si accede a un database che sta per autenticare il client originale. A tale scopo, l'applicazione deve rappresentare il client. COM+ fornisce funzionalità per consentire diversi livelli di rappresentazione. La rappresentazione è configurata in modo amministrativo, ma è necessario anche fornire supporto per la rappresentazione con il codice dei componenti dell'applicazione. Per una descrizione della rappresentazione e dei problemi relativi all'utilizzo, vedere [rappresentazione e delega del client](client-impersonation-and-delegation.md).

## <a name="using-the-software-restriction-policy-in-com"></a>Uso dei criteri di restrizione software in COM+

I criteri di restrizione software consentono di eseguire codice non attendibile e potenzialmente dannoso in un ambiente vincolato, in modo che non possa usare i privilegi dell'utente in modo improprio. Questa operazione viene eseguita assegnando livelli di attendibilità ai file che l'utente può eseguire. Alcuni file di sistema, ad esempio, possono essere completamente attendibili e concedere un accesso illimitato ai privilegi dell'utente, mentre un file scaricato da Internet potrebbe essere completamente non attendibile e quindi consentirne l'esecuzione solo in un ambiente con restrizioni in cui non è consentito l'utilizzo di privilegi utente sensibili alla sicurezza.

I criteri di restrizione software di a livello sono controllati tramite lo strumento di amministrazione Criteri di sicurezza locali, che consente agli amministratori di configurare i livelli di attendibilità per i singoli file. Tuttavia, tutte le applicazioni server COM+ vengono eseguite nel file di dllhost.exe. COM+ consente pertanto di specificare i criteri di restrizione software per ogni applicazione server in modo che non debbano dipendere dai criteri di restrizione del file dllhost.exe. Per informazioni sull'utilizzo dei criteri di restrizione software in COM+, vedere [utilizzo dei criteri di restrizione software in com+](using-the-software-restriction-policy-in-com-.md).

## <a name="library-application-security"></a>Sicurezza delle applicazioni di libreria

Le applicazioni di libreria hanno particolari considerazioni sulla sicurezza. Dal momento che queste applicazioni vengono eseguite nel processo del client, sono interessate dalla sicurezza applicata dal processo di hosting e non possono controllare la sicurezza a livello di processo. Per una descrizione dei fattori da considerare per le applicazioni di libreria, vedere [Library Application Security](library-application-security.md).

## <a name="multi-tier-application-security"></a>Sicurezza delle applicazioni a più livelli

Le applicazioni COM+ sono in genere applicazioni di livello intermedio; ovvero spostano le informazioni tra i client e le risorse back-end, ad esempio i database. Le scelte difficili possono essere necessarie per determinare la posizione in cui deve essere applicata la sicurezza e il grado. La sicurezza implica ingenti compromessi in materia di prestazioni. Alcuni dei più gravi di questi si verificano quando è necessario applicare il controllo di sicurezza a livello di dati e di livello intermedio. Per informazioni sui problemi da prendere in considerazione, vedere [sicurezza delle applicazioni](multi-tier-application-security.md)a più livelli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega client](client-impersonation-and-delegation.md)
</dt> <dt>

[Attività di sicurezza COM+](com--security-tasks.md)
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

 

 



