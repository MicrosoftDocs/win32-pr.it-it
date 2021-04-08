---
title: Gestione dello stato di un'applicazione
description: Una routine di finestra è semplicemente una funzione che viene richiamata per ogni messaggio, quindi è intrinsecamente senza stato. Pertanto, è necessario un modo per tenere traccia dello stato dell'applicazione da una chiamata di funzione a quella successiva.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e275833c30c612b5b40ab29d089d07ed7794b429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046719"
---
# <a name="managing-application-state"></a><span data-ttu-id="eb84f-104">Gestione dello stato di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="eb84f-104">Managing Application State</span></span>

<span data-ttu-id="eb84f-105">Una routine di finestra è semplicemente una funzione che viene richiamata per ogni messaggio, quindi è intrinsecamente senza stato.</span><span class="sxs-lookup"><span data-stu-id="eb84f-105">A window procedure is just a function that gets invoked for every message, so it is inherently stateless.</span></span> <span data-ttu-id="eb84f-106">Pertanto, è necessario un modo per tenere traccia dello stato dell'applicazione da una chiamata di funzione a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="eb84f-106">Therefore, you need a way to track the state of your application from one function call to the next.</span></span>

<span data-ttu-id="eb84f-107">L'approccio più semplice consiste semplicemente nell'inserire tutti gli elementi delle variabili globali.</span><span class="sxs-lookup"><span data-stu-id="eb84f-107">The simplest approach is simply to put everything in global variables.</span></span> <span data-ttu-id="eb84f-108">Questo approccio funziona correttamente per i programmi di piccole dimensioni e molti degli esempi di SDK usano questo approccio.</span><span class="sxs-lookup"><span data-stu-id="eb84f-108">This works well enough for small programs, and many of the SDK samples use this approach.</span></span> <span data-ttu-id="eb84f-109">In un programma di grandi dimensioni, tuttavia, comporta una proliferazione di variabili globali.</span><span class="sxs-lookup"><span data-stu-id="eb84f-109">In a large program, however, it leads to a proliferation of global variables.</span></span> <span data-ttu-id="eb84f-110">Inoltre, è possibile disporre di più finestre, ognuna con la propria routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="eb84f-110">Also, you might have several windows, each with its own window procedure.</span></span> <span data-ttu-id="eb84f-111">Tenere traccia della finestra che dovrebbe accedere alle variabili che risultano confuse e soggette a errori.</span><span class="sxs-lookup"><span data-stu-id="eb84f-111">Keeping track of which window should access which variables becomes confusing and error-prone.</span></span>

