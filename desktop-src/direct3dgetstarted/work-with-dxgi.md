---
title: Usare le risorse del dispositivo DirectX
description: Comprendere il ruolo di Microsoft DirectX Graphic Infrastructure (DXGI) nel gioco DirectX Windows Store.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600af9c5ca2d2ba8ce8a7b078c769e195c4a7898384d102a21be3aaaf2c936bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068661"
---
# <a name="work-with-directx-device-resources"></a>Usare le risorse del dispositivo DirectX

Comprendere il ruolo di Microsoft DirectX Graphic Infrastructure (DXGI) nel gioco DirectX Windows Store. DXGI è un set di API usate per configurare e gestire risorse di scheda grafica e grafica di basso livello. Senza di essa, non sarebbe possibile disegnare la grafica del gioco in una finestra.

Si pensi a DXGI in questo modo: per accedere direttamente alla GPU e gestirne le risorse, è necessario avere un modo per descriverlo nell'app. La parte più importante delle informazioni necessarie sulla GPU è la posizione in cui disegnare i pixel in modo da poter inviare tali pixel sullo schermo. In genere si tratta del "buffer nascosto", ovvero una posizione nella memoria GPU in cui è possibile disegnare i pixel e quindi "capovolti" o "scambiati" e inviati allo schermo su un segnale di aggiornamento. DXGI consente di acquisire tale posizione e i  mezzi per usare tale buffer (chiamato catena di scambio perché si tratta di una catena di buffer scambiabili, consentendo più strategie di buffering).

A tale scopo, è necessario accedere alla scrittura nella catena di scambio e un handle per la finestra che visualizza il buffer nascosto corrente per la catena di scambio. È anche necessario connettere i due elementi per assicurarsi che il sistema operativo a refreshrà la finestra con il contenuto del buffer nascosto quando lo si richiede.

Il processo generale per disegnare sullo schermo è il seguente:

-   Ottenere un [**oggetto CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) per l'app.
-   Ottenere un'interfaccia per il contesto e il dispositivo Direct3D.
-   Creare la catena di scambio per visualizzare l'immagine sottoposta a rendering in [**CoreWindow.**](/uwp/api/Windows.UI.Core.CoreWindow)
-   Creare una destinazione di rendering per il disegno e popolarla con pixel.
-   Presentare la catena di scambio.

## <a name="create-a-window-for-your-app"></a>Creare una finestra per l'app

La prima cosa da fare è creare una finestra. Creare prima di tutto una classe di finestra popolando un'istanza di [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)e quindi registrarla usando [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa). La classe window contiene le proprietà essenziali della finestra, tra cui l'icona che usa, la funzione di elaborazione dei messaggi statici (altre informazioni più avanti) e un nome univoco per la classe della finestra.


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



Creare quindi la finestra. È anche necessario specificare le informazioni sulle dimensioni per la finestra e il nome della classe della finestra appena creata. Quando chiami [**CreateWindow,**](/windows/desktop/api/winuser/nf-winuser-createwindowa)ottieni un puntatore opaco alla finestra denominato HWND; È necessario mantenere il puntatore HWND e usarlo ogni volta che è necessario fare riferimento alla finestra, inclusa l'eliminazione o la ricreazione, e (particolarmente importante) quando si crea la catena di scambio DXGI che si usa per disegnare nella finestra.


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



Il Windows di app desktop include un hook nel ciclo Windows messaggi. È necessario basare il ciclo del programma principale su questo hook scrivendo una funzione "StaticWindowProc" per elaborare gli eventi di windowing. Deve essere una funzione statica perché Windows la chiamerà all'esterno del contesto di qualsiasi istanza di classe. Ecco un esempio molto semplice di funzione di elaborazione di messaggi statici.


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



Questo semplice esempio controlla solo le condizioni di uscita del programma: [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close), inviato quando viene richiesta la chiusura della finestra e [**WM \_ DESTROY,**](/windows/desktop/winmsg/wm-destroy)che viene inviato dopo che la finestra è stata effettivamente rimossa dallo schermo. Un'app di produzione completa deve gestire anche altri eventi di windowing. Per l'elenco completo degli eventi di windowing, vedere [Notifiche delle finestre.](/windows/desktop/winmsg/window-notifications)

Il ciclo del programma principale stesso deve riconoscere Windows messaggi, consentendo Windows la possibilità di eseguire la procedura di messaggio statico. Consentire l'esecuzione efficiente del programma tramite forking del comportamento: ogni iterazione deve scegliere di elaborare nuovi messaggi Windows se disponibili e, se non sono presenti messaggi nella coda, deve eseguire il rendering di un nuovo frame. Ecco un esempio molto semplice:


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



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>Ottenere un'interfaccia per il contesto e il dispositivo Direct3D

