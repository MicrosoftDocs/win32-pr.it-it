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
# <a name="work-with-directx-device-resources"></a>Usare le risorse del dispositivo DirectX

Informazioni sul ruolo di Microsoft DirectX Graphics Infrastructure (DXGI) nel gioco DirectX di Windows Store. DXGI è un set di API che consente di configurare e gestire le risorse grafiche di basso livello e di schede grafiche. Senza di esso, non sarebbe possibile creare grafica del gioco in una finestra.

Si pensi a DXGI in questo modo: per accedere direttamente alla GPU e gestire le relative risorse, è necessario disporre di un modo per descriverlo all'app. La parte più importante delle informazioni necessarie sulla GPU è la posizione in cui creare i pixel, in modo che possa inviare tali pixel sullo schermo. In genere, questo è il "buffer nascosto", ovvero un percorso nella memoria GPU, in cui è possibile creare i pixel e quindi "invertiti" o "scambiati" e inviati allo schermo su un segnale di aggiornamento. DXGI consente di acquisire tale posizione e i mezzi per usare tale buffer (denominato *catena di scambio* perché si tratta di una catena di buffer scambiabili, che consente più strategie di buffering).

A tale scopo, è necessario l'accesso per scrivere nella catena di scambio e un handle per la finestra che visualizzerà il buffer nascosto corrente per la catena di scambio. È anche necessario connettere i due per assicurarsi che il sistema operativo aggiorni la finestra con il contenuto del buffer nascosto quando si richiede questa operazione.

Il processo generale per disegnare sullo schermo è il seguente:

-   Ottenere un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) per l'app.
-   Ottenere un'interfaccia per il dispositivo e il contesto Direct3D.
-   Creare la catena di scambio per visualizzare l'immagine di cui è stato eseguito il rendering in [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).
-   Creare una destinazione di rendering per il disegno e popolarla con pixel.
-   Presentare la catena di scambio.

## <a name="create-a-window-for-your-app"></a>Creare una finestra per l'app

La prima cosa da fare è creare una finestra. Per prima cosa, creare una classe di finestra popolando un'istanza di [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)e quindi registrarla usando [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa). La classe Window contiene le proprietà essenziali della finestra, inclusa l'icona utilizzata, la funzione di elaborazione dei messaggi statici (più avanti in questo esempio) e un nome univoco per la classe Window.


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



Successivamente, creare la finestra. È anche necessario fornire informazioni sulle dimensioni per la finestra e il nome della classe di finestra appena creata. Quando si chiama [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), si ottiene un puntatore opaco alla finestra denominata HWND; è necessario che il puntatore HWND venga usato ogni volta che è necessario fare riferimento alla finestra, inclusa l'eliminazione o la ricreazione, e (soprattutto importante) quando si crea la catena di scambio DXGI usata per creare la finestra.


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



Il modello di app desktop di Windows include un hook nel ciclo di messaggi di Windows. È necessario basare il ciclo del programma principale da questo hook scrivendo una funzione "StaticWindowProc" per elaborare gli eventi di windowing. Deve essere una funzione statica perché verrà chiamata da Windows al di fuori del contesto di qualsiasi istanza di classe. Di seguito è riportato un esempio molto semplice di una funzione di elaborazione statica dei messaggi.


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



Questo semplice esempio controlla solo le condizioni di uscita del programma: [**WM \_ Close**](/windows/desktop/winmsg/wm-close), inviato quando viene richiesta la chiusura della finestra e [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy), che viene inviato dopo che la finestra è stata effettivamente rimossa dallo schermo. Per l'elenco completo degli eventi di windowing, è necessario che un'app di produzione completa gestisca anche altri eventi di windowing. vedere [notifiche della finestra](/windows/desktop/winmsg/window-notifications).

Il ciclo del programma principale deve essere in grado di riconoscere i messaggi di Windows consentendo a Windows di eseguire il processo statico del messaggio. Consentire l'esecuzione efficiente del programma mediante la creazione di un fork del comportamento. ogni iterazione deve scegliere di elaborare nuovi messaggi di Windows, se disponibili, e se nessun messaggio si trova nella coda deve eseguire il rendering di un nuovo frame. Ecco un esempio molto semplice:


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



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>Ottenere un'interfaccia per il dispositivo e il contesto Direct3D

