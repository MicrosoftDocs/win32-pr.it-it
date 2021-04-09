---
title: Miglioramenti della protezione DCOM in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1
description: Windows Server XP Service Pack 2 (SP2) e Windows Server 2003 Service Pack 1 (SP1) introducono impostazioni di sicurezza predefinite avanzate per il Component Object Model distribuito (DCOM).
ms.assetid: 1917834c-5216-4ef3-a0c2-d8ca63cef53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ad51807e27a9b97e8b05e467d8a84881c3993a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118518"
---
# <a name="dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Miglioramenti della protezione DCOM in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1

Windows Server XP Service Pack 2 (SP2) e Windows Server 2003 Service Pack 1 (SP1) introducono impostazioni di sicurezza predefinite avanzate per il Component Object Model distribuito (DCOM). In particolare, introducono diritti più granulari che consentono a un amministratore di avere un controllo indipendente sulle autorizzazioni locali e remote per l'avvio, l'attivazione e l'accesso ai server COM.

## <a name="what-does-dcom-do"></a>Che cosa fa DCOM?

Microsoft Component Object Model (COM) è un sistema indipendente dalla piattaforma, distribuito e orientato a oggetti per la creazione di componenti software binari in grado di interagire. Il Component Object Model distribuito (DCOM) consente la distribuzione delle applicazioni tra le varie posizioni più sensate per l'utente e l'applicazione. Il protocollo wire DCOM fornisce in modo trasparente supporto per la comunicazione affidabile, sicura ed efficiente tra i componenti COM.

## <a name="who-does-this-feature-apply-to"></a>Destinatari del servizio

Se si utilizza COM solo per i componenti COM in-process, questa funzionalità non si applica all'utente.

Questa funzionalità è applicabile se si dispone di un'applicazione server COM che soddisfa uno dei criteri seguenti:

-   L'autorizzazione di accesso per l'applicazione è meno rigorosa rispetto all'autorizzazione di avvio, necessaria per eseguire l'applicazione.
-   L'applicazione viene in genere attivata da un client COM remoto senza utilizzare un account amministrativo.
-   L'applicazione deve essere usata solo localmente. Ciò significa che è possibile limitare l'applicazione server COM in modo che non sia accessibile in remoto.

## <a name="what-new-functionality-is-added-to-this-feature-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Quali nuove funzionalità sono state aggiunte a questa funzionalità in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1?

### <a name="computer-wide-restrictions"></a>Restrizioni a livello di computer

In COM è stata apportata una modifica per fornire controlli di accesso a livello di computer che regolano l'accesso a tutte le richieste di chiamata, attivazione o avvio nel computer. Il modo più semplice per considerare questi controlli di accesso è costituito da una chiamata [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) aggiuntiva eseguita su un elenco di controllo di accesso (ACL) a livello di computer per ogni chiamata, attivazione o avvio di qualsiasi server com nel computer. Se il **AccessCheck** ha esito negativo, la chiamata, l'attivazione o la richiesta di avvio viene negata. Questa operazione è aggiunta a qualsiasi **AccessCheck** che viene eseguito in base agli ACL specifici del server. In effetti, fornisce uno standard di autorizzazione minimo che deve essere passato per accedere a qualsiasi server COM nel computer. È disponibile un ACL a livello di computer per le autorizzazioni di avvio per coprire i diritti di attivazione e di avvio e un ACL a livello di computer per le autorizzazioni di accesso per coprire i diritti di chiamata. Questi elementi possono essere configurati tramite Microsoft Management Console (MMC) di Servizi componenti.

Questi ACL a livello di computer consentono di eseguire l'override delle impostazioni di sicurezza vulnerabili specificate da un'applicazione specifica tramite [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o impostazioni di sicurezza specifiche dell'applicazione. Questo fornisce uno standard di sicurezza minimo che deve essere passato, indipendentemente dalle impostazioni del server specifico.

Questi ACL vengono controllati quando si accede alle interfacce esposte da RPCSS. Fornisce un metodo per controllare l'accesso a questo servizio di sistema.

Questi ACL forniscono una posizione centralizzata in cui un amministratore può impostare i criteri di autorizzazione generali applicabili a tutti i server COM nel computer.

> [!Note]  
> La modifica delle impostazioni di sicurezza a livello di computer avrà effetto su tutte le applicazioni server COM e potrebbe impedire il corretto funzionamento. Se sono presenti applicazioni server COM con restrizioni meno restrittive rispetto a quelle a livello di computer, la riduzione delle restrizioni a livello di computer potrebbe esporre tali applicazioni a un accesso indesiderato. Viceversa, se si aumentano le restrizioni a livello di computer, alcune applicazioni server COM potrebbero non essere più accessibili chiamando le applicazioni.

 

Per impostazione predefinita, le impostazioni di restrizione del computer Windows XP SP2 sono:



| Autorizzazione        | Amministratore                                                                                             | Tutti                                            | Anonima               |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-------------------------|
| Launch<br/> | Avvio locale<br/> Attivazione locale<br/> Avvio remoto<br/> Attivazione remota<br/> | Avvio locale<br/> Attivazione locale<br/> |                         |
| Access<br/> |                                                                                                           | Accesso locale<br/> Accesso remoto<br/>    | Accesso locale<br/> |



 

Per impostazione predefinita, le impostazioni di restrizione del computer di Windows Server 2003 SP 1 sono le seguenti.



| Autorizzazione        | Amministratore                                                                                             | Utenti COM distribuiti (gruppo incorporato)                                                                    | Tutti                                            | Anonima                                        |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------|
| Launch<br/> | Avvio locale<br/> Attivazione locale<br/> Avvio remoto<br/> Attivazione remota<br/> | Avvio locale<br/> Attivazione locale<br/> Avvio remoto<br/> Attivazione remota<br/> | Avvio locale<br/> Attivazione locale<br/> | N/D<br/>                                   |
| Access<br/> | N/D<br/>                                                                                            | Accesso locale<br/> Accesso remoto<br/>                                                          | Accesso locale<br/> Accesso remoto<br/>    | Accesso locale<br/> Accesso remoto<br/> |



 

> [!Note]  
> Distributed COM Users è un nuovo gruppo incorporato incluso in Windows Server 2003 SP1 per accelerare il processo di aggiunta di utenti alle impostazioni di restrizione del computer DCOM. Questo gruppo fa parte dell'ACL usato dalle impostazioni [MachineAccessRestriction](machineaccessrestriction.md) e [MachineLaunchRestriction](machinelaunchrestriction.md) , quindi la rimozione degli utenti da questo gruppo influirà su tali impostazioni.

 

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Vantaggi della nuova funzionalità e rischi che consente di attenuare

Molte applicazioni COM includono un codice specifico per la sicurezza (ad esempio, la chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)), ma usano impostazioni vulnerabili, consentendo spesso l'accesso non autenticato al processo. Attualmente un amministratore non è in grado di eseguire l'override di queste impostazioni per forzare una sicurezza più avanzata nelle versioni precedenti di Windows.

L'infrastruttura COM include RPCSS, un servizio di sistema che viene eseguito durante l'avvio del sistema ed eseguito sempre successivamente. Gestisce l'attivazione di oggetti COM e la tabella degli oggetti in esecuzione e fornisce servizi helper per la comunicazione remota DCOM. Espone le interfacce RPC che possono essere chiamate in remoto. Poiché alcuni server COM consentono l'accesso remoto non autenticato, queste interfacce possono essere chiamate da chiunque, inclusi gli utenti non autenticati. Di conseguenza, RPCSS può essere aggredito da utenti malintenzionati in computer remoti e non autenticati.

Nelle versioni precedenti di Windows non era possibile per un amministratore comprendere il livello di esposizione dei server COM in un computer. Un amministratore ha avuto un'idea del livello di esposizione controllando sistematicamente le impostazioni di sicurezza configurate per tutte le applicazioni COM registrate nel computer, ma, dato che ci sono circa 150 server COM in un'installazione predefinita di Windows, l'attività era scoraggiante. Non è stato possibile visualizzare le impostazioni per un server che incorpora la sicurezza nel software, a meno di esaminare il codice sorgente per il software.

Le restrizioni a livello di computer DCOM attenuano questi tre problemi. Fornisce inoltre a un amministratore la possibilità di disabilitare l'attivazione, l'avvio e le chiamate DCOM in ingresso.

### <a name="what-works-differently"></a>Differenze di funzionamento

Per impostazione predefinita, al gruppo Everyone vengono concesse le autorizzazioni di avvio locale, attivazione locale e chiamata di accesso locale. Questo consente a tutti gli scenari locali di funzionare senza modifiche al software o al sistema operativo.

