---
title: Input da tastiera (introduzione a Win32 e C++)
description: Input da tastiera
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "106320255"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a><span data-ttu-id="e0066-103">Input da tastiera (introduzione a Win32 e C++)</span><span class="sxs-lookup"><span data-stu-id="e0066-103">Keyboard Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="e0066-104">La tastiera viene utilizzata per diversi tipi distinti di input, tra cui:</span><span class="sxs-lookup"><span data-stu-id="e0066-104">The keyboard is used for several distinct types of input, including:</span></span>

-   <span data-ttu-id="e0066-105">Input di caratteri.</span><span class="sxs-lookup"><span data-stu-id="e0066-105">Character input.</span></span> <span data-ttu-id="e0066-106">Testo che l'utente digita in un documento o in una casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="e0066-106">Text that the user types into a document or edit box.</span></span>
-   <span data-ttu-id="e0066-107">Tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e0066-107">Keyboard shortcuts.</span></span> <span data-ttu-id="e0066-108">Tratti chiave che richiamano le funzioni dell'applicazione; ad esempio, CTRL + O per aprire un file.</span><span class="sxs-lookup"><span data-stu-id="e0066-108">Key strokes that invoke application functions; for example, CTRL + O to open a file.</span></span>
-   <span data-ttu-id="e0066-109">Comandi di sistema.</span><span class="sxs-lookup"><span data-stu-id="e0066-109">System commands.</span></span> <span data-ttu-id="e0066-110">Tratti chiave che richiamano funzioni di sistema; ad esempio, ALT + TAB per passare a Windows.</span><span class="sxs-lookup"><span data-stu-id="e0066-110">Key strokes that invoke system functions; for example, ALT + TAB to switch windows.</span></span>

<span data-ttu-id="e0066-111">Quando si pensa all'input da tastiera, è importante ricordare che un tratto di chiave non è uguale a un carattere.</span><span class="sxs-lookup"><span data-stu-id="e0066-111">When thinking about keyboard input, it is important to remember that a key stroke is not the same as a character.</span></span> <span data-ttu-id="e0066-112">Ad esempio, la pressione di un tasto può causare uno dei caratteri seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0066-112">For example, pressing the A key could result in any of the following characters.</span></span>

-   <span data-ttu-id="e0066-113">a</span><span class="sxs-lookup"><span data-stu-id="e0066-113">a</span></span>
-   <span data-ttu-id="e0066-114">A</span><span class="sxs-lookup"><span data-stu-id="e0066-114">A</span></span>
-   <span data-ttu-id="e0066-115">á (se la tastiera supporta la combinazione dei segni diacritici)</span><span class="sxs-lookup"><span data-stu-id="e0066-115">á (if the keyboard supports combining diacritics)</span></span>

<span data-ttu-id="e0066-116">Inoltre, se il tasto ALT è premuto, premendo il tasto A viene prodotto ALT + A, che il sistema non considera come un carattere, ma piuttosto come un comando di sistema.</span><span class="sxs-lookup"><span data-stu-id="e0066-116">Further, if the ALT key is held down, pressing the A key produces ALT+A, which the system does not treat as a character at all, but rather as a system command.</span></span>

## <a name="key-codes"></a><span data-ttu-id="e0066-117">Codici chiave</span><span class="sxs-lookup"><span data-stu-id="e0066-117">Key Codes</span></span>

<span data-ttu-id="e0066-118">Quando si preme un tasto, l'hardware genera un *codice di analisi*.</span><span class="sxs-lookup"><span data-stu-id="e0066-118">When you press a key, the hardware generates a *scan code*.</span></span> <span data-ttu-id="e0066-119">I codici di analisi variano da una tastiera all'altra e sono disponibili codici di analisi distinti per gli eventi di chiave e di discesa.</span><span class="sxs-lookup"><span data-stu-id="e0066-119">Scan codes vary from one keyboard to the next, and there are separate scan codes for key-up and key-down events.</span></span> <span data-ttu-id="e0066-120">I codici di analisi non vengono mai interessati.</span><span class="sxs-lookup"><span data-stu-id="e0066-120">You will almost never care about scan codes.</span></span> <span data-ttu-id="e0066-121">Il driver della tastiera converte i codici di analisi in *codici chiave virtuale*.</span><span class="sxs-lookup"><span data-stu-id="e0066-121">The keyboard driver translates scan codes into *virtual-key codes*.</span></span> <span data-ttu-id="e0066-122">I codici delle chiavi virtuali sono indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0066-122">Virtual-key codes are device-independent.</span></span> <span data-ttu-id="e0066-123">Premendo il tasto A su qualsiasi tastiera viene generato lo stesso codice di chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0066-123">Pressing the A key on any keyboard generates the same virtual-key code.</span></span>

