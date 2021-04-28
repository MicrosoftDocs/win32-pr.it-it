---
title: Creazione di una finestra
description: Creazione di una finestra
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea5ec39187b389405d3c6d8eca475944278a3d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103969"
---
# <a name="creating-a-window"></a><span data-ttu-id="d7df2-103">Creazione di una finestra</span><span class="sxs-lookup"><span data-stu-id="d7df2-103">Creating a Window</span></span>

## <a name="window-classes"></a><span data-ttu-id="d7df2-104">Classi di finestra</span><span class="sxs-lookup"><span data-stu-id="d7df2-104">Window Classes</span></span>

<span data-ttu-id="d7df2-105">Una *classe finestra* definisce un set di comportamenti che possono avere in comune diverse finestre.</span><span class="sxs-lookup"><span data-stu-id="d7df2-105">A *window class* defines a set of behaviors that several windows might have in common.</span></span> <span data-ttu-id="d7df2-106">Ad esempio, in un gruppo di pulsanti, ogni pulsante ha un comportamento simile quando l'utente fa clic sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="d7df2-106">For example, in a group of buttons, each button has a similar behavior when the user clicks the button.</span></span> <span data-ttu-id="d7df2-107">Naturalmente, i pulsanti non sono completamente identici. ogni pulsante visualizza la propria stringa di testo e ha le proprie coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="d7df2-107">Of course, buttons are not completely identical; each button displays its own text string and has its own screen coordinates.</span></span> <span data-ttu-id="d7df2-108">I dati univoci per ogni finestra sono denominati *dati di istanza*.</span><span class="sxs-lookup"><span data-stu-id="d7df2-108">Data that is unique for each window is called *instance data*.</span></span>

<span data-ttu-id="d7df2-109">Ogni finestra deve essere associata a una classe finestra, anche se il programma crea una sola istanza di tale classe.</span><span class="sxs-lookup"><span data-stu-id="d7df2-109">Every window must be associated with a window class, even if your program only ever creates one instance of that class.</span></span> <span data-ttu-id="d7df2-110">È importante comprendere che una classe finestra non è una "classe" nel senso C++.</span><span class="sxs-lookup"><span data-stu-id="d7df2-110">It is important to understand that a window class is not a "class" in the C++ sense.</span></span> <span data-ttu-id="d7df2-111">Si tratta piuttosto di una struttura di dati usata internamente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d7df2-111">Rather, it is a data structure used internally by the operating system.</span></span> <span data-ttu-id="d7df2-112">Le classi finestra vengono registrate con il sistema in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d7df2-112">Window classes are registered with the system at run time.</span></span> <span data-ttu-id="d7df2-113">Per registrare una nuova classe finestra, iniziare compilando una [**struttura WNDCLASS:**](/windows/win32/api/winuser/ns-winuser-wndclassa)</span><span class="sxs-lookup"><span data-stu-id="d7df2-113">To register a new window class, start by filling in a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure:</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

<span data-ttu-id="d7df2-114">È necessario impostare i membri della struttura seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7df2-114">You must set the following structure members:</span></span>

- <span data-ttu-id="d7df2-115">**lpfnWndProc** è un puntatore a una funzione definita dall'applicazione denominata *routine della* finestra o "proc finestra".</span><span class="sxs-lookup"><span data-stu-id="d7df2-115">**lpfnWndProc** is a pointer to an application-defined function called the *window procedure* or "window proc."</span></span> <span data-ttu-id="d7df2-116">La routine della finestra definisce la maggior parte del comportamento della finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-116">The window procedure defines most of the behavior of the window.</span></span> <span data-ttu-id="d7df2-117">La procedura della finestra verrà esaminata in dettaglio più avanti.</span><span class="sxs-lookup"><span data-stu-id="d7df2-117">We'll examine the window procedure in detail later.</span></span> <span data-ttu-id="d7df2-118">Per il momento, è sufficiente considerarlo come un riferimento in avanti.</span><span class="sxs-lookup"><span data-stu-id="d7df2-118">For now, just treat this as a forward reference.</span></span>
- <span data-ttu-id="d7df2-119">**hInstance è** l'handle per l'istanza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7df2-119">**hInstance** is the handle to the application instance.</span></span> <span data-ttu-id="d7df2-120">Ottenere questo valore dal *parametro hInstance* di **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="d7df2-120">Get this value from the *hInstance* parameter of **wWinMain**.</span></span>
- <span data-ttu-id="d7df2-121">**lpszClassName** è una stringa che identifica la classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-121">**lpszClassName** is a string that identifies the window class.</span></span>

