---
title: Applicazione di patch al software di gioco in Windows XP, Windows Vista e Windows 7
description: Questo articolo esamina alcuni metodi di applicazione di patch che funzionano bene in Windows Vista e Windows 7, nonché Windows XP.
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dae9b3bc91c96006f3b2117093962ee485db948fd983191f2db3c7f88fb33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042501"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>Applicazione di patch al software di gioco in Windows XP, Windows Vista e Windows 7

Windows Vista e Windows 7 hanno una serie di funzionalità per rendere il sistema operativo più sicuro. La sicurezza aggiunta significa che l'applicazione di patch al software non è semplice come in passato. Questo articolo esamina alcuni metodi di applicazione di patch che funzionano bene in Windows Vista e Windows 7, nonché Windows XP.

Esistono due categorie principali di giochi che richiedono patch:

-   Giochi che richiedono solo patch occasionali, ad esempio la maggior parte dei giochi offline.
-   Giochi che richiedono patch frequenti, ad esempio la maggior parte dei giochi online.

Questo articolo offre anche una breve introduzione al controllo dell'account utente per fungere da sfondo sui diritti che gli sviluppatori possono aspettarsi che gli utenti di Windows Vista e Windows 7.

-   [Controllo dell'account utente](#user-account-control)
-   [Giochi che richiedono solo patch occasionali](#games-that-require-only-occasional-patches)
    -   [Metodo 1: Usare il Windows per patch occasionali](#method-1-use-windows-installer-for-occasional-patches)
    -   [Metodo 2: Richiedere i diritti di amministratore per applicare le patch](#method-2-require-administrator-rights-to-apply-patches)
-   [Giochi che richiedono patch frequenti](#games-that-require-frequent-patches)
    -   [Metodo 3: Installare per utente](#method-3-install-per-user)
    -   [Metodo 4: Installare in un percorso Per-Computer comune](#method-4-install-to-a-common-per-computer-location)
    -   [Altre possibilità](#other-possibilities)
-   [Summary](#summary)

## <a name="user-account-control"></a>Controllo dell'account utente

Windows Vista e Windows 7 hanno due tipi principali di account utente: Utente standard e Amministratore. Un account utente Standard ha diverse restrizioni di accesso. Ad esempio, non può scrivere dati nel file system in %SystemDrive% Programmi o nel Registro \\ di sistema nella chiave \_ HKEY LOCAL \_ MACHINE. Ciò ha implicazioni per l'applicazione di patch a un gioco se è installato in un percorso di sola lettura. A differenza di Windows XP, l'account utente Standard è molto più comune in Windows Vista e Windows 7. Gli account utente standard sono necessari anche per importanti funzionalità del sistema operativo, ad esempio il controllo genitori. Controllo genitori richiede che l'account figlio sia Utente Standard e l'elevazione di tale account all'amministratore per un solo gioco impedisce a Controllo genitori di lavorare con tutti gli altri giochi. È quindi importante che i giochi siano progettati per l'utente standard.

Windows Vista e Windows 7 hanno un modello più recente per i diritti utente, per impedire agli utenti di eseguire programmi che tentano di eseguire operazioni che l'utente non intende o autorizza. A tale scopo, controllo dell'account utente (in precedenza denominato account utente con privilegi minimi o LUA) consente agli utenti di operare il computer con diritti di basso livello la maggior parte del tempo, pur essendo in grado di eseguire facilmente applicazioni che richiedono diritti di livello superiore, quando necessario. Ciò significa che gli account utente Standard e gli account amministratore eseguono entrambe le applicazioni con diritti utente Standard, ma solo gli account amministratore hanno la possibilità di concedere diritti elevati alle applicazioni. Il sistema operativo chiede agli utenti con account amministratore il consenso esplicito prima di eseguire un'applicazione con diritti elevati e se un programma che richiede diritti di amministratore viene eseguito in un account utente standard, il sistema richiede l'approvazione dell'amministratore.

## <a name="games-that-require-only-occasional-patches"></a>Giochi che richiedono solo patch occasionali

Alcuni giochi richiedono solo alcune patch per tutto il ciclo di vita. Due metodi che è possibile usare per questa frequenza di applicazione delle patch sono la distribuzione di patch come pacchetti del programma di installazione di Windows, che in genere non richiedono diritti di amministratore, o l'uso di un altro tipo di distribuzione che modifica direttamente i file di gioco.

> [!Note]  
> Indipendentemente dal fatto che un gioco richieda frequenti patch, le applicazioni richiedono in genere diritti di amministratore per essere installate o rimosse.

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>Metodo 1: Usare il Windows per patch occasionali

In questo metodo viene usato Windows Installer per installare un pacchetto (file .msi) e viene distribuita una patch Windows Installer (file con estensione msp) per installare le patch. Il pacchetto deve avere una tabella MsiPatchCertificate e la patch deve essere firmata digitalmente da un certificato nella tabella. Altre informazioni sulla firma digitale sono disponibili in [Firma Authenticode per sviluppatori di giochi.](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

Altri dettagli e requisiti per l'uso di questo metodo di applicazione delle patch sono disponibili nella documentazione Windows Installer:

-   [Applicazione di patch e aggiornamenti](/windows/desktop/Msi/patching-and-upgrades)
-   [Applicazione di patch al controllo dell'account utente](/windows/desktop/Msi/user-account-control--uac--patching)

Lo svantaggio di questo metodo è che se il gioco non è stato installato da supporti rimovibili in Windows XP, l'applicazione di patch richiede diritti di amministratore. Tuttavia, questo non è probabilmente troppo restrittivo, perché la maggior parte degli amministratori degli utenti in Windows XP e la restrizione al software installato da supporti rimovibili non è presente in Windows Vista.

Il vantaggio principale di questo metodo è che le patch possono essere applicate da un account utente Standard senza richiedere una richiesta e l'autenticazione per i diritti elevati. Ciò offre un'esperienza utente migliore, perché per riprodurre un gioco, un utente con un account utente Standard non deve chiedere a un utente con un account amministratore di installare la patch o di fornire all'account utente Standard diritti di amministratore permanenti.

È possibile che questo metodo funzioni per i giochi che richiedono patch frequenti, ma il sovraccarico dell'uso dei pacchetti del programma di installazione di Windows, in termini di integrazione della compilazione e supporto di un numero elevato di file, potrebbe rendere questo metodo meno desiderabile rispetto ad altri.

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>Metodo 2: Richiedere i diritti di amministratore per applicare le patch

In questo metodo, il file eseguibile che applica la patch richiede diritti di amministratore per l'esecuzione. Con i diritti di amministratore, il file eseguibile di applicazione delle patch può modificare direttamente i file di gioco che si trovano in %SystemDrive% \\ Programmi.

Il vantaggio di questo metodo è la semplicità. Tuttavia, questo metodo non è adatto se il gioco richiede patch frequenti, perché se un utente con un account utente Standard vuole eseguire un gioco che richiede patch frequenti, ad esempio un gioco online con più giocatori, l'utente ha due opzioni:

-   Richiedere a un amministratore di accedere e applicare patch al gioco, che potrebbe essere poco pratico per entrambe le parti.
-   Avere un account con privilegi elevati in modo permanente con diritti di amministratore.

> [!Note]  
> Quest'ultima soluzione non solo attenua la sicurezza del sistema nel suo complesso, ma impedisce il funzionamento di funzionalità importanti, come il controllo genitori.

 

Quando si implementa questo metodo, il file eseguibile che applica la patch deve essere diverso dall'eseguibile del gioco. Il manifesto dell'eseguibile di applicazione delle patch deve specificare requireAdministrator per requestedExecutionLevel per indicarlo come un'applicazione che richiede diritti di amministratore. Altre informazioni su come eseguire questa operazione sono disponibili in Procedure consigliate per gli sviluppatori e linee guida per le applicazioni [in](/previous-versions/dotnet/articles/aa480150(v=msdn.10))un ambiente con privilegi minimi in "Schema manifesto dell'applicazione".

Quando si usa questo metodo, anche con le impostazioni nel manifesto, il file eseguibile potrebbe comunque essere avviato senza diritti di amministratore in due casi:

-   Se il sistema operativo è Windows XP e l'account dell'utente è un utente con restrizioni.
-   Se il sistema operativo è Windows Vista o Windows 7, l'account dell'utente è un utente standard e il controllo dell'account utente è disabilitato.

Entrambi questi scenari sono rari per i consumer. Tuttavia, il patcher deve avere il manifesto che richiede diritti di amministratore e deve chiamare [**IsUserAnAdmin**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin). se questa funzione restituisce FALSE, viene visualizzato il messaggio di errore "Sono necessari diritti di amministratore".

In generale, il metodo 1 è preferibile per i giochi che necessitano di poche patch nel corso della loro durata.

## <a name="games-that-require-frequent-patches"></a>Giochi che richiedono patch frequenti

Molti giochi basati su Internet vengono migliorati in modo continuo e in genere richiedono patch regolari. Per questi giochi, è possibile applicare patch per utente o per computer, come descritto negli argomenti seguenti. Altre soluzioni possibili includono la modifica dell'elenco di controllo di accesso che protegge %SystemDrive% \\ Programmi o la creazione di un servizio personalizzato.

### <a name="method-3-install-per-user"></a>Metodo 3: Installare Per-User

Un approccio consigliato e semplice consiste nell'installare l'intero gioco in una sottocartella per utente della cartella dei dati dell'applicazione locale, che è possibile trovare chiamando [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL \_ LOCAL \_ APPDATA. Un percorso di esempio è C: \\ Documents e Impostazioni nome utente Local Impostazioni Application Data \\ \\ \\ \\ ExampleGame. Tale percorso consente a un'applicazione in esecuzione con diritti utente Standard di modificare direttamente i file di gioco.

Tuttavia, questo approccio presenta uno svantaggio quando in un computer sono presenti più utenti: ogni utente dispone di una copia del gioco installata e le patch devono essere scaricate e applicate da ogni utente. Ciò comporta uno spreco di tempo e spazio su disco non solo per gli utenti, ma aumenta anche l'uso della larghezza di banda di rete per il server che fornisce patch. Inoltre, poiché qualsiasi applicazione con diritti utente standard può modificare il gioco, i file eseguibili del gioco sono meno protetti; è il produttore del gioco a decidere se è accettabile o meno.

### <a name="method-4-install-to-a-common-per-computer-location"></a>Metodo 4: Eseguire l'installazione in un percorso Per-Computer comune

Un altro metodo è installare i dati del gioco non eseguibili in una sottodirectory del percorso specificato da [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL COMMON APPDATA; un percorso di esempio è C: Documenti e \_ Impostazioni All Users Application Data \_ \\ \\ \\ \\ ExampleGame. Si tratta di un percorso condiviso per tutti gli utenti e può essere modificato dalle applicazioni eseguite con diritti utente standard. Questo metodo riduce al minimo la necessità di riapplicare patch di grandi dimensioni quando il gioco viene riprodotto da più account. I file eseguibili per il gioco devono essere mantenuti in %SystemDrive% Programmi File per ridurre al minimo il rischio per altri \\ account nel sistema. I file eseguibili devono verificare l'integrità del nuovo contenuto nella directory condivisa, poiché tale percorso può essere modificato da un programma o da una persona con diritti utente Standard; È [**consigliabile usare MapFileAndCheckSum**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) per calcolare un checksum dei file.

Questo metodo ha il vantaggio di funzionare allo stesso modo su Windows XP e Windows Vista e non richiede diritti di amministratore.

### <a name="other-possibilities"></a>Altre possibilità

Al di fuori dei metodi già discussi, un'altra possibilità è modificare l'ACL di %SystemDrive% Program Files Game Folder durante \\ l'installazione del gioco in modo che uno strumento di applicazione delle patch possa scrivere direttamente nei file del gioco anche quando viene eseguito con diritti \\ \\ utente Standard. Anche se questo non è difficile, ignora la protezione di sicurezza offerta dal sistema ai file del gioco e offre la possibilità a programmi dannosi di modificare il contenuto della directory. Questa operazione non è consigliabile ed è consigliabile usare un'alternativa.

Un'ultima possibilità è scrivere un servizio personalizzato. In generale, la scrittura di un servizio personalizzato nei giochi di patch non è una buona idea, perché questa operazione è complessa e erta da errori. È consigliabile eseguire l'applicazione di patch usando altri metodi descritti in questo articolo. Tuttavia, un servizio personalizzato potrebbe essere necessario in combinazione con soluzioni anti-trucchi o antipirateria. Tale servizio deve supportare un numero elevato di giochi ed essere progettato in modo che possa scaricare solo i file di patch e scrivere solo nella directory di installazione per il gioco di destinazione. È importante che il servizio sia di piccole dimensioni, abbia una superficie di attacco minima vulnerabile agli attacchi e usi il numero minimo possibile di risorse di sistema quando il gioco non è in esecuzione.

## <a name="summary"></a>Riepilogo

In definitiva, è l'utente a decidere quale metodo implementare. È necessario valutare i fattori che sono importanti per l'utente. Sicurezza, frequenza di applicazione delle patch, facilità d'uso da parte del cliente, carico di lavoro necessario per implementare, complessità della soluzione e conformità delle funzionalità della piattaforma sono i fattori che ogni sviluppatore deve considerare prima di decidere un metodo specifico.

Altre informazioni sulla protezione dell'account utente sono disponibili in Requisiti di sviluppo delle applicazioni di [Windows Vista per il controllo dell'account utente .](/previous-versions/aa905330(v=msdn.10))

 

 