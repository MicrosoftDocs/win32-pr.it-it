---
title: Uso di un editor del metodo di input in un gioco
description: In questo articolo viene illustrato come implementare un controllo di base di modifica IME in un'applicazione Microsoft DirectX a schermo intero.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1519f07a4e105ae822bd13fd7acd8b29e5ad8a0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "103969282"
---
# <a name="using-an-input-method-editor-in-a-game"></a><span data-ttu-id="09310-103">Uso di un editor del metodo di input in un gioco</span><span class="sxs-lookup"><span data-stu-id="09310-103">Using an Input Method Editor in a Game</span></span>

> [!Note]  
> <span data-ttu-id="09310-104">Questo articolo descrive in dettaglio l'uso dell'IME (Input Method Editor) di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="09310-104">This article details working with the Windows XP Input Method Editor (IME).</span></span> <span data-ttu-id="09310-105">Sono state apportate modifiche all'IME per Windows Vista che non sono completamente descritte in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="09310-105">Changes were made to the IME for Windows Vista that are not fully detailed in this article.</span></span> <span data-ttu-id="09310-106">Per ulteriori informazioni sulle modifiche apportate all'IME per Windows Vista, vedere [Input Method Editor (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows vista: una Ever-Expanding visualizzazione dell'internazionalizzazione](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) nel portale Microsoft per lo sviluppo e l'elaborazione globale.</span><span class="sxs-lookup"><span data-stu-id="09310-106">For more info about changes to the IME for Windows Vista, see [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista - An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) on the Microsoft Global Development and Computing Portal.</span></span>

 

<span data-ttu-id="09310-107">Un Input Method Editor (IME) è un programma che consente una voce di testo semplice utilizzando una tastiera standard per le lingue asiatiche orientali, come il cinese, il giapponese, il coreano e altri linguaggi con caratteri complessi.</span><span class="sxs-lookup"><span data-stu-id="09310-107">An input method editor (IME) is a program that allows easy text entry using a standard keyboard for East Asian languages such as Chinese, Japanese, Korean, and other languages with complex characters.</span></span> <span data-ttu-id="09310-108">Con gli IME, ad esempio, un utente può digitare caratteri complessi in un elaboratore di testo o un giocatore di un gioco multiplayer online massive può chattare con amici in caratteri complessi.</span><span class="sxs-lookup"><span data-stu-id="09310-108">For example, with IMEs a user can type complex characters in a word processor, or a player of a massive multiplayer online game can chat with friends in complex characters.</span></span>

<span data-ttu-id="09310-109">In questo articolo viene illustrato come implementare un controllo di base di modifica IME in un'applicazione Microsoft DirectX a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="09310-109">This article explains how you can implement a basic IME edit control in a full-screen Microsoft DirectX application.</span></span> <span data-ttu-id="09310-110">Le applicazioni che sfruttano i vantaggi di DXUT ottengono automaticamente la funzionalità IME.</span><span class="sxs-lookup"><span data-stu-id="09310-110">Applications that take advantage of DXUT automatically get IME functionality.</span></span> <span data-ttu-id="09310-111">Per le applicazioni che non usano il Framework, in questo articolo viene descritto come aggiungere il supporto IME a un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-111">For applications that do not make use of the framework, this article describes how to add IME support to an edit control.</span></span>

<span data-ttu-id="09310-112">Contenuto:</span><span class="sxs-lookup"><span data-stu-id="09310-112">Contents:</span></span>

-   [<span data-ttu-id="09310-113">Comportamento IME predefinito</span><span class="sxs-lookup"><span data-stu-id="09310-113">Default IME Behavior</span></span>](#default-ime-behavior)
-   [<span data-ttu-id="09310-114">Uso di IME con DXUT</span><span class="sxs-lookup"><span data-stu-id="09310-114">Using IMEs with DXUT</span></span>](#using-imes-with-dxut)
-   [<span data-ttu-id="09310-115">Override del comportamento predefinito di IME</span><span class="sxs-lookup"><span data-stu-id="09310-115">Overriding the Default IME Behavior</span></span>](#overriding-the-default-ime-behavior)
-   [<span data-ttu-id="09310-116">Funzioni</span><span class="sxs-lookup"><span data-stu-id="09310-116">Functions</span></span>](#functions)
-   [<span data-ttu-id="09310-117">Messaggi</span><span class="sxs-lookup"><span data-stu-id="09310-117">Messages</span></span>](#ime-messages)
-   [<span data-ttu-id="09310-118">esempi</span><span class="sxs-lookup"><span data-stu-id="09310-118">Examples</span></span>](#examples)
    -   [<span data-ttu-id="09310-119">CHT IME versione 4,2, 4,3 e 4,4</span><span class="sxs-lookup"><span data-stu-id="09310-119">CHT IME version 4.2, 4.3 and 4.4</span></span>](#cht-ime-version-42-43-and-44)
    -   [<span data-ttu-id="09310-120">CHT IME versione 5,0</span><span class="sxs-lookup"><span data-stu-id="09310-120">CHT IME version 5.0</span></span>](#cht-ime-version-50)
    -   [<span data-ttu-id="09310-121">CHT IME versione 5,1, 5,2 e CHS versione 5,3</span><span class="sxs-lookup"><span data-stu-id="09310-121">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [<span data-ttu-id="09310-122">CHS IME versione 4,1</span><span class="sxs-lookup"><span data-stu-id="09310-122">CHS IME version 4.1</span></span>](#chs-ime-version-41)
    -   [<span data-ttu-id="09310-123">CHS IME versione 4,2</span><span class="sxs-lookup"><span data-stu-id="09310-123">CHS IME version 4.2</span></span>](#chs-ime-version-42)
-   [<span data-ttu-id="09310-124">Messaggi IME</span><span class="sxs-lookup"><span data-stu-id="09310-124">IME Messages</span></span>](#ime-messages)
    -   [<span data-ttu-id="09310-125">\_INPUTLANGCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="09310-125">WM\_INPUTLANGCHANGE</span></span>](#wm_inputlangchange)
    -   [<span data-ttu-id="09310-126">\_STARTCOMPOSITION IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="09310-126">WM\_IME\_STARTCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="09310-127">\_composizione IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="09310-127">WM\_IME\_COMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="09310-128">\_ENDCOMPOSITION IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="09310-128">WM\_IME\_ENDCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="09310-129">\_notifica IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="09310-129">WM\_IME\_NOTIFY</span></span>](/windows)
-   [<span data-ttu-id="09310-130">Rendering</span><span class="sxs-lookup"><span data-stu-id="09310-130">Rendering</span></span>](#rendering)
    -   [<span data-ttu-id="09310-131">Indicatore impostazioni locali di input</span><span class="sxs-lookup"><span data-stu-id="09310-131">Input Locale Indicator</span></span>](#input-locale-indicator)
    -   [<span data-ttu-id="09310-132">Finestra di composizione</span><span class="sxs-lookup"><span data-stu-id="09310-132">Composition Window</span></span>](#composition-window)
    -   [<span data-ttu-id="09310-133">Lettura e finestre candidate</span><span class="sxs-lookup"><span data-stu-id="09310-133">Reading and Candidate Windows</span></span>](#reading-and-candidate-windows)
-   [<span data-ttu-id="09310-134">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="09310-134">Limitations</span></span>](#limitations)
-   [<span data-ttu-id="09310-135">Informazioni registro di sistema</span><span class="sxs-lookup"><span data-stu-id="09310-135">Registry Information</span></span>](#registry-information)
-   [<span data-ttu-id="09310-136">Appendice A: versioni CHT per sistema operativo</span><span class="sxs-lookup"><span data-stu-id="09310-136">Appendix A: CHT Versions per Operating System</span></span>](#appendix-a-cht-versions-per-operating-system)
-   [<span data-ttu-id="09310-137">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="09310-137">Further Information</span></span>](#further-information)
-   [<span data-ttu-id="09310-138">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="09310-138">GetReadingString</span></span>](#getreadingstring)
-   [<span data-ttu-id="09310-139">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="09310-139">ShowReadingWindow</span></span>](#showreadingwindow)

## <a name="default-ime-behavior"></a><span data-ttu-id="09310-140">Comportamento IME predefinito</span><span class="sxs-lookup"><span data-stu-id="09310-140">Default IME Behavior</span></span>

<span data-ttu-id="09310-141">Gli IME mappano l'input da tastiera a componenti fonetici o altri elementi di linguaggio specifici di una lingua selezionata.</span><span class="sxs-lookup"><span data-stu-id="09310-141">IMEs map keyboard input to phonetic components or other language elements specific to a selected language.</span></span> <span data-ttu-id="09310-142">In uno scenario tipico, l'utente digita le chiavi che rappresentano la pronuncia di un carattere complesso.</span><span class="sxs-lookup"><span data-stu-id="09310-142">In a typical scenario, the user types keys that represent pronunciation of a complex character.</span></span> <span data-ttu-id="09310-143">Se l'IME riconosce la pronuncia come valida, presenta all'utente un elenco di candidati Word o phrase da cui l'utente può selezionare una scelta finale.</span><span class="sxs-lookup"><span data-stu-id="09310-143">If the IME recognizes the pronunciation as valid, it presents the user with a list of word or phrase candidates from which the user can select a final choice.</span></span> <span data-ttu-id="09310-144">La parola scelta viene quindi inviata all'applicazione tramite una serie di messaggi di Microsoft Windows [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="09310-144">The chosen word is then sent to the application through a series of Microsoft Windows [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span> <span data-ttu-id="09310-145">Poiché l'IME funziona a un livello al di sotto dell'applicazione intercettando l'input da tastiera, la presenza di un IME è trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="09310-145">Because the IME works at a level below the application by intercepting keyboard input, the presence of an IME is transparent to the application.</span></span> <span data-ttu-id="09310-146">Quasi tutte le applicazioni Windows possono sfruttare immediatamente gli IME senza essere consapevoli della loro esistenza e senza la necessità di scrivere codice speciale.</span><span class="sxs-lookup"><span data-stu-id="09310-146">Almost all Windows applications can readily take advantage of IMEs without being aware of their existence and without requiring special coding.</span></span>

<span data-ttu-id="09310-147">Un IME tipico Visualizza diverse finestre per guidare l'utente attraverso la voce di carattere, come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="09310-147">A typical IME displays several windows to guide the user through character entry, as shown in the following examples.</span></span>

![IME Visualizza diverse finestre](images/ime-elements.png)

| <span data-ttu-id="09310-149">Tipo di finestra</span><span class="sxs-lookup"><span data-stu-id="09310-149">Window Type</span></span>                                       | <span data-ttu-id="09310-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09310-150">Description</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="09310-151">Output IME</span><span class="sxs-lookup"><span data-stu-id="09310-151">IME Output</span></span>                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="09310-152">R.</span><span class="sxs-lookup"><span data-stu-id="09310-152">A.</span></span> <span data-ttu-id="09310-153">Lettura della finestra</span><span class="sxs-lookup"><span data-stu-id="09310-153">Reading Window</span></span>                                 | <span data-ttu-id="09310-154">Contiene le sequenze di tasti della tastiera; in genere viene modificato dopo ogni pressione di tasto.</span><span class="sxs-lookup"><span data-stu-id="09310-154">Contains keystrokes from the keyboard; typically changes after each keystroke.</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="09310-155">lettura stringa</span><span class="sxs-lookup"><span data-stu-id="09310-155">reading string</span></span>                               |
| <span data-ttu-id="09310-156">B.</span><span class="sxs-lookup"><span data-stu-id="09310-156">B.</span></span> <span data-ttu-id="09310-157">Finestra di composizione</span><span class="sxs-lookup"><span data-stu-id="09310-157">Composition Window</span></span>                             | <span data-ttu-id="09310-158">Contiene la raccolta di caratteri che l'utente ha composto con l'IME.</span><span class="sxs-lookup"><span data-stu-id="09310-158">Contains the collection of characters that the user has composed with the IME.</span></span> <span data-ttu-id="09310-159">Questi caratteri vengono disegnati dall'IME all'inizio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="09310-159">These characters are drawn by the IME on top of the application.</span></span> <span data-ttu-id="09310-160">Quando l'utente informa l'IME che la stringa di composizione è soddisfacente, l'IME invia la stringa di composizione all'applicazione tramite una serie di messaggi WM \_ Char.</span><span class="sxs-lookup"><span data-stu-id="09310-160">When the user notifies the IME that the composition string is satisfactory, the IME then sends the composition string to the application via a series of WM\_CHAR messages.</span></span> | <span data-ttu-id="09310-161">stringa di composizione</span><span class="sxs-lookup"><span data-stu-id="09310-161">composition string</span></span>                           |
| <span data-ttu-id="09310-162">C.</span><span class="sxs-lookup"><span data-stu-id="09310-162">C.</span></span> <span data-ttu-id="09310-163">Finestra candidata</span><span class="sxs-lookup"><span data-stu-id="09310-163">Candidate Window</span></span>                               | <span data-ttu-id="09310-164">Quando l'utente ha immesso una pronuncia valida, l'IME Visualizza un elenco di caratteri candidati che corrispondono alla pronuncia specificata.</span><span class="sxs-lookup"><span data-stu-id="09310-164">When the user has entered a valid pronunciation, the IME displays a list of candidate characters that all match the given pronunciation.</span></span> <span data-ttu-id="09310-165">L'utente seleziona quindi il carattere desiderato da questo elenco e l'IME aggiunge questo carattere alla visualizzazione della finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-165">The user then selects the intended character from this list, and the IME adds this character to the Composition Window display.</span></span>                                                    | <span data-ttu-id="09310-166">carattere successivo nella stringa di composizione</span><span class="sxs-lookup"><span data-stu-id="09310-166">the next character in the composition string</span></span> |
| <span data-ttu-id="09310-167">D.</span><span class="sxs-lookup"><span data-stu-id="09310-167">D.</span></span> <span data-ttu-id="09310-168">Indicatore [impostazioni locali di input](/windows/desktop/Intl/nls-terminology)</span><span class="sxs-lookup"><span data-stu-id="09310-168">[Input Locale](/windows/desktop/Intl/nls-terminology) indicator</span></span> | <span data-ttu-id="09310-169">Mostra la lingua selezionata dall'utente per l'input da tastiera.</span><span class="sxs-lookup"><span data-stu-id="09310-169">Shows the language the user has selected for keyboard input.</span></span> <span data-ttu-id="09310-170">Questo indicatore è incorporato nella barra delle applicazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="09310-170">This indicator is embedded in the Windows taskbar.</span></span> <span data-ttu-id="09310-171">È possibile selezionare la lingua di input aprendo il pannello di controllo Opzioni internazionali e della lingua e quindi facendo clic su dettagli nella scheda lingue.</span><span class="sxs-lookup"><span data-stu-id="09310-171">The input language can be selected by opening the Regional and Language Options Control Panel and then clicking Details on the Languages tab.</span></span>                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a><span data-ttu-id="09310-172">Uso di IME con DXUT</span><span class="sxs-lookup"><span data-stu-id="09310-172">Using IMEs with DXUT</span></span>

<span data-ttu-id="09310-173">In DXUT la classe CDXUTIMEEditBox implementa la funzionalità IME.</span><span class="sxs-lookup"><span data-stu-id="09310-173">In DXUT, the CDXUTIMEEditBox class implements IME functionality.</span></span> <span data-ttu-id="09310-174">Questa classe è derivata dalla classe CDXUTEditBox, il controllo di base di modifica fornito dal Framework.</span><span class="sxs-lookup"><span data-stu-id="09310-174">This class is derived from the CDXUTEditBox class, the basic edit control provided by the framework.</span></span> <span data-ttu-id="09310-175">CDXUTIMEEditBox estende il controllo di modifica per supportare gli IME eseguendo l'override dei metodi CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="09310-175">CDXUTIMEEditBox extends that edit control to support IMEs by overriding the CDXUTIMEEditBox methods.</span></span> <span data-ttu-id="09310-176">Queste classi sono progettate in modo da consentire agli sviluppatori di apprendere gli elementi necessari dal Framework per implementare il supporto IME nei propri controlli di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-176">The classes are designed this way to help developers learn what they need to take from the framework to implement IME support in their own edit controls.</span></span> <span data-ttu-id="09310-177">Nella parte restante di questo argomento viene illustrato come, in particolare, il Framework e CDXUTIMEEditBox esegue l'override di un controllo di modifica di base per implementare la funzionalità IME.</span><span class="sxs-lookup"><span data-stu-id="09310-177">The rest of this topic explains how the framework, and CDXUTIMEEditBox in particular, overrides a basic edit control to implement IME functionality.</span></span>

<span data-ttu-id="09310-178">La maggior parte delle variabili specifiche di IME in CDXUTIMEEditBox viene dichiarata come statica, perché molti buffer e Stati IME sono specifici del processo.</span><span class="sxs-lookup"><span data-stu-id="09310-178">Most of the IME-specific variables in CDXUTIMEEditBox are declared as static, because many IME buffers and states are specific to the process.</span></span> <span data-ttu-id="09310-179">Un processo, ad esempio, dispone di un solo buffer per la stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-179">For instance, a process has only one buffer for the composition string.</span></span> <span data-ttu-id="09310-180">Anche se il processo ha dieci controlli di modifica, tutti condivideranno lo stesso buffer di stringhe di composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-180">Even if the process has ten edit controls, they will all be sharing the same composition string buffer.</span></span> <span data-ttu-id="09310-181">Il buffer della stringa di composizione per CDXUTIMEEditBox è pertanto statico e impedisce all'applicazione di occupare spazio di memoria superfluo.</span><span class="sxs-lookup"><span data-stu-id="09310-181">The composition string buffer for CDXUTIMEEditBox is therefore static, preventing the application from taking up unnecessary memory space.</span></span>

<span data-ttu-id="09310-182">CDXUTIMEEditBox viene implementato nel codice DXUT seguente:</span><span class="sxs-lookup"><span data-stu-id="09310-182">CDXUTIMEEditBox is implemented in the following DXUT code:</span></span>

<span data-ttu-id="09310-183">(Radice SDK) \\ Esempi \\ comuni di C++ \\ \\ DXUTgui. cpp</span><span class="sxs-lookup"><span data-stu-id="09310-183">(SDK root)\\Samples\\C++\\Common\\DXUTgui.cpp</span></span>

## <a name="overriding-the-default-ime-behavior"></a><span data-ttu-id="09310-184">Override del comportamento predefinito di IME</span><span class="sxs-lookup"><span data-stu-id="09310-184">Overriding the Default IME Behavior</span></span>

<span data-ttu-id="09310-185">In genere, un IME usa le procedure standard di Windows per creare una finestra (vedere [uso di Windows](/windows/desktop/winmsg/using-windows)).</span><span class="sxs-lookup"><span data-stu-id="09310-185">Normally an IME uses standard Windows procedures to create a window (see [Using Windows](/windows/desktop/winmsg/using-windows)).</span></span> <span data-ttu-id="09310-186">In circostanze normali, questo produce risultati soddisfacenti.</span><span class="sxs-lookup"><span data-stu-id="09310-186">Under normal circumstances, this produces satisfactory results.</span></span> <span data-ttu-id="09310-187">Tuttavia, quando l'applicazione presenta la modalità schermo intero, come avviene in genere per i giochi, le finestre standard non funzionano più e potrebbero non essere visualizzate sopra l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="09310-187">However, when the application presents in full-screen mode, as is common for games, standard windows no longer work and may not display on top of the application.</span></span> <span data-ttu-id="09310-188">Per ovviare a questo problema, l'applicazione deve creare le finestre IME anziché basarsi su Windows per eseguire questa attività.</span><span class="sxs-lookup"><span data-stu-id="09310-188">To overcome this issue, the application must draw the IME windows itself instead of relying on Windows to perform this task.</span></span>

<span data-ttu-id="09310-189">Quando il comportamento predefinito della creazione della finestra IME non fornisce ciò che un'applicazione richiede, l'applicazione può eseguire l'override della gestione della finestra IME.</span><span class="sxs-lookup"><span data-stu-id="09310-189">When the default IME window creation behavior does not provide what an application requires, the application can override the IME window handling.</span></span> <span data-ttu-id="09310-190">Per ottenere questo risultato, un'applicazione può elaborare i messaggi relativi a IME e chiamare l'API di [Input Method Manager](/windows/desktop/Intl/input-method-manager) (IMM).</span><span class="sxs-lookup"><span data-stu-id="09310-190">An application can achieve this by processing IME-related messages and calling the [Input Method Manager](/windows/desktop/Intl/input-method-manager) (IMM) API.</span></span>

<span data-ttu-id="09310-191">Quando un utente interagisce con un IME per inserire caratteri complessi, IMM invia messaggi all'applicazione per notificare gli eventi importanti, ad esempio l'avvio di una composizione o la visualizzazione della finestra candidata.</span><span class="sxs-lookup"><span data-stu-id="09310-191">When a user interacts with an IME to input complex characters, the IMM sends messages to the application to notify it of important events, such as starting a composition or showing the candidate window.</span></span> <span data-ttu-id="09310-192">Un'applicazione in genere ignora questi messaggi e li passa al gestore di messaggi predefinito, che ne determina la gestione da parte dell'IME.</span><span class="sxs-lookup"><span data-stu-id="09310-192">An application typically ignores these messages and passes them to the default message handler, which causes the IME to handle them.</span></span> <span data-ttu-id="09310-193">Quando l'applicazione, anziché il gestore predefinito, gestisce i messaggi, controlla esattamente cosa accade in ogni evento IME.</span><span class="sxs-lookup"><span data-stu-id="09310-193">When the application, instead of the default handler, handles the messages, it controls exactly what happens at each of the IME events.</span></span> <span data-ttu-id="09310-194">Spesso il gestore di messaggi Recupera il contenuto delle varie finestre IME chiamando l'API IMM.</span><span class="sxs-lookup"><span data-stu-id="09310-194">Often the message handler retrieves the content of the various IME windows by calling the IMM API.</span></span> <span data-ttu-id="09310-195">Una volta fornite queste informazioni, l'applicazione può disegnare correttamente le finestre IME quando è necessario eseguirne il rendering sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="09310-195">Once the application has this information, it can properly draw the IME windows itself when it needs to render to the display.</span></span>

## <a name="functions"></a><span data-ttu-id="09310-196">Funzioni</span><span class="sxs-lookup"><span data-stu-id="09310-196">Functions</span></span>

<span data-ttu-id="09310-197">È necessario che un IME ottenga la stringa di lettura, nasconda la finestra di lettura e ottenga l'orientamento della finestra di lettura.</span><span class="sxs-lookup"><span data-stu-id="09310-197">An IME needs to get the reading string, hide the reading window, and get the orientation of reading window.</span></span> <span data-ttu-id="09310-198">Questa tabella mostra le funzionalità per ogni versione di IME:</span><span class="sxs-lookup"><span data-stu-id="09310-198">This table shows the functionalities per IME version:</span></span>



|                    | <span data-ttu-id="09310-199">Recupero della stringa di lettura</span><span class="sxs-lookup"><span data-stu-id="09310-199">Getting reading string</span></span>                                                | <span data-ttu-id="09310-200">Nascondere la finestra di lettura</span><span class="sxs-lookup"><span data-stu-id="09310-200">Hiding reading window</span></span>                       | <span data-ttu-id="09310-201">Orientamento della finestra di lettura</span><span class="sxs-lookup"><span data-stu-id="09310-201">Orientation of reading window</span></span>                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="09310-202">Prima della versione 6,0</span><span class="sxs-lookup"><span data-stu-id="09310-202">Before version 6.0</span></span> | <span data-ttu-id="09310-203">R.</span><span class="sxs-lookup"><span data-stu-id="09310-203">A.</span></span> <span data-ttu-id="09310-204">Lettura diretta dei dati di accesso alla finestra IME privata.</span><span class="sxs-lookup"><span data-stu-id="09310-204">Reading Window Access IME private data directly.</span></span> <span data-ttu-id="09310-205">Vedere "4 struttura"</span><span class="sxs-lookup"><span data-stu-id="09310-205">See "4 Structure"</span></span> | <span data-ttu-id="09310-206">Trap messaggi privati IME.</span><span class="sxs-lookup"><span data-stu-id="09310-206">Trap IME private messages.</span></span> <span data-ttu-id="09310-207">Vedere "3 messaggi"</span><span class="sxs-lookup"><span data-stu-id="09310-207">See "3 Messages"</span></span> | <span data-ttu-id="09310-208">Esaminare le informazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="09310-208">Examine registry information.</span></span> <span data-ttu-id="09310-209">Vedere "5 informazioni sul Registro di sistema"</span><span class="sxs-lookup"><span data-stu-id="09310-209">See "5 Registry Information"</span></span> |
| <span data-ttu-id="09310-210">Dopo la versione 6,0</span><span class="sxs-lookup"><span data-stu-id="09310-210">After version 6.0</span></span>  | [<span data-ttu-id="09310-211">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="09310-211">GetReadingString</span></span>](#getreadingstring)                                 | [<span data-ttu-id="09310-212">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="09310-212">ShowReadingWindow</span></span>](#showreadingwindow)     | [<span data-ttu-id="09310-213">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="09310-213">GetReadingString</span></span>](#getreadingstring)                      |



 

## <a name="messages"></a><span data-ttu-id="09310-214">Messaggi</span><span class="sxs-lookup"><span data-stu-id="09310-214">Messages</span></span>

<span data-ttu-id="09310-215">I messaggi seguenti non devono essere elaborati per l'IME più recente che implementa [ShowReadingWindow](#showreadingwindow)().</span><span class="sxs-lookup"><span data-stu-id="09310-215">The following messages don't have to be processed for newer IME that implements [ShowReadingWindow](#showreadingwindow)().</span></span>

<span data-ttu-id="09310-216">I messaggi seguenti sono intercettati dal gestore di messaggi dell'applicazione, ovvero non vengono passati a DefWindowProc, per impedire la visualizzazione della finestra di lettura.</span><span class="sxs-lookup"><span data-stu-id="09310-216">The following messages are trapped by application message handler (i.e. they are not passed to DefWindowProc) to prevent the reading window from showing up.</span></span>

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a><span data-ttu-id="09310-217">Esempio</span><span class="sxs-lookup"><span data-stu-id="09310-217">Examples</span></span>

<span data-ttu-id="09310-218">Negli esempi seguenti viene illustrato come ottenere informazioni sulla stringa da un IME precedente che non dispone di GetReadingString ().</span><span class="sxs-lookup"><span data-stu-id="09310-218">The following examples illustrate how to get reading string information from older IME that doesn't have GetReadingString().</span></span> <span data-ttu-id="09310-219">Il codice genera gli output seguenti:</span><span class="sxs-lookup"><span data-stu-id="09310-219">The code generates the following outputs:</span></span>



|              |                                                                                       |
|--------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09310-220">Dwlen DWORD</span><span class="sxs-lookup"><span data-stu-id="09310-220">DWORD dwlen</span></span>  | <span data-ttu-id="09310-221">Lunghezza della stringa di lettura</span><span class="sxs-lookup"><span data-stu-id="09310-221">Length of the reading string</span></span>                                                          |
| <span data-ttu-id="09310-222">Dwerr DWORD</span><span class="sxs-lookup"><span data-stu-id="09310-222">DWORD dwerr</span></span>  | <span data-ttu-id="09310-223">Indice del carattere di errore</span><span class="sxs-lookup"><span data-stu-id="09310-223">Index of error char</span></span>                                                                   |
| <span data-ttu-id="09310-224">WSTR LPWSTR</span><span class="sxs-lookup"><span data-stu-id="09310-224">LPWSTR wstr</span></span>  | <span data-ttu-id="09310-225">Puntatore alla stringa di lettura</span><span class="sxs-lookup"><span data-stu-id="09310-225">Pointer to the reading string</span></span>                                                         |
| <span data-ttu-id="09310-226">BOOL Unicode</span><span class="sxs-lookup"><span data-stu-id="09310-226">BOOL unicode</span></span> | <span data-ttu-id="09310-227">Se true, la stringa di lettura è in formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="09310-227">If true, the reading string is in Unicode format.</span></span> <span data-ttu-id="09310-228">In caso contrario, è in formato multibyte.</span><span class="sxs-lookup"><span data-stu-id="09310-228">Otherwise it's in multibyte format.</span></span> |



 

### <a name="cht-ime-version-42-43-and-44"></a><span data-ttu-id="09310-229">CHT IME versione 4,2, 4,3 e 4,4</span><span class="sxs-lookup"><span data-stu-id="09310-229">CHT IME version 4.2, 4.3 and 4.4</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a><span data-ttu-id="09310-230">CHT IME versione 5,0</span><span class="sxs-lookup"><span data-stu-id="09310-230">CHT IME version 5.0</span></span>

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

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a><span data-ttu-id="09310-231">CHT IME versione 5,1, 5,2 e CHS versione 5,3</span><span class="sxs-lookup"><span data-stu-id="09310-231">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>

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

### <a name="chs-ime-version-41"></a><span data-ttu-id="09310-232">CHS IME versione 4,1</span><span class="sxs-lookup"><span data-stu-id="09310-232">CHS IME version 4.1</span></span>

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

### <a name="chs-ime-version-42"></a><span data-ttu-id="09310-233">CHS IME versione 4,2</span><span class="sxs-lookup"><span data-stu-id="09310-233">CHS IME version 4.2</span></span>

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

## <a name="ime-messages"></a><span data-ttu-id="09310-234">Messaggi IME</span><span class="sxs-lookup"><span data-stu-id="09310-234">IME Messages</span></span>

<span data-ttu-id="09310-235">Un'applicazione a schermo intero deve gestire correttamente i messaggi relativi a IME seguenti:</span><span class="sxs-lookup"><span data-stu-id="09310-235">A full-screen application must properly handle the following IME-related messages:</span></span>

### <a name="wm_inputlangchange"></a><span data-ttu-id="09310-236">\_INPUTLANGCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="09310-236">WM\_INPUTLANGCHANGE</span></span>

<span data-ttu-id="09310-237">IMM Invia un messaggio WM \_ INPUTLANGCHANGE alla finestra attiva di un'applicazione dopo che l'utente ha modificato le impostazioni locali di input con una combinazione di tasti (in genere Alt + Maiusc) o con l'indicatore delle impostazioni locali di input sulla barra delle applicazioni o sulla barra della lingua.</span><span class="sxs-lookup"><span data-stu-id="09310-237">The IMM sends a WM\_INPUTLANGCHANGE message to the active window of an application after the input locale has been changed by the user with a key combination (usually ALT+SHIFT), or with the input locale indicator on the taskbar or language bar.</span></span> <span data-ttu-id="09310-238">La barra del linguaggio è un controllo su schermo con il quale l'utente può configurare un servizio di testo.</span><span class="sxs-lookup"><span data-stu-id="09310-238">The language bar is an on-screen control with which the user can configure a text service.</span></span> <span data-ttu-id="09310-239">Vedere [come visualizzare la barra della lingua](/windows/desktop/TSF/how-to-set-up-tsf). Lo screenshot seguente mostra un elenco di selezione della lingua che viene visualizzato quando l'utente fa clic sull'indicatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="09310-239">(See [How to show the language bar](/windows/desktop/TSF/how-to-set-up-tsf).) The following screen shot shows a language selection list that is displayed when the user clicks on the locale indicator.</span></span>

![elenco di selezione della lingua visualizzato quando l'utente fa clic sull'indicatore delle impostazioni locali](images/ime-langselection.png)

<span data-ttu-id="09310-241">Quando IMM Invia un messaggio WM \_ INPUTLANGCHANGE, CDXUTIMEEditBox deve eseguire diverse attività importanti:</span><span class="sxs-lookup"><span data-stu-id="09310-241">When the IMM sends a WM\_INPUTLANGCHANGE message, CDXUTIMEEditBox must perform several important tasks:</span></span>

1.  <span data-ttu-id="09310-242">Il metodo GetKeyboardLayout viene chiamato per restituire l'identificatore delle impostazioni locali di input (ID) per il thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="09310-242">The GetKeyboardLayout method is called to return the input locale identifier (ID) for the application thread.</span></span> <span data-ttu-id="09310-243">La classe CDXUTIMEEditBox Salva questo ID nelle variabili membro statiche s \_ hklCurrent per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="09310-243">The CDXUTIMEEditBox class saves this ID in its static member variable s\_hklCurrent for later use.</span></span> <span data-ttu-id="09310-244">È importante che l'applicazione conosca le impostazioni locali di input correnti, perché l'IME per ogni lingua presenta un proprio comportamento distinto.</span><span class="sxs-lookup"><span data-stu-id="09310-244">It is important for the application to know the current input locale, because the IME for each language has its own distinct behavior.</span></span> <span data-ttu-id="09310-245">Lo sviluppatore potrebbe dover fornire codice diverso per le diverse impostazioni locali di input.</span><span class="sxs-lookup"><span data-stu-id="09310-245">The developer may need to provide different code for different input locales.</span></span>
2.  <span data-ttu-id="09310-246">CDXUTIMEEditBox Inizializza una stringa da visualizzare nell'indicatore della lingua della casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-246">CDXUTIMEEditBox initializes a string to display in the edit box language indicator.</span></span> <span data-ttu-id="09310-247">Questo indicatore può visualizzare la lingua di input attiva quando l'applicazione è in esecuzione in modalità a schermo intero e non è visibile né la barra delle applicazioni né la barra della lingua.</span><span class="sxs-lookup"><span data-stu-id="09310-247">This indicator can display the active input language when the application is running in full-screen mode and neither the taskbar nor language bar is visible.</span></span>
3.  <span data-ttu-id="09310-248">Il metodo ImmGetConversionStatus viene chiamato per indicare se le impostazioni locali di input sono in modalità di conversione nativa o non nativa.</span><span class="sxs-lookup"><span data-stu-id="09310-248">The ImmGetConversionStatus method is called to indicate whether the input locale is in native or non-native conversion mode.</span></span> <span data-ttu-id="09310-249">La modalità di conversione nativa consente all'utente di immettere testo nella lingua scelta.</span><span class="sxs-lookup"><span data-stu-id="09310-249">Native conversion mode lets the user enter text in the chosen language.</span></span> <span data-ttu-id="09310-250">La modalità di conversione non nativa fa in modo che la tastiera funga da tastiera inglese standard.</span><span class="sxs-lookup"><span data-stu-id="09310-250">Non-native conversion mode makes the keyboard act as a standard English keyboard.</span></span> <span data-ttu-id="09310-251">È importante fornire all'utente un segnale visivo per il tipo di modalità di conversione in cui si trova l'IME, in modo che l'utente possa facilmente sapere quali sono i caratteri da prevedere quando si preme un tasto.</span><span class="sxs-lookup"><span data-stu-id="09310-251">It is important to give the user a visual cue as to what type of conversion mode the IME is in, so that the user can easily know what characters to expect when hitting a key.</span></span> <span data-ttu-id="09310-252">CDXUTIMEEditBox fornisce questo segnale visivo con un colore dell'indicatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="09310-252">CDXUTIMEEditBox provides this visual cue with a language indicator color.</span></span> <span data-ttu-id="09310-253">Quando le impostazioni locali di input usano un IME con la modalità di conversione nativa, la classe CDXUTIMEEditBox disegna il testo dell'indicatore con il colore definito dal \_ parametro m IndicatorImeColor.</span><span class="sxs-lookup"><span data-stu-id="09310-253">When the input locale uses an IME with native conversion mode, the CDXUTIMEEditBox class draws the indicator text with the color defined by the m\_IndicatorImeColor parameter.</span></span> <span data-ttu-id="09310-254">Quando l'IME si trova in modalità di conversione non nativa oppure non viene utilizzato alcun IME, la classe disegna il testo dell'indicatore con il colore definito dal parametro m \_ IndicatorEngColor.</span><span class="sxs-lookup"><span data-stu-id="09310-254">When the IME is in non-native conversion mode, or no IME is used at all, the class draws the indicator text with the color defined by the m\_IndicatorEngColor parameter.</span></span>
4.  <span data-ttu-id="09310-255">CDXUTIMEEditBox controlla le impostazioni locali di input e imposta la variabile membro statica s \_ bInsertOnType su true per il coreano e false per tutte le altre lingue.</span><span class="sxs-lookup"><span data-stu-id="09310-255">CDXUTIMEEditBox checks the input locale and sets the static member variable s\_bInsertOnType to TRUE for Korean and FALSE for all other languages.</span></span> <span data-ttu-id="09310-256">Questo flag è obbligatorio a causa dei diversi comportamenti degli IME coreano e di tutti gli altri IME.</span><span class="sxs-lookup"><span data-stu-id="09310-256">This flag is required because of the different behaviors of Korean IMEs and all other IMEs.</span></span> <span data-ttu-id="09310-257">Quando si immettono caratteri in lingue diverse dal coreano, il testo immesso dall'utente viene visualizzato nella finestra di composizione e l'utente può modificare liberamente il contenuto della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-257">When entering characters in languages other than Korean, the user-entered text is displayed in the composition window, and the user can freely change the content of the composition string.</span></span> <span data-ttu-id="09310-258">L'utente preme il tasto INVIO quando è soddisfatto dalla stringa di composizione e la stringa di composizione viene inviata all'applicazione come una serie di messaggi WM \_ Char.</span><span class="sxs-lookup"><span data-stu-id="09310-258">The user presses the ENTER key when satisfied with the composition string, and the composition string is sent to the application as a series of WM\_CHAR messages.</span></span> <span data-ttu-id="09310-259">Negli IME coreano, tuttavia, quando un utente preme un tasto per immettere il testo, un carattere viene immediatamente inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="09310-259">In Korean IMEs, however, when a user presses a key to enter text, a character is immediately sent to the application.</span></span> <span data-ttu-id="09310-260">Quando l'utente preme successivamente più tasti per modificare il carattere iniziale, il carattere nella casella di modifica viene modificato in modo da riflettere l'input aggiuntivo da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="09310-260">When the user subsequently presses more keys to modify that initial character, the character in the edit box changes to reflect additional input from the user.</span></span> <span data-ttu-id="09310-261">In sostanza, l'utente sta componendo i caratteri nella casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-261">Essentially, the user is composing characters in the edit box.</span></span> <span data-ttu-id="09310-262">Questi due comportamenti sono abbastanza diversi da consentire a CDXUTIMEEditBox di scrivere codice per ognuno di essi in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="09310-262">These two behaviors are different enough that CDXUTIMEEditBox must code for each of them specifically.</span></span>
5.  <span data-ttu-id="09310-263">Il metodo del membro statico SetupImeApi viene chiamato per recuperare gli indirizzi di due funzioni dal modulo IME: GetReadingString e ShowReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="09310-263">The static member method SetupImeApi is called to retrieve addresses of two functions from the IME module: GetReadingString and ShowReadingWindow.</span></span> <span data-ttu-id="09310-264">Se queste funzioni esistono, viene chiamato ShowReadingWindow per nascondere la finestra di lettura predefinita per questo IME.</span><span class="sxs-lookup"><span data-stu-id="09310-264">If these functions exist, ShowReadingWindow is called to hide the default reading window for this IME.</span></span> <span data-ttu-id="09310-265">Poiché l'applicazione esegue il rendering della finestra di lettura, viene inviata una notifica all'IME per disabilitare il disegno della finestra di lettura predefinita in modo che non interferisca con il rendering a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="09310-265">Because the application renders the reading window itself, it notifies the IME to disable drawing the default reading window so that it will not interfere with full-screen rendering.</span></span>

<span data-ttu-id="09310-266">IMM Invia un \_ \_ messaggio di contestuale di WM IME quando viene attivata una finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="09310-266">The IMM sends a WM\_IME\_SETCONTEXT message when a window of the application is activated.</span></span> <span data-ttu-id="09310-267">Il parametro lParam di questo messaggio contiene un flag che indica all'IME quali finestre devono essere disegnate e quali no.</span><span class="sxs-lookup"><span data-stu-id="09310-267">The lParam parameter of this message contains a flag that indicates to the IME which windows should get drawn and which should not.</span></span> <span data-ttu-id="09310-268">Poiché l'applicazione gestisce tutto il disegno, non è necessario che l'IME disegni le finestre IME.</span><span class="sxs-lookup"><span data-stu-id="09310-268">Because the application is handling all of the drawing, it does not need the IME to draw any of the IME windows.</span></span> <span data-ttu-id="09310-269">Il gestore di messaggi dell'applicazione, pertanto, imposta semplicemente lParam su 0 e restituisce.</span><span class="sxs-lookup"><span data-stu-id="09310-269">Therefore, the application's message handler simply sets lParam to 0 and returns.</span></span>

<span data-ttu-id="09310-270">Per consentire alle applicazioni di supportare l'IME, è necessaria un'elaborazione speciale per il messaggio relativo al contesto IME di WM per il messaggio correlato a IME \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="09310-270">In order for applications to support IME, special processing is needed for the IME-related message WM\_IME\_SETCONTEXT.</span></span> <span data-ttu-id="09310-271">Poiché Windows in genere invia questo messaggio all'applicazione prima di chiamare il metodo PanoramaInitialize (), panorama non ha la possibilità di elaborare l'interfaccia utente per visualizzare le finestre di elenco dei candidati.</span><span class="sxs-lookup"><span data-stu-id="09310-271">Since Windows typically sends this message to the application prior to calling the PanoramaInitialize() method, Panorama doesn't have a chance to process the UI for showing candidate list windows.</span></span>

<span data-ttu-id="09310-272">Il frammento di codice seguente specifica alle applicazioni Windows di non visualizzare alcuna interfaccia utente associata alla finestra elenco candidati, consentendo a Panorama di gestire questa interfaccia utente in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="09310-272">The following code snippet specifies to Windows applications not to display any UI associated with the candidate list window, allowing Panorama to specifically handle this UI.</span></span>

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a><span data-ttu-id="09310-273">\_STARTCOMPOSITION IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="09310-273">WM\_IME\_STARTCOMPOSITION</span></span>

<span data-ttu-id="09310-274">IMM Invia un \_ \_ messaggio STARTCOMPOSITION di WM IME all'applicazione quando una composizione IME sta per iniziare in seguito a sequenze di tasti da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="09310-274">The IMM sends a WM\_IME\_STARTCOMPOSITION message to the application when an IME composition is about to begin as a result of keystrokes by the user.</span></span> <span data-ttu-id="09310-275">Se l'IME usa la finestra di composizione, Visualizza la stringa di composizione corrente in una finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-275">If the IME uses the composition window, it displays the current composition string in a composition window.</span></span> <span data-ttu-id="09310-276">CDXUTIMEEditBox gestisce questo messaggio eseguendo due attività:</span><span class="sxs-lookup"><span data-stu-id="09310-276">CDXUTIMEEditBox handles this message by performing two tasks:</span></span>

1.  <span data-ttu-id="09310-277">CDXUTIMEEditBox Cancella il buffer della stringa di composizione e il buffer dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="09310-277">CDXUTIMEEditBox clears the composition string buffer and attribute buffer.</span></span> <span data-ttu-id="09310-278">Questi buffer sono membri statici di CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="09310-278">These buffers are static members of CDXUTIMEEditBox.</span></span>
2.  <span data-ttu-id="09310-279">CDXUTIMEEditBox imposta la \_ variabile membro statico s bHideCaret su true.</span><span class="sxs-lookup"><span data-stu-id="09310-279">CDXUTIMEEditBox sets the s\_bHideCaret static member variable to TRUE.</span></span> <span data-ttu-id="09310-280">Questo membro, definito nella classe di base CDXUTEditBox, determina se il cursore nella casella di modifica deve essere disegnato quando viene eseguito il rendering della casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-280">This member, defined in the base CDXUTEditBox class, controls whether the cursor in the edit box should be drawn when the edit box is rendered.</span></span> <span data-ttu-id="09310-281">La finestra di composizione funziona in modo analogo a una casella di modifica con testo e cursore.</span><span class="sxs-lookup"><span data-stu-id="09310-281">The composition window functions similarly to an edit box with text and cursor.</span></span> <span data-ttu-id="09310-282">Per evitare confusione quando la finestra di composizione è visibile, la casella di modifica nasconde il cursore in modo che sia visibile solo un cursore alla volta.</span><span class="sxs-lookup"><span data-stu-id="09310-282">To avoid confusion when the composition window is visible, the edit box hides its cursor so that only one cursor is visible at a time.</span></span>

### <a name="wm_ime_composition"></a><span data-ttu-id="09310-283">\_composizione IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="09310-283">WM\_IME\_COMPOSITION</span></span>

<span data-ttu-id="09310-284">IMM Invia un \_ \_ messaggio di composizione IME WM all'applicazione quando l'utente immette una sequenza di tasti per modificare la stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-284">The IMM sends a WM\_IME\_COMPOSITION message to the application when the user enters a keystroke to change the composition string.</span></span> <span data-ttu-id="09310-285">Il valore di lParam indica il tipo di informazioni che l'applicazione può recuperare da input Method Manager (IMM).</span><span class="sxs-lookup"><span data-stu-id="09310-285">The value of lParam indicates what type of information the application can retrieve from the Input Method Manager (IMM).</span></span> <span data-ttu-id="09310-286">L'applicazione deve recuperare le informazioni disponibili chiamando [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) e quindi salvare le informazioni nel buffer privato in modo che sia in grado di eseguire il rendering degli elementi IME in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="09310-286">The application should retrieve the available information by calling [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) and then should save the information in its private buffer so that it can render the IME elements later.</span></span>

<span data-ttu-id="09310-287">CDXUTIMEEditBox verifica e recupera i dati di stringa di composizione seguenti:</span><span class="sxs-lookup"><span data-stu-id="09310-287">CDXUTIMEEditBox checks for and retrieves the following composition string data:</span></span>



| <span data-ttu-id="09310-288">[**WM \_ Valore \_**](/windows/desktop/Intl/wm-ime-composition) del flag lParam composizione IME</span><span class="sxs-lookup"><span data-stu-id="09310-288">[**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam Flag Value</span></span> | <span data-ttu-id="09310-289">Data</span><span class="sxs-lookup"><span data-stu-id="09310-289">Data</span></span>                           | <span data-ttu-id="09310-290">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09310-290">Description</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09310-291">comaccarezzatore cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="09310-291">GCS\_COMPATTR</span></span>                                                         | <span data-ttu-id="09310-292">Attributo Composition</span><span class="sxs-lookup"><span data-stu-id="09310-292">Composition Attribute</span></span>          | <span data-ttu-id="09310-293">Questo attributo contiene informazioni quali lo stato di ogni carattere nella stringa di composizione (ad esempio, convertito o non convertito).</span><span class="sxs-lookup"><span data-stu-id="09310-293">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="09310-294">Queste informazioni sono necessarie perché CDXUTIMEEditBox colora i caratteri della stringa di composizione in modo diverso in base ai rispettivi attributi.</span><span class="sxs-lookup"><span data-stu-id="09310-294">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span>                                                                                   |
| <span data-ttu-id="09310-295">COMPCLAUSE cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="09310-295">GCS\_COMPCLAUSE</span></span>                                                       | <span data-ttu-id="09310-296">Informazioni sulla clausola di composizione</span><span class="sxs-lookup"><span data-stu-id="09310-296">Composition Clause Information</span></span> | <span data-ttu-id="09310-297">Le informazioni sulla clausola vengono utilizzate quando l'IME giapponese è attivo.</span><span class="sxs-lookup"><span data-stu-id="09310-297">This clause information is used when the Japanese IME is active.</span></span> <span data-ttu-id="09310-298">Quando viene convertita una stringa di composizione giapponese, i caratteri possono essere raggruppati come una clausola che viene convertita in una singola entità.</span><span class="sxs-lookup"><span data-stu-id="09310-298">When a Japanese composition string is converted, characters may be grouped together as a clause that gets converted to a single entity.</span></span> <span data-ttu-id="09310-299">Quando l'utente sposta il cursore, CDXUTIMEEditBox usa queste informazioni per evidenziare l'intera clausola, anziché un solo carattere nella clausola.</span><span class="sxs-lookup"><span data-stu-id="09310-299">When the user moves the cursor, CDXUTIMEEditBox uses this information to highlight the entire clause, instead of just a single character within the clause.</span></span> |
| <span data-ttu-id="09310-300">COMPSTR cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="09310-300">GCS\_COMPSTR</span></span>                                                          | <span data-ttu-id="09310-301">Stringa di composizione</span><span class="sxs-lookup"><span data-stu-id="09310-301">Composition String</span></span>             | <span data-ttu-id="09310-302">Questa stringa è la stringa aggiornata composta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="09310-302">This string is the up-to-date string being composed by the user.</span></span> <span data-ttu-id="09310-303">Si tratta anche della stringa visualizzata nella finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-303">This is also the string displayed in the composition window.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="09310-304">CURSORPOS cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="09310-304">GCS\_CURSORPOS</span></span>                                                        | <span data-ttu-id="09310-305">Posizione del cursore di composizione</span><span class="sxs-lookup"><span data-stu-id="09310-305">Composition Cursor Position</span></span>    | <span data-ttu-id="09310-306">La finestra di composizione implementa un cursore, simile al cursore in una casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-306">The composition window implements a cursor, similar to the cursor in an edit box.</span></span> <span data-ttu-id="09310-307">L'applicazione può recuperare la posizione del cursore durante l'elaborazione del \_ messaggio di composizione IME WM per \_ creare correttamente il cursore.</span><span class="sxs-lookup"><span data-stu-id="09310-307">The application can retrieve the cursor position when processing the WM\_IME\_COMPOSITION message in order to draw the cursor properly.</span></span>                                                                                                                                            |
| <span data-ttu-id="09310-308">RESULTSTR cataloghi globali \_</span><span class="sxs-lookup"><span data-stu-id="09310-308">GCS\_RESULTSTR</span></span>                                                        | <span data-ttu-id="09310-309">Stringa di risultato</span><span class="sxs-lookup"><span data-stu-id="09310-309">Result String</span></span>                  | <span data-ttu-id="09310-310">La stringa di risultato è disponibile quando l'utente sta per completare il processo di composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-310">The result string is available when the user is about to complete the composition process.</span></span> <span data-ttu-id="09310-311">Questa stringa deve essere recuperata e i caratteri devono essere inviati alla casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-311">This string should be retrieved and the characters should be sent to the edit box.</span></span>                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a><span data-ttu-id="09310-312">\_ENDCOMPOSITION IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="09310-312">WM\_IME\_ENDCOMPOSITION</span></span>

<span data-ttu-id="09310-313">IMM Invia un \_ \_ messaggio ENDCOMPOSITION di WM IME all'applicazione al termine dell'operazione di composizione IME.</span><span class="sxs-lookup"><span data-stu-id="09310-313">The IMM sends a WM\_IME\_ENDCOMPOSITION message to the application when the IME composition operation is ending.</span></span> <span data-ttu-id="09310-314">Questa situazione può verificarsi quando l'utente preme il tasto INVIO per approvare la stringa di composizione o il tasto ESC per annullare la composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-314">This can occur when the user presses the ENTER key to approve the composition string, or the ESC key to cancel the composition.</span></span> <span data-ttu-id="09310-315">CDXUTIMEEditBox gestisce questo messaggio impostando il buffer della stringa di composizione come vuoto.</span><span class="sxs-lookup"><span data-stu-id="09310-315">CDXUTIMEEditBox handles this message by setting the composition string buffer to be empty.</span></span> <span data-ttu-id="09310-316">Imposta quindi s \_ bHideCaret su false perché la finestra di composizione è chiusa e il cursore nella casella di modifica deve essere nuovamente visibile.</span><span class="sxs-lookup"><span data-stu-id="09310-316">It then sets s\_bHideCaret to FALSE because the composition window is closed and the cursor in the edit box should again be visible.</span></span>

<span data-ttu-id="09310-317">Il gestore di messaggi CDXUTIMEEditBox imposta inoltre s \_ bShowReadingWindow su false.</span><span class="sxs-lookup"><span data-stu-id="09310-317">The CDXUTIMEEditBox message handler also sets s\_bShowReadingWindow to FALSE.</span></span> <span data-ttu-id="09310-318">Questo flag controlla se la classe disegna la finestra di lettura quando viene eseguito il rendering della casella di modifica, pertanto deve essere impostata su FALSE al termine di una composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-318">This flag controls whether the class draws the reading window when the edit box renders itself, so it must be set to FALSE when a composition ends.</span></span>

### <a name="wm_ime_notify"></a><span data-ttu-id="09310-319">\_notifica IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="09310-319">WM\_IME\_NOTIFY</span></span>

<span data-ttu-id="09310-320">IMM Invia un \_ \_ messaggio di notifica dell'IME WM all'applicazione ogni volta che viene modificata una finestra IME.</span><span class="sxs-lookup"><span data-stu-id="09310-320">The IMM sends a WM\_IME\_NOTIFY message to the application whenever an IME window changes.</span></span> <span data-ttu-id="09310-321">Un'applicazione che gestisce il disegno delle finestre IME deve elaborare questo messaggio in modo che sia in grado di riconoscere eventuali aggiornamenti al contenuto della finestra.</span><span class="sxs-lookup"><span data-stu-id="09310-321">An application that handles the drawing of the IME windows should process this message so that it is aware of any update to the content of the window.</span></span> <span data-ttu-id="09310-322">Il wParam indica il comando o la modifica che si sta verificando.</span><span class="sxs-lookup"><span data-stu-id="09310-322">The wParam indicates the command or the change that is taking place.</span></span> <span data-ttu-id="09310-323">CDXUTIMEEditBox gestisce i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="09310-323">CDXUTIMEEditBox handles the following commands:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09310-324">Comando IME</span><span class="sxs-lookup"><span data-stu-id="09310-324">IME Command</span></span></th>
<th><span data-ttu-id="09310-325">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09310-325">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09310-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="09310-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span></span></td>
<td><span data-ttu-id="09310-327">Questo attributo contiene informazioni quali lo stato di ogni carattere nella stringa di composizione (ad esempio, convertito o non convertito).</span><span class="sxs-lookup"><span data-stu-id="09310-327">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="09310-328">Queste informazioni sono necessarie perché CDXUTIMEEditBox colora i caratteri della stringa di composizione in modo diverso in base ai rispettivi attributi.</span><span class="sxs-lookup"><span data-stu-id="09310-328">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09310-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="09310-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> / <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span></span></td>
<td><span data-ttu-id="09310-330">Inviato all'applicazione quando la finestra candidata sta per essere aperta o aggiornata rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="09310-330">Sent to the application when the candidate window is about to be opened or updated, respectively.</span></span> <span data-ttu-id="09310-331">La finestra candidato si apre quando un utente desidera modificare la scelta del testo convertito.</span><span class="sxs-lookup"><span data-stu-id="09310-331">The candidate window opens when a user wishes to change the converted text choice.</span></span> <span data-ttu-id="09310-332">La finestra viene aggiornata quando un utente sposta l'indicatore di selezione o modifica la pagina.</span><span class="sxs-lookup"><span data-stu-id="09310-332">The window is updated when a user moves the selection indicator or changes the page.</span></span> <span data-ttu-id="09310-333">CDXUTIMEEditBox usa un gestore di messaggi per entrambi i comandi perché le attività richieste sono esattamente le stesse:</span><span class="sxs-lookup"><span data-stu-id="09310-333">CDXUTIMEEditBox uses one message handler for both of these commands because the tasks required are exactly the same:</span></span><br/>
<ol>
<li><span data-ttu-id="09310-334">CDXUTIMEEditBox imposta il membro bShowWindow della struttura dell'elenco dei candidati s_CandList su TRUE per indicare che è necessario disegnare la finestra candidata durante il rendering del frame.</span><span class="sxs-lookup"><span data-stu-id="09310-334">CDXUTIMEEditBox sets the bShowWindow member of the candidate list structure s_CandList to TRUE to indicate that the candidate window needs to be drawn during frame rendering.</span></span></li>
<li><span data-ttu-id="09310-335">CDXUTIMEEditBox recupera l'elenco dei candidati chiamando <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, prima di tutto per ottenere la dimensione del buffer richiesta e quindi di nuovo per ottenere i dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="09310-335">CDXUTIMEEditBox retrieves the candidate list by calling <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, first to get the required buffer size, and then again to get the actual data.</span></span></li>
<li><span data-ttu-id="09310-336">La struttura dell'elenco dei candidati privati s_CandList viene inizializzata con i dati candidati recuperati.</span><span class="sxs-lookup"><span data-stu-id="09310-336">The private candidate list structure s_CandList is initialized with the retrieved candidate data.</span></span></li>
<li><span data-ttu-id="09310-337">Le stringhe candidate vengono archiviate come una matrice di stringhe.</span><span class="sxs-lookup"><span data-stu-id="09310-337">The candidate strings are stored as an array of strings.</span></span></li>
<li><span data-ttu-id="09310-338">L'indice della voce selezionata, nonché l'indice della pagina, viene salvato.</span><span class="sxs-lookup"><span data-stu-id="09310-338">The index of the selected entry, as well as the page index, is saved.</span></span></li>
<li><span data-ttu-id="09310-339">CDXUTIMEEditBox controlla se lo stile della finestra candidato è verticale o orizzontale.</span><span class="sxs-lookup"><span data-stu-id="09310-339">CDXUTIMEEditBox checks whether the candidate window style is vertical or horizontal.</span></span> <span data-ttu-id="09310-340">Se lo stile della finestra è orizzontale, un buffer di stringa aggiuntivo, il membro HoriCand di s_CandList, deve essere inizializzato con tutte le stringhe candidate, con spazi compresi tra tutte le stringhe adiacenti.</span><span class="sxs-lookup"><span data-stu-id="09310-340">If the window style is horizontal, an additional string buffer, the HoriCand member of s_CandList, must be initialized with all of the candidate strings, with space characters inserted between all adjacent strings.</span></span> <span data-ttu-id="09310-341">Quando si esegue il rendering di una finestra candidata verticale, le singole stringhe candidate vengono disegnate una alla volta, con le coordinate y incrementate per ogni stringa.</span><span class="sxs-lookup"><span data-stu-id="09310-341">When rendering a vertical candidate window, the individual candidate strings are drawn one at a time, with the y coordinates incremented for each string.</span></span> <span data-ttu-id="09310-342">Questa stringa HoriCand deve tuttavia essere usata per il rendering di una finestra candidata orizzontale, perché il carattere spazio è il modo migliore per separare due stringhe adiacenti sulla stessa riga.</span><span class="sxs-lookup"><span data-stu-id="09310-342">However, this HoriCand string should be used when rendering a horizontal candidate window, because the space character is the best way to separate two adjacent strings on the same line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09310-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="09310-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span></span></td>
<td><span data-ttu-id="09310-344">Inviato all'applicazione quando una finestra candidata sta per essere chiusa.</span><span class="sxs-lookup"><span data-stu-id="09310-344">Sent to the application when a candidate window is about to close.</span></span> <span data-ttu-id="09310-345">Questo errore si verifica quando un utente ha effettuato una selezione dall'elenco dei candidati.</span><span class="sxs-lookup"><span data-stu-id="09310-345">This happens when a user has made a selection from the candidate list.</span></span> <span data-ttu-id="09310-346">CDXUTIMEEditBox gestisce questo comando impostando il flag visibile della finestra candidata su FALSE e quindi deselezionando il buffer di stringhe candidato.</span><span class="sxs-lookup"><span data-stu-id="09310-346">CDXUTIMEEditBox handles this command by setting the visible flag of the candidate window to FALSE and then clearing the candidate string buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09310-347">IMN_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="09310-347">IMN_PRIVATE</span></span></td>
<td><span data-ttu-id="09310-348">Inviato all'applicazione quando l'IME ha aggiornato la relativa stringa di lettura in seguito alla digitazione o alla rimozione di caratteri da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="09310-348">Sent to the application when the IME has updated its reading string as a result of the user typing or removing characters.</span></span> <span data-ttu-id="09310-349">L'applicazione deve recuperare la stringa di lettura e salvarla per il rendering.</span><span class="sxs-lookup"><span data-stu-id="09310-349">The application should retrieve the reading string and save it for rendering.</span></span> <span data-ttu-id="09310-350">CDXUTIMEEditBox dispone di due metodi per recuperare la stringa di lettura, in base al modo in cui le stringhe di lettura sono supportate nell'IME:</span><span class="sxs-lookup"><span data-stu-id="09310-350">CDXUTIMEEditBox has two methods to retrieve the reading string, based upon how reading strings are supported in the IME:</span></span> <br/>
<ul>
<li><span data-ttu-id="09310-351">Se l'IME supporta la funzione GetReadingString, viene chiamato GetReadingString per recuperare la stringa di lettura.</span><span class="sxs-lookup"><span data-stu-id="09310-351">If the IME supports the GetReadingString function, GetReadingString is called to retrieve the reading string.</span></span></li>
<li><span data-ttu-id="09310-352">Se l'IME non implementa GetReadingString, CDXUTIMEEditBox recupera la stringa di lettura dal contenuto del contesto di input.</span><span class="sxs-lookup"><span data-stu-id="09310-352">If the IME does not implement GetReadingString, CDXUTIMEEditBox retrieves the reading string from the input context content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a><span data-ttu-id="09310-353">Rendering</span><span class="sxs-lookup"><span data-stu-id="09310-353">Rendering</span></span>

<span data-ttu-id="09310-354">Il rendering degli elementi e delle finestre IME è semplice.</span><span class="sxs-lookup"><span data-stu-id="09310-354">Rendering of the IME elements and windows is straightforward.</span></span> <span data-ttu-id="09310-355">CDXUTIMEEditBox consente di eseguire prima il rendering della classe di base perché le finestre IME verranno visualizzate nella parte superiore del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-355">CDXUTIMEEditBox lets the base class render first because IME windows should appear on top of the edit control.</span></span> <span data-ttu-id="09310-356">Dopo il rendering della casella di modifica di base, CDXUTIMEEditBox controlla il flag di visibilità di ogni finestra IME (indicatore, composizione, candidato e finestra di lettura) e disegna la finestra se deve essere visibile.</span><span class="sxs-lookup"><span data-stu-id="09310-356">After the base edit box is rendered, CDXUTIMEEditBox checks the visibility flag of each IME window (indicator, composition, candidate, and reading window) and draws the window if it should be visible.</span></span> <span data-ttu-id="09310-357">Vedere comportamento IME predefinito per le descrizioni dei diversi tipi di finestra IME.</span><span class="sxs-lookup"><span data-stu-id="09310-357">See Default IME Behavior for descriptions of the different IME window types.</span></span>

### <a name="input-locale-indicator"></a><span data-ttu-id="09310-358">Indicatore impostazioni locali di input</span><span class="sxs-lookup"><span data-stu-id="09310-358">Input Locale Indicator</span></span>

<span data-ttu-id="09310-359">Viene eseguito il rendering dell'indicatore delle impostazioni locali di input prima di qualsiasi altra finestra IME perché è un elemento che viene sempre visualizzato.</span><span class="sxs-lookup"><span data-stu-id="09310-359">The input locale indicator is rendered before any other IME windows because it is an element that is always displayed.</span></span> <span data-ttu-id="09310-360">Viene pertanto visualizzato sotto le altre finestre IME.</span><span class="sxs-lookup"><span data-stu-id="09310-360">It should therefore appear below other IME windows.</span></span> <span data-ttu-id="09310-361">CDXUTIMEEditBox esegue il rendering dell'indicatore chiamando il metodo RenderIndicator, in cui il colore del tipo di carattere dell'indicatore viene determinato esaminando la \_ variabile statica di proprietà, che riflette la modalità di conversione IME corrente.</span><span class="sxs-lookup"><span data-stu-id="09310-361">CDXUTIMEEditBox renders the indicator by calling the RenderIndicator method, in which the indicator font color is determined by examining the s\_ImeState static variable, which reflects the current IME conversion mode.</span></span> <span data-ttu-id="09310-362">Quando l'IME è abilitato e la conversione nativa è attiva, il metodo usa m \_ IndicatorImeColor come colore dell'indicatore.</span><span class="sxs-lookup"><span data-stu-id="09310-362">When the IME is enabled and native conversion is active, the method uses m\_IndicatorImeColor as the indicator color.</span></span> <span data-ttu-id="09310-363">Se l'IME è disabilitato o si trova in modalità di conversione non nativa, \_ viene usato m IndicatorImeColor per creare il testo dell'indicatore.</span><span class="sxs-lookup"><span data-stu-id="09310-363">If the IME is disabled or is in non-native conversion mode, m\_IndicatorImeColor is used to draw the indicator text.</span></span> <span data-ttu-id="09310-364">Per impostazione predefinita, la finestra indicatore viene disegnata a destra della casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-364">By default, the indicator window itself is drawn to the right of the edit box.</span></span> <span data-ttu-id="09310-365">Le applicazioni possono modificare questo comportamento eseguendo l'override del metodo RenderIndicator.</span><span class="sxs-lookup"><span data-stu-id="09310-365">Applications can change this behavior by overriding the RenderIndicator method.</span></span>

<span data-ttu-id="09310-366">Nella figura seguente vengono illustrati i diversi aspetti di un indicatore delle impostazioni locali di input per la lingua inglese, giapponese in modalità di conversione alfanumerica e giapponese in modalità di conversione nativa:</span><span class="sxs-lookup"><span data-stu-id="09310-366">The following figure shows the different appearances of an input locale indicator for English, Japanese in alphanumeric conversion mode, and Japanese in native conversion mode:</span></span>

![aspetti diversi di un indicatore delle impostazioni locali di input per l'inglese e il giapponese](images/ime-indicator.png)

### <a name="composition-window"></a><span data-ttu-id="09310-368">Finestra di composizione</span><span class="sxs-lookup"><span data-stu-id="09310-368">Composition Window</span></span>

<span data-ttu-id="09310-369">Il disegno della finestra di composizione viene gestito nel metodo RenderComposition di CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="09310-369">The drawing of the composition window is handled in the RenderComposition method of CDXUTIMEEditBox.</span></span> <span data-ttu-id="09310-370">La finestra di composizione viene spostata sopra la casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="09310-370">The composition window floats above the edit box.</span></span> <span data-ttu-id="09310-371">Deve essere disegnato in corrispondenza della posizione del cursore del controllo di modifica sottostante.</span><span class="sxs-lookup"><span data-stu-id="09310-371">It should be drawn at the cursor position of the underlying edit control.</span></span> <span data-ttu-id="09310-372">CDXUTIMEEditBox gestisce il rendering come segue:</span><span class="sxs-lookup"><span data-stu-id="09310-372">CDXUTIMEEditBox handles the rendering as follows:</span></span>

1.  <span data-ttu-id="09310-373">L'intera stringa di composizione viene disegnata utilizzando i colori predefiniti della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="09310-373">The entire composition string is drawn using the default composition string colors.</span></span>
2.  <span data-ttu-id="09310-374">I caratteri con determinati attributi speciali devono essere disegnati in colori diversi, quindi CDXUTIMEEditBox esamina i caratteri della stringa di composizione e controlla l'attributo della stringa.</span><span class="sxs-lookup"><span data-stu-id="09310-374">Characters with certain special attributes should be drawn in different colors, so CDXUTIMEEditBox reviews the characters of the composition string and inspects the string attribute.</span></span> <span data-ttu-id="09310-375">Se l'attributo richiede colori diversi, il carattere viene disegnato nuovamente con i colori appropriati.</span><span class="sxs-lookup"><span data-stu-id="09310-375">If the attribute calls for different colors, the character is drawn again with the appropriate colors.</span></span>
3.  <span data-ttu-id="09310-376">Il cursore della finestra di composizione viene disegnato per completare il rendering.</span><span class="sxs-lookup"><span data-stu-id="09310-376">The cursor of the composition window is drawn to complete the rendering.</span></span>

<span data-ttu-id="09310-377">Il cursore deve lampeggiare per gli IME coreano, ma non per altri IME.</span><span class="sxs-lookup"><span data-stu-id="09310-377">The cursor should blink for Korean IMEs, but it should not for other IMEs.</span></span> <span data-ttu-id="09310-378">RenderComposition determina se il cursore deve essere visibile in base ai valori del timer quando viene utilizzato l'IME coreano.</span><span class="sxs-lookup"><span data-stu-id="09310-378">RenderComposition determines whether the cursor should be visible based upon timer values when the Korean IME is used.</span></span>

### <a name="reading-and-candidate-windows"></a><span data-ttu-id="09310-379">Lettura e finestre candidate</span><span class="sxs-lookup"><span data-stu-id="09310-379">Reading and Candidate Windows</span></span>

<span data-ttu-id="09310-380">Il rendering delle finestre di lettura e candidato viene eseguito dallo stesso metodo CDXUTIMEEditBox, RenderCandidateReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="09310-380">The reading and candidate windows are rendered by the same CDXUTIMEEditBox method, RenderCandidateReadingWindow.</span></span> <span data-ttu-id="09310-381">Entrambe le finestre contengono una matrice di stringhe per il layout verticale o una singola stringa nel caso del layout orizzontale.</span><span class="sxs-lookup"><span data-stu-id="09310-381">Both windows contain an array of strings for vertical layout, or a single string in the case of horizontal layout.</span></span> <span data-ttu-id="09310-382">La maggior parte del codice in RenderCandidateReadingWindow viene utilizzata per posizionare la finestra in modo che nessuna parte della finestra venga ritagliata all'esterno della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="09310-382">The bulk of the code in RenderCandidateReadingWindow is used to position the window so that no part of the window falls outside the application window and gets clipped.</span></span>

## <a name="limitations"></a><span data-ttu-id="09310-383">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="09310-383">Limitations</span></span>

<span data-ttu-id="09310-384">Gli IME talvolta contengono funzionalità avanzate per migliorare la facilità di inserimento del testo.</span><span class="sxs-lookup"><span data-stu-id="09310-384">IMEs sometimes contain advanced features to improve the ease of inputting text.</span></span> <span data-ttu-id="09310-385">Alcune delle funzionalità disponibili negli IME più recenti sono illustrate nelle figure seguenti.</span><span class="sxs-lookup"><span data-stu-id="09310-385">Some of the features found in newer IMEs are shown in the following figures.</span></span> <span data-ttu-id="09310-386">Queste funzionalità avanzate non sono presenti in DXUT.</span><span class="sxs-lookup"><span data-stu-id="09310-386">These advanced features are not present in DXUT.</span></span> <span data-ttu-id="09310-387">L'implementazione del supporto per queste funzionalità avanzate può risultare complessa perché non è stata definita alcuna interfaccia per ottenere le informazioni necessarie dagli IME.</span><span class="sxs-lookup"><span data-stu-id="09310-387">Implementing support for these advanced features can be challenging because there is no interface defined to obtain the necessary information from the IMEs.</span></span>

<span data-ttu-id="09310-388">IME cinese tradizionale avanzato con elenco di candidati espanso:</span><span class="sxs-lookup"><span data-stu-id="09310-388">Advanced Traditional Chinese IME with expanded candidate list:</span></span>

![IME cinese tradizionale avanzato con elenco di candidati espanso](images/ime-advanced1.png)

<span data-ttu-id="09310-390">IME giapponese avanzato con alcune voci candidate contenenti testo aggiuntivo per descrivere i loro significati:</span><span class="sxs-lookup"><span data-stu-id="09310-390">Advanced Japanese IME with some candidate entries that contain additional text to describe their meanings:</span></span>

![IME giapponese avanzato con alcune voci candidate che contengono testo aggiuntivo per descrivere i significati](images/ime-advanced2.png)

<span data-ttu-id="09310-392">IME coreano avanzato che include un sistema di riconoscimento della grafia:</span><span class="sxs-lookup"><span data-stu-id="09310-392">Advanced Korean IME that includes a handwriting recognition system:</span></span>

![IME coreano avanzato che include un sistema di riconoscimento della grafia](images/ime-advanced3.png)

## <a name="registry-information"></a><span data-ttu-id="09310-394">Informazioni registro di sistema</span><span class="sxs-lookup"><span data-stu-id="09310-394">Registry Information</span></span>

<span data-ttu-id="09310-395">Le seguenti informazioni del registro di sistema vengono verificate per determinare l'orientamento della finestra di lettura, quando l'IME corrente è un nuovo fonetico precedente, che non implementa GetReadingString ().</span><span class="sxs-lookup"><span data-stu-id="09310-395">The following registry information is checked to determine the orientation of the reading window, when the current IME is older CHT New Phonetic that doesn't implement GetReadingString().</span></span>



| <span data-ttu-id="09310-396">Chiave</span><span class="sxs-lookup"><span data-stu-id="09310-396">Key</span></span>                                                           | <span data-ttu-id="09310-397">Valore</span><span class="sxs-lookup"><span data-stu-id="09310-397">Value</span></span>            |
|---------------------------------------------------------------|------------------|
| <span data-ttu-id="09310-398">HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ IME \_ nome</span><span class="sxs-lookup"><span data-stu-id="09310-398">HKCU\\software\\microsoft\\windows\\currentversion\\IME\_Name</span></span> | <span data-ttu-id="09310-399">mappatura della tastiera</span><span class="sxs-lookup"><span data-stu-id="09310-399">keyboard mapping</span></span> |



 

<span data-ttu-id="09310-400">Dove: \_ il nome IME è MSTCIPH se la versione del file IME è 5,1 o successiva; in caso contrario, il \_ nome IME è tintlgnt.</span><span class="sxs-lookup"><span data-stu-id="09310-400">Where: IME\_Name is MSTCIPH if the IME file version is 5.1 or later; otherwise IME\_Name is TINTLGNT.</span></span>

<span data-ttu-id="09310-401">L'orientamento della finestra di lettura è orizzontale se uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="09310-401">The orientation of reading window is horizontal if either:</span></span>

-   <span data-ttu-id="09310-402">L'IME è la versione 5,0 e il valore di mappatura della tastiera è 0x22 o 0x23</span><span class="sxs-lookup"><span data-stu-id="09310-402">The IME is version 5.0 and keyboard mapping value is 0x22 or 0x23</span></span>
-   <span data-ttu-id="09310-403">L'IME è la versione 5,1 o la versione 5,2 e il valore di mappatura della tastiera è 0x22, 0x23 o 0x24.</span><span class="sxs-lookup"><span data-stu-id="09310-403">The IME is version 5.1 or version 5.2 and keyboard mapping value is 0x22, 0x23 or 0x24.</span></span>

<span data-ttu-id="09310-404">Se nessuna delle due condizioni viene soddisfatta, la finestra di lettura è verticale.</span><span class="sxs-lookup"><span data-stu-id="09310-404">If neither condition is met, the reading window is vertical.</span></span>

## <a name="appendix-a-cht-versions-per-operating-system"></a><span data-ttu-id="09310-405">Appendice A: versioni CHT per sistema operativo</span><span class="sxs-lookup"><span data-stu-id="09310-405">Appendix A: CHT Versions per Operating System</span></span>



| <span data-ttu-id="09310-406">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="09310-406">Operating System</span></span>           | <span data-ttu-id="09310-407">Versione IME di CHT</span><span class="sxs-lookup"><span data-stu-id="09310-407">CHT IME Version</span></span> |
|----------------------------|-----------------|
| <span data-ttu-id="09310-408">Windows 98</span><span class="sxs-lookup"><span data-stu-id="09310-408">Windows 98</span></span>                 | <span data-ttu-id="09310-409">4.2</span><span class="sxs-lookup"><span data-stu-id="09310-409">4.2</span></span>             |
| <span data-ttu-id="09310-410">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="09310-410">Windows 2000</span></span>               | <span data-ttu-id="09310-411">4.3</span><span class="sxs-lookup"><span data-stu-id="09310-411">4.3</span></span>             |
| <span data-ttu-id="09310-412">unknown</span><span class="sxs-lookup"><span data-stu-id="09310-412">unknown</span></span>                    | <span data-ttu-id="09310-413">4.4</span><span class="sxs-lookup"><span data-stu-id="09310-413">4.4</span></span>             |
| <span data-ttu-id="09310-414">Windows ME</span><span class="sxs-lookup"><span data-stu-id="09310-414">Windows ME</span></span>                 | <span data-ttu-id="09310-415">5.0</span><span class="sxs-lookup"><span data-stu-id="09310-415">5.0</span></span>             |
| <span data-ttu-id="09310-416">Office XP</span><span class="sxs-lookup"><span data-stu-id="09310-416">Office XP</span></span>                  | <span data-ttu-id="09310-417">5.1</span><span class="sxs-lookup"><span data-stu-id="09310-417">5.1</span></span>             |
| <span data-ttu-id="09310-418">Windows XP</span><span class="sxs-lookup"><span data-stu-id="09310-418">Windows XP</span></span>                 | <span data-ttu-id="09310-419">5,2</span><span class="sxs-lookup"><span data-stu-id="09310-419">5.2</span></span>             |
| <span data-ttu-id="09310-420">Downloadble Web autonome</span><span class="sxs-lookup"><span data-stu-id="09310-420">Standalone web downloadble</span></span> | <span data-ttu-id="09310-421">6.0</span><span class="sxs-lookup"><span data-stu-id="09310-421">6.0</span></span>             |



 

## <a name="further-information"></a><span data-ttu-id="09310-422">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="09310-422">Further Information</span></span>

<span data-ttu-id="09310-423">Per ulteriori informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="09310-423">For additional information, see the following:</span></span>

-   [<span data-ttu-id="09310-424">Installazione e utilizzo degli editor del metodo di input</span><span class="sxs-lookup"><span data-stu-id="09310-424">Installing and Using Input Method Editors</span></span>](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [<span data-ttu-id="09310-425">Visualizzazione del testo internazionale</span><span class="sxs-lookup"><span data-stu-id="09310-425">International Text Display</span></span>](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [<span data-ttu-id="09310-426">Il Consorzio Unicode</span><span class="sxs-lookup"><span data-stu-id="09310-426">The Unicode Consortium</span></span>](https://www.unicode.org/)
-   <span data-ttu-id="09310-427">Sviluppo di software internazionale.</span><span class="sxs-lookup"><span data-stu-id="09310-427">Developing International Software.</span></span> <span data-ttu-id="09310-428">Dr. International.</span><span class="sxs-lookup"><span data-stu-id="09310-428">Dr. International.</span></span> <span data-ttu-id="09310-429">secondo ed.</span><span class="sxs-lookup"><span data-stu-id="09310-429">2nd ed.</span></span> <span data-ttu-id="09310-430">Redmond, WA: Microsoft Press, 2003.</span><span class="sxs-lookup"><span data-stu-id="09310-430">Redmond, WA: Microsoft Press, 2003.</span></span>

## <a name="getreadingstring"></a><span data-ttu-id="09310-431">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="09310-431">GetReadingString</span></span>

<span data-ttu-id="09310-432">Ottiene informazioni sulla stringa di lettura.</span><span class="sxs-lookup"><span data-stu-id="09310-432">Gets reading string information.</span></span>

<span data-ttu-id="09310-433">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="09310-433">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="09310-434"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="09310-434"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="09310-435">\[nel \] contesto di input.</span><span class="sxs-lookup"><span data-stu-id="09310-435">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="09310-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span><span class="sxs-lookup"><span data-stu-id="09310-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span></span>
</dt> <dd>

<span data-ttu-id="09310-437">\[\]lunghezza di lpwReadingBuf in WCHAR.</span><span class="sxs-lookup"><span data-stu-id="09310-437">\[in\] Length of lpwReadingBuf, in WCHAR.</span></span> <span data-ttu-id="09310-438">Se è zero, indica la lunghezza del buffer di lettura della query.</span><span class="sxs-lookup"><span data-stu-id="09310-438">If it is zero, it means query reading buffer length.</span></span>

</dd> <dt>

<span data-ttu-id="09310-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span><span class="sxs-lookup"><span data-stu-id="09310-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span></span> 
</dt> <dd>

<span data-ttu-id="09310-440">\[out \] restituisce la stringa di lettura (non zero end).</span><span class="sxs-lookup"><span data-stu-id="09310-440">\[out\] Return reading string (not zero end).</span></span>

</dd> <dt>

<span data-ttu-id="09310-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span><span class="sxs-lookup"><span data-stu-id="09310-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="09310-442">\[out \] restituisce l'indice del carattere di errore nella stringa di lettura se è presente.</span><span class="sxs-lookup"><span data-stu-id="09310-442">\[out\] Return index of error character in the reading string if there is.</span></span>

</dd> <dt>

<span data-ttu-id="09310-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span><span class="sxs-lookup"><span data-stu-id="09310-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span></span> 
</dt> <dd>

<span data-ttu-id="09310-444">\[\]se è true, la lettura dell'interfaccia utente è verticale.</span><span class="sxs-lookup"><span data-stu-id="09310-444">\[out\] If it is TRUE, reading UI is vertical.</span></span> <span data-ttu-id="09310-445">In caso contrario, puMaxReadingLen orizzontali.</span><span class="sxs-lookup"><span data-stu-id="09310-445">Otherwise, horizontal puMaxReadingLen.</span></span>

</dd> <dt>

<span data-ttu-id="09310-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span><span class="sxs-lookup"><span data-stu-id="09310-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span></span> 
</dt> <dd>

<span data-ttu-id="09310-447">\[\]lunghezza dell'interfaccia utente di lettura.</span><span class="sxs-lookup"><span data-stu-id="09310-447">\[out\] The reading UI length.</span></span> <span data-ttu-id="09310-448">La lunghezza massima di lettura non è fissa; dipende non solo dal layout della tastiera, ma anche dalla modalità di input (ad esempio, codice interno, input surrogato).</span><span class="sxs-lookup"><span data-stu-id="09310-448">The max reading length is not fixed; it depends not only on keyboard layout, but also on input mode (for example, internal code, surrogate input).</span></span>

</dd> </dl>

<span data-ttu-id="09310-449">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="09310-449">**Return Values**</span></span>

<span data-ttu-id="09310-450">Lunghezza della stringa di lettura.</span><span class="sxs-lookup"><span data-stu-id="09310-450">The reading string length.</span></span>

<span data-ttu-id="09310-451">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="09310-451">**Remarks**</span></span>

<span data-ttu-id="09310-452">Se il valore restituito è maggiore del valore di uReadingBufLen, tutti i parametri di output non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="09310-452">If the return value is greater than the value of uReadingBufLen, then all output parameters are undefined.</span></span>

<span data-ttu-id="09310-453">Questa funzione è implementata in CHT IME 6,0 o versioni successive e può essere acquisita da GetProcAddress in un handle del modulo IME. l'handle del modulo IME può essere acquisito da ImmGetIMEFileName e LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="09310-453">This function is implemented in CHT IME 6.0 or later, and can be acquired by GetProcAddress on an IME module handle; the IME module handle can be acquired by ImmGetIMEFileName and LoadLibrary.</span></span>

<span data-ttu-id="09310-454">**Requisiti**</span><span class="sxs-lookup"><span data-stu-id="09310-454">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="09310-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="09310-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="09310-456">Dichiarata in Imm. h.</span><span class="sxs-lookup"><span data-stu-id="09310-456">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="09310-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Libreria di importazione**</span><span class="sxs-lookup"><span data-stu-id="09310-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="09310-458">Usare Imm. lib.</span><span class="sxs-lookup"><span data-stu-id="09310-458">Use Imm.lib.</span></span>

</dd> </dl>

## <a name="showreadingwindow"></a><span data-ttu-id="09310-459">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="09310-459">ShowReadingWindow</span></span>

<span data-ttu-id="09310-460">Mostra (o Nascondi) la finestra di lettura.</span><span class="sxs-lookup"><span data-stu-id="09310-460">Show (or hide) the reading window.</span></span>

<span data-ttu-id="09310-461">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="09310-461">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="09310-462"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="09310-462"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="09310-463">\[nel \] contesto di input.</span><span class="sxs-lookup"><span data-stu-id="09310-463">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="09310-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="09310-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span></span> 
</dt> <dd>

<span data-ttu-id="09310-465">\[in \] impostare su true per visualizzare la finestra di lettura (o false per nasconderla).</span><span class="sxs-lookup"><span data-stu-id="09310-465">\[in\] Set to TRUE to show the reading window (or FALSE to hide it).</span></span>

</dd> </dl>

<span data-ttu-id="09310-466">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="09310-466">**Return Values**</span></span>

<span data-ttu-id="09310-467">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="09310-467">**Remarks**</span></span>

<span data-ttu-id="09310-468">Restituisce TRUE se ha esito positivo o FALSE in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="09310-468">Return TRUE if successful or FALSE if otherwise.</span></span>

<span data-ttu-id="09310-469">**Requisiti**</span><span class="sxs-lookup"><span data-stu-id="09310-469">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="09310-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="09310-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="09310-471">Dichiarata in Imm. h.</span><span class="sxs-lookup"><span data-stu-id="09310-471">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="09310-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Libreria di importazione**</span><span class="sxs-lookup"><span data-stu-id="09310-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="09310-473">Usare Imm. lib.</span><span class="sxs-lookup"><span data-stu-id="09310-473">Use Imm.lib.</span></span>

</dd> </dl>