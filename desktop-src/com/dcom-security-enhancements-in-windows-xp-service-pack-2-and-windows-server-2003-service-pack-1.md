---
title: Miglioramenti della sicurezza DCOM in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1
description: Windows Server XP Service Pack 2 (SP2) e Windows Server 2003 Service Pack 1 (SP1) introducono impostazioni di sicurezza predefinite avanzate per Distributed Component Object Model (DCOM).
ms.assetid: 1917834c-5216-4ef3-a0c2-d8ca63cef53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d093186f3d0a028112248409b71e0d71ed084e15cc075a1aced7a589aa0733ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501331"
---
# <a name="dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Miglioramenti della sicurezza DCOM in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1

Windows Server XP Service Pack 2 (SP2) e Windows Server 2003 Service Pack 1 (SP1) introducono impostazioni di sicurezza predefinite avanzate per Distributed Component Object Model (DCOM). In particolare, introducono diritti più granulari che consentono a un amministratore di avere un controllo indipendente sulle autorizzazioni locali e remote per l'avvio, l'attivazione e l'accesso ai server COM.

## <a name="what-does-dcom-do"></a>Che cosa fa DCOM?

Microsoft Component Object Model (COM) è un sistema indipendente dalla piattaforma, distribuito e orientato a oggetti per la creazione di componenti software binari in grado di interagire. Distributed Component Object Model (DCOM) consente di distribuire le applicazioni tra posizioni più sensato per l'utente e per l'applicazione. Il protocollo di collegamento DCOM fornisce in modo trasparente il supporto per comunicazioni affidabili, sicure ed efficienti tra i componenti COM.

## <a name="who-does-this-feature-apply-to"></a>Destinatari del servizio

Se si usa SOLO COM per i componenti COM in-process, questa funzionalità non è applicabile all'utente.

Questa funzionalità si applica all'utente se si dispone di un'applicazione server COM che soddisfa uno dei criteri seguenti:

-   L'autorizzazione di accesso per l'applicazione è meno stringente rispetto all'autorizzazione di avvio, necessaria per eseguire l'applicazione.
-   L'applicazione viene in genere attivata da un client COM remoto senza usare un account amministrativo.
-   L'applicazione deve essere usata solo in locale. Ciò significa che è possibile limitare l'applicazione server COM in modo che non sia accessibile in remoto.

## <a name="what-new-functionality-is-added-to-this-feature-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Quali nuove funzionalità vengono aggiunte a questa funzionalità in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1?

### <a name="computer-wide-restrictions"></a>Restrizioni a livello di computer

In COM è stata apportata una modifica per fornire controlli di accesso a livello di computer che regolano l'accesso a tutte le richieste di chiamata, attivazione o avvio nel computer. Il modo più semplice per pensare a questi controlli di accesso è come una chiamata [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) aggiuntiva eseguita su un elenco di controllo di accesso (ACL) a livello di computer a ogni chiamata, attivazione o avvio di qualsiasi server COM nel computer. Se **accessCheck ha** esito negativo, la richiesta di chiamata, attivazione o avvio viene negata. Oltre a qualsiasi **controllo** di accesso eseguito con gli ACL specifici del server. In effetti, fornisce uno standard di autorizzazione minimo che deve essere passato per accedere a qualsiasi server COM nel computer. È disponibile un ACL a livello di computer per le autorizzazioni di avvio per coprire i diritti di attivazione e avvio e un ACL a livello di computer per le autorizzazioni di accesso per coprire i diritti di chiamata. Questi possono essere configurati tramite l'Microsoft Management Console servizi componenti (MMC).