Il primo passaggio per l'utilizzo di Direct3D consiste nell'acquisire un'interfaccia per l'hardware Direct3D (GPU), rappresentata come istanze di [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) e [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2). Il primo è una rappresentazione virtuale delle risorse GPU e quest'ultimo è un'astrazione indipendente dal dispositivo della pipeline e del processo di rendering. Questo è un modo semplice per considerarlo: **ID3D11Device** contiene i metodi grafici che vengono chiamati raramente, in genere prima che si verifichi il rendering, per acquisire e configurare il set di risorse necessarie per iniziare a disegnare pixel. **Sul ID3D11DeviceContext**, invece, contiene i metodi che vengono chiamati ogni frame, ovvero il caricamento in buffer e visualizzazioni e altre risorse, la modifica dello stato di Unione e rasterizzazione dell'output, la gestione degli shader e la creazione dei risultati del passaggio di tali risorse tramite gli Stati e gli shader.

C'è una parte molto importante di questo processo: impostare il livello di funzionalità. Il livello di funzionalità indica a DirectX il livello minimo di hardware supportato dall'app, con il livello di funzionalità di D3D \_ \_ \_ 9 \_ 1 come set di funzionalità più basso e il \_ livello di funzionalità D3D \_ \_ 11 \_ 1 come il più alto attuale. \_Se si desidera raggiungere il maggior numero possibile di destinatari, è necessario supportare almeno 9 1. È necessario attendere alcuni minuti per leggere i [livelli di funzionalità](/previous-versions/windows/apps/hh994923(v=win.10)) Direct3D e valutare i livelli di funzionalità minimo e massimo che si desidera che il gioco supporti e per comprendere le implicazioni di propria scelta.

Ottenere i riferimenti (puntatori) al contesto del dispositivo e del dispositivo Direct3D e archiviarli come variabili a livello di classe nell'istanza di **DeviceResources** (come puntatori intelligenti **ComPtr** ). Usare questi riferimenti ogni volta che è necessario accedere al dispositivo Direct3D o al contesto di dispositivo.


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



## <a name="create-the-swap-chain"></a>Creare la catena di scambio

OK: è presente una finestra in cui eseguire il progetto e si dispone di un'interfaccia per inviare i dati e fornire comandi alla GPU. Ora vediamo come riunirle.

In primo luogo, si indica a DXGI quali valori usare per le proprietà della catena di scambio. Eseguire questa operazione usando una struttura [**\_ desc della \_ catena \_ di scambio DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) . Sei campi sono particolarmente importanti per le app desktop:

-   **Windowed**: indica se la catena di scambio è a schermo intero o ritagliata nella finestra. Impostare su TRUE per inserire la catena di scambio nella finestra creata in precedenza.
-   **BufferUsage**: impostare questa impostazione \_ sull'output della destinazione di rendering dell'utilizzo di DXGI \_ \_ \_ . Ciò indica che la catena di scambio sarà una superficie di disegno, che consente di usarla come destinazione di rendering Direct3D.
-   **SwapEffect**: impostare questa impostazione su DXGI \_ swap \_ Effect \_ Flip \_ sequenziale.
-   **Format**: il formato \_ DXGI \_ B8G8R8A8 \_ UNORM specifica un colore a 32 bit: 8 bit per ognuno dei tre canali colori RGB e 8 bit per il canale alfa.
-   **BufferCount**: impostare su 2 per un comportamento tradizionale con doppio buffer per evitare lo strappo. Impostare il numero di buffer su 3 Se il contenuto della grafica richiede più di un ciclo di aggiornamento del monitor per eseguire il rendering di un singolo frame (a 60 Hz, ad esempio, la soglia è superiore a 16 ms).
-   **SampleDesc**: questo campo controlla il campionamento multiplo. Impostare il **conteggio** su 1 e la **qualità** su 0 per le catene di scambio del modello flip. Per usare il campionamento multiplo con le catene di scambio Flip-Model, disegnare su una destinazione di rendering multicampionata separata e quindi risolvere la destinazione nella catena di scambio appena prima di presentarla. Il codice di esempio viene fornito in [multisampling nelle app di Windows Store](/previous-versions/windows/apps/dn458384(v=win.10)).

Dopo aver specificato una configurazione per la catena di scambio, è necessario usare la stessa Factory DXGI che ha creato il dispositivo Direct3D e il contesto di dispositivo per creare la catena di scambio.

**Forma breve:  **

