---
description: Una volta che l'applicazione ha individuato un oggetto file, il passaggio successivo è spesso quello di intervenire in qualche modo.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Avvio di applicazioni (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880770"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="38170-103">Avvio di applicazioni (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span><span class="sxs-lookup"><span data-stu-id="38170-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="38170-104">Una volta che l'applicazione ha individuato un oggetto file, il passaggio successivo è spesso quello di intervenire in qualche modo.</span><span class="sxs-lookup"><span data-stu-id="38170-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="38170-105">Ad esempio, l'applicazione potrebbe voler avviare un'altra applicazione che consente all'utente di modificare un file di dati.</span><span class="sxs-lookup"><span data-stu-id="38170-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="38170-106">Se il file di interesse è un eseguibile, è possibile che l'applicazione voglia semplicemente avviarla.</span><span class="sxs-lookup"><span data-stu-id="38170-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="38170-107">Questo documento illustra come usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per eseguire queste attività.</span><span class="sxs-lookup"><span data-stu-id="38170-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="38170-108">Uso di ShellExecute e ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="38170-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="38170-109">Verbi oggetto</span><span class="sxs-lookup"><span data-stu-id="38170-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="38170-110">Uso di ShellExecuteEx per fornire servizi di attivazione da un sito</span><span class="sxs-lookup"><span data-stu-id="38170-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="38170-111">Utilizzo di ShellExecute per avviare la finestra di dialogo di ricerca</span><span class="sxs-lookup"><span data-stu-id="38170-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="38170-112">Esempio semplice di utilizzo di ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="38170-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="38170-113">Uso di ShellExecute e ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="38170-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="38170-114">Per usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), l'applicazione deve specificare l'oggetto file o cartella di cui eseguire l'azione e un *verbo* che specifica l'operazione.</span><span class="sxs-lookup"><span data-stu-id="38170-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="38170-115">Per **ShellExecute**, assegnare questi valori ai parametri appropriati.</span><span class="sxs-lookup"><span data-stu-id="38170-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="38170-116">Per **ShellExecuteEx**, compilare i membri appropriati di una struttura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="38170-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="38170-117">Sono inoltre disponibili diversi altri membri o parametri che possono essere utilizzati per ottimizzare il comportamento delle due funzioni.</span><span class="sxs-lookup"><span data-stu-id="38170-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="38170-118">Gli oggetti file e cartella possono far parte del file system o degli oggetti virtuali e possono essere identificati da percorsi o puntatori a elenchi di identificatori di elemento (PIDL).</span><span class="sxs-lookup"><span data-stu-id="38170-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="38170-119">Verbi oggetto</span><span class="sxs-lookup"><span data-stu-id="38170-119">Object Verbs</span></span>

