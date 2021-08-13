---
description: Informazioni su come creare un motore di sincronizzazione dei file cloud che usa i file segnaposto usando l'API dei file cloud.
title: Creare un motore di sincronizzazione cloud che supporti i file segnaposto
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: d7d1efae4a56e6f52473002953730fb9f1f9459f1ed8dc82e0ba75ddebf05dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551578"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>Creare un motore di sincronizzazione cloud che supporti i file segnaposto

Un motore di sincronizzazione è un servizio che sincronizza i file, in genere tra un host remoto e un client locale. I motori di sincronizzazione Windows spesso presentano tali file all'utente tramite Windows file system e Esplora file. Prima di Windows 10, versione 1709, il supporto del motore di sincronizzazione in Windows era limitato alle superfici ad hoc indipendenti da scenari, ad esempio il riquadro di spostamento di Esplora file, la barra delle applicazioni Windows e (per applicazioni più tecniche) i driver di filtro file system.

Windows 10 versione 1709 (denominata anche Fall Creators Update) ha introdotto *l'API di file cloud*. Questa API è una nuova piattaforma che formalizza il supporto per i motori di sincronizzazione. L'API file cloud offre il supporto per i motori di sincronizzazione in modo da offrire molti nuovi vantaggi agli sviluppatori e agli utenti finali.

L'API dei file cloud contiene le API Win32 native seguenti e Windows Runtime (WinRT):

* [API filtro cloud:](cloud-filter-reference.md)questa API Win32 nativa offre funzionalità al limite tra la modalità utente e la file system. Questa API gestisce la creazione e la gestione di file segnaposto e directory.
* [Windows. Archiviazione. Spazio dei nomi del](/uwp/api/windows.storage.provider)provider: questa API WinRT consente alle applicazioni di configurare il provider di archiviazione cloud e registrare la radice di sincronizzazione con il sistema operativo.

> [!NOTE]
> L'API file cloud non supporta attualmente l'implementazione di motori di sincronizzazione cloud nelle app UWP. I motori di sincronizzazione cloud devono essere implementati nelle app desktop.

## <a name="supported-features"></a>Caratteristiche supportate

L'API file cloud offre le funzionalità seguenti per la creazione di motori di sincronizzazione cloud.

### <a name="placeholder-files"></a>File segnaposto

* I motori di sincronizzazione possono creare file segnaposto che utilizzano solo 1 KB di spazio di archiviazione per l'intestazione del file system e che si idratono automaticamente in file completi in condizioni di utilizzo normali. File segnaposto presenti come file tipici per le app e per gli utenti finali in Windows Shell.
* I file segnaposto sono integrati verticalmente dal kernel Windows fino alla shell di Windows e la compatibilità delle app con i file segnaposto è in genere un problema. Indipendentemente dal fatto che si usino API file system, il prompt dei comandi o un desktop o un'app UWP per accedere a un file segnaposto, il file si idrato senza modifiche aggiuntive al codice e tale app può usare il file normalmente.
* I file possono essere presenti in tre stati:
  * **File segnaposto:** rappresentazione vuota del file e disponibile solo se il servizio di sincronizzazione è disponibile.
  * **File completo:** il file è stato idratato in modo implicito e potrebbe essere disidratato dal sistema se è necessario spazio.
  * **File completo aggiunto:** il file è stato idrato in modo esplicito dall'utente tramite Esplora file ed è garantito che sia disponibile offline.

L'immagine seguente illustra come vengono visualizzati gli stati del file completo segnaposto, completo e aggiunto in Esplora file.

  ![Esempio di tre stati di file in Esplora file](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>Registrazione radice di sincronizzazione standardizzata

* La registrazione di una radice di sincronizzazione è semplice e standardizzata. Ciò include la creazione di un nodo personalizzato nel riquadro di spostamento Esplora file, come illustrato nello screenshot seguente. Le radici possono essere create come singole voci di primo livello o come elementi figlio di un raggruppamento padre.

  ![Esempio di una voce radice di sincronizzazione in Esplora file](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Integrazione della shell

* Icone di stato:
  * L'API dei file cloud fornisce icone di stato dell'idratazione automatica standardizzate Esplora file e sul desktop Windows cloud.
  * Oltre alle icone di stato Windows standard usate per lo stato di idratazione, è possibile fornire icone di stato personalizzate per proprietà aggiuntive specifiche del servizio.
  * Sostituisce le estensioni shell di sovrimpressione dell'icona legacy.
* Indicazione dello stato:
  * L'apertura di un file segnaposto che richiede più di pochi secondi per l'idratazione mostrerà lo stato di avanzamento dell'idratazione. Lo stato di avanzamento viene visualizzato in alcune posizioni a seconda del contesto:
    * In una finestra di dialogo del motore di copia.
    * Lo stato inline viene visualizzato accanto al file in Esplora file.
    * Se il file non viene aperto all'istruzione specifica dell'utente, viene visualizzata una notifica di tipo avviso popup per informare l'utente e fornire un modo per controllare l'attività di idratazione non intenzionale.
* Anteprime e metadati:
  * I file segnaposto possono avere anteprime fornite dal servizio e metadati di file estesi per offrire all'utente un'esperienza Esplora file semplice.
* Esplora file di spostamento:
  * La registrazione di una radice di sincronizzazione con l'API dei file cloud fa sì che la radice di sincronizzazione (con un'icona e un nome personalizzato) venga visualizzata nel riquadro di spostamento Esplora file di spostamento.
* Esplora file menu di scelta rapida:
  * La registrazione di una radice di sincronizzazione con l'API dei file cloud fornisce automaticamente diversi verbi (voci di menu) nel menu di scelta rapida di Esplora file che consentono all'utente di controllare lo stato di idratazione del file.
  * È possibile aggiungere altri verbi a questa sezione del menu di scelta rapida usando Desktop Bridge API compatibili con .
* Controllo utente dell'idratazione dei file:
  * Gli utenti hanno sempre il controllo dell'idratazione dei file, anche quando i file non vengono idratati in modo esplicito dall'utente. Viene visualizzato un avviso popup interattivo per l'idratazione in background per avvisare l'utente e fornire opzioni. L'immagine seguente illustra una notifica di tipo avviso popup per un file di idratazione.
    ![Esempio di avviso popup interattivo visualizzato per l'idratazione dei file in background](images/file-hydration-interactive-toast.png)
  * Se un utente impedisce a un'app di idratare i file tramite un avviso popup interattivo, può sbloccare l'app nella pagina **Download automatici file** in **Impostazioni**.
    ![Screenshot dell'impostazione di download automatici dei file](images/allow-automatic-file-downloads-setting.png)
* Hook delle operazioni del motore di copia (supportato in Windows 10 Insider Preview Build 19624 e versioni successive):
  * I provider di archiviazione cloud possono registrare un hook di copia della shell per il monitoraggio delle operazioni sui file all'interno della radice di sincronizzazione.
  * Il provider registra l'hook di copia impostando il valore del Registro di sistema **CopyHook** nella chiave del Registro di sistema radice di sincronizzazione su un CLSID dell'oggetto server locale COM. Questo oggetto server locale implementa [l'interfaccia IStorageProviderCopyHook.](../shell/nn-shobjidl-istorageprovidercopyhook.md)

### <a name="desktop-bridge"></a>Desktop Bridge

* I motori di sincronizzazione che usano le API dei file cloud sono progettati per usare il Desktop Bridge [come](/windows/uwp/porting/desktop-to-uwp-root) requisito di implementazione.

## <a name="cloud-mirror-sample"></a>Esempio di cloud mirror

[L'esempio Cloud Mirror](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror) illustra come compilare una soluzione che usa l'API dei file cloud. Non deve essere usato come codice di produzione. La gestione degli errori è priva di affidabilità e viene scritta per essere il più facilmente comprensibile possibile. Si chiama Cloud Mirror perché si limita a eseguire il mirroring di una cartella locale sul disco locale. Si specifica una cartella del server che deve rappresentare il file server cloud e una cartella client che deve specificare il percorso radice di sincronizzazione. Nel riquadro di spostamento di Esplora file viene visualizzato un nodo di primo livello denominato **TestStorageProviderDisplayName** e questo nodo viene mappato alla cartella client specificata.

Quando si tratta di sincronizzazione, questi sono gli elementi che un provider di sincronizzazione di file cloud completamente sviluppato deve implementare:

* Quando il file radice di sincronizzazione è solo un segnaposto, il servizio è responsabile della copia del contenuto del file per l'idratazione. Questa operazione viene implementata nell'esempio.
* Quando il file radice di sincronizzazione è un file completo e il contenuto del file nel servizio cloud cambia, il servizio è responsabile della notifica della modifica al client di sincronizzazione locale e il client di sincronizzazione locale deve gestire le unioni in base alle specifiche specifiche. Questa operazione non viene implementata nell'esempio.
* Quando il file radice di sincronizzazione è un file completo e il contenuto del file nel percorso radice di sincronizzazione (client locale) cambia, il client di sincronizzazione locale deve inviare una notifica al servizio cloud e gestire le unioni in base alle specifiche specifiche. La notifica di modifica del file locale viene implementata nell'esempio, ma non esegue alcun'operazione.

### <a name="use-the-sample"></a>Usare l'esempio

1. Creare due cartelle nel disco rigido locale. Uno di essi fungerà da server e l'altro come client.
2. Aggiungere alcuni file alla cartella del server. Assicurarsi che la cartella client sia vuota.
3. Aprire l'esempio cloud mirror in Visual Studio. Impostare il **progetto CloudMirrorPackage** come progetto di avvio e quindi compilare ed eseguire l'esempio. Quando richiesto dall'esempio, immettere i due percorsi delle cartelle server e client. Verrà visualizzata una finestra della console con informazioni di diagnostica.
4. Aprire Esplora file verificare che sia visualizzato il nodo **TestStorageProviderDisplayName** e i segnaposto per tutti i file copiati nella cartella del server. Per simulare un'applicazione che tenta di aprire i file senza usare la selezione, copiare diverse immagini nella cartella del server. Fare doppio clic su uno di essi nella cartella radice di sincronizzazione e verificare che si idrato. Aprire quindi l'app Foto app. L'app precarica i file adiacenti in background per renderla più probabile che l'utente non presenti ritardi durante la ricerca delle altre immagini. È possibile osservare che la disidratazione in background avviene tramite avvisi popup o Esplora file.
5. Fare clic con il pulsante destro del mouse su un file Esplora file per visualizzare un menu di scelta rapida e verificare che sia visualizzata la voce di menu **TestCommand.** Facendo clic su questa voce di menu verrà visualizzata una finestra di messaggio.
6. Per arrestare l'esempio, impostare lo stato attivo sull'output della console e premere **CTRL+C**. Verrà eseguita la pulizia della registrazione radice di sincronizzazione in modo che il provider sia disinstallato. Se l'esempio si arresta in modo anomalo, è possibile che la radice di sincronizzazione rimanga registrata. In questo modo Esplora file riavvio ogni volta che si fa clic su qualsiasi elemento e viene richiesto di specificare i percorsi del client e del server falsi. In questo caso, disinstallare **l'applicazione di esempio CloudMirrorPackage** dal computer.

### <a name="sample-architecture"></a>Architettura di esempio

L'esempio è volutamente semplice. Usa classi statiche per rendere superfluo passare puntatori di istanza. Ecco le classi principali dell'esempio:

* **FakeCloudProvider:** questa classe di primo livello controlla le classi di lavoro seguenti:
  * **CloudProviderRegistrar:** registra le informazioni radice di sincronizzazione con Windows Shell.
  * **Segnaposto:** genera i file segnaposto nel percorso radice di sincronizzazione.
  * **ShellServices:** costruisce i Windows shell per il menu di scelta rapida, le anteprime e altri servizi.
  * **CloudProviderSyncRootWatcher:** crea un'istanza di un oggetto DirectoryWatcher per monitorare le modifiche al percorso radice di sincronizzazione e agire sulle modifiche.
  * **FileCopierWithProgress:** copia i file dalla cartella del server alla cartella client lentamente in blocchi per simulare il download da un server cloud reale. Fornisce un'indicazione di stato in modo che gli avvisi popup e Esplora file'interfaccia utente mostrano all'utente qualcosa di informativo.

Oltre alle classi precedenti, l'esempio fornisce anche diverse classi helper per richiedere all'utente cartelle e alcune utilità. **TestExplorerCommandHandler,** **CustomStateProvider,** **ThumbnailProvider** e **UriSource** sono tutti esempi di provider di servizi Shell.

## <a name="cloud-files-api-architecture"></a>Architettura dell'API file cloud

Alla base dello stack di archiviazione nell'API dei file cloud è presente un driver minifiltro file system denominato cldflt.sys. Questo driver funge da proxy tra le applicazioni dell'utente e il motore di sincronizzazione. Il motore di sincronizzazione sa come scaricare e caricare i dati su richiesta, mentre è responsabilità di cldflt.sys usare shell per presentare i file come se i dati cloud fossero disponibili in locale.

Cldflt.sys attualmente supporta solo volumi NTFS perché dipende da alcune funzionalità specifiche di NTFS.

Esistono molti file system minifiltri in un sistema e possono essere attivi in un determinato volume contemporaneamente. I driver di maggiore interesse per l'API dei file cloud sono i filtri antivirus file system software.

I driver minifilter del file system sono gestiti e supportati da uno speciale componente in modalità kernel denominato gestione filtri. Tra gli altri compiti, gestione filtri facilita la comunicazione non filtrata tra i filtri e i componenti in modalità utente tramite un costrutto noto come porta del messaggio di filtro.

## <a name="hydration-policies"></a>Criteri di idratazione

Windows supporta un'ampia gamma di criteri di idratazione [primari](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary) e modificatori dei criteri [di idratazione](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier) secondari. I criteri di idratazione primari hanno questo ordine:

  **Sempre completa > completa > progressive > parziali**

Sia le applicazioni che i motori di sincronizzazione possono definire i criteri di idratazione primari preferiti. Se non viene specificato, i criteri di idratazione predefiniti sono progressivi sia per le applicazioni che per i motori di sincronizzazione.

I criteri di idratazione di un file cloud vengono determinati in fase di apertura del file con questa formula:

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

Si supponga, ad esempio, che l'utente stia tentando di aprire un file PDF archiviato in Fabrikam Cloud Drive usando Contoso PDF Viewer, che non specifica i criteri di idratazione preferiti. I criteri di idratazione dell'applicazione sono quindi l'idratazione progressiva, in questo caso per impostazione predefinita. Tuttavia, poiché Fabrikam Cloud Drive è un motore di sincronizzazione dell'idratazione completo, i criteri di idratazione finali sul file diventano completamente idrato, con il risultato che il file viene completamente idratato al primo accesso. Lo stesso risultato si verifica nei casi in cui il motore di sincronizzazione supporta l'idratazione progressiva, ma la preferenza dell'app è l'idratazione completa.

Si noti che i criteri di idratazione dei file non possono essere modificati dopo l'apertura del file.

## <a name="compatibility-with-applications-that-use-reparse-points"></a>Compatibilità con le applicazioni che usano reparse point

L'API dei file cloud implementa il sistema segnaposto usando [reparse point.](/windows/desktop/FileIO/reparse-points) Un errore comune sui reparse point è che sono gli stessi dei collegamenti simbolici. Questo errore si riflette occasionalmente nelle implementazioni dell'applicazione e di conseguenza molte applicazioni esistenti riscontrano errori quando si verificano reparse point.

Per attenuare questo problema di compatibilità, l'API dei file cloud nasconde sempre i reparse point da tutte le applicazioni, ad eccezione dei motori di sincronizzazione e dei processi la cui immagine principale risiede in **%systemroot%**. Le applicazioni che comprendono correttamente i reparse point possono forzare la piattaforma a esporre i reparse point dell'API dei file cloud usando [RtlSetProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) o [RtlSetThreadProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode).