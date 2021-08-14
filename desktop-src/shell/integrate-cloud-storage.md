---
description: Illustra come eseguire la registrazione come provider radice di sincronizzazione e integrare un provider di archiviazione cloud nel livello radice del riquadro di spostamento.
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: Integrare un provider Archiviazione cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e218caa292e2b85e13e00374562c172158be8bb2f062f25b47979902046282c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458201"
---
# <a name="integrate-a-cloud-storage-provider"></a>Integrare un provider Archiviazione cloud

Quando si dispone di un provider di archiviazione cloud, è necessario eseguire un paio di passaggi per offrire un'esperienza coerente e preferita per l'utente. Questi due elementi vengono registrati come provider radice di sincronizzazione e integrano l'applicazione nel livello radice del riquadro di spostamento.

> [!IMPORTANT]
> L'integrazione del provider di archiviazione cloud è supportata solo a partire da Windows 10.

 

La prima cosa da fare è registrare come provider radice di sincronizzazione. Ciò consente alla shell Windows informazioni sull'applicazione e che l'applicazione sarà responsabile della sincronizzazione dei file nella radice di sincronizzazione. In questo modo anche altre applicazioni sapranno che si sta sincronizzando questi file in modo che possano rispondere in modo appropriato. Altre applicazioni possono quindi usare [**StorageFile.Provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) per ottenere [**displayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) e [**ID**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) dell'applicazione.

Per eseguire la registrazione come provider radice di sincronizzazione, è necessario creare più voci del Registro di sistema. Prima di fornire l'elenco delle coppie chiave-valore, ecco alcuni segnaposto da sostituire con i propri dati dell'applicazione.

-   *\[ storage provider \] ID (ID provider* di archiviazione): nome del provider di archiviazione cloud. Questo nome deve essere coerente indipendentemente dalla versione dell'applicazione. Un esempio è OneDrive.
-   *\[ Windows SID \]*: SID Windows univoco che identifica l'utente. Se l'app supporta più installazioni per più utenti in un singolo computer, questa operazione è obbligatoria.
-   *\[ ID \] account:* identificatore del provider di servizi per l'account corrente dell'utente. Alcuni provider richiedono la possibilità di fornire più radici di sincronizzazione per un utente. Un esempio è un account aziendale e un account personale. *L'ID account* consente di avere più account registrati per un utente. Se il provider supporta più radici di sincronizzazione per ogni utente, questa parte è obbligatoria.

Questi segnaposto vengono combinati insieme per formare l'ID radice di sincronizzazione. È necessario inserire un oggetto **.** tra i segnaposto quando si forma l'ID radice di sincronizzazione. Ecco le coppie chiave-valore che devono essere create.

-   **HKLM \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer \\ \\ SyncRootManager \\** storage provider _\[ ID \]_*_!_* _\[ Windows SID \]_*_!_* _\[ ID \] account_*_\\ DisplayNameResource:_* punta alla risorsa in cui Windows Shell o altre applicazioni possono ottenere un nome descrittivo per la radice di sincronizzazione.
-   **HKLM \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer \\ \\ SyncRootManager \\** storage provider _\[ ID \]_*_!_* _\[ Windows SID \]_*_!_* _\[ Icona \] ID_*_\\ accountRisorsa:_* punta alla risorsa in cui Windows Shell o altre applicazioni possono ottenere un'icona per la radice di sincronizzazione.
-   **HKLM \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer \\ \\ SyncRootManager \\** storage provider _\[ ID \]_*_!_* _\[ Windows SID \]_*_!_* _\[ ID \] account_*_\\ UserSyncRoots \\_*_\[ Windows SID: \]_ percorso sul disco in cui si trova la radice di sincronizzazione.

Oltre alla registrazione come provider radice di sincronizzazione, si vuole anche consentire agli utenti di accedere facilmente ai dati forniti. Lo Esplora file spazio dei nomi è progettato per fornire un metodo per tale accesso semplice. La creazione di un'estensione dello spazio dei nomi per il provider e la sua incorporazione nella finestra di Esplora file consentirà agli utenti di interagire con il livello radice dei servizi esattamente come vengono usati con altri Esplora file elementi. Questo argomento illustra come estendere lo spazio dei nomi Esplora file in modo che il provider venga visualizzato a livello di radice nel riquadro di spostamento.

