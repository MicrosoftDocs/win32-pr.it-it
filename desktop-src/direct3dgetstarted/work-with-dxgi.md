---
title: Usare le risorse del dispositivo DirectX
description: Informazioni sul ruolo di Microsoft DirectX Graphics Infrastructure (DXGI) nel gioco DirectX di Windows Store.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096e2be6f957d99bc6e5055f845c14448ecd647f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473539"
---
# <a name="work-with-directx-device-resources"></a><span data-ttu-id="77139-103">Usare le risorse del dispositivo DirectX</span><span class="sxs-lookup"><span data-stu-id="77139-103">Work with DirectX device resources</span></span>

<span data-ttu-id="77139-104">Informazioni sul ruolo di Microsoft DirectX Graphics Infrastructure (DXGI) nel gioco DirectX di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="77139-104">Understand the role of the Microsoft DirectX Graphics Infrastructure (DXGI) in your Windows Store DirectX game.</span></span> <span data-ttu-id="77139-105">DXGI è un set di API che consente di configurare e gestire le risorse grafiche di basso livello e di schede grafiche.</span><span class="sxs-lookup"><span data-stu-id="77139-105">DXGI is a set of APIs used to configure and manage low-level graphics and graphics adapter resources.</span></span> <span data-ttu-id="77139-106">Senza di esso, non sarebbe possibile creare grafica del gioco in una finestra.</span><span class="sxs-lookup"><span data-stu-id="77139-106">Without it, you'd have no way to draw your game's graphics to a window.</span></span>

<span data-ttu-id="77139-107">Si pensi a DXGI in questo modo: per accedere direttamente alla GPU e gestire le relative risorse, è necessario disporre di un modo per descriverlo all'app.</span><span class="sxs-lookup"><span data-stu-id="77139-107">Think of DXGI this way: to directly access the GPU and manage its resources, you must have a way to describe it to your app.</span></span> <span data-ttu-id="77139-108">La parte più importante delle informazioni necessarie sulla GPU è la posizione in cui creare i pixel, in modo che possa inviare tali pixel sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="77139-108">The most important piece of info you need about the GPU is the place to draw pixels so it can send those pixels to the screen.</span></span> <span data-ttu-id="77139-109">In genere, questo è il "buffer nascosto", ovvero un percorso nella memoria GPU, in cui è possibile creare i pixel e quindi "invertiti" o "scambiati" e inviati allo schermo su un segnale di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="77139-109">Typically this is called the "back buffer"—a location in GPU memory where you can draw the pixels and then have it "flipped" or "swapped" and sent to the screen on a refresh signal.</span></span> <span data-ttu-id="77139-110">DXGI consente di acquisire tale posizione e i mezzi per usare tale buffer (denominato *catena di scambio* perché si tratta di una catena di buffer scambiabili, che consente più strategie di buffering).</span><span class="sxs-lookup"><span data-stu-id="77139-110">DXGI lets you acquire that location and the means to use that buffer (called a *swap chain* because it is a chain of swappable buffers, allowing for multiple buffering strategies).</span></span>

<span data-ttu-id="77139-111">A tale scopo, è necessario l'accesso per scrivere nella catena di scambio e un handle per la finestra che visualizzerà il buffer nascosto corrente per la catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="77139-111">To do this, you need access to write to the swap chain, and a handle to the window that will display the current back buffer for the swap chain.</span></span> <span data-ttu-id="77139-112">È anche necessario connettere i due per assicurarsi che il sistema operativo aggiorni la finestra con il contenuto del buffer nascosto quando si richiede questa operazione.</span><span class="sxs-lookup"><span data-stu-id="77139-112">You also need to connect the two to ensure that the operating system will refresh the window with the contents of the back buffer when you request it to do so.</span></span>

<span data-ttu-id="77139-113">Il processo generale per disegnare sullo schermo è il seguente:</span><span class="sxs-lookup"><span data-stu-id="77139-113">The overall process for drawing to the screen is as follows:</span></span>

-   <span data-ttu-id="77139-114">Ottenere un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) per l'app.</span><span class="sxs-lookup"><span data-stu-id="77139-114">Get a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) for your app.</span></span>
-   <span data-ttu-id="77139-115">Ottenere un'interfaccia per il dispositivo e il contesto Direct3D.</span><span class="sxs-lookup"><span data-stu-id="77139-115">Get an interface for the Direct3D device and context.</span></span>
-   <span data-ttu-id="77139-116">Creare la catena di scambio per visualizzare l'immagine di cui è stato eseguito il rendering in [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="77139-116">Create the swap chain to display your rendered image in the [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>
-   <span data-ttu-id="77139-117">Creare una destinazione di rendering per il disegno e popolarla con pixel.</span><span class="sxs-lookup"><span data-stu-id="77139-117">Create a render target for drawing and populate it with pixels.</span></span>
-   <span data-ttu-id="77139-118">Presentare la catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="77139-118">Present the swap chain!</span></span>

