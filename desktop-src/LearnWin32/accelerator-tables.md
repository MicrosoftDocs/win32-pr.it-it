---
title: Tabelle dei tasti di scelta rapida
description: .
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9929445809bee71f273b6bd2334e182de59edbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046754"
---
# <a name="accelerator-tables"></a><span data-ttu-id="f0f1a-103">Tabelle dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="f0f1a-103">Accelerator Tables</span></span>

<span data-ttu-id="f0f1a-104">Le applicazioni spesso definiscono scelte rapide da tastiera, ad esempio CTRL + O per il comando Apri file.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-104">Applications often define keyboard shortcuts, such as CTRL+O for the File Open command.</span></span> <span data-ttu-id="f0f1a-105">È possibile implementare le scelte rapide da tastiera gestendo singoli messaggi di [**WM \_**](/windows/desktop/inputdev/wm-keydown) . Tuttavia, le tabelle degli acceleratori forniscono una soluzione migliore:</span><span class="sxs-lookup"><span data-stu-id="f0f1a-105">You could implement keyboard shortcuts by handling individual [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, but accelerator tables provide a better solution that:</span></span>

-   <span data-ttu-id="f0f1a-106">Richiede un minor numero di codice.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-106">Requires less coding.</span></span>
-   <span data-ttu-id="f0f1a-107">Consolida tutti i collegamenti in un unico file di dati.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-107">Consolidates all of your shortcuts into one data file.</span></span>
-   <span data-ttu-id="f0f1a-108">Supporta la localizzazione in altre lingue.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-108">Supports localization into other languages.</span></span>
-   <span data-ttu-id="f0f1a-109">Consente ai tasti di scelta rapida e ai comandi di menu di usare la stessa logica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-109">Enables shortcuts and menu commands to use the same application logic.</span></span>

<span data-ttu-id="f0f1a-110">Una *tabella di tasti di scelta rapida* è una risorsa di dati che esegue il mapping delle combinazioni di tasti, ad esempio CTRL + O, ai comandi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-110">An *accelerator table* is a data resource that maps keyboard combinations, such as CTRL+O, to application commands.</span></span> <span data-ttu-id="f0f1a-111">Prima di vedere come usare una tabella di tasti di scelta rapida, è necessaria una rapida introduzione alle risorse.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-111">Before we see how to use an accelerator table, we'll need a quick introduction to resources.</span></span> <span data-ttu-id="f0f1a-112">Una *risorsa* è un BLOB di dati incorporato in un file binario dell'applicazione (exe o dll).</span><span class="sxs-lookup"><span data-stu-id="f0f1a-112">A *resource* is a data blob that is built into an application binary (EXE or DLL).</span></span> <span data-ttu-id="f0f1a-113">Le risorse archiviano i dati necessari per l'applicazione, ad esempio menu, cursori, icone, immagini, stringhe di testo o qualsiasi tipo di dati dell'applicazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-113">Resources store data that are needed by the application, such as menus, cursors, icons, images, text strings, or any custom application data.</span></span> <span data-ttu-id="f0f1a-114">L'applicazione carica i dati della risorsa dal file binario in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-114">The application loads the resource data from the binary at run time.</span></span> <span data-ttu-id="f0f1a-115">Per includere le risorse in un file binario, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0f1a-115">To include resources in a binary, do the following:</span></span>

