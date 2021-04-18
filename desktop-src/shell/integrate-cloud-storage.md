---
description: Viene illustrato come eseguire la registrazione come provider radice di sincronizzazione e come integrare un provider di archiviazione cloud nel livello radice del riquadro di spostamento.
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: Integrare un provider di archiviazione cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21fdc5abfbf9881bfe23b00a924fce989aec7c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571158"
---
# <a name="integrate-a-cloud-storage-provider"></a>Integrare un provider di archiviazione cloud

Quando si dispone di un provider di archiviazione cloud, è necessario eseguire un paio di passaggi per offrire un'esperienza coerente e preferibile per l'utente. Questi due elementi sono la registrazione come provider radice di sincronizzazione e l'integrazione dell'applicazione nel livello radice del riquadro di spostamento.

> [!IMPORTANT]
> L'integrazione del provider di archiviazione cloud è supportata solo a partire da Windows 10.

 

La prima cosa da fare è registrarsi come provider radice di sincronizzazione. In questo modo la shell di Windows è in grado di conoscere l'applicazione e che l'applicazione sarà responsabile della sincronizzazione dei file nella radice di sincronizzazione. Questo consentirà anche ad altre applicazioni di essere in grado di sincronizzare questi file in modo che possano rispondere in modo appropriato. Altre applicazioni possono quindi usare [**StorageFile. provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) per ottenere il [**DisplayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) e l' [**ID**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) dell'applicazione.

Per eseguire la registrazione come provider radice di sincronizzazione, sarà necessario creare più voci del registro di sistema. Prima di fornire l'elenco di coppie chiave-valore, di seguito sono riportati alcuni segnaposto che è necessario sostituire con i dati dell'applicazione.

-   *\[ storage provider ID \]*: nome del provider di archiviazione cloud. Questo nome deve essere coerente indipendentemente dalla versione dell'applicazione. Un esempio è OneDrive.
-   *\[ SID \] di Windows*: il SID di Windows univoco che identifica l'utente. Se l'app supporta più installazioni per più utenti in un singolo computer, questo elemento è obbligatorio.
-   *\[ ID \] account*: identificatore del provider di servizi per l'account corrente dell'utente. Alcuni provider richiedono la possibilità di fornire più radici di sincronizzazione per un utente. Un esempio è costituito da un account di lavoro e personale. L' *ID account* consente la registrazione di più account per un utente. Se il provider supporta più radici di sincronizzazione per utente, questo elemento è obbligatorio.

Questi segnaposto vengono combinati insieme per formare l'ID radice di sincronizzazione. È necessario inserire un **!** carattere tra i segnaposto quando si forma l'ID radice di sincronizzazione. Ecco le coppie chiave-valore che devono essere create.

-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\**_\[ storage provider ID \]_** _\[ SID \] di Windows_** _\[ ID \] account_*_\\ DisplayNameResource_* : punta alla risorsa in cui la shell di Windows o altre applicazioni possono ottenere un nome descrittivo per la radice di sincronizzazione.
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\**_\[ storage provider ID \]_** _\[ SID \] di Windows_** _\[ ID \] account_*_\\ IconResource_* : punta alla risorsa in cui la shell di Windows o altre applicazioni possono ottenere un'icona per la radice di sincronizzazione.
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\**_\[ storage provider ID \]_** _\[ SID \] di Windows_** _\[ ID \] account_*_\\ UserSyncRoots \\_*_\[ Windows SID \]_ : percorso su disco in cui si trova la radice di sincronizzazione.

Oltre alla registrazione come provider radice di sincronizzazione, si vuole che gli utenti abbiano accesso facile ai dati forniti. Lo spazio dei nomi Esplora file è progettato per fornire un metodo per semplificare l'accesso. La creazione di un'estensione dello spazio dei nomi per il provider e l'incorporamento nella finestra Esplora file consentirà agli utenti di interagire con il livello radice dei servizi esattamente come vengono usati con altri elementi di Esplora file. In questo argomento viene illustrato come estendere lo spazio dei nomi di Esplora file in modo che il provider venga visualizzato a livello di radice nel riquadro di spostamento.