<span data-ttu-id="e0066-124">In generale, i codici delle chiavi virtuali non corrispondono a codici ASCII o a qualsiasi altro standard di codifica dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="e0066-124">In general, virtual-key codes do not correspond to ASCII codes or any other character-encoding standard.</span></span> <span data-ttu-id="e0066-125">Si tratta di un'operazione ovvia, perché la stessa chiave può generare caratteri diversi (a, A, á) e alcune chiavi, ad esempio i tasti funzione, non corrispondono a nessun carattere.</span><span class="sxs-lookup"><span data-stu-id="e0066-125">This is obvious if you think about it, because the same key can generate different characters (a, A, á), and some keys, such as function keys, do not correspond to any character.</span></span>

<span data-ttu-id="e0066-126">Detto ciò, i codici a chiave virtuale seguenti eseguono il mapping agli equivalenti ASCII:</span><span class="sxs-lookup"><span data-stu-id="e0066-126">That said, the following virtual-key codes do map to ASCII equivalents:</span></span>

-   <span data-ttu-id="e0066-127">da 0 a 9 chiavi = ASCII ' 0' –' 9' (0x30 – 0x39)</span><span class="sxs-lookup"><span data-stu-id="e0066-127">0 through 9 keys = ASCII '0' – '9' (0x30 – 0x39)</span></span>
-   <span data-ttu-id="e0066-128">Da a a Z chiavi = ASCII ' A '-' Z ' (0x41 – 0x5A)</span><span class="sxs-lookup"><span data-stu-id="e0066-128">A through Z keys = ASCII 'A' – 'Z' (0x41 – 0x5A)</span></span>

<span data-ttu-id="e0066-129">Per alcuni aspetti, questo mapping è sfortunato, perché i codici di chiave virtuale non devono mai essere considerati come caratteri, per i motivi illustrati.</span><span class="sxs-lookup"><span data-stu-id="e0066-129">In some respects this mapping is unfortunate, because you should never think of virtual-key codes as characters, for the reasons discussed.</span></span>

<span data-ttu-id="e0066-130">Il file di intestazione WinUser. h definisce le costanti per la maggior parte dei codici della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0066-130">The header file WinUser.h defines constants for most of the virtual-key codes.</span></span> <span data-ttu-id="e0066-131">Ad esempio, il codice della chiave virtuale per il tasto freccia sinistra è **VK \_ Left** (0x25).</span><span class="sxs-lookup"><span data-stu-id="e0066-131">For example, the virtual-key code for the LEFT ARROW key is **VK\_LEFT** (0x25).</span></span> <span data-ttu-id="e0066-132">Per l'elenco completo dei codici delle chiavi virtuali, vedere [**codici chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="e0066-132">For the complete list of virtual-key codes, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="e0066-133">Non sono definite costanti per i codici chiave virtuale che corrispondono ai valori ASCII.</span><span class="sxs-lookup"><span data-stu-id="e0066-133">No constants are defined for the virtual-key codes that match ASCII values.</span></span> <span data-ttu-id="e0066-134">Il codice della chiave virtuale per la chiave A è ad esempio 0x41, ma non esiste una costante denominata **VK \_ A**.</span><span class="sxs-lookup"><span data-stu-id="e0066-134">For example, the virtual-key code for the A key is 0x41, but there is no constant named **VK\_A**.</span></span> <span data-ttu-id="e0066-135">In alternativa, è sufficiente usare il valore numerico.</span><span class="sxs-lookup"><span data-stu-id="e0066-135">Instead, just use the numeric value.</span></span>

