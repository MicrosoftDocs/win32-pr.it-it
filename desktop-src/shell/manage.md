---
description: Shell offre diversi modi per gestire i file system.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Gestione del file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0f3b47e17e691c540a9775f3b8588b311b9878
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581619"
---
# <a name="managing-the-file-system"></a>Gestione del file system

Shell offre diversi modi per gestire i file system. Shell fornisce una funzione, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), che consente a un'applicazione di spostare, copiare, rinominare ed eliminare file a livello di codice. Shell supporta anche alcune funzionalità di gestione dei file aggiuntive.

-   I documenti HTML possono *essere connessi* a file correlati, ad esempio file di grafica o fogli di stile. Quando il documento viene spostato o copiato, anche i file connessi vengono spostati o copiati automaticamente.
-   Per i sistemi disponibili per più utenti, i file possono essere gestiti in base all'utente. Gli utenti possono accedere facilmente ai file di dati, ma non ai file appartenenti ad altri utenti.
-   Se i file di documento vengono aggiunti o modificati, possono essere aggiunti all'elenco di documenti recenti della shell. Quando l'utente fa clic **sul comando** Documenti nel menu Start, viene visualizzato un elenco di collegamenti ai documenti.

Questo documento illustra il funzionamento di queste tecnologie di gestione dei file. Descrive quindi come usare Shell per spostare, copiare, rinominare ed eliminare file e come gestire gli oggetti nel Cestino.