Il riquadro di spostamento Esplora file finestra di spostamento è la parte della finestra visualizzata sul lato sinistro. Nell'immagine seguente è possibile visualizzare la struttura dello spazio dei nomi per questo utente. Il livello radice nel riquadro di spostamento include gli oggetti **per OneDrive**, **Questo PC** e **Rete.** Seguendo questa procedura, l'estensione verrà aggiunta allo stesso livello.

![riquadro di spostamento](images/navigationpane.png)

Per aggiungere l'estensione al riquadro di spostamento, è necessario disporre di quanto segue prima di modificare il Registro di sistema:

-   Una file system che contiene i dati da visualizzare all'utente.

-   Nome del servizio cloud che verrà visualizzato nel riquadro di spostamento. Può anche essere il nome dell'istanza se il servizio supporta più account.

-   Icona identificabile per l'applicazione.

-   CLSID per l'applicazione. Un modo per generare un CLSID per l'applicazione è usare il Uuidgen.exe. Per [altre informazioni su CLSID,](../com/clsid-key-hklm.md) vedere Chiave CLSID.

I passaggi seguenti modificano il Registro di sistema per ottenere le informazioni necessarie nello spazio dei nomi Esplora file . I passaggi specifici ese cosa fanno tre cose.

-   Creare chiavi nel Registro di sistema per il CLSID che include i valori per il nome e l'icona per l'estensione, nonché altre informazioni che ne definiscono il comportamento.

-   Configurare l'estensione per l'integrazione nel riquadro di spostamento nella posizione corretta e con la visibilità appropriata.

-   Configurare l'estensione in modo che abbia il comportamento previsto per un elemento nel riquadro di spostamento.

Queste istruzioni usano in modo specifico **reg.exe** comando , ma è possibile usare qualsiasi strumento di modifica del Registro di sistema di propria scelta. È anche possibile integrare questi passaggi in un programma di installazione che aggiorna il Registro di sistema a livello di codice.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>Passaggio 1: Aggiungere il CLSID e assegnare un nome all'estensione

Aggiungere il nome dell'estensione al Registro di sistema in HKEY \_ CURRENT \_ USER. Si aggiungerà anche l'identificatore univoco per questa estensione. È possibile aggiungere più estensioni per utente, ma in questo caso sono necessari un nome e un identificatore univoci per ogni estensione. Il nome e l'identificatore devono essere coerenti nel resto di questi passaggi. In questo esempio il nome è *MyCloudStorageApp.*

> [!IMPORTANT]
> L'identificatore fornito (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) in questi passaggi viene usato solo come esempio. Sarà necessario modificarlo nel CLSID univoco.

 

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG \_ SZ /d "MyCloudStorageApp" /f**

### <a name="step-2-set-the-image-for-your-icon"></a>Passaggio 2: Impostare l'immagine per l'icona

Specificare il percorso dell'icona che deve essere visualizzata nel riquadro di spostamento. Nell'esempio *seguente, 1043* fa riferimento all'identificatore di risorsa per l'icona nella DLL indicata.

> [!IMPORTANT]
> È necessario aggiornare il percorso dell'immagine. Deve puntare a un percorso generico in cui l'app ha installato un'immagine.

 

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ DefaultIcon /ve /t REG \_ EXPAND \_ SZ /d %%SystemRoot%% \\ system32 \\imageres.dll,-1043 /f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>Passaggio 3: Aggiungere l'estensione al riquadro di spostamento e renderla visibile

