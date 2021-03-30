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
# <a name="getting-a-folders-id"></a><span data-ttu-id="0cf3b-103">Recupero dell'ID di una cartella</span><span class="sxs-lookup"><span data-stu-id="0cf3b-103">Getting a Folder's ID</span></span>

<span data-ttu-id="0cf3b-104">Prima di poter usare un oggetto spazio dei nomi, è necessario un modo per identificarlo.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-104">Before you can make use of a namespace object, you need a way to identify it.</span></span> <span data-ttu-id="0cf3b-105">Ciò significa che è possibile ottenere il relativo puntatore a un elenco di identificatori di elemento (PIDL) o, nel caso di file system oggetti, il suo percorso.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-105">This means obtaining either its pointer to an item identifier list (PIDL) or, in the case of file system objects, its path.</span></span> <span data-ttu-id="0cf3b-106">In questa sezione vengono descritti due dei modi più semplici per ottenere gli ID oggetto.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-106">This section discusses two of the simpler ways to obtain object IDs.</span></span>

<span data-ttu-id="0cf3b-107">Per un approccio più efficace che funzionerà con qualsiasi cartella, usare l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="0cf3b-107">For a more powerful approach that will work with any folder, use the [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="0cf3b-108">Per altri dettagli, vedere [ottenere informazioni sul contenuto di una cartella](folder-info.md) .</span><span class="sxs-lookup"><span data-stu-id="0cf3b-108">See [Getting Information About the Contents of a Folder](folder-info.md) for more details.</span></span>

-   [<span data-ttu-id="0cf3b-109">Finestra di dialogo OpenFiles</span><span class="sxs-lookup"><span data-stu-id="0cf3b-109">The OpenFiles Dialog Box</span></span>](#the-openfiles-dialog-box)
-   [<span data-ttu-id="0cf3b-110">Finestra di dialogo SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="0cf3b-110">The SHBrowseForFolder Dialog Box</span></span>](#the-shbrowseforfolder-dialog-box)
-   [<span data-ttu-id="0cf3b-111">Cartelle speciali e CSIDL</span><span class="sxs-lookup"><span data-stu-id="0cf3b-111">Special Folders and CSIDLs</span></span>](#special-folders-and-csidls)
-   [<span data-ttu-id="0cf3b-112">Un semplice esempio di come usare CSIDL e SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="0cf3b-112">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a><span data-ttu-id="0cf3b-113">Finestra di dialogo OpenFiles</span><span class="sxs-lookup"><span data-stu-id="0cf3b-113">The OpenFiles Dialog Box</span></span>

<span data-ttu-id="0cf3b-114">Per consentire all'utente di spostarsi nello spazio dei nomi e selezionare una cartella, l'applicazione può usare l'interfaccia [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) .</span><span class="sxs-lookup"><span data-stu-id="0cf3b-114">To enable the user to navigate the namespace and select a folder, your application can use the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface.</span></span> <span data-ttu-id="0cf3b-115">Chiamando questa interfaccia con il flag **Fos \_ PICKFOLDERS** viene avviata la finestra di dialogo [Apri file](../dlgbox/open-and-save-as-dialog-boxes.md) comuni in modalità "Seleziona cartelle".</span><span class="sxs-lookup"><span data-stu-id="0cf3b-115">Calling this interface with the **FOS\_PICKFOLDERS** flag launches the [Open Files](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box in "pick folders" mode.</span></span>

<span data-ttu-id="0cf3b-116">Per Windows Vista e versioni successive, si tratta della modalità consigliata per scegliere le cartelle.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-116">For Windows Vista and later, this is the recommended way to pick folders.</span></span>

## <a name="the-shbrowseforfolder-dialog-box"></a><span data-ttu-id="0cf3b-117">Finestra di dialogo SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="0cf3b-117">The SHBrowseForFolder Dialog Box</span></span>

<span data-ttu-id="0cf3b-118">Per consentire all'utente di spostarsi nello spazio dei nomi e selezionare una cartella, l'applicazione può semplicemente richiamare [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="0cf3b-118">To enable the user to navigate the namespace and select a folder, your application can simply invoke [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="0cf3b-119">Se si chiama questa funzione, viene avviata una finestra di dialogo con un'interfaccia utente che funziona in modo analogo alle finestre di dialogo comuni [aperte o SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) .</span><span class="sxs-lookup"><span data-stu-id="0cf3b-119">Calling this function launches a dialog box with a UI that works somewhat like the [Open or SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog boxes.</span></span>

<span data-ttu-id="0cf3b-120">Quando l'utente seleziona una cartella, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) restituisce il PIDL completo della cartella e il relativo nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-120">When the user selects a folder, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) returns the folder's fully qualified PIDL and its display name.</span></span> <span data-ttu-id="0cf3b-121">Se la cartella si trova nel file system, l'applicazione può convertire il PIDL in un percorso chiamando [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span><span class="sxs-lookup"><span data-stu-id="0cf3b-121">If the folder is in the file system, the application can convert the PIDL to a path by calling [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span></span> <span data-ttu-id="0cf3b-122">L'applicazione può anche limitare l'intervallo di cartelle da cui l'utente può selezionare specificando una cartella radice.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-122">The application can also restrict the range of folders that the user can select from by specifying a root folder.</span></span> <span data-ttu-id="0cf3b-123">Verranno visualizzate solo le cartelle che si trovano sotto la radice nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-123">Only folders that are below that root in the namespace will appear.</span></span> <span data-ttu-id="0cf3b-124">Nella figura seguente viene illustrata la finestra di dialogo **SHBrowseForFolder** con la cartella radice impostata su programmi.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-124">The following illustration shows the **SHBrowseForFolder** dialog box, with the root folder set to Program Files.</span></span>

![screenshot della finestra di dialogo Sfoglia per cartelle](images/shell1.png)

<span data-ttu-id="0cf3b-126">Un esempio semplice di utilizzo di [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) è disponibile in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-126">A simple example of how to use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) is provided later.</span></span>

## <a name="special-folders-and-csidls"></a><span data-ttu-id="0cf3b-127">Cartelle speciali e CSIDL</span><span class="sxs-lookup"><span data-stu-id="0cf3b-127">Special Folders and CSIDLs</span></span>

<span data-ttu-id="0cf3b-128">Una serie di cartelle di uso comune viene designata come *speciale* dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-128">A number of commonly used folders are designated as *special* by the system.</span></span> <span data-ttu-id="0cf3b-129">Queste cartelle hanno uno scopo ben definito e la maggior parte di esse sono presenti in tutti i sistemi.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-129">These folders have a well-defined purpose, and most of them are present on all systems.</span></span> <span data-ttu-id="0cf3b-130">Anche se non sono presenti inizialmente, i nomi e le posizioni sono ancora definiti, quindi possono essere aggiunti in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-130">Even if they are not present initially, their names and locations are still defined, so they can be added later.</span></span> <span data-ttu-id="0cf3b-131">La raccolta di cartelle speciali include tutte le cartelle virtuali standard del sistema, ad esempio stampanti, documenti e vicinanza alla rete.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-131">The collection of special folders includes all of the system's standard virtual folders, such as Printers, My Documents, and Network Neighborhood.</span></span> <span data-ttu-id="0cf3b-132">Include inoltre una serie di cartelle di file system standard, ad esempio file di programma e di sistema.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-132">It also includes a number of standard file system folders, such as Program Files and System.</span></span>

<span data-ttu-id="0cf3b-133">Anche se le cartelle sono un componente standard di tutti i sistemi, i relativi nomi e posizioni nello spazio dei nomi possono variare.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-133">Even though the folders are a standard component of all systems, their names and locations in the namespace can vary.</span></span> <span data-ttu-id="0cf3b-134">Ad esempio, la directory di sistema è C: \\ WinNT \\ System32 in alcuni sistemi e c: \\ Windows \\ system32 su altri.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-134">For example, the System directory is C:\\Winnt\\System32 on some systems and C:\\Windows\\System32 on others.</span></span> <span data-ttu-id="0cf3b-135">In passato, le variabili di ambiente fornivano un modo per determinare il nome e la posizione di una cartella speciale in un sistema particolare.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-135">In the past, environment variables provided a way to determine the name and location of a special folder on any particular system.</span></span> <span data-ttu-id="0cf3b-136">La Shell offre ora un modo più solido e flessibile per identificare cartelle speciali, [**CSIDL**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="0cf3b-136">The Shell now provides a more robust and flexible way to identify special folders, [**CSIDLs**](csidl.md).</span></span> <span data-ttu-id="0cf3b-137">In genere è consigliabile usarli invece delle variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-137">You should generally use them instead of environment variables.</span></span>

<span data-ttu-id="0cf3b-138">CSIDL forniscono un modo uniforme per identificare e individuare cartelle speciali, indipendentemente dal nome o dalla posizione in un sistema specifico.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-138">CSIDLs provide a uniform way of identifying and locating special folders, regardless of their name or location on a particular system.</span></span> <span data-ttu-id="0cf3b-139">A differenza delle variabili di ambiente, è possibile usare CSIDL con le cartelle virtuali e file system cartelle.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-139">Unlike environment variables, CSIDLs can be used with virtual folders as well as file system folders.</span></span> <span data-ttu-id="0cf3b-140">A ciascuna cartella speciale è assegnato un CSIDL univoco.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-140">Each special folder has a unique CSIDL assigned to it.</span></span> <span data-ttu-id="0cf3b-141">Ad esempio, la cartella programmi file system dispone di un CSIDL di **\_ \_ file di programma CSIDL** e la cartella virtuale del quartiere rete ha un CSIDL **della \_ rete CSIDL**.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-141">For example, the Program Files file system folder has a CSIDL of **CSIDL\_PROGRAM\_FILES**, and the Network Neighborhood virtual folder has a CSIDL of **CSIDL\_NETWORK**.</span></span>

<span data-ttu-id="0cf3b-142">Un CSIDL viene usato insieme a una delle diverse funzioni della Shell per recuperare il PIDL di una cartella speciale o un percorso speciale della cartella file system.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-142">A CSIDL is used in conjunction with one of several Shell functions to retrieve a special folder's PIDL, or a special file system folder's path.</span></span> <span data-ttu-id="0cf3b-143">Se la cartella non esiste in un sistema, l'applicazione può forzarla a crearla combinando il relativo CSIDL con **il \_ flag CSIDL \_ create**.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-143">If the folder does not exist on a system, your application can force it to be created by combining its CSIDL with **CSIDL\_FLAG\_CREATE**.</span></span> <span data-ttu-id="0cf3b-144">CSIDL può essere passato alle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0cf3b-144">The CSIDL can be passed to the following functions:</span></span>

-   <span data-ttu-id="0cf3b-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), che recupera il PIDL di una cartella speciale.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), which retrieves the PIDL of a special folder.</span></span>
-   <span data-ttu-id="0cf3b-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), che recupera il percorso di una file System cartella speciale.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), which retrieves the path of a file system special folder.</span></span>

<span data-ttu-id="0cf3b-147">Si noti che queste due funzioni sono state introdotte con la versione 5,0 della shell e sostituiscono le funzioni [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) e [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) .</span><span class="sxs-lookup"><span data-stu-id="0cf3b-147">Note that these two functions were introduced with version 5.0 of the Shell and supersede the [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) and [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) functions.</span></span>

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a><span data-ttu-id="0cf3b-148">Un semplice esempio di come usare CSIDL e SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="0cf3b-148">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>

<span data-ttu-id="0cf3b-149">La funzione di esempio seguente, PidlBrowse, illustra come usare CSIDL per recuperare PIDL di una cartella e usare [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) per fare in modo che l'utente selezioni una cartella.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-149">The following sample function, PidlBrowse, illustrates how to use CSIDLs to retrieve a folder's PIDL, and use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) to have the user select a folder.</span></span> <span data-ttu-id="0cf3b-150">Restituisce il PIDL e il nome visualizzato della cartella selezionata.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-150">It returns the PIDL and display name of the selected folder.</span></span>


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



<span data-ttu-id="0cf3b-151">L'applicazione chiamante passa un handle di finestra, che è necessario per [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="0cf3b-151">The calling application passes in a window handle, which is needed by [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="0cf3b-152">Il parametro *nCSIDL* è un CSIDL facoltativo utilizzato per specificare una cartella radice.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-152">The *nCSIDL* parameter is an optional CSIDL that is used to specify a root folder.</span></span> <span data-ttu-id="0cf3b-153">Verranno visualizzate solo le cartelle sotto la cartella radice nella gerarchia.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-153">Only folders below the root folder in the hierarchy will be displayed.</span></span> <span data-ttu-id="0cf3b-154">L'illustrazione mostrata in precedenza è stata generata chiamando questa funzione con *nCSIDL* impostato su **CSIDL \_ Program \_ files**.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-154">The illustration shown earlier was generated by calling this function with *nCSIDL* set to **CSIDL\_PROGRAM\_FILES**.</span></span> <span data-ttu-id="0cf3b-155">L'applicazione chiamante passa anche un buffer di stringa, *pszDisplayName*, per mantenere il nome visualizzato della cartella selezionata quando PidlBrowse restituisce.</span><span class="sxs-lookup"><span data-stu-id="0cf3b-155">The calling application also passes in a string buffer, *pszDisplayName*, to hold the display name of the selected folder when PidlBrowse returns.</span></span> <span data-ttu-id="0cf3b-156">È responsabilità dell'applicazione chiamante liberare il IDList restituito da **SHBrowseForFolder** usando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="0cf3b-156">It is the responsibility of the calling application to free the IDList returned by **SHBrowseForFolder** using [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

 

 
