---
description: Questo argomento descrive alcuni aspetti da considerare quando si usano le librerie nel programma.
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: Uso delle librerie nel programma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2812a66b148d9bd16fc3951efab64a4d37afaaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350356"
---
# <a name="using-libraries-in-your-program"></a>Uso delle librerie nel programma

Questo argomento descrive alcuni aspetti da considerare quando si usano le librerie nel programma.

In questo argomento

-   [Panoramica della programmazione della libreria](#library-programming-overview)
-   [Programmazione con le librerie](#programming-with-libraries)
    -   [Passaggio da cartelle note a librerie](#moving-from-known-folders-to-libraries)
    -   [Gruppo Home e librerie condivise](#homegroup-and-shared-libraries)
-   [Utilizzo di una finestra di dialogo file comune con le librerie](#using-a-common-file-dialog-box-with-libraries)
-   [Abilitazione della selezione della libreria dall'interfaccia utente](#enabling-library-selection-from-the-user-interface)
-   [Accesso al contenuto della libreria in un programma](#accessing-library-content-in-a-program)
    -   [Accesso al contenuto della libreria con l'interfaccia IShellLibrary](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [Accesso al contenuto della libreria con le API della shell](#accessing-library-content-with-the-shell-apis)
-   [Salvataggio del contenuto utente in una raccolta](#saving-user-content-in-a-library)
-   [Supporto delle operazioni di trascinamento della selezione in una libreria](#supporting-drag-and-drop-operations-in-a-library)
-   [Mantenimento della sincronizzazione con una libreria](#keeping-in-sync-with-a-library)
    -   [Aggiornamento bulk](#bulk-update)
    -   [Notifica API shell](#shell-api-notification)
    -   [Notifica dell'API del file System](#file-system-api-notification)
-   [Argomenti correlati](#related-topics)

## <a name="library-programming-overview"></a>Panoramica della programmazione della libreria

Le librerie consentono agli utenti di organizzare il contenuto basato su file in modo significativo e non limitato dall'organizzazione del file system. Quando il programma supporta le librerie, consente all'utente di trovare il contenuto in modo che abbia senso, presentando un'interfaccia utente coerente con l'esperienza utente di Windows 7. Le librerie consentono inoltre al programma di individuare in modo più semplice contenuto basato su file archiviato in cartelle diverse o in computer diversi.

Negli argomenti di questa sezione viene descritto come aggiungere il supporto della libreria al programma e sfruttare le nuove funzionalità offerte dalle librerie. Windows 7 fornisce parte del supporto per impostazione predefinita. Se il programma non modifica le finestre di dialogo file comuni attualmente in uso, potrebbe essere necessaria una programmazione aggiuntiva minima per supportare le librerie.

In questa sezione vengono descritte alcune delle funzionalità chiave fornite dalle librerie e il modo in cui supportarle nel programma. Con queste informazioni, è possibile decidere quali funzionalità forniranno la migliore esperienza utente dal programma. Se il programma Personalizza le finestre di dialogo file comuni, le informazioni contenute in questa sezione consentono di determinare come utilizzare le nuove finestre di dialogo file comuni per utilizzare le librerie e fornire funzionalità equivalenti in Windows 7.

## <a name="programming-with-libraries"></a>Programmazione con le librerie

Il modello di programmazione shell di Windows descrive il modo in cui un programma interagisce con gli oggetti di programmazione della shell di Windows. Mentre gli oggetti di file System, ad esempio file e directory, sono rappresentati da oggetti della shell di Windows, non tutti gli oggetti della shell di Windows sono rappresentati dal file System. Le librerie, ad esempio, sono oggetti della shell di Windows che non hanno un equivalente del file System. L'uso di oggetti della shell di Windows nel programma consente al programma di accedere a tutti gli oggetti della shell e non solo a oggetti di file System.

Per ottenere risultati ottimali, il programma utilizzerà l' [**API della libreria della shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) per interagire con le librerie e accedere al contenuto. Mentre le librerie contengono elementi di file System, ad esempio cartelle e file, le librerie non sono elementi del file System. Di conseguenza, non è possibile utilizzare le API del file System per accedere alle funzionalità della libreria o al contenuto della raccolta.

Se si dispone di un programma esistente che attualmente usa molte API del file System, il programma può comunque sfruttare le funzionalità della libreria. L' [**API della libreria della shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) può fornire riferimenti a file System agli elementi presenti in una raccolta e questi riferimenti del file System, ad esempio il nome e il percorso del file, possono essere passati alle API del file System esistente presenti nel programma esistente.

### <a name="moving-from-known-folders-to-libraries"></a>Passaggio da cartelle note a librerie

Prima di Windows 7, era comune usare una cartella nota, ad esempio la cartella documenti, come cartella predefinita in operazioni di salvataggio file o file aperti. In Windows 7, è necessario utilizzare la libreria corrispondente in modo che l'utente abbia la stessa esperienza del programma in uso con altri programmi di Windows 7, ad esempio Esplora risorse.

Se attualmente si usa l'API shell di Windows nel programma, l'aggiunta del supporto per le librerie è semplice. Se, ad esempio, si chiama la funzione [**SHGetKnownFolderItem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) per ottenere il percorso della cartella documenti, è possibile sostituire il valore [**KNOWNFOLDERID**](knownfolderid.md) della cartella documenti nota con il valore **KNOWNFOLDERID** della libreria corrispondente.

Nella tabella seguente viene illustrata la relazione tra i valori [**KNOWNFOLDERID**](knownfolderid.md) delle cartelle note e il valore **KNOWNFOLDERID** della libreria corrispondente in Windows 7. 

| Valori KNOWNFOLDERID cartella nota | Valori KNOWNFOLDERID della libreria |
|-----------------------------------|------------------------------|
| \_Documenti FOLDERID               | \_DOCUMENTSLIBRARY FOLDERID   |
| Immagini di FOLDERID \_                | \_PICTURESLIBRARY FOLDERID    |
| \_Musica FOLDERID                   | \_MUSICLIBRARY FOLDERID       |
| \_RECORDEDTV FOLDERID              | \_RECORDEDTVLIBRARY FOLDERID  |



 

### <a name="homegroup-and-shared-libraries"></a>Gruppo Home e librerie condivise

L'aggiunta del supporto per la libreria al programma Abilita il supporto per le librerie condivise in un gruppo Home. Il gruppo Home è identificato dal relativo valore [**KNOWNFOLDERID**](knownfolderid.md) di [**FOLDERID \_ Gruppo Home**](knownfolderid.md). Il programma può individuare il percorso di salvataggio predefinito privato o condiviso dell'utente impostando il valore [**DEFAULTSAVEFOLDERTYPE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype) nella chiamata al metodo [**IShellLibrary:: GetDefaultSaveFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder) .

## <a name="using-a-common-file-dialog-box-with-libraries"></a>Utilizzo di una finestra di dialogo file comune con le librerie

Utilizzo di una finestra di dialogo file comune con le librerie la finestra di dialogo file comune è stata aggiornata per supportare le librerie in Windows 7. Nella figura seguente viene illustrato come viene visualizzata la finestra di dialogo file comune di un utente in Windows 7.

![screenshot della finestra di dialogo file comune che mostra le librerie](images/libraries-commonfiledialog.png)

In Windows 7, se il programma visualizza attualmente una finestra di dialogo file comune e non modifica il modello della finestra di dialogo o non associa alcun evento, verrà visualizzata automaticamente la nuova versione di Windows 7 della finestra di dialogo. In particolare, nella chiamata alla funzione della finestra di dialogo file comune i membri **lpfnHook**, **HINSTANCE**, **lpTemplatename** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) devono essere **null** **e i flag OFN ENABLEHOOK \_** e **OFN \_ ENABLETEMPLATE** devono essere cancellati.

In Windows 7 le interfacce correlate a [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)sostituiscono le funzioni della finestra di dialogo file comuni utilizzate nelle versioni precedenti di Windows. Le funzioni della finestra di dialogo file comuni precedenti sono ancora supportate in Windows 7 ma non offrono l'esperienza utente completa di Windows 7 e non supportano le librerie. Di seguito sono riportate alcune delle nuove funzionalità supportate dalle interfacce correlate a **IFileDialog**:

-   L'utente può accedere alle proprietà del file supportate da Esplora risorse di Windows 7 per la ricerca e la selezione dei file.
-   Il programma può usare interfacce e metodi dell'API dello spazio dei nomi della Shell per lavorare con gli elementi.
-   Il programma può utilizzare un modello di personalizzazione basato sui dati anziché un modello di personalizzazione basato sui file di risorse per aggiungere nuovi controlli alle finestre di dialogo file comuni.

È consigliabile usare le interfacce correlate a [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)nei casi seguenti:

-   è necessario personalizzare la finestra di dialogo file comune per il programma in Windows 7. Questo consentirà al programma di lavorare con le librerie e supportare la personalizzazione della finestra di dialogo.
-   si desidera che l'utente sia in grado di selezionare più file da una finestra di dialogo file comune. In questo modo si otterrà i percorsi corretti per l'oggetto selezionato perché una raccolta può includere contenuto archiviato in cartelle diverse.

Per ulteriori informazioni sulle interfacce correlate a [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), vedere:

-   [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a>Abilitazione della selezione della libreria dall'interfaccia utente

Se il programma consente all'utente di selezionare una cartella, ad esempio per le funzioni di importazione o esportazione, in Windows 7, deve consentire all'utente di selezionare anche una libreria. L'interfaccia [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) e la funzione [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) consentono all'utente di selezionare una libreria quando viene richiesto di selezionare una cartella. Per la funzione **SHBrowseForFolder** è preferibile l'interfaccia **IFileOpenDialog** , perché **IFileOpenDialog** supporta l'interfaccia utente di Windows 7.

Per consentire agli utenti di selezionare le cartelle quando si usa l'interfaccia [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) , chiamare SetOption con il \_ flag Fos PICKFOLDERS impostato e assicurarsi che il \_ flag Fos FORCEFILESYSTEM sia chiaro.


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



Per consentire agli utenti di selezionare le cartelle quando si chiama la funzione SHBrowseForFolder, nel membro ulFlags della struttura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) impostare il \_ flag BIF USENEWUI e deselezionare il \_ flag BIF RETURNONLYFSDIRS.


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a>Accesso al contenuto della libreria in un programma

Per accedere al contenuto di una raccolta, è necessario usare l'API shell di Windows. Non è possibile usare le funzioni dell'API del file System per accedere al contenuto della libreria perché le librerie non sono oggetti di file System. Se il programma usa un browser file personalizzato basato sull'API del file System, non sarà in grado di esplorare le librerie o accedere al contenuto della libreria.

In questa sezione viene descritto come accedere al contenuto della libreria in modo che sia possibile selezionare il modo migliore per aggiornare il programma per l'utilizzo delle librerie.

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a>Accesso al contenuto della libreria con l'interfaccia IShellLibrary

Il modo più semplice per accedere al contenuto della libreria consiste nell'usare l' [**API della libreria della shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary). Se si sta lavorando a un programma che usa l'API del file System, l' **API della libreria shell** può restituire le cartelle del file System di una libreria, riducendo al minimo la modifica apportata al codice del programma esistente.


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



### <a name="accessing-library-content-with-the-shell-apis"></a>Accesso al contenuto della libreria con le API della shell

Poiché gli oggetti libreria fanno parte del modello di programmazione della shell, possono essere usati con altre API della shell di Windows. Ad esempio, è possibile usare le interfacce [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) e [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) nel programma, insieme alle funzioni di supporto correlate, per accedere al contenuto di una libreria allo stesso modo in cui si enumerano le cartelle e il contenuto della cartella per accedere al contenuto con le API file System.

Le API della shell di Windows supportano due modalità di enumerazione per accedere al contenuto di una libreria:

-   **Esplora enumerazione**

    L'enumerazione Browse è la modalità di enumerazione predefinita ed enumera il contenuto di una cartella di libreria. \_ \_ Per utilizzare questa modalità, deselezionare il flag di enumerazione di navigazione SHCONTF.

-   **Enumerazione di navigazione**

    L'enumerazione di navigazione enumera le cartelle della libreria. Impostare il \_ \_ flag di enumerazione di navigazione SHCONTF per utilizzare questa modalità.

Se il programma utilizza un controllo albero personalizzato per spostarsi tra le cartelle dell'utente, l'enumerazione delle cartelle nella modalità di enumerazione di navigazione fornirà un elenco delle cartelle di una libreria coerenti con il modo in cui Esplora risorse enumera le cartelle in Windows 7.

Per esempi relativi all'uso di queste funzionalità in un programma, vedere l'esempio ShellStorage nel Windows SDK.

## <a name="saving-user-content-in-a-library"></a>Salvataggio del contenuto utente in una raccolta

Il programma può salvare il contenuto utente in una raccolta e in una cartella della libreria. Analogamente, l'utente può salvare in una cartella specifica in una raccolta o semplicemente salvarla nella libreria.

Ogni libreria ha una cartella che viene designata come percorso di salvataggio predefinito. Il percorso di salvataggio predefinito viene definito al momento della creazione della libreria. Tuttavia, l'utente può riassegnare il percorso di salvataggio predefinito come qualsiasi cartella della libreria. Mentre l'utente non deve configurare un percorso di salvataggio predefinito, è possibile modificarlo. Se l'utente elimina la cartella attualmente impostata come percorso di salvataggio predefinito, nella libreria la cartella successiva nella libreria verrà automaticamente configurata come percorso di salvataggio predefinito.

È possibile salvare il contenuto utente in una raccolta in diversi modi.

-   **API shell**

    Se si usa il modello di programmazione della shell e si salva un elemento della shell, come rappresentato da [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem), IStorage o IStream, in un oggetto libreria, l'elemento della shell verrà automaticamente archiviato nel percorso di salvataggio predefinito della libreria.

-   **API del file System**

    Se si dispone di un programma esistente che utilizza molte chiamate API del file System, è possibile ottenere il percorso della cartella definita come percorso di salvataggio predefinito della libreria. Il percorso della cartella può quindi essere passato a un'API del file System.

Per esempi relativi all'uso di queste funzionalità in un programma, vedere l'esempio ShellStorage nel Windows SDK.

## <a name="supporting-drag-and-drop-operations-in-a-library"></a>Supporto delle operazioni di trascinamento della selezione in una libreria

Se il programma supporta le operazioni di trascinamento della selezione, è necessario aggiornarle per supportare l'interazione corretta della libreria. Se un file viene rilasciato in una raccolta, il file eliminato deve essere salvato nel percorso di salvataggio predefinito. Se una cartella viene rilasciata in una raccolta, la cartella eliminata deve essere aggiunta come nuova cartella alla libreria. Se un file viene rilasciato in una cartella esistente che non è il percorso di salvataggio predefinito, il file deve essere aggiunto alla cartella selezionata.

Per esempi relativi all'aggiunta del supporto per le librerie per la funzionalità di trascinamento della selezione dei programmi, vedere l'esempio ShellLibraryCommandLine nel Windows SDK.

## <a name="keeping-in-sync-with-a-library"></a>Mantenimento della sincronizzazione con una libreria

In questo argomento viene descritto come un programma può rimanere aggiornato sul contenuto di una raccolta.

### <a name="bulk-update"></a>Aggiornamento bulk

Poiché l'utente può modificare le cartelle di una libreria in modo interattivo quando il programma non è in esecuzione, il programma deve chiamare [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) quando inizia a individuare e archiviare le modifiche apportate alla libreria. L'API shell fornisce la funzione **SHResolveLibrary** per consentire a un programma di ottenere il contenuto corrente di una raccolta e i percorsi correnti di tutte le cartelle che la libreria potrebbe contenere.

Si noti che [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) è una funzione di blocco che può richiedere molto tempo per la restituzione a seconda di ciò che è stato modificato nella libreria. Di conseguenza, non deve essere chiamato da un thread dell'interfaccia utente.

Dopo che il programma è stato aggiornato, è possibile registrarsi per le notifiche di modifica per mantenere una visualizzazione corrente.

### <a name="shell-api-notification"></a>Notifica API shell

L'API shell di Windows fornisce la funzione [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) , che rappresenta la modalità preferita per i processi non di servizio di ricevere una notifica di una modifica nella libreria.

Per rilevare le modifiche apportate agli elementi all'interno di una libreria tramite l'API della shell di Windows, chiamare [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) per registrare il programma per le notifiche delle modifiche apportate agli elementi in una cartella di libreria. Questa funzione può notificare al programma se è presente una modifica in qualsiasi libreria o solo in una libreria specifica. Le notifiche vengono inviate immediatamente quando viene modificata una libreria.

### <a name="file-system-api-notification"></a>Notifica dell'API del file System

Le notifiche del file System devono essere usate nei processi del servizio.

Per rilevare le modifiche apportate agli elementi di una raccolta tramite l'API del file System, enumerare le cartelle nella libreria e chiamare [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) per ogni cartella da monitorare. Il programma riceverà una notifica in caso di modifica di una cartella monitorata. Per trovare il file specifico di file modificato nella cartella, chiamare [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw). Per rilevare le modifiche nel file di descrizione della libreria, monitorare la cartella che lo contiene. Il file di descrizione della libreria si trova nella cartella [**FOLDERID \_ Libraries**](knownfolderid.md) . Il file di descrizione della libreria, tuttavia, non deve essere aperto o modificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle librerie](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Collegamenti Shell](./links.md)
</dt> <dt>

[Cartelle note](known-folders.md)
</dt> <dt>

[Schema Descrizione libreria](library-schema-entry.md)
</dt> <dt>

[**argomenti di IID \_ PPV \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