## <a name="key-down-and-key-up-messages"></a><span data-ttu-id="e0066-136">Messaggi di Key-Down e Key-Up</span><span class="sxs-lookup"><span data-stu-id="e0066-136">Key-Down and Key-Up Messages</span></span>

<span data-ttu-id="e0066-137">Quando si preme un tasto, la finestra con lo stato attivo della tastiera riceve uno dei messaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0066-137">When you press a key, the window that has keyboard focus receives one of the following messages.</span></span>

-   [<span data-ttu-id="e0066-138">**\_SYSKEYDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="e0066-138">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
-   [<span data-ttu-id="e0066-139">**KeyDown di WM \_**</span><span class="sxs-lookup"><span data-stu-id="e0066-139">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)

<span data-ttu-id="e0066-140">Il messaggio [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) indica una *chiave di sistema*, ovvero un tratto di chiave che richiama un comando di sistema.</span><span class="sxs-lookup"><span data-stu-id="e0066-140">The [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message indicates a *system key*, which is a key stroke that invokes a system command.</span></span> <span data-ttu-id="e0066-141">Esistono due tipi di chiave di sistema:</span><span class="sxs-lookup"><span data-stu-id="e0066-141">There are two types of system key:</span></span>

-   <span data-ttu-id="e0066-142">ALT + qualsiasi tasto</span><span class="sxs-lookup"><span data-stu-id="e0066-142">ALT + any key</span></span>
-   <span data-ttu-id="e0066-143">F10</span><span class="sxs-lookup"><span data-stu-id="e0066-143">F10</span></span>

<span data-ttu-id="e0066-144">Il tasto F10 attiva la barra dei menu di una finestra.</span><span class="sxs-lookup"><span data-stu-id="e0066-144">The F10 key activates the menu bar of a window.</span></span> <span data-ttu-id="e0066-145">Diverse combinazioni di tasti ALT richiamano i comandi di sistema.</span><span class="sxs-lookup"><span data-stu-id="e0066-145">Various ALT-key combinations invoke system commands.</span></span> <span data-ttu-id="e0066-146">Ad esempio, ALT + TAB passa a una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="e0066-146">For example, ALT + TAB switches to a new window.</span></span> <span data-ttu-id="e0066-147">Inoltre, se una finestra dispone di un menu, è possibile utilizzare il tasto ALT per attivare le voci di menu.</span><span class="sxs-lookup"><span data-stu-id="e0066-147">In addition, if a window has a menu, the ALT key can be used to activate menu items.</span></span> <span data-ttu-id="e0066-148">Alcune combinazioni di tasti ALT non eseguono alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="e0066-148">Some ALT key combinations do not do anything.</span></span>

<span data-ttu-id="e0066-149">Tutti gli altri tratti chiave sono considerati chiavi non di sistema e producono il messaggio del [**\_ KeyDown di WM**](/windows/desktop/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="e0066-149">All other key strokes are considered nonsystem keys and produce the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span> <span data-ttu-id="e0066-150">Sono inclusi i tasti funzione diversi da F10.</span><span class="sxs-lookup"><span data-stu-id="e0066-150">This includes the function keys other than F10.</span></span>

<span data-ttu-id="e0066-151">Quando si rilascia un tasto, il sistema invia un messaggio di chiave corrispondente:</span><span class="sxs-lookup"><span data-stu-id="e0066-151">When you release a key, the system sends a corresponding key-up message:</span></span>

-   [<span data-ttu-id="e0066-152">**KEYUP di WM \_**</span><span class="sxs-lookup"><span data-stu-id="e0066-152">**WM\_KEYUP**</span></span>](/windows/desktop/inputdev/wm-keyup)
-   [<span data-ttu-id="e0066-153">**\_SYSKEYUP WM**</span><span class="sxs-lookup"><span data-stu-id="e0066-153">**WM\_SYSKEYUP**</span></span>](/windows/desktop/inputdev/wm-syskeyup)

<span data-ttu-id="e0066-154">Se si tiene premuto un tasto sufficientemente lungo per avviare la funzionalità di ripetizione della tastiera, il sistema invia più messaggi di chiave, seguiti da un singolo messaggio di chiave.</span><span class="sxs-lookup"><span data-stu-id="e0066-154">If you hold down a key long enough to start the keyboard's repeat feature, the system sends multiple key-down messages, followed by a single key-up message.</span></span>

<span data-ttu-id="e0066-155">In tutti e quattro i messaggi della tastiera discussi finora, il parametro *wParam* contiene il codice della chiave virtuale della chiave.</span><span class="sxs-lookup"><span data-stu-id="e0066-155">In all four of the keyboard messages discussed so far, the *wParam* parameter contains the virtual-key code of the key.</span></span> <span data-ttu-id="e0066-156">Il parametro *lParam* contiene alcune informazioni varie compresse in 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e0066-156">The *lParam* parameter contains some miscellaneous information packed into 32 bits.</span></span> <span data-ttu-id="e0066-157">In genere non sono necessarie le informazioni in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="e0066-157">You typically do not need the information in *lParam*.</span></span> <span data-ttu-id="e0066-158">Un flag che può essere utile è il bit 30, il flag "stato della chiave precedente", che è impostato su 1 per i messaggi di chiave inattivo ripetuti.</span><span class="sxs-lookup"><span data-stu-id="e0066-158">One flag that might be useful is bit 30, the "previous key state" flag, which is set to 1 for repeated key-down messages.</span></span>

<span data-ttu-id="e0066-159">Come suggerisce il nome, i tratti chiave di sistema sono destinati principalmente all'uso da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e0066-159">As the name implies, system key strokes are primarily intended for use by the operating system.</span></span> <span data-ttu-id="e0066-160">Se si intercetta il messaggio [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) , chiamare [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) in seguito.</span><span class="sxs-lookup"><span data-stu-id="e0066-160">If you intercept the [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message, call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) afterward.</span></span> <span data-ttu-id="e0066-161">In caso contrario, il sistema operativo non riuscirà a gestire il comando.</span><span class="sxs-lookup"><span data-stu-id="e0066-161">Otherwise, you will block the operating system from handling the command.</span></span>

## <a name="character-messages"></a><span data-ttu-id="e0066-162">Messaggi di tipo carattere</span><span class="sxs-lookup"><span data-stu-id="e0066-162">Character Messages</span></span>

<span data-ttu-id="e0066-163">I tratti chiave vengono convertiti in caratteri dalla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , che è stata esaminata prima nel [modulo 1](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="e0066-163">Key strokes are converted into characters by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function, which we first saw in [Module 1](your-first-windows-program.md).</span></span> <span data-ttu-id="e0066-164">Questa funzione esamina i messaggi di chiave e li converte in caratteri.</span><span class="sxs-lookup"><span data-stu-id="e0066-164">This function examines key-down messages and translates them into characters.</span></span> <span data-ttu-id="e0066-165">Per ogni carattere prodotto, la funzione **TranslateMessage** inserisce un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) o [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) nella coda di messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="e0066-165">For each character that is produced, the **TranslateMessage** function puts a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) or [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message on the message queue of the window.</span></span> <span data-ttu-id="e0066-166">Il parametro *wParam* del messaggio contiene il carattere UTF-16.</span><span class="sxs-lookup"><span data-stu-id="e0066-166">The *wParam* parameter of the message contains the UTF-16 character.</span></span>

<span data-ttu-id="e0066-167">Come si può immaginare, i messaggi [**WM \_ char**](/windows/desktop/inputdev/wm-char) vengono generati da messaggi di [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) , mentre i messaggi [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) vengono generati da messaggi [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) .</span><span class="sxs-lookup"><span data-stu-id="e0066-167">As you might guess, [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages are generated from [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, while [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) messages are generated from [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) messages.</span></span> <span data-ttu-id="e0066-168">Si supponga, ad esempio, che l'utente prema il tasto MAIUSC seguito da un tasto A.</span><span class="sxs-lookup"><span data-stu-id="e0066-168">For example, suppose the user presses the SHIFT key followed by the A key.</span></span> <span data-ttu-id="e0066-169">Supponendo un layout di tastiera standard, si otterrebbe la seguente sequenza di messaggi:</span><span class="sxs-lookup"><span data-stu-id="e0066-169">Assuming a standard keyboard layout, you would get the following sequence of messages:</span></span>

<span data-ttu-id="e0066-170">**WM \_ KEYDOWN**: MAIUSC</span><span class="sxs-lookup"><span data-stu-id="e0066-170">**WM\_KEYDOWN**: SHIFT</span></span>  
<span data-ttu-id="e0066-171">**WM \_ KEYDOWN**: A</span><span class="sxs-lookup"><span data-stu-id="e0066-171">**WM\_KEYDOWN**: A</span></span>  
<span data-ttu-id="e0066-172">**WM \_ CHAR**:' A '</span><span class="sxs-lookup"><span data-stu-id="e0066-172">**WM\_CHAR**: 'A'</span></span>  


<span data-ttu-id="e0066-173">D'altra parte, la combinazione ALT + P genererebbe:</span><span class="sxs-lookup"><span data-stu-id="e0066-173">On the other hand, the combination ALT + P would generate:</span></span>

 <span data-ttu-id="e0066-174">**WM \_ SYSKEYDOWN**: \_ menu VK</span><span class="sxs-lookup"><span data-stu-id="e0066-174">**WM\_SYSKEYDOWN**: VK\_MENU</span></span>  
<span data-ttu-id="e0066-175">**WM \_ SYSKEYDOWN**: 0x50</span><span class="sxs-lookup"><span data-stu-id="e0066-175">**WM\_SYSKEYDOWN**: 0x50</span></span>  
<span data-ttu-id="e0066-176">**WM \_ SYSCHAR**: "p"</span><span class="sxs-lookup"><span data-stu-id="e0066-176">**WM\_SYSCHAR**: 'p'</span></span>  
<span data-ttu-id="e0066-177">**WM \_ SYSKEYUP**: 0x50</span><span class="sxs-lookup"><span data-stu-id="e0066-177">**WM\_SYSKEYUP**: 0x50</span></span>  
<span data-ttu-id="e0066-178">**WM \_ MENU KEYUP**: VK \_</span><span class="sxs-lookup"><span data-stu-id="e0066-178">**WM\_KEYUP**: VK\_MENU</span></span>  


<span data-ttu-id="e0066-179">Il codice della chiave virtuale per il tasto ALT è denominato VK \_ MENU per motivi cronologici.)</span><span class="sxs-lookup"><span data-stu-id="e0066-179">(The virtual-key code for the ALT key is named VK\_MENU for historical reasons.)</span></span>

<span data-ttu-id="e0066-180">Il messaggio [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) indica un carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="e0066-180">The [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message indicates a system character.</span></span> <span data-ttu-id="e0066-181">Come per [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), in genere è necessario passare questo messaggio direttamente a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="e0066-181">As with [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), you should generally pass this message directly to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="e0066-182">In caso contrario, è possibile interferire con i comandi di sistema standard.</span><span class="sxs-lookup"><span data-stu-id="e0066-182">Otherwise, you may interfere with standard system commands.</span></span> <span data-ttu-id="e0066-183">In particolare, non considerare **WM \_ SYSCHAR** come testo digitato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e0066-183">In particular, do not treat **WM\_SYSCHAR** as text that the user has typed.</span></span>

<span data-ttu-id="e0066-184">Il messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) è quello che si considera normalmente come input di caratteri.</span><span class="sxs-lookup"><span data-stu-id="e0066-184">The [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message is what you normally think of as character input.</span></span> <span data-ttu-id="e0066-185">Il tipo di dati per il carattere è **WCHAR \_ t**, che rappresenta un carattere Unicode UTF-16.</span><span class="sxs-lookup"><span data-stu-id="e0066-185">The data type for the character is **wchar\_t**, representing a UTF-16 Unicode character.</span></span> <span data-ttu-id="e0066-186">L'input di caratteri può includere caratteri non compresi nell'intervallo ASCII, specialmente con i layout di tastiera utilizzati in genere all'esterno del Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="e0066-186">Character input can include characters outside the ASCII range, especially with keyboard layouts that are commonly used outside of the United States.</span></span> <span data-ttu-id="e0066-187">È possibile provare diversi layout di tastiera installando una tastiera a livello di area e quindi usando la funzionalità della tastiera su schermo.</span><span class="sxs-lookup"><span data-stu-id="e0066-187">You can try different keyboard layouts by installing a regional keyboard and then using the On-Screen Keyboard feature.</span></span>

<span data-ttu-id="e0066-188">Gli utenti possono anche installare un IME (Input Method Editor) per immettere script complessi, ad esempio caratteri giapponesi, con una tastiera standard.</span><span class="sxs-lookup"><span data-stu-id="e0066-188">Users can also install an Input Method Editor (IME) to enter complex scripts, such as Japanese characters, with a standard keyboard.</span></span> <span data-ttu-id="e0066-189">Ad esempio, se si usa un IME giapponese per immettere il carattere katakana カ (KA), è possibile che vengano visualizzati i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0066-189">For example, using a Japanese IME to enter the katakana character カ (ka), you might get the following messages:</span></span>

<span data-ttu-id="e0066-190">**WM \_ KEYDOWN**: VK \_ PROCESSKEY (chiave di processo IME)</span><span class="sxs-lookup"><span data-stu-id="e0066-190">**WM\_KEYDOWN**: VK\_PROCESSKEY (the IME PROCESS key)</span></span>  
<span data-ttu-id="e0066-191">**WM \_ KEYUP**: 0x4B</span><span class="sxs-lookup"><span data-stu-id="e0066-191">**WM\_KEYUP**: 0x4B</span></span>  
<span data-ttu-id="e0066-192">**WM \_ KEYDOWN**: VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="e0066-192">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="e0066-193">**WM \_ KEYUP**: 0x41</span><span class="sxs-lookup"><span data-stu-id="e0066-193">**WM\_KEYUP**: 0x41</span></span>  
<span data-ttu-id="e0066-194">**WM \_ KEYDOWN**: VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="e0066-194">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="e0066-195">**WM \_ CHAR**: カ</span><span class="sxs-lookup"><span data-stu-id="e0066-195">**WM\_CHAR**: カ</span></span>  
<span data-ttu-id="e0066-196">**WM \_ KEYUP**: \_ risultato VK</span><span class="sxs-lookup"><span data-stu-id="e0066-196">**WM\_KEYUP**: VK\_RETURN</span></span>  


<span data-ttu-id="e0066-197">Alcune combinazioni di tasti CTRL vengono convertite in caratteri di controllo ASCII.</span><span class="sxs-lookup"><span data-stu-id="e0066-197">Some CTRL key combinations are translated into ASCII control characters.</span></span> <span data-ttu-id="e0066-198">Ad esempio, CTRL + A viene convertito nel carattere ASCII CTRL-A (SOH) (valore ASCII 0x01).</span><span class="sxs-lookup"><span data-stu-id="e0066-198">For example, CTRL+A is translated to the ASCII ctrl-A (SOH) character (ASCII value 0x01).</span></span> <span data-ttu-id="e0066-199">Per l'input di testo, è in genere necessario escludere i caratteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="e0066-199">For text input, you should generally filter out the control characters.</span></span> <span data-ttu-id="e0066-200">Evitare inoltre di usare [**WM \_ char**](/windows/desktop/inputdev/wm-char) per implementare i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e0066-200">Also, avoid using [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) to implement keyboard shortcuts.</span></span> <span data-ttu-id="e0066-201">Usare invece i messaggi di [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) oppure, ancora meglio, usare una tabella di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e0066-201">Instead, use [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages; or even better, use an accelerator table.</span></span> <span data-ttu-id="e0066-202">Le tabelle degli acceleratori sono descritte nell'argomento successivo, [tabelle di tasti di scelta rapida](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e0066-202">Accelerator tables are described in the next topic, [Accelerator Tables](accelerator-tables.md).</span></span>

<span data-ttu-id="e0066-203">Nel codice seguente vengono visualizzati i messaggi principali della tastiera nel debugger.</span><span class="sxs-lookup"><span data-stu-id="e0066-203">The following code displays the main keyboard messages in the debugger.</span></span> <span data-ttu-id="e0066-204">Provare a giocare con diverse combinazioni di tasti e vedere quali messaggi vengono generati.</span><span class="sxs-lookup"><span data-stu-id="e0066-204">Try playing with different keystroke combinations and see what messages are generated.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a><span data-ttu-id="e0066-205">Messaggi della tastiera vari</span><span class="sxs-lookup"><span data-stu-id="e0066-205">Miscellaneous Keyboard Messages</span></span>

<span data-ttu-id="e0066-206">Alcuni altri messaggi della tastiera possono essere ignorati in modo sicuro dalla maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e0066-206">Some other keyboard messages can safely be ignored by most applications.</span></span>

-   <span data-ttu-id="e0066-207">Il messaggio [**WM \_ DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) viene inviato per una chiave di combinazione, ad esempio un diacritici.</span><span class="sxs-lookup"><span data-stu-id="e0066-207">The [**WM\_DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) message is sent for a combining key, such as a diacritic.</span></span> <span data-ttu-id="e0066-208">Ad esempio, in una tastiera in lingua spagnola, digitando accento (') seguito da E viene prodotto il carattere è.</span><span class="sxs-lookup"><span data-stu-id="e0066-208">For example, on a Spanish language keyboard, typing accent (') followed by E produces the character é.</span></span> <span data-ttu-id="e0066-209">Il **\_ DEADCHAR WM** viene inviato per il carattere accentato.</span><span class="sxs-lookup"><span data-stu-id="e0066-209">The **WM\_DEADCHAR** is sent for the accent character.</span></span>
-   <span data-ttu-id="e0066-210">Il messaggio di [**WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e0066-210">The [**WM\_UNICHAR**](/windows/desktop/inputdev/wm-unichar) message is obsolete.</span></span> <span data-ttu-id="e0066-211">Consente ai programmi ANSI di ricevere input di caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="e0066-211">It enables ANSI programs to receive Unicode character input.</span></span>
-   <span data-ttu-id="e0066-212">Il carattere [**WM \_ IME \_ char**](/windows/desktop/Intl/wm-ime-char) viene inviato quando un IME converte una sequenza di tasti in caratteri.</span><span class="sxs-lookup"><span data-stu-id="e0066-212">The [**WM\_IME\_CHAR**](/windows/desktop/Intl/wm-ime-char) character is sent when an IME translates a keystroke sequence into characters.</span></span> <span data-ttu-id="e0066-213">Viene inviata oltre al normale messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="e0066-213">It is sent in addition to the usual [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>

## <a name="keyboard-state"></a><span data-ttu-id="e0066-214">Stato della tastiera</span><span class="sxs-lookup"><span data-stu-id="e0066-214">Keyboard State</span></span>

<span data-ttu-id="e0066-215">I messaggi della tastiera sono basati sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="e0066-215">The keyboard messages are event-driven.</span></span> <span data-ttu-id="e0066-216">Ovvero, viene visualizzato un messaggio quando si verifica un evento interessante, ad esempio la pressione di un tasto, e il messaggio indica cosa si è appena verificato.</span><span class="sxs-lookup"><span data-stu-id="e0066-216">That is, you get a message when something interesting happens, such as a key press, and the message tells you what just happened.</span></span> <span data-ttu-id="e0066-217">Tuttavia, è anche possibile testare lo stato di una chiave in qualsiasi momento, chiamando la funzione [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) .</span><span class="sxs-lookup"><span data-stu-id="e0066-217">But you can also test the state of a key at any time, by calling the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function.</span></span>

<span data-ttu-id="e0066-218">Si consideri ad esempio il modo in cui si rileva la combinazione di clic con il tasto sinistro del mouse + ALT.</span><span class="sxs-lookup"><span data-stu-id="e0066-218">For example, consider how would you detect the combination of left mouse click + ALT key.</span></span> <span data-ttu-id="e0066-219">È possibile tenere traccia dello stato del tasto ALT ascoltando i messaggi della sequenza di tasti e archiviando un flag, ma [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) Salva il problema.</span><span class="sxs-lookup"><span data-stu-id="e0066-219">You could track the state of the ALT key by listening for key-stroke messages and storing a flag, but [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) saves you the trouble.</span></span> <span data-ttu-id="e0066-220">Quando si riceve il messaggio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , è sufficiente chiamare **GetKeyState** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e0066-220">When you receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, just call **GetKeyState** as follows:</span></span>


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



<span data-ttu-id="e0066-221">Il messaggio [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) accetta come input un codice di chiave virtuale e restituisce un set di flag di bit, in realtà solo due flag.</span><span class="sxs-lookup"><span data-stu-id="e0066-221">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) message takes a virtual-key code as input and returns a set of bit flags (actually just two flags).</span></span> <span data-ttu-id="e0066-222">Il valore 0x8000 contiene il flag di bit che verifica se la chiave è attualmente premuta.</span><span class="sxs-lookup"><span data-stu-id="e0066-222">The value 0x8000 contains the bit flag that tests whether the key is currently pressed.</span></span>

<span data-ttu-id="e0066-223">La maggior parte delle tastiere dispone di due tasti ALT, a sinistra e a destra.</span><span class="sxs-lookup"><span data-stu-id="e0066-223">Most keyboards have two ALT keys, left and right.</span></span> <span data-ttu-id="e0066-224">Nell'esempio precedente viene verificato se uno di questi elementi è stato premuto.</span><span class="sxs-lookup"><span data-stu-id="e0066-224">The previous example tests whether either of them of pressed.</span></span> <span data-ttu-id="e0066-225">È anche possibile usare [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) per distinguere tra le istanze di sinistra e destra dei tasti ALT, MAIUSC o CTRL.</span><span class="sxs-lookup"><span data-stu-id="e0066-225">You can also use [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) to distinguish between the left and right instances of the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="e0066-226">Il codice seguente, ad esempio, verifica se viene premuto il tasto ALT destro.</span><span class="sxs-lookup"><span data-stu-id="e0066-226">For example, the following code tests if the right ALT key is pressed.</span></span>


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



<span data-ttu-id="e0066-227">La funzione [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) è interessante perché segnala uno stato della tastiera *virtuale* .</span><span class="sxs-lookup"><span data-stu-id="e0066-227">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function is interesting because it reports a *virtual* keyboard state.</span></span> <span data-ttu-id="e0066-228">Questo stato virtuale si basa sul contenuto della coda di messaggi e viene aggiornato quando si rimuovono i messaggi dalla coda.</span><span class="sxs-lookup"><span data-stu-id="e0066-228">This virtual state is based on the contents of your message queue, and gets updated as you remove messages from the queue.</span></span> <span data-ttu-id="e0066-229">Quando il programma elabora i messaggi della finestra, **GetKeyState** fornisce uno snapshot della tastiera nel momento in cui ogni messaggio è stato accodato.</span><span class="sxs-lookup"><span data-stu-id="e0066-229">As your program processes window messages, **GetKeyState** gives you a snapshot of the keyboard at the time that each message was queued.</span></span> <span data-ttu-id="e0066-230">Se, ad esempio, l'ultimo messaggio della coda è [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** segnala lo stato della tastiera al momento in cui l'utente ha fatto clic sul pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="e0066-230">For example, if the last message on the queue was [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** reports the keyboard state at the moment when the user clicked the mouse button.</span></span>

<span data-ttu-id="e0066-231">Poiché [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) è basato sulla coda di messaggi, ignora anche l'input da tastiera inviato a un altro programma.</span><span class="sxs-lookup"><span data-stu-id="e0066-231">Because [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) is based on your message queue, it also ignores keyboard input that was sent to another program.</span></span> <span data-ttu-id="e0066-232">Se l'utente passa a un altro programma, tutte le pressioni dei tasti inviate al programma vengono ignorate da **GetKeyState**.</span><span class="sxs-lookup"><span data-stu-id="e0066-232">If the user switches to another program, any key presses that are sent to that program are ignored by **GetKeyState**.</span></span> <span data-ttu-id="e0066-233">Se si desidera effettivamente ottenere lo stato fisico immediato della tastiera, è presente una funzione per: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="e0066-233">If you really want to know the immediate physical state of the keyboard, there is a function for that: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span> <span data-ttu-id="e0066-234">Per la maggior parte del codice dell'interfaccia utente, tuttavia, la funzione corretta è **GetKeyState**.</span><span class="sxs-lookup"><span data-stu-id="e0066-234">For most UI code, however, the correct function is **GetKeyState**.</span></span>

## <a name="next"></a><span data-ttu-id="e0066-235">Prossima</span><span class="sxs-lookup"><span data-stu-id="e0066-235">Next</span></span>

[<span data-ttu-id="e0066-236">Tabelle dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="e0066-236">Accelerator Tables</span></span>](accelerator-tables.md)

 

 