<span data-ttu-id="38170-120">I verbi disponibili per un oggetto sono essenzialmente gli elementi individuati nel menu di scelta rapida di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="38170-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="38170-121">Per individuare i verbi disponibili, cercare nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="38170-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="38170-122">**HKEY \_ Verbi \_ radice delle classi** \\ **CLSID** \\ *{Object \_ CLSID}* \\ **Shell** \\ </span><span class="sxs-lookup"><span data-stu-id="38170-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="38170-123">dove l' *oggetto \_ CLSID* è l'identificatore di classe (CLSID) dell'oggetto e *Verb* è il nome del verbo disponibile.</span><span class="sxs-lookup"><span data-stu-id="38170-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="38170-124">La  \\ sottochiave del **comando** verb contiene i dati che indicano cosa accade quando il verbo viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="38170-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="38170-125">Per scoprire quali verbi sono disponibili per [gli oggetti della shell predefiniti](handlers.md), cercare nel registro di sistema in</span><span class="sxs-lookup"><span data-stu-id="38170-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="38170-126">**HKEY \_ \_** \\ *\_* Verbo della \\ **Shell** \\  del nome dell'oggetto radice delle classi</span><span class="sxs-lookup"><span data-stu-id="38170-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="38170-127">dove *\_ nome oggetto* è il nome dell'oggetto shell predefinito.</span><span class="sxs-lookup"><span data-stu-id="38170-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="38170-128">Anche in questo caso, la \\ sottochiave del **comando** verb contiene i dati che indicano cosa accade quando il verbo viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="38170-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="38170-129">I verbi comunemente disponibili includono:</span><span class="sxs-lookup"><span data-stu-id="38170-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="38170-130">Verbo</span><span class="sxs-lookup"><span data-stu-id="38170-130">Verb</span></span>       | <span data-ttu-id="38170-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38170-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38170-132">modifica</span><span class="sxs-lookup"><span data-stu-id="38170-132">edit</span></span>       | <span data-ttu-id="38170-133">Avvia un editor e apre il documento per la modifica.</span><span class="sxs-lookup"><span data-stu-id="38170-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="38170-134">trovare</span><span class="sxs-lookup"><span data-stu-id="38170-134">find</span></span>       | <span data-ttu-id="38170-135">Avvia una ricerca a partire dalla directory specificata.</span><span class="sxs-lookup"><span data-stu-id="38170-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="38170-136">apre</span><span class="sxs-lookup"><span data-stu-id="38170-136">open</span></span>       | <span data-ttu-id="38170-137">Avvia un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38170-137">Launches an application.</span></span> <span data-ttu-id="38170-138">Se il file non è un file eseguibile, viene avviata l'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="38170-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="38170-139">print</span><span class="sxs-lookup"><span data-stu-id="38170-139">print</span></span>      | <span data-ttu-id="38170-140">Stampa il file di documento.</span><span class="sxs-lookup"><span data-stu-id="38170-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="38170-141">properties</span><span class="sxs-lookup"><span data-stu-id="38170-141">properties</span></span> | <span data-ttu-id="38170-142">Consente di visualizzare le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="38170-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="38170-143">RunAs</span><span class="sxs-lookup"><span data-stu-id="38170-143">runas</span></span>      | <span data-ttu-id="38170-144">Avvia un'applicazione come amministratore.</span><span class="sxs-lookup"><span data-stu-id="38170-144">Launches an application as Administrator.</span></span> <span data-ttu-id="38170-145">Il controllo dell'account utente (UAC) richiederà all'utente il consenso per</span><span class="sxs-lookup"><span data-stu-id="38170-145">User Account Control (UAC) will prompt the user for consent to</span></span> |
|            | <span data-ttu-id="38170-146">eseguire l'applicazione con privilegi elevati o immettere le credenziali di un account amministratore usato per eseguire il</span><span class="sxs-lookup"><span data-stu-id="38170-146">run the application elevated or enter the credentials of an administrator account used to run the</span></span>        |
|            | <span data-ttu-id="38170-147">nell'applicazione Aha!.</span><span class="sxs-lookup"><span data-stu-id="38170-147">application.</span></span>                                                                                             |

 