<span data-ttu-id="eb84f-112">La funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) fornisce un modo per passare qualsiasi struttura di dati a una finestra.</span><span class="sxs-lookup"><span data-stu-id="eb84f-112">The [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function provides a way to pass any data structure to a window.</span></span> <span data-ttu-id="eb84f-113">Quando questa funzione viene chiamata, invia i due messaggi seguenti alla routine della finestra:</span><span class="sxs-lookup"><span data-stu-id="eb84f-113">When this function is called, it sends the following two messages to your window procedure:</span></span>

- [<span data-ttu-id="eb84f-114">**\_NCCREATE WM**</span><span class="sxs-lookup"><span data-stu-id="eb84f-114">**WM\_NCCREATE**</span></span>](/windows/desktop/winmsg/wm-nccreate)
- [<span data-ttu-id="eb84f-115">**creazione di WM \_**</span><span class="sxs-lookup"><span data-stu-id="eb84f-115">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)

<span data-ttu-id="eb84f-116">Questi messaggi vengono inviati nell'ordine indicato.</span><span class="sxs-lookup"><span data-stu-id="eb84f-116">These messages are sent in the order listed.</span></span> <span data-ttu-id="eb84f-117">(Questi non sono gli unici due messaggi inviati durante [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), ma è possibile ignorare gli altri per questa discussione).</span><span class="sxs-lookup"><span data-stu-id="eb84f-117">(These are not the only two messages sent during [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), but we can ignore the others for this discussion.)</span></span>

<span data-ttu-id="eb84f-118">I messaggi [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e [**WM \_ create**](/windows/desktop/winmsg/wm-create) vengono inviati prima che la finestra diventi visibile.</span><span class="sxs-lookup"><span data-stu-id="eb84f-118">The [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message are sent before the window becomes visible.</span></span> <span data-ttu-id="eb84f-119">Questo consente di inizializzare l'interfaccia utente, ad esempio per determinare il layout iniziale della finestra.</span><span class="sxs-lookup"><span data-stu-id="eb84f-119">That makes them a good place to initialize your UI—for example, to determine the initial layout of the window.</span></span>

<span data-ttu-id="eb84f-120">L'ultimo parametro di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) è un puntatore di tipo **void \***.</span><span class="sxs-lookup"><span data-stu-id="eb84f-120">The last parameter of [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) is a pointer of type **void\***.</span></span> <span data-ttu-id="eb84f-121">È possibile passare qualsiasi valore del puntatore che si desidera in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="eb84f-121">You can pass any pointer value that you want in this parameter.</span></span> <span data-ttu-id="eb84f-122">Quando la routine della finestra gestisce il messaggio [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) o [**WM \_ create**](/windows/desktop/winmsg/wm-create) , può estrarre questo valore dai dati del messaggio.</span><span class="sxs-lookup"><span data-stu-id="eb84f-122">When the window procedure handles the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) or [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, it can extract this value from the message data.</span></span>

<span data-ttu-id="eb84f-123">Viene ora illustrato come usare questo parametro per passare i dati dell'applicazione alla finestra.</span><span class="sxs-lookup"><span data-stu-id="eb84f-123">Let's see how you would use this parameter to pass application data to your window.</span></span> <span data-ttu-id="eb84f-124">In primo luogo, definire una classe o una struttura che include informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="eb84f-124">First, define a class or structure that holds state information.</span></span>

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

<span data-ttu-id="eb84f-125">Quando si chiama [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), passare un puntatore a questa struttura nel parametro **void \*** finale.</span><span class="sxs-lookup"><span data-stu-id="eb84f-125">When you call [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), pass a pointer to this structure in the final **void\*** parameter.</span></span>

```C++
StateInfo *pState = new (std::nothrow) StateInfo;

if (pState == NULL)
{
    return 0;
}

// Initialize the structure members (not shown).

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
    pState      // Additional application data
    );
```

<span data-ttu-id="eb84f-126">Quando si ricevono i [**messaggi \_ WM NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e [**WM \_ create**](/windows/desktop/winmsg/wm-create) , il parametro *lParam* di ogni messaggio è un puntatore a una struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="eb84f-126">When you receive the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) messages, the *lParam* parameter of each message is a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="eb84f-127">La struttura **struttura CREATESTRUCT** contiene a sua volta il puntatore passato in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="eb84f-127">The **CREATESTRUCT** structure, in turn, contains the pointer that you passed into [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>

![diagramma che mostra il layout della struttura struttura CREATESTRUCT](images/appstate01.png)

<span data-ttu-id="eb84f-129">Ecco come estrarre il puntatore nella struttura dei dati.</span><span class="sxs-lookup"><span data-stu-id="eb84f-129">Here is how you extract the pointer to your data structure.</span></span> <span data-ttu-id="eb84f-130">Per prima cosa, ottenere la struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) eseguendo il cast del parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="eb84f-130">First, get the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure by casting the *lParam* parameter.</span></span>

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

<span data-ttu-id="eb84f-131">Il membro **lpCreateParams** della struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) è il puntatore void originale specificato in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="eb84f-131">The **lpCreateParams** member of the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure is the original void pointer that you specified in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="eb84f-132">Ottenere un puntatore alla struttura dei dati personalizzata eseguendo il cast di **lpCreateParams**.</span><span class="sxs-lookup"><span data-stu-id="eb84f-132">Get a pointer to your own data structure by casting **lpCreateParams**.</span></span>

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

<span data-ttu-id="eb84f-133">Chiamare quindi la funzione [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) e passare il puntatore alla struttura dei dati.</span><span class="sxs-lookup"><span data-stu-id="eb84f-133">Next, call the [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function and pass in the pointer to your data structure.</span></span>

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

<span data-ttu-id="eb84f-134">Lo scopo di questa ultima chiamata di funzione consiste nell'archiviare il puntatore *stateInfo* nei dati dell'istanza per la finestra.</span><span class="sxs-lookup"><span data-stu-id="eb84f-134">The purpose of this last function call is to store the *StateInfo* pointer in the instance data for the window.</span></span> <span data-ttu-id="eb84f-135">Una volta eseguita questa operazione, è sempre possibile riportare il puntatore dalla finestra chiamando [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span><span class="sxs-lookup"><span data-stu-id="eb84f-135">Once you do this, you can always get the pointer back from the window by calling [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span></span>

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

<span data-ttu-id="eb84f-136">Ogni finestra ha i propri dati di istanza, pertanto è possibile creare più finestre e assegnare a ogni finestra una propria istanza della struttura dei dati.</span><span class="sxs-lookup"><span data-stu-id="eb84f-136">Each window has its own instance data, so you can create multiple windows and give each window its own instance of the data structure.</span></span> <span data-ttu-id="eb84f-137">Questo approccio è particolarmente utile se si definisce una classe di finestre e si crea più di una finestra di tale classe, ad esempio se si crea una classe di controlli personalizzata.</span><span class="sxs-lookup"><span data-stu-id="eb84f-137">This approach is especially useful if you define a class of windows and create more than one window of that class—for example, if you create a custom control class.</span></span> <span data-ttu-id="eb84f-138">È consigliabile eseguire il wrapping della chiamata [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) in una piccola funzione helper.</span><span class="sxs-lookup"><span data-stu-id="eb84f-138">It is convenient to wrap the [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) call in a small helper function.</span></span>

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

<span data-ttu-id="eb84f-139">A questo punto è possibile scrivere la routine della finestra come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="eb84f-139">Now you can write your window procedure as follows.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;
    if (uMsg == WM_CREATE)
    {
        CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
        pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
        SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
    }
    else
    {
        pState = GetAppState(hwnd);
    }

    switch (uMsg)
    {


    // Remainder of the window procedure not shown ...

    }
    return TRUE;
}
```

## <a name="an-object-oriented-approach"></a><span data-ttu-id="eb84f-140">Un approccio Object-Oriented</span><span class="sxs-lookup"><span data-stu-id="eb84f-140">An Object-Oriented Approach</span></span>

<span data-ttu-id="eb84f-141">È possibile estendere ulteriormente questo approccio.</span><span class="sxs-lookup"><span data-stu-id="eb84f-141">We can extend this approach further.</span></span> <span data-ttu-id="eb84f-142">È già stata definita una struttura di dati per contenere le informazioni sullo stato relative alla finestra.</span><span class="sxs-lookup"><span data-stu-id="eb84f-142">We have already defined a data structure to hold state information about the window.</span></span> <span data-ttu-id="eb84f-143">È sensato fornire questa struttura di dati con funzioni membro (metodi) che operano sui dati.</span><span class="sxs-lookup"><span data-stu-id="eb84f-143">It makes sense to provide this data structure with member functions (methods) that operate on the data.</span></span> <span data-ttu-id="eb84f-144">Questo comporta naturalmente un progetto in cui la struttura (o la classe) è responsabile di tutte le operazioni nella finestra.</span><span class="sxs-lookup"><span data-stu-id="eb84f-144">This naturally leads to a design where the structure (or class) is responsible for all of the operations on the window.</span></span> <span data-ttu-id="eb84f-145">La routine della finestra diventerebbe quindi parte della classe.</span><span class="sxs-lookup"><span data-stu-id="eb84f-145">The window procedure would then become part of the class.</span></span>

<span data-ttu-id="eb84f-146">In altre parole, si desidera procedere nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="eb84f-146">In other words, we would like to go from this:</span></span>

```C++
// pseudocode

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;

    /* Get pState from the HWND. */

    switch (uMsg)
    {
        case WM_SIZE:
            HandleResize(pState, ...);
            break;

        case WM_PAINT:
            HandlePaint(pState, ...);
            break;

       // And so forth.
    }
}
```

<span data-ttu-id="eb84f-147">A questo scopo:</span><span class="sxs-lookup"><span data-stu-id="eb84f-147">To this:</span></span>

```C++
// pseudocode

LRESULT MyWindow::WindowProc(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_SIZE:
            this->HandleResize(...);
            break;

        case WM_PAINT:
            this->HandlePaint(...);
            break;
    }
}
```

<span data-ttu-id="eb84f-148">L'unico problema è come associare il `MyWindow::WindowProc` metodo.</span><span class="sxs-lookup"><span data-stu-id="eb84f-148">The only problem is how to hook up the `MyWindow::WindowProc` method.</span></span> <span data-ttu-id="eb84f-149">La funzione [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) prevede che la routine della finestra sia un puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="eb84f-149">The [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function expects the window procedure to be a function pointer.</span></span> <span data-ttu-id="eb84f-150">Non è possibile passare un puntatore a una funzione membro (non statica) in questo contesto.</span><span class="sxs-lookup"><span data-stu-id="eb84f-150">You can't pass a pointer to a (non-static) member function in this context.</span></span> <span data-ttu-id="eb84f-151">È tuttavia possibile passare un puntatore a una funzione membro *statica* e quindi delegare la funzione membro.</span><span class="sxs-lookup"><span data-stu-id="eb84f-151">However, you can pass a pointer to a *static* member function and then delegate to the member function.</span></span> <span data-ttu-id="eb84f-152">Ecco un modello di classe che mostra questo approccio:</span><span class="sxs-lookup"><span data-stu-id="eb84f-152">Here is a class template that shows this approach:</span></span>

```C++
template <class DERIVED_TYPE> 
class BaseWindow
{
public:
    static LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
    {
        DERIVED_TYPE *pThis = NULL;

        if (uMsg == WM_NCCREATE)
        {
            CREATESTRUCT* pCreate = (CREATESTRUCT*)lParam;
            pThis = (DERIVED_TYPE*)pCreate->lpCreateParams;
            SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pThis);

            pThis->m_hwnd = hwnd;
        }
        else
        {
            pThis = (DERIVED_TYPE*)GetWindowLongPtr(hwnd, GWLP_USERDATA);
        }
        if (pThis)
        {
            return pThis->HandleMessage(uMsg, wParam, lParam);
        }
        else
        {
            return DefWindowProc(hwnd, uMsg, wParam, lParam);
        }
    }

    BaseWindow() : m_hwnd(NULL) { }

    BOOL Create(
        PCWSTR lpWindowName,
        DWORD dwStyle,
        DWORD dwExStyle = 0,
        int x = CW_USEDEFAULT,
        int y = CW_USEDEFAULT,
        int nWidth = CW_USEDEFAULT,
        int nHeight = CW_USEDEFAULT,
        HWND hWndParent = 0,
        HMENU hMenu = 0
        )
    {
        WNDCLASS wc = {0};

        wc.lpfnWndProc   = DERIVED_TYPE::WindowProc;
        wc.hInstance     = GetModuleHandle(NULL);
        wc.lpszClassName = ClassName();

        RegisterClass(&wc);

        m_hwnd = CreateWindowEx(
            dwExStyle, ClassName(), lpWindowName, dwStyle, x, y,
            nWidth, nHeight, hWndParent, hMenu, GetModuleHandle(NULL), this
            );

        return (m_hwnd ? TRUE : FALSE);
    }

    HWND Window() const { return m_hwnd; }

protected:

    virtual PCWSTR  ClassName() const = 0;
    virtual LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam) = 0;

    HWND m_hwnd;
};
```

<span data-ttu-id="eb84f-153">La `BaseWindow` classe è una classe di base astratta dalla quale derivano le classi di finestra specifiche.</span><span class="sxs-lookup"><span data-stu-id="eb84f-153">The `BaseWindow` class is an abstract base class, from which specific window classes are derived.</span></span> <span data-ttu-id="eb84f-154">Ecco, ad esempio, la dichiarazione di una classe semplice derivata da `BaseWindow` :</span><span class="sxs-lookup"><span data-stu-id="eb84f-154">For example, here is the declaration of a simple class derived from `BaseWindow`:</span></span>

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

<span data-ttu-id="eb84f-155">Per creare la finestra, chiamare `BaseWindow::Create` :</span><span class="sxs-lookup"><span data-stu-id="eb84f-155">To create the window, call `BaseWindow::Create`:</span></span>

```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Learn to Program Windows", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}
```

<span data-ttu-id="eb84f-156">Il metodo virtuale puro `BaseWindow::HandleMessage` viene usato per implementare la routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="eb84f-156">The pure-virtual `BaseWindow::HandleMessage` method is used to implement the window procedure.</span></span> <span data-ttu-id="eb84f-157">Ad esempio, l'implementazione seguente equivale alla procedura della finestra visualizzata all'inizio del [modulo 1](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="eb84f-157">For example, the following implementation is equivalent to the window procedure shown at the start of [Module 1](your-first-windows-program.md).</span></span>

```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(m_hwnd, &ps);
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(m_hwnd, &ps);
        }
        return 0;

    default:
        return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
    }
    return TRUE;
}
```

<span data-ttu-id="eb84f-158">Si noti che l'handle della finestra viene archiviato in una variabile membro (*\_ HWND m*), pertanto non è necessario passarlo come parametro a `HandleMessage` .</span><span class="sxs-lookup"><span data-stu-id="eb84f-158">Notice that the window handle is stored in a member variable (*m\_hwnd*), so we do not need to pass it as a parameter to `HandleMessage`.</span></span>

<span data-ttu-id="eb84f-159">Molti dei framework di programmazione Windows esistenti, ad esempio Microsoft Foundation Classes (MFC) e Active Template Library (ATL), usano approcci sostanzialmente simili a quelli illustrati di seguito.</span><span class="sxs-lookup"><span data-stu-id="eb84f-159">Many of the existing Windows programming frameworks, such as Microsoft Foundation Classes (MFC) and Active Template Library (ATL), use approaches that are basically similar to the one shown here.</span></span> <span data-ttu-id="eb84f-160">Naturalmente, un Framework completamente generalizzato, ad esempio MFC, è più complesso rispetto a questo esempio relativamente semplicistico.</span><span class="sxs-lookup"><span data-stu-id="eb84f-160">Of course, a fully generalized framework such as MFC is more complex than this relatively simplistic example.</span></span>

## <a name="next"></a><span data-ttu-id="eb84f-161">Prossima</span><span class="sxs-lookup"><span data-stu-id="eb84f-161">Next</span></span>

[<span data-ttu-id="eb84f-162">Modulo 2: uso di COM nel programma Windows</span><span class="sxs-lookup"><span data-stu-id="eb84f-162">Module 2: Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a><span data-ttu-id="eb84f-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb84f-163">Related topics</span></span>

[<span data-ttu-id="eb84f-164">Esempio BaseWindow</span><span class="sxs-lookup"><span data-stu-id="eb84f-164">BaseWindow Sample</span></span>](basewindow-sample.md)