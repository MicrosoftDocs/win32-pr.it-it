---
description: Informazioni su come creare un motore di sincronizzazione di file cloud che usa file segnaposto usando l'API file cloud.
title: Creare un motore di sincronizzazione cloud che supporti i file segnaposto
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: 4f1330285d0c8ef0359639f2be84162f8bc2ef3b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554885"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>Creare un motore di sincronizzazione cloud che supporti i file segnaposto

Un motore di sincronizzazione è un servizio che sincronizza i file, in genere tra un host remoto e un client locale. I motori di sincronizzazione in Windows spesso presentano tali file all'utente tramite Windows file system ed Esplora file. Prima di Windows 10, la versione 1709, il supporto del motore di sincronizzazione in Windows era limitato a superfici ad hoc indipendenti dallo scenario, come il riquadro di spostamento di Esplora file, la barra di sistema di Windows e (per applicazioni più tecniche) file system i driver di filtro.

Windows 10 versione 1709 (denominata anche Fall Creators Update) ha introdotto l' *API per i file Cloud*. Questa API è una nuova piattaforma che formalizza il supporto per i motori di sincronizzazione. L'API file Cloud fornisce il supporto per i motori di sincronizzazione in modo da offrire molti nuovi vantaggi agli sviluppatori e agli utenti finali.

L'API per i file cloud contiene le API Win32 native e Windows Runtime (WinRT) seguenti:

* [API di filtro cloud](cloud-filter-reference.md): questa API Win32 nativa fornisce funzionalità al limite tra la modalità utente e la file System. Questa API gestisce la creazione e la gestione di file e directory segnaposto.
* [Spazio dei nomi Windows. storage. provider](/uwp/api/windows.storage.provider): questa API WinRT consente alle applicazioni di configurare il provider di archiviazione cloud e di registrare la radice di sincronizzazione con il sistema operativo.

> [!NOTE]
> L'API file cloud attualmente non supporta l'implementazione di motori di sincronizzazione cloud nelle app UWP. I motori di sincronizzazione cloud devono essere implementati nelle app desktop.

## <a name="supported-features"></a>Caratteristiche supportate

L'API per i file Cloud fornisce le funzionalità seguenti per la creazione di motori di sincronizzazione cloud.

### <a name="placeholder-files"></a>File segnaposto

* I motori di sincronizzazione possono creare file segnaposto che utilizzano solo 1 KB di spazio di archiviazione per l'intestazione filesystem e che vengono automaticamente idratati in file completi in condizioni di utilizzo normali. File segnaposto presenti come file tipici per le app e per gli utenti finali nella shell di Windows.
* I file segnaposto sono integrati verticalmente dal kernel di Windows fino alla shell di Windows e la compatibilità delle app con i file segnaposto in genere non è un problema. Se si usano file system API, il prompt dei comandi o un desktop o un'app UWP per accedere a un file segnaposto, il file verrà idrato senza modifiche aggiuntive al codice e l'app potrà usare il file normalmente.
* I file possono esistere in tre stati:
  * **File segnaposto**: rappresentazione vuota del file e disponibile solo se il servizio di sincronizzazione è disponibile.
  * **File completo**: il file è stato idratato in modo implicito e potrebbe essere disidratato dal sistema se è necessario spazio.
  * **File completo bloccato**: il file è stato idratato in modo esplicito dall'utente tramite Esplora file ed è garantito che sia disponibile offline.