-   [Gestione file per utente](#per-user-file-management)
-   [cartelle Documenti e Immagini personali](#my-documents-and-my-pictures-folders)
-   [File connessi](#connected-files)
-   [Spostamento, copia, ridenominazione ed eliminazione di file](#moving-copying-renaming-and-deleting-files)
    -   [Notifica alla shell](#notifying-the-shell)
-   [Esempio semplice di gestione dei file con SHFileOperation](#simple-example-of-managing-files-with-shfileoperation)
-   [Aggiunta di file all'elenco di documenti recenti della shell](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a>Per-User Gestione file

La Windows 2000 Shell consente di associare i file a un determinato utente in modo che i file rimangano nascosti ad altri utenti. In termini di file system, i file vengono archiviati nella cartella del profilo dell'utente, in genere C: Documents e Impostazioni Username nei sistemi \\ \\  \\ Windows 2000. Questa funzionalità consente a molti utenti di usare lo stesso computer, mantenendo la privacy dei file di altri utenti. Per utenti diversi possono essere disponibili programmi diversi. Offre anche un modo semplice per gli amministratori e le applicazioni di archiviare elementi quali l'inizializzazione (.ini) o i file di collegamento (con estensione lnk). Le applicazioni possono quindi mantenere uno stato diverso per ogni utente e ripristinare facilmente tale stato specifico quando necessario. Esiste anche una cartella del profilo per l'archiviazione di informazioni comuni a tutti gli utenti.

Poiché è poco pratico determinare quale utente è connesso e dove si trovano i file, le cartelle standard per utente sono cartelle speciali e sono identificate da [**CSIDL**](csidl.md). Ad esempio, il linguaggio CSIDL per la cartella Programmi per utente è PROGRAMMI \_ CSIDL. Se l'applicazione chiama [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con uno dei CSIDL per utente, la funzione restituisce il puntatore a un elenco di identificatori di elemento (PIDL) o al percorso appropriato per l'utente attualmente connesso. Se l'applicazione deve recuperare il percorso o il file PIDL della cartella del profilo, CSIDL è **CSIDL \_ PROFILE**.

## <a name="my-documents-and-my-pictures-folders"></a>Documenti cartelle Immagini personali

Una delle icone standard presenti sul desktop è **Documenti**. Quando si apre questa cartella, contiene i file di documento dell'utente corrente. L'istanza desktop di Documenti è una cartella virtuale, ovvero un alias del percorso file system usato per archiviare fisicamente i documenti dell'utente, che si trova immediatamente sotto il desktop nella gerarchia dello spazio dei nomi.

Lo scopo delle cartelle Documenti e Immagini è fornire agli utenti un modo semplice e sicuro per accedere ai file di documenti e immagini in un sistema che potrebbe avere più utenti. A ogni utente vengono assegnate cartelle file system per i file. Ad esempio, il percorso della cartella documenti di un utente nel file system è in genere simile a C: Documenti e Impostazioni \\ \\ *nome utente* \\ Documenti. Non è necessario che gli utenti sappiano nulla sulla posizione fisica delle file system cartelle. È sufficiente accedere ai file tramite l'icona Documenti.

> [!Note]  
> Documenti consente a un utente di accedere ai propri file, ma non a quelli di altri utenti. Se più utenti usano lo stesso computer, un amministratore può bloccare gli utenti dalla parte del file system in cui sono archiviati i file effettivi. Gli utenti potranno quindi lavorare sui propri documenti tramite la cartella Documenti ma non sui documenti che appartengono ad altri utenti.

 

In genere non è necessario che un'applicazione sappia quale utente è connesso o dove si trova file system cartella Documenti dell'utente. L'applicazione può invece recuperare il file PIDL dell'icona del desktop Documenti chiamando il metodo [**IShellFolder::P arseDisplayName del**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) desktop. Il nome di analisi usato per identificare la cartella Documenti non è un percorso di file, ma piuttosto ::{450d8fba-ad25-11d0-98a8-0800361b1103}. L'espressione tra parentesi quadre è la forma di testo del GUID Documenti. Ad esempio, per recuperare il file PIDL di Documenti, l'applicazione deve usare questa chiamata a **IShellFolder::P arseDisplayName**.


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



Una volta che l'applicazione ha il Documenti PIDL, può gestire la cartella esattamente come una normale cartella file system, enumerando elementi, analizzando, associando ed eseguendo qualsiasi altra operazione di cartella valida. Shell esegue automaticamente il mapping delle Documenti o delle relative sottocartelle alle cartelle file system appropriate.

Se l'applicazione deve accedere alla cartella file system che contiene i documenti dell'utente corrente, passare CSIDL \_ PERSONAL a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation). La funzione restituisce il file PIDL della file system visualizzata nella cartella Documenti dell'utente corrente.

## <a name="connected-files"></a>File connessi

I documenti HTML hanno spesso una serie di file grafici associati, un file di foglio di stile, diversi file di Microsoft JScript (compatibili con la specifica del linguaggio ECMA 262) e così via. Quando si sposta o si copia il documento HTML primario, in genere si vogliono anche spostare o copiare i file associati per evitare collegamenti di rilievo. Sfortunatamente, finora non esisteva un modo semplice per determinare quali file sono correlati a un determinato documento HTML se non analizzandone il contenuto. Per risolvere questo problema, Windows 2000 offre un  modo semplice per connettere un documento HTML primario al gruppo di file associati. Se la connessione file è abilitata, quando il documento viene spostato o copiato, vengono associati tutti i file connessi.

Per creare un gruppo di file connessi, il documento primario deve avere un'estensione .htm o .html file. Creare una sottocartella della cartella padre del documento primario. Il nome della sottocartella deve essere il nome del documento primario, meno l'estensione .htm o .html, seguita da una delle estensioni elencate di seguito. Le estensioni usate più di frequente sono ".files" o \_ "files". Ad esempio, se il documento primario è denominato MyDoc.htm, il nome della sottocartella "File MyDoc" definisce la sottocartella come contenitore per i \_ file connessi del documento. Se il documento primario viene spostato o copiato, anche la sottocartella e i relativi file vengono spostati o copiati.

Per alcune lingue, è possibile usare un equivalente localizzato di \_ "file" per creare una sottocartella per i file connessi. Nella tabella seguente sono elencate le stringhe valide che possono essere aggiunte a un nome di documento per creare una sottocartella di file connessi. Si noti che alcune di queste stringhe hanno '-' come primo carattere anziché \_ '' o '.'.



:::row:::
   :::column span="":::
      \_"archivos"
   :::column-end:::
   :::column span="":::
      \_"arquivos"
   :::column-end:::
   :::column span="":::
      \_"bestanden"
   :::column-end:::
   :::column span="":::
      " \_ bylos"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      "-Dateien"
   :::column-end:::
   :::column span="":::
      \_"datoteke"
   :::column-end:::
   :::column span="":::
      \_"dosyalar"
   :::column-end:::
   :::column span="":::
      \_"elemei"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ failid"
   :::column-end:::
   :::column span="":::
      "ha \_ esito negativo"
   :::column-end:::
   :::column span="":::
      \_"fajlovi"
   :::column-end:::
   :::column span="":::
      \_"ficheiros"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      \_"fichiers"
   :::column-end:::
   :::column span="":::
      "-filer"
   :::column-end:::
   :::column span="":::
      ".files"
   :::column-end:::
   :::column span="":::
      \_"files"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      \_"file"
   :::column-end:::
   :::column span="":::
      \_"fitxers"
   :::column-end:::
   :::column span="":::
      \_"fitxategiak"
   :::column-end:::
   :::column span="":::
      \_"pliki"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      \_"soubory"
   :::column-end:::
   :::column span="":::
      \_"tiedostot"
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> Questa funzionalità è sensibile al caso dell'estensione. Ad esempio, per l'esempio indicato in precedenza, una sottocartella denominata "MyDoc Files" non verrà connessa a \_ MyDoc.htm.

 

Se la connessione file è abilitata o disabilitata è controllata da un valore **\_ DWORD REG,** NoFileFolderConnection, della chiave del Registro di sistema seguente.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

Questo valore in genere non è definito e la connessione file è abilitata. Se necessario, è possibile disabilitare la connessione file aggiungendo questo valore alla chiave e impostandola su 1. Per abilitare nuovamente la connessione file, impostare NoFileFolderConnection su zero.

> [!Note]  
> La connessione file deve in genere essere abilitata perché altre applicazioni potrebbero dipendere da essa. Disabilitare la connessione file solo se assolutamente necessario.

 

## <a name="moving-copying-renaming-and-deleting-files"></a>Spostamento, copia, ridenominazione ed eliminazione di file

Lo spazio dei nomi non è statico e le applicazioni in genere devono gestire file system eseguendo una delle operazioni seguenti.

-   Copia di un oggetto in un'altra cartella.
-   Spostamento di un oggetto in un'altra cartella.
-   Eliminazione di un oggetto.
-   Ridenominazione di un oggetto.

Queste operazioni vengono tutte eseguite con [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). Questa funzione accetta uno o più file di origine e produce i file di destinazione corrispondenti. Nel caso dell'operazione di eliminazione, il sistema tenta di inserire i file eliminati nel Cestino.

È anche possibile spostare i file usando la [funzionalità di trascinamento della](dragdrop.md) selezione.

Per usare la funzione , è necessario compilare i membri di una struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) e passarla [**a SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). I membri chiave della struttura sono **pFrom** e **pTo.**

Il **membro pFrom** è una stringa con terminazione **Null** doppia che contiene uno o più nomi di file di origine. Questi nomi possono essere percorsi completi o caratteri jolly DOS standard, ad esempio \* \* . Anche se questo membro è dichiarato come stringa con terminazione **Null,** viene usato come buffer per contenere più nomi di file. Ogni nome di file deve essere terminato dal singolo carattere **NULL** consueto. È necessario aggiungere un carattere **NULL** aggiuntivo alla fine del nome finale per indicare la fine di **pFrom.**

Il **membro pTo** è una stringa con terminazione **Null** doppia, in modo molto simile a **pFrom**. Il **membro pTo** contiene i nomi di uno o più nomi di destinazione completi. Vengono imballati in **pTo** nello stesso modo in cui sono per **pFrom**. Se **pTo** contiene più nomi, è necessario impostare anche il flag **\_ FOF MULTIDESTFILES** nel **membro fFlags.** L'utilizzo **di pTo** dipende dall'operazione come descritto di seguito.

-   Per le operazioni di copia e spostamento, se tutti i file vengono spostati in una singola directory, **pTo** contiene il nome completo della directory. Se i file vengono verso destinazioni diverse, **pTo** può contenere anche una directory o un nome file completo per ogni file di origine. Se non esiste una directory, il sistema la crea.
-   Per le operazioni di **ridenominazione, pTo** contiene un percorso completo per ogni file di origine in **pFrom**.
-   Per le operazioni di eliminazione, **pTo** non viene usato.

### <a name="notifying-the-shell"></a>Notifica alla shell

Notificare alla shell la modifica dopo l'uso di [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) per spostare, copiare, rinominare o eliminare file o dopo l'azione che interessa lo spazio dei nomi. Di seguito sono riportate le azioni che devono essere accompagnate da una notifica:

-   Aggiunta o eliminazione di file o cartelle.
-   Spostamento, copia o ridenominazione di file o cartelle.
-   Modifica di un'associazione di file.
-   Modifica degli attributi del file.
-   Aggiunta o rimozione di unità o supporti di archiviazione.
-   Creazione o disabilitazione di una cartella condivisa.
-   Modifica dell'elenco di immagini di sistema.

Un'applicazione invia una notifica alla shell chiamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con i dettagli delle modifiche. Shell può quindi aggiornare l'immagine dello spazio dei nomi in modo da riflettere in modo accurato il nuovo stato.

## <a name="simple-example-of-managing-files-with-shfileoperation"></a>Esempio semplice di gestione dei file con SHFileOperation

L'applicazione console di esempio seguente illustra l'uso di [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) per copiare file da una directory a un'altra. Le directory di origine e di destinazione, C: My Docs e \\ \_ C: \\ My \_ Docs2, sono hard-coded nell'applicazione per semplicità.


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



L'applicazione recupera innanzitutto un puntatore [**all'interfaccia IShellFolder del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) desktop. Recupera quindi il file PIDL della directory di origine passando il percorso completo a [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname). Si noti **che IShellFolder::P arseDisplayName** richiede che il percorso della directory sia una stringa Unicode. L'applicazione esegue quindi il binding alla directory di origine e usa la relativa **interfaccia IShellFolder** per recuperare l'interfaccia [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) di un oggetto enumeratore.

Quando ogni file nella directory di origine viene enumerato, viene usato [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per recuperarne il nome. Il flag SHGDN FORPARSING è impostato \_ e **IShellFolder::GetDisplayNameOf** restituisce il percorso completo del file. I percorsi di file, inclusi i caratteri **NULL** di terminazione, vengono concatenati in una singola matrice, *szSourceFiles*. Un secondo **carattere NULL** viene aggiunto al percorso finale per terminare correttamente la matrice.

Al termine dell'enumerazione, l'applicazione assegna valori a [**una struttura SHFILEOPSTRUCT.**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) Si noti che anche la matrice assegnata a **pTo** per specificare la destinazione deve essere terminata da un valore **NULL doppio.** In questo caso, viene semplicemente incluso nella stringa assegnata a **pTo**. Poiché si tratta di un'applicazione console, i flag FOF \_ SILENT, FOF \_ NOCONFIRMATION e FOF NOCONFIRMMKDIR sono impostati per eliminare eventuali finestre di dialogo che potrebbero \_ essere visualizzate. Al [**termine di SHFileOperation,**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) [**viene chiamato SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) per notificare la modifica alla shell. L'applicazione esegue quindi la pulizia consueta e restituisce .

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a>Aggiunta di file all'elenco di documenti recenti della shell

Shell gestisce un elenco di documenti aggiunti o modificati di recente per ogni utente. L'utente può visualizzare un elenco di collegamenti a questi file facendo clic su Documenti nel menu Start. Come per Documenti, ogni utente ha una directory file system per contenere i collegamenti effettivi. Per recuperare il FILE PIDL della directory Recent dell'utente corrente, l'applicazione può chiamare [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) con CSIDL \_ RECENT oppure chiamare [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) per recuperarne il percorso.

L'applicazione può enumerare il contenuto della cartella Recenti usando le tecniche descritte in precedenza in questo documento. Tuttavia, un'applicazione non deve modificare il contenuto della cartella come se fosse una normale file system cartella. In questo caso, l'elenco di documenti recenti della Shell non verrà aggiornato correttamente e le modifiche non verranno riflesse nel menu Start. Al contrario, per aggiungere un collegamento di documento alla cartella Recenti di un utente, l'applicazione può chiamare [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Shell aggiungerà un collegamento alla cartella file system appropriata, oltre ad aggiornare l'elenco dei documenti recenti e il menu Start. È anche possibile usare questa funzione per cancellare la cartella.

 

 
