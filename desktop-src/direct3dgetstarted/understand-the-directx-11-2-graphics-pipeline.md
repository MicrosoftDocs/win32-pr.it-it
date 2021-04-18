---
title: Informazioni sulla pipeline di rendering Direct3D 11
description: In precedenza, si è appreso come creare una finestra che è possibile usare per il disegno con risorse del dispositivo DirectX. Viene ora illustrato come compilare la pipeline grafica e dove è possibile collegarla.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50f9a387b2d44fe750abcf5a8856f75e6d0110e
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/17/2021
ms.locfileid: "106320452"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a>Informazioni sulla pipeline di rendering Direct3D 11

In precedenza, si è appreso come creare una finestra che è possibile usare per il disegno [con risorse del dispositivo DirectX](work-with-dxgi.md). Viene ora illustrato come compilare la pipeline grafica e dove è possibile collegarla.

Si noterà che sono disponibili due interfacce Direct3D che definiscono la pipeline grafica: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), che fornisce una rappresentazione virtuale della GPU e delle relative risorse; e [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), che rappresenta l'elaborazione grafica per la pipeline. In genere si usa un'istanza di **ID3D11Device** per configurare e ottenere le risorse GPU necessarie per iniziare a elaborare la grafica in una scena e si usa **sul ID3D11DeviceContext** per elaborare tali risorse in ogni fase dello shader appropriata nella pipeline grafica. In genere i metodi **ID3D11Device** vengono chiamati raramente, ovvero solo quando si configura una scena o quando il dispositivo viene modificato. D'altra parte, si chiamerà **sul ID3D11DeviceContext** ogni volta che si elabora un frame per la visualizzazione.

In questo esempio viene creata e configurata una pipeline grafica minima adatta per la visualizzazione di un cubo semplice rotante ombreggiato. Viene illustrato approssimativamente il set di risorse più piccolo necessario per la visualizzazione. Quando si leggono le informazioni qui, si notino le limitazioni dell'esempio specificato, in cui potrebbe essere necessario estenderlo per supportare la scena di cui si vuole eseguire il rendering.

Questo esempio illustra due classi C++ per la grafica: una classe di Resource Manager del dispositivo e una classe renderer della scena 3D. Questo argomento è incentrato in particolare sul renderer della scena 3D.

## <a name="what-does-the-cube-renderer-do"></a>Che cosa fa il renderer del cubo?

La pipeline grafica è definita dalla classe renderer della scena 3D. Il renderer della scena è in grado di:

-   Definire i buffer costanti per archiviare i dati uniformi.
-   Definire i buffer dei vertici per i dati dei vertici degli oggetti e i buffer di indice corrispondenti per consentire al vertex shader di esaminare correttamente i triangoli.
-   Creare risorse di trama e visualizzazioni di risorse.
-   Caricare gli oggetti shader.
-   Aggiornare i dati grafici per visualizzare ogni frame.
-   Render (disegnare) la grafica nella catena di scambio.

I primi quattro processi usano in genere i metodi dell'interfaccia [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) per l'inizializzazione e la gestione delle risorse grafiche, mentre gli ultimi due usano i metodi di interfaccia [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) per gestire ed eseguire la pipeline grafica.

Un'istanza della classe **renderer** viene creata e gestita come variabile membro nella classe del progetto principale. L'istanza di **DeviceResources** viene gestita come puntatore condiviso tra più classi, tra cui la classe principale del progetto, la classe del provider di visualizzazione **app** e il **renderer**. Se si sostituisce **renderer** con una classe personalizzata, provare a dichiarare e ad assegnare l'istanza di **DeviceResources** come membro del puntatore condiviso:

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

È sufficiente passare il puntatore al costruttore della classe (o un altro metodo di inizializzazione) dopo che l'istanza di **DeviceResources** è stata creata nel metodo **Initialize** della classe **app** . È anche possibile passare un riferimento a **\_ ptr debole** se, invece, si vuole che la classe principale sia completamente proprietaria dell'istanza di **DeviceResources** .

## <a name="create-the-cube-renderer"></a>Creare il renderer del cubo

In questo esempio viene organizzata la classe renderer della scena con i metodi seguenti:

-   **CreateDeviceDependentResources**: viene chiamato ogni volta che la scena deve essere inizializzata o riavviata. Questo metodo carica i dati dei vertici iniziali, le trame, gli shader e altre risorse e costruisce i buffer di costanti e vertici iniziali. In genere, la maggior parte del lavoro viene eseguita con i metodi [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , non con i metodi [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .
-   **CreateWindowSizeDependentResources**: viene chiamato ogni volta che viene modificato lo stato della finestra, ad esempio quando si verifica il ridimensionamento o quando si modifica l'orientamento. Questo metodo ricompila le matrici di trasformazione, ad esempio quelle per la fotocamera.
-   **Aggiornamento**: in genere chiamato dalla parte del programma che gestisce lo stato del gioco immediato. in questo esempio, è sufficiente chiamarlo dalla classe **principale** . Questo metodo consente di leggere tutte le informazioni sullo stato del gioco che influiscono sul rendering, ad esempio gli aggiornamenti alla posizione dell'oggetto o ai frame di animazione, oltre a tutti i dati del gioco globale, ad esempio i livelli leggeri o le modifiche alla fisica Questi input vengono usati per aggiornare i buffer costanti per fotogramma e i dati degli oggetti.
-   **Render**: generalmente chiamato dalla parte del programma che gestisce il ciclo di gioco; in questo caso, viene chiamato dalla classe **principale** . Questo metodo costruisce la pipeline grafica: associa gli shader, associa i buffer e le risorse alle fasi dello shader e richiama il disegno per il frame corrente.

Questi metodi comprendono il corpo dei comportamenti per il rendering di una scena con Direct3D usando gli asset. Se si estende questo esempio con una nuova classe di rendering, dichiararla nella classe principale del progetto. Quindi:

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

diventa:

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

Si noti che in questo esempio si presuppone che i metodi abbiano le stesse firme nell'implementazione. Se le firme sono state modificate, rivedere il ciclo **principale** e apportare le modifiche di conseguenza.

Verranno ora esaminati in modo più dettagliato i metodi di rendering della scena.

## <a name="create-device-dependent-resources"></a>Creare risorse dipendenti dal dispositivo

**CreateDeviceDependentResources** consolida tutte le operazioni per inizializzare la scena e le relative risorse usando le chiamate [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) . Questo metodo presuppone che il dispositivo Direct3D sia stato appena inizializzato (o sia stato ricreato) per una scena. Ricrea o ricarica tutte le risorse grafiche specifiche della scena, ad esempio i vertex e i pixel shader, i buffer di Vertex e di indice per gli oggetti e qualsiasi altra risorsa (ad esempio, le trame e le visualizzazioni corrispondenti).

Ecco il codice di esempio per **CreateDeviceDependentResources**:


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



Ogni volta che si caricano risorse dal disco: risorse come file o trame dell'oggetto shader compilato (CSO o CSO), eseguire questa operazione in modo asincrono. In questo modo è possibile continuare a lavorare allo stesso tempo (come ad altre attività di configurazione) e, poiché il ciclo principale non è bloccato, è possibile continuare a visualizzare elementi visivamente interessanti per l'utente (ad esempio un'animazione di caricamento per il gioco). In questo esempio viene utilizzata l'API Concurrency:: Tasks disponibile a partire da Windows 8. Si noti la sintassi lambda utilizzata per incapsulare le attività di caricamento asincrono. Queste espressioni lambda rappresentano le funzioni chiamate fuori thread, quindi un puntatore all'oggetto classe corrente (**this**) viene acquisito in modo esplicito.

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



Di seguito è riportato un esempio di come creare buffer di Vertex e di indice:


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



Questo esempio non carica mesh o trame. È necessario creare i metodi per caricare i tipi di trama e mesh specifici del gioco e chiamarli in modo asincrono.

Inserire qui i valori iniziali per i buffer costanti per scena. Esempi di buffer di costante per scena includono luci fisse o altri elementi e dati della scena statica.

## <a name="implement-the-createwindowsizedependentresources-method"></a>Implementare il metodo CreateWindowSizeDependentResources

I metodi **CreateWindowSizeDependentResources** vengono chiamati ogni volta che le dimensioni della finestra, l'orientamento o la risoluzione cambiano.

Le risorse delle dimensioni della finestra vengono aggiornate in questo modo: il processo statico del messaggio ottiene uno dei diversi eventi possibili che indicano una modifica nello stato della finestra. Il ciclo principale viene quindi informato sull'evento e chiama **CreateWindowSizeDependentResources** sull'istanza della classe principale, che quindi chiama l'implementazione di **CreateWindowSizeDependentResources** nella classe renderer della scena.

Il compito principale di questo metodo è quello di assicurarsi che gli oggetti visivi non vengano confusi o non siano validi a causa di una modifica nelle proprietà della finestra. In questo esempio vengono aggiornate le matrici di progetto con un nuovo campo di visualizzazione (FOV) per la finestra ridimensionata o riorientata.

È già stato illustrato il codice per la creazione di risorse della finestra in **DeviceResources** , ovvero la catena di scambio (con buffer nascosto) e la visualizzazione della destinazione di rendering. Ecco come il renderer crea le trasformazioni dipendenti dalle proporzioni:


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



Se la scena dispone di un layout specifico di componenti che dipendono dalle proporzioni, questo è il punto in cui riordinarle in modo che corrispondano a tali proporzioni. Potrebbe essere necessario modificare la configurazione del comportamento di post-elaborazione anche qui.

## <a name="implement-the-update-method"></a>Implementare il metodo Update

Il metodo **Update** viene chiamato una volta per ogni ciclo di gioco, in questo esempio viene chiamato dal metodo della classe principale con lo stesso nome. Ha uno scopo semplice: aggiornare la geometria della scena e lo stato del gioco in base alla quantità di tempo trascorso (o passaggi temporali passati) rispetto al frame precedente. In questo esempio il cubo viene semplicemente ruotato una volta per frame. In una scena di gioco reale, questo metodo contiene molto altro codice per il controllo dello stato del gioco, l'aggiornamento di buffer costanti per fotogramma (o altri), i buffer di geometria e altri asset in memoria di conseguenza. Poiché la comunicazione tra la CPU e la GPU comporta un sovraccarico, assicurarsi di aggiornare solo i buffer che sono stati effettivamente modificati dall'ultimo frame. i buffer costanti possono essere raggruppati o divisi in base alle esigenze per renderli più efficienti.


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



In tal caso, **ruotare** aggiorna il buffer costante con una nuova matrice di trasformazione per il cubo. La matrice verrà moltiplicata per ogni vertice durante la fase vertex shader. Poiché questo metodo viene chiamato con ogni frame, si tratta di una posizione ideale per aggregare tutti i metodi che aggiornano i buffer delle costanti e dei vertici dinamici o per eseguire altre operazioni che preparano gli oggetti nella scena per la trasformazione da parte della pipeline grafica.

## <a name="implement-the-render-method"></a>Implementare il metodo Render

Questo metodo viene chiamato una volta per ogni ciclo di gioco dopo aver chiamato **Update**. Come **Update**, anche il metodo **Render** viene chiamato dalla classe principale. Si tratta del metodo in cui la pipeline grafica viene costruita ed elaborata per il frame mediante i metodi dell'istanza [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) . Questo culmine in una chiamata finale a [**sul ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed). È importante tenere presente che questa chiamata (o altre **\* *chiamate di tipo di definizione di tipo _* sul ID3D11DeviceContext**) esegue effettivamente la pipeline. In particolare, quando Direct3D comunica con la GPU per impostare lo stato di disegno, esegue ogni fase della pipeline e scrive i risultati dei pixel nella risorsa del buffer di destinazione di rendering per la visualizzazione da parte della catena di scambio. Poiché la comunicazione tra la CPU e la GPU comporta un sovraccarico, combinare più chiamate di disegna in una sola, se possibile, soprattutto se la scena ha molti oggetti di cui è stato eseguito il rendering.


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



È consigliabile impostare le varie fasi della pipeline grafica sul contesto in ordine. In genere, l'ordine è:

-   Aggiornare le risorse del buffer costante con nuovi dati in base alle esigenze (usando i dati dell' **aggiornamento**).
-   Assembly di input (IA): questa è la posizione in cui vengono collegati i buffer di Vertex e index che definiscono la geometria della scena. È necessario alleghi ogni Vertex e buffer di indice per ogni oggetto nella scena. Poiché questo esempio ha solo il cubo, è piuttosto semplice.
-   Vertex shader (VS): alleghi tutti i vertex shader che trasformeranno i dati nei buffer dei vertici e allegherà i buffer costanti per il vertex shader.
-   Pixel shader (PS): alleghi qualsiasi pixel shader che eseguirà operazioni per pixel nella scena rasterizzata e collegherà le risorse del dispositivo per il pixel shader (buffer costanti, trame e così via).
-   Merge di output (OM): questa è la fase in cui si fondono i pixel, al termine degli shader. Si tratta di un'eccezione alla regola, perché si allineano gli stencil di profondità e le destinazioni di rendering prima di impostare le altre fasi. È possibile disporre di più stencil e destinazioni se si dispone di vertex shader e pixel shader aggiuntivi che generano trame, ad esempio mappe Shadow, mappe di altezza o altre tecniche di campionamento, in questo caso, per ogni passaggio di disegno sarà necessario impostare la destinazione o le destinazioni appropriate prima di chiamare una funzione di disegno.

Successivamente, nella sezione finale ([usare shader e risorse shader](work-with-shaders-and-shader-resources.md)) verranno esaminati gli shader e verrà illustrato come Direct3D li esegue.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Successivo**
</dt> <dt>

[Usare shader e risorse shader](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
