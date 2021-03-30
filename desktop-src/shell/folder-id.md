---
description: Prima di poter usare un oggetto spazio dei nomi, è necessario un modo per identificarlo.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Recupero dell'ID di una cartella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2e62454bf27f2c203f59aecb325cefe6537d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994733"
---
# <a name="getting-a-folders-id"></a>Recupero dell'ID di una cartella

Prima di poter usare un oggetto spazio dei nomi, è necessario un modo per identificarlo. Ciò significa che è possibile ottenere il relativo puntatore a un elenco di identificatori di elemento (PIDL) o, nel caso di file system oggetti, il suo percorso. In questa sezione vengono descritti due dei modi più semplici per ottenere gli ID oggetto.

Per un approccio più efficace che funzionerà con qualsiasi cartella, usare l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Per altri dettagli, vedere [ottenere informazioni sul contenuto di una cartella](folder-info.md) .

-   [Finestra di dialogo OpenFiles](#the-openfiles-dialog-box)
-   [Finestra di dialogo SHBrowseForFolder](#the-shbrowseforfolder-dialog-box)
-   [Cartelle speciali e CSIDL](#special-folders-and-csidls)
-   [Un semplice esempio di come usare CSIDL e SHBrowseForFolder](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a>Finestra di dialogo OpenFiles

Per consentire all'utente di spostarsi nello spazio dei nomi e selezionare una cartella, l'applicazione può usare l'interfaccia [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) . Chiamando questa interfaccia con il flag **Fos \_ PICKFOLDERS** viene avviata la finestra di dialogo [Apri file](../dlgbox/open-and-save-as-dialog-boxes.md) comuni in modalità "Seleziona cartelle".

Per Windows Vista e versioni successive, si tratta della modalità consigliata per scegliere le cartelle.

## <a name="the-shbrowseforfolder-dialog-box"></a>Finestra di dialogo SHBrowseForFolder

Per consentire all'utente di spostarsi nello spazio dei nomi e selezionare una cartella, l'applicazione può semplicemente richiamare [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). Se si chiama questa funzione, viene avviata una finestra di dialogo con un'interfaccia utente che funziona in modo analogo alle finestre di dialogo comuni [aperte o SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) .

Quando l'utente seleziona una cartella, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) restituisce il PIDL completo della cartella e il relativo nome visualizzato. Se la cartella si trova nel file system, l'applicazione può convertire il PIDL in un percorso chiamando [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista). L'applicazione può anche limitare l'intervallo di cartelle da cui l'utente può selezionare specificando una cartella radice. Verranno visualizzate solo le cartelle che si trovano sotto la radice nello spazio dei nomi. Nella figura seguente viene illustrata la finestra di dialogo **SHBrowseForFolder** con la cartella radice impostata su programmi.

![screenshot della finestra di dialogo Sfoglia per cartelle](images/shell1.png)

Un esempio semplice di utilizzo di [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) è disponibile in un secondo momento.

## <a name="special-folders-and-csidls"></a>Cartelle speciali e CSIDL

Una serie di cartelle di uso comune viene designata come *speciale* dal sistema. Queste cartelle hanno uno scopo ben definito e la maggior parte di esse sono presenti in tutti i sistemi. Anche se non sono presenti inizialmente, i nomi e le posizioni sono ancora definiti, quindi possono essere aggiunti in un secondo momento. La raccolta di cartelle speciali include tutte le cartelle virtuali standard del sistema, ad esempio stampanti, documenti e vicinanza alla rete. Include inoltre una serie di cartelle di file system standard, ad esempio file di programma e di sistema.

Anche se le cartelle sono un componente standard di tutti i sistemi, i relativi nomi e posizioni nello spazio dei nomi possono variare. Ad esempio, la directory di sistema è C: \\ WinNT \\ System32 in alcuni sistemi e c: \\ Windows \\ system32 su altri. In passato, le variabili di ambiente fornivano un modo per determinare il nome e la posizione di una cartella speciale in un sistema particolare. La Shell offre ora un modo più solido e flessibile per identificare cartelle speciali, [**CSIDL**](csidl.md). In genere è consigliabile usarli invece delle variabili di ambiente.

CSIDL forniscono un modo uniforme per identificare e individuare cartelle speciali, indipendentemente dal nome o dalla posizione in un sistema specifico. A differenza delle variabili di ambiente, è possibile usare CSIDL con le cartelle virtuali e file system cartelle. A ciascuna cartella speciale è assegnato un CSIDL univoco. Ad esempio, la cartella programmi file system dispone di un CSIDL di **\_ \_ file di programma CSIDL** e la cartella virtuale del quartiere rete ha un CSIDL **della \_ rete CSIDL**.

Un CSIDL viene usato insieme a una delle diverse funzioni della Shell per recuperare il PIDL di una cartella speciale o un percorso speciale della cartella file system. Se la cartella non esiste in un sistema, l'applicazione può forzarla a crearla combinando il relativo CSIDL con **il \_ flag CSIDL \_ create**. CSIDL può essere passato alle funzioni seguenti:

-   [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), che recupera il PIDL di una cartella speciale.
-   [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), che recupera il percorso di una file System cartella speciale.

Si noti che queste due funzioni sono state introdotte con la versione 5,0 della shell e sostituiscono le funzioni [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) e [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) .

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a>Un semplice esempio di come usare CSIDL e SHBrowseForFolder

La funzione di esempio seguente, PidlBrowse, illustra come usare CSIDL per recuperare PIDL di una cartella e usare [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) per fare in modo che l'utente selezioni una cartella. Restituisce il PIDL e il nome visualizzato della cartella selezionata.


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



L'applicazione chiamante passa un handle di finestra, che è necessario per [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). Il parametro *nCSIDL* è un CSIDL facoltativo utilizzato per specificare una cartella radice. Verranno visualizzate solo le cartelle sotto la cartella radice nella gerarchia. L'illustrazione mostrata in precedenza è stata generata chiamando questa funzione con *nCSIDL* impostato su **CSIDL \_ Program \_ files**. L'applicazione chiamante passa anche un buffer di stringa, *pszDisplayName*, per mantenere il nome visualizzato della cartella selezionata quando PidlBrowse restituisce. È responsabilità dell'applicazione chiamante liberare il IDList restituito da **SHBrowseForFolder** usando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

 

 
