---
description: La Shell offre diversi modi per gestire i file System.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Gestione del file System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404b456ce1f26c128e6c3fc3bc9971672378a0d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342431"
---
# <a name="managing-the-file-system"></a>Gestione del file System

La Shell offre diversi modi per gestire i file System. La shell fornisce una funzione, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), che consente a un'applicazione di spostare, copiare, rinominare ed eliminare i file a livello di codice. La Shell supporta inoltre alcune funzionalità di gestione dei file aggiuntive.

-   I documenti HTML possono essere *connessi* a file correlati, ad esempio file di grafica o fogli di stile. Quando il documento viene spostato o copiato, anche i file connessi vengono spostati o copiati automaticamente.
-   Per i sistemi disponibili per più di un utente, i file possono essere gestiti in base ai singoli utenti. Gli utenti possono accedere facilmente ai file di dati, ma non ai file appartenenti ad altri utenti.
-   Se i file di documento vengono aggiunti o modificati, è possibile aggiungerli all'elenco dei documenti recenti della shell. Quando l'utente fa clic sul comando **documenti** nel menu Start, viene visualizzato un elenco di collegamenti ai documenti.

In questo documento viene illustrato il funzionamento di queste tecnologie di gestione file. Viene quindi descritto come utilizzare la Shell per spostare, copiare, rinominare ed eliminare i file e come gestire gli oggetti nel Cestino.