1.  <span data-ttu-id="f0f1a-116">Creare un file di definizione di risorsa (RC).</span><span class="sxs-lookup"><span data-stu-id="f0f1a-116">Create a resource definition (.rc) file.</span></span> <span data-ttu-id="f0f1a-117">Questo file definisce i tipi di risorse e i relativi identificatori.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-117">This file defines the types of resources and their identifiers.</span></span> <span data-ttu-id="f0f1a-118">Il file di definizione della risorsa può includere riferimenti ad altri file.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-118">The resource definition file may include references to other files.</span></span> <span data-ttu-id="f0f1a-119">Ad esempio, una risorsa icona viene dichiarata nel file RC, ma l'immagine dell'icona viene archiviata in un file separato.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-119">For example, an icon resource is declared in the .rc file, but the icon image is stored in a separate file.</span></span>
2.  <span data-ttu-id="f0f1a-120">Usare il compilatore di risorse di Microsoft Windows (RC) per compilare il file di definizione di risorsa in un file di risorse compilato (res).</span><span class="sxs-lookup"><span data-stu-id="f0f1a-120">Use the Microsoft Windows Resource Compiler (RC) to compile the resource definition file into a compiled resource (.res) file.</span></span> <span data-ttu-id="f0f1a-121">Il compilatore RC viene fornito con Visual Studio e anche con la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-121">The RC compiler is provided with Visual Studio and also the Windows SDK.</span></span>
3.  <span data-ttu-id="f0f1a-122">Collegare il file di risorse compilato al file binario.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-122">Link the compiled resource file to the binary file.</span></span>

<span data-ttu-id="f0f1a-123">Questi passaggi sono approssimativamente equivalenti al processo di compilazione/collegamento per i file di codice.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-123">These steps are roughly equivalent to the compile/link process for code files.</span></span> <span data-ttu-id="f0f1a-124">Visual Studio offre un set di editor di risorse che semplificano la creazione e la modifica delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-124">Visual Studio provides a set of resource editors that make it easy to create and modify resources.</span></span> <span data-ttu-id="f0f1a-125">Questi strumenti non sono disponibili nelle edizioni Express di Visual Studio. Tuttavia, un file RC è semplicemente un file di testo e la sintassi è documentata in MSDN, quindi è possibile creare un file RC usando un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-125">(These tools are not available in the Express editions of Visual Studio.) But an .rc file is simply a text file, and the syntax is documented on MSDN, so it is possible to create an .rc file using any text editor.</span></span> <span data-ttu-id="f0f1a-126">Per ulteriori informazioni, vedere [informazioni sui file di risorse](/windows/desktop/menurc/about-resource-files).</span><span class="sxs-lookup"><span data-stu-id="f0f1a-126">For more information, see [About Resource Files](/windows/desktop/menurc/about-resource-files).</span></span>

## <a name="defining-an-accelerator-table"></a><span data-ttu-id="f0f1a-127">Definizione di una tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="f0f1a-127">Defining an Accelerator Table</span></span>

<span data-ttu-id="f0f1a-128">Una tabella di tasti di scelta rapida è una tabella di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-128">An accelerator table is a table of keyboard shortcuts.</span></span> <span data-ttu-id="f0f1a-129">Ogni collegamento è definito da:</span><span class="sxs-lookup"><span data-stu-id="f0f1a-129">Each shortcut is defined by:</span></span>

-   <span data-ttu-id="f0f1a-130">Identificatore numerico.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-130">A numeric identifier.</span></span> <span data-ttu-id="f0f1a-131">Questo numero identifica il comando dell'applicazione che verrà richiamato dal collegamento.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-131">This number identifies the application command that will be invoked by the shortcut.</span></span>
-   <span data-ttu-id="f0f1a-132">Il carattere ASCII o il codice della chiave virtuale del collegamento.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-132">The ASCII character or virtual-key code of the shortcut.</span></span>
-   <span data-ttu-id="f0f1a-133">Tasti di modifica facoltativi: ALT, MAIUSC o CTRL.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-133">Optional modifier keys: ALT, SHIFT, or CTRL.</span></span>

<span data-ttu-id="f0f1a-134">La tabella dei tasti di scelta rapida contiene un identificatore numerico che identifica la tabella nell'elenco delle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-134">The accelerator table itself has a numeric identifier, which identifies the table in the list of application resources.</span></span> <span data-ttu-id="f0f1a-135">Viene ora creata una tabella dei tasti di scelta rapida per un semplice programma di disegno.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-135">Let's create an accelerator table for a simple drawing program.</span></span> <span data-ttu-id="f0f1a-136">Questo programma disporrà di due modalità, modalità di visualizzazione e modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-136">This program will have two modes, draw mode and selection mode.</span></span> <span data-ttu-id="f0f1a-137">In modalità di estrazione, l'utente può creare forme.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-137">In draw mode, the user can draw shapes.</span></span> <span data-ttu-id="f0f1a-138">In modalità di selezione, l'utente può selezionare forme.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-138">In selection mode, the user can select shapes.</span></span> <span data-ttu-id="f0f1a-139">Per questo programma si desidera definire i tasti di scelta rapida seguenti.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-139">For this program, we would like to define the following keyboard shortcuts.</span></span>