Questi ACL a livello di computer consentono di eseguire l'override delle impostazioni di sicurezza deboli specificate da un'applicazione specifica tramite [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o impostazioni di sicurezza specifiche dell'applicazione. In questo modo viene fornito uno standard di sicurezza minimo che deve essere passato, indipendentemente dalle impostazioni del server specifico.

Questi ACL vengono controllati quando si accede alle interfacce esposte da RPCSS. In questo modo viene fornito un metodo per controllare l'accesso a questo servizio di sistema.

Questi elenchi di controllo di accesso forniscono una posizione centralizzata in cui un amministratore può impostare criteri di autorizzazione generali applicabili a tutti i server COM nel computer.

> [!Note]  
> La modifica delle impostazioni di sicurezza a livello di computer influirà su tutte le applicazioni server COM e potrebbe impedirne il corretto funzionamento. Se sono presenti applicazioni server COM con restrizioni meno stringenti rispetto alle restrizioni a livello di computer, la riduzione delle restrizioni a livello di computer potrebbe esporre tali applicazioni ad accessi indesiderati. Viceversa, se si aumentano le restrizioni a livello di computer, alcune applicazioni server COM potrebbero non essere più accessibili chiamando le applicazioni.

 

Per impostazione predefinita, Windows di restrizione del computer XP SP2 sono:



| Autorizzazione        | Amministratore                                                                                             | Tutti                                            | Anonimo               |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-------------------------|
| Launch<br/> | Avvio locale<br/> Attivazione locale<br/> Avvio remoto<br/> Attivazione remota<br/> | Avvio locale<br/> Attivazione locale<br/> |                         |
| Access<br/> |                                                                                                           | Accesso locale<br/> Accesso remoto<br/>    | Accesso locale<br/> |



 

Per impostazione predefinita, Windows le impostazioni relative alle restrizioni del computer per Server 2003 SP 1 sono le seguenti.



| Autorizzazione        | Amministratore                                                                                             | Utenti COM distribuiti (gruppo predefinito)                                                                    | Tutti                                            | Anonimo                                        |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------|
| Launch<br/> | Avvio locale<br/> Attivazione locale<br/> Avvio remoto<br/> Attivazione remota<br/> | Avvio locale<br/> Attivazione locale<br/> Avvio remoto<br/> Attivazione remota<br/> | Avvio locale<br/> Attivazione locale<br/> | N/A<br/>                                   |
| Access<br/> | N/A<br/>                                                                                            | Accesso locale<br/> Accesso remoto<br/>                                                          | Accesso locale<br/> Accesso remoto<br/>    | Accesso locale<br/> Accesso remoto<br/> |



 

> [!Note]  
> Distributed COM Users è un nuovo gruppo predefinito incluso in Windows Server 2003 SP1 per velocizzare il processo di aggiunta di utenti alle impostazioni relative alle restrizioni del computer DCOM. Questo gruppo fa parte dell'elenco di controllo di accesso usato dalle impostazioni [MachineAccessRestriction](machineaccessrestriction.md) e [MachineLaunchRestriction,](machinelaunchrestriction.md) quindi la rimozione di utenti da questo gruppo influirà su tali impostazioni.

 

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Vantaggi della nuova funzionalità e rischi che consente di attenuare

Molte applicazioni COM includono codice specifico della sicurezza (ad esempio, la chiamata [**a CoInitializeSecurity),**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)ma usano impostazioni deboli, consentendo spesso l'accesso non autenticato al processo. Non è attualmente possibile per un amministratore eseguire l'override di queste impostazioni per forzare una maggiore sicurezza nelle versioni precedenti di Windows.

L'infrastruttura COM include RPCSS, un servizio di sistema che viene eseguito durante l'avvio del sistema e viene sempre eseguito successivamente. Gestisce l'attivazione di oggetti COM e la tabella di oggetti in esecuzione e fornisce servizi helper per la comunicazione remota DCOM. Espone le interfacce RPC che possono essere chiamate in remoto. Poiché alcuni server COM consentono l'accesso remoto non autenticato, queste interfacce possono essere chiamate da chiunque, inclusi gli utenti non autenticati. Di conseguenza, RPCSS può essere oggetto di attacchi da parte di utenti malintenzionati in computer remoti non autenticati.

Nelle versioni precedenti di Windows, un amministratore non era in grado di comprendere il livello di esposizione dei server COM in un computer. Un amministratore ha avuto un'idea del livello di esposizione controllando sistematicamente le impostazioni di sicurezza configurate per tutte le applicazioni COM registrate nel computer, ma, dato che sono presenti circa 150 server COM in un'installazione predefinita di Windows, l'attività era difficile. Non è possibile visualizzare le impostazioni per un server che incorpora la sicurezza nel software, a meno che non si riveda il codice sorgente per tale software.

Le restrizioni a livello di computer DCOM attenuano questi tre problemi. Offre inoltre a un amministratore la possibilità di disabilitare l'attivazione, l'avvio e le chiamate DCOM in ingresso.

### <a name="what-works-differently"></a>Differenze di funzionamento

Per impostazione predefinita, al gruppo Everyone vengono concesse le autorizzazioni di avvio locale, attivazione locale e chiamata di accesso locale. In questo modo tutti gli scenari locali possono funzionare senza modifiche al software o al sistema operativo.

Per impostazione predefinita, in Windows XP SP2, al gruppo Everyone vengono concesse le autorizzazioni di chiamata di accesso remoto. In Windows Server 2003 SP1, ai gruppi Everyone e Anonymous vengono concesse autorizzazioni di accesso remoto. Ciò consente la maggior parte degli scenari client COM, incluso il caso comune in cui un client COM passa un riferimento locale a un server remoto, trasformando di fatto il client in un server. In Windows XP SP2, questo potrebbe disabilitare gli scenari che richiedono chiamate di accesso remoto non autenticate.

Inoltre, per impostazione predefinita, solo ai membri del gruppo Administrators vengono concesse le autorizzazioni di attivazione remota e avvio. In questo modo le attivazioni remote da parte di utenti non amministratori vengono disabilitate nei server COM installati.

### <a name="how-do-i-resolve-these-issues"></a>Ricerca per categorie risolvere questi problemi?

Se si implementa un server COM e si prevede di supportare l'attivazione remota da parte di un client COM non amministrativo, è necessario valutare se il rischio associato all'abilitazione di questo processo è accettabile o se è necessario modificare l'implementazione per non richiedere l'attivazione remota da parte di un client COM non amministrativo o chiamate remote non autenticate.

Se il rischio è accettabile e si vuole abilitare l'attivazione remota da un client COM non amministrativo o da chiamate remote non autenticate, è necessario modificare la configurazione predefinita per questa funzionalità.

> [!Note]  
> La modifica delle impostazioni di sicurezza a livello di computer influirà su tutte le applicazioni server COM e potrebbe impedirne il corretto funzionamento. Se sono presenti applicazioni server COM con restrizioni meno stringenti rispetto alle restrizioni a livello di computer, la riduzione delle restrizioni a livello di computer può esporre queste applicazioni ad accesso indesiderato. Al contrario, se si aumentano le restrizioni a livello di computer, alcune applicazioni server COM potrebbero non essere più accessibili chiamando le applicazioni.

 

È possibile modificare le impostazioni di configurazione usando l'Microsoft Management Console servizi componenti (MMC) o il registro Windows.

Se si usa lo snap-in MMC Servizi componenti, queste impostazioni  possono essere configurate nella scheda **Sicurezza COM** della finestra di dialogo Proprietà per il computer che si sta gestendo. **L'area Autorizzazioni** di accesso è stata modificata per consentire di impostare limiti a livello di computer oltre alle impostazioni predefinite standard per i server COM. Inoltre, è possibile specificare impostazioni ACL separate per l'accesso locale e remoto sia nei limiti che nelle impostazioni predefinite.

**Nell'area Autorizzazioni di** avvio e attivazione è possibile controllare le autorizzazioni locali e remote, nonché i limiti a livello di computer e le impostazioni predefinite. È possibile specificare le autorizzazioni di attivazione locale e remota e di avvio in modo indipendente.

In alternativa, è possibile configurare queste impostazioni ACL usando il Registro di sistema.

Questi ACL vengono archiviati nel Registro di sistema nei percorsi seguenti:

``` syntax
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineAccessRestriction=ACL
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineLaunchRestriction=ACL
```

Si tratta di valori denominati di tipo REG BINARY che contengono dati che descrivono l'ACL delle entità che possono accedere a qualsiasi classe COM o oggetto \_ COM nel computer. I diritti di accesso nell'elenco di controllo di accesso sono:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Questi ACL possono essere creati usando normali funzioni di sicurezza.

> [!Note]  
> Per garantire la compatibilità con le versioni precedenti, un elenco di controllo di accesso può esistere nel formato usato prima di Windows XP SP2 e Windows Server 2003 SP1, che usa solo il diritto di accesso COM RIGHTS EXECUTE, oppure può esistere nel nuovo formato usato in Windows XP SP2 e \_ Windows Server 2003 SP1, che usa COM RIGHTS EXECUTE insieme a una combinazione di \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE \_ \_ \_ REMOTE, COM RIGHTS ACTIVATE LOCAL \_ e COM RIGHTS ACTIVATE \_ \_ \_ \_ \_ REMOTE. Si noti che COM RIGHTS EXECUTE> deve essere sempre presente. L'assenza di questo diritto genera un descrittore \_ \_ di sicurezza non valido. Si noti anche che non è necessario combinare il formato precedente e il nuovo formato all'interno di un singolo ACL. Tutte le voci di controllo di accesso (ACE) devono concedere solo il diritto di accesso COM RIGHTS EXECUTE oppure tutte devono concedere COM RIGHTS EXECUTE insieme a una combinazione di \_ \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL e \_ COM RIGHTS \_ ACTIVATE \_ \_ \_ \_ \_ \_ \_ REMOTE.

 

> [!Note]  
> Solo gli utenti con diritti di amministratore possono modificare queste impostazioni.

 

## <a name="what-existing-functionality-is-changing-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Quali funzionalità esistenti stanno cambiando in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1?

### <a name="rpcss-runs-as-a-network-service"></a>RPCSS viene eseguito come servizio di rete

RPCSS è un servizio chiave per l'infrastruttura DCOM e mapper di endpoint RPC. Questo servizio è stato eseguito come sistema locale nelle versioni precedenti di Windows. Per ridurre la superficie di Windows e fornire una difesa approfondita, la funzionalità del servizio RPCSS è stata suddivisa in due servizi. Il servizio RPCSS con tutte le funzionalità originali che non richiedeva privilegi di sistema locale viene ora eseguito con l'account del servizio di rete. Un nuovo servizio DCOMLaunch che include funzionalità che richiedono privilegi di sistema locale viene eseguito con l'account di sistema locale.

### <a name="why-is-this-change-important"></a>Vantaggi della nuova funzionalità e

Questa modifica riduce la superficie di attacco e fornisce una difesa approfondita per il servizio RPCSS perché l'elevazione dei privilegi nel servizio RPCSS è ora limitata al privilegio Servizio di rete.

### <a name="what-works-differently"></a>Differenze di funzionamento

Questa modifica deve essere trasparente per gli utenti perché la combinazione dei servizi RPCSS e DCOMLaunch equivale al servizio RPCSS precedente fornito nelle versioni precedenti di Windows.

### <a name="more-specific-com-permissions"></a>Autorizzazioni COM più specifiche

Le applicazioni server COM hanno due tipi di autorizzazioni: autorizzazioni di avvio e autorizzazioni di accesso. Le autorizzazioni di avvio controllano l'autorizzazione per avviare un server COM durante l'attivazione COM se il server non è già in esecuzione. Queste autorizzazioni sono definite come descrittori di sicurezza specificati nelle impostazioni del Registro di sistema. Le autorizzazioni di accesso controllano l'autorizzazione per chiamare un server COM in esecuzione. Queste autorizzazioni sono definite come descrittori di sicurezza forniti all'infrastruttura COM tramite l'API [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o usando le impostazioni del Registro di sistema. Sia le autorizzazioni di avvio che di accesso consentono o negano l'accesso in base alle entità e non fanno distinzione se il chiamante è locale al server o remoto.

La prima modifica distingue i diritti di accesso COM in base alla distanza. Le due distanze definite sono Local e Remote. Un messaggio COM locale arriva tramite il protocollo LRPC (Local Remote Procedure Call), mentre un messaggio COM remoto arriva tramite un protocollo host RPC (Remote Procedure Call), ad esempio tcp (Transmission Control Protocol).

L'attivazione COM è l'azione di ottenere un proxy di interfaccia COM in un client chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o una delle relative varianti. Come effetto collaterale di questo processo di attivazione, talvolta un server COM deve essere avviato per soddisfare la richiesta del client. Un elenco di controllo di accesso per le autorizzazioni di avvio asserirà chi è autorizzato ad avviare un server COM. Un ACL per le autorizzazioni di accesso asserzione chi può attivare un oggetto COM o chiamare tale oggetto una volta che il server COM è già in esecuzione.

La seconda modifica è che i diritti di chiamata e attivazione sono separati in modo da riflettere due operazioni distinte e spostare il diritto di attivazione dall'ACL dell'autorizzazione di accesso all'ACL di autorizzazione di avvio. Poiché l'attivazione e l'avvio sono entrambi correlati all'acquisizione di un puntatore a interfaccia, i diritti di accesso di attivazione e avvio appartengono logicamente a un unico elenco di controllo di accesso. Inoltre, poiché si specificano sempre le autorizzazioni di avvio tramite la configurazione (rispetto alle autorizzazioni di accesso, spesso specificate a livello di codice), l'inserimento dei diritti di attivazione nell'elenco di controllo di accesso delle autorizzazioni di avvio fornisce all'amministratore il controllo sull'attivazione.

Le voci di controllo di accesso delle autorizzazioni di avvio sono suddivise in quattro diritti di accesso:

-   Avvio locale (LL)
-   Avvio remoto (RL)
-   Attivazione locale (LA)
-   Attivazione remota (RA)

Il descrittore di sicurezza dell'autorizzazione di accesso è suddiviso in due diritti di accesso:

-   Chiamate di accesso locale (LC)
-   Chiamate di accesso remoto (RC)

In questo modo l'amministratore può applicare configurazioni di sicurezza molto specifiche. Ad esempio, è possibile configurare un server COM in modo che accetti le chiamate di accesso locale da tutti gli utenti, accettando al tempo stesso solo chiamate di accesso remoto da amministratori. Queste distinzioni possono essere specificate tramite modifiche ai descrittori di sicurezza delle autorizzazioni COM.

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Vantaggi della nuova funzionalità e rischi che consente di attenuare

Nelle versioni precedenti dell'applicazione server COM non è possibile limitare un'applicazione in modo che possa essere usata solo in locale senza esporre l'applicazione in rete tramite DCOM. Quando un utente ha accesso a un'applicazione server COM, può accedere sia per l'uso locale che per quello remoto.

Un'applicazione server COM potrebbe esporsi agli utenti non autenticati per implementare uno scenario di callback COM. In questo scenario, l'applicazione deve anche esporre la propria attivazione agli utenti non autenticati, il che potrebbe non essere auspicabile.

Autorizzazioni COM precise offrono flessibilità all'amministratore per controllare i criteri di autorizzazione COM di un computer. Queste autorizzazioni abilitano la sicurezza per gli scenari descritti.

### <a name="what-works-differently-are-there-any-dependencies"></a>Differenze di funzionamento Sono presenti dipendenze?

Per garantire la compatibilità con le versioni precedenti, i descrittori di sicurezza COM esistenti vengono interpretati per consentire o negare contemporaneamente l'accesso locale e remoto. Ovvero, una voce di controllo di accesso (ACE) consente sia locale che remota o nega sia locale che remota.

Non sono presenti problemi di compatibilità con le versioni precedenti per i diritti di chiamata o di avvio. Esiste tuttavia un problema di compatibilità dei diritti di attivazione. Se, nei descrittori di sicurezza esistenti per un server COM, le autorizzazioni di avvio configurate sono più restrittive delle autorizzazioni di accesso e sono più restrittive di quelle minime necessarie per gli scenari di attivazione client, è necessario modificare l'elenco di controllo di accesso delle autorizzazioni di avvio per concedere ai client autorizzati le autorizzazioni di attivazione appropriate.

Per le applicazioni COM che usano le impostazioni di sicurezza predefinite, non si verificano problemi di compatibilità. Per le applicazioni avviate dinamicamente con l'attivazione COM, la maggior parte non presenta problemi di compatibilità, perché le autorizzazioni di avvio devono già includere chiunque sia in grado di attivare un oggetto. In caso contrario, tali applicazioni generano errori di attivazione anche prima di applicare Windows XP SP2 o Windows Server 2003 SP1, quando i chiamanti senza autorizzazione di avvio provano ad attivare un oggetto e il server COM non è già in esecuzione.

Le applicazioni più problematiche per i problemi di compatibilità sono le applicazioni COM già avviate da un altro meccanismo, ad esempio Windows Explorer o Gestione controllo servizi. È anche possibile avviare queste applicazioni con un'attivazione COM precedente, che esegue l'override delle autorizzazioni di accesso e avvio predefinite e specifica le autorizzazioni di avvio più restrittive rispetto alle autorizzazioni di chiamata. Per altre informazioni sulla risoluzione di questo problema di compatibilità, vedere "Ricerca per categorie risolvere questi problemi?" nella sezione successiva.

Se viene eseguito il rollback di un sistema aggiornato a Windows XP SP2 o Windows Server 2003 SP1 a uno stato precedente, qualsiasi ACE modificata per consentire l'accesso locale, l'accesso remoto o entrambi, viene interpretata per consentire l'accesso locale e remoto. Qualsiasi ACE modificata per negare l'accesso locale, l'accesso remoto o entrambi, viene interpretata per negare sia l'accesso locale che quello remoto. Ogni volta che si disinstalla un Service Pack, è necessario assicurarsi che nessuna ACE appena impostata impedirà il funzionamento delle applicazioni.

### <a name="how-do-i-resolve-these-issues"></a>Ricerca per categorie risolvere questi problemi?

Se si implementa un server COM e si eseguono l'override delle impostazioni di sicurezza predefinite, verificare che l'elenco di controllo di accesso delle autorizzazioni di avvio specifiche dell'applicazione concedi l'autorizzazione di attivazione agli utenti appropriati. In caso contrario, è necessario modificare l'ACL dell'autorizzazione di avvio specifica dell'applicazione per concedere agli utenti i diritti di attivazione appropriati in modo che le applicazioni e i componenti Windows che usano DCOM non riescano. Queste autorizzazioni di avvio specifiche dell'applicazione vengono archiviate nel Registro di sistema.

Gli ACL COM possono essere creati o modificati usando normali funzioni di sicurezza.

## <a name="what-settings-are-added-or-changed-in-windows-xp-service-pack-2"></a>Quali impostazioni vengono aggiunte o modificate in Windows XP Service Pack 2?

> [!Caution]  
> Un uso improprio di queste impostazioni può causare l'esito negativo Windows applicazioni e componenti che usano DCOM.

 

Nella tabella seguente vengono usate queste abbreviazioni:

LL - Avvio locale

LA - Attivazione locale

RL - Avvio remoto

RA - Attivazione remota

LC - Chiamate di accesso locale

RC - Chiamate di accesso remoto

ACL - Elenco di controllo di accesso



| Nome impostazione                                                                                         | Località                                                                                                       | Valore predefinito precedente                                                                                                                                                                     | Valore predefinito                                                                                                                                                                                                                                                                                                                                                             | Valori possibili                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Everyone - LL, LA, RL, RA<br/> Anonimo -<br/> LL, LA, RL, RA<br/> Si tratta di una nuova chiave del Registro di sistema. In base al comportamento esistente, questi sono i valori effettivi.<br/> | Amministratore: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Everyone - LC, RC<br/> Anonimo - LC, RC<br/> Si tratta di una nuova chiave del Registro di sistema. In base al comportamento esistente, questi sono i valori effettivi.<br/>                            | Everyone: LC, RC<br/> Anonimo: LC<br/>                                                                                                                                                                                                                                                                                                                      | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Non applicabile.<br/>                                                                                                                                                                 | Questa chiave del Registro di sistema non è presente. Tuttavia, una chiave o un valore mancante viene interpretato come 2.<br/> Questo evento non viene registrato per impostazione predefinita. Se si modifica questo valore in 1 per avviare la registrazione di queste informazioni per facilitare la risoluzione di un problema, assicurarsi di monitorare le dimensioni del registro eventi, perché si tratta di un evento che può generare un numero elevato di voci.<br/> | 1 - Registra sempre gli errori del registro eventi durante una chiamata nel processo del server COM.<br/> 2 - Non registrare mai gli errori del registro eventi durante una chiamata nel processo del server di chiamata.<br/>                                                  |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Non applicabile.<br/>                                                                                                                                                                 | Questa chiave del Registro di sistema non è presente. Tuttavia, una chiave o un valore mancante viene interpretato come 1.<br/> Questo evento viene registrato per impostazione predefinita. Raramente dovrebbe verificarsi.<br/>                                                                                                                                                                                                    | 1 - Registra sempre gli errori del registro eventi quando l'infrastruttura COM rileva un descrittore di sicurezza non valido.<br/> 2 - Non registrare mai errori del registro eventi quando l'infrastruttura COM rileva un descrittore di sicurezza non valido.<br/> |
| Restrizioni di avvio del computer DCOM nella sintassi SDDL (Security Descriptor Definition Language)<br/> | (Criteri di gruppo oggetto ) Configurazione computer e \\ Windows Impostazioni di sicurezza dei criteri \\ \\ locali<br/>  | Non applicabile.<br/>                                                                                                                                                                 | Non definito<br/>                                                                                                                                                                                                                                                                                                                                                    | Elenco di controllo di accesso in formato SDDL. L'esistenza di questo criterio sostituisce i valori in MachineLaunchRestriction, in precedenza.<br/>                                                                                            |
| DCOM:Machine Access Restrictions in Security Descriptor Definition Language (SDDL) Syntax<br/> | (Criteri di gruppo oggetto ) Configurazione computer e \\ Windows Impostazioni di sicurezza dei criteri \\ \\ locali<br/> | Non applicabile.<br/>                                                                                                                                                                 | Non definito<br/>                                                                                                                                                                                                                                                                                                                                                    | Elenco di controllo di accesso in formato SDDL. L'esistenza di questo criterio sostituisce i valori in MachineAccessRestriction, in precedenza.<br/>                                                                                            |



 

## <a name="what-settings-are-added-or-changed-in-windows-server-2003-service-pack-1"></a>Impostazioni aggiunte o modificate in Windows Server 2003 Service Pack 1

> [!Note]  
> L'uso non corretto di queste impostazioni può causare errori Windows applicazioni e componenti che usano DCOM.

 

Nella tabella seguente vengono usate queste abbreviazioni:

LL - Avvio locale

LA - Attivazione locale

RL - Avvio remoto

RA - Attivazione remota

LC - Chiamate di accesso locale

RC - Chiamate di accesso remoto

ACL - Elenco di controllo di accesso



| Nome impostazione                                                                                         | Località                                                                                                       | Valore predefinito precedente                                                                                                                                                             | Valore predefinito                                                                                                                                                                                                                                                                                                                                                             | Valori possibili                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Everyone: LL, LA, RL, RA<br/> Anonimo: LL, LA, RL, RA<br/> Si tratta di una nuova chiave del Registro di sistema. In base al comportamento esistente, si tratta dei valori effettivi.<br/> | Amministratore: LL, LA, RL, RA<br/> Everyone: LL, LA<br/> Utenti COM distribuiti: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                     | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Everyone: LC, RC<br/> Anonimo: LC, RC<br/> Si tratta di una nuova chiave del Registro di sistema. In base al comportamento esistente, si tratta dei valori effettivi.<br/>                 | Everyone: LC, RC<br/> Anonimo: LC, RC<br/>                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Non applicabile.<br/>                                                                                                                                                         | Questa chiave del Registro di sistema non è presente. Tuttavia, una chiave o un valore mancante viene interpretato come 2.<br/> Questo evento non viene registrato per impostazione predefinita. Se si modifica questo valore in 1 per avviare la registrazione di queste informazioni per facilitare la risoluzione di un problema, assicurarsi di monitorare le dimensioni del registro eventi, perché si tratta di un evento che può generare un numero elevato di voci.<br/> | 1 - Registra sempre gli errori del registro eventi quando l'infrastruttura COM rileva un descrittore di sicurezza non valido.<br/> 2 - Non registrare mai errori del registro eventi quando l'infrastruttura COM rileva un descrittore di sicurezza non valido.<br/> |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Non applicabile.<br/>                                                                                                                                                         | Questa chiave del Registro di sistema non è presente. Tuttavia, una chiave o un valore mancante viene interpretato come 1.<br/> Questo evento viene registrato per impostazione predefinita. Raramente dovrebbe verificarsi.<br/>                                                                                                                                                                                                    | 1 - Registra sempre gli errori del registro eventi quando l'infrastruttura COM rileva un descrittore di sicurezza non valido.<br/> 2 - Non registrare mai errori del registro eventi quando l'infrastruttura COM rileva un descrittore di sicurezza non valido.<br/>         |
| Restrizioni di avvio del computer DCOM nella sintassi SDDL (Security Descriptor Definition Language)<br/> | (Criteri di gruppo oggetto ) Configurazione computer e \\ Windows Impostazioni di sicurezza dei criteri \\ \\ locali<br/> | Non applicabile.<br/>                                                                                                                                                         | Non definito.<br/>                                                                                                                                                                                                                                                                                                                                                   | Elenco di controllo di accesso in formato SDDL. L'esistenza di questo criterio sostituisce i valori in MachineLaunchRestriction, in precedenza.<br/>                                                                                            |
| DCOM:Machine Access Restrictions in Security Descriptor Definition Language (SDDL) Syntax<br/> | (Criteri di gruppo oggetto ) Configurazione computer e \\ Windows Impostazioni di sicurezza dei criteri \\ \\ locali<br/> | Non applicabile.<br/>                                                                                                                                                         | Non definito.<br/>                                                                                                                                                                                                                                                                                                                                                   | Elenco di controllo di accesso in formato SDDL. L'esistenza di questo criterio sostituisce i valori in MachineAccessRestriction, in precedenza.<br/>                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