Ottenere il riferimento [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) creato in precedenza. Eseguire il cast in [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (se non è già stato fatto) e quindi chiamare [**IDXGIDevice:: GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) per acquisire l'adattatore DXGI. Ottenere la factory padre per l'adapter chiamando [**IDXGIFactory2:: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) eredita da [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)). ora è possibile usare tale factory per creare la catena di scambio chiamando [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), come illustrato nell'esempio di codice seguente.


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



Se si sta iniziando, probabilmente è preferibile usare la configurazione illustrata di seguito. A questo punto, se si ha già familiarità con le versioni precedenti di DirectX, è possibile che venga chiesto: "perché non è stato creato il dispositivo e la catena di scambio nello stesso momento, anziché ripercorrere tutte queste classi?" La risposta è l'efficienza: le catene di scambio sono risorse del dispositivo Direct3D e le risorse del dispositivo sono associate al particolare dispositivo Direct3D che le ha create. Se si crea un nuovo dispositivo con una nuova catena di scambio, è necessario ricreare tutte le risorse del dispositivo usando il nuovo dispositivo Direct3D. Creando quindi la catena di scambio con la stessa Factory (come illustrato in precedenza), è possibile ricreare la catena di scambio e continuare a usare le risorse del dispositivo Direct3D già caricate.

A questo punto è disponibile una finestra dal sistema operativo, un modo per accedere alla GPU e alle relative risorse e una catena di scambio per visualizzare i risultati del rendering. Tutto ciò che rimane è quello di collegare l'intera operazione.

## <a name="create-a-render-target-for-drawing"></a>Creare una destinazione di rendering per il disegno

Per la pipeline dello shader è necessaria una risorsa in cui creare pixel. Il modo più semplice per creare questa risorsa consiste nel definire una risorsa [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) come buffer nascosto per la pixel shader di cui attingere, quindi leggere tale trama nella catena di scambio.

A tale scopo, creare una *visualizzazione* di destinazione del rendering. In Direct3D, una vista è un modo per accedere a una risorsa specifica. In questo caso, la vista consente all'pixel shader di scrivere nella trama quando completa le operazioni per pixel.

Esaminiamo il codice per questa operazione. Quando si imposta \_ \_ \_ l'output della destinazione di rendering dell'utilizzo di DXGI \_ nella catena di scambio, che ha consentito l'utilizzo della risorsa Direct3D sottostante come superficie di disegno. Quindi, per ottenere la visualizzazione della destinazione di rendering, è sufficiente ottenere il buffer nascosto dalla catena di scambio e creare una visualizzazione di destinazione del rendering associata alla risorsa buffer di back-down.


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



Creare anche un *buffer di stencil profondità*. Un buffer di stencil Depth è solo un tipo particolare di risorsa [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , che in genere viene usato per determinare quali pixel hanno priorità di prelievo durante la rasterizzazione in base alla distanza degli oggetti nella scena dalla fotocamera. Un buffer di stencil depth può essere usato anche per gli effetti degli stencil, in cui i pixel specifici vengono rimossi o ignorati durante la rasterizzazione. Questo buffer deve avere le stesse dimensioni della destinazione di rendering. Si noti che non è possibile leggere da o eseguire il rendering nella trama dello stencil depth buffer frame, perché viene usata esclusivamente dalla pipeline dello shader prima e durante la rasterizzazione finale.

Creare inoltre una visualizzazione per il buffer di stencil Depth come [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview). La vista indica alla pipeline dello shader come interpretare la risorsa [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) sottostante. Pertanto, se non si fornisce questa visualizzazione, non viene eseguito alcun test di profondità per pixel e gli oggetti nella scena potrebbero sembrare un po' all'interno.


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



L'ultimo passaggio consiste nel creare un viewport. Definisce il rettangolo visibile del buffer nascosto visualizzato sullo schermo; è possibile modificare la parte del buffer visualizzata sullo schermo cambiando i parametri del viewport. Questo codice è destinato alla dimensione intera della finestra o alla risoluzione dello schermo, nel caso di catene di scambio a schermo intero. Per divertimento, modificare i valori delle coordinate fornite e osservare i risultati.


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



Questo è il modo in cui si passa da un elemento a un altro per disegnare pixel in una finestra. Quando si inizia, è consigliabile acquisire familiarità con il modo in cui DirectX, tramite DXGI, gestisce le risorse di base necessarie per iniziare a disegnare pixel.

Verrà ora esaminata la struttura della pipeline grafica. vedere [informazioni sulla pipeline di rendering del modello di app DirectX](understand-the-directx-11-2-graphics-pipeline.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Successivo**
</dt> <dt>

[Usare shader e risorse shader](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 