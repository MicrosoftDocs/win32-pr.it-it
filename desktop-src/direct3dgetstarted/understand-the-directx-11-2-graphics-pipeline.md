---
title: Informazioni sulla pipeline di rendering Direct3D 11
description: In precedenza si è esaminato come creare una finestra che è possibile usare per il disegno in Usare le risorse del dispositivo DirectX. A questo punto, si apprenderà come compilare la pipeline grafica e dove è possibile collegarla.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41a3e0fa7e3f7775c5cd51d49f9867864e7a204975fd982565491a63db829aa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727521"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a>Informazioni sulla pipeline di rendering Direct3D 11

In precedenza si è esaminato come creare una finestra che è possibile usare per il disegno in [Usare le risorse del dispositivo DirectX](work-with-dxgi.md). A questo punto, si apprenderà come compilare la pipeline grafica e dove è possibile collegarla.

Si ricorderà che esistono due interfacce Direct3D che definiscono la pipeline grafica: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), che fornisce una rappresentazione virtuale della GPU e delle relative risorse. e [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), che rappresenta l'elaborazione grafica per la pipeline. In genere, si usa un'istanza di **ID3D11Device** per configurare e ottenere le risorse GPU necessarie per avviare l'elaborazione della grafica in una scena e si usa **ID3D11DeviceContext** per elaborare tali risorse in ogni fase dello shader appropriata nella pipeline grafica. In genere si chiamano raramente i metodi **ID3D11Device,** ovvero solo quando si configura una scena o quando il dispositivo cambia. D'altra parte, si chiamerà **ID3D11DeviceContext** ogni volta che si elabora un frame per la visualizzazione.

In questo esempio viene creata e configurata una pipeline grafica minima adatta per la visualizzazione di un cubo semplice ruotato con ombreggiatura dei vertici. Illustra approssimativamente il set più piccolo di risorse necessarie per la visualizzazione. Quando si leggono le informazioni qui, prendere nota delle limitazioni dell'esempio specificato in cui potrebbe essere necessario estenderlo per supportare la scena di cui si vuole eseguire il rendering.

Questo esempio illustra due classi C++ per la grafica: una classe device resource manager e una classe renderer di scena 3D. Questo argomento si concentra in particolare sul renderer della scena 3D.

## <a name="what-does-the-cube-renderer-do"></a>Che cosa fa il renderer del cubo?

La pipeline di grafica è definita dalla classe renderer della scena 3D. Il renderer della scena è in grado di:

-   Definire buffer costanti per archiviare i dati uniformi.
-   Definire i vertex buffer per contenere i dati dei vertici dell'oggetto e i buffer di indice corrispondenti per consentire al vertex shader di eseguire correttamente i triangoli.
-   Creare le risorse di trama e le visualizzazioni delle risorse.
-   Caricare gli oggetti shader.
-   Aggiornare i dati grafici per visualizzare ogni frame.
-   Eseguire il rendering (disegnare) della grafica nella catena di scambio.

I primi quattro processi usano in genere i metodi dell'interfaccia [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) per l'inizializzazione e la gestione delle risorse grafiche e gli ultimi due usano i metodi dell'interfaccia [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) per gestire ed eseguire la pipeline grafica.

Un'istanza della **classe Renderer** viene creata e gestita come variabile membro nella classe di progetto principale. **L'istanza DeviceResources** viene gestita come puntatore condiviso tra diverse classi, tra cui la classe di progetto principale, la classe **del** provider di visualizzazione app e **renderer**. Se si **sostituisce Renderer** con una classe personalizzata, è consigliabile dichiarare e assegnare anche l'istanza **DeviceResources** come membro puntatore condiviso:

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

È sufficiente passare il puntatore al costruttore della classe (o a un altro metodo di inizializzazione) dopo la creazione dell'istanza **DeviceResources** nel **metodo Initialize** della **classe App.** È anche possibile passare un **riferimento \_ ptr** debole se invece si vuole che la classe principale sia completamente proprietaria dell'istanza **deviceResources.**

## <a name="create-the-cube-renderer"></a>Creare il renderer del cubo

In questo esempio la classe renderer della scena viene organizzata con i metodi seguenti:

-   **CreateDeviceDependentResources:** chiamato ogni volta che la scena deve essere inizializzata o riavviata. Questo metodo carica i dati iniziali dei vertici, le trame, gli shader e altre risorse e costruisce la costante iniziale e i buffer dei vertici. In genere, la maggior parte delle operazioni viene eseguita con [**i metodi ID3D11Device,**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) non [**con i metodi ID3D11DeviceContext.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2)
-   **CreateWindowSizeDependentResources:** chiamato ogni volta che cambia lo stato della finestra, ad esempio quando si verifica il ridimensionamento o quando cambia l'orientamento. Questo metodo ricompila le matrici di trasformazione, ad esempio quelle per la fotocamera.
-   **Update:** in genere chiamato dalla parte del programma che gestisce lo stato immediato del gioco. In questo esempio viene semplicemente chiamato dalla **classe** Main. Fare in modo che questo metodo letta da qualsiasi informazione sullo stato del gioco che influisca sul rendering, ad esempio gli aggiornamenti alla posizione dell'oggetto o ai fotogrammi di animazione, oltre a tutti i dati globali del gioco, ad esempio i livelli di luce o le modifiche alla fisica del gioco. Questi input vengono usati per aggiornare i buffer costanti per frame e i dati oggetto.
-   **Rendering:** chiamato in genere dalla parte del programma che gestisce il ciclo del gioco. In questo caso, viene chiamato dalla **classe** Main. Questo metodo costruisce la pipeline grafica: associa shader, associa buffer e risorse alle fasi dello shader e richiama il disegno per il frame corrente.

Questi metodi comprendono il corpo dei comportamenti per il rendering di una scena con Direct3D usando gli asset. Se si estende questo esempio con una nuova classe di rendering, dichiararlo nella classe di progetto principale. Quindi, questo:

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

diventa:

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

Anche in questo esempio si presuppone che i metodi presentino le stesse firme nell'implementazione. Se le firme sono state modificate, esaminare il **ciclo Main** e apportare le modifiche di conseguenza.

Di seguito vengono descritti più in dettaglio i metodi di rendering della scena.

## <a name="create-device-dependent-resources"></a>Creare risorse dipendenti dal dispositivo

**CreateDeviceDependentResources** consolida tutte le operazioni per l'inizializzazione della scena e delle relative risorse usando [**le chiamate ID3D11Device.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) Questo metodo presuppone che il dispositivo Direct3D sia stato appena inizializzato (o ricreato) per una scena. Ricrea o ricarica tutte le risorse grafiche specifiche della scena, ad esempio i vertici e i pixel shader, i buffer di vertice e indice per gli oggetti e qualsiasi altra risorsa, ad esempio come trame e le relative visualizzazioni corrispondenti.

Di seguito è riportato il codice di esempio **per CreateDeviceDependentResources:**


```C++
void Renderer::CreateDeviceDependentResources()
{
    // Compile shaders using the Effects library.
    auto CreateShadersTask = Concurrency::create_task(
            [this]( )
            {
                CreateShaders();
            }
        );

    // Load the geometry for the spinning cube.
    auto CreateCubeTask = CreateShadersTask.then(
            [this]()
            {
                CreateCube();
            }
        );
}

void Renderer::CreateWindowSizeDependentResources()
{
    // Create the view matrix and the perspective matrix.
    CreateViewAndPerspective();
}
```



Ogni volta che si caricano risorse dal disco, ad esempio file o trame di oggetti shader compilati (CSO o cso), eseguire questa operazione in modo asincrono. In questo modo è possibile continuare a lavorare contemporaneamente (come altre attività di configurazione) e, poiché il ciclo principale non è bloccato, è possibile continuare a visualizzare qualcosa di visivamente interessante per l'utente,ad esempio un'animazione di caricamento per il gioco. Questo esempio usa l'API Concurrency::Tasks disponibile a partire da Windows 8; Si noti la sintassi lambda usata per incapsulare le attività di caricamento asincrono. Queste espressioni lambda rappresentano le funzioni chiamate off-thread, quindi un puntatore all'oggetto classe corrente (**this**) viene acquisito in modo esplicito.

Ecco un esempio di come è possibile caricare il bytecode dello shader:


```C++
HRESULT hr = S_OK;

// Use the Direct3D device to load resources into graphics memory.
ID3D11Device* device = m_deviceResources->GetDevice();

// You'll need to use a file loader to load the shader bytecode. In this
// example, we just use the standard library.
FILE* vShader, * pShader;
BYTE* bytes;

size_t destSize = 4096;
size_t bytesRead = 0;
bytes = new BYTE[destSize];

fopen_s(&vShader, "CubeVertexShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, vShader);
hr = device->CreateVertexShader(
    bytes,
    bytesRead,
    nullptr,
    &m_pVertexShader
    );

D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );

delete bytes;


bytes = new BYTE[destSize];
bytesRead = 0;
fopen_s(&pShader, "CubePixelShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, pShader);
hr = device->CreatePixelShader(
    bytes,
    bytesRead,
    nullptr,
    m_pPixelShader.GetAddressOf()
    );

delete bytes;

CD3D11_BUFFER_DESC cbDesc(
    sizeof(ConstantBufferStruct),
    D3D11_BIND_CONSTANT_BUFFER
    );

hr = device->CreateBuffer(
    &cbDesc,
    nullptr,
    m_pConstantBuffer.GetAddressOf()
    );

fclose(vShader);
fclose(pShader);
```



Ecco un esempio di come creare buffer di vertici e indici:


```C++
HRESULT Renderer::CreateCube()
{
    HRESULT hr = S_OK;

    // Use the Direct3D device to load resources into graphics memory.
    ID3D11Device* device = m_deviceResources->GetDevice();

    // Create cube geometry.
    VertexPositionColor CubeVertices[] =
    {
        {DirectX::XMFLOAT3(-0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  0,   0,   0),},
        {DirectX::XMFLOAT3(-0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  0,   0,   1),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  0,   1,   0),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  0,   1,   1),},

        {DirectX::XMFLOAT3( 0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  1,   0,   0),},
        {DirectX::XMFLOAT3( 0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  1,   0,   1),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  1,   1,   0),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  1,   1,   1),},
    };
    
    // Create vertex buffer:
    
    CD3D11_BUFFER_DESC vDesc(
        sizeof(CubeVertices),
        D3D11_BIND_VERTEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA vData;
    ZeroMemory(&vData, sizeof(D3D11_SUBRESOURCE_DATA));
    vData.pSysMem = CubeVertices;
    vData.SysMemPitch = 0;
    vData.SysMemSlicePitch = 0;

    hr = device->CreateBuffer(
        &vDesc,
        &vData,
        &m_pVertexBuffer
        );

    // Create index buffer:
    unsigned short CubeIndices [] = 
    {
        0,2,1, // -x
        1,2,3,

        4,5,6, // +x
        5,7,6,

        0,1,5, // -y
        0,5,4,

        2,6,7, // +y
        2,7,3,

        0,4,6, // -z
        0,6,2,

        1,3,7, // +z
        1,7,5,
    };

    m_indexCount = ARRAYSIZE(CubeIndices);

    CD3D11_BUFFER_DESC iDesc(
        sizeof(CubeIndices),
        D3D11_BIND_INDEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA iData;
    ZeroMemory(&iData, sizeof(D3D11_SUBRESOURCE_DATA));
    iData.pSysMem = CubeIndices;
    iData.SysMemPitch = 0;
    iData.SysMemSlicePitch = 0;
    
    hr = device->CreateBuffer(
        &iDesc,
        &iData,
        &m_pIndexBuffer
        );

    return hr;
}
```



In questo esempio non vengono caricate mesh o trame. È necessario creare i metodi per caricare i tipi di mesh e trama specifici del gioco e chiamarli in modo asincrono.

Popolare anche qui i valori iniziali per i buffer costanti per scena. Esempi di buffer costante per scena includono luci fisse o altri elementi e dati statici della scena.

## <a name="implement-the-createwindowsizedependentresources-method"></a>Implementare il metodo CreateWindowSizeDependentResources

**I metodi CreateWindowSizeDependentResources** vengono chiamati ogni volta che le dimensioni della finestra, l'orientamento o la risoluzione cambiano.

Le risorse delle dimensioni della finestra vengono aggiornate in questo modo: la procedura del messaggio statico ottiene uno dei diversi eventi possibili che indicano una modifica dello stato della finestra. Il ciclo principale viene quindi informato dell'evento e chiama **CreateWindowSizeDependentResources** nell'istanza della classe principale, che chiama quindi l'implementazione **CreateWindowSizeDependentResources** nella classe renderer della scena.

Il compito principale di questo metodo è assicurarsi che gli oggetti visivi non diventino confusi o non validi a causa di una modifica nelle proprietà della finestra. In questo esempio le matrici del progetto vengono aggiornate con un nuovo campo di visualizzazione (FOV) per la finestra ridimensionata o riorientata.

È già stato visualizzato il codice per la creazione di risorse della finestra in **DeviceResources,** ovvero la catena di scambio (con buffer nascosto) e la visualizzazione di destinazione del rendering. Ecco come il renderer crea trasformazioni dipendenti dalle proporzioni:


```C++
void Renderer::CreateViewAndPerspective()
{
    // Use DirectXMath to create view and perspective matrices.

    DirectX::XMVECTOR eye = DirectX::XMVectorSet(0.0f, 0.7f, 1.5f, 0.f);
    DirectX::XMVECTOR at  = DirectX::XMVectorSet(0.0f,-0.1f, 0.0f, 0.f);
    DirectX::XMVECTOR up  = DirectX::XMVectorSet(0.0f, 1.0f, 0.0f, 0.f);

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.view,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixLookAtRH(
                eye,
                at,
                up
                )
            )
        );

    float aspectRatioX = m_deviceResources->GetAspectRatio();
    float aspectRatioY = aspectRatioX < (16.0f / 9.0f) ? aspectRatioX / (16.0f / 9.0f) : 1.0f;

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.projection,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixPerspectiveFovRH(
                2.0f * std::atan(std::tan(DirectX::XMConvertToRadians(70) * 0.5f) / aspectRatioY),
                aspectRatioX,
                0.01f,
                100.0f
                )
            )
        );
}
```



Se la scena ha un layout specifico di componenti che dipende dalle proporzioni, questa è la posizione in cui riorganizzarli in modo che corrispondano a tali proporzioni. È anche possibile modificare la configurazione del comportamento di post-elaborazione qui.

## <a name="implement-the-update-method"></a>Implementare il metodo Update

Il **metodo Update** viene chiamato una volta per ogni ciclo di gioco. In questo esempio viene chiamato dal metodo della classe principale con lo stesso nome. Ha uno scopo semplice: aggiornare la geometria della scena e lo stato del gioco in base alla quantità di tempo trascorso (o passaggi del tempo trascorso) dal fotogramma precedente. In questo esempio il cubo viene semplicemente ruotato una volta per fotogramma. In una scena di gioco reale, questo metodo contiene molto più codice per controllare lo stato del gioco, aggiornare di conseguenza buffer costanti per frame (o altri dinamici), buffer geometry e altri asset in memoria. Poiché la comunicazione tra CPU e GPU comporta un sovraccarico, assicurarsi di aggiornare solo i buffer effettivamente modificati dall'ultimo frame. I buffer costanti possono essere raggruppati o suddivisi, in base alle esigenze per rendere più efficiente questa operazione.


```C++
void Renderer::Update()
{
    // Rotate the cube 1 degree per frame.
    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.world,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixRotationY(
                DirectX::XMConvertToRadians(
                    (float) m_frameCount++
                    )
                )
            )
        );

    if (m_frameCount == MAXUINT)  m_frameCount = 0;
}
```



In questo caso, **Rotate** aggiorna il buffer costante con una nuova matrice di trasformazione per il cubo. La matrice verrà moltiplicata per vertice durante la fase vertex shader. Poiché questo metodo viene chiamato con ogni frame, si tratta di un buon punto per aggregare tutti i metodi che aggiornano i buffer costanti e dei vertici dinamici o per eseguire qualsiasi altra operazione che prepari gli oggetti nella scena per la trasformazione dalla pipeline grafica.

## <a name="implement-the-render-method"></a>Implementare il metodo Render

Questo metodo viene chiamato una volta per ogni ciclo di gioco dopo la chiamata a **Update**. Come **Update,** anche **il metodo Render** viene chiamato dalla classe main. Questo è il metodo in cui la pipeline grafica viene costruita ed elaborata per il frame usando i metodi [**nell'istanza ID3D11DeviceContext.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) Questo culmina in una chiamata finale a [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed). È importante comprendere che questa chiamata (o altre chiamate Draw _ simili definite in **\* *_* ID3D11DeviceContext**) esegue effettivamente la pipeline. In particolare, questo è il momento in cui Direct3D comunica con la GPU per impostare lo stato di disegno, esegue ogni fase della pipeline e scrive i risultati dei pixel nella risorsa buffer di destinazione di rendering per la visualizzazione da parte della catena di scambio. Poiché la comunicazione tra CPU e GPU comporta un sovraccarico, combinare più chiamate di disegno in una singola, se possibile, soprattutto se la scena ha molti oggetti sottoposti a rendering.


```C++
void Renderer::Render()
{
    // Use the Direct3D device context to draw.
    ID3D11DeviceContext* context = m_deviceResources->GetDeviceContext();

    ID3D11RenderTargetView* renderTarget = m_deviceResources->GetRenderTarget();
    ID3D11DepthStencilView* depthStencil = m_deviceResources->GetDepthStencil();

    context->UpdateSubresource(
        m_pConstantBuffer.Get(),
        0,
        nullptr,
        &m_constantBufferData,
        0,
        0
        );

    // Clear the render target and the z-buffer.
    const float teal [] = { 0.098f, 0.439f, 0.439f, 1.000f };
    context->ClearRenderTargetView(
        renderTarget,
        teal
        );
    context->ClearDepthStencilView(
        depthStencil,
        D3D11_CLEAR_DEPTH | D3D11_CLEAR_STENCIL,
        1.0f,
        0);

    // Set the render target.
    context->OMSetRenderTargets(
        1,
        &renderTarget,
        depthStencil
        );

    // Set up the IA stage by setting the input topology and layout.
    UINT stride = sizeof(VertexPositionColor);
    UINT offset = 0;

    context->IASetVertexBuffers(
        0,
        1,
        m_pVertexBuffer.GetAddressOf(),
        &stride,
        &offset
        );

    context->IASetIndexBuffer(
        m_pIndexBuffer.Get(),
        DXGI_FORMAT_R16_UINT,
        0
        );
    
    context->IASetPrimitiveTopology(
        D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST
        );

    context->IASetInputLayout(m_pInputLayout.Get());

    // Set up the vertex shader stage.
    context->VSSetShader(
        m_pVertexShader.Get(),
        nullptr,
        0
        );

    context->VSSetConstantBuffers(
        0,
        1,
        m_pConstantBuffer.GetAddressOf()
        );

    // Set up the pixel shader stage.
    context->PSSetShader(
        m_pPixelShader.Get(),
        nullptr,
        0
        );

    // Calling Draw tells Direct3D to start sending commands to the graphics device.
    context->DrawIndexed(
        m_indexCount,
        0,
        0
        );
}
```



È consigliabile impostare le varie fasi della pipeline grafica nel contesto in ordine. In genere, l'ordine è:

-   Aggiornare le risorse del buffer costante con i nuovi dati in base alle esigenze (usando i dati di **Update**).
-   Assembly di input (IA): qui vengono collegati i buffer vertice e indice che definiscono la geometria della scena. È necessario collegare ogni vertice e ogni index buffer per ogni oggetto nella scena. Poiché questo esempio ha solo il cubo, è piuttosto semplice.
-   Vertex shader (VS): collegare tutti i vertex shader che trasformeranno i dati nei vertex buffer e allegare buffer costanti per il vertex shader.
-   Pixel shader (PS): collegare eventuali pixel shader che eseguono operazioni per pixel nella scena rasterizzata e collegare le risorse del dispositivo per il pixel shader (buffer costanti, trame e così via).
-   Fusione dell'output ( OM): questa è la fase in cui i pixel vengono uniti al termine degli shader. Si tratta di un'eccezione alla regola, perché si collegano gli stencil di profondità e si esegue il rendering delle destinazioni prima di impostare una delle altre fasi. È possibile avere più stencil e destinazioni se sono presenti vertici e pixel shader aggiuntivi che generano trame, ad esempio mappe ombreggiate, mappe di altezza o altre tecniche di campionamento. In questo caso, ogni passaggio di disegno dovrà impostare le destinazioni appropriate prima di chiamare una funzione di disegno.

Successivamente, nella sezione finale ( Usare shader e risorse[di shader](work-with-shaders-and-shader-resources.md)), verranno illustrati gli shader e verrà illustrato il modo in cui Direct3D li esegue.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Successivo**
</dt> <dt>

[Usare shader e risorse shader](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
