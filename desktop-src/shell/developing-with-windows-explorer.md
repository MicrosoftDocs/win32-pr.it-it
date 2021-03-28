---
description: Esplora risorse è una potente applicazione di esplorazione e gestione delle risorse.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Sviluppo con Esplora risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7b68d48f2d1becea23311847a5ce41b3776321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484388"
---
# <a name="developing-with-windows-explorer"></a><span data-ttu-id="f4bd5-103">Sviluppo con Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="f4bd5-103">Developing with Windows Explorer</span></span>

<span data-ttu-id="f4bd5-104">Esplora risorse è una potente applicazione di esplorazione e gestione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-104">Windows Explorer is a powerful resource-browsing and management application.</span></span> <span data-ttu-id="f4bd5-105">È possibile accedere a Esplora risorse come un intero integrato tramite Explorer.exe o l'interfaccia [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="f4bd5-105">Windows Explorer can be accessed as an integrated whole through Explorer.exe or the [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="f4bd5-106">Esplora risorse (Explorer.exe) può essere generato come processo separato utilizzando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) o una funzione simile.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-106">Windows Explorer (Explorer.exe) can be spawned as a separate process using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) or a similar function.</span></span>

> [!Note]  
> <span data-ttu-id="f4bd5-107">Le opzioni della riga di comando per Explorer.exe sono documentate nel sito di supporto di Microsoft Windows nell'articolo [Opzioni di Esplora risorse Command-Line](https://support.microsoft.com/kb/152457).</span><span class="sxs-lookup"><span data-stu-id="f4bd5-107">Command-line options for Explorer.exe are documented on the Microsoft Windows Support site in the article [Windows Explorer Command-Line Options](https://support.microsoft.com/kb/152457).</span></span>

 

<span data-ttu-id="f4bd5-108">Le finestre aperte di Esplora risorse possono essere individuate e programmate tramite [**ishellwindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows) e le nuove istanze di Esplora risorse possono essere create tramite [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).</span><span class="sxs-lookup"><span data-stu-id="f4bd5-108">Open explorer windows can be discovered and programmed by using [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID\_ShellWindows), and new instances of Windows Explorer can be created by using [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID\_ShellBrowserWindow).</span></span>

<span data-ttu-id="f4bd5-109">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare il modello di automazione di Esplora risorse per creare e individuare le finestre di esplorazione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-109">The following code sample demonstrates how the Windows Explorer automation model can be used to create and discover explorer windows that are running.</span></span>