## <a name="create-a-window-for-your-app"></a><span data-ttu-id="77139-119">Creare una finestra per l'app</span><span class="sxs-lookup"><span data-stu-id="77139-119">Create a window for your app</span></span>

<span data-ttu-id="77139-120">La prima cosa da fare è creare una finestra.</span><span class="sxs-lookup"><span data-stu-id="77139-120">The first thing we need to do is create a window.</span></span> <span data-ttu-id="77139-121">Per prima cosa, creare una classe di finestra popolando un'istanza di [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)e quindi registrarla usando [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="77139-121">First, create a window class by populating an instance of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa), then register it using [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="77139-122">La classe Window contiene le proprietà essenziali della finestra, inclusa l'icona utilizzata, la funzione di elaborazione dei messaggi statici (più avanti in questo esempio) e un nome univoco per la classe Window.</span><span class="sxs-lookup"><span data-stu-id="77139-122">The window class contains essential properties of the window, including the icon it uses, the static message processing function (more on this later), and a unique name for the window class.</span></span>


```C++
if(m_hInstance == NULL) 
    m_hInstance = (HINSTANCE)GetModuleHandle(NULL);

HICON hIcon = NULL;
WCHAR szExePath[MAX_PATH];
    GetModuleFileName(NULL, szExePath, MAX_PATH);

// If the icon is NULL, then use the first one found in the exe
if(hIcon == NULL)
    hIcon = ExtractIcon(m_hInstance, szExePath, 0); 

// Register the windows class
WNDCLASS wndClass;
wndClass.style = CS_DBLCLKS;
wndClass.lpfnWndProc = MainClass::StaticWindowProc;
wndClass.cbClsExtra = 0;
wndClass.cbWndExtra = 0;
wndClass.hInstance = m_hInstance;
wndClass.hIcon = hIcon;
wndClass.hCursor = LoadCursor(NULL, IDC_ARROW);
wndClass.hbrBackground = (HBRUSH)GetStockObject(BLACK_BRUSH);
wndClass.lpszMenuName = NULL;
wndClass.lpszClassName = m_windowClassName.c_str();

if(!RegisterClass(&wndClass))
{
    DWORD dwError = GetLastError();
    if(dwError != ERROR_CLASS_ALREADY_EXISTS)
        return HRESULT_FROM_WIN32(dwError);
}
```



<span data-ttu-id="77139-123">Successivamente, creare la finestra.</span><span class="sxs-lookup"><span data-stu-id="77139-123">Next, you create the window.</span></span> <span data-ttu-id="77139-124">È anche necessario fornire informazioni sulle dimensioni per la finestra e il nome della classe di finestra appena creata.</span><span class="sxs-lookup"><span data-stu-id="77139-124">We also need to provide size information for the window and the name of the window class we just created.</span></span> <span data-ttu-id="77139-125">Quando si chiama [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), si ottiene un puntatore opaco alla finestra denominata HWND; è necessario che il puntatore HWND venga usato ogni volta che è necessario fare riferimento alla finestra, inclusa l'eliminazione o la ricreazione, e (soprattutto importante) quando si crea la catena di scambio DXGI usata per creare la finestra.</span><span class="sxs-lookup"><span data-stu-id="77139-125">When you call [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), you get back an opaque pointer to the window called an HWND; you'll need to keep the HWND pointer and use it any time you need to reference the window, including destroying or recreating it, and (especially important) when creating the DXGI swap chain you use to draw in the window.</span></span>


```C++
m_rc;
int x = CW_USEDEFAULT;
int y = CW_USEDEFAULT;

// No menu in this example.
m_hMenu = NULL;

// This example uses a non-resizable 640 by 480 viewport for simplicity.
int nDefaultWidth = 640;
int nDefaultHeight = 480;
SetRect(&m_rc, 0, 0, nDefaultWidth, nDefaultHeight);        
AdjustWindowRect(
    &m_rc,
    WS_OVERLAPPEDWINDOW,
    (m_hMenu != NULL) ? true : false
    );

// Create the window for our viewport.
m_hWnd = CreateWindow(
    m_windowClassName.c_str(),
    L"Cube11",
    WS_OVERLAPPEDWINDOW,
    x, y,
    (m_rc.right-m_rc.left), (m_rc.bottom-m_rc.top),
    0,
    m_hMenu,
    m_hInstance,
    0
    );

if(m_hWnd == NULL)
{
    DWORD dwError = GetLastError();
    return HRESULT_FROM_WIN32(dwError);
}
```