Il riquadro di spostamento della finestra Esplora file è la parte della finestra visualizzata sul lato sinistro. Nell'immagine seguente è possibile visualizzare la struttura dello spazio dei nomi per questo utente. Il livello radice nel riquadro di spostamento include gli oggetti per **OneDrive**, **questo PC** e la **rete**. Con la procedura seguente l'estensione viene aggiunta allo stesso livello.

![riquadro di spostamento](images/navigationpane.png)

Per aggiungere l'estensione al riquadro di spostamento, è necessario disporre di quanto segue prima di modificare il registro di sistema:

-   Una file system cartella che contiene i dati da visualizzare all'utente.

-   Nome del servizio cloud che verrà visualizzato nel riquadro di spostamento. Potrebbe anche essere il nome dell'istanza se il servizio supporta più account.

-   Icona identificabile per l'applicazione.

-   CLSID per l'applicazione. Un modo per generare un CLSID per l'applicazione consiste nell'usare il Uuidgen.exe. Per ulteriori informazioni su CLSID, vedere la [chiave CLSID](../com/clsid-key-hklm.md) .

La procedura seguente consente di modificare il registro di sistema per ottenere le informazioni necessarie nello spazio dei nomi di Esplora file. I passaggi specifici eseguono tre operazioni.

-   Creare le chiavi nel registro di sistema per il CLSID che include i valori per il nome e l'icona dell'estensione, nonché altre informazioni che ne definiscono il comportamento.

-   Configurare l'estensione in modo che sia integrata nel riquadro di spostamento nella posizione corretta e con la visibilità corretta.

-   Configurare l'estensione in modo che abbia il comportamento previsto per un elemento nel riquadro di spostamento.

Queste istruzioni usano in modo specifico il comando **reg.exe** , ma è possibile usare qualsiasi strumento di modifica del registro di sistema di propria scelta. È anche possibile integrare questi passaggi in un programma di installazione che aggiorna il registro di sistema a livello di codice.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>Passaggio 1: aggiungere il CLSID e assegnare un nome all'estensione

Aggiungere il nome dell'estensione al registro di sistema in HKEY \_ Current \_ User. Si aggiungerà anche l'identificatore univoco per questa estensione. È possibile aggiungere più di un'estensione per utente, ma in tal caso sarà necessario un nome univoco e un identificatore per ogni estensione. Il nome e l'identificatore devono essere coerenti per tutti gli altri passaggi. In questo esempio il nome è *MyCloudStorageApp*.

> [!IMPORTANT]
> L'identificatore fornito (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) in questi passaggi viene usato solo come esempio. È necessario modificarlo in un CLSID univoco.

 

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3}/ve/t reg \_ SZ/d "MyCloudStorageApp"/f**

### <a name="step-2-set-the-image-for-your-icon"></a>Passaggio 2: impostare l'immagine per l'icona

Consente di specificare il percorso dell'icona da visualizzare nel riquadro di spostamento. Nell'esempio seguente, *1043* si riferisce all'identificatore di risorsa per l'icona nella dll indicata.

> [!IMPORTANT]
> È necessario aggiornare il percorso dell'immagine. Deve puntare a un percorso generico in cui l'app ha installato un'immagine.

 

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3} \\ DefaultIcon/ve/t reg \_ expand \_ SZ/d%% SystemRoot%% \\ system32 \\imageres.dll,-1043/f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>Passaggio 3: aggiungere l'estensione al riquadro di spostamento e renderla visibile

L'impostazione di questo valore su 0x1 indica che l'estensione deve essere bloccata. In questo modo gli utenti vengono visualizzati per impostazione predefinita. La configurazione predefinita per un utente è che solo gli elementi aggiunti verranno visualizzati nel riquadro di spostamento. Un utente può modificare l'impostazione facendo clic con il pulsante destro del mouse nel riquadro di spostamento e selezionando **Mostra tutte le cartelle**. Se non si vuole aggiungere l'estensione, è possibile impostare questo valore su 0x0. Questa operazione non rimuove l'estensione, ma impedisce semplicemente che venga visualizzata all'utente per impostazione predefinita.

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3}/v System. IsPinnedToNameSpaceTree/t reg \_ DWORD/d 0x1/f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>Passaggio 4: impostare il percorso per l'estensione nel riquadro di spostamento