Nell'immagine seguente viene illustrato il modo in cui vengono visualizzati gli Stati dei file completi segnaposto, completo e bloccato in Esplora file.

  ![Esempio di tre stati di file in Esplora file](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>Registrazione radice di sincronizzazione standardizzata

* La registrazione di una radice di sincronizzazione è semplice e standardizzata. Ciò include la creazione di un nodo personalizzato nel riquadro di spostamento di Esplora file, come illustrato nella schermata seguente. È possibile creare radici come singole voci di primo livello o come elementi figlio di un raggruppamento padre.

  ![Esempio di una voce radice di sincronizzazione in Esplora file](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Integrazione della shell

* Icone di stato:
  * L'API file Cloud fornisce le icone di stato di idratazione automatiche standardizzate visualizzate in Esplora file e sul desktop di Windows.
  * Oltre alle icone di stato standard di Windows usate per lo stato di idratazione, è possibile fornire icone di stato personalizzate per ulteriori proprietà specifiche del servizio.
  * Sostituisce le estensioni legacy della shell di sovrapposizione delle icone.
* Indicazione di stato:
  * L'apertura di un file segnaposto che richiede più di alcuni secondi per idratare indicherà lo stato dell'idratazione. Lo stato di avanzamento viene visualizzato in alcune posizioni a seconda del contesto:
    * In una finestra di dialogo del motore di copia.
    * Lo stato di avanzamento inline viene visualizzato accanto al file in Esplora file.
    * Se il file non viene aperto con l'istruzione specifica dell'utente, viene visualizzata una notifica di tipo avviso popup che informa l'utente e fornisce un modo per controllare l'attività di idratazione imprevista.
* Anteprime e metadati:
  * I file segnaposto possono avere anteprime avanzate fornite dal servizio e metadati di file estesi per offrire all'utente un'esperienza di esplorazione di file semplice.
* Riquadro di spostamento di Esplora file:
  * La registrazione di una radice di sincronizzazione con l'API dei file Cloud causa la visualizzazione della radice di sincronizzazione (con un'icona e un nome personalizzato) nel riquadro di spostamento di Esplora file.
* Menu di scelta rapida di Esplora file:
  * La registrazione di una radice di sincronizzazione con l'API file Cloud fornisce automaticamente diversi verbi (voci di menu) nel menu di scelta rapida di Esplora file che consentono all'utente di controllare lo stato di idratazione del file.
  * È possibile aggiungere verbi aggiuntivi a questa sezione del menu di scelta rapida usando le API compatibili con i desktop Bridge.
* Controllo utente dell'idratazione dei file:
  * Gli utenti hanno sempre il controllo dell'idratazione dei file, anche quando i file non vengono idratati in modo esplicito dall'utente. Viene visualizzato un avviso popup interattivo per l'idratazione in background per avvisare l'utente e fornire opzioni. Nell'immagine seguente viene illustrata una notifica di tipo avviso popup per un file idratante.
    ![Esempio di un avviso popup interattivo visualizzato per l'idratazione dei file in background](images/file-hydration-interactive-toast.png)
  * Se un utente blocca un'app da file idratanti tramite un avviso popup interattivo, può sbloccare l'app nella pagina di **download automatico dei file** in **Impostazioni**.
    ![Screenshot dell'impostazione di download automatico dei file](images/allow-automatic-file-downloads-setting.png)
* Associazione delle operazioni del motore di copia (supportata in Windows 10 Insider Preview Build 19624 e versioni successive):
  * I provider di archiviazione cloud possono registrare un hook di copia della Shell per il monitoraggio delle operazioni sui file all'interno della radice di sincronizzazione.
  * Il provider registra l'hook di copia impostando il valore del registro di sistema **CopyHook** nella chiave del registro di sistema radice di sincronizzazione su un CLSID dell'oggetto server locale com. Questo oggetto server locale implementa l'interfaccia [IStorageProviderCopyHook](../shell/nn-shobjidl-istorageprovidercopyhook.md) .

### <a name="desktop-bridge"></a>Desktop Bridge

* I motori di sincronizzazione che usano le API per i file cloud sono progettati per usare [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) come requisito di implementazione.

## <a name="cloud-mirror-sample"></a>Esempio di mirroring cloud

L' [esempio cloud mirror](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror) illustra come compilare una soluzione che usa l'API per i file cloud. Non può essere usato come codice di produzione. La gestione degli errori non è affidabile e viene scritta nel modo più semplice possibile. Questo metodo è denominato mirroring cloud perché riflette semplicemente una cartella locale nel disco locale. Specificare una cartella del server destinata a rappresentare il file server cloud e una cartella client destinata a specificare il percorso radice di sincronizzazione. Un nodo di primo livello viene visualizzato nel riquadro di spostamento in Esplora file denominato **TestStorageProviderDisplayName** e il nodo viene mappato alla cartella client specificata.

Per quanto riguarda la sincronizzazione, questi sono gli elementi che devono essere implementati da un provider di sincronizzazione dei file cloud completamente sviluppato:

* Quando il file radice di sincronizzazione è semplicemente un segnaposto, il servizio è responsabile della copia del contenuto del file per l'idratazione. Questa operazione è implementata nell'esempio.
* Quando il file radice di sincronizzazione è un file completo e il contenuto del file nel servizio cloud viene modificato, il servizio è responsabile della notifica al client di sincronizzazione locale della modifica e il client di sincronizzazione locale deve gestire le unioni in base alle specifiche. Questa operazione non è implementata nell'esempio.
* Quando il file radice di sincronizzazione è un file completo e il contenuto del file nel percorso radice di sincronizzazione (client locale) cambia, il client di sincronizzazione locale deve inviare una notifica al servizio cloud e gestire le unioni in base alle specifiche. La notifica della modifica del file locale è implementata nell'esempio, ma non esegue alcuna operazione.

### <a name="use-the-sample"></a>Usare l'esempio

1. Creare due cartelle sul disco rigido locale. Uno di essi fungerà da server e dall'altro come client.
2. Aggiungere alcuni file alla cartella del server. Verificare che la cartella client sia vuota.
3. Aprire l'esempio cloud mirror in Visual Studio. Impostare il progetto **CloudMirrorPackage** come progetto di avvio e quindi compilare ed eseguire l'esempio. Quando richiesto dall'esempio, immettere i due percorsi per le cartelle server e client. Al termine, verrà visualizzata una finestra della console con le informazioni di diagnostica.
4. Aprire Esplora file e verificare che siano visualizzati il nodo **TestStorageProviderDisplayName** e i segnaposto per tutti i file copiati nella cartella del server. Per simulare un'applicazione che tenti di aprire i file senza utilizzare il selettore, copiare diverse immagini nella cartella del server. Fare doppio clic su uno di essi nella cartella radice di sincronizzazione e verificare che venga idratata. Quindi, aprire l'app Photos. L'app effettuerà il pre-caricamento dei file adiacenti in background per rendere più probabile che l'utente non ritardi la ricerca nelle altre immagini. È possibile osservare la disidratazione in background tramite popup o in Esplora file.
5. Fare clic con il pulsante destro del mouse su un file in Esplora file per visualizzare un menu di scelta rapida e verificare che sia visualizzata la voce di menu **TestCommand** . Quando si fa clic su questa voce di menu, viene visualizzata una finestra di messaggio.
6. Per arrestare l'esempio, impostare lo stato attivo sull'output della console e premere **CTRL-C**. Questa operazione consente di pulire la registrazione radice di sincronizzazione in modo che il provider venga disinstallato. Se l'esempio si arresta in modo anomalo, è possibile che la radice di sincronizzazione rimanga registrata. In questo modo verrà eseguito il riavviamento di Esplora file ogni volta che si fa clic su qualsiasi elemento e vengono richiesti i percorsi del client e del server fittizi. In tal caso, disinstallare l'applicazione di esempio **CloudMirrorPackage** dal computer.

### <a name="sample-architecture"></a>Architettura di esempio

L'esempio è volutamente semplice. USA classi statiche per rendere superfluo il passaggio di puntatori di istanza. Di seguito sono riportate le classi principali dell'esempio:

* **FakeCloudProvider**: questa classe di primo livello controlla le classi di lavoro seguenti:
  * **CloudProviderRegistrar**: registra le informazioni della radice di sincronizzazione con la shell di Windows.
  * **Segnaposto**: genera i file segnaposto nel percorso radice di sincronizzazione.
  * **ShellServices**: crea i provider della shell di Windows per il menu di scelta rapida, le anteprime e altri servizi.
  * **CloudProviderSyncRootWatcher**: crea un'istanza di un DirectoryWatcher per monitorare le modifiche al percorso radice di sincronizzazione e agire sulle modifiche.
  * **FileCopierWithProgress**: copia i file dalla cartella del server alla cartella client lentamente in blocchi per simularne il download da un server cloud reale. Fornisce indicazioni sullo stato di avanzamento, in modo che i popup e l'interfaccia utente di Esplora file visualizzino l'utente.

Oltre alle classi precedenti, l'esempio fornisce anche diverse classi helper per richiedere all'utente le cartelle e alcune utilità. **TestExplorerCommandHandler**, **CustomStateProvider**, **ThumbnailProvider** e **UriSource** sono tutti esempi di provider di servizi Shell.

## <a name="cloud-files-api-architecture"></a>Architettura API dei file Cloud

Alla base dello stack di archiviazione nell'API per i file Cloud è presente un driver file system mini denominato cldflt.sys. Questo driver funge da proxy tra le applicazioni dell'utente e il motore di sincronizzazione. Il motore di sincronizzazione sa come scaricare e caricare i dati su richiesta, mentre è responsabilità del cldflt.sys usare la Shell per presentare i file come se i dati del cloud fossero disponibili localmente.

Cldflt.sys attualmente supporta solo i volumi NTFS perché dipende da alcune funzionalità univoche per NTFS.

Sono disponibili molti file system driver mini in un sistema e possono essere attivi contemporaneamente in un determinato volume. I driver di maggiore interesse per l'API per i file cloud sono i filtri file system antivirus.

I driver mini del file System sono gestiti e supportati da un particolare componente in modalità kernel denominato gestione filtri. Tra molti altri compiti, gestione filtri facilita la comunicazione non filtrata tra i filtri e i componenti in modalità utente tramite un costrutto noto come porta filtro messaggio.

## <a name="hydration-policies"></a>Criteri di idratazione

Windows supporta un'ampia gamma di [criteri di idratazione primari](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary) e modificatori di [criteri di idratazione secondari](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier) . I criteri di idratazione primari hanno questo ordine:

  **Sempre pieno > > progressivo completo > parziale**

Sia le applicazioni che i motori di sincronizzazione possono definire i criteri di idratazione primari preferiti. Se non specificato, i criteri di idratazione predefiniti sono progressivi per le applicazioni e i motori di sincronizzazione.

I criteri di idratazione di un file cloud vengono determinati in base all'ora di apertura del file da questa formula:

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

Si immagini, ad esempio, che l'utente stia tentando di aprire un file PDF archiviato nell'unità cloud Fabrikam usando contoso PDF Viewer, che non specifica i criteri di idratazione preferiti. I criteri di idratazione dell'applicazione sono quindi un'idratazione progressiva, in questo caso per impostazione predefinita. Tuttavia, poiché Fabrikam Cloud Drive è un motore di sincronizzazione dell'idratazione completa, i criteri di idratazione finali per il file diventano un'idratazione completa, pertanto il file verrà completamente idratato al primo accesso. Lo stesso risultato si verifica nei casi in cui il motore di sincronizzazione supporta l'idratazione progressiva, ma la preferenza dell'app è l'idratazione completa.

Si noti che i criteri di idratazione dei file non possono essere modificati dopo l'apertura del file.

## <a name="compatibility-with-applications-that-use-reparse-points"></a>Compatibilità con le applicazioni che usano i reparse point

L'API dei file Cloud implementa il sistema segnaposto usando i [reparse point](/windows/desktop/FileIO/reparse-points). Un malinteso comune sui reparse point è che corrispondono ai collegamenti simbolici. Questo malinteso viene occasionalmente riflesso nelle implementazioni delle applicazioni e, di conseguenza, molte applicazioni esistenti rilevano errori quando si verifica un reparse point.

Per attenuare questo problema di compatibilità, l'API dei file Cloud nasconde sempre i reparse point da tutte le applicazioni, ad eccezione dei motori di sincronizzazione e dei processi la cui immagine principale risiede in **% systemroot%**. Le applicazioni che comunicano correttamente i reparse point possono forzare la piattaforma a esporre i reparse point API dei file cloud tramite [RtlSetProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) o [RtlSetThreadProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode).