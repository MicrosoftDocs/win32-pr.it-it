---
title: Applicazione di patch al software di gioco in Windows XP, Windows Vista e Windows 7
description: In questo articolo vengono esaminati alcuni metodi di applicazione delle patch che funzionano bene in Windows Vista e Windows 7, oltre che in Windows XP.
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ae0b1455cae61b8372f81e6928977743084c9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300046"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>Applicazione di patch al software di gioco in Windows XP, Windows Vista e Windows 7

Windows Vista e Windows 7 includono diverse funzionalità per rendere più sicuro il sistema operativo. Una maggiore sicurezza significa che l'applicazione di patch al software non è così semplice come in passato. In questo articolo vengono esaminati alcuni metodi di applicazione delle patch che funzionano bene in Windows Vista e Windows 7, oltre che in Windows XP.

Esistono due categorie principali di giochi che richiedono patch:

-   Giochi che richiedono solo patch occasionali, come la maggior parte dei giochi offline.
-   Giochi che richiedono patch frequenti, ad esempio la maggior parte dei giochi online.

In questo articolo viene inoltre offerta una breve introduzione al controllo dell'account utente (UAC) per fornire informazioni di base sui diritti che gli sviluppatori possono prevedere per gli utenti in Windows Vista e Windows 7.

-   [Controllo dell'account utente](#user-account-control)
-   [Giochi che richiedono solo patch occasionali](#games-that-require-only-occasional-patches)
    -   [Metodo 1: usare Windows Installer per le patch occasionali](#method-1-use-windows-installer-for-occasional-patches)
    -   [Metodo 2: richiedere i diritti di amministratore per l'applicazione di patch](#method-2-require-administrator-rights-to-apply-patches)
-   [Giochi che richiedono patch frequenti](#games-that-require-frequent-patches)
    -   [Metodo 3: installare per utente](#method-3-install-per-user)
    -   [Metodo 4: eseguire l'installazione in un percorso di Per-Computer comune](#method-4-install-to-a-common-per-computer-location)
    -   [Altre possibilità](#other-possibilities)
-   [Summary](#summary)

## <a name="user-account-control"></a>Controllo dell'account utente

Windows Vista e Windows 7 hanno due tipi principali di account utente: utente standard e amministratore. Un account utente standard presenta diverse restrizioni di accesso. ad esempio, non è in grado di scrivere dati nel file system in% SystemDrive% \\ Program Files o nel registro di sistema \_ nel \_ computer locale HKEY. Ciò implica l'applicazione di patch a un gioco se viene installato in un percorso di sola lettura. Diversamente da Windows XP, l'account utente standard è molto più comune in Windows Vista e Windows 7. Gli account utente standard sono necessari anche per le funzionalità importanti del sistema operativo, ad esempio i controlli padre. Per i controlli padre è necessario che l'account figlio sia un utente standard e l'elevazione di un account di questo tipo a un amministratore per anche un gioco impedisce ai controlli padre di lavorare con tutti gli altri giochi. Pertanto, è importante che i giochi siano progettati per gli utenti standard.

Windows Vista e Windows 7 hanno un modello più recente per i diritti utente, per evitare che gli utenti eseguano programmi che tentano di eseguire operazioni che l'utente non intende né autorizzare. A tale scopo, il controllo dell'account utente (denominato in precedenza account utente con privilegi minimi o LUA) consente agli utenti di utilizzare la maggior parte del tempo nel computer con diritti di basso livello, pur essendo in grado di eseguire facilmente applicazioni che richiedono diritti di livello superiore, quando necessario. Questo significa che gli account utente standard e gli account amministratore eseguono entrambe le applicazioni con diritti utente standard, ma solo gli account amministratore hanno la possibilità di concedere diritti elevati per le applicazioni. Il sistema operativo chiede agli utenti con account di amministratore il consenso esplicito prima di eseguire un'applicazione con diritti elevati e se un programma che richiede diritti di amministratore viene eseguito su un account utente standard, il sistema richiede l'approvazione dell'amministratore.

## <a name="games-that-require-only-occasional-patches"></a>Giochi che richiedono solo patch occasionali

Alcuni giochi richiedono solo alcune patch per tutto il ciclo di vita. Due metodi che è possibile utilizzare per questa frequenza di applicazione di patch sono la distribuzione di patch come Windows Installer pacchetti, che in genere non richiedono diritti di amministratore o l'utilizzo di un altro tipo di distribuzione che modifica direttamente i file di gioco.

> [!Note]  
> Indipendentemente dal fatto che un gioco richieda l'applicazione di patch frequenti, le applicazioni in genere richiedono l'installazione o la rimozione di diritti di amministratore.

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>Metodo 1: usare Windows Installer per le patch occasionali

In questo metodo, viene utilizzato un Windows Installer per installare un pacchetto (file con estensione msi) e viene distribuita una patch Windows Installer (file con estensione msp) per l'installazione di patch. Il pacchetto deve avere una tabella MsiPatchCertificate e la patch deve essere firmata digitalmente da un certificato nella tabella. Altre informazioni sulla firma digitale sono disponibili in [firma Authenticode per sviluppatori di giochi](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Per informazioni dettagliate e requisiti per l'uso di questo metodo di applicazione di patch, vedere la documentazione Windows Installer:

-   [Applicazione di patch e aggiornamenti](/windows/desktop/Msi/patching-and-upgrades)
-   [Applicazione di patch al controllo dell'account utente (UAC)](/windows/desktop/Msi/user-account-control--uac--patching)

Lo svantaggio di questo metodo è che se il gioco non è stato installato da supporti rimovibili in Windows XP, l'applicazione di patch richiede i diritti di amministratore. Tuttavia, questo non è probabilmente troppo restrittivo, perché la maggior parte degli amministratori di utenti in Windows XP e la restrizione del software installato da supporti rimovibili non è presente in Windows Vista.

Il vantaggio principale di questo metodo è che le patch possono essere applicate da un account utente standard senza richiedere una richiesta di autenticazione per i diritti elevati. Questo garantisce un'esperienza utente migliore, perché per riprodurre un gioco, un utente con un account utente standard non deve chiedere a un utente con un account amministratore di installare la patch o fornire l'account utente standard con diritti di amministratore permanenti.

È possibile che questo metodo possa funzionare per i giochi che richiedono patch frequenti, ma il sovraccarico dell'uso di pacchetti di Windows Installer, in termini di integrazione della compilazione e supporto di un numero elevato di file, potrebbe rendere questo metodo meno auspicabile rispetto ad altri.

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>Metodo 2: richiedere i diritti di amministratore per l'applicazione di patch

In questo metodo, il file eseguibile che applica la patch richiede i diritti di amministratore per l'esecuzione. Con i diritti di amministratore, l'eseguibile di patch può modificare direttamente i file di gioco presenti in% SystemDrive% \\ Program Files.

Il vantaggio di questo metodo è la sua semplicità. Tuttavia, questo metodo non è adatto se il gioco richiede patch frequenti, perché se un utente con un account utente standard vuole riprodurre un gioco che richiede patch frequenti, ad esempio un gioco in linea a più giocatori, l'utente ha due opzioni:

-   Chiedere a un amministratore di accedere e applicare patch al gioco, il che potrebbe non essere utile per entrambe le parti.
-   Disporre di un account con diritti di amministratore elevato in modo permanente.

> [!Note]  
> Quest'ultima soluzione non solo indebolisce la sicurezza del sistema nel suo complesso, ma impedisce il funzionamento di importanti funzionalità, ad esempio i controlli padre.

 

Quando si implementa questo metodo, il file eseguibile che applica la patch deve essere diverso dall'eseguibile del gioco. Il manifesto dell'eseguibile per l'applicazione di patch deve specificare requireAdministrator per requestedExecutionLevel per identificarlo come un'applicazione che richiede diritti di amministratore. Ulteriori informazioni su come eseguire questa operazione sono disponibili in procedure consigliate [e linee guida per gli sviluppatori per le applicazioni in un ambiente con privilegi minimi](/previous-versions/dotnet/articles/aa480150(v=msdn.10)), in "schema del manifesto dell'applicazione".

Quando si usa questo metodo, anche con le impostazioni nel manifesto, il file eseguibile potrebbe essere ancora avviato senza diritti di amministratore in due casi:

-   Se il sistema operativo è Windows XP, l'account dell'utente è un utente con restrizioni.
-   Se il sistema operativo è Windows Vista o Windows 7, l'account dell'utente è un utente standard e il controllo dell'account utente è disabilitato.

Entrambi sono rari scenari consumer. Tuttavia, il patcher deve avere il manifesto che richiede diritti di amministratore e deve chiamare [**IsUserAnAdmin**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin); Se questa funzione restituisce FALSE, viene visualizzato il messaggio di errore "diritti di amministratore sono necessari".

Nel complesso, il metodo 1 è preferibile per i giochi che necessitano solo di alcune patch per la loro durata.

## <a name="games-that-require-frequent-patches"></a>Giochi che richiedono patch frequenti

Molti giochi basati su Internet sono stati migliorati continuamente e in genere richiedono patch regolari. Per questi giochi, le patch possono essere applicate per utente o per computer, come illustrato negli argomenti seguenti. Altre soluzioni possibili includono la modifica dell'ACL che protegge% SystemDrive% dei \\ file di programma o la creazione di un servizio personalizzato.

### <a name="method-3-install-per-user"></a>Metodo 3: installare Per-User

Un approccio consigliato e semplice consiste nell'installare l'intero gioco in una sottocartella per singolo utente della cartella Local Application Data, che è possibile trovare chiamando [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL \_ Local \_ AppData. Un percorso di esempio è C: \\ Documents and Settings \\ nome utente impostazioni \\ locali \\ dati applicazione \\ ExampleGame. Tale percorso consente a un'applicazione in esecuzione con diritti utente standard di modificare direttamente i file di gioco.

Tuttavia, esiste uno svantaggio di questo approccio quando un computer ha più utenti: ogni utente ha una copia del gioco installato e le patch devono essere scaricate e applicate da ogni utente. Questo consente di sprecare non solo i tempi e lo spazio su disco degli utenti, ma aumenta anche l'utilizzo della larghezza di banda di rete per il server che fornisce patch. Inoltre, poiché qualsiasi applicazione con diritti utente standard può modificare il gioco, gli eseguibili del gioco sono meno protetti. il produttore del gioco decide se è accettabile o meno.

### <a name="method-4-install-to-a-common-per-computer-location"></a>Metodo 4: eseguire l'installazione in un percorso di Per-Computer comune

Un altro metodo consiste nell'installare i dati del gioco non eseguibili in una sottodirectory del percorso specificato da [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL \_ Common \_ AppData; un percorso di esempio è C: \\ Documents and Settings \\ All Users \\ Application Data \\ ExampleGame. Si tratta di un percorso condiviso per tutti gli utenti e può essere modificato da applicazioni che vengono eseguite con diritti utente standard. Questo metodo riduce al minimo la necessità di riapplicare le patch di grandi dimensioni quando il gioco viene riprodotto da più di un account. I file eseguibili per il gioco devono essere conservati nei file% SystemDrive% \\ Programs per ridurre al minimo il rischio di altri account nel sistema. I file eseguibili devono verificare l'integrità del nuovo contenuto nella directory condivisa, perché tale percorso può essere modificato da un programma o da una persona con diritti utente standard. prendere in considerazione l'uso di [**MapFileAndCheckSum**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) per calcolare un checksum dei file.

Questo metodo ha il vantaggio di funzionare ugualmente correttamente sia in Windows XP che in Windows Vista e non richiede diritti di amministratore.

### <a name="other-possibilities"></a>Altre possibilità

Al di fuori dei metodi già illustrati, un'altra possibilità consiste nel modificare l'ACL della cartella% SystemDrive% \\ Program Files \\ Game \\ durante l'installazione del gioco, in modo che uno strumento di patch possa scrivere direttamente nei file del gioco anche quando viene eseguito con diritti utente standard. Sebbene questo non sia difficile, ignora la protezione della sicurezza offerta dal sistema ai file del gioco e consente ai programmi dannosi di modificare il contenuto della directory. Questa operazione non è consigliata ed è consigliabile usare invece un'alternativa.

Una possibilità finale consiste nel scrivere un servizio personalizzato. In generale, non è consigliabile scrivere un servizio personalizzato per applicare patch ai giochi, perché questa operazione è complessa e soggetta a errori. Si consiglia di eseguire l'applicazione di patch usando altri metodi descritti in questo articolo. Tuttavia, un servizio personalizzato potrebbe essere necessario in combinazione con soluzioni anti-cheat o anti-pirateria. Un servizio di questo tipo deve supportare un numero elevato di giochi ed essere progettato in modo da poter scaricare solo i file di patch e scrivere solo nella directory di installazione per il gioco di destinazione. È importante che il servizio sia di piccole dimensioni, disponga di una superficie di attacco minima vulnerabile agli attacchi e usi il minor numero possibile di risorse di sistema quando il gioco non è in esecuzione.

## <a name="summary"></a>Riepilogo

Infine, è responsabilità dell'utente decidere quale metodo implementare. È necessario valutare i fattori che sono importanti per l'utente. Sicurezza, frequenza delle patch, facilità d'uso da parte dei clienti, carico di lavoro richiesto per implementare, complessità della soluzione e conformità delle funzionalità della piattaforma sono i fattori che ogni sviluppatore deve considerare prima di decidere su un particolare metodo.

Per ulteriori informazioni sulla protezione dell'account utente, vedere [requisiti di sviluppo delle applicazioni di Windows Vista per controllo dell'account utente (UAC)](/previous-versions/aa905330(v=msdn.10)).

 

 