Si tratta di una procedura fondamentale per assicurarsi che il riquadro di spostamento fornisca un'esperienza coerente per l'utente.

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3}/V SortOrderIndex/t reg \_ DWORD/d 0x42/f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>Passaggio 5: specificare la dll che ospita l'estensione.

Usare il shell32.dll per emulare le cartelle di Windows predefinite. Modificare questa operazione solo se si dispone di un motivo specifico per eseguire questa operazione e si ha familiarità con le estensioni dello spazio dei nomi.

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3} \\ InprocServer32/ve/t reg \_ expand \_ SZ/d%% SystemRoot%% \\ system32 \\shell32.dll/f**

### <a name="step-6-define-the-instance-object"></a>Passaggio 6: definire l'oggetto istanza

Indica che l'estensione dello spazio dei nomi deve funzionare come altre strutture di cartelle di file in Esplora file. Per altre informazioni sugli oggetti istanza della shell, vedere Creazione di estensioni della shell [con oggetti istanza della shell](/previous-versions/ms997573(v=msdn.10)).

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3} \\ istanza/v CLSID/T reg \_ SZ/d {0E5AAE11-a475-4c5b-AB00-C66DE400274E}/f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>Passaggio 7: specificare gli attributi file system della cartella di destinazione

Questa operazione è necessaria per garantire che Esplora file fornisca un'esperienza coerente e prevista per gli utenti. Questo comando imposta **la \_ \_ directory degli attributi** di file e l'attributo di **file \_ \_ ReadOnly**, che sono entrambi [**costanti di attributi di file**](../fileio/file-attribute-constants.md).

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3} \\ instance \\ InitPropertyBag/v Attributes/t reg \_ DWORD/d 0x11/f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>Passaggio 8: impostare il percorso per la radice di sincronizzazione

Imposta il percorso per la radice di sincronizzazione.

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3} \\ istanza \\ InitPropertyBag/v TargetFolderPath/t reg \_ expand \_ SZ/d%% UserProfile%% \\ MyCloudStorageApp/f**

### <a name="step-9-set-appropriate-shell-flags"></a>Passaggio 9: impostare i flag della shell appropriati

Impostare alcuni flag necessari per aggiungere l'estensione dello spazio dei nomi all'albero di Esplora file.

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3} \\ ShellFolder/v FolderValueFlags/t reg \_ DWORD/d 0x28/f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>Passaggio 10: impostare i flag appropriati per controllare il comportamento della shell

Impostare i flag [**SFGAO**](sfgao.md) appropriati. I flag rilevanti sono SFGAO \_ CANCOPY, SFGAO \_ CANLINK, SFGAO \_ storage, SFGAO HASPROPSHEET \_ , SFGAO STORAGEANCESTOR, \_ SFGAO \_ FILESYSANCESTOR, SFGAO \_ Folder, SFGAO \_ filesystem e SFGAO HASSUBFOLDER \_ .

**reg add HKCU \\ software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3} \\ SHELLFOLDER/V Attributes/t reg \_ DWORD/d 0xF080004D/f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>Passaggio 11: registrare l'estensione nella radice dello spazio dei nomi

Configurare l'estensione dello spazio dei nomi in modo che sia un elemento figlio della cartella desktop.

**reg add HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ Desktop \\ Namespace \\ {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3}/ve/t reg \_ SZ/d MyCloudStorageApp/f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>Passaggio 12: nascondere l'estensione dal desktop

È importante che l'estensione venga visualizzata solo nel riquadro di spostamento di Esplora file. Un'estensione dello spazio dei nomi non funziona come un collegamento normale. Pertanto, non è consigliabile utilizzare questo metodo per creare un collegamento sul desktop.

**reg add HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ HideDesktopIcons \\ NewStartPanel/v {0672A6D1-A6E0-40fe-AB16-F25BADC6D9E3}/t reg \_ DWORD/d 0x1/f**

 

 