```
#define _WIN32_WINNT 0x0600
#define _WIN32_IE 0x0700
#define _UNICODE

#include <windows.h>
#include <shobjidl.h>
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>
#include <propvarutil.h>
 
#pragma comment(lib, "shlwapi.lib")
#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "shell32.lib")
#pragma comment(lib, "propsys.lib")
 
// Use the Shell Windows object to find all of the explorer and IExplorer 
// windows and close them.
 
void CloseExplorerWindows()
{
    IShellWindows* psw;
    
    if (SUCCEEDED(CoCreateInstance(CLSID_ShellWindows, 
                                   NULL,  
                                   CLSCTX_LOCAL_SERVER, 
                                   IID_PPV_ARGS(&psw))))
    {
        VARIANT v = { VT_I4 };
        if (SUCCEEDED(psw->get_Count(&v.lVal)))
        {
            // Walk backward to make sure that the windows that close
            // do not cause the array to be reordered.
            while (--v.lVal >= 0)
            {
                IDispatch *pdisp;
                
                if (S_OK == psw->Item(v, &pdisp))
                {
                    IWebBrowser2 *pwb;
                    if (SUCCEEDED(pdisp->QueryInterface(IID_PPV_ARGS(&pwb))))
                    {
                        pwb->Quit();
                        pwb->Release();
                    }
                    pdisp->Release();
                }
            }
        }
        psw->Release();
    }
}
 
// Convert an IShellItem or IDataObject into a VARIANT that holds an IDList
// suitable for use with IWebBrowser2::Navigate2.
 
HRESULT InitVariantFromObject(IUnknown *punk, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetIDListFromObject(punk, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}
 
HRESULT ParseItemAsVariant(PCWSTR pszItem, IBindCtx *pbc, VARIANT *pvar)
{
    VariantInit(pvar);
 
    IShellItem *psi;
    HRESULT hr = SHCreateItemFromParsingName(pszItem, NULL, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

HRESULT GetKnownFolderAsVariant(REFKNOWNFOLDERID kfid, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetKnownFolderIDList(kfid, 0, NULL, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}

HRESULT GetShellItemFromCommandLine(REFIID riid, void **ppv)
{
    *ppv = NULL;
    HRESULT hr = E_FAIL;

    int cArgs;
    PWSTR *ppszCmd = CommandLineToArgvW(GetCommandLineW(), &cArgs);
    if (ppszCmd && cArgs > 1)
    {
        WCHAR szSpec[MAX_PATH];
        StringCchCopyW(szSpec, ARRAYSIZE(szSpec), ppszCmd[1]);
        PathUnquoteSpacesW(szSpec);

        hr = szSpec[0] ? S_OK : E_FAIL;   // Protect against empty data
        if (SUCCEEDED(hr))
        {
            hr = SHCreateItemFromParsingName(szSpec, NULL, riid, ppv);
            if (FAILED(hr))
            {
                WCHAR szFolder[MAX_PATH];
                GetCurrentDirectoryW(ARRAYSIZE(szFolder), szFolder);

                hr = PathAppendW(szFolder, szSpec) ? S_OK : E_FAIL;
                if (SUCCEEDED(hr))
                {
                    hr = SHCreateItemFromParsingName(szFolder, NULL, riid, ppv);
                }
            }
        }
    }
    return hr;
}

HRESULT GetShellItemFromCommandLineAsVariant(VARIANT *pvar)
{
    VariantInit(pvar);

    IShellItem *psi;
    HRESULT hr = GetShellItemFromCommandLine(IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

void OpenWindow()
{
    IWebBrowser2 *pwb;
    HRESULT hr = CoCreateInstance(CLSID_ShellBrowserWindow, 
                                  NULL,
                                  CLSCTX_LOCAL_SERVER, 
                                  IID_PPV_ARGS(&pwb));
    if (SUCCEEDED(hr))
    {
        CoAllowSetForegroundWindow(pwb, 0);

        pwb->put_Left(100);
        pwb->put_Top(100);
        pwb->put_Height(600);
        pwb->put_Width(800);
 
        VARIANT varTarget = {0};
        hr = GetShellItemFromCommandLineAsVariant(&varTarget);
        if (FAILED(hr))
        {
            hr = GetKnownFolderAsVariant(FOLDERID_UsersFiles, &varTarget);
        }

        if (SUCCEEDED(hr))
        {
            VARIANT vEmpty = {0};
            hr = pwb->Navigate2(&varTarget, &vEmpty, &vEmpty, &vEmpty, &vEmpty);
            if (SUCCEEDED(hr))
            {
                pwb->put_Visible(VARIANT_TRUE);
            }
            VariantClear(&varTarget);
        }
        pwb->Release();
    }
}

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |  COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CloseExplorerWindows();

        OpenWindow();

        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="f4bd5-110">L'area client di Esplora risorse può essere ospitata tramite l'interfaccia [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="f4bd5-110">The Windows Explorer client area can be hosted by using the [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="f4bd5-111">Il client di Esplora risorse e i controlli struttura ad albero dello spazio dei nomi sono componenti standard di Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-111">The Windows Explorer client and the namespace tree controls are standard components of Windows Vista and later.</span></span> <span data-ttu-id="f4bd5-112">Gli sviluppatori possono riutilizzare le interfacce come componenti di compilazione.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-112">Developers can reuse the interfaces as building components.</span></span> <span data-ttu-id="f4bd5-113">Un uso comune di questi controlli consiste nel creare esplorazioni personalizzate appropriate per il dominio del problema.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-113">One common use of these controls is to create customized explorers appropriate to the problem domain.</span></span>

<span data-ttu-id="f4bd5-114">I controlli in Esplora risorse sono suddivisi nelle seguenti categorie funzionali:</span><span class="sxs-lookup"><span data-stu-id="f4bd5-114">The controls in Windows Explorer are classified into the following functional categories:</span></span>

-   [<span data-ttu-id="f4bd5-115">Controlli di navigazione</span><span class="sxs-lookup"><span data-stu-id="f4bd5-115">Navigation Controls</span></span>](#navigation-controls)
-   [<span data-ttu-id="f4bd5-116">Controlli Command</span><span class="sxs-lookup"><span data-stu-id="f4bd5-116">Command Controls</span></span>](#command-controls)
-   [<span data-ttu-id="f4bd5-117">Controlli di proprietà e di anteprima</span><span class="sxs-lookup"><span data-stu-id="f4bd5-117">Property and Preview Controls</span></span>](#property-and-preview-controls)
-   [<span data-ttu-id="f4bd5-118">Filtro e visualizzazione di controlli</span><span class="sxs-lookup"><span data-stu-id="f4bd5-118">Filtering and View Controls</span></span>](#filtering-and-view-controls)
-   [<span data-ttu-id="f4bd5-119">ListView (controllo)</span><span class="sxs-lookup"><span data-stu-id="f4bd5-119">Listview Control</span></span>](#listview-control)

## <a name="navigation-controls"></a><span data-ttu-id="f4bd5-120">Controlli di navigazione</span><span class="sxs-lookup"><span data-stu-id="f4bd5-120">Navigation Controls</span></span>

<span data-ttu-id="f4bd5-121">I controlli di spostamento aiutano gli utenti a determinare il contesto e a spostarsi nello spazio del dominio logico associato, denominato pagespace.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-121">Navigation controls assist users in determining context and navigating the associated logical domain space, called the pagespace.</span></span> <span data-ttu-id="f4bd5-122">Ad esempio, pagespace per Esplora risorse è lo spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-122">For example, the pagespace for Windows Explorer is the Shell namespace.</span></span> <span data-ttu-id="f4bd5-123">Pagespaces sono costituiti da zero o più pagine.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-123">Pagespaces are composed of zero or more pages.</span></span>

<span data-ttu-id="f4bd5-124">Nella tabella seguente sono elencati e descritti i controlli di navigazione disponibili in Esplora risorse in Windows Vista e nei sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-124">The following table lists and describes the navigation controls available in Windows Explorer in the Windows Vista and later operating systems.</span></span>



| <span data-ttu-id="f4bd5-125">Controllo di navigazione</span><span class="sxs-lookup"><span data-stu-id="f4bd5-125">Navigation control</span></span>               | <span data-ttu-id="f4bd5-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4bd5-126">Description</span></span>                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4bd5-127">Barra degli indirizzi (controllo di navigazione)</span><span class="sxs-lookup"><span data-stu-id="f4bd5-127">Address Bar (Breadcrumb control)</span></span> | <span data-ttu-id="f4bd5-128">Consente di visualizzare l'indirizzo della pagina corrente in pagespace.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-128">Displays the address of the current page in the pagespace.</span></span> <span data-ttu-id="f4bd5-129">È possibile fare clic sui pulsanti di navigazione per spostarsi tra i predecessori in pagespace.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-129">Breadcrumb buttons can be clicked to navigate to any ancestor in the pagespace.</span></span> <span data-ttu-id="f4bd5-130">Gli utenti possono anche digitare URL e percorsi da esplorare.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-130">Users can also type URLs and paths to navigate.</span></span> |
| <span data-ttu-id="f4bd5-131">Albero delle cartelle</span><span class="sxs-lookup"><span data-stu-id="f4bd5-131">Folder Tree</span></span>                      | <span data-ttu-id="f4bd5-132">Fornisce una nuova versione di un controllo struttura ad albero, ottimizzata per pagespaces di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-132">Provides a new version of a tree control, optimized for large pagespaces.</span></span>                                                                                                                  |
| <span data-ttu-id="f4bd5-133">Viaggi</span><span class="sxs-lookup"><span data-stu-id="f4bd5-133">Travel</span></span>                           | <span data-ttu-id="f4bd5-134">Abilita la navigazione relativa attraverso pulsanti di tipo Web, ad esempio **indietro** e **in** secondo piano.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-134">Enables relative navigation through web-style buttons such as **Back** and **Forward**.</span></span>                                                                                                    |
| <span data-ttu-id="f4bd5-135">Titolo</span><span class="sxs-lookup"><span data-stu-id="f4bd5-135">Title</span></span>                            | <span data-ttu-id="f4bd5-136">Visualizza il nome e il contesto della finestra di esplorazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-136">Displays the current explorer name and context.</span></span>                                                                                                                                            |
| <span data-ttu-id="f4bd5-137">Pagespace</span><span class="sxs-lookup"><span data-stu-id="f4bd5-137">Pagespace</span></span>                        | <span data-ttu-id="f4bd5-138">Visualizza il ramo corrente di pagespace.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-138">Displays the current branch of the pagespace.</span></span> <span data-ttu-id="f4bd5-139">Le pagine possono essere ordinate in base a criteri diversi.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-139">Pages can be ordered by different criteria.</span></span> <span data-ttu-id="f4bd5-140">Gli utenti possono fare clic su una pagina per passare a questa pagina.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-140">Users can click a page to navigate to it.</span></span>                                                        |



 

## <a name="command-controls"></a><span data-ttu-id="f4bd5-141">Controlli Command</span><span class="sxs-lookup"><span data-stu-id="f4bd5-141">Command Controls</span></span>

<span data-ttu-id="f4bd5-142">I controlli comando annunciano le funzionalità e le funzionalità di Esplora risorse agli utenti.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-142">Command controls advertise the features and functionality of the Windows Explorer to users.</span></span> <span data-ttu-id="f4bd5-143">Questi controlli eseguono azioni generali o azioni specifiche per uno o più elementi selezionati.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-143">These controls perform either general actions or actions specific to one selected item or items.</span></span>



| <span data-ttu-id="f4bd5-144">Controllo Command</span><span class="sxs-lookup"><span data-stu-id="f4bd5-144">Command control</span></span> | <span data-ttu-id="f4bd5-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4bd5-145">Description</span></span>                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4bd5-146">Barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="f4bd5-146">Toolbar</span></span>         | <span data-ttu-id="f4bd5-147">Visualizza i pulsanti per i comandi di uso comune, ovvero una nuova versione di una barra degli strumenti dei comandi.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-147">Displays buttons for commonly used commands (a new version of a command toolbar).</span></span> <span data-ttu-id="f4bd5-148">Le opzioni di personalizzazione includono i pulsanti a discesa, i pulsanti di divisione, il testo descrittivo facoltativo e un'area di overflow.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-148">Customization options include drop-down buttons, split buttons, optional descriptive text, and an overflow area.</span></span> |
| <span data-ttu-id="f4bd5-149">Banner</span><span class="sxs-lookup"><span data-stu-id="f4bd5-149">Hero</span></span>            | <span data-ttu-id="f4bd5-150">Viene visualizzato come singolo controllo personalizzato, facoltativo al centro della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-150">Appears as a single, optional, custom control in the center of the toolbar.</span></span> <span data-ttu-id="f4bd5-151">Rappresenta il comando primario per il contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-151">It represents the primary command for the current context.</span></span>                                                             |
| <span data-ttu-id="f4bd5-152">Barra dei menu</span><span class="sxs-lookup"><span data-stu-id="f4bd5-152">Menu Bar</span></span>        | <span data-ttu-id="f4bd5-153">Visualizza i comandi attraverso i menu.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-153">Presents commands through menus.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="f4bd5-154">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="f4bd5-154">Context Menu</span></span>    | <span data-ttu-id="f4bd5-155">Elenca un subset di comandi disponibili in modo contestuale pertinente che vengono visualizzati in seguito al clic con il pulsante destro del mouse su un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-155">Lists a contextually relevant subset of available commands that are displayed as a result of right-clicking an item.</span></span>                                                                               |



 

## <a name="property-and-preview-controls"></a><span data-ttu-id="f4bd5-156">Controlli di proprietà e di anteprima</span><span class="sxs-lookup"><span data-stu-id="f4bd5-156">Property and Preview Controls</span></span>

<span data-ttu-id="f4bd5-157">I controlli proprietà e anteprima vengono usati per visualizzare in anteprima gli elementi e per visualizzare e modificare le proprietà degli elementi.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-157">Property and preview controls are used to preview items, and to view and edit item properties.</span></span>



| <span data-ttu-id="f4bd5-158">Controllo</span><span class="sxs-lookup"><span data-stu-id="f4bd5-158">Control</span></span>    | <span data-ttu-id="f4bd5-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4bd5-159">Description</span></span>                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4bd5-160">Anteprima</span><span class="sxs-lookup"><span data-stu-id="f4bd5-160">Preview</span></span>    | <span data-ttu-id="f4bd5-161">Visualizza un'anteprima dell'elemento selezionato, ad esempio un'anteprima o un'icona in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-161">Displays a preview of the selected item, such as a thumbnail or a Live Icon.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="f4bd5-162">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f4bd5-162">Properties</span></span> | <span data-ttu-id="f4bd5-163">Consente di visualizzare le proprietà dell'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-163">Displays properties of the selected item.</span></span> <span data-ttu-id="f4bd5-164">Per le selezioni multiple, viene visualizzato un riepilogo delle proprietà per il gruppo selezionato di elementi.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-164">For multiple selections, it displays a summary of properties for the selected group of items.</span></span> <span data-ttu-id="f4bd5-165">Per una selezione null, viene visualizzato un riepilogo delle proprietà della pagina corrente (contenuto del controllo ListView).</span><span class="sxs-lookup"><span data-stu-id="f4bd5-165">For a null selection, it displays a summary of properties for the current page (contents of the listview).</span></span> |



 

## <a name="filtering-and-view-controls"></a><span data-ttu-id="f4bd5-166">Filtro e visualizzazione di controlli</span><span class="sxs-lookup"><span data-stu-id="f4bd5-166">Filtering and View Controls</span></span>

<span data-ttu-id="f4bd5-167">I controlli Filtering e View vengono usati per modificare il set di elementi nel controllo ListView e per modificare la presentazione degli elementi nel controllo ListView.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-167">Filtering and view controls are used to manipulate the set of items in the listview and to change the presentation of items in the listview.</span></span>



| <span data-ttu-id="f4bd5-168">Controllo</span><span class="sxs-lookup"><span data-stu-id="f4bd5-168">Control</span></span>   | <span data-ttu-id="f4bd5-169">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4bd5-169">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4bd5-170">Filtro</span><span class="sxs-lookup"><span data-stu-id="f4bd5-170">Filter</span></span>    | <span data-ttu-id="f4bd5-171">Filtra o dispone gli elementi in un controllo ListView in base alle proprietà elencate come colonne.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-171">Filters or arranges items in a listview based on properties listed as columns.</span></span> <span data-ttu-id="f4bd5-172">Facendo clic su una colonna viene ordinata in base a tale proprietà.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-172">Clicking on a column sorts by that property.</span></span> |
| <span data-ttu-id="f4bd5-173">Wordwheel</span><span class="sxs-lookup"><span data-stu-id="f4bd5-173">Wordwheel</span></span> | <span data-ttu-id="f4bd5-174">Filtra dinamicamente e in modo incrementale gli elementi visualizzati in un controllo ListView in base a una stringa di testo di input.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-174">Dynamically and incrementally filters the displayed items in a listview based on an input text string.</span></span>                      |
| <span data-ttu-id="f4bd5-175">Visualizzazione</span><span class="sxs-lookup"><span data-stu-id="f4bd5-175">View</span></span>      | <span data-ttu-id="f4bd5-176">Consente all'utente di modificare la modalità di visualizzazione di un controllo ListView.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-176">Enables the user to change the view mode of a listview control.</span></span> <span data-ttu-id="f4bd5-177">Un dispositivo di scorrimento può essere utilizzato per determinare le dimensioni dell'icona.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-177">A slider can be used to determine icon size.</span></span>                |



 

## <a name="listview-control"></a><span data-ttu-id="f4bd5-178">ListView (controllo)</span><span class="sxs-lookup"><span data-stu-id="f4bd5-178">Listview Control</span></span>

<span data-ttu-id="f4bd5-179">Il controllo ListView viene usato per visualizzare un set di elementi in una delle quattro modalità di visualizzazione: dettagli, riquadri, icone o panorama.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-179">The listview control is used to view a set of items in one of four view modes: details, tiles, icons, or panorama.</span></span> <span data-ttu-id="f4bd5-180">Il controllo ListView consente inoltre all'utente di selezionare e attivare uno o più elementi.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-180">The listview control also enables the user to select and activate one or more items.</span></span>

> [!Caution]  
> <span data-ttu-id="f4bd5-181">Anche se alcuni di questi controlli hanno nomi e/o funzionalità simili ai controlli Windows Presentation Foundation standard (WPF) trovati nello spazio dei nomi System. Windows. Controls, sono classi distinte.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-181">Although some of these controls have names and/or functionality that is similar to standard Windows Presentation Foundation (WPF) controls found in the System.Windows.Controls namespace, they are distinct classes.</span></span>

 

<span data-ttu-id="f4bd5-182">Questi controlli separati interagiscono in gran parte tramite gli eventi generati dall'interazione dell'utente o dai controlli stessi.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-182">These separate controls work together largely through events generated either by user interaction or by the controls themselves.</span></span> <span data-ttu-id="f4bd5-183">Nella tabella seguente vengono illustrate le tre categorie di eventi principali.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-183">The following table shows the three primary event categories.</span></span>



| <span data-ttu-id="f4bd5-184">Categoria evento</span><span class="sxs-lookup"><span data-stu-id="f4bd5-184">Event category</span></span> | <span data-ttu-id="f4bd5-185">Esempio</span><span class="sxs-lookup"><span data-stu-id="f4bd5-185">Example</span></span>                                                       |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="f4bd5-186">Spostamento</span><span class="sxs-lookup"><span data-stu-id="f4bd5-186">Navigation</span></span>     | <span data-ttu-id="f4bd5-187">Passa da una pagina all'altra.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-187">Going from one page to another.</span></span>                               |
| <span data-ttu-id="f4bd5-188">Selezione</span><span class="sxs-lookup"><span data-stu-id="f4bd5-188">Selection</span></span>      | <span data-ttu-id="f4bd5-189">Modifica della selezione corrente nel controllo ListView.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-189">Changing the current selection in the listview.</span></span>               |
| <span data-ttu-id="f4bd5-190">Visualizza modifica</span><span class="sxs-lookup"><span data-stu-id="f4bd5-190">View Change</span></span>    | <span data-ttu-id="f4bd5-191">Modifica dell'ordine di presentazione o della modalità di visualizzazione in ListView.</span><span class="sxs-lookup"><span data-stu-id="f4bd5-191">Changing the presentation order or view mode in the listview.</span></span> |



 

 

 
