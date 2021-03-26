---
description: Un collegamento della shell è un oggetto dati che contiene informazioni utilizzate per accedere a un altro oggetto nello spazio dei nomi della shell&\# 8212, ovvero qualsiasi oggetto visibile tramite Esplora risorse.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Collegamenti Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327bcb425f998bcc2a4c0714118d4461ded253ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232114"
---
# <a name="shell-links"></a>Collegamenti Shell

Un *collegamento della shell* è un oggetto dati che contiene le informazioni utilizzate per accedere a un altro oggetto nello spazio dei nomi della shell, ovvero qualsiasi oggetto visibile tramite Esplora risorse. I tipi di oggetti a cui è possibile accedere tramite i collegamenti della shell includono file, cartelle, unità disco e stampanti. Un collegamento della shell consente a un utente o a un'applicazione di accedere a un oggetto da qualsiasi punto dello spazio dei nomi. Non è necessario che l'utente o l'applicazione conosca il nome e il percorso correnti dell'oggetto.

-   [Informazioni sui collegamenti della shell](#about-shell-links)
    -   [Risoluzione dei collegamenti](#link-resolution)
    -   [File di collegamento](#link-files)
    -   [Identificatori di elementi ed elenchi di identificatori](#item-identifiers-and-identifier-lists)
-   [Uso di collegamenti della shell](#using-shell-links)
    -   [Creazione di un collegamento e di un collegamento a una cartella in un file](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [Risoluzione di un collegamento](#resolving-a-shortcut)
    -   [Creazione di un collegamento a un oggetto non file](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a>Informazioni sui collegamenti della shell

L'utente crea un collegamento della shell scegliendo il comando **Crea collegamento** dal menu di scelta rapida di un oggetto. Il sistema crea automaticamente un'icona per il collegamento della shell combinando l'icona dell'oggetto con una piccola freccia (nota come icona della sovrapposizione dei collegamenti definita dal sistema) visualizzata nell'angolo inferiore sinistro dell'icona. Un collegamento della shell con un'icona viene definito collegamento. Tuttavia, i termini collegamento e collegamento della shell vengono spesso usati in modo interscambiabile. In genere, l'utente crea collegamenti per ottenere accesso rapido agli oggetti archiviati nelle sottocartelle o in cartelle condivise in altri computer. Ad esempio, un utente può creare un collegamento a un documento di Microsoft Word che si trova in una sottocartella e posizionare l'icona del collegamento sul desktop. L'utente può quindi aprire il documento facendo doppio clic sull'icona del collegamento. Se il documento viene spostato o rinominato dopo la creazione del collegamento, il sistema tenterà di aggiornare il collegamento alla successiva selezione dell'utente.

Le applicazioni possono inoltre creare e utilizzare collegamenti a Shell e collegamenti. Ad esempio, un'applicazione di elaborazione di testo può creare un collegamento alla Shell per implementare un elenco dei documenti usati più di recente. Un'applicazione crea un collegamento della shell usando l'interfaccia [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) per creare un oggetto collegamento della shell. L'applicazione usa l'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) per archiviare l'oggetto in un file o un flusso.

> [!Note]  
> Non è possibile usare [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) per creare un collegamento a un URL.

 

In questa panoramica viene descritta l'interfaccia [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) e viene illustrato come utilizzarla per creare e risolvere i collegamenti a Shell dall'interno di un'applicazione basata su Microsoft Win32. Poiché la progettazione dei collegamenti della shell si basa su OLE Component Object Model (COM), è necessario acquisire familiarità con i concetti di base della programmazione COM e OLE prima di leggere questa panoramica.

### <a name="link-resolution"></a>Risoluzione dei collegamenti

Se un utente crea un collegamento a un oggetto e il nome o il percorso dell'oggetto viene modificato in un secondo momento, il sistema esegue automaticamente i passaggi per aggiornare o risolvere il collegamento alla successiva selezione dell'utente. Tuttavia, se un'applicazione crea un collegamento della shell e lo archivia in un flusso, il sistema non tenta automaticamente di risolvere il collegamento. L'applicazione deve risolvere il collegamento chiamando il metodo [**IShellLink:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) .

Quando viene creato un collegamento alla shell, il sistema salva le informazioni sul collegamento. Quando si risolve un collegamento, in modo automatico o con una chiamata [**IShellLink:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) , il sistema recupera innanzitutto il percorso associato al collegamento della shell utilizzando un puntatore all'elenco di identificatori del collegamento della shell. Per ulteriori informazioni sull'elenco degli identificatori, vedere [identificatori di elemento ed elenchi di identificatori](#item-identifiers-and-identifier-lists). Il sistema cerca l'oggetto associato in tale percorso e, se trova l'oggetto, risolve il collegamento. Se il sistema non riesce a trovare l'oggetto, chiama sul servizio di [rilevamento dei collegamenti distribuiti e degli identificatori di oggetto](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT), se disponibile, per individuare l'oggetto. Se il servizio DLT non è disponibile o non è in grado di trovare l'oggetto, il sistema cerca nella stessa directory un oggetto con lo stesso tempo di creazione del file e gli stessi attributi ma con un nome diverso. Questo tipo di ricerca risolve un collegamento a un oggetto che è stato rinominato.

Se il sistema non è ancora in grado di trovare l'oggetto, Cerca le directory, il desktop e i volumi locali, cercando in modo ricorsivo l'albero di directory per un oggetto con lo stesso nome o ora di creazione. Se il sistema non trova ancora una corrispondenza, viene visualizzata una finestra di dialogo in cui viene richiesto all'utente la presenza di una posizione. Un'applicazione può eliminare la finestra di dialogo specificando il valore **SLR \_ Nessuna \_ interfaccia utente** in una chiamata a [**IShellLink:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).

### <a name="initialization-of-the-component-object-library"></a>Inizializzazione della libreria di oggetti componente

Prima che un'applicazione possa creare e risolvere i collegamenti, è necessario inizializzare la libreria di oggetti componente chiamando la funzione [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) . Ogni chiamata a **CoInitialize** richiede una chiamata corrispondente alla funzione [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , che deve essere chiamata da un'applicazione al momento della terminazione. La chiamata a **CoUninitialize** garantisce che l'applicazione non venga terminata fino a quando non riceve tutti i messaggi in sospeso.

### <a name="location-independent-names"></a>Nomi Location-Independent

Il sistema fornisce nomi indipendenti dalla posizione per i collegamenti della shell a oggetti archiviati in cartelle condivise. Se l'oggetto viene archiviato localmente, il sistema fornisce il percorso locale e il nome file per l'oggetto. Se l'oggetto viene archiviato in modalità remota, il sistema fornisce un nome di risorsa di rete Universal Naming Convention (UNC) per l'oggetto. Poiché il sistema fornisce nomi indipendenti dalla località, un collegamento della shell può fungere da nome universale per un file che può essere trasferito ad altri computer.

### <a name="link-files"></a>File di collegamento

Quando l'utente crea un collegamento a un oggetto scegliendo il comando **Crea collegamento** dal menu di scelta rapida dell'oggetto, Windows archivia le informazioni necessarie per accedere all'oggetto in un file di collegamento, ovvero un file binario con estensione lnk. Un file di collegamento contiene le informazioni seguenti:

-   Posizione (percorso) dell'oggetto a cui fa riferimento il collegamento, denominato oggetto corrispondente.
-   Directory di lavoro dell'oggetto corrispondente.
-   Elenco di argomenti passati dal sistema all'oggetto corrispondente quando il metodo [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) viene attivato per il collegamento.
-   Il comando show utilizzato per impostare lo stato di visualizzazione iniziale dell'oggetto corrispondente. Questo è uno dei valori SW \_ descritti in [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).
-   Posizione (percorso e indice) dell'icona del tasto di scelta rapida.
-   Stringa di descrizione del collegamento.
-   Tasto di scelta rapida per il collegamento.

Quando viene eliminato un file di collegamento, l'oggetto corrispondente non è interessato.

Se si crea un collegamento a un altro collegamento, il sistema copia semplicemente il file di collegamento anziché creare un nuovo file di collegamento. In questo caso, i tasti di scelta rapida non saranno indipendenti l'uno dall'altro.

Un'applicazione può registrare un'estensione di file come tipo di file di collegamento. Se un file ha un'estensione di file che è stata registrata come tipo di file di collegamento, il sistema aggiunge automaticamente l'icona della sovrapposizione dei collegamenti definita dal sistema, ovvero una piccola freccia, all'icona del file. Per registrare un'estensione di file in un tipo di file di collegamento, è necessario aggiungere il valore di nome utente alla descrizione del registro di sistema dell'estensione del nome di file, come illustrato nell'esempio riportato di seguito. Si noti che la shell deve essere riavviata per rendere effettiva l'icona della sovrimpressione. Il valore di di collegamento non ha alcun valore di dati.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a>Nomi dei collegamenti

Il nome del collegamento, che è una stringa visualizzata sotto l'icona del collegamento della shell, è in realtà il nome del file del collegamento stesso. L'utente può modificare la stringa di descrizione selezionandola e immettendo una nuova stringa.

### <a name="location-of-shortcuts-in-the-namespace"></a>Posizione dei collegamenti nello spazio dei nomi

Sul desktop o in qualsiasi punto dello spazio dei nomi della shell può esistere un collegamento. Analogamente, l'oggetto associato al collegamento può esistere anche in qualsiasi punto dello spazio dei nomi della shell. Un'applicazione può usare il metodo [**IShellLink:: SEPATH**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) per impostare il percorso e il nome file per l'oggetto associato e il metodo [**IShellLink:: GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) per recuperare il percorso e il nome file correnti per l'oggetto.

### <a name="shortcut-working-directory"></a>Directory di lavoro collegamento

La directory di lavoro è la directory in cui l'oggetto corrispondente di un collegamento carica o archivia i file quando l'utente non identifica una directory specifica. Un file di collegamento contiene il nome della directory di lavoro per l'oggetto corrispondente. Un'applicazione può impostare il nome della directory di lavoro per l'oggetto corrispondente usando il metodo [**IShellLink:: SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) e può recuperare il nome della directory di lavoro corrente per l'oggetto corrispondente usando il metodo [**IShellLink:: GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) .

### <a name="shortcut-command-line-arguments"></a>Argomenti della riga di comando di collegamento

Un file di collegamento contiene argomenti della riga di comando che la shell passa all'oggetto corrispondente quando l'utente seleziona il collegamento. Un'applicazione può impostare gli argomenti della riga di comando per un collegamento usando il metodo [**IShellLink:: Searguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) . È utile impostare gli argomenti della riga di comando quando l'applicazione corrispondente, ad esempio un linker o un compilatore, accetta flag speciali come argomenti. Un'applicazione può recuperare gli argomenti della riga di comando da un collegamento usando il metodo [**IShellLink:: GetArguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) .

### <a name="shortcut-show-commands"></a>Comandi di visualizzazione collegamento

Quando l'utente fa doppio clic su un collegamento, il sistema avvia l'applicazione associata all'oggetto corrispondente e imposta lo stato di visualizzazione iniziale dell'applicazione in base al comando Mostra specificato dal collegamento. Il comando show può essere uno qualsiasi dei \_ valori SW inclusi nella descrizione della funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) . Un'applicazione può impostare il comando show per un tasto di scelta rapida usando il metodo [**IShellLink:: SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) e può recuperare il comando show corrente usando il metodo [**IShellLink:: GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) .

### <a name="shortcut-icons"></a>Icone di collegamento

Analogamente ad altri oggetti della shell, un collegamento presenta un'icona. L'utente accede all'oggetto associato a un tasto di scelta rapida facendo doppio clic sull'icona del collegamento. Quando il sistema crea un'icona per un collegamento, usa la bitmap dell'oggetto corrispondente e aggiunge l'icona della sovrapposizione dei collegamenti definita dal sistema (una piccola freccia) nell'angolo in basso a sinistra. Un'applicazione può impostare la posizione (percorso e indice) dell'icona di un tasto di scelta rapida usando il metodo [**IShellLink:: SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) . Un'applicazione può recuperare questo percorso usando il metodo [**IShellLink:: GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) .

### <a name="shortcut-descriptions"></a>Descrizioni dei collegamenti

I collegamenti includono descrizioni, ma l'utente non le Visualizza. Un'applicazione può usare una descrizione per archiviare le informazioni di testo. Le descrizioni vengono impostate usando il metodo [**IShellLink:: sedescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) e recuperate usando il metodo [**IShellLink:: GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) .

### <a name="shortcut-keyboard-shortcuts"></a>Tasti di scelta rapida

A un oggetto collegamento può essere associato un tasto di scelta rapida. Le scelte rapide da tastiera consentono a un utente di premere una combinazione di tasti per attivare un collegamento. Un'applicazione può impostare il tasto di scelta rapida per un tasto di scelta rapida usando il metodo [**IShellLink:: sehotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) ed è in grado di recuperare il tasto di scelta rapida corrente usando il metodo [**IShellLink:: GetHotKey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) .

### <a name="item-identifiers-and-identifier-lists"></a>Identificatori di elementi ed elenchi di identificatori

La shell usa gli identificatori di oggetto nello spazio dei nomi della shell. Tutti gli oggetti visibili nella shell (file, directory, server, gruppi di lavoro e così via) hanno identificatori univoci tra gli oggetti all'interno della cartella padre. Questi identificatori sono denominati identificatori di elemento e hanno il tipo di dati [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) come definito nel file di intestazione shtypes. h. Un identificatore di elemento è un flusso di byte a lunghezza variabile che contiene informazioni che identificano un oggetto all'interno di una cartella. Solo l'autore di un identificatore di elemento conosce il contenuto e il formato dell'identificatore. L'unica parte di un identificatore di elemento usato dalla shell è costituita dai primi due byte, che specificano la dimensione dell'identificatore.

Ogni cartella padre ha un identificatore di elemento che lo identifica all'interno della propria cartella padre. Pertanto, qualsiasi oggetto Shell può essere identificato in modo univoco da un elenco di identificatori di elemento. Una cartella padre mantiene un elenco di identificatori per gli elementi in esso contenuti. L'elenco include il tipo di dati [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Gli elenchi di identificatori di elemento vengono allocati dalla shell e possono essere passati tra le interfacce della shell, ad esempio [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder). È importante ricordare che ogni identificatore in un elenco di identificatori di elemento è significativo solo all'interno del contesto della relativa cartella padre.

Un'applicazione può impostare un elenco di identificatori di elemento di un collegamento usando il metodo [**IShellLink:: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) . Questo metodo è utile quando si imposta un collegamento a un oggetto che non è un file, ad esempio una stampante o un'unità disco. Un'applicazione può recuperare un elenco di identificatori di elemento di un collegamento usando il metodo [**IShellLink:: GetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) .

## <a name="using-shell-links"></a>Uso di collegamenti della shell

In questa sezione sono contenuti esempi che illustrano come creare e risolvere i collegamenti da un'applicazione basata su Win32. In questa sezione si presuppone che l'utente abbia familiarità con la programmazione Win32, C++ e OLE COM.

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a>Creazione di un collegamento e di un collegamento a una cartella in un file

La funzione di esempio CreateLink nell'esempio seguente crea un collegamento. I parametri includono un puntatore al nome del file a cui collegarsi, un puntatore al nome del collegamento che si sta creando e un puntatore alla descrizione del collegamento. La descrizione è costituita dalla stringa "collegamento al **nome file**", dove **nome file** è il nome del file a cui collegarsi.

Per creare un collegamento alla cartella utilizzando la funzione di esempio CreateLink, chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) utilizzando CLSID \_ FOLDERSHORTCUT, anziché CLSID \_ ShellLink (CLSID \_ FolderShortcut supporta IShellLink). Tutto il resto del codice rimane invariato.

Poiché CreateLink chiama la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , si presuppone che la funzione [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) sia già stata chiamata. CreateLink usa l'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) per salvare il collegamento e l'interfaccia [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) per archiviare il nome e la descrizione del file.


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a>Risoluzione di un collegamento

È possibile che un'applicazione debba accedere e modificare un collegamento creato in precedenza. Questa operazione viene definita risoluzione del collegamento.

La funzione ResolveIt definita dall'applicazione nell'esempio seguente risolve un collegamento. I parametri includono un handle di finestra, un puntatore al percorso del collegamento e l'indirizzo di un buffer che riceve il nuovo percorso dell'oggetto. L'handle della finestra identifica la finestra padre per le finestre di messaggio che possono essere visualizzate dalla Shell. La shell, ad esempio, può visualizzare una finestra di messaggio se il collegamento si trova su un supporto non condiviso, se si verificano problemi di rete, se l'utente deve inserire un disco floppy e così via.

La funzione ResolveIt chiama la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e presuppone che la funzione [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) sia già stata chiamata. Si noti che ResolveIt deve usare l'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) per archiviare le informazioni sul collegamento. **IPersistFile** viene implementato dall'oggetto [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) . È necessario caricare le informazioni sul collegamento prima di recuperare le informazioni sul percorso, come illustrato più avanti nell'esempio. Se non si caricano le informazioni sul collegamento, le chiamate alle funzioni membro [**IShellLink:: GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) e [**IShellLink:: GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) hanno esito negativo.


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a>Creazione di un collegamento a un oggetto non file

La creazione di un collegamento a un oggetto non file, ad esempio una stampante, è simile alla creazione di un collegamento a un file con la differenza che anziché impostare il percorso del file, è necessario impostare l'elenco di identificatori sulla stampante. Per impostare l'elenco di identificatori, chiamare il metodo [**IShellLink:: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) , specificando l'indirizzo di un elenco di identificatori.

Ogni oggetto nello spazio dei nomi della shell ha un identificatore di elemento. La shell spesso concatena gli identificatori di elemento in elenchi con terminazione null costituiti da un numero qualsiasi di identificatori di elemento. Per ulteriori informazioni sugli identificatori di elemento, vedere [identificatori di elemento ed elenchi di identificatori](#item-identifiers-and-identifier-lists).

In generale, se è necessario impostare un collegamento a un elemento che non ha un nome file, ad esempio una stampante, sarà già presente un puntatore all'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) dell'oggetto. **IShellFolder** viene utilizzato per creare estensioni dello spazio dei nomi.

Una volta ottenuto l'identificatore di classe per [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), è possibile chiamare la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per recuperare l'indirizzo dell'interfaccia. È quindi possibile chiamare l'interfaccia per enumerare gli oggetti nella cartella e recuperare l'indirizzo dell'identificatore di elemento per l'oggetto che si sta cercando. Infine, è possibile usare l'indirizzo in una chiamata alla funzione membro [**IShellLink:: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) per creare un collegamento all'oggetto.

 

 
