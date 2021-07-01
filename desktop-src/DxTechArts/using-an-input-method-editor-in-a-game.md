---
title: Uso di Input Method Editor in un gioco
description: Questo articolo illustra come implementare un controllo di modifica IME di base in un'applicazione Microsoft DirectX a schermo intero.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119c5933aae14e2d3e45085dafa241a4dcb11e1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118676"
---
# <a name="using-an-input-method-editor-in-a-game"></a><span data-ttu-id="bc567-103">Uso di Input Method Editor in un gioco</span><span class="sxs-lookup"><span data-stu-id="bc567-103">Using an Input Method Editor in a Game</span></span>

> [!Note]  
> <span data-ttu-id="bc567-104">Questo articolo illustra in dettaglio l'uso di Input Method Editor (IME) di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc567-104">This article details working with the Windows XP Input Method Editor (IME).</span></span> <span data-ttu-id="bc567-105">Sono state apportate modifiche all'IME per Windows Vista che non sono completamente dettagliate in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="bc567-105">Changes were made to the IME for Windows Vista that are not fully detailed in this article.</span></span> <span data-ttu-id="bc567-106">Per altre informazioni sulle modifiche apportate all'IME per Windows Vista, vedere [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in Windows Vista - An Ever-Expanding View of Internationalization (Input Method Editors (IME) in [Windows Vista - An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) (Editor dei metodi di input in Windows Vista - Visualizzazione Ever-Expanding dell'internazionalizzazione) nel portale Microsoft Global Development and Computing Portal.</span><span class="sxs-lookup"><span data-stu-id="bc567-106">For more info about changes to the IME for Windows Vista, see [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista - An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) on the Microsoft Global Development and Computing Portal.</span></span>

 

<span data-ttu-id="bc567-107">Un input method editor (IME) è un programma che consente l'immissione di testo semplice usando una tastiera standard per le lingue dell'Asia orientale, ad esempio cinese, giapponese, coreano e altre lingue con caratteri complessi.</span><span class="sxs-lookup"><span data-stu-id="bc567-107">An input method editor (IME) is a program that allows easy text entry using a standard keyboard for East Asian languages such as Chinese, Japanese, Korean, and other languages with complex characters.</span></span> <span data-ttu-id="bc567-108">Con gli IME, ad esempio, un utente può digitare caratteri complessi in un elaboratore di testo oppure un giocatore di un gioco online multiplayer di grandi quantità può chattare con amici in caratteri complessi.</span><span class="sxs-lookup"><span data-stu-id="bc567-108">For example, with IMEs a user can type complex characters in a word processor, or a player of a massive multiplayer online game can chat with friends in complex characters.</span></span>

<span data-ttu-id="bc567-109">Questo articolo illustra come implementare un controllo di modifica IME di base in un'applicazione Microsoft DirectX a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="bc567-109">This article explains how you can implement a basic IME edit control in a full-screen Microsoft DirectX application.</span></span> <span data-ttu-id="bc567-110">Le applicazioni che sfruttano DXUT ottengono automaticamente la funzionalità IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-110">Applications that take advantage of DXUT automatically get IME functionality.</span></span> <span data-ttu-id="bc567-111">Per le applicazioni che non usano il framework, questo articolo descrive come aggiungere il supporto IME a un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-111">For applications that do not make use of the framework, this article describes how to add IME support to an edit control.</span></span>

<span data-ttu-id="bc567-112">Contenuto:</span><span class="sxs-lookup"><span data-stu-id="bc567-112">Contents:</span></span>

-   [<span data-ttu-id="bc567-113">Comportamento IME predefinito</span><span class="sxs-lookup"><span data-stu-id="bc567-113">Default IME Behavior</span></span>](#default-ime-behavior)
-   [<span data-ttu-id="bc567-114">Uso di IME con DXUT</span><span class="sxs-lookup"><span data-stu-id="bc567-114">Using IMEs with DXUT</span></span>](#using-imes-with-dxut)
-   [<span data-ttu-id="bc567-115">Override del comportamento IME predefinito</span><span class="sxs-lookup"><span data-stu-id="bc567-115">Overriding the Default IME Behavior</span></span>](#overriding-the-default-ime-behavior)
-   [<span data-ttu-id="bc567-116">Funzioni</span><span class="sxs-lookup"><span data-stu-id="bc567-116">Functions</span></span>](#functions)
-   [<span data-ttu-id="bc567-117">Messaggi</span><span class="sxs-lookup"><span data-stu-id="bc567-117">Messages</span></span>](#ime-messages)
-   [<span data-ttu-id="bc567-118">esempi</span><span class="sxs-lookup"><span data-stu-id="bc567-118">Examples</span></span>](#examples)
    -   [<span data-ttu-id="bc567-119">CHT IME versione 4.2, 4.3 e 4.4</span><span class="sxs-lookup"><span data-stu-id="bc567-119">CHT IME version 4.2, 4.3 and 4.4</span></span>](#cht-ime-version-42-43-and-44)
    -   [<span data-ttu-id="bc567-120">CHT IME versione 5.0</span><span class="sxs-lookup"><span data-stu-id="bc567-120">CHT IME version 5.0</span></span>](#cht-ime-version-50)
    -   [<span data-ttu-id="bc567-121">CHT IME versione 5.1, 5.2 e CHS IME versione 5.3</span><span class="sxs-lookup"><span data-stu-id="bc567-121">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [<span data-ttu-id="bc567-122">CHS IME versione 4.1</span><span class="sxs-lookup"><span data-stu-id="bc567-122">CHS IME version 4.1</span></span>](#chs-ime-version-41)
    -   [<span data-ttu-id="bc567-123">CHS IME versione 4.2</span><span class="sxs-lookup"><span data-stu-id="bc567-123">CHS IME version 4.2</span></span>](#chs-ime-version-42)
-   [<span data-ttu-id="bc567-124">Messaggi IME</span><span class="sxs-lookup"><span data-stu-id="bc567-124">IME Messages</span></span>](#ime-messages)
    -   [<span data-ttu-id="bc567-125">WM \_ INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="bc567-125">WM\_INPUTLANGCHANGE</span></span>](#wm_inputlangchange)
    -   [<span data-ttu-id="bc567-126">WM \_ IME \_ STARTCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="bc567-126">WM\_IME\_STARTCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="bc567-127">COMPOSIZIONE \_ IME WM \_</span><span class="sxs-lookup"><span data-stu-id="bc567-127">WM\_IME\_COMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="bc567-128">WM \_ IME \_ ENDCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="bc567-128">WM\_IME\_ENDCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="bc567-129">WM \_ IME \_ NOTIFY</span><span class="sxs-lookup"><span data-stu-id="bc567-129">WM\_IME\_NOTIFY</span></span>](/windows)
-   [<span data-ttu-id="bc567-130">Rendering</span><span class="sxs-lookup"><span data-stu-id="bc567-130">Rendering</span></span>](#rendering)
    -   [<span data-ttu-id="bc567-131">Indicatore delle impostazioni locali di input</span><span class="sxs-lookup"><span data-stu-id="bc567-131">Input Locale Indicator</span></span>](#input-locale-indicator)
    -   [<span data-ttu-id="bc567-132">Finestra di composizione</span><span class="sxs-lookup"><span data-stu-id="bc567-132">Composition Window</span></span>](#composition-window)
    -   [<span data-ttu-id="bc567-133">Lettura e finestre candidate</span><span class="sxs-lookup"><span data-stu-id="bc567-133">Reading and Candidate Windows</span></span>](#reading-and-candidate-windows)
-   [<span data-ttu-id="bc567-134">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="bc567-134">Limitations</span></span>](#limitations)
-   [<span data-ttu-id="bc567-135">Informazioni del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="bc567-135">Registry Information</span></span>](#registry-information)
-   [<span data-ttu-id="bc567-136">Appendice A: Versioni CHT per sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bc567-136">Appendix A: CHT Versions per Operating System</span></span>](#appendix-a-cht-versions-per-operating-system)
-   [<span data-ttu-id="bc567-137">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="bc567-137">Further Information</span></span>](#further-information)
-   [<span data-ttu-id="bc567-138">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="bc567-138">GetReadingString</span></span>](#getreadingstring)
-   [<span data-ttu-id="bc567-139">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="bc567-139">ShowReadingWindow</span></span>](#showreadingwindow)

## <a name="default-ime-behavior"></a><span data-ttu-id="bc567-140">Comportamento IME predefinito</span><span class="sxs-lookup"><span data-stu-id="bc567-140">Default IME Behavior</span></span>

<span data-ttu-id="bc567-141">Gli IME e mappano l'input della tastiera ai componenti fonetici o ad altri elementi del linguaggio specifici di una lingua selezionata.</span><span class="sxs-lookup"><span data-stu-id="bc567-141">IMEs map keyboard input to phonetic components or other language elements specific to a selected language.</span></span> <span data-ttu-id="bc567-142">In uno scenario tipico, l'utente tipi di chiavi che rappresentano la pronuncia di un carattere complesso.</span><span class="sxs-lookup"><span data-stu-id="bc567-142">In a typical scenario, the user types keys that represent pronunciation of a complex character.</span></span> <span data-ttu-id="bc567-143">Se l'IME riconosce la pronuncia come valida, presenta all'utente un elenco di candidati per parole o frasi da cui l'utente può selezionare una scelta finale.</span><span class="sxs-lookup"><span data-stu-id="bc567-143">If the IME recognizes the pronunciation as valid, it presents the user with a list of word or phrase candidates from which the user can select a final choice.</span></span> <span data-ttu-id="bc567-144">La parola scelta viene quindi inviata all'applicazione tramite una serie di messaggi [**CHAR WM \_ di**](/windows/desktop/inputdev/wm-char) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bc567-144">The chosen word is then sent to the application through a series of Microsoft Windows [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span> <span data-ttu-id="bc567-145">Poiché l'IME funziona a un livello inferiore all'applicazione intercettando l'input della tastiera, la presenza di un IME è trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc567-145">Because the IME works at a level below the application by intercepting keyboard input, the presence of an IME is transparent to the application.</span></span> <span data-ttu-id="bc567-146">Quasi tutte le applicazioni Windows possono immediatamente sfruttare gli IME senza essere consapevoli della loro esistenza e senza richiedere codice speciale.</span><span class="sxs-lookup"><span data-stu-id="bc567-146">Almost all Windows applications can readily take advantage of IMEs without being aware of their existence and without requiring special coding.</span></span>

<span data-ttu-id="bc567-147">Un IME tipico visualizza diverse finestre per guidare l'utente attraverso l'immissione di caratteri, come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="bc567-147">A typical IME displays several windows to guide the user through character entry, as shown in the following examples.</span></span>

![ime visualizza diverse finestre](images/ime-elements.png)

| <span data-ttu-id="bc567-149">Tipo di finestra</span><span class="sxs-lookup"><span data-stu-id="bc567-149">Window Type</span></span>                                       | <span data-ttu-id="bc567-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc567-150">Description</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="bc567-151">IME Output</span><span class="sxs-lookup"><span data-stu-id="bc567-151">IME Output</span></span>                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="bc567-152">A.</span><span class="sxs-lookup"><span data-stu-id="bc567-152">A.</span></span> <span data-ttu-id="bc567-153">Finestra di lettura</span><span class="sxs-lookup"><span data-stu-id="bc567-153">Reading Window</span></span>                                 | <span data-ttu-id="bc567-154">Contiene le sequenze di tasti della tastiera. in genere cambia dopo ogni pressione di tasto.</span><span class="sxs-lookup"><span data-stu-id="bc567-154">Contains keystrokes from the keyboard; typically changes after each keystroke.</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="bc567-155">lettura di una stringa</span><span class="sxs-lookup"><span data-stu-id="bc567-155">reading string</span></span>                               |
| <span data-ttu-id="bc567-156">B.</span><span class="sxs-lookup"><span data-stu-id="bc567-156">B.</span></span> <span data-ttu-id="bc567-157">Finestra di composizione</span><span class="sxs-lookup"><span data-stu-id="bc567-157">Composition Window</span></span>                             | <span data-ttu-id="bc567-158">Contiene la raccolta di caratteri che l'utente ha composto con l'IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-158">Contains the collection of characters that the user has composed with the IME.</span></span> <span data-ttu-id="bc567-159">Questi caratteri vengono disegnati dall'IME sopra l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc567-159">These characters are drawn by the IME on top of the application.</span></span> <span data-ttu-id="bc567-160">Quando l'utente notifica all'IME che la stringa di composizione è soddisfacente, l'IME invia quindi la stringa di composizione all'applicazione tramite una serie di messaggi WM \_ CHAR.</span><span class="sxs-lookup"><span data-stu-id="bc567-160">When the user notifies the IME that the composition string is satisfactory, the IME then sends the composition string to the application via a series of WM\_CHAR messages.</span></span> | <span data-ttu-id="bc567-161">stringa di composizione</span><span class="sxs-lookup"><span data-stu-id="bc567-161">composition string</span></span>                           |
| <span data-ttu-id="bc567-162">C.</span><span class="sxs-lookup"><span data-stu-id="bc567-162">C.</span></span> <span data-ttu-id="bc567-163">Finestra Candidata</span><span class="sxs-lookup"><span data-stu-id="bc567-163">Candidate Window</span></span>                               | <span data-ttu-id="bc567-164">Quando l'utente ha immesso una pronuncia valida, l'IME visualizza un elenco di caratteri candidati che corrispondono tutti alla pronuncia specificata.</span><span class="sxs-lookup"><span data-stu-id="bc567-164">When the user has entered a valid pronunciation, the IME displays a list of candidate characters that all match the given pronunciation.</span></span> <span data-ttu-id="bc567-165">L'utente seleziona quindi il carattere desiderato dall'elenco e l'IME lo aggiunge alla visualizzazione della finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-165">The user then selects the intended character from this list, and the IME adds this character to the Composition Window display.</span></span>                                                    | <span data-ttu-id="bc567-166">carattere successivo nella stringa di composizione</span><span class="sxs-lookup"><span data-stu-id="bc567-166">the next character in the composition string</span></span> |
| <span data-ttu-id="bc567-167">D.</span><span class="sxs-lookup"><span data-stu-id="bc567-167">D.</span></span> <span data-ttu-id="bc567-168">[Indicatore delle impostazioni locali di](/windows/desktop/Intl/nls-terminology) input</span><span class="sxs-lookup"><span data-stu-id="bc567-168">[Input Locale](/windows/desktop/Intl/nls-terminology) indicator</span></span> | <span data-ttu-id="bc567-169">Mostra la lingua selezionata dall'utente per l'input da tastiera.</span><span class="sxs-lookup"><span data-stu-id="bc567-169">Shows the language the user has selected for keyboard input.</span></span> <span data-ttu-id="bc567-170">Questo indicatore è incorporato nella barra delle applicazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="bc567-170">This indicator is embedded in the Windows taskbar.</span></span> <span data-ttu-id="bc567-171">Per selezionare la lingua di input, aprire opzioni internazionali e della lingua Pannello di controllo quindi fare clic su Dettagli nella scheda Lingue.</span><span class="sxs-lookup"><span data-stu-id="bc567-171">The input language can be selected by opening the Regional and Language Options Control Panel and then clicking Details on the Languages tab.</span></span>                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a><span data-ttu-id="bc567-172">Uso di IME con DXUT</span><span class="sxs-lookup"><span data-stu-id="bc567-172">Using IMEs with DXUT</span></span>

<span data-ttu-id="bc567-173">In DXUT la classe CDXUTIMEEditBox implementa la funzionalità IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-173">In DXUT, the CDXUTIMEEditBox class implements IME functionality.</span></span> <span data-ttu-id="bc567-174">Questa classe è derivata dalla classe CDXUTEditBox, il controllo di modifica di base fornito dal framework.</span><span class="sxs-lookup"><span data-stu-id="bc567-174">This class is derived from the CDXUTEditBox class, the basic edit control provided by the framework.</span></span> <span data-ttu-id="bc567-175">CDXUTIMEEditBox estende il controllo di modifica per supportare gli IME eseguendo l'override dei metodi CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="bc567-175">CDXUTIMEEditBox extends that edit control to support IMEs by overriding the CDXUTIMEEditBox methods.</span></span> <span data-ttu-id="bc567-176">Le classi sono progettate in questo modo per aiutare gli sviluppatori a capire cosa devono prendere dal framework per implementare il supporto IME nei propri controlli di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-176">The classes are designed this way to help developers learn what they need to take from the framework to implement IME support in their own edit controls.</span></span> <span data-ttu-id="bc567-177">Nella parte restante di questo argomento viene illustrato in che modo il framework, in particolare CDXUTIMEEditBox, esegue l'override di un controllo di modifica di base per implementare la funzionalità IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-177">The rest of this topic explains how the framework, and CDXUTIMEEditBox in particular, overrides a basic edit control to implement IME functionality.</span></span>

<span data-ttu-id="bc567-178">La maggior parte delle variabili specifiche di IME in CDXUTIMEEditBox viene dichiarata come statica, perché molti buffer e stati IME sono specifici del processo.</span><span class="sxs-lookup"><span data-stu-id="bc567-178">Most of the IME-specific variables in CDXUTIMEEditBox are declared as static, because many IME buffers and states are specific to the process.</span></span> <span data-ttu-id="bc567-179">Ad esempio, un processo ha un solo buffer per la stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-179">For instance, a process has only one buffer for the composition string.</span></span> <span data-ttu-id="bc567-180">Anche se il processo ha dieci controlli di modifica, condivideranno tutti lo stesso buffer della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-180">Even if the process has ten edit controls, they will all be sharing the same composition string buffer.</span></span> <span data-ttu-id="bc567-181">Il buffer della stringa di composizione per CDXUTIMEEditBox è pertanto statico, impedendo all'applicazione di occupare spazio di memoria non necessario.</span><span class="sxs-lookup"><span data-stu-id="bc567-181">The composition string buffer for CDXUTIMEEditBox is therefore static, preventing the application from taking up unnecessary memory space.</span></span>

<span data-ttu-id="bc567-182">CDXUTIMEEditBox viene implementato nel codice DXUT seguente:</span><span class="sxs-lookup"><span data-stu-id="bc567-182">CDXUTIMEEditBox is implemented in the following DXUT code:</span></span>

<span data-ttu-id="bc567-183">(radice SDK) \\ Esempi \\ \\ \\ DXUTgui.cpp comuni C++</span><span class="sxs-lookup"><span data-stu-id="bc567-183">(SDK root)\\Samples\\C++\\Common\\DXUTgui.cpp</span></span>

## <a name="overriding-the-default-ime-behavior"></a><span data-ttu-id="bc567-184">Override del comportamento IME predefinito</span><span class="sxs-lookup"><span data-stu-id="bc567-184">Overriding the Default IME Behavior</span></span>

<span data-ttu-id="bc567-185">In genere un IME usa procedure standard di Windows per creare una finestra (vedere [Uso di Windows).](/windows/desktop/winmsg/using-windows)</span><span class="sxs-lookup"><span data-stu-id="bc567-185">Normally an IME uses standard Windows procedures to create a window (see [Using Windows](/windows/desktop/winmsg/using-windows)).</span></span> <span data-ttu-id="bc567-186">In circostanze normali, ciò produce risultati soddisfacenti.</span><span class="sxs-lookup"><span data-stu-id="bc567-186">Under normal circumstances, this produces satisfactory results.</span></span> <span data-ttu-id="bc567-187">Tuttavia, quando l'applicazione viene visualizzata in modalità schermo intero, come è comune per i giochi, le finestre standard non funzionano più e potrebbero non essere visualizzate sopra l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc567-187">However, when the application presents in full-screen mode, as is common for games, standard windows no longer work and may not display on top of the application.</span></span> <span data-ttu-id="bc567-188">Per risolvere questo problema, l'applicazione deve disegnare le finestre IME anziché basarsi su Windows per eseguire questa attività.</span><span class="sxs-lookup"><span data-stu-id="bc567-188">To overcome this issue, the application must draw the IME windows itself instead of relying on Windows to perform this task.</span></span>

<span data-ttu-id="bc567-189">Quando il comportamento predefinito di creazione della finestra IME non fornisce ciò che un'applicazione richiede, l'applicazione può eseguire l'override della gestione della finestra IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-189">When the default IME window creation behavior does not provide what an application requires, the application can override the IME window handling.</span></span> <span data-ttu-id="bc567-190">Un'applicazione può ottenere questo risultato elaborando i messaggi correlati all'IME e chiamando l'API [IMM (Input Method Manager).](/windows/desktop/Intl/input-method-manager)</span><span class="sxs-lookup"><span data-stu-id="bc567-190">An application can achieve this by processing IME-related messages and calling the [Input Method Manager](/windows/desktop/Intl/input-method-manager) (IMM) API.</span></span>

<span data-ttu-id="bc567-191">Quando un utente interagisce con un IME per inserire caratteri complessi, invia messaggi all'applicazione per notificare eventi importanti, ad esempio l'avvio di una composizione o la visualizzazione della finestra candidata.</span><span class="sxs-lookup"><span data-stu-id="bc567-191">When a user interacts with an IME to input complex characters, the IMM sends messages to the application to notify it of important events, such as starting a composition or showing the candidate window.</span></span> <span data-ttu-id="bc567-192">Un'applicazione in genere ignora questi messaggi e li passa al gestore di messaggi predefinito, in modo che l'IME li gestirà.</span><span class="sxs-lookup"><span data-stu-id="bc567-192">An application typically ignores these messages and passes them to the default message handler, which causes the IME to handle them.</span></span> <span data-ttu-id="bc567-193">Quando l'applicazione, anziché il gestore predefinito, gestisce i messaggi, controlla esattamente ciò che accade in ogni evento IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-193">When the application, instead of the default handler, handles the messages, it controls exactly what happens at each of the IME events.</span></span> <span data-ttu-id="bc567-194">Spesso il gestore di messaggi recupera il contenuto delle varie finestre IME chiamando l'API IMM.</span><span class="sxs-lookup"><span data-stu-id="bc567-194">Often the message handler retrieves the content of the various IME windows by calling the IMM API.</span></span> <span data-ttu-id="bc567-195">Quando l'applicazione ha queste informazioni, può disegnare correttamente le finestre IME quando deve eseguire il rendering sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="bc567-195">Once the application has this information, it can properly draw the IME windows itself when it needs to render to the display.</span></span>

## <a name="functions"></a><span data-ttu-id="bc567-196">Funzioni</span><span class="sxs-lookup"><span data-stu-id="bc567-196">Functions</span></span>

<span data-ttu-id="bc567-197">Un IME deve ottenere la stringa di lettura, nascondere la finestra di lettura e ottenere l'orientamento della finestra di lettura.</span><span class="sxs-lookup"><span data-stu-id="bc567-197">An IME needs to get the reading string, hide the reading window, and get the orientation of reading window.</span></span> <span data-ttu-id="bc567-198">Questa tabella mostra le funzionalità per ogni versione IME:</span><span class="sxs-lookup"><span data-stu-id="bc567-198">This table shows the functionalities per IME version:</span></span>



|                    | <span data-ttu-id="bc567-199">Recupero della stringa di lettura</span><span class="sxs-lookup"><span data-stu-id="bc567-199">Getting reading string</span></span>                                                | <span data-ttu-id="bc567-200">Nascondere la finestra di lettura</span><span class="sxs-lookup"><span data-stu-id="bc567-200">Hiding reading window</span></span>                       | <span data-ttu-id="bc567-201">Orientamento della finestra di lettura</span><span class="sxs-lookup"><span data-stu-id="bc567-201">Orientation of reading window</span></span>                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bc567-202">**Prima della versione 6.0**</span><span class="sxs-lookup"><span data-stu-id="bc567-202">**Before version 6.0**</span></span> | <span data-ttu-id="bc567-203">A.</span><span class="sxs-lookup"><span data-stu-id="bc567-203">A.</span></span> <span data-ttu-id="bc567-204">Lettura diretta dei dati privati IME di Accesso finestra.</span><span class="sxs-lookup"><span data-stu-id="bc567-204">Reading Window Access IME private data directly.</span></span> <span data-ttu-id="bc567-205">Vedere "4 Struttura"</span><span class="sxs-lookup"><span data-stu-id="bc567-205">See "4 Structure"</span></span> | <span data-ttu-id="bc567-206">Intercettare i messaggi privati IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-206">Trap IME private messages.</span></span> <span data-ttu-id="bc567-207">Vedere "3 messaggi"</span><span class="sxs-lookup"><span data-stu-id="bc567-207">See "3 Messages"</span></span> | <span data-ttu-id="bc567-208">Esaminare le informazioni del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bc567-208">Examine registry information.</span></span> <span data-ttu-id="bc567-209">Vedere "5 Informazioni del Registro di sistema"</span><span class="sxs-lookup"><span data-stu-id="bc567-209">See "5 Registry Information"</span></span> |
| <span data-ttu-id="bc567-210">**Dopo la versione 6.0**</span><span class="sxs-lookup"><span data-stu-id="bc567-210">**After version 6.0**</span></span>  | [<span data-ttu-id="bc567-211">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="bc567-211">GetReadingString</span></span>](#getreadingstring)                                 | [<span data-ttu-id="bc567-212">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="bc567-212">ShowReadingWindow</span></span>](#showreadingwindow)     | [<span data-ttu-id="bc567-213">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="bc567-213">GetReadingString</span></span>](#getreadingstring)                      |



 

## <a name="messages"></a><span data-ttu-id="bc567-214">Messaggi</span><span class="sxs-lookup"><span data-stu-id="bc567-214">Messages</span></span>

<span data-ttu-id="bc567-215">Non è necessario elaborare i messaggi seguenti per un IME più recente che implementa [ShowReadingWindow](#showreadingwindow)().</span><span class="sxs-lookup"><span data-stu-id="bc567-215">The following messages don't have to be processed for newer IME that implements [ShowReadingWindow](#showreadingwindow)().</span></span>

<span data-ttu-id="bc567-216">I messaggi seguenti vengono intercettati dal gestore di messaggi dell'applicazione(ad esempio, non vengono passati a DefWindowProc) per impedire la visualizzazione della finestra di lettura.</span><span class="sxs-lookup"><span data-stu-id="bc567-216">The following messages are trapped by application message handler (i.e. they are not passed to DefWindowProc) to prevent the reading window from showing up.</span></span>

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a><span data-ttu-id="bc567-217">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc567-217">Examples</span></span>

<span data-ttu-id="bc567-218">Gli esempi seguenti illustrano come ottenere informazioni di stringa da IME meno recenti che non hanno GetReadingString().</span><span class="sxs-lookup"><span data-stu-id="bc567-218">The following examples illustrate how to get reading string information from older IME that doesn't have GetReadingString().</span></span> <span data-ttu-id="bc567-219">Il codice genera gli output seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc567-219">The code generates the following outputs:</span></span>



| <span data-ttu-id="bc567-220">Output</span><span class="sxs-lookup"><span data-stu-id="bc567-220">Output</span></span>              | <span data-ttu-id="bc567-221">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc567-221">Description</span></span>                                                                                      |
|--------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc567-222">DWORD dwlen</span><span class="sxs-lookup"><span data-stu-id="bc567-222">DWORD dwlen</span></span>  | <span data-ttu-id="bc567-223">Lunghezza della stringa di lettura.</span><span class="sxs-lookup"><span data-stu-id="bc567-223">Length of the reading string.</span></span>                                                          |
| <span data-ttu-id="bc567-224">DWORD dwerr</span><span class="sxs-lookup"><span data-stu-id="bc567-224">DWORD dwerr</span></span>  | <span data-ttu-id="bc567-225">Indice del carattere di errore.</span><span class="sxs-lookup"><span data-stu-id="bc567-225">Index of the error character.</span></span>                                                                   |
| <span data-ttu-id="bc567-226">LPWSTR wstr</span><span class="sxs-lookup"><span data-stu-id="bc567-226">LPWSTR wstr</span></span>  | <span data-ttu-id="bc567-227">Puntatore alla stringa di lettura.</span><span class="sxs-lookup"><span data-stu-id="bc567-227">Pointer to the reading string.</span></span>                                                         |
| <span data-ttu-id="bc567-228">UNICODE BOOL</span><span class="sxs-lookup"><span data-stu-id="bc567-228">BOOL unicode</span></span> | <span data-ttu-id="bc567-229">Se true, la stringa di lettura è in formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="bc567-229">If true, the reading string is in Unicode format.</span></span> <span data-ttu-id="bc567-230">In caso contrario, è in formato multibyte.</span><span class="sxs-lookup"><span data-stu-id="bc567-230">Otherwise it's in multibyte format.</span></span> |



 

### <a name="cht-ime-version-42-43-and-44"></a><span data-ttu-id="bc567-231">CHT IME versione 4.2, 4.3 e 4.4</span><span class="sxs-lookup"><span data-stu-id="bc567-231">CHT IME version 4.2, 4.3 and 4.4</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a><span data-ttu-id="bc567-232">CHT IME versione 5.0</span><span class="sxs-lookup"><span data-stu-id="bc567-232">CHT IME version 5.0</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a><span data-ttu-id="bc567-233">CHT IME versione 5.1, 5.2 e CHS IME versione 5.3</span><span class="sxs-lookup"><span data-stu-id="bc567-233">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a><span data-ttu-id="bc567-234">CHS IME versione 4.1</span><span class="sxs-lookup"><span data-stu-id="bc567-234">CHS IME version 4.1</span></span>

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a><span data-ttu-id="bc567-235">CHS IME versione 4.2</span><span class="sxs-lookup"><span data-stu-id="bc567-235">CHS IME version 4.2</span></span>

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a><span data-ttu-id="bc567-236">Messaggi IME</span><span class="sxs-lookup"><span data-stu-id="bc567-236">IME Messages</span></span>

<span data-ttu-id="bc567-237">Un'applicazione a schermo intero deve gestire correttamente i messaggi correlati all'IME seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc567-237">A full-screen application must properly handle the following IME-related messages:</span></span>

### <a name="wm_inputlangchange"></a><span data-ttu-id="bc567-238">WM \_ INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="bc567-238">WM\_INPUTLANGCHANGE</span></span>

<span data-ttu-id="bc567-239">IMM invia un messaggio WM INPUTLANGCHANGE alla finestra attiva di un'applicazione dopo che le impostazioni locali di input sono state modificate dall'utente con una combinazione di tasti (in genere ALT+MAIUSC) o con l'indicatore delle impostazioni locali di input sulla barra delle applicazioni o sulla barra della \_ lingua.</span><span class="sxs-lookup"><span data-stu-id="bc567-239">The IMM sends a WM\_INPUTLANGCHANGE message to the active window of an application after the input locale has been changed by the user with a key combination (usually ALT+SHIFT), or with the input locale indicator on the taskbar or language bar.</span></span> <span data-ttu-id="bc567-240">La barra della lingua è un controllo su schermo con cui l'utente può configurare un servizio di testo.</span><span class="sxs-lookup"><span data-stu-id="bc567-240">The language bar is an on-screen control with which the user can configure a text service.</span></span> <span data-ttu-id="bc567-241">Vedere [Come visualizzare la barra della lingua.](/windows/desktop/TSF/how-to-set-up-tsf) La schermata seguente mostra un elenco di selezione della lingua che viene visualizzato quando l'utente fa clic sull'indicatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bc567-241">(See [How to show the language bar](/windows/desktop/TSF/how-to-set-up-tsf).) The following screen shot shows a language selection list that is displayed when the user clicks on the locale indicator.</span></span>

![elenco di selezione della lingua visualizzato quando l'utente fa clic sull'indicatore delle impostazioni locali](images/ime-langselection.png)

<span data-ttu-id="bc567-243">Quando IMM invia un messaggio WM \_ INPUTLANGCHANGE, CDXUTIMEEditBox deve eseguire diverse attività importanti:</span><span class="sxs-lookup"><span data-stu-id="bc567-243">When the IMM sends a WM\_INPUTLANGCHANGE message, CDXUTIMEEditBox must perform several important tasks:</span></span>

1.  <span data-ttu-id="bc567-244">Il metodo GetKeyboardLayout viene chiamato per restituire l'identificatore delle impostazioni locali di input (ID) per il thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc567-244">The GetKeyboardLayout method is called to return the input locale identifier (ID) for the application thread.</span></span> <span data-ttu-id="bc567-245">La classe CDXUTIMEEditBox salva questo ID nella variabile membro statica s \_ hklCurrent per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="bc567-245">The CDXUTIMEEditBox class saves this ID in its static member variable s\_hklCurrent for later use.</span></span> <span data-ttu-id="bc567-246">È importante che l'applicazione sappia le impostazioni locali di input correnti, perché l'IME per ogni lingua ha un comportamento distinto.</span><span class="sxs-lookup"><span data-stu-id="bc567-246">It is important for the application to know the current input locale, because the IME for each language has its own distinct behavior.</span></span> <span data-ttu-id="bc567-247">Lo sviluppatore potrebbe dover fornire codice diverso per impostazioni locali di input diverse.</span><span class="sxs-lookup"><span data-stu-id="bc567-247">The developer may need to provide different code for different input locales.</span></span>
2.  <span data-ttu-id="bc567-248">CDXUTIMEEditBox inizializza una stringa da visualizzare nell'indicatore di lingua della casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-248">CDXUTIMEEditBox initializes a string to display in the edit box language indicator.</span></span> <span data-ttu-id="bc567-249">Questo indicatore può visualizzare la lingua di input attiva quando l'applicazione è in esecuzione in modalità schermo intero e non è visibile né la barra delle applicazioni né la barra della lingua.</span><span class="sxs-lookup"><span data-stu-id="bc567-249">This indicator can display the active input language when the application is running in full-screen mode and neither the taskbar nor language bar is visible.</span></span>
3.  <span data-ttu-id="bc567-250">Il metodo ImmGetConversionStatus viene chiamato per indicare se le impostazioni locali di input sono in modalità di conversione nativa o non nativa.</span><span class="sxs-lookup"><span data-stu-id="bc567-250">The ImmGetConversionStatus method is called to indicate whether the input locale is in native or non-native conversion mode.</span></span> <span data-ttu-id="bc567-251">La modalità di conversione nativa consente all'utente di immettere testo nella lingua scelta.</span><span class="sxs-lookup"><span data-stu-id="bc567-251">Native conversion mode lets the user enter text in the chosen language.</span></span> <span data-ttu-id="bc567-252">La modalità di conversione non nativa fa in modo che la tastiera funzioni come tastiera inglese standard.</span><span class="sxs-lookup"><span data-stu-id="bc567-252">Non-native conversion mode makes the keyboard act as a standard English keyboard.</span></span> <span data-ttu-id="bc567-253">È importante fornire all'utente un segnale visivo sul tipo di modalità di conversione in cui si trova l'IME, in modo che l'utente possa facilmente sapere quali caratteri aspettarsi quando si tocca un tasto.</span><span class="sxs-lookup"><span data-stu-id="bc567-253">It is important to give the user a visual cue as to what type of conversion mode the IME is in, so that the user can easily know what characters to expect when hitting a key.</span></span> <span data-ttu-id="bc567-254">CDXUTIMEEditBox fornisce questo segnale visivo con un colore indicatore della lingua.</span><span class="sxs-lookup"><span data-stu-id="bc567-254">CDXUTIMEEditBox provides this visual cue with a language indicator color.</span></span> <span data-ttu-id="bc567-255">Quando le impostazioni locali di input utilizzano un IME con modalità di conversione nativa, la classe CDXUTIMEEditBox disegna il testo dell'indicatore con il colore definito dal parametro \_ m IndicatorImeColor.</span><span class="sxs-lookup"><span data-stu-id="bc567-255">When the input locale uses an IME with native conversion mode, the CDXUTIMEEditBox class draws the indicator text with the color defined by the m\_IndicatorImeColor parameter.</span></span> <span data-ttu-id="bc567-256">Quando l'IME è in modalità di conversione non nativa o non viene usato alcun IME, la classe disegna il testo dell'indicatore con il colore definito dal parametro \_ m IndicatorEngColor.</span><span class="sxs-lookup"><span data-stu-id="bc567-256">When the IME is in non-native conversion mode, or no IME is used at all, the class draws the indicator text with the color defined by the m\_IndicatorEngColor parameter.</span></span>
4.  <span data-ttu-id="bc567-257">CDXUTIMEEditBox controlla le impostazioni locali di input e imposta la variabile membro statica bInsertOnType su TRUE per il coreano e \_ FALSE per tutte le altre lingue.</span><span class="sxs-lookup"><span data-stu-id="bc567-257">CDXUTIMEEditBox checks the input locale and sets the static member variable s\_bInsertOnType to TRUE for Korean and FALSE for all other languages.</span></span> <span data-ttu-id="bc567-258">Questo flag è obbligatorio a causa dei diversi comportamenti degli IME coreani e di tutti gli altri IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-258">This flag is required because of the different behaviors of Korean IMEs and all other IMEs.</span></span> <span data-ttu-id="bc567-259">Quando si immettono caratteri in lingue diverse dal coreano, il testo immesso dall'utente viene visualizzato nella finestra di composizione e l'utente può modificare liberamente il contenuto della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-259">When entering characters in languages other than Korean, the user-entered text is displayed in the composition window, and the user can freely change the content of the composition string.</span></span> <span data-ttu-id="bc567-260">L'utente preme il tasto INVIO quando viene soddisfatta la stringa di composizione e la stringa di composizione viene inviata all'applicazione come una serie di messaggi WM \_ CHAR.</span><span class="sxs-lookup"><span data-stu-id="bc567-260">The user presses the ENTER key when satisfied with the composition string, and the composition string is sent to the application as a series of WM\_CHAR messages.</span></span> <span data-ttu-id="bc567-261">Negli IME coreani, tuttavia, quando un utente preme un tasto per immettere testo, viene immediatamente inviato un carattere all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc567-261">In Korean IMEs, however, when a user presses a key to enter text, a character is immediately sent to the application.</span></span> <span data-ttu-id="bc567-262">Quando successivamente l'utente preme più tasti per modificare il carattere iniziale, il carattere nella casella di modifica cambia per riflettere l'input aggiuntivo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bc567-262">When the user subsequently presses more keys to modify that initial character, the character in the edit box changes to reflect additional input from the user.</span></span> <span data-ttu-id="bc567-263">Essenzialmente, l'utente sta componendo caratteri nella casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-263">Essentially, the user is composing characters in the edit box.</span></span> <span data-ttu-id="bc567-264">Questi due comportamenti sono sufficientemente diversi che CDXUTIMEEditBox deve codificare in modo specifico per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="bc567-264">These two behaviors are different enough that CDXUTIMEEditBox must code for each of them specifically.</span></span>
5.  <span data-ttu-id="bc567-265">Il metodo membro statico SetupImeApi viene chiamato per recuperare gli indirizzi di due funzioni dal modulo IME: GetReadingString e ShowReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="bc567-265">The static member method SetupImeApi is called to retrieve addresses of two functions from the IME module: GetReadingString and ShowReadingWindow.</span></span> <span data-ttu-id="bc567-266">Se queste funzioni esistono, showReadingWindow viene chiamato per nascondere la finestra di lettura predefinita per questo IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-266">If these functions exist, ShowReadingWindow is called to hide the default reading window for this IME.</span></span> <span data-ttu-id="bc567-267">Poiché l'applicazione esegue il rendering della finestra di lettura stessa, notifica all'IME di disabilitare il disegno della finestra di lettura predefinita in modo che non interferisca con il rendering a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="bc567-267">Because the application renders the reading window itself, it notifies the IME to disable drawing the default reading window so that it will not interfere with full-screen rendering.</span></span>

<span data-ttu-id="bc567-268">L'IMM invia un messaggio WM \_ IME \_ SETCONTEXT quando viene attivata una finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc567-268">The IMM sends a WM\_IME\_SETCONTEXT message when a window of the application is activated.</span></span> <span data-ttu-id="bc567-269">Il parametro lParam di questo messaggio contiene un flag che indica all'IME quali finestre devono essere disegnate e quali no.</span><span class="sxs-lookup"><span data-stu-id="bc567-269">The lParam parameter of this message contains a flag that indicates to the IME which windows should get drawn and which should not.</span></span> <span data-ttu-id="bc567-270">Poiché l'applicazione gestisce tutto il disegno, non è necessario l'IME per disegnare le finestre IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-270">Because the application is handling all of the drawing, it does not need the IME to draw any of the IME windows.</span></span> <span data-ttu-id="bc567-271">Pertanto, il gestore di messaggi dell'applicazione imposta semplicemente lParam su 0 e restituisce .</span><span class="sxs-lookup"><span data-stu-id="bc567-271">Therefore, the application's message handler simply sets lParam to 0 and returns.</span></span>

<span data-ttu-id="bc567-272">Per consentire alle applicazioni di supportare IME, è necessaria un'elaborazione speciale per il messaggio WM \_ IME SETCONTEXT correlato all'IME. \_</span><span class="sxs-lookup"><span data-stu-id="bc567-272">In order for applications to support IME, special processing is needed for the IME-related message WM\_IME\_SETCONTEXT.</span></span> <span data-ttu-id="bc567-273">Poiché Windows in genere invia questo messaggio all'applicazione prima di chiamare il metodo PanoramaInitialize(), Panorama non ha la possibilità di elaborare l'interfaccia utente per visualizzare le finestre dell'elenco candidato.</span><span class="sxs-lookup"><span data-stu-id="bc567-273">Since Windows typically sends this message to the application prior to calling the PanoramaInitialize() method, Panorama doesn't have a chance to process the UI for showing candidate list windows.</span></span>

<span data-ttu-id="bc567-274">Il frammento di codice seguente specifica alle applicazioni Windows di non visualizzare alcuna interfaccia utente associata alla finestra dell'elenco dei candidati, consentendo a Panorama di gestire in modo specifico questa interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bc567-274">The following code snippet specifies to Windows applications not to display any UI associated with the candidate list window, allowing Panorama to specifically handle this UI.</span></span>

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a><span data-ttu-id="bc567-275">AVVIO \_ DI WM \_ IMECOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="bc567-275">WM\_IME\_STARTCOMPOSITION</span></span>

<span data-ttu-id="bc567-276">L'IMM invia un messaggio WM IME STARTCOMPOSITION all'applicazione quando una composizione IME sta per iniziare in seguito a sequenze di tasti da parte \_ \_ dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bc567-276">The IMM sends a WM\_IME\_STARTCOMPOSITION message to the application when an IME composition is about to begin as a result of keystrokes by the user.</span></span> <span data-ttu-id="bc567-277">Se l'IME usa la finestra di composizione, visualizza la stringa di composizione corrente in una finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-277">If the IME uses the composition window, it displays the current composition string in a composition window.</span></span> <span data-ttu-id="bc567-278">CDXUTIMEEditBox gestisce questo messaggio eseguendo due attività:</span><span class="sxs-lookup"><span data-stu-id="bc567-278">CDXUTIMEEditBox handles this message by performing two tasks:</span></span>

1.  <span data-ttu-id="bc567-279">CDXUTIMEEditBox cancella il buffer della stringa di composizione e il buffer degli attributi.</span><span class="sxs-lookup"><span data-stu-id="bc567-279">CDXUTIMEEditBox clears the composition string buffer and attribute buffer.</span></span> <span data-ttu-id="bc567-280">Questi buffer sono membri statici di CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="bc567-280">These buffers are static members of CDXUTIMEEditBox.</span></span>
2.  <span data-ttu-id="bc567-281">CDXUTIMEEditBox imposta la variabile membro \_ statica bHideCaret su TRUE.</span><span class="sxs-lookup"><span data-stu-id="bc567-281">CDXUTIMEEditBox sets the s\_bHideCaret static member variable to TRUE.</span></span> <span data-ttu-id="bc567-282">Questo membro, definito nella classe CDXUTEditBox di base, controlla se il cursore nella casella di modifica deve essere disegnato quando viene eseguito il rendering della casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-282">This member, defined in the base CDXUTEditBox class, controls whether the cursor in the edit box should be drawn when the edit box is rendered.</span></span> <span data-ttu-id="bc567-283">La finestra di composizione funziona in modo simile a una casella di modifica con testo e cursore.</span><span class="sxs-lookup"><span data-stu-id="bc567-283">The composition window functions similarly to an edit box with text and cursor.</span></span> <span data-ttu-id="bc567-284">Per evitare confusione quando la finestra di composizione è visibile, la casella di modifica nasconde il cursore in modo che sia visibile un solo cursore alla volta.</span><span class="sxs-lookup"><span data-stu-id="bc567-284">To avoid confusion when the composition window is visible, the edit box hides its cursor so that only one cursor is visible at a time.</span></span>

### <a name="wm_ime_composition"></a><span data-ttu-id="bc567-285">COMPOSIZIONE \_ IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="bc567-285">WM\_IME\_COMPOSITION</span></span>

<span data-ttu-id="bc567-286">L'IMM invia un messaggio WM IME COMPOSITION all'applicazione quando l'utente immette una sequenza di tasti \_ per modificare la stringa di \_ composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-286">The IMM sends a WM\_IME\_COMPOSITION message to the application when the user enters a keystroke to change the composition string.</span></span> <span data-ttu-id="bc567-287">Il valore di lParam indica il tipo di informazioni che l'applicazione può recuperare da Input Method Manager (IMM).</span><span class="sxs-lookup"><span data-stu-id="bc567-287">The value of lParam indicates what type of information the application can retrieve from the Input Method Manager (IMM).</span></span> <span data-ttu-id="bc567-288">L'applicazione deve recuperare le informazioni disponibili chiamando [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) e quindi salvare le informazioni nel buffer privato in modo che possa eseguire il rendering degli elementi IME in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="bc567-288">The application should retrieve the available information by calling [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) and then should save the information in its private buffer so that it can render the IME elements later.</span></span>

<span data-ttu-id="bc567-289">CDXUTIMEEditBox verifica e recupera i dati della stringa di composizione seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc567-289">CDXUTIMEEditBox checks for and retrieves the following composition string data:</span></span>



| <span data-ttu-id="bc567-290">[**WM \_ Valore \_ del**](/windows/desktop/Intl/wm-ime-composition) flag IME COMPOSITION lParam</span><span class="sxs-lookup"><span data-stu-id="bc567-290">[**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam Flag Value</span></span> | <span data-ttu-id="bc567-291">Dati</span><span class="sxs-lookup"><span data-stu-id="bc567-291">Data</span></span>                           | <span data-ttu-id="bc567-292">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc567-292">Description</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc567-293">GCS \_ COMPATTR</span><span class="sxs-lookup"><span data-stu-id="bc567-293">GCS\_COMPATTR</span></span>                                                         | <span data-ttu-id="bc567-294">Attributo di composizione</span><span class="sxs-lookup"><span data-stu-id="bc567-294">Composition Attribute</span></span>          | <span data-ttu-id="bc567-295">Questo attributo contiene informazioni quali lo stato di ogni carattere nella stringa di composizione, ad esempio convertito o non convertito.</span><span class="sxs-lookup"><span data-stu-id="bc567-295">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="bc567-296">Queste informazioni sono necessarie perché CDXUTIMEEditBox colora i caratteri della stringa di composizione in modo diverso in base ai relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="bc567-296">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span>                                                                                   |
| <span data-ttu-id="bc567-297">GCS \_ COMPCLAUSE</span><span class="sxs-lookup"><span data-stu-id="bc567-297">GCS\_COMPCLAUSE</span></span>                                                       | <span data-ttu-id="bc567-298">Informazioni sulla clausola composition</span><span class="sxs-lookup"><span data-stu-id="bc567-298">Composition Clause Information</span></span> | <span data-ttu-id="bc567-299">Queste informazioni sulla clausola vengono usate quando l'IME giapponese è attivo.</span><span class="sxs-lookup"><span data-stu-id="bc567-299">This clause information is used when the Japanese IME is active.</span></span> <span data-ttu-id="bc567-300">Quando una stringa di composizione giapponese viene convertita, i caratteri possono essere raggruppati come clausola che viene convertita in una singola entità.</span><span class="sxs-lookup"><span data-stu-id="bc567-300">When a Japanese composition string is converted, characters may be grouped together as a clause that gets converted to a single entity.</span></span> <span data-ttu-id="bc567-301">Quando l'utente sposta il cursore, CDXUTIMEEditBox usa queste informazioni per evidenziare l'intera clausola, anziché un solo carattere all'interno della clausola .</span><span class="sxs-lookup"><span data-stu-id="bc567-301">When the user moves the cursor, CDXUTIMEEditBox uses this information to highlight the entire clause, instead of just a single character within the clause.</span></span> |
| <span data-ttu-id="bc567-302">GCS \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="bc567-302">GCS\_COMPSTR</span></span>                                                          | <span data-ttu-id="bc567-303">Stringa di composizione</span><span class="sxs-lookup"><span data-stu-id="bc567-303">Composition String</span></span>             | <span data-ttu-id="bc567-304">Questa stringa è la stringa aggiornata composta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bc567-304">This string is the up-to-date string being composed by the user.</span></span> <span data-ttu-id="bc567-305">Questa è anche la stringa visualizzata nella finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-305">This is also the string displayed in the composition window.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="bc567-306">GCS \_ CURSORPOS</span><span class="sxs-lookup"><span data-stu-id="bc567-306">GCS\_CURSORPOS</span></span>                                                        | <span data-ttu-id="bc567-307">Posizione del cursore di composizione</span><span class="sxs-lookup"><span data-stu-id="bc567-307">Composition Cursor Position</span></span>    | <span data-ttu-id="bc567-308">La finestra di composizione implementa un cursore, simile al cursore in una casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-308">The composition window implements a cursor, similar to the cursor in an edit box.</span></span> <span data-ttu-id="bc567-309">L'applicazione può recuperare la posizione del cursore durante l'elaborazione del messaggio WM \_ IME \_ COMPOSITION per disegnare correttamente il cursore.</span><span class="sxs-lookup"><span data-stu-id="bc567-309">The application can retrieve the cursor position when processing the WM\_IME\_COMPOSITION message in order to draw the cursor properly.</span></span>                                                                                                                                            |
| <span data-ttu-id="bc567-310">GCS \_ RESULTSTR</span><span class="sxs-lookup"><span data-stu-id="bc567-310">GCS\_RESULTSTR</span></span>                                                        | <span data-ttu-id="bc567-311">Stringa di risultato</span><span class="sxs-lookup"><span data-stu-id="bc567-311">Result String</span></span>                  | <span data-ttu-id="bc567-312">La stringa di risultato è disponibile quando l'utente sta per completare il processo di composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-312">The result string is available when the user is about to complete the composition process.</span></span> <span data-ttu-id="bc567-313">Questa stringa deve essere recuperata e i caratteri devono essere inviati alla casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-313">This string should be retrieved and the characters should be sent to the edit box.</span></span>                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a><span data-ttu-id="bc567-314">\_ENDCOMPOSITION DI WM IME \_</span><span class="sxs-lookup"><span data-stu-id="bc567-314">WM\_IME\_ENDCOMPOSITION</span></span>

<span data-ttu-id="bc567-315">L'IMM invia un messaggio ENDCOMPOSITION IME WM all'applicazione al termine dell'operazione di composizione \_ \_ IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-315">The IMM sends a WM\_IME\_ENDCOMPOSITION message to the application when the IME composition operation is ending.</span></span> <span data-ttu-id="bc567-316">Ciò può verificarsi quando l'utente preme INVIO per approvare la stringa di composizione o il tasto ESC per annullare la composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-316">This can occur when the user presses the ENTER key to approve the composition string, or the ESC key to cancel the composition.</span></span> <span data-ttu-id="bc567-317">CDXUTIMEEditBox gestisce questo messaggio impostando il buffer della stringa di composizione su vuoto.</span><span class="sxs-lookup"><span data-stu-id="bc567-317">CDXUTIMEEditBox handles this message by setting the composition string buffer to be empty.</span></span> <span data-ttu-id="bc567-318">Imposta quindi s bHideCaret su FALSE perché la finestra di composizione è chiusa e il cursore nella casella di modifica \_ dovrebbe essere nuovamente visibile.</span><span class="sxs-lookup"><span data-stu-id="bc567-318">It then sets s\_bHideCaret to FALSE because the composition window is closed and the cursor in the edit box should again be visible.</span></span>

<span data-ttu-id="bc567-319">Il gestore di messaggi CDXUTIMEEditBox imposta anche \_ bShowReadingWindow su FALSE.</span><span class="sxs-lookup"><span data-stu-id="bc567-319">The CDXUTIMEEditBox message handler also sets s\_bShowReadingWindow to FALSE.</span></span> <span data-ttu-id="bc567-320">Questo flag controlla se la classe disegna la finestra di lettura quando la casella di modifica esegue il rendering, quindi deve essere impostata su FALSE al termine di una composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-320">This flag controls whether the class draws the reading window when the edit box renders itself, so it must be set to FALSE when a composition ends.</span></span>

### <a name="wm_ime_notify"></a><span data-ttu-id="bc567-321">NOTIFICA \_ IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="bc567-321">WM\_IME\_NOTIFY</span></span>

<span data-ttu-id="bc567-322">L'IMM invia un messaggio WM \_ IME \_ NOTIFY all'applicazione ogni volta che cambia una finestra IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-322">The IMM sends a WM\_IME\_NOTIFY message to the application whenever an IME window changes.</span></span> <span data-ttu-id="bc567-323">Un'applicazione che gestisce il disegno delle finestre IME deve elaborare questo messaggio in modo che sia a conoscenza di qualsiasi aggiornamento al contenuto della finestra.</span><span class="sxs-lookup"><span data-stu-id="bc567-323">An application that handles the drawing of the IME windows should process this message so that it is aware of any update to the content of the window.</span></span> <span data-ttu-id="bc567-324">wParam indica il comando o la modifica in corso.</span><span class="sxs-lookup"><span data-stu-id="bc567-324">The wParam indicates the command or the change that is taking place.</span></span> <span data-ttu-id="bc567-325">CDXUTIMEEditBox gestisce i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc567-325">CDXUTIMEEditBox handles the following commands:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc567-326">Comando IME</span><span class="sxs-lookup"><span data-stu-id="bc567-326">IME Command</span></span></th>
<th><span data-ttu-id="bc567-327">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc567-327">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc567-328"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="bc567-328"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span></span></td>
<td><span data-ttu-id="bc567-329">Questo attributo contiene informazioni quali lo stato di ogni carattere nella stringa di composizione, ad esempio convertito o non convertito.</span><span class="sxs-lookup"><span data-stu-id="bc567-329">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="bc567-330">Queste informazioni sono necessarie perché CDXUTIMEEditBox colora i caratteri della stringa di composizione in modo diverso in base ai relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="bc567-330">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc567-331"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="bc567-331"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> / <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span></span></td>
<td><span data-ttu-id="bc567-332">Inviato all'applicazione quando la finestra candidata sta per essere aperta o aggiornata, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="bc567-332">Sent to the application when the candidate window is about to be opened or updated, respectively.</span></span> <span data-ttu-id="bc567-333">La finestra candidata si apre quando un utente vuole modificare la scelta del testo convertito.</span><span class="sxs-lookup"><span data-stu-id="bc567-333">The candidate window opens when a user wishes to change the converted text choice.</span></span> <span data-ttu-id="bc567-334">La finestra viene aggiornata quando un utente sposta l'indicatore di selezione o modifica la pagina.</span><span class="sxs-lookup"><span data-stu-id="bc567-334">The window is updated when a user moves the selection indicator or changes the page.</span></span> <span data-ttu-id="bc567-335">CDXUTIMEEditBox usa un gestore di messaggi per entrambi questi comandi perché le attività necessarie sono esattamente le stesse:</span><span class="sxs-lookup"><span data-stu-id="bc567-335">CDXUTIMEEditBox uses one message handler for both of these commands because the tasks required are exactly the same:</span></span><br/>
<ol>
<li><span data-ttu-id="bc567-336">CDXUTIMEEditBox imposta il membro bShowWindow della struttura dell'elenco candidato s_CandList su TRUE per indicare che la finestra candidata deve essere disegnata durante il rendering dei frame.</span><span class="sxs-lookup"><span data-stu-id="bc567-336">CDXUTIMEEditBox sets the bShowWindow member of the candidate list structure s_CandList to TRUE to indicate that the candidate window needs to be drawn during frame rendering.</span></span></li>
<li><span data-ttu-id="bc567-337">CDXUTIMEEditBox recupera l'elenco di candidati chiamando <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, prima per ottenere le dimensioni del buffer necessarie e quindi di nuovo per ottenere i dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="bc567-337">CDXUTIMEEditBox retrieves the candidate list by calling <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, first to get the required buffer size, and then again to get the actual data.</span></span></li>
<li><span data-ttu-id="bc567-338">La struttura dell'elenco s_CandList candidato privato viene inizializzata con i dati candidati recuperati.</span><span class="sxs-lookup"><span data-stu-id="bc567-338">The private candidate list structure s_CandList is initialized with the retrieved candidate data.</span></span></li>
<li><span data-ttu-id="bc567-339">Le stringhe candidate vengono archiviate come matrice di stringhe.</span><span class="sxs-lookup"><span data-stu-id="bc567-339">The candidate strings are stored as an array of strings.</span></span></li>
<li><span data-ttu-id="bc567-340">L'indice della voce selezionata, nonché l'indice della pagina, viene salvato.</span><span class="sxs-lookup"><span data-stu-id="bc567-340">The index of the selected entry, as well as the page index, is saved.</span></span></li>
<li><span data-ttu-id="bc567-341">CDXUTIMEEditBox controlla se lo stile della finestra candidata è verticale o orizzontale.</span><span class="sxs-lookup"><span data-stu-id="bc567-341">CDXUTIMEEditBox checks whether the candidate window style is vertical or horizontal.</span></span> <span data-ttu-id="bc567-342">Se lo stile della finestra è orizzontale, è necessario inizializzare un buffer di stringhe aggiuntivo, il membro HoriCand di s_CandList, con tutte le stringhe candidate, con spazi inseriti tra tutte le stringhe adiacenti.</span><span class="sxs-lookup"><span data-stu-id="bc567-342">If the window style is horizontal, an additional string buffer, the HoriCand member of s_CandList, must be initialized with all of the candidate strings, with space characters inserted between all adjacent strings.</span></span> <span data-ttu-id="bc567-343">Quando si esegue il rendering di una finestra candidata verticale, le singole stringhe candidate vengono disegnate una alla volta, con le coordinate y incrementate per ogni stringa.</span><span class="sxs-lookup"><span data-stu-id="bc567-343">When rendering a vertical candidate window, the individual candidate strings are drawn one at a time, with the y coordinates incremented for each string.</span></span> <span data-ttu-id="bc567-344">Tuttavia, questa stringa HoriCand deve essere usata durante il rendering di una finestra candidata orizzontale, perché lo spazio è il modo migliore per separare due stringhe adiacenti nella stessa riga.</span><span class="sxs-lookup"><span data-stu-id="bc567-344">However, this HoriCand string should be used when rendering a horizontal candidate window, because the space character is the best way to separate two adjacent strings on the same line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc567-345"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="bc567-345"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span></span></td>
<td><span data-ttu-id="bc567-346">Inviato all'applicazione quando una finestra candidata sta per essere chiusa.</span><span class="sxs-lookup"><span data-stu-id="bc567-346">Sent to the application when a candidate window is about to close.</span></span> <span data-ttu-id="bc567-347">Ciò si verifica quando un utente ha effettuato una selezione dall'elenco dei candidati.</span><span class="sxs-lookup"><span data-stu-id="bc567-347">This happens when a user has made a selection from the candidate list.</span></span> <span data-ttu-id="bc567-348">CDXUTIMEEditBox gestisce questo comando impostando il flag visibile della finestra candidata su FALSE e quindi cancellando il buffer della stringa candidata.</span><span class="sxs-lookup"><span data-stu-id="bc567-348">CDXUTIMEEditBox handles this command by setting the visible flag of the candidate window to FALSE and then clearing the candidate string buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc567-349">IMN_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="bc567-349">IMN_PRIVATE</span></span></td>
<td><span data-ttu-id="bc567-350">Inviato all'applicazione quando l'IME ha aggiornato la stringa di lettura in seguito alla digitazione o alla rimozione di caratteri da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bc567-350">Sent to the application when the IME has updated its reading string as a result of the user typing or removing characters.</span></span> <span data-ttu-id="bc567-351">L'applicazione deve recuperare la stringa di lettura e salvarla per il rendering.</span><span class="sxs-lookup"><span data-stu-id="bc567-351">The application should retrieve the reading string and save it for rendering.</span></span> <span data-ttu-id="bc567-352">CDXUTIMEEditBox dispone di due metodi per recuperare la stringa di lettura, in base al supporto della lettura delle stringhe nell'IME:</span><span class="sxs-lookup"><span data-stu-id="bc567-352">CDXUTIMEEditBox has two methods to retrieve the reading string, based upon how reading strings are supported in the IME:</span></span> <br/>
<ul>
<li><span data-ttu-id="bc567-353">Se l'IME supporta la funzione GetReadingString, viene chiamato GetReadingString per recuperare la stringa di lettura.</span><span class="sxs-lookup"><span data-stu-id="bc567-353">If the IME supports the GetReadingString function, GetReadingString is called to retrieve the reading string.</span></span></li>
<li><span data-ttu-id="bc567-354">Se l'IME non implementa GetReadingString, CDXUTIMEEditBox recupera la stringa di lettura dal contenuto del contesto di input.</span><span class="sxs-lookup"><span data-stu-id="bc567-354">If the IME does not implement GetReadingString, CDXUTIMEEditBox retrieves the reading string from the input context content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a><span data-ttu-id="bc567-355">Rendering</span><span class="sxs-lookup"><span data-stu-id="bc567-355">Rendering</span></span>

<span data-ttu-id="bc567-356">Il rendering degli elementi IME e delle finestre è semplice.</span><span class="sxs-lookup"><span data-stu-id="bc567-356">Rendering of the IME elements and windows is straightforward.</span></span> <span data-ttu-id="bc567-357">CDXUTIMEEditBox consente alla classe di base di eseguire il rendering per primo perché le finestre IME devono essere visualizzate sopra il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-357">CDXUTIMEEditBox lets the base class render first because IME windows should appear on top of the edit control.</span></span> <span data-ttu-id="bc567-358">Dopo il rendering della casella di modifica di base, CDXUTIMEEditBox controlla il flag di visibilità di ogni finestra IME (indicatore, composizione, candidato e finestra di lettura) e disegna la finestra se deve essere visibile.</span><span class="sxs-lookup"><span data-stu-id="bc567-358">After the base edit box is rendered, CDXUTIMEEditBox checks the visibility flag of each IME window (indicator, composition, candidate, and reading window) and draws the window if it should be visible.</span></span> <span data-ttu-id="bc567-359">Per le descrizioni dei diversi tipi di finestra IME, vedere Comportamento IME predefinito.</span><span class="sxs-lookup"><span data-stu-id="bc567-359">See Default IME Behavior for descriptions of the different IME window types.</span></span>

### <a name="input-locale-indicator"></a><span data-ttu-id="bc567-360">Indicatore delle impostazioni locali di input</span><span class="sxs-lookup"><span data-stu-id="bc567-360">Input Locale Indicator</span></span>

<span data-ttu-id="bc567-361">Il rendering dell'indicatore delle impostazioni locali di input viene eseguito prima di qualsiasi altra finestra IME perché è un elemento che viene sempre visualizzato.</span><span class="sxs-lookup"><span data-stu-id="bc567-361">The input locale indicator is rendered before any other IME windows because it is an element that is always displayed.</span></span> <span data-ttu-id="bc567-362">Dovrebbe quindi essere visualizzata sotto altre finestre IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-362">It should therefore appear below other IME windows.</span></span> <span data-ttu-id="bc567-363">CDXUTIMEEditBox esegue il rendering dell'indicatore chiamando il metodo RenderIndicator, in cui il colore del carattere dell'indicatore viene determinato esaminando la variabile statica S ImeState, che riflette la modalità di \_ conversione IME corrente.</span><span class="sxs-lookup"><span data-stu-id="bc567-363">CDXUTIMEEditBox renders the indicator by calling the RenderIndicator method, in which the indicator font color is determined by examining the s\_ImeState static variable, which reflects the current IME conversion mode.</span></span> <span data-ttu-id="bc567-364">Quando l'IME è abilitato e la conversione nativa è attiva, il metodo usa m \_ IndicatorImeColor come colore dell'indicatore.</span><span class="sxs-lookup"><span data-stu-id="bc567-364">When the IME is enabled and native conversion is active, the method uses m\_IndicatorImeColor as the indicator color.</span></span> <span data-ttu-id="bc567-365">Se l'IME è disabilitato o è in modalità di conversione non nativa, m \_ IndicatorImeColor viene usato per disegnare il testo dell'indicatore.</span><span class="sxs-lookup"><span data-stu-id="bc567-365">If the IME is disabled or is in non-native conversion mode, m\_IndicatorImeColor is used to draw the indicator text.</span></span> <span data-ttu-id="bc567-366">Per impostazione predefinita, la finestra dell'indicatore viene disegnata a destra della casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-366">By default, the indicator window itself is drawn to the right of the edit box.</span></span> <span data-ttu-id="bc567-367">Le applicazioni possono modificare questo comportamento eseguendo l'override del metodo RenderIndicator.</span><span class="sxs-lookup"><span data-stu-id="bc567-367">Applications can change this behavior by overriding the RenderIndicator method.</span></span>

<span data-ttu-id="bc567-368">La figura seguente illustra i diversi aspetti di un indicatore delle impostazioni locali di input per l'inglese, il giapponese in modalità di conversione alfanumerica e il giapponese in modalità di conversione nativa:</span><span class="sxs-lookup"><span data-stu-id="bc567-368">The following figure shows the different appearances of an input locale indicator for English, Japanese in alphanumeric conversion mode, and Japanese in native conversion mode:</span></span>

![diversi aspetti di un indicatore delle impostazioni locali di input per l'inglese e il giapponese](images/ime-indicator.png)

### <a name="composition-window"></a><span data-ttu-id="bc567-370">Finestra composizione</span><span class="sxs-lookup"><span data-stu-id="bc567-370">Composition Window</span></span>

<span data-ttu-id="bc567-371">Il disegno della finestra di composizione viene gestito nel metodo RenderComposition di CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="bc567-371">The drawing of the composition window is handled in the RenderComposition method of CDXUTIMEEditBox.</span></span> <span data-ttu-id="bc567-372">La finestra di composizione è mobile sopra la casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="bc567-372">The composition window floats above the edit box.</span></span> <span data-ttu-id="bc567-373">Deve essere disegnata in corrispondenza della posizione del cursore del controllo di modifica sottostante.</span><span class="sxs-lookup"><span data-stu-id="bc567-373">It should be drawn at the cursor position of the underlying edit control.</span></span> <span data-ttu-id="bc567-374">CDXUTIMEEditBox gestisce il rendering come segue:</span><span class="sxs-lookup"><span data-stu-id="bc567-374">CDXUTIMEEditBox handles the rendering as follows:</span></span>

1.  <span data-ttu-id="bc567-375">L'intera stringa di composizione viene disegnata usando i colori predefiniti della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="bc567-375">The entire composition string is drawn using the default composition string colors.</span></span>
2.  <span data-ttu-id="bc567-376">I caratteri con determinati attributi speciali devono essere disegnati in colori diversi, quindi CDXUTIMEEditBox esamina i caratteri della stringa di composizione e controlla l'attributo stringa.</span><span class="sxs-lookup"><span data-stu-id="bc567-376">Characters with certain special attributes should be drawn in different colors, so CDXUTIMEEditBox reviews the characters of the composition string and inspects the string attribute.</span></span> <span data-ttu-id="bc567-377">Se l'attributo chiama colori diversi, il carattere viene disegnato di nuovo con i colori appropriati.</span><span class="sxs-lookup"><span data-stu-id="bc567-377">If the attribute calls for different colors, the character is drawn again with the appropriate colors.</span></span>
3.  <span data-ttu-id="bc567-378">Il cursore della finestra di composizione viene disegnato per completare il rendering.</span><span class="sxs-lookup"><span data-stu-id="bc567-378">The cursor of the composition window is drawn to complete the rendering.</span></span>

<span data-ttu-id="bc567-379">Il cursore dovrebbe lampeggiare per gli IME coreani, ma non per altri IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-379">The cursor should blink for Korean IMEs, but it should not for other IMEs.</span></span> <span data-ttu-id="bc567-380">RenderComposition determina se il cursore deve essere visibile in base ai valori del timer quando viene usato l'IME coreano.</span><span class="sxs-lookup"><span data-stu-id="bc567-380">RenderComposition determines whether the cursor should be visible based upon timer values when the Korean IME is used.</span></span>

### <a name="reading-and-candidate-windows"></a><span data-ttu-id="bc567-381">Lettura e finestre candidate</span><span class="sxs-lookup"><span data-stu-id="bc567-381">Reading and Candidate Windows</span></span>

<span data-ttu-id="bc567-382">Il rendering delle finestre di lettura e candidate viene eseguito dallo stesso metodo CDXUTIMEEditBox, RenderCandidateReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="bc567-382">The reading and candidate windows are rendered by the same CDXUTIMEEditBox method, RenderCandidateReadingWindow.</span></span> <span data-ttu-id="bc567-383">Entrambe le finestre contengono una matrice di stringhe per il layout verticale o una singola stringa nel caso del layout orizzontale.</span><span class="sxs-lookup"><span data-stu-id="bc567-383">Both windows contain an array of strings for vertical layout, or a single string in the case of horizontal layout.</span></span> <span data-ttu-id="bc567-384">La maggior parte del codice in RenderCandidateReadingWindow viene usata per posizionare la finestra in modo che nessuna parte della finestra sia esterna alla finestra dell'applicazione e venga ritagliata.</span><span class="sxs-lookup"><span data-stu-id="bc567-384">The bulk of the code in RenderCandidateReadingWindow is used to position the window so that no part of the window falls outside the application window and gets clipped.</span></span>

## <a name="limitations"></a><span data-ttu-id="bc567-385">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="bc567-385">Limitations</span></span>

<span data-ttu-id="bc567-386">Gli IME contengono talvolta funzionalità avanzate per migliorare la facilità di immissione del testo.</span><span class="sxs-lookup"><span data-stu-id="bc567-386">IMEs sometimes contain advanced features to improve the ease of inputting text.</span></span> <span data-ttu-id="bc567-387">Alcune delle funzionalità disponibili negli IME più recenti sono illustrate nelle figure seguenti.</span><span class="sxs-lookup"><span data-stu-id="bc567-387">Some of the features found in newer IMEs are shown in the following figures.</span></span> <span data-ttu-id="bc567-388">Queste funzionalità avanzate non sono presenti in DXUT.</span><span class="sxs-lookup"><span data-stu-id="bc567-388">These advanced features are not present in DXUT.</span></span> <span data-ttu-id="bc567-389">L'implementazione del supporto per queste funzionalità avanzate può essere complessa perché non è definita alcuna interfaccia per ottenere le informazioni necessarie dagli IME.</span><span class="sxs-lookup"><span data-stu-id="bc567-389">Implementing support for these advanced features can be challenging because there is no interface defined to obtain the necessary information from the IMEs.</span></span>

<span data-ttu-id="bc567-390">IME cinese tradizionale avanzato con elenco di candidati espanso:</span><span class="sxs-lookup"><span data-stu-id="bc567-390">Advanced Traditional Chinese IME with expanded candidate list:</span></span>

![ime cinese tradizionale avanzato con elenco di candidati espanso](images/ime-advanced1.png)

<span data-ttu-id="bc567-392">IME giapponese avanzato con alcune voci candidate che contengono testo aggiuntivo per descriverne il significato:</span><span class="sxs-lookup"><span data-stu-id="bc567-392">Advanced Japanese IME with some candidate entries that contain additional text to describe their meanings:</span></span>

![ime giapponese avanzato con alcune voci candidate che contengono testo aggiuntivo per descriverne i significati](images/ime-advanced2.png)

<span data-ttu-id="bc567-394">IME coreano avanzato che include un sistema di riconoscimento della grafia:</span><span class="sxs-lookup"><span data-stu-id="bc567-394">Advanced Korean IME that includes a handwriting recognition system:</span></span>

![ime coreano avanzato che include un sistema di riconoscimento della grafia](images/ime-advanced3.png)

## <a name="registry-information"></a><span data-ttu-id="bc567-396">Informazioni del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="bc567-396">Registry Information</span></span>

<span data-ttu-id="bc567-397">Le informazioni del Registro di sistema seguenti vengono controllate per determinare l'orientamento della finestra di lettura, quando l'IME corrente è CHT New Phonetic meno recente che non implementa GetReadingString().</span><span class="sxs-lookup"><span data-stu-id="bc567-397">The following registry information is checked to determine the orientation of the reading window, when the current IME is older CHT New Phonetic that doesn't implement GetReadingString().</span></span>



| <span data-ttu-id="bc567-398">Chiave</span><span class="sxs-lookup"><span data-stu-id="bc567-398">Key</span></span>                                                           | <span data-ttu-id="bc567-399">Valore</span><span class="sxs-lookup"><span data-stu-id="bc567-399">Value</span></span>            |
|---------------------------------------------------------------|------------------|
| <span data-ttu-id="bc567-400">HKCU \\ software \\ microsoft \\ windows \\ currentversion \\ IME \_ Name</span><span class="sxs-lookup"><span data-stu-id="bc567-400">HKCU\\software\\microsoft\\windows\\currentversion\\IME\_Name</span></span> | <span data-ttu-id="bc567-401">mapping della tastiera</span><span class="sxs-lookup"><span data-stu-id="bc567-401">keyboard mapping</span></span> |



 

<span data-ttu-id="bc567-402">Dove: Nome IME è MSTCIPH se la versione del file IME è 5.1 o successiva; in caso contrario, il nome \_ IME \_ è TINTLGNT.</span><span class="sxs-lookup"><span data-stu-id="bc567-402">Where: IME\_Name is MSTCIPH if the IME file version is 5.1 or later; otherwise IME\_Name is TINTLGNT.</span></span>

<span data-ttu-id="bc567-403">L'orientamento della finestra di lettura è orizzontale se:</span><span class="sxs-lookup"><span data-stu-id="bc567-403">The orientation of reading window is horizontal if either:</span></span>

-   <span data-ttu-id="bc567-404">L'IME è versione 5.0 e il valore di mapping della tastiera 0x22 o 0x23</span><span class="sxs-lookup"><span data-stu-id="bc567-404">The IME is version 5.0 and keyboard mapping value is 0x22 or 0x23</span></span>
-   <span data-ttu-id="bc567-405">L'IME è versione 5.1 o versione 5.2 e il valore di mapping della tastiera è 0x22, 0x23 o 0x24.</span><span class="sxs-lookup"><span data-stu-id="bc567-405">The IME is version 5.1 or version 5.2 and keyboard mapping value is 0x22, 0x23 or 0x24.</span></span>

<span data-ttu-id="bc567-406">Se nessuna delle due condizioni viene soddisfatta, la finestra di lettura è verticale.</span><span class="sxs-lookup"><span data-stu-id="bc567-406">If neither condition is met, the reading window is vertical.</span></span>

## <a name="appendix-a-cht-versions-per-operating-system"></a><span data-ttu-id="bc567-407">Appendice A: Versioni CHT per sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bc567-407">Appendix A: CHT Versions per Operating System</span></span>



| <span data-ttu-id="bc567-408">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bc567-408">Operating System</span></span>           | <span data-ttu-id="bc567-409">Versione IME di CHT</span><span class="sxs-lookup"><span data-stu-id="bc567-409">CHT IME Version</span></span> |
|----------------------------|-----------------|
| <span data-ttu-id="bc567-410">Windows 98</span><span class="sxs-lookup"><span data-stu-id="bc567-410">Windows 98</span></span>                 | <span data-ttu-id="bc567-411">4.2</span><span class="sxs-lookup"><span data-stu-id="bc567-411">4.2</span></span>             |
| <span data-ttu-id="bc567-412">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bc567-412">Windows 2000</span></span>               | <span data-ttu-id="bc567-413">4.3</span><span class="sxs-lookup"><span data-stu-id="bc567-413">4.3</span></span>             |
| <span data-ttu-id="bc567-414">unknown</span><span class="sxs-lookup"><span data-stu-id="bc567-414">unknown</span></span>                    | <span data-ttu-id="bc567-415">4.4</span><span class="sxs-lookup"><span data-stu-id="bc567-415">4.4</span></span>             |
| <span data-ttu-id="bc567-416">Windows ME</span><span class="sxs-lookup"><span data-stu-id="bc567-416">Windows ME</span></span>                 | <span data-ttu-id="bc567-417">5.0</span><span class="sxs-lookup"><span data-stu-id="bc567-417">5.0</span></span>             |
| <span data-ttu-id="bc567-418">Office XP</span><span class="sxs-lookup"><span data-stu-id="bc567-418">Office XP</span></span>                  | <span data-ttu-id="bc567-419">5,1</span><span class="sxs-lookup"><span data-stu-id="bc567-419">5.1</span></span>             |
| <span data-ttu-id="bc567-420">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc567-420">Windows XP</span></span>                 | <span data-ttu-id="bc567-421">5,2</span><span class="sxs-lookup"><span data-stu-id="bc567-421">5.2</span></span>             |
| <span data-ttu-id="bc567-422">Download web autonomo</span><span class="sxs-lookup"><span data-stu-id="bc567-422">Standalone web downloadble</span></span> | <span data-ttu-id="bc567-423">6.0</span><span class="sxs-lookup"><span data-stu-id="bc567-423">6.0</span></span>             |



 

## <a name="further-information"></a><span data-ttu-id="bc567-424">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="bc567-424">Further Information</span></span>

<span data-ttu-id="bc567-425">Per altre informazioni, vedere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="bc567-425">For additional information, see the following:</span></span>

-   [<span data-ttu-id="bc567-426">Installazione e uso di editor di metodi di input</span><span class="sxs-lookup"><span data-stu-id="bc567-426">Installing and Using Input Method Editors</span></span>](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [<span data-ttu-id="bc567-427">Visualizzazione di testo internazionale</span><span class="sxs-lookup"><span data-stu-id="bc567-427">International Text Display</span></span>](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [<span data-ttu-id="bc567-428">Consorzio Unicode</span><span class="sxs-lookup"><span data-stu-id="bc567-428">The Unicode Consortium</span></span>](https://www.unicode.org/)
-   <span data-ttu-id="bc567-429">Sviluppo di software internazionale.</span><span class="sxs-lookup"><span data-stu-id="bc567-429">Developing International Software.</span></span> <span data-ttu-id="bc567-430">Dr. International.</span><span class="sxs-lookup"><span data-stu-id="bc567-430">Dr. International.</span></span> <span data-ttu-id="bc567-431">2° ed.</span><span class="sxs-lookup"><span data-stu-id="bc567-431">2nd ed.</span></span> <span data-ttu-id="bc567-432">Redmond, WA: Microsoft Press, 2003.</span><span class="sxs-lookup"><span data-stu-id="bc567-432">Redmond, WA: Microsoft Press, 2003.</span></span>

## <a name="getreadingstring"></a><span data-ttu-id="bc567-433">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="bc567-433">GetReadingString</span></span>

<span data-ttu-id="bc567-434">Ottiene la lettura delle informazioni sulla stringa.</span><span class="sxs-lookup"><span data-stu-id="bc567-434">Gets reading string information.</span></span>

<span data-ttu-id="bc567-435">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="bc567-435">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="bc567-436"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="bc567-436"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="bc567-437">\[nel \] contesto di input.</span><span class="sxs-lookup"><span data-stu-id="bc567-437">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="bc567-438"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span><span class="sxs-lookup"><span data-stu-id="bc567-438"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span></span>
</dt> <dd>

<span data-ttu-id="bc567-439">\[in \] Lunghezza di lpwReadingBuf, in WCHAR.</span><span class="sxs-lookup"><span data-stu-id="bc567-439">\[in\] Length of lpwReadingBuf, in WCHAR.</span></span> <span data-ttu-id="bc567-440">Se è zero, significa la lunghezza del buffer di lettura delle query.</span><span class="sxs-lookup"><span data-stu-id="bc567-440">If it is zero, it means query reading buffer length.</span></span>

</dd> <dt>

<span data-ttu-id="bc567-441"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span><span class="sxs-lookup"><span data-stu-id="bc567-441"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span></span> 
</dt> <dd>

<span data-ttu-id="bc567-442">\[out \] Restituisce la stringa di lettura (non l'estremità zero).</span><span class="sxs-lookup"><span data-stu-id="bc567-442">\[out\] Return reading string (not zero end).</span></span>

</dd> <dt>

<span data-ttu-id="bc567-443"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span><span class="sxs-lookup"><span data-stu-id="bc567-443"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="bc567-444">\[out \] Restituisce l'indice del carattere di errore nella stringa di lettura, se presente.</span><span class="sxs-lookup"><span data-stu-id="bc567-444">\[out\] Return index of error character in the reading string if there is.</span></span>

</dd> <dt>

<span data-ttu-id="bc567-445"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span><span class="sxs-lookup"><span data-stu-id="bc567-445"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span></span> 
</dt> <dd>

<span data-ttu-id="bc567-446">\[out \] Se è TRUE, la lettura dell'interfaccia utente è verticale.</span><span class="sxs-lookup"><span data-stu-id="bc567-446">\[out\] If it is TRUE, reading UI is vertical.</span></span> <span data-ttu-id="bc567-447">In caso contrario, puMaxReadingLen orizzontale.</span><span class="sxs-lookup"><span data-stu-id="bc567-447">Otherwise, horizontal puMaxReadingLen.</span></span>

</dd> <dt>

<span data-ttu-id="bc567-448"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span><span class="sxs-lookup"><span data-stu-id="bc567-448"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span></span> 
</dt> <dd>

<span data-ttu-id="bc567-449">\[out \] Lunghezza dell'interfaccia utente di lettura.</span><span class="sxs-lookup"><span data-stu-id="bc567-449">\[out\] The reading UI length.</span></span> <span data-ttu-id="bc567-450">La lunghezza massima di lettura non è fissa. dipende non solo dal layout di tastiera, ma anche dalla modalità di input (ad esempio, codice interno, input surrogato).</span><span class="sxs-lookup"><span data-stu-id="bc567-450">The max reading length is not fixed; it depends not only on keyboard layout, but also on input mode (for example, internal code, surrogate input).</span></span>

</dd> </dl>

<span data-ttu-id="bc567-451">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="bc567-451">**Return Values**</span></span>

<span data-ttu-id="bc567-452">Lunghezza della stringa di lettura.</span><span class="sxs-lookup"><span data-stu-id="bc567-452">The reading string length.</span></span>

<span data-ttu-id="bc567-453">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="bc567-453">**Remarks**</span></span>

<span data-ttu-id="bc567-454">Se il valore restituito è maggiore del valore di uReadingBufLen, tutti i parametri di output non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="bc567-454">If the return value is greater than the value of uReadingBufLen, then all output parameters are undefined.</span></span>

<span data-ttu-id="bc567-455">Questa funzione viene implementata in CHT IME 6.0 o versione successiva e può essere acquisita da GetProcAddress in un handle di modulo IME. L'handle del modulo IME può essere acquisito da ImmGetIMEFileName e LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="bc567-455">This function is implemented in CHT IME 6.0 or later, and can be acquired by GetProcAddress on an IME module handle; the IME module handle can be acquired by ImmGetIMEFileName and LoadLibrary.</span></span>

<span data-ttu-id="bc567-456">**Requisiti**</span><span class="sxs-lookup"><span data-stu-id="bc567-456">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="bc567-457"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="bc567-457"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="bc567-458">Dichiarato in Imm.h.</span><span class="sxs-lookup"><span data-stu-id="bc567-458">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="bc567-459"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Importa libreria**</span><span class="sxs-lookup"><span data-stu-id="bc567-459"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="bc567-460">Usare Imm.lib.</span><span class="sxs-lookup"><span data-stu-id="bc567-460">Use Imm.lib.</span></span>

</dd> </dl>

## <a name="showreadingwindow"></a><span data-ttu-id="bc567-461">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="bc567-461">ShowReadingWindow</span></span>

<span data-ttu-id="bc567-462">Mostra (o nascondi) la finestra di lettura.</span><span class="sxs-lookup"><span data-stu-id="bc567-462">Show (or hide) the reading window.</span></span>

<span data-ttu-id="bc567-463">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="bc567-463">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="bc567-464"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="bc567-464"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="bc567-465">\[nel \] contesto di input.</span><span class="sxs-lookup"><span data-stu-id="bc567-465">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="bc567-466"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*Bshow*</span><span class="sxs-lookup"><span data-stu-id="bc567-466"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span></span> 
</dt> <dd>

<span data-ttu-id="bc567-467">\[in \] Imposta su TRUE per visualizzare la finestra di lettura (o FALSE per nasconderla).</span><span class="sxs-lookup"><span data-stu-id="bc567-467">\[in\] Set to TRUE to show the reading window (or FALSE to hide it).</span></span>

</dd> </dl>

<span data-ttu-id="bc567-468">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="bc567-468">**Return Values**</span></span>

<span data-ttu-id="bc567-469">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="bc567-469">**Remarks**</span></span>

<span data-ttu-id="bc567-470">Restituisce TRUE se l'operazione ha esito positivo o FALSE in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc567-470">Return TRUE if successful or FALSE if otherwise.</span></span>

<span data-ttu-id="bc567-471">**Requisiti**</span><span class="sxs-lookup"><span data-stu-id="bc567-471">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="bc567-472"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="bc567-472"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="bc567-473">Dichiarato in Imm.h.</span><span class="sxs-lookup"><span data-stu-id="bc567-473">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="bc567-474"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Importa libreria**</span><span class="sxs-lookup"><span data-stu-id="bc567-474"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="bc567-475">Usare Imm.lib.</span><span class="sxs-lookup"><span data-stu-id="bc567-475">Use Imm.lib.</span></span>

</dd> </dl>