---
description: Questo argomento descrive alcuni aspetti da considerare quando si usano librerie nel programma.
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: Uso di librerie nel programma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2c76c4ce8bf9114d7294b257c03bcc62adecc947a3d7e651d6f94fa8876d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821111"
---
# <a name="using-libraries-in-your-program"></a>Uso di librerie nel programma

Questo argomento descrive alcuni aspetti da considerare quando si usano librerie nel programma.

In questo argomento

-   [Panoramica della programmazione delle librerie](#library-programming-overview)
-   [Programmazione con librerie](#programming-with-libraries)
    -   [Spostamento da cartelle note a librerie](#moving-from-known-folders-to-libraries)
    -   [HomeGroup e librerie condivise](#homegroup-and-shared-libraries)
-   [Uso di una finestra di dialogo file comune con le librerie](#using-a-common-file-dialog-box-with-libraries)
-   [Abilitazione della selezione della libreria dall'interfaccia utente](#enabling-library-selection-from-the-user-interface)
-   [Accesso al contenuto della libreria in un programma](#accessing-library-content-in-a-program)
    -   [Accesso al contenuto della libreria con l'interfaccia IShellLibrary](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [Accesso al contenuto della libreria con le API shell](#accessing-library-content-with-the-shell-apis)
-   [Salvataggio del contenuto utente in una raccolta](#saving-user-content-in-a-library)
-   [Supporto delle operazioni di trascinamento della selezione in una libreria](#supporting-drag-and-drop-operations-in-a-library)
-   [Mantenere la sincronizzazione con una libreria](#keeping-in-sync-with-a-library)
    -   [Aggiornamento bulk](#bulk-update)
    -   [Notifica dell'API shell](#shell-api-notification)
    -   [Notifica dell'API del file system](#file-system-api-notification)
-   [Argomenti correlati](#related-topics)

## <a name="library-programming-overview"></a>Panoramica della programmazione delle librerie

Le librerie consentono agli utenti di organizzare il contenuto basato su file in modo significativo e non limitato dall'organizzazione del file system. Quando il programma supporta le librerie, consente all'utente di trovare il contenuto in modo sensato durante la presentazione di un'interfaccia utente coerente con l'esperienza utente Windows 7. Le librerie semplificano inoltre al programma l'individuazione di contenuto basato su file archiviato in cartelle diverse o in computer diversi.

Negli argomenti di questa sezione viene descritto come aggiungere il supporto per le librerie al programma e sfruttare le nuove funzionalità offerte da librerie. Windows 7 offre parte di questo supporto per impostazione predefinita. Se il programma non modifica le finestre di dialogo di file comuni attualmente in uso, potrebbe essere necessaria una programmazione aggiuntiva molto piccola per supportare le librerie.

In questa sezione vengono descritte alcune delle funzionalità principali fornite nelle librerie e viene descritto come supportarle nel programma. Con queste informazioni, è possibile decidere quali funzionalità offriranno la migliore esperienza utente dal programma. Se il programma personalizza le finestre di dialogo di file comuni, le informazioni contenute in questa sezione consentono di determinare come usare le nuove finestre di dialogo file comuni per usare le librerie e fornire funzionalità equivalenti in Windows 7.

## <a name="programming-with-libraries"></a>Programmazione con librerie

Il Windows di programmazione shell descrive il modo in cui un programma interagisce con Windows di programmazione shell. Mentre gli oggetti del file system, ad esempio file e directory, sono rappresentati da oggetti shell Windows, non tutti gli oggetti Windows Shell sono rappresentati dal file system. Le librerie, ad esempio, Windows shell che non hanno un equivalente del file system. L Windows di shell nel programma consente al programma di accedere a tutti gli oggetti shell e non solo agli oggetti del file system.

Per ottenere risultati ottimali, il programma userebbe [**l'API Shell Library**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) per interagire con le librerie e accedere al relativo contenuto. Sebbene le librerie contengano elementi del file system, ad esempio cartelle e file, le librerie non sono elementi del file system. Di conseguenza, le API del file system non possono essere usate per accedere alle funzionalità della libreria o al contenuto della libreria.

Se si dispone di un programma esistente che attualmente usa molte API del file system, il programma può comunque sfruttare le funzionalità della libreria. [**L'API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) Shell Library può fornire riferimenti al file system agli elementi presenti in una libreria e questi riferimenti al file system, ad esempio il nome e il percorso, possono essere passati alle API del file system esistenti presenti nel programma esistente.

### <a name="moving-from-known-folders-to-libraries"></a>Spostamento da cartelle note a librerie

Prima Windows 7 era comune usare una cartella nota, ad esempio la cartella Documenti, come cartella predefinita nelle operazioni di salvataggio o apertura file. In Windows 7, è consigliabile usare la libreria corrispondente in modo che l'utente abbia la stessa esperienza nel programma in uso con altri programmi Windows 7, ad esempio Windows Explorer.

Se attualmente si usa l'API shell Windows nel programma, l'aggiunta del supporto della libreria è semplice. Ad esempio, se attualmente si chiama la funzione [**SHGetKnownFolderItem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) per ottenere il percorso della cartella Documenti, è possibile sostituire il valore [**KNOWNFOLDERID**](knownfolderid.md) della cartella nota Documenti con il **valore KNOWNFOLDERID** della libreria corrispondente.

Nella tabella seguente viene illustrata la relazione tra i valori [**KNOWNFOLDERID**](knownfolderid.md) delle cartelle note e il **valore KNOWNFOLDERID** della libreria corrispondente in Windows 7. 

| Valori known folder KNOWNFOLDERID | Valori KNOWNFOLDERID della libreria |
|-----------------------------------|------------------------------|
| Documenti \_ FOLDERID               | FOLDERID \_ DocumentsLibrary   |
| Immagini \_ FOLDERID                | FOLDERID \_ PicturesLibrary    |
| FOLDERID \_ Musica                   | FOLDERID \_ MusicLibrary       |
| FOLDERID \_ RecordedTV              | FOLDERID \_ RecordedTVLibrary  |



 

### <a name="homegroup-and-shared-libraries"></a>HomeGroup e librerie condivise

L'aggiunta del supporto della libreria al programma abiliterà il supporto per le librerie condivise in un gruppo Home. Il gruppo Home è identificato dal [**relativo valore KNOWNFOLDERID**](knownfolderid.md) [**di FOLDERID \_ HomeGroup**](knownfolderid.md). Il programma può individuare il percorso di salvataggio predefinito privato o condiviso dell'utente impostando il [**valore DEFAULTSAVEFOLDERTYPE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype) nella chiamata al metodo [**IShellLibrary::GetDefaultSaveFolder.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder)

## <a name="using-a-common-file-dialog-box-with-libraries"></a>Uso di una finestra di dialogo file comune con le librerie

Uso di una finestra di dialogo file comune con librerie La finestra di dialogo File comune è stata aggiornata per supportare le librerie Windows 7. La figura seguente mostra come viene visualizzata la finestra di dialogo file comune a un utente in Windows 7.

![Screenshot della finestra di dialogo file comune che mostra le librerie](images/libraries-commonfiledialog.png)

In Windows 7, se il programma visualizza attualmente una finestra di dialogo di file comune e non modifica il modello di finestra di dialogo o esegue l'hook di uno dei relativi eventi, verrà visualizzata automaticamente la nuova versione Windows 7 della finestra di dialogo. In particolare, nella chiamata alla funzione della finestra di dialogo file comune, i membri **lpfnHook**, **hInstance**, **lpTemplatename** della struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) devono essere **NULL** e i flag **\_ OFN ENABLEHOOK** e **OFN \_ ENABLETEMPLATE** devono essere deselezionati.

In Windows 7, le interfacce correlate a [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)sostituiscono le funzioni comuni della finestra di dialogo dei file usate nelle versioni precedenti di Windows. Le funzioni della finestra di dialogo file comuni precedenti sono ancora supportate in Windows 7, ma non forniscono l'esperienza utente completa Windows 7 e non supportano le librerie. Alcune delle nuove funzionalità supportate dalle **interfacce correlate a IFileDialog** includono:

-   L'utente può accedere alle proprietà dei file supportate dal Windows 7 Windows Explorer per cercare e selezionare i file.
-   Il programma può usare interfacce e metodi dell'API dello spazio dei nomi Shell per usare gli elementi.
-   Il programma può usare un modello di personalizzazione basato sui dati anziché un modello di personalizzazione basato su file di risorse per aggiungere nuovi controlli alle finestre di dialogo di file comuni.

È consigliabile usare [**le interfacce correlate a IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)quando:

-   è necessario personalizzare la finestra di dialogo file comune per il programma in Windows 7. In questo modo il programma può usare le librerie e supportare la personalizzazione della finestra di dialogo.
-   si vuole che l'utente sia in grado di selezionare più file da una finestra di dialogo di file comune. In questo modo si otterrà i percorsi corretti per l'oggetto selezionato perché una libreria può avere contenuto archiviato in cartelle diverse.

Per altre informazioni sulle [**interfacce correlate a IFileDialog,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)vedere:

-   [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a>Abilitazione della selezione della libreria dall'interfaccia utente

Se il programma consente all'utente di selezionare una cartella, ad esempio per le funzioni di importazione o esportazione, in Windows 7 dovrebbe consentire all'utente di selezionare anche una libreria. [**L'interfaccia IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) e la [**funzione SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) consentono all'utente di selezionare una libreria quando viene richiesto di selezionare una cartella. **L'interfaccia IFileOpenDialog** è preferibile alla funzione **SHBrowseForFolder** perché **IFileOpenDialog** supporta l'interfaccia utente Windows 7.

Per consentire agli utenti di selezionare cartelle quando si usa [**l'interfaccia IFileOpenDialog,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) chiamare SetOptions con il flag FOS PICKFOLDERS impostato e assicurarsi che il \_ flag FOS \_ FORCEFILESYSTEM sia deselezionato.


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



Per consentire agli utenti di selezionare cartelle quando chiamano la funzione SHBrowseForFolder, nel membro ulFlags della struttura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) impostare il flag BIF USENEWUI e cancellare il \_ flag BIF \_ RETURNONLYFSDIRS.


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a>Accesso al contenuto della libreria in un programma

Per accedere al contenuto di una libreria, è necessario usare l'API Windows Shell. Le funzioni dell'API del file system non possono essere usate per accedere al contenuto della libreria perché le librerie non sono oggetti del file system. Se il programma usa un browser di file personalizzato basato sull'API del file system, non sarà in grado di esplorare le librerie o accedere al contenuto della libreria.

Questa sezione descrive come accedere al contenuto della libreria in modo da poter selezionare il modo migliore per aggiornare il programma in modo che funzioni con le librerie.

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a>Accesso al contenuto della libreria con l'interfaccia IShellLibrary

Il modo più semplice per un programma di accedere al contenuto della libreria è usare [**l'API Shell Library**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary). Se si usa un programma che usa l'API del file system, **l'API** Libreria shell può restituire le cartelle del file system di una libreria, riducendo al minimo la modifica al codice del programma esistente.


```C++
IShellLibrary *picturesLibrary;

hr = SHLoadLibraryFromKnownFolder(FOLDERID_PicturesLibrary, 
                                  STGM_READ, 
                                  IID_PPV_ARGS(&picturesLibrary));

// picturesLibrary now points to the user's picture library
    
IShellItemArray *pictureFolders; 

hr = pslLibrary->GetFolders(LFF_FORCEFILESYSTEM, IID_PPV_ARGS(&pictureFolders));

// pictureFolders now contains an array of Shell items that
// represent the folders found in the user's pictures library
```



### <a name="accessing-library-content-with-the-shell-apis"></a>Accesso al contenuto della libreria con le API shell

Poiché gli oggetti libreria fanno parte del modello di programmazione Shell, possono essere usati con altre API Windows Shell. Ad esempio, è possibile usare le interfacce [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) e [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) nel programma, insieme alle funzioni helper correlate, per accedere al contenuto di una libreria nello stesso modo in cui si enumerano le cartelle e il contenuto delle cartelle per accedere al contenuto con le API file system.

Le WINDOWS Shell supportano due modalità di enumerazione per accedere al contenuto di una libreria:

-   **Enumerazione Browse**

    L'enumerazione Browse è la modalità di enumerazione predefinita ed enumera il contenuto di una cartella della libreria. Deselezionare il flag SHCONTF \_ NAVIGATION \_ ENUM per usare questa modalità.

-   **Enumerazione di navigazione**

    L'enumerazione di navigazione enumera le cartelle della libreria. Impostare il flag SHCONTF \_ NAVIGATION \_ ENUM per usare questa modalità.

Se il programma usa un controllo albero personalizzato per esplorare le cartelle dell'utente, l'enumerazione delle cartelle nella modalità di enumerazione di navigazione offrirà un elenco delle cartelle di una libreria coerente con il modo in cui esplora Windows enumera le cartelle in Windows 7.

Per esempi su come utilizzare queste funzionalità in un programma, vedere l'esempio ShellStorage in Windows SDK.

## <a name="saving-user-content-in-a-library"></a>Salvataggio del contenuto utente in una raccolta

Il programma può salvare il contenuto dell'utente in una libreria e in una cartella della libreria. Analogamente, l'utente può salvare in una cartella specifica in una libreria o semplicemente salvarla nella libreria.

Ogni libreria ha una cartella designata come percorso di salvataggio predefinito. Il percorso di salvataggio predefinito viene definito al momento della creazione della libreria. tuttavia l'utente può riassegnare il percorso di salvataggio predefinito come qualsiasi cartella nella libreria. Anche se l'utente non deve configurare un percorso di salvataggio predefinito, ha la possibilità di modificarlo. Se l'utente elimina la cartella attualmente impostata come percorso di salvataggio predefinito, la libreria configurerà automaticamente la cartella successiva nella libreria come percorso di salvataggio predefinito.

Esistono diversi modi per salvare il contenuto utente in una raccolta.

-   **Shell API**

    Se si usa il modello di programmazione Shell e si salva un elemento Shell, come rappresentato da [**IShellItem,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)IStorage o IStream, in un oggetto libreria, l'elemento Shell verrà archiviato automaticamente nel percorso di salvataggio predefinito della libreria.

-   **API del file system**

    Se si dispone di un programma esistente che usa molte chiamate API del file system, è possibile ottenere un percorso alla cartella definita come percorso di salvataggio predefinito della libreria. Il percorso della cartella può quindi essere passato a un'API del file system.

Per esempi su come utilizzare queste funzionalità in un programma, vedere l'esempio ShellStorage in Windows SDK.

## <a name="supporting-drag-and-drop-operations-in-a-library"></a>Supporto delle operazioni di trascinamento della selezione in una libreria

Se il programma supporta le azioni di trascinamento della selezione, queste devono essere aggiornate per supportare l'interazione corretta con la libreria. Se un file viene rilasciato in una libreria, il file eliminato deve essere salvato nel percorso di salvataggio predefinito. Se una cartella viene rilasciata in una libreria, la cartella eliminata deve essere aggiunta come nuova cartella alla libreria. Se un file viene rilasciato in una cartella esistente che non è il percorso di salvataggio predefinito, il file deve essere aggiunto alla cartella selezionata.

Per esempi su come aggiungere il supporto della libreria per la funzionalità di trascinamento della selezione dei programmi, vedere l'esempio ShellLibraryCommandLine in Windows SDK.

## <a name="keeping-in-sync-with-a-library"></a>Mantenere la sincronizzazione con una libreria

Questo argomento descrive come un programma può mantenere aggiornata la visualizzazione del contenuto di una libreria.

### <a name="bulk-update"></a>Aggiornamento bulk

Poiché l'utente può modificare le cartelle di una libreria in modo interattivo quando il programma non è in esecuzione, il programma deve chiamare [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) quando inizia a individuare e archiviare le modifiche alla libreria. L'API Shell fornisce la funzione **SHResolveLibrary** per consentire a un programma di ottenere il contenuto corrente di una libreria e i percorsi correnti di tutte le cartelle che la libreria potrebbe contenere.

Si noti [**che SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) è una funzione di blocco che potrebbe richiedere molto tempo a seconda delle modifiche nella libreria. Di conseguenza, non deve essere chiamato da un thread dell'interfaccia utente.

Dopo che il programma è stato aggiornato, può quindi registrarsi per le notifiche di modifica per mantenere una visualizzazione corrente.

### <a name="shell-api-notification"></a>Notifica dell'API shell

L Windows API Shell di Windows fornisce la funzione [**SHChangeNotifyRegister,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) che è il modo preferito per ricevere una notifica ai processi non di servizio di una modifica nella libreria.

Per rilevare le modifiche agli elementi all'interno di una libreria usando l'API shell di Windows, chiamare [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) per registrare il programma per le notifiche delle modifiche apportate agli elementi in una cartella della libreria. Questa funzione può inviare una notifica al programma in caso di modifica in una libreria o solo in una libreria specifica. Le notifiche vengono inviate immediatamente quando viene modificata una libreria.

### <a name="file-system-api-notification"></a>Notifica dell'API del file system

Le notifiche del file system devono essere usate nei processi del servizio.

Per rilevare le modifiche apportate agli elementi in una libreria usando l'API del file system, enumerare le cartelle nella libreria e chiamare [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) per ogni cartella da monitorare. Il programma riceverà una notifica quando cambia una cartella monitorata. Per trovare il file specifico dei file modificati nella cartella, chiamare [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw). Per rilevare le modifiche nel file di descrizione della libreria, monitorare la cartella che lo contiene. Il file di descrizione della libreria è disponibile nella [**cartella LIBRERIE \_ FOLDERID.**](knownfolderid.md) Il file di descrizione della libreria, tuttavia, non deve essere aperto o modificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle librerie](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Collegamenti alla shell](./links.md)
</dt> <dt>

[Cartelle note](known-folders.md)
</dt> <dt>

[Schema di descrizione della libreria](library-schema-entry.md)
</dt> <dt>

[**IID \_ PPV \_ ARGS**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
