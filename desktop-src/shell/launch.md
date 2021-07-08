---
description: Dopo che l'applicazione ha individuato un oggetto file, il passaggio successivo consiste spesso nell'agire in qualche modo su di esso.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Avvio di applicazioni (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508612"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="f0f22-103">Avvio di applicazioni (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span><span class="sxs-lookup"><span data-stu-id="f0f22-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="f0f22-104">Dopo che l'applicazione ha individuato un oggetto file, il passaggio successivo consiste spesso nell'agire in qualche modo su di esso.</span><span class="sxs-lookup"><span data-stu-id="f0f22-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="f0f22-105">Ad esempio, l'applicazione potrebbe voler avviare un'altra applicazione che consente all'utente di modificare un file di dati.</span><span class="sxs-lookup"><span data-stu-id="f0f22-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="f0f22-106">Se il file di interesse è un eseguibile, è possibile che l'applicazione voglia semplicemente avviarlo.</span><span class="sxs-lookup"><span data-stu-id="f0f22-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="f0f22-107">Questo documento illustra come usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per eseguire queste attività.</span><span class="sxs-lookup"><span data-stu-id="f0f22-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="f0f22-108">Uso di ShellExecute e ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="f0f22-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="f0f22-109">Verbi oggetto</span><span class="sxs-lookup"><span data-stu-id="f0f22-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="f0f22-110">Uso di ShellExecuteEx per fornire servizi di attivazione da un sito</span><span class="sxs-lookup"><span data-stu-id="f0f22-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="f0f22-111">Uso di ShellExecute per avviare la finestra di dialogo Di ricerca</span><span class="sxs-lookup"><span data-stu-id="f0f22-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="f0f22-112">Esempio semplice di come usare ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="f0f22-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="f0f22-113">Uso di ShellExecute e ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="f0f22-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="f0f22-114">Per usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx,**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)l'applicazione deve specificare l'oggetto file o cartella su cui intervenire e un *verbo* che specifica l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f0f22-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="f0f22-115">Per **ShellExecute assegnare** questi valori ai parametri appropriati.</span><span class="sxs-lookup"><span data-stu-id="f0f22-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="f0f22-116">Per **ShellExecuteEx** compilare i membri appropriati di una [**struttura SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)</span><span class="sxs-lookup"><span data-stu-id="f0f22-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="f0f22-117">Esistono anche diversi altri membri o parametri che possono essere usati per ottimizzare il comportamento delle due funzioni.</span><span class="sxs-lookup"><span data-stu-id="f0f22-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="f0f22-118">Gli oggetti file e cartelle possono far parte dell'file system o degli oggetti virtuali e possono essere identificati da percorsi o puntatori agli elenchi di identificatori di elemento (PID).</span><span class="sxs-lookup"><span data-stu-id="f0f22-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="f0f22-119">Verbi oggetto</span><span class="sxs-lookup"><span data-stu-id="f0f22-119">Object Verbs</span></span>

<span data-ttu-id="f0f22-120">I verbi disponibili per un oggetto sono essenzialmente gli elementi disponibili nel menu di scelta rapida di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="f0f22-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="f0f22-121">Per trovare i verbi disponibili, cercare nel Registro di sistema in</span><span class="sxs-lookup"><span data-stu-id="f0f22-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="f0f22-122">**HKEY \_ CLASS \_ ROOT** \\ **CLSID** \\ *{object \_ clsid}* \\ **Verbo shell** \\ </span><span class="sxs-lookup"><span data-stu-id="f0f22-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="f0f22-123">dove *object \_ clsid* è l'identificatore di classe (CLSID) dell'oggetto e *verbo* è il nome del verbo disponibile.</span><span class="sxs-lookup"><span data-stu-id="f0f22-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="f0f22-124">La *sottochiave* del comando del verbo contiene i dati \\  che indicano cosa accade quando viene richiamato tale verbo.</span><span class="sxs-lookup"><span data-stu-id="f0f22-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="f0f22-125">Per scoprire quali verbi sono disponibili per [gli oggetti shell predefiniti,](handlers.md)cercare nel Registro di sistema in</span><span class="sxs-lookup"><span data-stu-id="f0f22-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="f0f22-126">**HKEY \_ Verbo \_ shell classes root** \\ *\_ nome* \\  \\ *oggetto*</span><span class="sxs-lookup"><span data-stu-id="f0f22-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="f0f22-127">dove *nome \_ oggetto* è il nome dell'oggetto Shell predefinito.</span><span class="sxs-lookup"><span data-stu-id="f0f22-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="f0f22-128">Anche in questo caso, *la sottochiave* del comando del verbo contiene i dati che indicano \\  cosa accade quando viene richiamato tale verbo.</span><span class="sxs-lookup"><span data-stu-id="f0f22-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="f0f22-129">I verbi disponibili comunemente includono:</span><span class="sxs-lookup"><span data-stu-id="f0f22-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="f0f22-130">Verbo</span><span class="sxs-lookup"><span data-stu-id="f0f22-130">Verb</span></span>       | <span data-ttu-id="f0f22-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0f22-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f22-132">modifica</span><span class="sxs-lookup"><span data-stu-id="f0f22-132">edit</span></span>       | <span data-ttu-id="f0f22-133">Avvia un editor e apre il documento per la modifica.</span><span class="sxs-lookup"><span data-stu-id="f0f22-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="f0f22-134">trovare</span><span class="sxs-lookup"><span data-stu-id="f0f22-134">find</span></span>       | <span data-ttu-id="f0f22-135">Avvia una ricerca a partire dalla directory specificata.</span><span class="sxs-lookup"><span data-stu-id="f0f22-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="f0f22-136">apre</span><span class="sxs-lookup"><span data-stu-id="f0f22-136">open</span></span>       | <span data-ttu-id="f0f22-137">Avvia un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f22-137">Launches an application.</span></span> <span data-ttu-id="f0f22-138">Se questo file non è un file eseguibile, viene avviata l'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="f0f22-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="f0f22-139">print</span><span class="sxs-lookup"><span data-stu-id="f0f22-139">print</span></span>      | <span data-ttu-id="f0f22-140">Stampa il file di documento.</span><span class="sxs-lookup"><span data-stu-id="f0f22-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="f0f22-141">properties</span><span class="sxs-lookup"><span data-stu-id="f0f22-141">properties</span></span> | <span data-ttu-id="f0f22-142">Visualizza le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f0f22-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="f0f22-143">RunAs</span><span class="sxs-lookup"><span data-stu-id="f0f22-143">runas</span></span>      | <span data-ttu-id="f0f22-144">Avvia un'applicazione come amministratore.</span><span class="sxs-lookup"><span data-stu-id="f0f22-144">Launches an application as Administrator.</span></span> <span data-ttu-id="f0f22-145">Controllo dell'account utente richiederà all'utente il consenso per eseguire l'applicazione con privilegi elevati o immissione delle credenziali di un account amministratore usato per eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f22-145">User Account Control (UAC) will prompt the user for consent to run the application elevated or enter the credentials of an administrator account used to run the application.</span></span> |



<span data-ttu-id="f0f22-146">Ogni verbo corrisponde al comando che verrebbe usato per avviare l'applicazione da una finestra della console.</span><span class="sxs-lookup"><span data-stu-id="f0f22-146">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="f0f22-147">Il  verbo aperto è un buon esempio, in quanto è comunemente supportato.</span><span class="sxs-lookup"><span data-stu-id="f0f22-147">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="f0f22-148">Per .exe file, **apri avvia** semplicemente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f22-148">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="f0f22-149">Tuttavia, viene usato più comunemente per avviare un'applicazione che opera su un file specifico.</span><span class="sxs-lookup"><span data-stu-id="f0f22-149">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="f0f22-150">Ad esempio, .txt file possono essere aperti da Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="f0f22-150">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="f0f22-151">Il **verbo** open per un .txt file corrisponderebbe quindi a qualcosa di simile al comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f0f22-151">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="f0f22-152">Quando si usa [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per aprire un file .txt, Wordpad.exe viene avviato con il file specificato come argomento.</span><span class="sxs-lookup"><span data-stu-id="f0f22-152">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="f0f22-153">Alcuni comandi possono avere argomenti aggiuntivi, ad esempio flag, che possono essere aggiunti in base alle esigenze per avviare correttamente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f22-153">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="f0f22-154">Per altre informazioni sui menu di scelta rapida e sui verbi, vedere [Estensione dei menu di scelta rapida](context.md).</span><span class="sxs-lookup"><span data-stu-id="f0f22-154">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="f0f22-155">In generale, il tentativo di determinare l'elenco di verbi disponibili per un determinato file è piuttosto complesso.</span><span class="sxs-lookup"><span data-stu-id="f0f22-155">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="f0f22-156">In molti casi, è sufficiente impostare il *parametro lpVerb* su **NULL,** che richiama il comando predefinito per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="f0f22-156">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="f0f22-157">Questa procedura equivale in genere all'impostazione *di lpVerb* su "open", ma alcuni tipi di file possono avere un comando predefinito diverso.</span><span class="sxs-lookup"><span data-stu-id="f0f22-157">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="f0f22-158">Per altre informazioni, vedere [Estensione dei menu di scelta rapida](context.md) e la documentazione di riferimento [**shellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)</span><span class="sxs-lookup"><span data-stu-id="f0f22-158">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="f0f22-159">Uso di ShellExecuteEx per fornire servizi di attivazione da un sito</span><span class="sxs-lookup"><span data-stu-id="f0f22-159">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="f0f22-160">I servizi di una catena di siti possono controllare molti comportamenti di attivazione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="f0f22-160">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="f0f22-161">A Windows 8, è possibile fornire un puntatore alla catena del sito a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per abilitare questi comportamenti.</span><span class="sxs-lookup"><span data-stu-id="f0f22-161">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="f0f22-162">Per fornire il sito a **ShellExecuteEx:**</span><span class="sxs-lookup"><span data-stu-id="f0f22-162">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="f0f22-163">Specificare il flag SEE \_ MASK \_ FLAG \_ HINST \_ IS SITE nel membro \_ **fMask** di [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="f0f22-163">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="f0f22-164">Specificare [**IUnknown nel**](/windows/win32/api/unknwn/nn-unknwn-iunknown) membro **hInstApp** di [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="f0f22-164">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="f0f22-165">Uso di ShellExecute per avviare la finestra di dialogo Di ricerca</span><span class="sxs-lookup"><span data-stu-id="f0f22-165">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="f0f22-166">Quando un utente fa clic con il pulsante destro del mouse sull'icona di una cartella Windows Explorer, una delle voci di menu è "Cerca".</span><span class="sxs-lookup"><span data-stu-id="f0f22-166">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="f0f22-167">Se selezionano tale elemento, Shell avvia l'utilità Di ricerca.</span><span class="sxs-lookup"><span data-stu-id="f0f22-167">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="f0f22-168">Questa utilità visualizza una finestra di dialogo che può essere usata per cercare nei file una stringa di testo specificata.</span><span class="sxs-lookup"><span data-stu-id="f0f22-168">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="f0f22-169">Un'applicazione può avviare a livello di codice l'utilità di ricerca per una directory chiamando [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), con "find" come parametro *lpVerb* e il percorso della directory come *parametro lpFile.*</span><span class="sxs-lookup"><span data-stu-id="f0f22-169">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="f0f22-170">Ad esempio, la riga di codice seguente avvia l'utilità di ricerca per la directory c: \\ MyPrograms.</span><span class="sxs-lookup"><span data-stu-id="f0f22-170">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="f0f22-171">Esempio semplice di come usare ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="f0f22-171">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="f0f22-172">L'applicazione console di esempio seguente illustra l'uso di [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="f0f22-172">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="f0f22-173">La maggior parte del codice di controllo degli errori è stata omessa per maggiore chiarezza.</span><span class="sxs-lookup"><span data-stu-id="f0f22-173">Most error checking code has been omitted for clarity.</span></span>


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



<span data-ttu-id="f0f22-174">L'applicazione recupera innanzitutto il file PIDL della directory Windows ed enumera il relativo contenuto finché non trova il primo file .bmp file.</span><span class="sxs-lookup"><span data-stu-id="f0f22-174">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="f0f22-175">A differenza dell'esempio precedente, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) viene usato per recuperare il nome di analisi del file anziché il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f0f22-175">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="f0f22-176">Poiché si tratta di file system, il nome di analisi è un percorso completo, che è quello necessario per [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)</span><span class="sxs-lookup"><span data-stu-id="f0f22-176">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="f0f22-177">Dopo aver individuato il .bmp file, i valori appropriati vengono assegnati ai membri di una [**struttura SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)</span><span class="sxs-lookup"><span data-stu-id="f0f22-177">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="f0f22-178">Il **membro lpFile** è impostato sul nome di analisi del file e il membro **lpVerb** su **NULL** per avviare l'operazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f0f22-178">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="f0f22-179">In questo caso, l'operazione predefinita è "open".</span><span class="sxs-lookup"><span data-stu-id="f0f22-179">In this case, the default operation is "open".</span></span> <span data-ttu-id="f0f22-180">La struttura viene quindi passata a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), che avvia il gestore predefinito per i file bitmap, in genere MSPaint.exe, per aprire il file.</span><span class="sxs-lookup"><span data-stu-id="f0f22-180">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="f0f22-181">Al termine della funzione, gli PID vengono liberati e Windows'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) della cartella.</span><span class="sxs-lookup"><span data-stu-id="f0f22-181">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 