<span data-ttu-id="77139-126">Il modello di app desktop di Windows include un hook nel ciclo di messaggi di Windows.</span><span class="sxs-lookup"><span data-stu-id="77139-126">The Windows desktop app model includes a hook into the Windows message loop.</span></span> <span data-ttu-id="77139-127">È necessario basare il ciclo del programma principale da questo hook scrivendo una funzione "StaticWindowProc" per elaborare gli eventi di windowing.</span><span class="sxs-lookup"><span data-stu-id="77139-127">You'll need to base your main program loop off of this hook by writing a "StaticWindowProc" function to process windowing events.</span></span> <span data-ttu-id="77139-128">Deve essere una funzione statica perché verrà chiamata da Windows al di fuori del contesto di qualsiasi istanza di classe.</span><span class="sxs-lookup"><span data-stu-id="77139-128">This must be a static function because Windows will call it outside of the context of any class instance.</span></span> <span data-ttu-id="77139-129">Di seguito è riportato un esempio molto semplice di una funzione di elaborazione statica dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="77139-129">Here's a very simple example of a static message processing function.</span></span>


```C++
LRESULT CALLBACK MainClass::StaticWindowProc(
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam
    )
{
    switch(uMsg)
    {
        case WM_CLOSE:
        {
            HMENU hMenu;
            hMenu = GetMenu(hWnd);
            if (hMenu != NULL)
            {
                DestroyMenu(hMenu);
            }
            DestroyWindow(hWnd);
            UnregisterClass(
                m_windowClassName.c_str(),
                m_hInstance
                );
            return 0;
        }

        case WM_DESTROY:
            PostQuitMessage(0);
            break;
    }
    
    return DefWindowProc(hWnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="77139-130">Questo semplice esempio controlla solo le condizioni di uscita del programma: [**WM \_ Close**](/windows/desktop/winmsg/wm-close), inviato quando viene richiesta la chiusura della finestra e [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy), che viene inviato dopo che la finestra è stata effettivamente rimossa dallo schermo.</span><span class="sxs-lookup"><span data-stu-id="77139-130">This simple example only checks for program exit conditions: [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), sent when the window is requested to be closed, and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy), which is sent after the window is actually removed from the screen.</span></span> <span data-ttu-id="77139-131">Per l'elenco completo degli eventi di windowing, è necessario che un'app di produzione completa gestisca anche altri eventi di windowing. vedere [notifiche della finestra](/windows/desktop/winmsg/window-notifications).</span><span class="sxs-lookup"><span data-stu-id="77139-131">A full, production app needs to handle other windowing events too—for the complete list of windowing events, see [Window Notifications](/windows/desktop/winmsg/window-notifications).</span></span>

<span data-ttu-id="77139-132">Il ciclo del programma principale deve essere in grado di riconoscere i messaggi di Windows consentendo a Windows di eseguire il processo statico del messaggio.</span><span class="sxs-lookup"><span data-stu-id="77139-132">The main program loop itself needs to acknowledge Windows messages by allowing Windows the opportunity to run the static message proc.</span></span> <span data-ttu-id="77139-133">Consentire l'esecuzione efficiente del programma mediante la creazione di un fork del comportamento. ogni iterazione deve scegliere di elaborare nuovi messaggi di Windows, se disponibili, e se nessun messaggio si trova nella coda deve eseguire il rendering di un nuovo frame.</span><span class="sxs-lookup"><span data-stu-id="77139-133">Help the program run efficiently by forking the behavior: each iteration should choose to process new Windows messages if they are available, and if no messages are in the queue it should render a new frame.</span></span> <span data-ttu-id="77139-134">Ecco un esempio molto semplice:</span><span class="sxs-lookup"><span data-stu-id="77139-134">Here's a very simple example:</span></span>


```C++
bool bGotMsg;
MSG  msg;
msg.message = WM_NULL;
PeekMessage(&msg, NULL, 0U, 0U, PM_NOREMOVE);