| <span data-ttu-id="f0f1a-140">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="f0f1a-140">Shortcut</span></span> | <span data-ttu-id="f0f1a-141">Comando</span><span class="sxs-lookup"><span data-stu-id="f0f1a-141">Command</span></span>                   |
|----------|---------------------------|
| <span data-ttu-id="f0f1a-142">CTRL+M</span><span class="sxs-lookup"><span data-stu-id="f0f1a-142">CTRL+M</span></span>   | <span data-ttu-id="f0f1a-143">Consente di passare da una modalità all'altra.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-143">Toggle between modes.</span></span>     |
| <span data-ttu-id="f0f1a-144">F1</span><span class="sxs-lookup"><span data-stu-id="f0f1a-144">F1</span></span>       | <span data-ttu-id="f0f1a-145">Passa alla modalità di estrazione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-145">Switch to draw mode.</span></span>      |
| <span data-ttu-id="f0f1a-146">F2</span><span class="sxs-lookup"><span data-stu-id="f0f1a-146">F2</span></span>       | <span data-ttu-id="f0f1a-147">Passa alla modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-147">Switch to selection mode.</span></span> |



 

<span data-ttu-id="f0f1a-148">Per prima cosa, definire gli identificatori numerici per la tabella e per i comandi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-148">First, define numeric identifiers for the table and for the application commands.</span></span> <span data-ttu-id="f0f1a-149">Questi valori sono arbitrari.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-149">These values are arbitrary.</span></span> <span data-ttu-id="f0f1a-150">È possibile assegnare costanti simboliche per gli identificatori definendoli in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-150">You can assign symbolic constants for the identifiers by defining them in a header file.</span></span> <span data-ttu-id="f0f1a-151">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f0f1a-151">For example:</span></span>


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



<span data-ttu-id="f0f1a-152">In questo esempio, il valore `IDR_ACCEL1` identifica la tabella dei tasti di scelta rapida e le tre costanti successive definiscono i comandi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-152">In this example, the value `IDR_ACCEL1` identifies the accelerator table, and the next three constants define the application commands.</span></span> <span data-ttu-id="f0f1a-153">Per convenzione, un file di intestazione che definisce le costanti di risorsa è spesso denominato Resource. h.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-153">By convention, a header file that defines resource constants is often named resource.h.</span></span> <span data-ttu-id="f0f1a-154">L'elenco successivo Mostra il file di definizione di risorsa.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-154">The next listing shows the resource definition file.</span></span>


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



<span data-ttu-id="f0f1a-155">I tasti di scelta rapida vengono definiti tra parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-155">The accelerator shortcuts are defined within the curly braces.</span></span> <span data-ttu-id="f0f1a-156">Ogni collegamento contiene le voci seguenti.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-156">Each shortcut contains the following entries.</span></span>

-   <span data-ttu-id="f0f1a-157">Il codice della chiave virtuale o il carattere ASCII che richiama il collegamento.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-157">The virtual-key code or ASCII character that invokes the shortcut.</span></span>
-   <span data-ttu-id="f0f1a-158">Comando dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-158">The application command.</span></span> <span data-ttu-id="f0f1a-159">Si noti che nell'esempio vengono usate costanti simboliche.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-159">Notice that symbolic constants are used in the example.</span></span> <span data-ttu-id="f0f1a-160">Il file di definizione della risorsa include Resource. h, in cui sono definite queste costanti.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-160">The resource definition file includes resource.h, where these constants are defined.</span></span>
-   <span data-ttu-id="f0f1a-161">La parola chiave **VIRTKEY** indica che la prima voce è un codice di chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-161">The keyword **VIRTKEY** means the first entry is a virtual-key code.</span></span> <span data-ttu-id="f0f1a-162">L'altra opzione consiste nell'usare caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-162">The other option is to use ASCII characters.</span></span>
-   <span data-ttu-id="f0f1a-163">Modificatori facoltativi: ALT, CTRL o MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-163">Optional modifiers: ALT, CONTROL, or SHIFT.</span></span>