<span data-ttu-id="d7df2-122">I nomi delle classi sono locali per il processo corrente, quindi il nome deve essere univoco solo all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="d7df2-122">Class names are local to the current process, so the name only needs to be unique within the process.</span></span> <span data-ttu-id="d7df2-123">Tuttavia, anche i controlli Windows standard hanno classi .</span><span class="sxs-lookup"><span data-stu-id="d7df2-123">However, the standard Windows controls also have classes.</span></span> <span data-ttu-id="d7df2-124">Se si usa uno di questi controlli, è necessario selezionare i nomi delle classi che non sono in conflitto con i nomi delle classi del controllo.</span><span class="sxs-lookup"><span data-stu-id="d7df2-124">If you use any of those controls, you must pick class names that do not conflict with the control class names.</span></span> <span data-ttu-id="d7df2-125">Ad esempio, la classe della finestra per il controllo pulsante è denominata "Button".</span><span class="sxs-lookup"><span data-stu-id="d7df2-125">For example, the window class for the button control is named "Button".</span></span>

<span data-ttu-id="d7df2-126">La [**struttura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ha altri membri non illustrati qui.</span><span class="sxs-lookup"><span data-stu-id="d7df2-126">The [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure has other members not shown here.</span></span> <span data-ttu-id="d7df2-127">È possibile impostarli su zero, come illustrato in questo esempio, o compilarli.</span><span class="sxs-lookup"><span data-stu-id="d7df2-127">You can set them to zero, as shown in this example, or fill them in.</span></span> <span data-ttu-id="d7df2-128">La documentazione MSDN descrive la struttura in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="d7df2-128">The MSDN documentation describes the structure in detail.</span></span>

<span data-ttu-id="d7df2-129">Passare quindi l'indirizzo della [**struttura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) alla [**funzione RegisterClass.**](/windows/desktop/api/winuser/nf-winuser-registerclassa)</span><span class="sxs-lookup"><span data-stu-id="d7df2-129">Next, pass the address of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="d7df2-130">Questa funzione registra la classe della finestra con il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d7df2-130">This function registers the window class with the operating system.</span></span>

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a><span data-ttu-id="d7df2-131">Creazione della finestra</span><span class="sxs-lookup"><span data-stu-id="d7df2-131">Creating the Window</span></span>

<span data-ttu-id="d7df2-132">Per creare una nuova istanza di una finestra, chiamare la [**funzione CreateWindowEx:**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)</span><span class="sxs-lookup"><span data-stu-id="d7df2-132">To create a new instance of a window, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function:</span></span>

```C++
HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}
```

<span data-ttu-id="d7df2-133">È possibile leggere le descrizioni dettagliate dei parametri in MSDN, ma di seguito è disponibile un breve riepilogo:</span><span class="sxs-lookup"><span data-stu-id="d7df2-133">You can read detailed parameter descriptions on MSDN, but here is a quick summary:</span></span>

- <span data-ttu-id="d7df2-134">Il primo parametro consente di specificare alcuni comportamenti facoltativi per la finestra, ad esempio le finestre trasparenti.</span><span class="sxs-lookup"><span data-stu-id="d7df2-134">The first parameter lets you specify some optional behaviors for the window (for example, transparent windows).</span></span> <span data-ttu-id="d7df2-135">Impostare questo parametro su zero per i comportamenti predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d7df2-135">Set this parameter to zero for the default behaviors.</span></span>
- <span data-ttu-id="d7df2-136">`CLASS_NAME` è il nome della classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-136">`CLASS_NAME` is the name of the window class.</span></span> <span data-ttu-id="d7df2-137">Definisce il tipo di finestra che si sta creando.</span><span class="sxs-lookup"><span data-stu-id="d7df2-137">This defines the type of window you are creating.</span></span>
- <span data-ttu-id="d7df2-138">Il testo della finestra viene usato in modi diversi da tipi diversi di finestre.</span><span class="sxs-lookup"><span data-stu-id="d7df2-138">The window text is used in different ways by different types of windows.</span></span> <span data-ttu-id="d7df2-139">Se la finestra ha una barra del titolo, il testo viene visualizzato nella barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="d7df2-139">If the window has a title bar, the text is displayed in the title bar.</span></span>
- <span data-ttu-id="d7df2-140">Lo stile della finestra è un set di flag che definiscono parte dell'aspetto di una finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-140">The window style is a set of flags that define some of the look and feel of a window.</span></span> <span data-ttu-id="d7df2-141">La costante **WS \_ OVERLAPPEDWINDOW è** in realtà di diversi flag combinati con or bit per **bit.**</span><span class="sxs-lookup"><span data-stu-id="d7df2-141">The constant **WS\_OVERLAPPEDWINDOW** is actually several flags combined with a bitwise **OR**.</span></span> <span data-ttu-id="d7df2-142">Insieme, questi flag forniscono alla finestra una barra del titolo, un bordo, un menu di sistema e **i pulsanti Riduci** a icona e **Ingrandisci.**</span><span class="sxs-lookup"><span data-stu-id="d7df2-142">Together these flags give the window a title bar, a border, a system menu, and **Minimize** and **Maximize** buttons.</span></span> <span data-ttu-id="d7df2-143">Questo set di flag è lo stile più comune per una finestra dell'applicazione di primo livello.</span><span class="sxs-lookup"><span data-stu-id="d7df2-143">This set of flags is the most common style for a top-level application window.</span></span>
- <span data-ttu-id="d7df2-144">Per posizione e dimensioni, la costante **CW \_ USEDEFAULT indica** l'uso dei valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d7df2-144">For position and size, the constant **CW\_USEDEFAULT** means to use default values.</span></span>
- <span data-ttu-id="d7df2-145">Il parametro successivo imposta una finestra padre o una finestra proprietaria per la nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-145">The next parameter sets a parent window or owner window for the new window.</span></span> <span data-ttu-id="d7df2-146">Impostare l'elemento padre se si sta creando una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="d7df2-146">Set the parent if you are creating a child window.</span></span> <span data-ttu-id="d7df2-147">Per una finestra di primo livello, impostare su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="d7df2-147">For a top-level window, set this to **NULL**.</span></span>
- <span data-ttu-id="d7df2-148">Per una finestra dell'applicazione, il parametro successivo definisce il menu per la finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-148">For an application window, the next parameter defines the menu for the window.</span></span> <span data-ttu-id="d7df2-149">In questo esempio non viene utilizzato un menu, quindi il valore è **NULL.**</span><span class="sxs-lookup"><span data-stu-id="d7df2-149">This example does not use a menu, so the value is **NULL**.</span></span>
- <span data-ttu-id="d7df2-150">*hInstance è* l'handle di istanza, descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="d7df2-150">*hInstance* is the instance handle, described previously.</span></span> <span data-ttu-id="d7df2-151">Vedere [WinMain: punto di ingresso dell'applicazione.](winmain--the-application-entry-point.md)</span><span class="sxs-lookup"><span data-stu-id="d7df2-151">(See [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).)</span></span>
- <span data-ttu-id="d7df2-152">L'ultimo parametro è un puntatore a dati arbitrari di tipo **void \***.</span><span class="sxs-lookup"><span data-stu-id="d7df2-152">The last parameter is a pointer to arbitrary data of type **void\***.</span></span> <span data-ttu-id="d7df2-153">È possibile usare questo valore per passare una struttura di dati alla routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-153">You can use this value to pass a data structure to your window procedure.</span></span> <span data-ttu-id="d7df2-154">Verrà illustrato un modo possibile per usare questo parametro nella sezione Gestione [dello stato dell'applicazione.](managing-application-state-.md)</span><span class="sxs-lookup"><span data-stu-id="d7df2-154">We'll show one possible way to use this parameter in the section [Managing Application State](managing-application-state-.md).</span></span>