<span data-ttu-id="38170-148">Ogni verbo corrisponde al comando da usare per avviare l'applicazione da una finestra della console.</span><span class="sxs-lookup"><span data-stu-id="38170-148">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="38170-149">Il verbo **Open** è un esempio valido, in quanto è generalmente supportato.</span><span class="sxs-lookup"><span data-stu-id="38170-149">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="38170-150">Per i file con estensione exe, **Apri** avvia semplicemente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38170-150">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="38170-151">Tuttavia, viene usato più di frequente per avviare un'applicazione che opera su un file specifico.</span><span class="sxs-lookup"><span data-stu-id="38170-151">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="38170-152">Ad esempio, i file con estensione txt possono essere aperti da Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="38170-152">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="38170-153">Il verbo **Open** per un file con estensione txt corrisponderebbe quindi a un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="38170-153">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="38170-154">Quando si usa [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per aprire un file con estensione txt, Wordpad.exe viene avviato con il file specificato come argomento.</span><span class="sxs-lookup"><span data-stu-id="38170-154">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="38170-155">Alcuni comandi possono avere argomenti aggiuntivi, ad esempio flag, che possono essere aggiunti in base alle esigenze per avviare correttamente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38170-155">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="38170-156">Per ulteriori informazioni sui menu di scelta rapida e sui verbi, vedere [estensione dei menu di scelta rapida](context.md).</span><span class="sxs-lookup"><span data-stu-id="38170-156">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="38170-157">In generale, il tentativo di determinare l'elenco dei verbi disponibili per un determinato file è piuttosto complesso.</span><span class="sxs-lookup"><span data-stu-id="38170-157">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="38170-158">In molti casi, è possibile semplicemente impostare il parametro *lpVerb* su **null**, che richiama il comando predefinito per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="38170-158">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="38170-159">Questa procedura è in genere equivalente all'impostazione di *lpVerb* su "Open", ma alcuni tipi di file possono avere un comando predefinito diverso.</span><span class="sxs-lookup"><span data-stu-id="38170-159">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="38170-160">Per ulteriori informazioni, vedere [estensione dei menu di scelta rapida](context.md) e la documentazione di riferimento di [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="38170-160">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="38170-161">Uso di ShellExecuteEx per fornire servizi di attivazione da un sito</span><span class="sxs-lookup"><span data-stu-id="38170-161">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="38170-162">I servizi di una catena di siti possono controllare molti comportamenti di attivazione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="38170-162">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="38170-163">A partire da Windows 8, è possibile fornire un puntatore alla catena di siti per [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per abilitare questi comportamenti.</span><span class="sxs-lookup"><span data-stu-id="38170-163">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="38170-164">Per fornire il sito a **ShellExecuteEx**:</span><span class="sxs-lookup"><span data-stu-id="38170-164">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="38170-165">Specificare il flag \_ See \_ mask \_ hInst \_ is \_ site flag nel membro **fmask** di [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="38170-165">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="38170-166">Fornire [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) nel membro **hInstApp** di [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="38170-166">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="38170-167">Utilizzo di ShellExecute per avviare la finestra di dialogo di ricerca</span><span class="sxs-lookup"><span data-stu-id="38170-167">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="38170-168">Quando un utente fa clic con il pulsante destro del mouse su un'icona di cartella in Esplora risorse, una delle voci di menu è "Search".</span><span class="sxs-lookup"><span data-stu-id="38170-168">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="38170-169">Se selezionano l'elemento, la shell avvia l'utilità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="38170-169">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="38170-170">Questa utilità consente di visualizzare una finestra di dialogo che può essere utilizzata per cercare una stringa di testo specificata nei file.</span><span class="sxs-lookup"><span data-stu-id="38170-170">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="38170-171">Un'applicazione può avviare l'utilità di ricerca a livello di codice per una directory chiamando [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), con "Find" come parametro *lpVerb* e il percorso della directory come parametro *lpFile* .</span><span class="sxs-lookup"><span data-stu-id="38170-171">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="38170-172">Ad esempio, la riga di codice seguente avvia l'utilità di ricerca per la directory c: \\ programmi.</span><span class="sxs-lookup"><span data-stu-id="38170-172">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="38170-173">Esempio semplice di utilizzo di ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="38170-173">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="38170-174">Nell'applicazione console di esempio seguente viene illustrato l'uso di [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="38170-174">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="38170-175">La maggior parte del codice di controllo degli errori è stata omessa per maggiore chiarezza.</span><span class="sxs-lookup"><span data-stu-id="38170-175">Most error checking code has been omitted for clarity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



<span data-ttu-id="38170-176">L'applicazione recupera prima di tutto il PIDL della directory di Windows ed enumera il contenuto finché non trova il primo file con estensione bmp.</span><span class="sxs-lookup"><span data-stu-id="38170-176">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="38170-177">A differenza dell'esempio precedente, [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) viene usato per recuperare il nome di analisi del file anziché il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="38170-177">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="38170-178">Poiché si tratta di una cartella file system, il nome di analisi è un percorso completo, ovvero ciò che è necessario per [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="38170-178">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="38170-179">Una volta individuato il primo file con estensione bmp, i valori appropriati vengono assegnati ai membri di una struttura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="38170-179">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="38170-180">Il membro **lpFile** è impostato sul nome di analisi del file e il membro **lpVerb** su **null** per iniziare l'operazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="38170-180">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="38170-181">In questo caso, l'operazione predefinita è "Open".</span><span class="sxs-lookup"><span data-stu-id="38170-181">In this case, the default operation is "open".</span></span> <span data-ttu-id="38170-182">La struttura viene quindi passata a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), che avvia il gestore predefinito per i file bitmap, in genere MSPaint.exe, per aprire il file.</span><span class="sxs-lookup"><span data-stu-id="38170-182">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="38170-183">Dopo la restituzione della funzione, i PIDL vengono liberati e viene rilasciata l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) della cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="38170-183">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 