<span data-ttu-id="f0f1a-164">Se si usano caratteri ASCII per i collegamenti, un carattere minuscolo sarà un tasto di scelta rapida diverso da un carattere maiuscolo.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-164">If you use ASCII characters for shortcuts, then a lowercase character will be a different shortcut than an uppercase character.</span></span> <span data-ttu-id="f0f1a-165">(Ad esempio, la digitazione di ' a' potrebbe richiamare un comando diverso rispetto alla digitazione di ' A '). Questo potrebbe confondere gli utenti, quindi è in genere preferibile usare i codici a chiave virtuale, anziché i caratteri ASCII, per i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-165">(For example, typing 'a' might invoke a different command than typing 'A'.) That might confuse users, so it is generally better to use virtual-key codes, rather than ASCII characters, for shortcuts.</span></span>

## <a name="loading-the-accelerator-table"></a><span data-ttu-id="f0f1a-166">Caricamento della tabella dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="f0f1a-166">Loading the Accelerator Table</span></span>

<span data-ttu-id="f0f1a-167">Per poter utilizzare il programma, è necessario caricare la risorsa per la tabella dei tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-167">The resource for the accelerator table must be loaded before the program can use it.</span></span> <span data-ttu-id="f0f1a-168">Per caricare una tabella dei tasti di scelta rapida, chiamare la funzione [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) .</span><span class="sxs-lookup"><span data-stu-id="f0f1a-168">To load an accelerator table, call the [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) function.</span></span>


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