while (WM_QUIT != msg.message)
{
    // Process window events.
    // Use PeekMessage() so we can use idle time to render the scene. 
    bGotMsg = (PeekMessage(&msg, NULL, 0U, 0U, PM_REMOVE) != 0);

    if (bGotMsg)
    {
        // Translate and dispatch the message
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
    else
    {
        // Update the scene.
        renderer->Update();

        // Render frames during idle time (when no messages are waiting).
        renderer->Render();

        // Present the frame to the screen.
        deviceResources->Present();
    }
}
```



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a><span data-ttu-id="77139-135">Ottenere un'interfaccia per il dispositivo e il contesto Direct3D</span><span class="sxs-lookup"><span data-stu-id="77139-135">Get an interface for the Direct3D device and context</span></span>

<span data-ttu-id="77139-136">Il primo passaggio per l'utilizzo di Direct3D consiste nell'acquisire un'interfaccia per l'hardware Direct3D (GPU), rappresentata come istanze di [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) e [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span><span class="sxs-lookup"><span data-stu-id="77139-136">The first step to using Direct3D is to acquire an interface for the Direct3D hardware (the GPU), represented as instances of [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span></span> <span data-ttu-id="77139-137">Il primo è una rappresentazione virtuale delle risorse GPU e quest'ultimo è un'astrazione indipendente dal dispositivo della pipeline e del processo di rendering.</span><span class="sxs-lookup"><span data-stu-id="77139-137">The former is a virtual representation of the GPU resources, and the latter is a device-agnostic abstraction of the rendering pipeline and process.</span></span> <span data-ttu-id="77139-138">Questo è un modo semplice per considerarlo: **ID3D11Device** contiene i metodi grafici che vengono chiamati raramente, in genere prima che si verifichi il rendering, per acquisire e configurare il set di risorse necessarie per iniziare a disegnare pixel.</span><span class="sxs-lookup"><span data-stu-id="77139-138">Here's an easy way to think of it: **ID3D11Device** contains the graphics methods you call infrequently, usually before any rendering occurs, to acquire and configure the set of resources you need to start drawing pixels.</span></span> <span data-ttu-id="77139-139">**Sul ID3D11DeviceContext**, invece, contiene i metodi che vengono chiamati ogni frame, ovvero il caricamento in buffer e visualizzazioni e altre risorse, la modifica dello stato di Unione e rasterizzazione dell'output, la gestione degli shader e la creazione dei risultati del passaggio di tali risorse tramite gli Stati e gli shader.</span><span class="sxs-lookup"><span data-stu-id="77139-139">**ID3D11DeviceContext**, on the other hand, contains the methods you call every frame: loading in buffers and views and other resources, changing output-merger and rasterizer state, managing shaders, and drawing the results of passing those resources through the states and shaders.</span></span>

<span data-ttu-id="77139-140">C'è una parte molto importante di questo processo: impostare il livello di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="77139-140">There's one very important part of this process: setting the feature level.</span></span> <span data-ttu-id="77139-141">Il livello di funzionalità indica a DirectX il livello minimo di hardware supportato dall'app, con il livello di funzionalità di D3D \_ \_ \_ 9 \_ 1 come set di funzionalità più basso e il \_ livello di funzionalità D3D \_ \_ 11 \_ 1 come il più alto attuale.</span><span class="sxs-lookup"><span data-stu-id="77139-141">The feature level tells DirectX the minimum level of hardware your app supports, with D3D\_FEATURE\_LEVEL\_9\_1 as the lowest feature set and D3D\_FEATURE\_LEVEL\_11\_1 as the current highest.</span></span> <span data-ttu-id="77139-142">\_Se si desidera raggiungere il maggior numero possibile di destinatari, è necessario supportare almeno 9 1.</span><span class="sxs-lookup"><span data-stu-id="77139-142">You should support 9\_1 as the minimum if you want to reach the widest possible audience.</span></span> <span data-ttu-id="77139-143">È necessario attendere alcuni minuti per leggere i [livelli di funzionalità](/previous-versions/windows/apps/hh994923(v=win.10)) Direct3D e valutare i livelli di funzionalità minimo e massimo che si desidera che il gioco supporti e per comprendere le implicazioni di propria scelta.</span><span class="sxs-lookup"><span data-stu-id="77139-143">Take some time to read up on Direct3D [feature levels](/previous-versions/windows/apps/hh994923(v=win.10)) and assess for yourself the minimum and maximum feature levels you want your game to support and to understand the implications of your choice.</span></span>

<span data-ttu-id="77139-144">Ottenere i riferimenti (puntatori) al contesto del dispositivo e del dispositivo Direct3D e archiviarli come variabili a livello di classe nell'istanza di **DeviceResources** (come puntatori intelligenti **ComPtr** ).</span><span class="sxs-lookup"><span data-stu-id="77139-144">Obtain references (pointers) to both the Direct3D device and device context and store them as class-level variables on the **DeviceResources** instance (as **ComPtr** smart pointers).</span></span> <span data-ttu-id="77139-145">Usare questi riferimenti ogni volta che è necessario accedere al dispositivo Direct3D o al contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77139-145">Use these references whenever you need to access the Direct3D device or device context.</span></span>


```C++
D3D_FEATURE_LEVEL levels[] = {
    D3D_FEATURE_LEVEL_9_1,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_11_1
};

// This flag adds support for surfaces with a color-channel ordering different
// from the API default. It is required for compatibility with Direct2D.
UINT deviceFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;

#if defined(DEBUG) || defined(_DEBUG)
deviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif

// Create the Direct3D 11 API device object and a corresponding context.
Microsoft::WRL::ComPtr<ID3D11Device>        device;
Microsoft::WRL::ComPtr<ID3D11DeviceContext> context;

hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    deviceFlags,                // Set debug and Direct2D compatibility flags.
    levels,                     // List of feature levels this app can support.
    ARRAYSIZE(levels),          // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_featureLevel,            // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (FAILED(hr))
{
    // Handle device interface creation failure if it occurs.
    // For example, reduce the feature level requirement, or fail over 
    // to WARP rendering.
}

// Store pointers to the Direct3D 11.1 API device and immediate context.
device.As(&m_pd3dDevice);
context.As(&m_pd3dDeviceContext);
```



## <a name="create-the-swap-chain"></a><span data-ttu-id="77139-146">Creare la catena di scambio</span><span class="sxs-lookup"><span data-stu-id="77139-146">Create the swap chain</span></span>

<span data-ttu-id="77139-147">OK: è presente una finestra in cui eseguire il progetto e si dispone di un'interfaccia per inviare i dati e fornire comandi alla GPU.</span><span class="sxs-lookup"><span data-stu-id="77139-147">Okay: You have a window to draw in, and you have an interface to send data and give commands to the GPU.</span></span> <span data-ttu-id="77139-148">Ora vediamo come riunirle.</span><span class="sxs-lookup"><span data-stu-id="77139-148">Now let's see how to bring them together.</span></span>

<span data-ttu-id="77139-149">In primo luogo, si indica a DXGI quali valori usare per le proprietà della catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="77139-149">First, you tell DXGI what values to use for the properties of the swap chain.</span></span> <span data-ttu-id="77139-150">Eseguire questa operazione usando una struttura [**\_ desc della \_ catena \_ di scambio DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) .</span><span class="sxs-lookup"><span data-stu-id="77139-150">Do this using a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure.</span></span> <span data-ttu-id="77139-151">Sei campi sono particolarmente importanti per le app desktop:</span><span class="sxs-lookup"><span data-stu-id="77139-151">Six fields are particularly important for desktop apps:</span></span>

-   <span data-ttu-id="77139-152">**Windowed**: indica se la catena di scambio è a schermo intero o ritagliata nella finestra.</span><span class="sxs-lookup"><span data-stu-id="77139-152">**Windowed**: Indicates whether the swap chain is full-screen or clipped to the window.</span></span> <span data-ttu-id="77139-153">Impostare su TRUE per inserire la catena di scambio nella finestra creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="77139-153">Set this to TRUE to put the swap chain in the window you created earlier.</span></span>
-   <span data-ttu-id="77139-154">**BufferUsage**: impostare questa impostazione \_ sull'output della destinazione di rendering dell'utilizzo di DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="77139-154">**BufferUsage**: Set this to DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT.</span></span> <span data-ttu-id="77139-155">Ciò indica che la catena di scambio sarà una superficie di disegno, che consente di usarla come destinazione di rendering Direct3D.</span><span class="sxs-lookup"><span data-stu-id="77139-155">This indicates that the swap chain will be a drawing surface, allowing you to use it as a Direct3D render-target.</span></span>
-   <span data-ttu-id="77139-156">**SwapEffect**: impostare questa impostazione su DXGI \_ swap \_ Effect \_ Flip \_ sequenziale.</span><span class="sxs-lookup"><span data-stu-id="77139-156">**SwapEffect**: Set this to DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL.</span></span>
-   <span data-ttu-id="77139-157">**Format**: il formato \_ DXGI \_ B8G8R8A8 \_ UNORM specifica un colore a 32 bit: 8 bit per ognuno dei tre canali colori RGB e 8 bit per il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="77139-157">**Format**: The DXGI\_FORMAT\_B8G8R8A8\_UNORM format specifies 32-bit color: 8 bits for each of the three RGB color channels, and 8 bits for the alpha channel.</span></span>
-   <span data-ttu-id="77139-158">**BufferCount**: impostare su 2 per un comportamento tradizionale con doppio buffer per evitare lo strappo.</span><span class="sxs-lookup"><span data-stu-id="77139-158">**BufferCount**: Set this to 2 for a traditional double-buffered behavior to avoid tearing.</span></span> <span data-ttu-id="77139-159">Impostare il numero di buffer su 3 Se il contenuto della grafica richiede più di un ciclo di aggiornamento del monitor per eseguire il rendering di un singolo frame (a 60 Hz, ad esempio, la soglia è superiore a 16 ms).</span><span class="sxs-lookup"><span data-stu-id="77139-159">Set the buffer count to 3 if your graphics content takes more than one monitor refresh cycle to render a single frame (at 60 Hz for example, the threshold is more than 16 ms).</span></span>
-   <span data-ttu-id="77139-160">**SampleDesc**: questo campo controlla il campionamento multiplo.</span><span class="sxs-lookup"><span data-stu-id="77139-160">**SampleDesc**: This field controls multisampling.</span></span> <span data-ttu-id="77139-161">Impostare il **conteggio** su 1 e la **qualità** su 0 per le catene di scambio del modello flip.</span><span class="sxs-lookup"><span data-stu-id="77139-161">Set **Count** to 1 and **Quality** to 0 for flip-model swap chains.</span></span> <span data-ttu-id="77139-162">Per usare il campionamento multiplo con le catene di scambio Flip-Model, disegnare su una destinazione di rendering multicampionata separata e quindi risolvere la destinazione nella catena di scambio appena prima di presentarla.</span><span class="sxs-lookup"><span data-stu-id="77139-162">(To use multisampling with flip-model swap chains, draw on a separate multisampled render target and then resolve that target to the swap chain just before presenting it.</span></span> <span data-ttu-id="77139-163">Il codice di esempio viene fornito in [multisampling nelle app di Windows Store](/previous-versions/windows/apps/dn458384(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="77139-163">Example code is provided in [Multisampling in Windows Store apps](/previous-versions/windows/apps/dn458384(v=win.10)).)</span></span>

<span data-ttu-id="77139-164">Dopo aver specificato una configurazione per la catena di scambio, è necessario usare la stessa Factory DXGI che ha creato il dispositivo Direct3D e il contesto di dispositivo per creare la catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="77139-164">After you have specified a configuration for the swap chain, you must use the same DXGI factory that created the Direct3D device (and device context) in order to create the swap chain.</span></span>

<span data-ttu-id="77139-165">**Forma breve:  **</span><span class="sxs-lookup"><span data-stu-id="77139-165">**Short form:  **</span></span>

<span data-ttu-id="77139-166">Ottenere il riferimento [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="77139-166">Get the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) reference you created previously.</span></span> <span data-ttu-id="77139-167">Eseguire il cast in [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (se non è già stato fatto) e quindi chiamare [**IDXGIDevice:: GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) per acquisire l'adattatore DXGI.</span><span class="sxs-lookup"><span data-stu-id="77139-167">Upcast it to [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (if you haven't already) and then call [**IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) to acquire the DXGI adapter.</span></span> <span data-ttu-id="77139-168">Ottenere la factory padre per l'adapter chiamando [**IDXGIFactory2:: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) eredita da [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)). ora è possibile usare tale factory per creare la catena di scambio chiamando [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="77139-168">Get the parent factory for that adapter by calling [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) inherits from [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject))—now you can use that factory to create the swap chain by calling [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), as seen in the following code sample.</span></span>


```C++
DXGI_SWAP_CHAIN_DESC desc;
ZeroMemory(&desc, sizeof(DXGI_SWAP_CHAIN_DESC));
desc.Windowed = TRUE; // Sets the initial state of full-screen mode.
desc.BufferCount = 2;
desc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
desc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
desc.SampleDesc.Count = 1;      //multisampling setting
desc.SampleDesc.Quality = 0;    //vendor-specific flag
desc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
desc.OutputWindow = hWnd;

// Create the DXGI device object to use in other factories, such as Direct2D.
Microsoft::WRL::ComPtr<IDXGIDevice3> dxgiDevice;
m_pd3dDevice.As(&dxgiDevice);

// Create swap chain.
Microsoft::WRL::ComPtr<IDXGIAdapter> adapter;
Microsoft::WRL::ComPtr<IDXGIFactory> factory;

hr = dxgiDevice->GetAdapter(&adapter);

if (SUCCEEDED(hr))
{
    adapter->GetParent(IID_PPV_ARGS(&factory));

    hr = factory->CreateSwapChain(
        m_pd3dDevice.Get(),
        &desc,
        &m_pDXGISwapChain
        );
}
```



<span data-ttu-id="77139-169">Se si sta iniziando, probabilmente è preferibile usare la configurazione illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="77139-169">If you're just starting out, it's probably best to use the configuration shown here.</span></span> <span data-ttu-id="77139-170">A questo punto, se si ha già familiarità con le versioni precedenti di DirectX, è possibile che venga chiesto: "perché non è stato creato il dispositivo e la catena di scambio nello stesso momento, anziché ripercorrere tutte queste classi?"</span><span class="sxs-lookup"><span data-stu-id="77139-170">Now at this point, if you are already familiar with previous versions of DirectX you might be asking: "Why didn't we create the device and swap chain at the same time, instead of walking back through all of those classes?"</span></span> <span data-ttu-id="77139-171">La risposta è l'efficienza: le catene di scambio sono risorse del dispositivo Direct3D e le risorse del dispositivo sono associate al particolare dispositivo Direct3D che le ha create.</span><span class="sxs-lookup"><span data-stu-id="77139-171">The answer is efficiency: swap chains are Direct3D device resources, and device resources are tied to the particular Direct3D device that created them.</span></span> <span data-ttu-id="77139-172">Se si crea un nuovo dispositivo con una nuova catena di scambio, è necessario ricreare tutte le risorse del dispositivo usando il nuovo dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="77139-172">If you create a new device with a new swap chain, you have to recreate all your device resources using the new Direct3D device.</span></span> <span data-ttu-id="77139-173">Creando quindi la catena di scambio con la stessa Factory (come illustrato in precedenza), è possibile ricreare la catena di scambio e continuare a usare le risorse del dispositivo Direct3D già caricate.</span><span class="sxs-lookup"><span data-stu-id="77139-173">So by creating the swap chain with the same factory (as shown above), you are able to recreate the swap chain and continue using the Direct3D device resources you already have loaded!</span></span>

<span data-ttu-id="77139-174">A questo punto è disponibile una finestra dal sistema operativo, un modo per accedere alla GPU e alle relative risorse e una catena di scambio per visualizzare i risultati del rendering.</span><span class="sxs-lookup"><span data-stu-id="77139-174">Now you've got a window from the operating system, a way to access the GPU and its resources, and a swap chain to display the rendering results.</span></span> <span data-ttu-id="77139-175">Tutto ciò che rimane è quello di collegare l'intera operazione.</span><span class="sxs-lookup"><span data-stu-id="77139-175">All that's left is to wire the whole thing together!</span></span>

## <a name="create-a-render-target-for-drawing"></a><span data-ttu-id="77139-176">Creare una destinazione di rendering per il disegno</span><span class="sxs-lookup"><span data-stu-id="77139-176">Create a render target for drawing</span></span>

<span data-ttu-id="77139-177">Per la pipeline dello shader è necessaria una risorsa in cui creare pixel.</span><span class="sxs-lookup"><span data-stu-id="77139-177">The shader pipeline needs a resource to draw pixels into.</span></span> <span data-ttu-id="77139-178">Il modo più semplice per creare questa risorsa consiste nel definire una risorsa [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) come buffer nascosto per la pixel shader di cui attingere, quindi leggere tale trama nella catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="77139-178">The simplest way to create this resource is to define a [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource as a back buffer for the pixel shader to draw into, and then read that texture into the swap chain.</span></span>

<span data-ttu-id="77139-179">A tale scopo, creare una *visualizzazione* di destinazione del rendering.</span><span class="sxs-lookup"><span data-stu-id="77139-179">To do this, you create a render-target *view*.</span></span> <span data-ttu-id="77139-180">In Direct3D, una vista è un modo per accedere a una risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="77139-180">In Direct3D, a view is a way to access a specific resource.</span></span> <span data-ttu-id="77139-181">In questo caso, la vista consente all'pixel shader di scrivere nella trama quando completa le operazioni per pixel.</span><span class="sxs-lookup"><span data-stu-id="77139-181">In this case, the view enables the pixel shader to write into the texture as it completes its per-pixel operations.</span></span>

<span data-ttu-id="77139-182">Esaminiamo il codice per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="77139-182">Let's look at the code for this.</span></span> <span data-ttu-id="77139-183">Quando si imposta \_ \_ \_ l'output della destinazione di rendering dell'utilizzo di DXGI \_ nella catena di scambio, che ha consentito l'utilizzo della risorsa Direct3D sottostante come superficie di disegno.</span><span class="sxs-lookup"><span data-stu-id="77139-183">When you set DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT on the swap chain, that enabled the underlying Direct3D resource to be used as a drawing surface.</span></span> <span data-ttu-id="77139-184">Quindi, per ottenere la visualizzazione della destinazione di rendering, è sufficiente ottenere il buffer nascosto dalla catena di scambio e creare una visualizzazione di destinazione del rendering associata alla risorsa buffer di back-down.</span><span class="sxs-lookup"><span data-stu-id="77139-184">So to get our render target view, we just need to get the back buffer from the swap chain and create a render target view bound to the back buffer resource.</span></span>


```C++
hr = m_pDXGISwapChain->GetBuffer(
    0,
    __uuidof(ID3D11Texture2D),
    (void**) &m_pBackBuffer);

hr = m_pd3dDevice->CreateRenderTargetView(
    m_pBackBuffer.Get(),
    nullptr,
    m_pRenderTarget.GetAddressOf()
    );

m_pBackBuffer->GetDesc(&m_bbDesc);
```



<span data-ttu-id="77139-185">Creare anche un *buffer di stencil profondità*.</span><span class="sxs-lookup"><span data-stu-id="77139-185">Also create a *depth-stencil buffer*.</span></span> <span data-ttu-id="77139-186">Un buffer di stencil Depth è solo un tipo particolare di risorsa [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , che in genere viene usato per determinare quali pixel hanno priorità di prelievo durante la rasterizzazione in base alla distanza degli oggetti nella scena dalla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="77139-186">A depth-stencil buffer is just a particular form of [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource, which is typically used to determine which pixels have draw priority during rasterization based on the distance of the objects in the scene from the camera.</span></span> <span data-ttu-id="77139-187">Un buffer di stencil depth può essere usato anche per gli effetti degli stencil, in cui i pixel specifici vengono rimossi o ignorati durante la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="77139-187">A depth-stencil buffer can also be used for stencil effects, where specific pixels are discarded or ignored during rasterization.</span></span> <span data-ttu-id="77139-188">Questo buffer deve avere le stesse dimensioni della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="77139-188">This buffer must be the same size as the render target.</span></span> <span data-ttu-id="77139-189">Si noti che non è possibile leggere da o eseguire il rendering nella trama dello stencil depth buffer frame, perché viene usata esclusivamente dalla pipeline dello shader prima e durante la rasterizzazione finale.</span><span class="sxs-lookup"><span data-stu-id="77139-189">Note that you cannot read from or render to the frame buffer depth-stencil texture because it is used exclusively by the shader pipeline before and during final rasterization.</span></span>

<span data-ttu-id="77139-190">Creare inoltre una visualizzazione per il buffer di stencil Depth come [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="77139-190">Also create a view for the depth-stencil buffer as an [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span></span> <span data-ttu-id="77139-191">La vista indica alla pipeline dello shader come interpretare la risorsa [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) sottostante. Pertanto, se non si fornisce questa visualizzazione, non viene eseguito alcun test di profondità per pixel e gli oggetti nella scena potrebbero sembrare un po' all'interno.</span><span class="sxs-lookup"><span data-stu-id="77139-191">The view tells the shader pipeline how to interpret the underlying [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource - so if you don't supply this view no per-pixel depth testing is performed, and the objects in your scene may seem a bit inside-out at the very least!</span></span>


```C++
CD3D11_TEXTURE2D_DESC depthStencilDesc(
    DXGI_FORMAT_D24_UNORM_S8_UINT,
    static_cast<UINT> (m_bbDesc.Width),
    static_cast<UINT> (m_bbDesc.Height),
    1, // This depth stencil view has only one texture.
    1, // Use a single mipmap level.
    D3D11_BIND_DEPTH_STENCIL
    );

m_pd3dDevice->CreateTexture2D(
    &depthStencilDesc,
    nullptr,
    &m_pDepthStencil
    );

CD3D11_DEPTH_STENCIL_VIEW_DESC depthStencilViewDesc(D3D11_DSV_DIMENSION_TEXTURE2D);

m_pd3dDevice->CreateDepthStencilView(
    m_pDepthStencil.Get(),
    &depthStencilViewDesc,
    &m_pDepthStencilView
    );
```



<span data-ttu-id="77139-192">L'ultimo passaggio consiste nel creare un viewport.</span><span class="sxs-lookup"><span data-stu-id="77139-192">The last step is to create a viewport.</span></span> <span data-ttu-id="77139-193">Definisce il rettangolo visibile del buffer nascosto visualizzato sullo schermo; è possibile modificare la parte del buffer visualizzata sullo schermo cambiando i parametri del viewport.</span><span class="sxs-lookup"><span data-stu-id="77139-193">This defines the visible rectangle of the back buffer displayed on the screen; you can change the part of the buffer that is displayed on the screen by changing the parameters of the viewport.</span></span> <span data-ttu-id="77139-194">Questo codice è destinato alla dimensione intera della finestra o alla risoluzione dello schermo, nel caso di catene di scambio a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="77139-194">This code targets the whole window size—or the screen resolution, in the case of full-screen swap chains.</span></span> <span data-ttu-id="77139-195">Per divertimento, modificare i valori delle coordinate fornite e osservare i risultati.</span><span class="sxs-lookup"><span data-stu-id="77139-195">For fun, change the supplied coordinate values and observe the results.</span></span>


```C++
ZeroMemory(&m_viewport, sizeof(D3D11_VIEWPORT));
m_viewport.Height = (float) m_bbDesc.Height;
m_viewport.Width = (float) m_bbDesc.Width;
m_viewport.MinDepth = 0;
m_viewport.MaxDepth = 1;

m_pd3dDeviceContext->RSSetViewports(
    1,
    &m_viewport
    );
```



<span data-ttu-id="77139-196">Questo è il modo in cui si passa da un elemento a un altro per disegnare pixel in una finestra.</span><span class="sxs-lookup"><span data-stu-id="77139-196">And that's how you go from nothing to drawing pixels in a window!</span></span> <span data-ttu-id="77139-197">Quando si inizia, è consigliabile acquisire familiarità con il modo in cui DirectX, tramite DXGI, gestisce le risorse di base necessarie per iniziare a disegnare pixel.</span><span class="sxs-lookup"><span data-stu-id="77139-197">As you start out, it's a good idea to become familiar with how DirectX, through DXGI, manages the core resources you need to start drawing pixels.</span></span>

<span data-ttu-id="77139-198">Verrà ora esaminata la struttura della pipeline grafica. vedere [informazioni sulla pipeline di rendering del modello di app DirectX](understand-the-directx-11-2-graphics-pipeline.md).</span><span class="sxs-lookup"><span data-stu-id="77139-198">Next you'll look at the structure of the graphics pipeline; see [Understand the DirectX app template's rendering pipeline](understand-the-directx-11-2-graphics-pipeline.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77139-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77139-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="77139-200">**Successivo**</span><span class="sxs-lookup"><span data-stu-id="77139-200">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="77139-201">Usare shader e risorse shader</span><span class="sxs-lookup"><span data-stu-id="77139-201">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 