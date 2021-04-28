---
title: Tabelle dei tasti di scelta rapida
description: Tabelle dei tasti di scelta rapida
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2951ee99a31a977e0909de5639fa3110cea10e0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090819"
---
# <a name="accelerator-tables"></a><span data-ttu-id="52bbd-103">Tabelle dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="52bbd-103">Accelerator Tables</span></span>

<span data-ttu-id="52bbd-104">Le applicazioni spesso definiscono tasti di scelta rapida, ad esempio CTRL+O per il comando Apri file.</span><span class="sxs-lookup"><span data-stu-id="52bbd-104">Applications often define keyboard shortcuts, such as CTRL+O for the File Open command.</span></span> <span data-ttu-id="52bbd-105">È possibile implementare i tasti di scelta rapida gestendo singoli [**messaggi WM \_ KEYDOWN,**](/windows/desktop/inputdev/wm-keydown) ma le tabelle dei tasti di scelta rapida offrono una soluzione migliore che:</span><span class="sxs-lookup"><span data-stu-id="52bbd-105">You could implement keyboard shortcuts by handling individual [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, but accelerator tables provide a better solution that:</span></span>

-   <span data-ttu-id="52bbd-106">Richiede meno codice.</span><span class="sxs-lookup"><span data-stu-id="52bbd-106">Requires less coding.</span></span>
-   <span data-ttu-id="52bbd-107">Consolida tutti i collegamenti in un unico file di dati.</span><span class="sxs-lookup"><span data-stu-id="52bbd-107">Consolidates all of your shortcuts into one data file.</span></span>
-   <span data-ttu-id="52bbd-108">Supporta la localizzazione in altre lingue.</span><span class="sxs-lookup"><span data-stu-id="52bbd-108">Supports localization into other languages.</span></span>
-   <span data-ttu-id="52bbd-109">Consente ai tasti di scelta rapida e ai comandi di menu di usare la stessa logica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-109">Enables shortcuts and menu commands to use the same application logic.</span></span>

<span data-ttu-id="52bbd-110">Una *tabella dei tasti di* scelta rapida è una risorsa dati che esegue il mapping delle combinazioni di tasti, ad esempio CTRL+O, ai comandi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-110">An *accelerator table* is a data resource that maps keyboard combinations, such as CTRL+O, to application commands.</span></span> <span data-ttu-id="52bbd-111">Prima di vedere come usare una tabella dei tasti di scelta rapida, è necessaria una rapida introduzione alle risorse.</span><span class="sxs-lookup"><span data-stu-id="52bbd-111">Before we see how to use an accelerator table, we'll need a quick introduction to resources.</span></span> <span data-ttu-id="52bbd-112">Una *risorsa* è un BLOB di dati incorporato in un file binario dell'applicazione (EXE o DLL).</span><span class="sxs-lookup"><span data-stu-id="52bbd-112">A *resource* is a data blob that is built into an application binary (EXE or DLL).</span></span> <span data-ttu-id="52bbd-113">Le risorse archiviano i dati necessari per l'applicazione, ad esempio menu, cursori, icone, immagini, stringhe di testo o dati personalizzati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-113">Resources store data that are needed by the application, such as menus, cursors, icons, images, text strings, or any custom application data.</span></span> <span data-ttu-id="52bbd-114">L'applicazione carica i dati delle risorse dal file binario in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-114">The application loads the resource data from the binary at run time.</span></span> <span data-ttu-id="52bbd-115">Per includere le risorse in un file binario, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="52bbd-115">To include resources in a binary, do the following:</span></span>

1.  <span data-ttu-id="52bbd-116">Creare un file di definizione di risorsa (RC).</span><span class="sxs-lookup"><span data-stu-id="52bbd-116">Create a resource definition (.rc) file.</span></span> <span data-ttu-id="52bbd-117">Questo file definisce i tipi di risorse e i relativi identificatori.</span><span class="sxs-lookup"><span data-stu-id="52bbd-117">This file defines the types of resources and their identifiers.</span></span> <span data-ttu-id="52bbd-118">Il file di definizione delle risorse può includere riferimenti ad altri file.</span><span class="sxs-lookup"><span data-stu-id="52bbd-118">The resource definition file may include references to other files.</span></span> <span data-ttu-id="52bbd-119">Ad esempio, una risorsa icona viene dichiarata nel file RC, ma l'immagine dell'icona viene archiviata in un file separato.</span><span class="sxs-lookup"><span data-stu-id="52bbd-119">For example, an icon resource is declared in the .rc file, but the icon image is stored in a separate file.</span></span>
2.  <span data-ttu-id="52bbd-120">Usare il compilatore di risorse di Microsoft Windows (RC) per compilare il file di definizione della risorsa in un file di risorse compilato (con estensione res).</span><span class="sxs-lookup"><span data-stu-id="52bbd-120">Use the Microsoft Windows Resource Compiler (RC) to compile the resource definition file into a compiled resource (.res) file.</span></span> <span data-ttu-id="52bbd-121">Il compilatore RC viene fornito con Visual Studio e anche il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="52bbd-121">The RC compiler is provided with Visual Studio and also the Windows SDK.</span></span>
3.  <span data-ttu-id="52bbd-122">Collegare il file di risorse compilato al file binario.</span><span class="sxs-lookup"><span data-stu-id="52bbd-122">Link the compiled resource file to the binary file.</span></span>

<span data-ttu-id="52bbd-123">Questi passaggi sono approssimativamente equivalenti al processo di compilazione/collegamento per i file di codice.</span><span class="sxs-lookup"><span data-stu-id="52bbd-123">These steps are roughly equivalent to the compile/link process for code files.</span></span> <span data-ttu-id="52bbd-124">Visual Studio un set di editor di risorse che semplificano la creazione e la modifica delle risorse.</span><span class="sxs-lookup"><span data-stu-id="52bbd-124">Visual Studio provides a set of resource editors that make it easy to create and modify resources.</span></span> <span data-ttu-id="52bbd-125">Questi strumenti non sono disponibili nelle edizioni Express di Visual Studio. Ma un file RC è semplicemente un file di testo e la sintassi è documentata in MSDN, quindi è possibile creare un file RC usando qualsiasi editor di testo.</span><span class="sxs-lookup"><span data-stu-id="52bbd-125">(These tools are not available in the Express editions of Visual Studio.) But an .rc file is simply a text file, and the syntax is documented on MSDN, so it is possible to create an .rc file using any text editor.</span></span> <span data-ttu-id="52bbd-126">Per altre informazioni, vedere [Informazioni sui file di risorse](/windows/desktop/menurc/about-resource-files).</span><span class="sxs-lookup"><span data-stu-id="52bbd-126">For more information, see [About Resource Files](/windows/desktop/menurc/about-resource-files).</span></span>

## <a name="defining-an-accelerator-table"></a><span data-ttu-id="52bbd-127">Definizione di una tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="52bbd-127">Defining an Accelerator Table</span></span>

<span data-ttu-id="52bbd-128">Una tabella dei tasti di scelta rapida è una tabella di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="52bbd-128">An accelerator table is a table of keyboard shortcuts.</span></span> <span data-ttu-id="52bbd-129">Ogni collegamento è definito da:</span><span class="sxs-lookup"><span data-stu-id="52bbd-129">Each shortcut is defined by:</span></span>

-   <span data-ttu-id="52bbd-130">Identificatore numerico.</span><span class="sxs-lookup"><span data-stu-id="52bbd-130">A numeric identifier.</span></span> <span data-ttu-id="52bbd-131">Questo numero identifica il comando dell'applicazione che verrà richiamato dal collegamento.</span><span class="sxs-lookup"><span data-stu-id="52bbd-131">This number identifies the application command that will be invoked by the shortcut.</span></span>
-   <span data-ttu-id="52bbd-132">Carattere ASCII o codice tasto virtuale del collegamento.</span><span class="sxs-lookup"><span data-stu-id="52bbd-132">The ASCII character or virtual-key code of the shortcut.</span></span>
-   <span data-ttu-id="52bbd-133">Tasti di modifica facoltativi: ALT, MAIUSC o CTRL.</span><span class="sxs-lookup"><span data-stu-id="52bbd-133">Optional modifier keys: ALT, SHIFT, or CTRL.</span></span>

<span data-ttu-id="52bbd-134">La tabella dei tasti di scelta rapida ha un identificatore numerico che identifica la tabella nell'elenco delle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-134">The accelerator table itself has a numeric identifier, which identifies the table in the list of application resources.</span></span> <span data-ttu-id="52bbd-135">Si creerà ora una tabella dei tasti di scelta rapida per un semplice programma di disegno.</span><span class="sxs-lookup"><span data-stu-id="52bbd-135">Let's create an accelerator table for a simple drawing program.</span></span> <span data-ttu-id="52bbd-136">Questo programma avrà due modalità, la modalità di disegno e la modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-136">This program will have two modes, draw mode and selection mode.</span></span> <span data-ttu-id="52bbd-137">In modalità di disegno, l'utente può disegnare forme.</span><span class="sxs-lookup"><span data-stu-id="52bbd-137">In draw mode, the user can draw shapes.</span></span> <span data-ttu-id="52bbd-138">In modalità di selezione, l'utente può selezionare le forme.</span><span class="sxs-lookup"><span data-stu-id="52bbd-138">In selection mode, the user can select shapes.</span></span> <span data-ttu-id="52bbd-139">Per questo programma, è necessario definire i tasti di scelta rapida seguenti.</span><span class="sxs-lookup"><span data-stu-id="52bbd-139">For this program, we would like to define the following keyboard shortcuts.</span></span>



| <span data-ttu-id="52bbd-140">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="52bbd-140">Shortcut</span></span> | <span data-ttu-id="52bbd-141">Comando</span><span class="sxs-lookup"><span data-stu-id="52bbd-141">Command</span></span>                   |
|----------|---------------------------|
| <span data-ttu-id="52bbd-142">CTRL+M</span><span class="sxs-lookup"><span data-stu-id="52bbd-142">CTRL+M</span></span>   | <span data-ttu-id="52bbd-143">Passare da una modalità all'altra.</span><span class="sxs-lookup"><span data-stu-id="52bbd-143">Toggle between modes.</span></span>     |
| <span data-ttu-id="52bbd-144">F1</span><span class="sxs-lookup"><span data-stu-id="52bbd-144">F1</span></span>       | <span data-ttu-id="52bbd-145">Passare alla modalità di disegno.</span><span class="sxs-lookup"><span data-stu-id="52bbd-145">Switch to draw mode.</span></span>      |
| <span data-ttu-id="52bbd-146">F2</span><span class="sxs-lookup"><span data-stu-id="52bbd-146">F2</span></span>       | <span data-ttu-id="52bbd-147">Passare alla modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-147">Switch to selection mode.</span></span> |



 

<span data-ttu-id="52bbd-148">Definire prima di tutto gli identificatori numerici per la tabella e per i comandi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-148">First, define numeric identifiers for the table and for the application commands.</span></span> <span data-ttu-id="52bbd-149">Questi valori sono arbitrari.</span><span class="sxs-lookup"><span data-stu-id="52bbd-149">These values are arbitrary.</span></span> <span data-ttu-id="52bbd-150">È possibile assegnare costanti simboliche per gli identificatori definendoli in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-150">You can assign symbolic constants for the identifiers by defining them in a header file.</span></span> <span data-ttu-id="52bbd-151">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="52bbd-151">For example:</span></span>


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



<span data-ttu-id="52bbd-152">In questo esempio il valore identifica `IDR_ACCEL1` la tabella dei tasti di scelta rapida e le tre costanti seguenti definiscono i comandi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-152">In this example, the value `IDR_ACCEL1` identifies the accelerator table, and the next three constants define the application commands.</span></span> <span data-ttu-id="52bbd-153">Per convenzione, un file di intestazione che definisce le costanti di risorsa è spesso denominato resource.h.</span><span class="sxs-lookup"><span data-stu-id="52bbd-153">By convention, a header file that defines resource constants is often named resource.h.</span></span> <span data-ttu-id="52bbd-154">L'elenco successivo mostra il file di definizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="52bbd-154">The next listing shows the resource definition file.</span></span>


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



<span data-ttu-id="52bbd-155">I tasti di scelta rapida sono definiti tra parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="52bbd-155">The accelerator shortcuts are defined within the curly braces.</span></span> <span data-ttu-id="52bbd-156">Ogni collegamento contiene le voci seguenti.</span><span class="sxs-lookup"><span data-stu-id="52bbd-156">Each shortcut contains the following entries.</span></span>

-   <span data-ttu-id="52bbd-157">Codice del tasto virtuale o carattere ASCII che richiama il tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="52bbd-157">The virtual-key code or ASCII character that invokes the shortcut.</span></span>
-   <span data-ttu-id="52bbd-158">Comando dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52bbd-158">The application command.</span></span> <span data-ttu-id="52bbd-159">Si noti che nell'esempio vengono usate costanti simboliche.</span><span class="sxs-lookup"><span data-stu-id="52bbd-159">Notice that symbolic constants are used in the example.</span></span> <span data-ttu-id="52bbd-160">Il file di definizione delle risorse include resource.h, in cui sono definite queste costanti.</span><span class="sxs-lookup"><span data-stu-id="52bbd-160">The resource definition file includes resource.h, where these constants are defined.</span></span>
-   <span data-ttu-id="52bbd-161">La parola **chiave VIRTKEY** indica che la prima voce è un codice di chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="52bbd-161">The keyword **VIRTKEY** means the first entry is a virtual-key code.</span></span> <span data-ttu-id="52bbd-162">L'altra opzione è l'uso di caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="52bbd-162">The other option is to use ASCII characters.</span></span>
-   <span data-ttu-id="52bbd-163">Modificatori facoltativi: ALT, CONTROL o MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="52bbd-163">Optional modifiers: ALT, CONTROL, or SHIFT.</span></span>

<span data-ttu-id="52bbd-164">Se si usano caratteri ASCII per i tasti di scelta rapida, un carattere minuscolo sarà un tasto di scelta rapida diverso da un carattere maiuscolo.</span><span class="sxs-lookup"><span data-stu-id="52bbd-164">If you use ASCII characters for shortcuts, then a lowercase character will be a different shortcut than an uppercase character.</span></span> <span data-ttu-id="52bbd-165">Ad esempio, la digitazione di "a" potrebbe richiamare un comando diverso rispetto alla digitazione di "A". Questo potrebbe confondere gli utenti, quindi è in genere consigliabile usare codici di chiave virtuale, anziché caratteri ASCII, per i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="52bbd-165">(For example, typing 'a' might invoke a different command than typing 'A'.) That might confuse users, so it is generally better to use virtual-key codes, rather than ASCII characters, for shortcuts.</span></span>

## <a name="loading-the-accelerator-table"></a><span data-ttu-id="52bbd-166">Caricamento della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="52bbd-166">Loading the Accelerator Table</span></span>

<span data-ttu-id="52bbd-167">La risorsa per la tabella dei tasti di scelta rapida deve essere caricata prima che il programma possa usarla.</span><span class="sxs-lookup"><span data-stu-id="52bbd-167">The resource for the accelerator table must be loaded before the program can use it.</span></span> <span data-ttu-id="52bbd-168">Per caricare una tabella dei tasti di scelta rapida, chiamare la [**funzione LoadAccelerators.**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa)</span><span class="sxs-lookup"><span data-stu-id="52bbd-168">To load an accelerator table, call the [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) function.</span></span>


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



<span data-ttu-id="52bbd-169">Chiamare questa funzione prima di immettere il ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="52bbd-169">Call this function before you enter the message loop.</span></span> <span data-ttu-id="52bbd-170">Il primo parametro è l'handle per il modulo.</span><span class="sxs-lookup"><span data-stu-id="52bbd-170">The first parameter is the handle to the module.</span></span> <span data-ttu-id="52bbd-171">Questo parametro viene passato alla [**funzione WinMain.**](/windows/desktop/api/winbase/nf-winbase-winmain)</span><span class="sxs-lookup"><span data-stu-id="52bbd-171">(This parameter is passed to your [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="52bbd-172">Per informazioni dettagliate, vedere [WinMain: Il punto di ingresso dell'applicazione.](winmain--the-application-entry-point.md) Il secondo parametro è l'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="52bbd-172">For details, see [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).) The second parameter is the resource identifier.</span></span> <span data-ttu-id="52bbd-173">La funzione restituisce un handle per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="52bbd-173">The function returns a handle to the resource.</span></span> <span data-ttu-id="52bbd-174">Si noti che un handle è un tipo opaco che fa riferimento a un oggetto gestito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="52bbd-174">Recall that a handle is an opaque type that refers to an object managed by the system.</span></span> <span data-ttu-id="52bbd-175">Se la funzione ha esito negativo, restituisce **NULL.**</span><span class="sxs-lookup"><span data-stu-id="52bbd-175">If the function fails, it returns **NULL**.</span></span>