<span data-ttu-id="f0f1a-169">Chiamare questa funzione prima di immettere il ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-169">Call this function before you enter the message loop.</span></span> <span data-ttu-id="f0f1a-170">Il primo parametro è l'handle per il modulo.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-170">The first parameter is the handle to the module.</span></span> <span data-ttu-id="f0f1a-171">Questo parametro viene passato alla funzione [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="f0f1a-171">(This parameter is passed to your [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="f0f1a-172">Per informazioni dettagliate, vedere [WinMain: punto di ingresso dell'applicazione](winmain--the-application-entry-point.md). Il secondo parametro è l'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-172">For details, see [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).) The second parameter is the resource identifier.</span></span> <span data-ttu-id="f0f1a-173">La funzione restituisce un handle per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-173">The function returns a handle to the resource.</span></span> <span data-ttu-id="f0f1a-174">Si ricordi che un handle è un tipo opaco che fa riferimento a un oggetto gestito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-174">Recall that a handle is an opaque type that refers to an object managed by the system.</span></span> <span data-ttu-id="f0f1a-175">Se la funzione ha esito negativo, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-175">If the function fails, it returns **NULL**.</span></span>

<span data-ttu-id="f0f1a-176">È possibile rilasciare una tabella dei tasti di scelta rapida chiamando [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span><span class="sxs-lookup"><span data-stu-id="f0f1a-176">You can release an accelerator table by calling [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span></span> <span data-ttu-id="f0f1a-177">Tuttavia, il sistema rilascia automaticamente la tabella quando il programma viene chiuso, quindi è necessario chiamare questa funzione solo se si sostituisce una tabella con un'altra.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-177">However, the system automatically releases the table when the program exits, so you only need to call this function if you are replacing one table with another.</span></span> <span data-ttu-id="f0f1a-178">Questo è un esempio interessante nell'argomento [creazione di acceleratori modificabili dall'utente](/windows/desktop/menurc/using-keyboard-accelerators).</span><span class="sxs-lookup"><span data-stu-id="f0f1a-178">There is an interesting example of this in the topic [Creating User Editable Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span></span>

## <a name="translating-key-strokes-into-commands"></a><span data-ttu-id="f0f1a-179">Conversione dei tratti chiave in comandi</span><span class="sxs-lookup"><span data-stu-id="f0f1a-179">Translating Key Strokes into Commands</span></span>

<span data-ttu-id="f0f1a-180">Una tabella di tasti di scelta rapida funziona convertendo i tratti chiave in messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="f0f1a-180">An accelerator table works by translating key strokes into [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="f0f1a-181">Il parametro *wParam* del **\_ comando WM** contiene l'identificatore numerico del comando.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-181">The *wParam* parameter of **WM\_COMMAND** contains the numeric identifier of the command.</span></span> <span data-ttu-id="f0f1a-182">Ad esempio, usando la tabella illustrata in precedenza, il tratto della chiave CTRL + M viene convertito in un messaggio di **\_ comando WM** con il valore `ID_TOGGLE_MODE` .</span><span class="sxs-lookup"><span data-stu-id="f0f1a-182">For example, using the table shown previously, the key stroke CTRL+M is translated into a **WM\_COMMAND** message with the value `ID_TOGGLE_MODE`.</span></span> <span data-ttu-id="f0f1a-183">Per eseguire questa operazione, modificare il ciclo di messaggi nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="f0f1a-183">To make this happen, change your message loop to the following:</span></span>


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



<span data-ttu-id="f0f1a-184">Questo codice aggiunge una chiamata alla funzione [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) all'interno del ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-184">This code adds a call to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function inside the message loop.</span></span> <span data-ttu-id="f0f1a-185">La funzione **TranslateAccelerator** esamina ogni messaggio della finestra, cercando i messaggi di chiave inattiva.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-185">The **TranslateAccelerator** function examines each window message, looking for key-down messages.</span></span> <span data-ttu-id="f0f1a-186">Se l'utente preme una delle combinazioni di tasti elencate nella tabella dei tasti di scelta rapida, **TranslateAccelerator** Invia un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-186">If the user presses one of the key combinations listed in the accelerator table, **TranslateAccelerator** sends a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message to the window.</span></span> <span data-ttu-id="f0f1a-187">La funzione Invia **il \_ comando WM** richiamando direttamente la routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-187">The function sends **WM\_COMMAND** by directly invoking the window procedure.</span></span> <span data-ttu-id="f0f1a-188">Quando **TranslateAccelerator** converte correttamente un tratto di chiave, la funzione restituisce un valore diverso da zero, il che significa che è necessario ignorare la normale elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-188">When **TranslateAccelerator** successfully translates a key stroke, the function returns a non-zero value, which means you should skip the normal processing for the message.</span></span> <span data-ttu-id="f0f1a-189">In caso contrario, **TranslateAccelerator** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-189">Otherwise, **TranslateAccelerator** returns zero.</span></span> <span data-ttu-id="f0f1a-190">In tal caso, passare il messaggio della finestra a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), come di consueto.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-190">In that case, pass the window message to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), as normal.</span></span>

<span data-ttu-id="f0f1a-191">Ecco il modo in cui il programma di disegno può gestire il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) :</span><span class="sxs-lookup"><span data-stu-id="f0f1a-191">Here is how the drawing program might handle the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message:</span></span>


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



<span data-ttu-id="f0f1a-192">Questo codice presuppone che `SetMode` sia una funzione definita dall'applicazione per passare tra le due modalità.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-192">This code assumes that `SetMode` is a function defined by the application to switch between the two modes.</span></span> <span data-ttu-id="f0f1a-193">I dettagli su come gestire ogni comando dipendono ovviamente dal programma.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-193">The details of how you would handle each command obviously depend on your program.</span></span>

## <a name="next"></a><span data-ttu-id="f0f1a-194">Prossima</span><span class="sxs-lookup"><span data-stu-id="f0f1a-194">Next</span></span>

[<span data-ttu-id="f0f1a-195">Impostazione dell'immagine del cursore</span><span class="sxs-lookup"><span data-stu-id="f0f1a-195">Setting the Cursor Image</span></span>](setting-the-cursor-image.md)

 

 