<span data-ttu-id="d7df2-155">[**CreateWindowEx restituisce**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) un handle per la nuova finestra oppure zero se la funzione non riesce.</span><span class="sxs-lookup"><span data-stu-id="d7df2-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) returns a handle to the new window, or zero if the function fails.</span></span> <span data-ttu-id="d7df2-156">Per visualizzare la finestra, ovvero renderla visibile, passare l'handle della finestra alla [**funzione ShowWindow:**](/windows/desktop/api/winuser/nf-winuser-showwindow)</span><span class="sxs-lookup"><span data-stu-id="d7df2-156">To show the window—that is, make the window visible —pass the window handle to the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function:</span></span>

```C++
ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="d7df2-157">Il *parametro hwnd* è l'handle di finestra restituito [**da CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)</span><span class="sxs-lookup"><span data-stu-id="d7df2-157">The *hwnd* parameter is the window handle returned by [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="d7df2-158">Il *parametro nCmdShow* può essere usato per ridurre a icona o ingrandire una finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-158">The *nCmdShow* parameter can be used to minimize or maximize a window.</span></span> <span data-ttu-id="d7df2-159">Il sistema operativo passa questo valore al programma tramite la **funzione wWinMain.**</span><span class="sxs-lookup"><span data-stu-id="d7df2-159">The operating system passes this value to the program through the **wWinMain** function.</span></span>

<span data-ttu-id="d7df2-160">Ecco il codice completo per creare la finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-160">Here is the complete code to create the window.</span></span> <span data-ttu-id="d7df2-161">Tenere presente `WindowProc` che è ancora solo una dichiarazione con inoltro di una funzione.</span><span class="sxs-lookup"><span data-stu-id="d7df2-161">Remember that `WindowProc` is still just a forward declaration of a function.</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;

RegisterClass(&wc);

// Create the window.

HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}

ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="d7df2-162">È stata creata una finestra.</span><span class="sxs-lookup"><span data-stu-id="d7df2-162">Congratulations, you've created a window!</span></span> <span data-ttu-id="d7df2-163">Al momento, la finestra non contiene contenuto né interagisce con l'utente.</span><span class="sxs-lookup"><span data-stu-id="d7df2-163">Right now, the window does not contain any content or interact with the user.</span></span> <span data-ttu-id="d7df2-164">In un'applicazione GUI reale, la finestra rispondeva agli eventi dell'utente e del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d7df2-164">In a real GUI application, the window would respond to events from the user and the operating system.</span></span> <span data-ttu-id="d7df2-165">La sezione successiva descrive come i messaggi finestra forniscono questo tipo di interattività.</span><span class="sxs-lookup"><span data-stu-id="d7df2-165">The next section describes how window messages provide this sort of interactivity.</span></span>

### <a name="next"></a><span data-ttu-id="d7df2-166">Prossima</span><span class="sxs-lookup"><span data-stu-id="d7df2-166">Next</span></span>

[<span data-ttu-id="d7df2-167">Messaggi di finestra</span><span class="sxs-lookup"><span data-stu-id="d7df2-167">Window Messages</span></span>](window-messages.md)