Per impostazione predefinita, in Windows XP SP2 al gruppo Everyone vengono concesse le autorizzazioni per le chiamate di accesso remoto. In Windows Server 2003 SP1, a tutti e a gruppi anonimi vengono concesse le autorizzazioni di accesso remoto. Questo consente la maggior parte degli scenari client COM, incluso il caso comune in cui un client COM passa un riferimento locale a un server remoto, attivando in tal modo il client in un server. In Windows XP SP2 questa operazione potrebbe disabilitare scenari che richiedono chiamate di accesso remoto non autenticate.

Inoltre, per impostazione predefinita, solo ai membri del gruppo Administrators vengono concesse le autorizzazioni di attivazione e avvio remote. Questo consente di disabilitare le attivazioni remote da parte degli amministratori non amministratori dei server COM installati.

### <a name="how-do-i-resolve-these-issues"></a>Ricerca per categorie risolvere questi problemi?

Se si implementa un server COM e si prevede di supportare l'attivazione remota da parte di un client non amministrativo COM, è necessario valutare se il rischio associato all'abilitazione di questo processo è accettabile o se è necessario modificare l'implementazione in modo che non richieda l'attivazione remota da parte di un client COM non amministrativo o di chiamate non autenticate remote.

Se il rischio è accettabile e si desidera abilitare l'attivazione remota da un client COM non amministrativo o da chiamate remote non autenticate, è necessario modificare la configurazione predefinita per questa funzionalità.

> [!Note]  
> La modifica delle impostazioni di sicurezza a livello di computer avrà effetto su tutte le applicazioni server COM e potrebbe impedire il corretto funzionamento. Se sono presenti applicazioni server COM con restrizioni meno restrittive rispetto a quelle a livello di computer, la riduzione delle restrizioni a livello di computer può esporre tali applicazioni a accessi non desiderati. Viceversa, se si aumentano le restrizioni a livello di computer, alcune applicazioni server COM potrebbero non essere più accessibili chiamando le applicazioni.

 

È possibile modificare le impostazioni di configurazione utilizzando Microsoft Management Console (MMC) di Servizi componenti o il registro di sistema di Windows.

Se si utilizza lo snap-in MMC Servizi componenti, queste impostazioni possono essere configurate nella scheda **sicurezza com** della finestra di dialogo **Proprietà** del computer che si sta gestendo. L'area **autorizzazioni di accesso** è stata modificata per consentire l'impostazione di limiti a livello di computer oltre alle impostazioni predefinite standard per i server com. Inoltre, è possibile fornire impostazioni ACL separate per l'accesso locale e remoto con limiti e valori predefiniti.

Nell'area **autorizzazioni di avvio e attivazione** è possibile controllare le autorizzazioni locali e remote, nonché i limiti a livello di computer e le impostazioni predefinite. È possibile specificare l'attivazione locale e remota e le autorizzazioni di avvio in modo indipendente.

In alternativa, è possibile configurare queste impostazioni ACL usando il registro di sistema.

Questi ACL vengono archiviati nel registro di sistema nei percorsi seguenti:

``` syntax
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineAccessRestriction=ACL
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineLaunchRestriction=ACL
```

Si tratta di valori denominati di tipo REG \_ Binary che contengono dati che descrivono l'ACL delle entità che possono accedere a qualsiasi classe com o oggetto com nel computer. I diritti di accesso nell'ACL sono:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Questi ACL possono essere creati usando le normali funzioni di sicurezza.

> [!Note]  
> Per garantire la compatibilità con le versioni precedenti, è possibile che esista un ACL nel formato utilizzato prima di Windows XP SP2 e Windows Server 2003 SP1, che utilizza solo l'accesso Rights right COM \_ \_ Execute oppure può esistere nel nuovo formato utilizzato in Windows XP SP2 e windows Server 2003 SP1, che utilizza \_ i diritti com \_ Execute insieme a una combinazione di diritti COM Execute \_ \_ \_ local, com \_ Rights \_ Execute \_ remote, com \_ Rights \_ Activate \_ local e com \_ Rights \_ Activate \_ remote. Si noti che \_ i diritti com \_ Execute> devono essere sempre presenti. l'assenza di questo diritto genera un descrittore di sicurezza non valido. Si noti inoltre che non è necessario combinare il vecchio formato e il nuovo formato all'interno di un singolo ACL. tutte le voci di controllo di accesso (ACE) devono concedere solo \_ il \_ diritto di accesso Execute Rights Execute oppure tutti devono concedere i \_ diritti com \_ Execute insieme a una combinazione di \_ diritti com \_ Execute \_ local, com \_ Rights \_ Execute \_ remote, com \_ Rights \_ Activate \_ local e com \_ Rights \_ Activate \_ remote.

 