-   [Gestione file per utente](#per-user-file-management)
-   [Cartelle documenti e immagini personali](#my-documents-and-my-pictures-folders)
-   [File connessi](#connected-files)
-   [Trasferimento, copia, ridenominazione ed eliminazione di file](#moving-copying-renaming-and-deleting-files)
    -   [Notifica della shell](#notifying-the-shell)
-   [Esempio semplice di gestione dei file con SHFileOperation](#simple-example-of-managing-files-with-shfileoperation)
-   [Aggiunta di file all'elenco di documenti recenti della shell](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a>Gestione dei file Per-User

La shell di Windows 2000 consente di associare i file a un utente specifico, in modo che i file rimangano nascosti ad altri utenti. In termini di file system, i file vengono archiviati nella cartella del profilo dell'utente, in genere C: \\ Documents and Settings \\ *username* \\ nei sistemi Windows 2000. Questa funzionalità consente a molti utenti di utilizzare lo stesso computer, mantenendo al tempo stesso la privacy dei file di altri utenti. Diversi utenti possono avere programmi diversi. Fornisce inoltre agli amministratori e alle applicazioni un modo semplice per archiviare elementi quali l'inizializzazione (INI) o i file di collegamento (lnk). Le applicazioni possono quindi mantenere uno stato diverso per ogni utente e recuperare facilmente lo stato specifico quando necessario. È disponibile anche una cartella del profilo per archiviare le informazioni comuni a tutti gli utenti.

Poiché non è pratico determinare quale utente è connesso e dove si trovano i file, le cartelle standard per utente sono cartelle speciali e sono identificate da un [**CSIDL**](csidl.md). Ad esempio, il CSIDL per la cartella dei file di programma per utente è CSIDL \_ Programs. Se l'applicazione chiama [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con uno dei CSIDL per utente, la funzione restituisce il puntatore a un elenco di identificatori di elemento (PIDL) o a un percorso appropriato per l'utente attualmente connesso. Se l'applicazione deve recuperare il percorso o PIDL della cartella del profilo, il relativo CSIDL è **CSIDL \_ profilo**.

## <a name="my-documents-and-my-pictures-folders"></a>Cartelle documenti e immagini personali

Una delle icone standard trovate sul desktop è la **mia documentazione**. Quando si apre questa cartella, contiene i file di documento dell'utente corrente. L'istanza desktop dei documenti è una cartella virtuale, ovvero un alias per il file system percorso usato per archiviare fisicamente i documenti dell'utente, situato immediatamente sotto il desktop nella gerarchia dello spazio dei nomi.

Lo scopo delle cartelle documenti e immagini è quello di fornire agli utenti un modo semplice e sicuro per accedere ai file di documenti e immagini in un sistema che potrebbe avere più utenti. A ogni utente vengono assegnate cartelle di file system separate per i propri file. Ad esempio, la posizione della cartella documenti di un utente nel file system è in genere simile a C: \\ Documents and Settings \\ *username* \\ My Documents. Non è necessario che gli utenti conoscano la posizione fisica delle cartelle file system. Si limitano ad accedere ai file tramite l'icona documenti.

> [!Note]  
> Documenti consente a un utente di accedere ai propri file ma non a quelli di altri utenti. Se più persone utilizzano lo stesso computer, un amministratore può bloccare gli utenti partendo dall'file system in cui sono archiviati i file effettivi. Gli utenti potranno quindi lavorare nei propri documenti tramite la cartella documenti, ma non nei documenti che appartengono ad altri utenti.

 

Non è in genere necessario che un'applicazione conosca quale utente è connesso o dove si trova nella file system cartella documenti dell'utente. Al contrario, l'applicazione può recuperare il PIDL dell'icona del desktop My Documents chiamando il metodo [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) del desktop. Il nome di analisi usato per identificare la cartella documenti non è un percorso di file, bensì:: {450D8FBA-AD25-11D0-98A8-0800361B1103}. L'espressione tra parentesi è il formato di testo del GUID documenti. Ad esempio, per recuperare il PIDL dei documenti, l'applicazione deve usare questa chiamata a **IShellFolder::P arsedisplayname**.


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



Una volta che l'applicazione dispone del PIDL documenti, può gestire la cartella in modo analogo a una normale cartella file system, enumerando gli elementi, analizzando, associando ed eseguendo qualsiasi altra operazione di cartella valida. La shell esegue automaticamente il mapping delle modifiche nei documenti o nelle relative sottocartelle alle cartelle file system appropriate.

Se l'applicazione deve accedere alla cartella file system effettiva che contiene i documenti dell'utente corrente, passare CSIDL \_ Personal a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation). La funzione restituisce il PIDL della cartella file system visualizzata nella cartella documenti dell'utente corrente.

## <a name="connected-files"></a>File connessi

I documenti HTML hanno spesso un certo numero di file di grafica associati, un file di foglio di stile, diversi file di Microsoft JScript (compatibili con ECMA 262 Language Specification) e così via. Quando si sposta o si copia il documento HTML primario, in genere si desidera spostare o copiare i file associati per evitare la suddivisione dei collegamenti. Sfortunatamente, finora non è stato possibile determinare quali file sono correlati a un documento HTML specifico, ad eccezione del fatto che analizzarne il contenuto. Per ovviare a questo problema, Windows 2000 fornisce un modo semplice per *connettere* un documento HTML primario al relativo gruppo di file associati. Se la connessione file è abilitata, quando il documento viene spostato o copiato tutti i relativi file connessi vengono associati.

Per creare un gruppo di file connessi, il documento primario deve avere un'estensione di file con estensione htm o HTML. Creare una sottocartella della cartella padre del documento primario. Il nome della sottocartella deve corrispondere al nome del documento primario, meno l'estensione. htm o. html, seguito da una delle estensioni elencate di seguito. Le estensioni usate più di frequente sono ". Files" o " \_ files". Ad esempio, se il documento primario è denominato MyDoc.htm, la denominazione della sottocartella "MyDoc \_ files" definisce la sottocartella come contenitore per i file connessi del documento. Se il documento primario viene spostato o copiato, anche la sottocartella e i relativi file vengono spostati o copiati.

Per alcune lingue, è possibile usare un equivalente localizzato di " \_ files" per creare una sottocartella per i file connessi. Nella tabella seguente sono elencate le stringhe valide che è possibile aggiungere al nome di un documento per creare una sottocartella di file connessi. Si noti che alcune di queste stringhe hanno '-' come primo carattere anziché come ' \_ ' o ' .'.



|              |               |                 |               |
|--------------|---------------|-----------------|---------------|
| " \_ archiviazioni" | " \_ arquivos"  | "si basa su" \_   | " \_ bylos"     |
| "-Dateien"   | " \_ datoteke"  | " \_ dosyalar"    | " \_ elemei"    |
| " \_ failid"   | " \_ non riuscito"     | " \_ fajlovi"     | " \_ ficheiros" |
| " \_ fichiers" | "-filer"      | ". Files"        | " \_ file"     |
| " \_ file"     | " \_ fitxers"   | " \_ fitxategiak" | " \_ pliki"     |
| " \_ Soubory"  | " \_ tiedostot" |                 |               |



 

> [!Note]  
> Questa funzionalità è sensibile al caso dell'estensione. Ad esempio, per l'esempio precedente, una sottocartella denominata "MyDoc \_ files" non verrà connessa a MyDoc.htm.

 

Se la connessione file è abilitata o disabilitata è controllata da un valore **reg \_ DWORD** , NoFileFolderConnection, della chiave del registro di sistema seguente.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

Questo valore non è normalmente definito e la connessione file è abilitata. Se necessario, è possibile disabilitare la connessione file aggiungendo questo valore alla chiave e impostandolo su 1. Per abilitare di nuovo la connessione file, impostare NoFileFolderConnection su zero.

> [!Note]  
> La connessione file deve in genere essere abilitata perché altre applicazioni potrebbero dipendere da tale connessione. Disabilitare la connessione file solo se assolutamente necessario.

 

## <a name="moving-copying-renaming-and-deleting-files"></a>Trasferimento, copia, ridenominazione ed eliminazione di file

Lo spazio dei nomi non è statico e le applicazioni in genere devono gestire il file system eseguendo una delle operazioni seguenti.

-   Copia di un oggetto in un'altra cartella.
-   Lo stato di un oggetto viene spostato in un'altra cartella.
-   Eliminazione di un oggetto.
-   Ridenominazione di un oggetto.

Tutte queste operazioni vengono eseguite con [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). Questa funzione accetta uno o più file di origine e produce file di destinazione corrispondenti. Nel caso dell'operazione di eliminazione, il sistema tenta di inserire i file eliminati nel Cestino.

È anche possibile spostare i file usando la funzionalità di [trascinamento della selezione](dragdrop.md) .

Per usare la funzione, è necessario compilare i membri di una struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) e passarla a [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). I membri chiave della struttura sono **pFrom** e **PTO**.

Il membro **pFrom** è una stringa con terminazione **null** doppia che contiene uno o più nomi di file di origine. Questi nomi possono essere percorsi completi o caratteri jolly standard di DOS, ad esempio \* . \* Sebbene questo membro sia dichiarato come stringa con terminazione **null**, viene usato come buffer per memorizzare più nomi di file. Ogni nome file deve terminare con il consueto carattere **null** singolo. È necessario aggiungere un carattere **null** aggiuntivo alla fine del nome finale per indicare la fine di **pFrom**.

Il membro **PTO** è una stringa con terminazione **null** doppia, molto simile a **pFrom**. Il membro **PTO** contiene i nomi di uno o più nomi di destinazione completi. Vengono compressi in **PTO** nello stesso modo in cui sono disponibili per **pFrom**. Se **PTO** contiene più nomi, è necessario impostare anche il flag **FOF \_ MULTIDESTFILES** nel membro **fFlags** . L'utilizzo di **PTO** dipende dall'operazione descritta qui.

-   Per le operazioni di copia e spostamento, se tutti i file passano a una singola directory, **PTO** contiene il nome completo della directory. Se i file passano a destinazioni diverse, **PTO** può anche contenere una directory o un nome di file completo per ogni file di origine. Se una directory non esiste, verrà creata dal sistema.
-   Per le operazioni di ridenominazione, **PTO** contiene un percorso completo per ogni file di origine in **pFrom**.
-   Per le operazioni di eliminazione, non viene usato **PTO** .

### <a name="notifying-the-shell"></a>Notifica della shell

Inviare una notifica alla shell della modifica dopo aver usato [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) per spostare, copiare, rinominare o eliminare file oppure dopo aver eseguito altre azioni che influiscono sullo spazio dei nomi. Le azioni che devono essere accompagnate dalla notifica includono quanto segue:

-   Aggiunta o eliminazione di file o cartelle.
-   Trasferimento, copia o ridenominazione di file o cartelle.
-   Modifica di un'associazione di file.
-   Modifica degli attributi del file.
-   Aggiunta o rimozione di unità o supporti di archiviazione.
-   Creazione o disabilitazione di una cartella condivisa.
-   Modifica dell'elenco di immagini di sistema.

Un'applicazione invia una notifica alla shell chiamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con i dettagli delle modifiche apportate. La shell può quindi aggiornare l'immagine dello spazio dei nomi per riflettere accuratamente il nuovo stato.

## <a name="simple-example-of-managing-files-with-shfileoperation"></a>Esempio semplice di gestione dei file con SHFileOperation

Nell'applicazione console di esempio seguente viene illustrato l'uso di [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) per copiare i file da una directory a un'altra. Le directory di origine e di destinazione, C: \\ My \_ docs e c: \\ My \_ Docs2, sono hardcoded nell'applicazione per semplicità.


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



L'applicazione recupera innanzitutto un puntatore all'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del desktop. Recupera quindi il PIDL della directory di origine passando il percorso completo a [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname). Si noti che **IShellFolder::P arsedisplayname** richiede che il percorso della directory sia una stringa Unicode. L'applicazione viene quindi associata alla directory di origine e utilizza l'interfaccia **IShellFolder** per recuperare l'interfaccia [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) di un oggetto enumeratore.

Poiché ogni file nella directory di origine è enumerato, [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) viene usato per recuperare il nome. \_Viene impostato il flag SHGDN FORPARSING, che fa sì che **IShellFolder:: GetDisplayNameOf** restituisca il percorso completo del file. I percorsi dei file, inclusi i caratteri **null** di terminazione, vengono concatenati in una singola matrice, *szSourceFiles*. Un secondo carattere **null** viene aggiunto al percorso finale per terminare correttamente la matrice.

Al termine dell'enumerazione, l'applicazione assegna valori a una struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) . Si noti che la matrice assegnata a **PTO** per specificare la destinazione deve anche essere terminata da un **valore null** doppio. In questo caso, viene semplicemente incluso nella stringa assegnata a **PTO**. Poiché si tratta di un'applicazione console, i \_ flag FOF Silent, FOF \_ noconfirmation e FOF \_ NOCONFIRMMKDIR sono impostati in modo da non visualizzare le finestre di dialogo eventualmente visualizzate. Dopo la restituzione di [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) , viene chiamato [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) per notificare la shell della modifica. Quindi, l'applicazione esegue la normale pulizia e restituisce il risultato.

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a>Aggiunta di file all'elenco di documenti recenti della shell

La shell gestisce un elenco di documenti aggiunti o modificati di recente per ogni utente. L'utente può visualizzare un elenco di collegamenti a questi file scegliendo documenti dal menu Start. Come per i documenti, ogni utente dispone di una directory file system per il collegamento dei collegamenti effettivi. Per recuperare il PIDL della directory recente dell'utente corrente, l'applicazione può chiamare [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) con CSIDL \_ recente oppure chiamare [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) per recuperare il percorso.

L'applicazione può enumerare il contenuto della cartella recente usando le tecniche descritte in precedenza in questo documento. Tuttavia, un'applicazione non deve modificare il contenuto della cartella come se si trattasse di una normale cartella file system. In tal caso, l'elenco dei documenti recenti della shell non verrà aggiornato correttamente e le modifiche non verranno riflesse nel menu Start. Per aggiungere un collegamento a un documento alla cartella recente di un utente, l'applicazione può invece chiamare [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). La Shell consente di aggiungere un collegamento alla cartella file system appropriata, nonché di aggiornare l'elenco dei documenti recenti e il menu Start. È anche possibile usare questa funzione per cancellare la cartella.

 

 
