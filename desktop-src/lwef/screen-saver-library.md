---
title: Gestione degli screen saver
description: L'API Microsoft Win32 supporta applicazioni speciali denominate screen saver.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- screen saver
- Pannello di controllo, screen saver
- ScreenSaverConfigureDialog
- file di definizione moduli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473019"
---
# <a name="handling-screen-savers"></a><span data-ttu-id="d5ca5-107">Gestione degli screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-107">Handling Screen Savers</span></span>

<span data-ttu-id="d5ca5-108">L'API Microsoft Win32 supporta applicazioni speciali denominate *screen saver*.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-108">The Microsoft Win32 API supports special applications called *screen savers*.</span></span> <span data-ttu-id="d5ca5-109">Gli screen saver iniziano quando il mouse e la tastiera sono rimasti inattivi per un periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-109">Screen savers start when the mouse and keyboard have been idle for a specified period of time.</span></span> <span data-ttu-id="d5ca5-110">Vengono usati per i due motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5ca5-110">They are used for these two reasons:</span></span>

-   <span data-ttu-id="d5ca5-111">Per proteggere una schermata dall'ustione fosforo causata da immagini statiche.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-111">To protect a screen from phosphor burn caused by static images.</span></span>
-   <span data-ttu-id="d5ca5-112">Per nascondere le informazioni riservate rimaste su una schermata.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-112">To conceal sensitive information left on a screen.</span></span>

<span data-ttu-id="d5ca5-113">Questo argomento è suddiviso nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-113">This topic is divided into the following sections.</span></span>

-   [<span data-ttu-id="d5ca5-114">Informazioni sugli screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-114">About Screen Savers</span></span>](#about-screen-savers)
-   [<span data-ttu-id="d5ca5-115">Uso delle funzioni screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-115">Using the Screen Saver Functions</span></span>](#using-the-screen-saver-functions)
    -   [<span data-ttu-id="d5ca5-116">Creazione di uno screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-116">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
    -   [<span data-ttu-id="d5ca5-117">Installazione di nuovi screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-117">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
    -   [<span data-ttu-id="d5ca5-118">Aggiunta della Guida alla finestra di dialogo configurazione screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-118">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a><span data-ttu-id="d5ca5-119">Informazioni sugli screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-119">About Screen Savers</span></span>

<span data-ttu-id="d5ca5-120">L'applicazione desktop nel pannello di controllo di Windows consente agli utenti di eseguire una selezione da un elenco di screen saver, specificare la quantità di tempo che deve trascorrere prima che l'screen saver venga avviata, configurare gli screen saver e visualizzare i salvaschermi.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-120">The Desktop application in the Windows Control Panel lets users select from a list of screen savers, specify how much time should elapse before the screen saver starts, configure screen savers, and preview screen savers.</span></span> <span data-ttu-id="d5ca5-121">Gli screen saver vengono caricati automaticamente all'avvio di Windows o quando un utente attiva il screen saver tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-121">Screen savers are loaded automatically when Windows starts or when a user activates the screen saver through the Control Panel.</span></span>

<span data-ttu-id="d5ca5-122">Una volta scelto un screen saver, Windows monitora le sequenze di tasti e i movimenti del mouse, quindi avvia il screen saver dopo un periodo di inattività.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-122">Once a screen saver is chosen, Windows monitors keystrokes and mouse movements and then starts the screen saver after a period of inactivity.</span></span> <span data-ttu-id="d5ca5-123">Tuttavia, Windows non avvia il screen saver se sussistono le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5ca5-123">However, Windows does not start the screen saver if any of the following conditions exist:</span></span>

-   <span data-ttu-id="d5ca5-124">L'applicazione attiva non è un'applicazione basata su Windows.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-124">The active application is not a Windows-based application.</span></span>
-   <span data-ttu-id="d5ca5-125">È presente una finestra di training basata su computer (CBT).</span><span class="sxs-lookup"><span data-stu-id="d5ca5-125">A computer-based training (CBT) window is present.</span></span>
-   <span data-ttu-id="d5ca5-126">L'applicazione attiva riceve il messaggio [WM \_ SYSCOMMAND](../menurc/wm-syscommand.md) con il parametro *wParam* impostato sul valore SC \_ SCREENSAVE, ma non passa il messaggio alla funzione [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-126">The active application receives the [WM\_SYSCOMMAND](../menurc/wm-syscommand.md) message with the *wParam* parameter set to the SC\_SCREENSAVE value, but it does not pass the message to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="d5ca5-127">**Contesto di sicurezza dello screen saver**</span><span class="sxs-lookup"><span data-stu-id="d5ca5-127">**Security Context of the Screen Saver**</span></span>

<span data-ttu-id="d5ca5-128">Il contesto di sicurezza del screen saver dipende dal fatto che un utente sia connesso in modo interattivo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-128">The security context of the screen saver is dependent on whether a user is interactively logged on.</span></span> <span data-ttu-id="d5ca5-129">Se un utente è connesso in modo interattivo quando viene richiamato il screen saver, il screen saver viene eseguito nel contesto di sicurezza dell'utente interattivo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-129">If a user is interactively logged on when the screen saver is invoked, the screen saver runs in the security context of the interactive user.</span></span> <span data-ttu-id="d5ca5-130">Se nessun utente è connesso, il contesto di sicurezza del screen saver dipende dalla versione di Windows in uso.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-130">If no user is logged on, the security context of the screen saver is dependent on the version of Windows being used.</span></span>

-   <span data-ttu-id="d5ca5-131">Windows XP e Windows 2000-screen saver vengono eseguiti nel contesto di LocalSystem con account con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-131">Windows XP and Windows 2000 - screen saver runs in the context of LocalSystem with accounts restricted.</span></span>
-   <span data-ttu-id="d5ca5-132">Windows 2003-screen saver viene eseguito nel contesto di LocalService con tutti i privilegi rimossi e il gruppo Administrators è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-132">Windows 2003 - screen saver runs in the context of LocalService with all privileges removed and administrators group disabled.</span></span>
-   <span data-ttu-id="d5ca5-133">Non si applica a Windows NT4.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-133">Does not apply to Windows NT4.</span></span>

<span data-ttu-id="d5ca5-134">Il contesto di sicurezza determina il livello delle operazioni con privilegi che possono essere eseguite da un screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-134">The security context determines the level of privileged operations which can be done from a screen saver.</span></span>

<span data-ttu-id="d5ca5-135">**Windows Vista e versioni successive:** Se la protezione con password è abilitata dal criterio, l'screen saver viene avviata indipendentemente dall'operazione eseguita da un'applicazione con la \_ notifica SC SCREENSAVE.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-135">**Windows Vista and later:** If password protection is enabled by policy, the screen saver is started regardless of what an application does with the SC\_SCREENSAVE notification.</span></span>

<span data-ttu-id="d5ca5-136">Gli screen saver contengono funzioni esportate, definizioni di risorse e dichiarazioni di variabili specifiche.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-136">Screen savers contain specific exported functions, resource definitions, and variable declarations.</span></span> <span data-ttu-id="d5ca5-137">La libreria screen saver contiene la funzione **principale** e un altro codice di avvio necessario per un screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-137">The screen saver library contains the **main** function and other startup code required for a screen saver.</span></span> <span data-ttu-id="d5ca5-138">All'avvio di un screen saver, il codice di avvio nella libreria screen saver crea una finestra a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-138">When a screen saver starts, the startup code in the screen saver library creates a full-screen window.</span></span> <span data-ttu-id="d5ca5-139">La classe della finestra per questa finestra è dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="d5ca5-139">The window class for this window is declared as follows:</span></span>


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



<span data-ttu-id="d5ca5-140">Per creare una screen saver, la maggior parte degli sviluppatori crea un modulo di codice sorgente contenente tre funzioni obbligatorie e le collega alla libreria di screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-140">To create a screen saver, most developers create a source code module containing three required functions and link them with the screen saver library.</span></span> <span data-ttu-id="d5ca5-141">Un modulo screen saver è responsabile solo per la configurazione e per fornire effetti visivi.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-141">A screen saver module is responsible only for configuring itself and for providing visual effects.</span></span>

<span data-ttu-id="d5ca5-142">Una delle tre funzioni obbligatorie in un modulo screen saver è [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="d5ca5-142">One of the three required functions in a screen saver module is [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="d5ca5-143">Questa funzione elabora messaggi specifici e passa di nuovo i messaggi non elaborati alla libreria screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-143">This function processes specific messages and passes any unprocessed messages back to the screen saver library.</span></span> <span data-ttu-id="d5ca5-144">Di seguito sono riportati alcuni dei messaggi tipici elaborati da **ScreenSaverProc**.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-144">Following are some of the typical messages processed by **ScreenSaverProc**.</span></span>



| <span data-ttu-id="d5ca5-145">Messaggio</span><span class="sxs-lookup"><span data-stu-id="d5ca5-145">Message</span></span>        | <span data-ttu-id="d5ca5-146">Significato</span><span class="sxs-lookup"><span data-stu-id="d5ca5-146">Meaning</span></span>                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ca5-147">creazione di WM \_</span><span class="sxs-lookup"><span data-stu-id="d5ca5-147">WM\_CREATE</span></span>     | <span data-ttu-id="d5ca5-148">Recuperare tutti i dati di inizializzazione dal file di Regedit.ini.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-148">Retrieve any initialization data from the Regedit.ini file.</span></span> <span data-ttu-id="d5ca5-149">Impostare un timer di finestra per la finestra di screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-149">Set a window timer for the screen saver window.</span></span> <span data-ttu-id="d5ca5-150">Eseguire qualsiasi altra inizializzazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-150">Perform any other required initialization.</span></span>                                     |
| <span data-ttu-id="d5ca5-151">\_ERASEBKGND WM</span><span class="sxs-lookup"><span data-stu-id="d5ca5-151">WM\_ERASEBKGND</span></span> | <span data-ttu-id="d5ca5-152">Cancellare la finestra screen saver e prepararsi per le operazioni di disegno successive.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-152">Erase the screen saver window and prepare for subsequent drawing operations.</span></span>                                                                                                               |
| <span data-ttu-id="d5ca5-153">\_timer WM</span><span class="sxs-lookup"><span data-stu-id="d5ca5-153">WM\_TIMER</span></span>      | <span data-ttu-id="d5ca5-154">Eseguire operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-154">Perform drawing operations.</span></span>                                                                                                                                                                |
| <span data-ttu-id="d5ca5-155">eliminazione di WM \_</span><span class="sxs-lookup"><span data-stu-id="d5ca5-155">WM\_DESTROY</span></span>    | <span data-ttu-id="d5ca5-156">Elimina i timer creati quando l'applicazione ha elaborato il messaggio [WM \_ create](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-156">Destroy the timers created when the application processed the [WM\_CREATE](../winmsg/wm-create.md) message.</span></span> <span data-ttu-id="d5ca5-157">Eseguire eventuali operazioni di pulizia necessarie aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-157">Perform any additional required cleanup.</span></span> |



 

<span data-ttu-id="d5ca5-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passa messaggi non elaborati alla libreria screen saver chiamando la funzione [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passes unprocessed messages to the screen saver library by calling the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="d5ca5-159">Nella tabella seguente viene descritto il modo in cui questa funzione elabora vari messaggi.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-159">The following table describes how this function processes various messages.</span></span>



| <span data-ttu-id="d5ca5-160">Message</span><span class="sxs-lookup"><span data-stu-id="d5ca5-160">Message</span></span>         | <span data-ttu-id="d5ca5-161">Azione</span><span class="sxs-lookup"><span data-stu-id="d5ca5-161">Action</span></span>                                                                    |
|-----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="d5ca5-162">\_cursore WM</span><span class="sxs-lookup"><span data-stu-id="d5ca5-162">WM\_SETCURSOR</span></span>   | <span data-ttu-id="d5ca5-163">Impostare il cursore sul cursore null, rimuovendo il cursore dalla schermata.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-163">Set the cursor to the null cursor, removing it from the screen.</span></span>           |
| <span data-ttu-id="d5ca5-164">\_disegno WM</span><span class="sxs-lookup"><span data-stu-id="d5ca5-164">WM\_PAINT</span></span>       | <span data-ttu-id="d5ca5-165">Disegnare lo sfondo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-165">Paint the screen background.</span></span>                                              |
| <span data-ttu-id="d5ca5-166">\_LBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="d5ca5-166">WM\_LBUTTONDOWN</span></span> | <span data-ttu-id="d5ca5-167">Terminare il screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-167">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="d5ca5-168">\_MBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="d5ca5-168">WM\_MBUTTONDOWN</span></span> | <span data-ttu-id="d5ca5-169">Terminare il screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-169">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="d5ca5-170">\_RBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="d5ca5-170">WM\_RBUTTONDOWN</span></span> | <span data-ttu-id="d5ca5-171">Terminare il screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-171">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="d5ca5-172">KeyDown di WM \_</span><span class="sxs-lookup"><span data-stu-id="d5ca5-172">WM\_KEYDOWN</span></span>     | <span data-ttu-id="d5ca5-173">Terminare il screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-173">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="d5ca5-174">MOUSEMOVE di WM \_</span><span class="sxs-lookup"><span data-stu-id="d5ca5-174">WM\_MOUSEMOVE</span></span>   | <span data-ttu-id="d5ca5-175">Terminare il screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-175">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="d5ca5-176">\_attivazione WM</span><span class="sxs-lookup"><span data-stu-id="d5ca5-176">WM\_ACTIVATE</span></span>    | <span data-ttu-id="d5ca5-177">Terminare il screen saver se il parametro *wParam* è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-177">Terminate the screen saver if the *wParam* parameter is set to **FALSE**.</span></span> |



 

<span data-ttu-id="d5ca5-178">La seconda funzione obbligatoria in un modulo screen saver è [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span><span class="sxs-lookup"><span data-stu-id="d5ca5-178">The second required function in a screen saver module is [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span></span> <span data-ttu-id="d5ca5-179">Questa funzione Visualizza una finestra di dialogo che consente all'utente di configurare il screen saver (un'applicazione deve fornire un modello di finestra di dialogo corrispondente).</span><span class="sxs-lookup"><span data-stu-id="d5ca5-179">This function displays a dialog box that enables the user to configure the screen saver (an application must provide a corresponding dialog box template).</span></span> <span data-ttu-id="d5ca5-180">Windows consente di visualizzare la finestra di dialogo configurazione quando l'utente seleziona il pulsante di **installazione** nella finestra di dialogo screen saver del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-180">Windows displays the configuration dialog box when the user selects the **Setup** button in the Control Panel's Screen Saver dialog box.</span></span>

<span data-ttu-id="d5ca5-181">La terza funzione obbligatoria in un modulo screen saver è [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span><span class="sxs-lookup"><span data-stu-id="d5ca5-181">The third required function in a screen saver module is [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span></span> <span data-ttu-id="d5ca5-182">Questa funzione deve essere chiamata da tutte le applicazioni screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-182">This function must be called by all screen saver applications.</span></span> <span data-ttu-id="d5ca5-183">Tuttavia, le applicazioni che non necessitano di speciali finestre o controlli personalizzati nella finestra di dialogo di configurazione possono semplicemente restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-183">However, applications that do not require special windows or custom controls in the configuration dialog box can simply return **TRUE**.</span></span> <span data-ttu-id="d5ca5-184">Per la registrazione delle classi di finestra corrispondenti, le applicazioni che richiedono controlli Windows o personalizzati speciali devono usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-184">Applications requiring special windows or custom controls should use this function to register the corresponding window classes.</span></span>

<span data-ttu-id="d5ca5-185">Oltre alla creazione di un modulo che supporta le tre funzioni appena descritte, un screen saver deve fornire un'icona.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-185">In addition to creating a module that supports the three functions just described, a screen saver should supply an icon.</span></span> <span data-ttu-id="d5ca5-186">Questa icona è visibile solo quando il screen saver viene eseguito come applicazione autonoma.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-186">This icon is visible only when the screen saver is run as a standalone application.</span></span> <span data-ttu-id="d5ca5-187">(Per essere eseguito dal pannello di controllo, una screen saver deve avere l'estensione di file SCR; per essere eseguita come applicazione autonoma, è necessario che l'estensione del nome file sia exe). L'icona deve essere identificata nel file di risorse del screen saver dall'app Constant ID \_ , definita nel file di intestazione scrnsave. h.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-187">(To be run by the Control Panel, a screen saver must have the .scr file name extension; to be run as a standalone application, it must have the .exe file name extension.) The icon must be identified in the screen saver's resource file by the constant ID\_APP, which is defined in the Scrnsave.h header file.</span></span>

<span data-ttu-id="d5ca5-188">Un requisito finale è una stringa di descrizione screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-188">One final requirement is a screen saver description string.</span></span> <span data-ttu-id="d5ca5-189">Il file di risorse per un screen saver deve contenere una stringa visualizzata dal pannello di controllo come nome del screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-189">The resource file for a screen saver must contain a string that the Control Panel displays as the screen saver name.</span></span> <span data-ttu-id="d5ca5-190">La stringa di descrizione deve essere la prima stringa nella tabella di stringhe del file di risorse (identificato con il valore ordinale 1).</span><span class="sxs-lookup"><span data-stu-id="d5ca5-190">The description string must be the first string in the resource file's string table (identified with the ordinal value 1).</span></span> <span data-ttu-id="d5ca5-191">Tuttavia, la stringa di descrizione viene ignorata dal pannello di controllo se il screen saver ha un nome di file lungo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-191">However, the description string is ignored by the Control Panel if the screen saver has a long filename.</span></span> <span data-ttu-id="d5ca5-192">In tal caso, il nome del file verrà usato come stringa di descrizione.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-192">In such case, the filename will be used as the description string.</span></span>

## <a name="using-the-screen-saver-functions"></a><span data-ttu-id="d5ca5-193">Uso delle funzioni screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-193">Using the Screen Saver Functions</span></span>

<span data-ttu-id="d5ca5-194">In questa sezione viene usato il codice di esempio tratto da un'applicazione screen saver per illustrare le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5ca5-194">This section uses example code taken from a screen saver application to illustrate the following tasks:</span></span>

-   [<span data-ttu-id="d5ca5-195">Creazione di uno screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-195">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
-   [<span data-ttu-id="d5ca5-196">Installazione di nuovi screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-196">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
-   [<span data-ttu-id="d5ca5-197">Aggiunta della Guida alla finestra di dialogo configurazione screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-197">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a><span data-ttu-id="d5ca5-198">Creazione di uno screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-198">Creating a Screen Saver</span></span>

<span data-ttu-id="d5ca5-199">A intervalli compresi tra 1 e 10 secondi, l'applicazione in questo esempio disegna la schermata con uno dei quattro colori seguenti: bianco, grigio chiaro, grigio scuro e nero.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-199">At intervals ranging from 1 through 10 seconds, the application in this example repaints the screen with one of four colors: white, light gray, dark gray, and black.</span></span> <span data-ttu-id="d5ca5-200">L'applicazione disegna la schermata ogni volta che riceve un messaggio [del \_ timer WM](../winmsg/wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-200">The application paints the screen each time it receives a [WM\_TIMER](../winmsg/wm-timer.md) message.</span></span> <span data-ttu-id="d5ca5-201">L'utente può regolare l'intervallo in corrispondenza del quale viene inviato il messaggio selezionando la finestra di dialogo di configurazione dell'applicazione e modificando una singola barra di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-201">The user can adjust the interval at which this message is sent by selecting the application's configuration dialog box and adjusting a single horizontal scroll bar.</span></span>

### <a name="screen-saver-library"></a><span data-ttu-id="d5ca5-202">Libreria screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-202">Screen saver library</span></span>

<span data-ttu-id="d5ca5-203">Le funzioni di screen saver statiche sono contenute nella libreria di screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-203">The static screen saver functions are contained in the screen saver library.</span></span> <span data-ttu-id="d5ca5-204">Sono disponibili due versioni della libreria, scrnsave. lib e Scrnsavw. lib.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-204">There are two versions of the library available, Scrnsave.lib and Scrnsavw.lib.</span></span> <span data-ttu-id="d5ca5-205">È necessario collegare il progetto a uno di questi.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-205">You must link your project with one of these.</span></span> <span data-ttu-id="d5ca5-206">Scrnsave. lib viene usato per gli screen saver che usano caratteri ANSI e Scrnsavw. lib viene usato per gli screen saver che usano caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-206">Scrnsave.lib is used for screen savers that use ANSI characters, and Scrnsavw.lib is used for screen savers that use Unicode characters.</span></span> <span data-ttu-id="d5ca5-207">Un screen saver collegato a Scrnsavw. lib verrà eseguito solo su piattaforme Windows che supportano Unicode, mentre una screen saver collegata a scrnsave. lib verrà eseguita su qualsiasi piattaforma Windows.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-207">A screen saver that is linked with Scrnsavw.lib will only run on Windows platforms that support Unicode, while a screen saver linked with Scrnsave.lib will run on any Windows platform.</span></span>

### <a name="supporting-the-configuration-dialog-box"></a><span data-ttu-id="d5ca5-208">Supporto della finestra di dialogo di configurazione</span><span class="sxs-lookup"><span data-stu-id="d5ca5-208">Supporting the configuration dialog box</span></span>

<span data-ttu-id="d5ca5-209">La maggior parte degli screen saver fornisce una finestra di dialogo di configurazione che consente all'utente di specificare i dati di personalizzazione, ad esempio colori univoci, velocità di disegno, spessore linea, caratteri e così via.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-209">Most screen savers provide a configuration dialog box to let the user specify customization data such as unique colors, drawing speeds, line thickness, fonts, and so on.</span></span> <span data-ttu-id="d5ca5-210">Per supportare la finestra di dialogo configurazione, l'applicazione deve fornire un modello di finestra di dialogo e deve supportare anche la funzione [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-210">To support the configuration dialog box, the application must provide a dialog box template and must also support the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function.</span></span> <span data-ttu-id="d5ca5-211">Di seguito è riportato il modello della finestra di dialogo per l'applicazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-211">Following is the dialog box template for the sample application.</span></span>


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



<span data-ttu-id="d5ca5-212">È necessario definire la costante utilizzata per identificare il modello della finestra di dialogo usando il valore decimale 2003, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="d5ca5-212">You must define the constant used to identify the dialog box template by using the decimal value 2003, as in the following example:</span></span>


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



<span data-ttu-id="d5ca5-213">Nell'esempio seguente viene illustrata la funzione [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) trovata nell'applicazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-213">The following example shows the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function found in the sample application.</span></span>


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



<span data-ttu-id="d5ca5-214">Oltre a fornire il modello della finestra di dialogo e a supportare la funzione [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , un'applicazione deve supportare anche la funzione [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-214">In addition to providing the dialog box template and supporting the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function, an application must also support the [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) function.</span></span> <span data-ttu-id="d5ca5-215">Questa funzione registra le classi di finestra non standard richieste dal screen saver.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-215">This function registers any nonstandard window classes required by the screen saver.</span></span> <span data-ttu-id="d5ca5-216">Poiché nell'applicazione di esempio sono state utilizzate solo classi di finestra standard nella relativa routine della finestra di dialogo, questa funzione restituisce semplicemente **true**, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="d5ca5-216">Because the sample application used only standard window classes in its dialog box procedure, this function simply returns **TRUE**, as in the following example:</span></span>


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a><span data-ttu-id="d5ca5-217">Supporto della procedura screen saver finestra</span><span class="sxs-lookup"><span data-stu-id="d5ca5-217">Supporting the screen saver window procedure</span></span>

<span data-ttu-id="d5ca5-218">Ogni screen saver deve supportare una routine della finestra denominata [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="d5ca5-218">Each screen saver must support a window procedure named [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="d5ca5-219">Analogamente alla maggior parte delle routine della finestra, **ScreenSaverProc** elabora un set di messaggi specifici e passa tutti i messaggi non elaborati a una procedura predefinita.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-219">Like most window procedures, **ScreenSaverProc** processes a set of specific messages and passes any unprocessed messages to a default procedure.</span></span> <span data-ttu-id="d5ca5-220">Tuttavia, anziché passarli alla funzione [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) , **ScreenSaverProc** passa i messaggi non elaborati alla funzione [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-220">However, instead of passing them to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function, **ScreenSaverProc** passes unprocessed messages to the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="d5ca5-221">Un'altra differenza tra **ScreenSaverProc** e una normale routine della finestra è che l'handle passato a **ScreenSaverProc** identifica l'intero desktop anziché una finestra client.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-221">Another difference between **ScreenSaverProc** and a normal window procedure is that the handle passed to **ScreenSaverProc** identifies the entire desktop rather than a client window.</span></span> <span data-ttu-id="d5ca5-222">Nell'esempio seguente viene illustrata la procedura della finestra **ScreenSaverProc** per l'screen saver di esempio.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-222">The following example shows the **ScreenSaverProc** window procedure for the sample screen saver.</span></span>


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a><span data-ttu-id="d5ca5-223">Creazione di un file di definizione del modulo</span><span class="sxs-lookup"><span data-stu-id="d5ca5-223">Creating a module-definition file</span></span>

<span data-ttu-id="d5ca5-224">Le funzioni [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) e [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) devono essere esportate nel file di definizione del modulo dell'applicazione. Tuttavia, [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) non deve essere esportato.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-224">The [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) and [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) functions must be exported in the application's module-definition file; [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) should not be exported, however.</span></span> <span data-ttu-id="d5ca5-225">Nell'esempio seguente viene illustrato il file di definizione del modulo per l'applicazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-225">The following example shows the module-definition file for the sample application.</span></span>


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a><span data-ttu-id="d5ca5-226">Installazione di nuovi screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-226">Installing New Screen Savers</span></span>

<span data-ttu-id="d5ca5-227">Quando si compila l'elenco di screen saver disponibili, il pannello di controllo Cerca i file con estensione SCR nella directory di avvio di Windows.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-227">When compiling the list of available screen savers, the Control Panel searches the Windows Startup directory for files with the .scr extension.</span></span> <span data-ttu-id="d5ca5-228">Poiché gli screen saver sono file eseguibili di Windows standard con estensioni exe, è necessario rinominarli in modo che dispongano di estensioni SCR e copiarli nella directory corretta.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-228">Because screen savers are standard Windows executable files with .exe extensions, you must rename them so they have .scr extensions and copy them to the correct directory.</span></span>

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a><span data-ttu-id="d5ca5-229">Aggiunta della Guida alla finestra di dialogo configurazione screen saver</span><span class="sxs-lookup"><span data-stu-id="d5ca5-229">Adding Help to the Screen Saver Configuration Dialog Box</span></span>

<span data-ttu-id="d5ca5-230">La finestra di dialogo di configurazione per un screen saver include in genere **un pulsante?** .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-230">The configuration dialog box for a screen saver typically includes a **Help** button.</span></span> <span data-ttu-id="d5ca5-231">Le applicazioni screen saver possono verificare l'identificatore del pulsante della guida e chiamare la funzione [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) nello stesso modo in cui vengono fornite informazioni in altre applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-231">Screen saver applications can check for the Help button identifier and call the [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) function in the same way Help is provided in other Windows-based applications.</span></span>

 

 