> [!Note]  
> Queste impostazioni possono essere modificate solo dagli utenti con diritti di amministratore.

 

## <a name="what-existing-functionality-is-changing-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Quale funzionalità esistente sta cambiando in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1?

### <a name="rpcss-runs-as-a-network-service"></a>RPCSS viene eseguito come servizio di rete

RPCSS è un servizio chiave per il mapper di endpoint RPC e l'infrastruttura DCOM. Questo servizio è stato eseguito come sistema locale nelle versioni precedenti di Windows. Per ridurre la superficie di attacco di Windows e fornire una difesa approfondita, la funzionalità del servizio RPCSS è stata suddivisa in due servizi. Il servizio RPCSS con tutte le funzionalità originali che non richiedevano i privilegi di sistema locale viene ora eseguito con l'account servizio di rete. Un nuovo servizio DCOMLaunch che include funzionalità che richiedono privilegi di sistema locali viene eseguito con l'account di sistema locale.

### <a name="why-is-this-change-important"></a>Vantaggi della nuova funzionalità e

Questa modifica riduce la superficie di attacco e fornisce una difesa in profondità per il servizio RPCSS, perché un'elevazione dei privilegi nel servizio RPCSS è ora limitata al privilegio servizio di rete.

### <a name="what-works-differently"></a>Differenze di funzionamento

Questa modifica dovrebbe essere trasparente per gli utenti perché la combinazione dei servizi RPCSS e DCOMLaunch è equivalente al servizio RPCSS precedente fornito nelle versioni precedenti di Windows.

### <a name="more-specific-com-permissions"></a>Autorizzazioni COM più specifiche

Le applicazioni server COM hanno due tipi di autorizzazioni: autorizzazioni di avvio e autorizzazioni di accesso. Avviare le autorizzazioni per controllare l'autorizzazione per avviare un server COM durante l'attivazione COM se il server non è già in esecuzione. Queste autorizzazioni sono definite come descrittori di sicurezza specificati nelle impostazioni del registro di sistema. Le autorizzazioni di accesso controllano l'autorizzazione per chiamare un server COM in esecuzione. Queste autorizzazioni sono definite come descrittori di sicurezza forniti all'infrastruttura COM tramite l'API [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o tramite le impostazioni del registro di sistema. Le autorizzazioni di avvio e di accesso consentono o negano l'accesso in base alle entità e non fanno distinzione se il chiamante è locale al server o remoto.

La prima modifica distingue i diritti di accesso COM, in base alla distanza. Le due distanze definite sono locale e remota. Un messaggio COM locale arriva tramite il protocollo LRPC (Remote Procedure Call) locale, mentre un messaggio COM remoto arriva tramite un protocollo host RPC (Remote Procedure Call) come TCP (Transmission Control Protocol).

L'attivazione COM è l'operazione di recupero di un proxy di interfaccia COM su un client chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o una delle relative varianti. Come effetto collaterale di questo processo di attivazione, a volte è necessario avviare un server COM per soddisfare la richiesta del client. Un ACL per le autorizzazioni di avvio dichiara l'utente autorizzato ad avviare un server COM. Un ACL per le autorizzazioni di accesso dichiara che può attivare un oggetto COM o chiamare tale oggetto quando il server COM è già in esecuzione.

La seconda modifica è che i diritti di chiamata e di attivazione sono separati per riflettere due operazioni distinte e per spostare il diritto di attivazione dall'ACL delle autorizzazioni di accesso all'ACL dell'autorizzazione di avvio. Poiché l'attivazione e l'avvio sono entrambi correlati all'acquisizione di un puntatore a interfaccia, i diritti di accesso di attivazione e avvio sono logicamente inclusi in un ACL. E poiché si specificano sempre le autorizzazioni di avvio tramite la configurazione (rispetto alle autorizzazioni di accesso, che vengono spesso specificate a livello di codice), l'inserimento dei diritti di attivazione nell'ACL dell'autorizzazione Launch consente all'amministratore di controllare l'attivazione.