Il primo passaggio per usare Direct3D consiste nell'acquisire un'interfaccia per l'hardware Direct3D (GPU), rappresentata come istanze di [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) e [**ID3D11DeviceContext.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) La prima è una rappresentazione virtuale delle risorse GPU e la seconda è un'astrazione indipendente dal dispositivo della pipeline e del processo di rendering. Ecco un modo semplice per pensare: **ID3D11Device** contiene i metodi grafici che si chiamano raramente, in genere prima di qualsiasi rendering, per acquisire e configurare il set di risorse necessarie per iniziare a disegnare pixel. **ID3D11DeviceContext,** d'altra parte, contiene i metodi che si chiamano ogni frame: caricamento in buffer e visualizzazioni e altre risorse, modifica dello stato di unione e rasterizzazione dell'output, gestione degli shader e disegno dei risultati del passaggio di tali risorse attraverso gli stati e gli shader.

C'è una parte molto importante di questo processo: l'impostazione del livello di funzionalità. Il livello di funzionalità indica a DirectX il livello minimo di hardware supportato dall'app, con D3D FEATURE LEVEL 9 1 come set di funzionalità più basso e \_ \_ \_ \_ D3D \_ FEATURE \_ LEVEL \_ 11 \_ 1 come valore massimo corrente. È consigliabile supportare \_ 9 1 come minimo se si vuole raggiungere il pubblico più ampio possibile. Leggere i livelli di funzionalità [Direct3D](/previous-versions/windows/apps/hh994923(v=win.10)) e valutare per se stessi i livelli di funzionalità minimo e massimo che il gioco deve supportare e per comprendere le implicazioni di propria scelta.

Ottenere riferimenti (puntatori) sia al dispositivo Direct3D che al contesto di dispositivo e archiviarli come variabili a livello di classe nell'istanza **deviceResources** (come puntatori **intelligenti ComPtr).** Usare questi riferimenti ogni volta che è necessario accedere al dispositivo Direct3D o al contesto di dispositivo.


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

Ok: è presente una finestra in cui disegnare e un'interfaccia per inviare dati e fornire comandi alla GPU. A questo punto si esamini come riunirli.

In primo luogo, indicare a DXGI quali valori usare per le proprietà della catena di scambio. Eseguire questa operazione usando [**una struttura \_ \_ \_ DESC DXGI SWAP CHAIN.**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) Sei campi sono particolarmente importanti per le app desktop:

-   **Windowed**: indica se la catena di scambio è a schermo intero o ritagliata nella finestra. Impostare questa opzione su TRUE per inserire la catena di scambio nella finestra creata in precedenza.
-   **BufferUsage:** impostare questa opzione su DXGI \_ USAGE RENDER TARGET OUTPUT \_ (OUTPUT DESTINAZIONE RENDERING \_ DXGI). \_ Ciò indica che la catena di scambio sarà una superficie di disegno, consentendo di usarla come destinazione di rendering Direct3D.
-   **SwapEffect:** impostare questa proprietà su DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL.
-   **Formato:** il formato DXGI \_ \_ B8G8R8A8 UNORM specifica il colore a \_ 32 bit: 8 bit per ognuno dei tre canali di colore RGB e 8 bit per il canale alfa.
-   **BufferCount:** impostare questa proprietà su 2 per un comportamento tradizionale a doppio buffer per evitare la rimozione. Impostare il numero di buffer su 3 se il contenuto grafico richiede più di un ciclo di aggiornamento del monitor per eseguire il rendering di un singolo fotogramma (ad esempio, a 60 Hz la soglia è superiore a 16 ms).
-   **SampleDesc:** questo campo controlla il multicampionamento. Impostare **Count (Conteggio)** su 1 e Quality **(Qualità)** su 0 per le catene di scambio del modello di capovolgimento. Per usare il multicampionamento con catene di scambio del modello di capovolgimento, disegnare su una destinazione di rendering multicampionata separata e quindi risolvere la destinazione nella catena di scambio subito prima di presentarla. Il codice di esempio è disponibile in [Multisampling nelle Windows Store.](/previous-versions/windows/apps/dn458384(v=win.10))

Dopo aver specificato una configurazione per la catena di scambio, è necessario usare la stessa factory DXGI che ha creato il dispositivo Direct3D (e il contesto di dispositivo) per creare la catena di scambio.

**Forma breve: **