Impostando questo valore su 0x1 indica che l'estensione deve essere bloccata. In questo modo si avrà la certezza che sia visualizzato agli utenti per impostazione predefinita. La configurazione predefinita per un utente è che nel riquadro di spostamento verranno visualizzati solo gli elementi aggiunti. Un utente può modificare tale impostazione facendo clic con il pulsante destro del mouse nel riquadro di spostamento e **scegliendo Mostra tutte le cartelle.** Se non si vuole aggiungere l'estensione, è possibile impostare questo valore su 0x0. Ciò non rimuoverà l'estensione, ma si limita a impedirne la visualizzazione all'utente per impostazione predefinita.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v System.IsPinnedToNameSpaceTree /t REG \_ DWORD /d 0x1 /f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>Passaggio 4: Impostare il percorso per l'estensione nel riquadro di spostamento

Questo è fondamentale per assicurarsi che il riquadro di spostamento garantisca un'esperienza coerente per l'utente.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v SortOrderIndex /t REG \_ DWORD /d 0x42 /f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>Passaggio 5: Specificare la DLL che ospita l'estensione.

Usare il shell32.dll per emulare le cartelle di Windows predefinite. Modificare questa impostazione solo se si ha un motivo specifico per farlo e si ha familiarità con le estensioni dello spazio dei nomi.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ InProcServer32 /ve /t REG \_ EXPAND \_ SZ /d %%systemroot%% \\ system32 \\shell32.dll /f**

### <a name="step-6-define-the-instance-object"></a>Passaggio 6: Definire l'oggetto istanza

Indicare che l'estensione dello spazio dei nomi deve funzionare come le altre strutture di cartelle di file Esplora file. Per altre informazioni sugli oggetti istanza della shell, vedere [Creating Shell Extensions with Shell Instance Objects](/previous-versions/ms997573(v=msdn.10)).

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance /v CLSID /t REG \_ SZ /d {0E5AAE11-A475-4c5b-AB00-C66DE400274E} /f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>Passaggio 7: Specificare gli file system della cartella di destinazione

Questa operazione è necessaria per assicurarsi che il Esplora file un'esperienza coerente e prevista per gli utenti. Questo comando imposta **FILE \_ ATTRIBUTE DIRECTORY \_ e** **FILE ATTRIBUTE \_ \_ READONLY,** entrambi costanti [**di attributi file.**](../fileio/file-attribute-constants.md)

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag /v Attributes /t REG \_ DWORD /d 0x11 /f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>Passaggio 8: Impostare il percorso per la radice di sincronizzazione

Impostare il percorso per la radice di sincronizzazione.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag /v TargetFolderPath /t REG \_ EXPAND \_ SZ /d %%USERPROFILE%% \\ MyCloudStorageApp /f**

### <a name="step-9-set-appropriate-shell-flags"></a>Passaggio 9: Impostare i flag della shell appropriati

Impostare alcuni flag necessari per aggiungere l'estensione dello spazio dei nomi all'Esplora file albero.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder /v FolderValueFlags /t REG \_ DWORD /d 0x28 /f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>Passaggio 10: Impostare i flag appropriati per controllare il comportamento della shell

Impostare i flag [**SFGAO**](sfgao.md) appropriati. I flag pertinenti sono SFGAO \_ CANCOPY, SFGAO \_ CANLINK, \_ SFGAO STORAGE, SFGAO \_ HASPROPSHEET, SFGAO \_ STORAGEANCESTOR, SFGAO \_ FILESYSANCESTOR, SFGAO \_ FOLDER, SFGAO \_ FILESYSTEM e SFGAO \_ HASSUBFOLDER.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder /v Attributes /t REG \_ DWORD /d 0xF080004D /f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>Passaggio 11: Registrare l'estensione nella radice dello spazio dei nomi

Configurare l'estensione dello spazio dei nomi come figlio della cartella desktop.

**reg add HKCU \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer Desktop \\ \\ \\ NameSpace \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG \_ SZ /d MyCloudStorageApp /f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>Passaggio 12: Nascondere l'estensione dal desktop

È importante che l'estensione venga visualizzata solo nel riquadro di spostamento del Esplora file. Un'estensione dello spazio dei nomi non funziona come un collegamento normale. Pertanto, non è consigliabile usare questo metodo per creare un collegamento desktop.

**reg add HKCU \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer \\ \\ HideDesktopIcons \\ NewStartPanel /v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /t REG \_ DWORD /d 0x1 /f**

 

 