Le voci di controllo di accesso (ACE) autorizzazione di avvio sono suddivise in quattro diritti di accesso:

-   Avvio locale (LL)
-   Avvio remoto (RL)
-   Attivazione locale (LA)
-   Attivazione remota (RA)

Il descrittore di sicurezza delle autorizzazioni di accesso è suddiviso in due diritti di accesso:

-   Chiamate di accesso locale (LC)
-   Chiamate di accesso remoto (RC)

Questo consente all'amministratore di applicare configurazioni di sicurezza molto specifiche. Ad esempio, è possibile configurare un server COM in modo che accetti le chiamate di accesso locale da tutti, accettando solo le chiamate di accesso remoto da parte degli amministratori. Queste distinzioni possono essere specificate tramite modifiche ai descrittori di sicurezza delle autorizzazioni COM.

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Vantaggi della nuova funzionalità e rischi che consente di attenuare

Le versioni precedenti dell'applicazione server COM non hanno alcun modo per limitare un'applicazione in modo che possa essere usata solo localmente senza esporre l'applicazione in rete mediante DCOM. Quando un utente ha accesso a un'applicazione server COM, può accedere sia a un uso locale che remoto.

Un'applicazione server COM potrebbe esporsi a utenti non autenticati per implementare uno scenario di callback COM. In questo scenario, l'applicazione deve esporre anche l'attivazione a utenti non autenticati, che potrebbero non essere auspicabili.

Le autorizzazioni COM precise forniscono flessibilità all'amministratore per controllare i criteri di autorizzazione COM di un computer. Queste autorizzazioni abilitano la sicurezza per gli scenari descritti.

### <a name="what-works-differently-are-there-any-dependencies"></a>Differenze di funzionamento Sono presenti dipendenze?

Per garantire la compatibilità con le versioni precedenti, i descrittori di sicurezza COM esistenti vengono interpretati per consentire o negare l'accesso sia locale che remoto simultaneamente. Ovvero una voce di controllo di accesso (ACE) consente sia locale che remoto oppure nega sia locale che remota.

Non esistono problemi di compatibilità con le versioni precedenti per i diritti di chiamata o avvio. Esiste tuttavia un problema di compatibilità dei diritti di attivazione. Se, nei descrittori di sicurezza esistenti per un server COM, le autorizzazioni di avvio configurate sono più restrittive rispetto alle autorizzazioni di accesso e sono più restrittive rispetto a quelle minime necessarie per gli scenari di attivazione client, è necessario modificare l'ACL delle autorizzazioni di avvio per concedere ai client autorizzati le autorizzazioni di attivazione appropriate.

Per le applicazioni COM che usano le impostazioni di sicurezza predefinite, non ci sono problemi di compatibilità. Per le applicazioni avviate dinamicamente con l'attivazione COM, la maggior parte non presenta problemi di compatibilità, perché le autorizzazioni di avvio devono includere già chiunque sia in grado di attivare un oggetto. In caso contrario, tali applicazioni generano errori di attivazione anche prima di applicare Windows XP SP2 o Windows Server 2003 SP1, quando i chiamanti senza autorizzazione Launch tentano di attivare un oggetto e il server COM non è già in esecuzione.

Le applicazioni più problematiche per i problemi di compatibilità sono le applicazioni COM già avviate da un altro meccanismo, ad esempio Esplora risorse o Gestione controllo servizi. È anche possibile avviare queste applicazioni mediante un'attivazione COM precedente, che sostituisce le autorizzazioni di accesso e di avvio predefinite e specifica le autorizzazioni di avvio più restrittive rispetto alle autorizzazioni di chiamata. Per ulteriori informazioni sulla risoluzione di questo problema di compatibilità, vedere "Ricerca per categorie risolvere questi problemi". nella sezione successiva.

Se viene eseguito il rollback di un sistema aggiornato a Windows XP SP2 o Windows Server 2003 SP1 a uno stato precedente, qualsiasi voce ACE modificata per consentire l'accesso locale, l'accesso remoto o entrambi viene interpretata in modo da consentire l'accesso locale e remoto. Qualsiasi voce ACE modificata per negare l'accesso locale, l'accesso remoto o entrambe le voci viene interpretata per negare l'accesso sia locale che remoto. Quando si disinstalla una Service Pack, è necessario assicurarsi che nessuna ACE appena impostata provochi l'arresto del funzionamento delle applicazioni.

### <a name="how-do-i-resolve-these-issues"></a>Ricerca per categorie risolvere questi problemi?

Se si implementa un server COM e si sostituiscono le impostazioni di sicurezza predefinite, verificare che l'ACL delle autorizzazioni di avvio specifico dell'applicazione conceda l'autorizzazione di attivazione agli utenti appropriati. In caso contrario, è necessario modificare l'ACL dell'autorizzazione di avvio specifico dell'applicazione per concedere diritti di attivazione agli utenti appropriati, in modo che le applicazioni e i componenti di Windows che utilizzano DCOM non abbiano esito negativo. Queste autorizzazioni di avvio specifiche dell'applicazione vengono archiviate nel registro di sistema.

Gli ACL COM possono essere creati o modificati usando le normali funzioni di sicurezza.

## <a name="what-settings-are-added-or-changed-in-windows-xp-service-pack-2"></a>Quali impostazioni sono state aggiunte o modificate in Windows XP Service Pack 2?

> [!Caution]  
> Un utilizzo non corretto di queste impostazioni può causare errori nelle applicazioni e nei componenti di Windows che utilizzano DCOM.

 

Nella tabella seguente vengono usate queste abbreviazioni:

LL-avvio locale

Attivazione locale

RL-avvio remoto

RA-attivazione remota

LC-chiamate di accesso locale

RC-chiamate di accesso remoto

Elenco di controllo di accesso ACL



| Nome impostazione                                                                                         | Location                                                                                                       | Valore predefinito precedente                                                                                                                                                                     | Valore predefinito                                                                                                                                                                                                                                                                                                                                                             | Valori possibili                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**<br/>                                                 | Everyone-LL, LA, RL, RA<br/> Anonimo<br/> LL, LA, RL, RA<br/> Si tratta di una nuova chiave del registro di sistema. In base al comportamento esistente, questi sono i valori effettivi.<br/> | Amministratore: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**<br/>                                                 | Tutti-LC, RC<br/> Anonimo-LC, RC<br/> Si tratta di una nuova chiave del registro di sistema. In base al comportamento esistente, questi sono i valori effettivi.<br/>                            | Tutti: LC, RC<br/> Anonimo: LC<br/>                                                                                                                                                                                                                                                                                                                      | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**<br/>                                                 | Non applicabile.<br/>                                                                                                                                                                 | Questa chiave del registro di sistema non è presente. Tuttavia, una chiave o un valore mancante viene interpretato come 2.<br/> Questo evento non viene registrato per impostazione predefinita. Se si imposta questo valore su 1 per avviare la registrazione di queste informazioni per facilitare la risoluzione di un problema, assicurarsi di monitorare le dimensioni del log eventi, perché si tratta di un evento che può generare un numero elevato di voci.<br/> | 1: registra sempre gli errori del log eventi durante una chiamata nel processo del server COM.<br/> 2: non registra mai errori nel registro eventi durante una chiamata nel processo del server di chiamata.<br/>                                                  |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**<br/>                                                 | Non applicabile.<br/>                                                                                                                                                                 | Questa chiave del registro di sistema non è presente. Tuttavia, una chiave o un valore mancante viene interpretato come 1.<br/> Questo evento viene registrato per impostazione predefinita. Questa situazione si verifica raramente.<br/>                                                                                                                                                                                                    | 1: registra sempre gli errori del log eventi quando l'infrastruttura COM trova un descrittore di sicurezza non valido.<br/> 2: non registra mai errori nel registro eventi quando l'infrastruttura COM trova un descrittore di sicurezza non valido.<br/> |
| DCOM: restrizioni di avvio del computer nella sintassi Security Descriptor Definition Language (SDDL)<br/> | (Oggetto Criteri di gruppo) Configurazione computer \\ Opzioni di Windows impostazioni di \\ sicurezza Criteri locali \\<br/>  | Non applicabile.<br/>                                                                                                                                                                 | Non definito<br/>                                                                                                                                                                                                                                                                                                                                                    | Elenco di controllo di accesso in formato SDDL. L'esistenza di questo criterio sostituisce i valori in MachineLaunchRestriction, in precedenza.<br/>                                                                                            |
| DCOM: restrizioni per l'accesso al computer nella sintassi Security Descriptor Definition Language (SDDL)<br/> | (Oggetto Criteri di gruppo) Configurazione computer \\ Opzioni di Windows impostazioni di \\ sicurezza Criteri locali \\<br/> | Non applicabile.<br/>                                                                                                                                                                 | Non definito<br/>                                                                                                                                                                                                                                                                                                                                                    | Elenco di controllo di accesso in formato SDDL. L'esistenza di questo criterio sostituisce i valori in MachineAccessRestriction, in precedenza.<br/>                                                                                            |



 

## <a name="what-settings-are-added-or-changed-in-windows-server-2003-service-pack-1"></a>Impostazioni aggiunte o modificate in Windows Server 2003 Service Pack 1

> [!Note]  
> Un utilizzo non corretto di queste impostazioni può causare errori nelle applicazioni e nei componenti di Windows che utilizzano DCOM.

 

Nella tabella seguente vengono usate queste abbreviazioni:

LL-avvio locale

Attivazione locale

RL-avvio remoto

RA-attivazione remota

LC-chiamate di accesso locale

RC-chiamate di accesso remoto

Elenco di controllo di accesso ACL



| Nome impostazione                                                                                         | Location                                                                                                       | Valore predefinito precedente                                                                                                                                                             | Valore predefinito                                                                                                                                                                                                                                                                                                                                                             | Valori possibili                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**<br/>                                                 | Tutti: LL, LA, RL, RA<br/> Anonimo: LL, LA, RL, RA<br/> Si tratta di una nuova chiave del registro di sistema. In base al comportamento esistente, questi sono i valori effettivi.<br/> | Amministratore: LL, LA, RL, RA<br/> Tutti: LL, LA<br/> Utenti COM distribuiti: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                     | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**<br/>                                                 | Tutti: LC, RC<br/> Anonimo: LC, RC<br/> Si tratta di una nuova chiave del registro di sistema. In base al comportamento esistente, questi sono i valori effettivi.<br/>                 | Tutti: LC, RC<br/> Anonimo: LC, RC<br/>                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**<br/>                                                 | Non applicabile.<br/>                                                                                                                                                         | Questa chiave del registro di sistema non è presente. Tuttavia, una chiave o un valore mancante viene interpretato come 2.<br/> Questo evento non viene registrato per impostazione predefinita. Se si imposta questo valore su 1 per avviare la registrazione di queste informazioni per facilitare la risoluzione di un problema, assicurarsi di monitorare le dimensioni del log eventi, perché si tratta di un evento che può generare un numero elevato di voci.<br/> | 1: registra sempre gli errori del log eventi quando l'infrastruttura COM trova un descrittore di sicurezza non valido.<br/> 2: non registra mai errori nel registro eventi quando l'infrastruttura COM trova un descrittore di sicurezza non valido.<br/> |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**<br/>                                                 | Non applicabile.<br/>                                                                                                                                                         | Questa chiave del registro di sistema non è presente. Tuttavia, una chiave o un valore mancante viene interpretato come 1.<br/> Questo evento viene registrato per impostazione predefinita. Questa situazione si verifica raramente.<br/>                                                                                                                                                                                                    | 1: registra sempre gli errori del log eventi quando l'infrastruttura COM trova un descrittore di sicurezza non valido.<br/> 2: non registra mai errori nel registro eventi quando l'infrastruttura COM trova un descrittore di sicurezza non valido.<br/>         |
| DCOM: restrizioni di avvio del computer nella sintassi Security Descriptor Definition Language (SDDL)<br/> | (Oggetto Criteri di gruppo) Configurazione computer \\ Opzioni di Windows impostazioni di \\ sicurezza Criteri locali \\<br/> | Non applicabile.<br/>                                                                                                                                                         | Non definito.<br/>                                                                                                                                                                                                                                                                                                                                                   | Elenco di controllo di accesso in formato SDDL. L'esistenza di questo criterio sostituisce i valori in MachineLaunchRestriction, in precedenza.<br/>                                                                                            |
| DCOM: restrizioni per l'accesso al computer nella sintassi Security Descriptor Definition Language (SDDL)<br/> | (Oggetto Criteri di gruppo) Configurazione computer \\ Opzioni di Windows impostazioni di \\ sicurezza Criteri locali \\<br/> | Non applicabile.<br/>                                                                                                                                                         | Non definito.<br/>                                                                                                                                                                                                                                                                                                                                                   | Elenco di controllo di accesso in formato SDDL. L'esistenza di questo criterio sostituisce i valori in MachineAccessRestriction, in precedenza.<br/>                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

