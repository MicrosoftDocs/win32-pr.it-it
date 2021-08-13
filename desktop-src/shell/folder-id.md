---
description: Prima di poter usare un oggetto spazio dei nomi, è necessario un modo per identificarlo.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Recupero dell'ID di una cartella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d75051d52f0dfcee54b6365a8f546d2cbda2c3b5f7c0f4b6fbbc19fa1e40c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459010"
---
# <a name="getting-a-folders-id"></a>Recupero dell'ID di una cartella

Prima di poter usare un oggetto spazio dei nomi, è necessario un modo per identificarlo. Ciò significa ottenere il puntatore a un elenco di identificatori di elemento (PIDL) o, nel caso di oggetti file system, il relativo percorso. Questa sezione illustra due dei modi più semplici per ottenere gli ID oggetto.

Per un approccio più efficace che funzioni con qualsiasi cartella, usare [**l'interfaccia IShellFolder.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Per [altri dettagli, vedere Recupero di informazioni sul contenuto di](folder-info.md) una cartella.

-   [Finestra di dialogo OpenFiles](#the-openfiles-dialog-box)
-   [Finestra di dialogo SHBrowseForFolder](#the-shbrowseforfolder-dialog-box)
-   [Cartelle speciali e CSIDL](#special-folders-and-csidls)
-   [Semplice esempio di come usare CSIDLs e SHBrowseForFolder](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a>Finestra di dialogo OpenFiles

Per consentire all'utente di esplorare lo spazio dei nomi e selezionare una cartella, l'applicazione può usare [**l'interfaccia IFileDialog.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) Se si chiama questa interfaccia con il [](../dlgbox/open-and-save-as-dialog-boxes.md) flag **\_ FOS PICKFOLDERS,** viene visualizzata la finestra di dialogo comune Apri file in modalità "Seleziona cartelle".

Per Windows Vista e versioni successive, questo è il modo consigliato per selezionare le cartelle.

## <a name="the-shbrowseforfolder-dialog-box"></a>Finestra di dialogo SHBrowseForFolder

Per consentire all'utente di spostarsi nello spazio dei nomi e selezionare una cartella, l'applicazione può semplicemente richiamare [**SHBrowseForFolder.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) La chiamata a questa funzione avvia una finestra di dialogo con un'interfaccia utente che funziona in modo simile alle finestre di dialogo comuni Apri o [SalvaAs.](../dlgbox/open-and-save-as-dialog-boxes.md)

Quando l'utente seleziona una cartella, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) restituisce il file PIDL completo della cartella e il relativo nome visualizzato. Se la cartella si trova nel file system, l'applicazione può convertire il file PIDL in un percorso chiamando [**SHGetPathFromIDList.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista) L'applicazione può anche limitare l'intervallo di cartelle che l'utente può selezionare specificando una cartella radice. Verranno visualizzate solo le cartelle al di sotto della radice nello spazio dei nomi . La figura seguente mostra la **finestra di dialogo SHBrowseForFolder,** con la cartella radice impostata su Programmi.

![Screenshot della finestra di dialogo Cerca cartella](images/shell1.png)

Un semplice esempio di come usare [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) viene fornito più avanti.

## <a name="special-folders-and-csidls"></a>Cartelle speciali e CSIDL

Alcune cartelle di uso comune sono designate come *speciali* dal sistema. Queste cartelle hanno uno scopo ben definito e la maggior parte di esse sono presenti in tutti i sistemi. Anche se inizialmente non sono presenti, i relativi nomi e percorsi sono ancora definiti, quindi possono essere aggiunti in un secondo momento. La raccolta di cartelle speciali include tutte le cartelle virtuali standard del sistema, ad esempio Stampanti, Documenti e Network Neighborhood. Include anche una serie di cartelle di file system standard, ad esempio Programmi e Sistema.

Anche se le cartelle sono un componente standard di tutti i sistemi, i relativi nomi e percorsi nello spazio dei nomi possono variare. Ad esempio, la directory System è C: Winnt System32 in alcuni sistemi e \\ \\ C: \\ Windows \\ System32 in altri. In passato, le variabili di ambiente consentono di determinare il nome e il percorso di una cartella speciale in un sistema specifico. La shell offre ora un modo più affidabile e flessibile per identificare cartelle speciali, [**i CSIDL.**](csidl.md) In genere è consigliabile usarli al posto delle variabili di ambiente.

I CRL offrono un modo uniforme per identificare e individuare cartelle speciali, indipendentemente dal nome o dalla posizione in un particolare sistema. A differenza delle variabili di ambiente, i CSID possono essere usati con cartelle virtuali e file system cartelle. A ogni cartella speciale è assegnato un CSIDL univoco. Ad esempio, la cartella programmi file system ha un CSIDL di **CSIDL \_ PROGRAM \_ FILES** e la cartella virtuale Network Neighborhood ha un CSIDL di **CSIDL \_ NETWORK**.

Un CSIDL viene usato in combinazione con una delle diverse funzioni shell per recuperare il PIDL di una cartella speciale o un percorso file system della cartella. Se la cartella non esiste in un sistema, l'applicazione può forzarne la creazione combinando il relativo CSIDL con **CSIDL \_ FLAG \_ CREATE**. Il linguaggio CSIDL può essere passato alle funzioni seguenti:

-   [**SHGetFolderLocation,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)che recupera il file PIDL di una cartella speciale.
-   [**SHGetFolderPath,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)che recupera il percorso di una file system cartella speciale.

Si noti che queste due funzioni sono state introdotte con la versione 5.0 della shell e hanno sostituito le funzioni [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) e [**SHGetSpecialFolderPath.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha)

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a>Semplice esempio di come usare CSIDLs e SHBrowseForFolder

La funzione di esempio seguente, PidlBrowse, illustra come usare i CSIDL per recuperare il file PIDL di una cartella e [**usare SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) per fare in modo che l'utente seleziona una cartella. Restituisce il file PIDL e il nome visualizzato della cartella selezionata.


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



L'applicazione chiamante passa un handle di finestra, necessario [**per SHBrowseForFolder.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) Il *parametro nCSIDL* è un CSIDL facoltativo usato per specificare una cartella radice. Verranno visualizzate solo le cartelle sotto la cartella radice nella gerarchia. La figura illustrata in precedenza è stata generata chiamando questa funzione con *nCSIDL impostato* su **CSIDL \_ PROGRAM \_ FILES**. L'applicazione chiamante passa anche un buffer di stringhe, *pszDisplayName,* per contenere il nome visualizzato della cartella selezionata quando Viene restituito PidlBrowse. È responsabilità dell'applicazione chiamante liberare l'elenco IDList restituito da **SHBrowseForFolder** usando [**CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

 

 