<span data-ttu-id="52bbd-176">È possibile rilasciare una tabella dei tasti di scelta rapida [**chiamando DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span><span class="sxs-lookup"><span data-stu-id="52bbd-176">You can release an accelerator table by calling [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span></span> <span data-ttu-id="52bbd-177">Tuttavia, il sistema rilascia automaticamente la tabella all'uscita del programma, quindi è necessario chiamare questa funzione solo se si sostituisce una tabella con un'altra.</span><span class="sxs-lookup"><span data-stu-id="52bbd-177">However, the system automatically releases the table when the program exits, so you only need to call this function if you are replacing one table with another.</span></span> <span data-ttu-id="52bbd-178">È disponibile un esempio interessante di questo argomento nell'argomento [Creazione di acceleratori modificabili dall'utente](/windows/desktop/menurc/using-keyboard-accelerators).</span><span class="sxs-lookup"><span data-stu-id="52bbd-178">There is an interesting example of this in the topic [Creating User Editable Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span></span>

## <a name="translating-key-strokes-into-commands"></a><span data-ttu-id="52bbd-179">Traduzione di tratti chiave in comandi</span><span class="sxs-lookup"><span data-stu-id="52bbd-179">Translating Key Strokes into Commands</span></span>

<span data-ttu-id="52bbd-180">Una tabella dei tasti di scelta rapida funziona traducendo i tratti dei tasti in [**messaggi WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="52bbd-180">An accelerator table works by translating key strokes into [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="52bbd-181">Il *parametro wParam* di **WM \_ COMMAND** contiene l'identificatore numerico del comando.</span><span class="sxs-lookup"><span data-stu-id="52bbd-181">The *wParam* parameter of **WM\_COMMAND** contains the numeric identifier of the command.</span></span> <span data-ttu-id="52bbd-182">Ad esempio, usando la tabella illustrata in precedenza, il tasto CTRL+M viene convertito in un **messaggio WM \_ COMMAND** con il valore `ID_TOGGLE_MODE` .</span><span class="sxs-lookup"><span data-stu-id="52bbd-182">For example, using the table shown previously, the key stroke CTRL+M is translated into a **WM\_COMMAND** message with the value `ID_TOGGLE_MODE`.</span></span> <span data-ttu-id="52bbd-183">A tale scopo, modificare il ciclo di messaggi nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="52bbd-183">To make this happen, change your message loop to the following:</span></span>


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



<span data-ttu-id="52bbd-184">Questo codice aggiunge una chiamata alla [**funzione TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) all'interno del ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="52bbd-184">This code adds a call to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function inside the message loop.</span></span> <span data-ttu-id="52bbd-185">La **funzione TranslateAccelerator** esamina ogni messaggio della finestra, cercando i messaggi key-down.</span><span class="sxs-lookup"><span data-stu-id="52bbd-185">The **TranslateAccelerator** function examines each window message, looking for key-down messages.</span></span> <span data-ttu-id="52bbd-186">Se l'utente preme una delle combinazioni di tasti elencate nella tabella dei tasti di scelta rapida, **TranslateAccelerator** invia un messaggio [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="52bbd-186">If the user presses one of the key combinations listed in the accelerator table, **TranslateAccelerator** sends a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message to the window.</span></span> <span data-ttu-id="52bbd-187">La funzione invia **WM \_ COMMAND** richiamando direttamente la routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="52bbd-187">The function sends **WM\_COMMAND** by directly invoking the window procedure.</span></span> <span data-ttu-id="52bbd-188">Quando **TranslateAccelerator** converte correttamente un tratto di tasto, la funzione restituisce un valore diverso da zero, il che significa che è necessario ignorare la normale elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="52bbd-188">When **TranslateAccelerator** successfully translates a key stroke, the function returns a non-zero value, which means you should skip the normal processing for the message.</span></span> <span data-ttu-id="52bbd-189">In caso **contrario, TranslateAccelerator** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="52bbd-189">Otherwise, **TranslateAccelerator** returns zero.</span></span> <span data-ttu-id="52bbd-190">In tal caso, passare il messaggio della finestra [**a TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), come di consueto.</span><span class="sxs-lookup"><span data-stu-id="52bbd-190">In that case, pass the window message to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), as normal.</span></span>

<span data-ttu-id="52bbd-191">Ecco come il programma di disegno può gestire il [**messaggio WM \_ COMMAND:**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="52bbd-191">Here is how the drawing program might handle the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message:</span></span>


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



<span data-ttu-id="52bbd-192">Questo codice presuppone che sia `SetMode` una funzione definita dall'applicazione per passare da una modalità all'altra.</span><span class="sxs-lookup"><span data-stu-id="52bbd-192">This code assumes that `SetMode` is a function defined by the application to switch between the two modes.</span></span> <span data-ttu-id="52bbd-193">I dettagli su come gestire ogni comando dipendono ovviamente dal programma.</span><span class="sxs-lookup"><span data-stu-id="52bbd-193">The details of how you would handle each command obviously depend on your program.</span></span>

## <a name="next"></a><span data-ttu-id="52bbd-194">Prossima</span><span class="sxs-lookup"><span data-stu-id="52bbd-194">Next</span></span>

[<span data-ttu-id="52bbd-195">Impostazione dell'immagine del cursore</span><span class="sxs-lookup"><span data-stu-id="52bbd-195">Setting the Cursor Image</span></span>](setting-the-cursor-image.md)

 

 