Ottenere il [**riferimento ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) creato in precedenza. Eseguire l'upcast [**a IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (se non è già stato fatto) e quindi chiamare [**IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) per acquisire l'adapter DXGI. Ottenere la factory padre per tale adapter chiamando [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) eredita da [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)). È ora possibile usare tale factory per creare la catena di scambio chiamando [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), come illustrato nell'esempio di codice seguente.


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



Se si sta iniziando, è probabilmente meglio usare la configurazione illustrata qui. A questo punto, se si ha già familiarità con le versioni precedenti di DirectX, si potrebbe chiedere: "Perché il dispositivo e la catena di scambio non sono stati creati contemporaneamente, invece di tornare indietro in tutte queste classi?" La risposta è l'efficienza: le catene di scambio sono risorse del dispositivo Direct3D e le risorse del dispositivo sono collegate al particolare dispositivo Direct3D che le ha create. Se si crea un nuovo dispositivo con una nuova catena di scambio, è necessario ricreare tutte le risorse del dispositivo usando il nuovo dispositivo Direct3D. Creando quindi la catena di scambio con la stessa factory (come illustrato in precedenza), è possibile ricreare la catena di scambio e continuare a usare le risorse del dispositivo Direct3D già caricate.

È ora disponibile una finestra dal sistema operativo, un modo per accedere alla GPU e alle relative risorse e una catena di scambio per visualizzare i risultati del rendering. Non resta che collegare l'intero oggetto.

## <a name="create-a-render-target-for-drawing"></a>Creare una destinazione di rendering per il disegno

La pipeline dello shader richiede una risorsa in cui disegnare pixel. Il modo più semplice per creare questa risorsa consiste nel definire una risorsa [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) come buffer nascosto in cui disegnare il pixel shader e quindi leggere la trama nella catena di scambio.

A tale scopo, creare una visualizzazione di destinazione di *rendering*. In Direct3D una visualizzazione è un modo per accedere a una risorsa specifica. In questo caso, la visualizzazione consente al pixel shader di scrivere nella trama mentre completa le operazioni per pixel.

Si esamini ora il codice per questa operazione. Quando si imposta OUTPUT DESTINAZIONE RENDERING DXGI USAGE sulla catena di scambio, la risorsa Direct3D sottostante può essere usata \_ \_ come superficie di \_ \_ disegno. Per ottenere la visualizzazione della destinazione di rendering, è sufficiente ottenere il buffer nascosto dalla catena di scambio e creare una visualizzazione della destinazione di rendering associata alla risorsa buffer nascosto.


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



Creare anche un *buffer depth-stencil.* Un buffer depth-stencil è solo una forma particolare di risorsa [**ID3D11Texture2D,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) che in genere viene usata per determinare quali pixel hanno priorità di disegno durante la rasterizzazione in base alla distanza degli oggetti nella scena dalla fotocamera. Un buffer depth-stencil può essere usato anche per gli effetti degli stencil, in cui pixel specifici vengono eliminati o ignorati durante la rasterizzazione. Questo buffer deve avere le stesse dimensioni della destinazione di rendering. Si noti che non è possibile leggere o eseguire il rendering nella trama depth-stencil del buffer del frame perché viene usata esclusivamente dalla pipeline di shader prima e durante la rasterizzazione finale.

Creare anche una visualizzazione per il buffer depth-stencil come [**ID3D11DepthStencilView.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview) La visualizzazione indica alla pipeline di shader come interpretare la risorsa [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) sottostante, quindi se non si specifica questa visualizzazione non viene eseguito alcun test di profondità per pixel e gli oggetti nella scena possono sembrare come minimo all'interno.


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



L'ultimo passaggio consiste nel creare un viewport. Definisce il rettangolo visibile del buffer nascosto visualizzato sullo schermo. È possibile modificare la parte del buffer visualizzata sullo schermo modificando i parametri del viewport. Questo codice è destinato alle dimensioni dell'intera finestra, o alla risoluzione dello schermo, nel caso di catene di scambio a schermo intero. Per essere divertente, modificare i valori delle coordinate forniti e osservare i risultati.


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



Ed è così che si passa dal nulla al disegno di pixel in una finestra. All'inizio, è buona idea acquisire familiarità con il modo in cui DirectX, tramite DXGI, gestisce le risorse di base necessarie per iniziare a disegnare pixel.

Verrà ora osservata la struttura della pipeline grafica. Vedere [Informazioni sulla pipeline di rendering del modello di app DirectX.](understand-the-directx-11-2-graphics-pipeline.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Successivo**
</dt> <dt>

[Usare shader e risorse shader](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 