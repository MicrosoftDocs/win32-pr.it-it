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
# <a name="understand-the-direct3d-11-rendering-pipeline"></a><span data-ttu-id="567ad-104">Informazioni sulla pipeline di rendering Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="567ad-104">Understand the Direct3D 11 rendering pipeline</span></span>

<span data-ttu-id="567ad-105">In precedenza, si è appreso come creare una finestra che è possibile usare per il disegno [con risorse del dispositivo DirectX](work-with-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="567ad-105">Previously, you looked at how to create a window you can use for drawing in [Work with DirectX device resources](work-with-dxgi.md).</span></span> <span data-ttu-id="567ad-106">Viene ora illustrato come compilare la pipeline grafica e dove è possibile collegarla.</span><span class="sxs-lookup"><span data-stu-id="567ad-106">Now, you learn how to build the graphics pipeline, and where you can hook into it.</span></span>

<span data-ttu-id="567ad-107">Si noterà che sono disponibili due interfacce Direct3D che definiscono la pipeline grafica: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), che fornisce una rappresentazione virtuale della GPU e delle relative risorse; e [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), che rappresenta l'elaborazione grafica per la pipeline.</span><span class="sxs-lookup"><span data-stu-id="567ad-107">You'll recall that there are two Direct3D interfaces that define the graphics pipeline: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), which provides a virtual representation of the GPU and its resources; and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), which represents the graphics processing for the pipeline.</span></span> <span data-ttu-id="567ad-108">In genere si usa un'istanza di **ID3D11Device** per configurare e ottenere le risorse GPU necessarie per iniziare a elaborare la grafica in una scena e si usa **sul ID3D11DeviceContext** per elaborare tali risorse in ogni fase dello shader appropriata nella pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="567ad-108">Typically, you use an instance of **ID3D11Device** to configure and obtain the GPU resources you need to start processing the graphics in a scene, and you use **ID3D11DeviceContext** to process those resources at each appropriate shader stage in the graphics pipeline.</span></span> <span data-ttu-id="567ad-109">In genere i metodi **ID3D11Device** vengono chiamati raramente, ovvero solo quando si configura una scena o quando il dispositivo viene modificato.</span><span class="sxs-lookup"><span data-stu-id="567ad-109">You usually call **ID3D11Device** methods infrequently—that is, only when you set up a scene or when the device changes.</span></span> <span data-ttu-id="567ad-110">D'altra parte, si chiamerà **sul ID3D11DeviceContext** ogni volta che si elabora un frame per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="567ad-110">On the other hand, you'll call **ID3D11DeviceContext** every time you process a frame for display.</span></span>

<span data-ttu-id="567ad-111">In questo esempio viene creata e configurata una pipeline grafica minima adatta per la visualizzazione di un cubo semplice rotante ombreggiato.</span><span class="sxs-lookup"><span data-stu-id="567ad-111">This example creates and configures a minimal graphics pipeline suitable for displaying a simple spinning, vertex-shaded cube.</span></span> <span data-ttu-id="567ad-112">Viene illustrato approssimativamente il set di risorse più piccolo necessario per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="567ad-112">It demonstrates approximately the smallest set of resources necessary for display.</span></span> <span data-ttu-id="567ad-113">Quando si leggono le informazioni qui, si notino le limitazioni dell'esempio specificato, in cui potrebbe essere necessario estenderlo per supportare la scena di cui si vuole eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="567ad-113">As you read the info here, note the limitations of the given example where you may have to extend it to support the scene you want to render.</span></span>

<span data-ttu-id="567ad-114">Questo esempio illustra due classi C++ per la grafica: una classe di Resource Manager del dispositivo e una classe renderer della scena 3D.</span><span class="sxs-lookup"><span data-stu-id="567ad-114">This example covers two C++ classes for graphics: a device resource manager class, and 3D scene renderer class.</span></span> <span data-ttu-id="567ad-115">Questo argomento è incentrato in particolare sul renderer della scena 3D.</span><span class="sxs-lookup"><span data-stu-id="567ad-115">This topic focuses specifically on the 3D scene renderer.</span></span>

## <a name="what-does-the-cube-renderer-do"></a><span data-ttu-id="567ad-116">Che cosa fa il renderer del cubo?</span><span class="sxs-lookup"><span data-stu-id="567ad-116">What does the cube renderer do?</span></span>

<span data-ttu-id="567ad-117">La pipeline grafica è definita dalla classe renderer della scena 3D.</span><span class="sxs-lookup"><span data-stu-id="567ad-117">The graphics pipeline is defined by the 3D scene renderer class.</span></span> <span data-ttu-id="567ad-118">Il renderer della scena è in grado di:</span><span class="sxs-lookup"><span data-stu-id="567ad-118">The scene renderer is able to:</span></span>

-   <span data-ttu-id="567ad-119">Definire i buffer costanti per archiviare i dati uniformi.</span><span class="sxs-lookup"><span data-stu-id="567ad-119">Define constant buffers to store your uniform data.</span></span>
-   <span data-ttu-id="567ad-120">Definire i buffer dei vertici per i dati dei vertici degli oggetti e i buffer di indice corrispondenti per consentire al vertex shader di esaminare correttamente i triangoli.</span><span class="sxs-lookup"><span data-stu-id="567ad-120">Define vertex buffers to hold your object vertex data, and corresponding index buffers to enable the vertex shader to walk the triangles correctly.</span></span>
-   <span data-ttu-id="567ad-121">Creare risorse di trama e visualizzazioni di risorse.</span><span class="sxs-lookup"><span data-stu-id="567ad-121">Create texture resources and resource views.</span></span>
-   <span data-ttu-id="567ad-122">Caricare gli oggetti shader.</span><span class="sxs-lookup"><span data-stu-id="567ad-122">Load your shader objects.</span></span>
-   <span data-ttu-id="567ad-123">Aggiornare i dati grafici per visualizzare ogni frame.</span><span class="sxs-lookup"><span data-stu-id="567ad-123">Update the graphics data to display each frame.</span></span>
-   <span data-ttu-id="567ad-124">Render (disegnare) la grafica nella catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="567ad-124">Render (draw) the graphics to the swap chain.</span></span>

<span data-ttu-id="567ad-125">I primi quattro processi usano in genere i metodi dell'interfaccia [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) per l'inizializzazione e la gestione delle risorse grafiche, mentre gli ultimi due usano i metodi di interfaccia [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) per gestire ed eseguire la pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="567ad-125">The first four processes typically use the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) interface methods for initializing and managing graphics resources, and the last two use the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) interface methods to manage and execute the graphics pipeline.</span></span>

<span data-ttu-id="567ad-126">Un'istanza della classe **renderer** viene creata e gestita come variabile membro nella classe del progetto principale.</span><span class="sxs-lookup"><span data-stu-id="567ad-126">An instance of the **Renderer** class is created and managed as a member variable on the main project class.</span></span> <span data-ttu-id="567ad-127">L'istanza di **DeviceResources** viene gestita come puntatore condiviso tra più classi, tra cui la classe principale del progetto, la classe del provider di visualizzazione **app** e il **renderer**.</span><span class="sxs-lookup"><span data-stu-id="567ad-127">The **DeviceResources** instance is managed as a shared pointer across several classes, including the main project class, the **App** view-provider class, and **Renderer**.</span></span> <span data-ttu-id="567ad-128">Se si sostituisce **renderer** con una classe personalizzata, provare a dichiarare e ad assegnare l'istanza di **DeviceResources** come membro del puntatore condiviso:</span><span class="sxs-lookup"><span data-stu-id="567ad-128">If you replace **Renderer** with your own class, consider declaring and assigning the **DeviceResources** instance as a shared pointer member as well:</span></span>

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

<span data-ttu-id="567ad-129">È sufficiente passare il puntatore al costruttore della classe (o un altro metodo di inizializzazione) dopo che l'istanza di **DeviceResources** è stata creata nel metodo **Initialize** della classe **app** .</span><span class="sxs-lookup"><span data-stu-id="567ad-129">Just pass the pointer into the class constructor (or other initialization method) after the **DeviceResources** instance is created in the **Initialize** method of the **App** class.</span></span> <span data-ttu-id="567ad-130">È anche possibile passare un riferimento a **\_ ptr debole** se, invece, si vuole che la classe principale sia completamente proprietaria dell'istanza di **DeviceResources** .</span><span class="sxs-lookup"><span data-stu-id="567ad-130">You can also pass a **weak\_ptr** reference if, instead, you want your main class to completely own the **DeviceResources** instance.</span></span>

## <a name="create-the-cube-renderer"></a><span data-ttu-id="567ad-131">Creare il renderer del cubo</span><span class="sxs-lookup"><span data-stu-id="567ad-131">Create the cube renderer</span></span>

<span data-ttu-id="567ad-132">In questo esempio viene organizzata la classe renderer della scena con i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="567ad-132">In this example, we organize the scene renderer class with the following methods:</span></span>

-   <span data-ttu-id="567ad-133">**CreateDeviceDependentResources**: viene chiamato ogni volta che la scena deve essere inizializzata o riavviata.</span><span class="sxs-lookup"><span data-stu-id="567ad-133">**CreateDeviceDependentResources**: Called whenever the scene must be initialized or restarted.</span></span> <span data-ttu-id="567ad-134">Questo metodo carica i dati dei vertici iniziali, le trame, gli shader e altre risorse e costruisce i buffer di costanti e vertici iniziali.</span><span class="sxs-lookup"><span data-stu-id="567ad-134">This method loads your initial vertex data, textures, shaders, and other resources, and constructs the initial constant and vertex buffers.</span></span> <span data-ttu-id="567ad-135">In genere, la maggior parte del lavoro viene eseguita con i metodi [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , non con i metodi [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .</span><span class="sxs-lookup"><span data-stu-id="567ad-135">Typically, most of the work here is done with [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) methods, not [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) methods.</span></span>
-   <span data-ttu-id="567ad-136">**CreateWindowSizeDependentResources**: viene chiamato ogni volta che viene modificato lo stato della finestra, ad esempio quando si verifica il ridimensionamento o quando si modifica l'orientamento.</span><span class="sxs-lookup"><span data-stu-id="567ad-136">**CreateWindowSizeDependentResources**: Called whenever the window state changes, such as when resizing occurs or when orientation changes.</span></span> <span data-ttu-id="567ad-137">Questo metodo ricompila le matrici di trasformazione, ad esempio quelle per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="567ad-137">This method rebuilds transform matrices, such as those for your camera.</span></span>
-   <span data-ttu-id="567ad-138">**Aggiornamento**: in genere chiamato dalla parte del programma che gestisce lo stato del gioco immediato. in questo esempio, è sufficiente chiamarlo dalla classe **principale** .</span><span class="sxs-lookup"><span data-stu-id="567ad-138">**Update**: Typically called from the part of the program that manages immediate game state; in this example, we just call it from the **Main** class.</span></span> <span data-ttu-id="567ad-139">Questo metodo consente di leggere tutte le informazioni sullo stato del gioco che influiscono sul rendering, ad esempio gli aggiornamenti alla posizione dell'oggetto o ai frame di animazione, oltre a tutti i dati del gioco globale, ad esempio i livelli leggeri o le modifiche alla fisica</span><span class="sxs-lookup"><span data-stu-id="567ad-139">Have this method read from any game-state information that affects rendering, such as updates to object position or animation frames, plus any global game data like light levels or changes to game physics.</span></span> <span data-ttu-id="567ad-140">Questi input vengono usati per aggiornare i buffer costanti per fotogramma e i dati degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="567ad-140">These inputs are used to update the per-frame constant buffers and object data.</span></span>
-   <span data-ttu-id="567ad-141">**Render**: generalmente chiamato dalla parte del programma che gestisce il ciclo di gioco; in questo caso, viene chiamato dalla classe **principale** .</span><span class="sxs-lookup"><span data-stu-id="567ad-141">**Render**: Typically called from the part of the program that manages the game loop; in this case, it's called from the **Main** class.</span></span> <span data-ttu-id="567ad-142">Questo metodo costruisce la pipeline grafica: associa gli shader, associa i buffer e le risorse alle fasi dello shader e richiama il disegno per il frame corrente.</span><span class="sxs-lookup"><span data-stu-id="567ad-142">This method constructs the graphics pipeline: it binds shaders, binds buffers and resources to shader stages, and invokes drawing for the current frame.</span></span>

<span data-ttu-id="567ad-143">Questi metodi comprendono il corpo dei comportamenti per il rendering di una scena con Direct3D usando gli asset.</span><span class="sxs-lookup"><span data-stu-id="567ad-143">These methods comprise the body of behaviors for rendering a scene with Direct3D using your assets.</span></span> <span data-ttu-id="567ad-144">Se si estende questo esempio con una nuova classe di rendering, dichiararla nella classe principale del progetto.</span><span class="sxs-lookup"><span data-stu-id="567ad-144">If you extend this example with a new rendering class, declare it on the main project class.</span></span> <span data-ttu-id="567ad-145">Quindi:</span><span class="sxs-lookup"><span data-stu-id="567ad-145">So this:</span></span>

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="567ad-146">diventa:</span><span class="sxs-lookup"><span data-stu-id="567ad-146">becomes this:</span></span>

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="567ad-147">Si noti che in questo esempio si presuppone che i metodi abbiano le stesse firme nell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="567ad-147">Again, note that this example assumes that the methods have the same signatures in your implementation.</span></span> <span data-ttu-id="567ad-148">Se le firme sono state modificate, rivedere il ciclo **principale** e apportare le modifiche di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="567ad-148">If the signatures have changed, review the **Main** loop and make the changes accordingly.</span></span>

<span data-ttu-id="567ad-149">Verranno ora esaminati in modo più dettagliato i metodi di rendering della scena.</span><span class="sxs-lookup"><span data-stu-id="567ad-149">Let's take a look at scene-rendering methods in more detail.</span></span>

## <a name="create-device-dependent-resources"></a><span data-ttu-id="567ad-150">Creare risorse dipendenti dal dispositivo</span><span class="sxs-lookup"><span data-stu-id="567ad-150">Create device dependent resources</span></span>

<span data-ttu-id="567ad-151">**CreateDeviceDependentResources** consolida tutte le operazioni per inizializzare la scena e le relative risorse usando le chiamate [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) .</span><span class="sxs-lookup"><span data-stu-id="567ad-151">**CreateDeviceDependentResources** consolidates all the operations for initializing the scene and its resources using [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) calls.</span></span> <span data-ttu-id="567ad-152">Questo metodo presuppone che il dispositivo Direct3D sia stato appena inizializzato (o sia stato ricreato) per una scena.</span><span class="sxs-lookup"><span data-stu-id="567ad-152">This method assumes that the Direct3D device has just been initialized (or has been recreated) for a scene.</span></span> <span data-ttu-id="567ad-153">Ricrea o ricarica tutte le risorse grafiche specifiche della scena, ad esempio i vertex e i pixel shader, i buffer di Vertex e di indice per gli oggetti e qualsiasi altra risorsa (ad esempio, le trame e le visualizzazioni corrispondenti).</span><span class="sxs-lookup"><span data-stu-id="567ad-153">It recreates or reloads all scene-specific graphics resources, such as the vertex and pixel shaders, the vertex and index buffers for objects, and any other resources (for example, as textures and their corresponding views).</span></span>

<span data-ttu-id="567ad-154">Ecco il codice di esempio per **CreateDeviceDependentResources**:</span><span class="sxs-lookup"><span data-stu-id="567ad-154">Here's example code for **CreateDeviceDependentResources**:</span></span>


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



<span data-ttu-id="567ad-155">Ogni volta che si caricano risorse dal disco: risorse come file o trame dell'oggetto shader compilato (CSO o CSO), eseguire questa operazione in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="567ad-155">Any time you load resources from disk—resources like compiled shader object (CSO, or .cso) files or textures—do so asynchronously.</span></span> <span data-ttu-id="567ad-156">In questo modo è possibile continuare a lavorare allo stesso tempo (come ad altre attività di configurazione) e, poiché il ciclo principale non è bloccato, è possibile continuare a visualizzare elementi visivamente interessanti per l'utente (ad esempio un'animazione di caricamento per il gioco).</span><span class="sxs-lookup"><span data-stu-id="567ad-156">This allows you to keep other work going at the same time (like other setup tasks), and because the main loop isn't blocked you can keep displaying something visually interesting to the user (like a loading animation for your game).</span></span> <span data-ttu-id="567ad-157">In questo esempio viene utilizzata l'API Concurrency:: Tasks disponibile a partire da Windows 8. Si noti la sintassi lambda utilizzata per incapsulare le attività di caricamento asincrono.</span><span class="sxs-lookup"><span data-stu-id="567ad-157">This example uses the Concurrency::Tasks API that is available starting in Windows 8; note the lambda syntax used to encapsulate asynchronous loading tasks.</span></span> <span data-ttu-id="567ad-158">Queste espressioni lambda rappresentano le funzioni chiamate fuori thread, quindi un puntatore all'oggetto classe corrente (**this**) viene acquisito in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="567ad-158">These lambdas represent the functions called off-thread, so a pointer to the current class object (**this**) is explicitly captured.</span></span>

<span data-ttu-id="567ad-159">Ecco un esempio di come è possibile caricare il bytecode dello shader:</span><span class="sxs-lookup"><span data-stu-id="567ad-159">Here's an example of how you can load shader bytecode:</span></span>


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



<span data-ttu-id="567ad-160">Di seguito è riportato un esempio di come creare buffer di Vertex e di indice:</span><span class="sxs-lookup"><span data-stu-id="567ad-160">Here's an example of how to create vertex and index buffers:</span></span>


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



<span data-ttu-id="567ad-161">Questo esempio non carica mesh o trame.</span><span class="sxs-lookup"><span data-stu-id="567ad-161">This example does not load any meshes or textures.</span></span> <span data-ttu-id="567ad-162">È necessario creare i metodi per caricare i tipi di trama e mesh specifici del gioco e chiamarli in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="567ad-162">You must create the methods for loading the mesh and texture types that are specific to your game, and call them asynchronously.</span></span>

<span data-ttu-id="567ad-163">Inserire qui i valori iniziali per i buffer costanti per scena.</span><span class="sxs-lookup"><span data-stu-id="567ad-163">Populate initial values for your per-scene constant buffers here, too.</span></span> <span data-ttu-id="567ad-164">Esempi di buffer di costante per scena includono luci fisse o altri elementi e dati della scena statica.</span><span class="sxs-lookup"><span data-stu-id="567ad-164">Examples of per-scene constant buffer include fixed lights, or other static scene elements and data.</span></span>

## <a name="implement-the-createwindowsizedependentresources-method"></a><span data-ttu-id="567ad-165">Implementare il metodo CreateWindowSizeDependentResources</span><span class="sxs-lookup"><span data-stu-id="567ad-165">Implement the CreateWindowSizeDependentResources method</span></span>

<span data-ttu-id="567ad-166">I metodi **CreateWindowSizeDependentResources** vengono chiamati ogni volta che le dimensioni della finestra, l'orientamento o la risoluzione cambiano.</span><span class="sxs-lookup"><span data-stu-id="567ad-166">**CreateWindowSizeDependentResources** methods are called every time the window size, orientation, or resolution changes.</span></span>

<span data-ttu-id="567ad-167">Le risorse delle dimensioni della finestra vengono aggiornate in questo modo: il processo statico del messaggio ottiene uno dei diversi eventi possibili che indicano una modifica nello stato della finestra.</span><span class="sxs-lookup"><span data-stu-id="567ad-167">Window size resources are updated like so: The static message proc gets one of several possible events indicating a change in window state.</span></span> <span data-ttu-id="567ad-168">Il ciclo principale viene quindi informato sull'evento e chiama **CreateWindowSizeDependentResources** sull'istanza della classe principale, che quindi chiama l'implementazione di **CreateWindowSizeDependentResources** nella classe renderer della scena.</span><span class="sxs-lookup"><span data-stu-id="567ad-168">Your main loop is then informed about the event and calls **CreateWindowSizeDependentResources** on the main class instance, which then calls the **CreateWindowSizeDependentResources** implementation on the scene renderer class.</span></span>

<span data-ttu-id="567ad-169">Il compito principale di questo metodo è quello di assicurarsi che gli oggetti visivi non vengano confusi o non siano validi a causa di una modifica nelle proprietà della finestra.</span><span class="sxs-lookup"><span data-stu-id="567ad-169">The primary job of this method is to make sure the visuals don't become confused or invalid because of a change in window properties.</span></span> <span data-ttu-id="567ad-170">In questo esempio vengono aggiornate le matrici di progetto con un nuovo campo di visualizzazione (FOV) per la finestra ridimensionata o riorientata.</span><span class="sxs-lookup"><span data-stu-id="567ad-170">In this example, we update the project matrices with a new field of view (FOV) for the resized or reoriented window.</span></span>

<span data-ttu-id="567ad-171">È già stato illustrato il codice per la creazione di risorse della finestra in **DeviceResources** , ovvero la catena di scambio (con buffer nascosto) e la visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="567ad-171">We already saw the code for creating window resources in **DeviceResources** - that was the swap chain (with back buffer) and render target view.</span></span> <span data-ttu-id="567ad-172">Ecco come il renderer crea le trasformazioni dipendenti dalle proporzioni:</span><span class="sxs-lookup"><span data-stu-id="567ad-172">Here's how the renderer creates aspect ratio-dependent transforms:</span></span>


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



<span data-ttu-id="567ad-173">Se la scena dispone di un layout specifico di componenti che dipendono dalle proporzioni, questo è il punto in cui riordinarle in modo che corrispondano a tali proporzioni.</span><span class="sxs-lookup"><span data-stu-id="567ad-173">If your scene has a specific layout of components that depends on the aspect ratio, this is the place to rearrange them to match that aspect ratio.</span></span> <span data-ttu-id="567ad-174">Potrebbe essere necessario modificare la configurazione del comportamento di post-elaborazione anche qui.</span><span class="sxs-lookup"><span data-stu-id="567ad-174">You may want to change the configuration of post-processing behavior here also.</span></span>

## <a name="implement-the-update-method"></a><span data-ttu-id="567ad-175">Implementare il metodo Update</span><span class="sxs-lookup"><span data-stu-id="567ad-175">Implement the Update method</span></span>

<span data-ttu-id="567ad-176">Il metodo **Update** viene chiamato una volta per ogni ciclo di gioco, in questo esempio viene chiamato dal metodo della classe principale con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="567ad-176">The **Update** method is called once per game loop - in this example, it is called by the main class's method of the same name.</span></span> <span data-ttu-id="567ad-177">Ha uno scopo semplice: aggiornare la geometria della scena e lo stato del gioco in base alla quantità di tempo trascorso (o passaggi temporali passati) rispetto al frame precedente.</span><span class="sxs-lookup"><span data-stu-id="567ad-177">It has a simple purpose: update scene geometry and game state based on the amount of elapsed time (or elapsed time steps) since the previous frame.</span></span> <span data-ttu-id="567ad-178">In questo esempio il cubo viene semplicemente ruotato una volta per frame.</span><span class="sxs-lookup"><span data-stu-id="567ad-178">In this example, we simply rotate the cube once per frame.</span></span> <span data-ttu-id="567ad-179">In una scena di gioco reale, questo metodo contiene molto altro codice per il controllo dello stato del gioco, l'aggiornamento di buffer costanti per fotogramma (o altri), i buffer di geometria e altri asset in memoria di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="567ad-179">In a real game scene, this method contains a lot more code for checking game state, updating per-frame (or other dynamic) constant buffers, geometry buffers, and other in-memory assets accordingly.</span></span> <span data-ttu-id="567ad-180">Poiché la comunicazione tra la CPU e la GPU comporta un sovraccarico, assicurarsi di aggiornare solo i buffer che sono stati effettivamente modificati dall'ultimo frame. i buffer costanti possono essere raggruppati o divisi in base alle esigenze per renderli più efficienti.</span><span class="sxs-lookup"><span data-stu-id="567ad-180">Since communication between the CPU and GPU incurs overhead, make sure you only update buffers that have actually changed since the last frame - your constant buffers can be grouped, or split up, as needed to make this more efficient.</span></span>


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



<span data-ttu-id="567ad-181">In tal caso, **ruotare** aggiorna il buffer costante con una nuova matrice di trasformazione per il cubo.</span><span class="sxs-lookup"><span data-stu-id="567ad-181">In this case, **Rotate** updates the constant buffer with a new transformation matrix for the cube.</span></span> <span data-ttu-id="567ad-182">La matrice verrà moltiplicata per ogni vertice durante la fase vertex shader.</span><span class="sxs-lookup"><span data-stu-id="567ad-182">The matrix will be multiplied per-vertex during the vertex shader stage.</span></span> <span data-ttu-id="567ad-183">Poiché questo metodo viene chiamato con ogni frame, si tratta di una posizione ideale per aggregare tutti i metodi che aggiornano i buffer delle costanti e dei vertici dinamici o per eseguire altre operazioni che preparano gli oggetti nella scena per la trasformazione da parte della pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="567ad-183">Since this method is called with every frame, this is a good place to aggregate any methods that update your dynamic constant and vertex buffers, or to perform any other operations that prepare the objects in the scene for transformation by the graphics pipeline.</span></span>

## <a name="implement-the-render-method"></a><span data-ttu-id="567ad-184">Implementare il metodo Render</span><span class="sxs-lookup"><span data-stu-id="567ad-184">Implement the Render method</span></span>

<span data-ttu-id="567ad-185">Questo metodo viene chiamato una volta per ogni ciclo di gioco dopo aver chiamato **Update**.</span><span class="sxs-lookup"><span data-stu-id="567ad-185">This method is called once per game loop after calling **Update**.</span></span> <span data-ttu-id="567ad-186">Come **Update**, anche il metodo **Render** viene chiamato dalla classe principale.</span><span class="sxs-lookup"><span data-stu-id="567ad-186">Like **Update**, the **Render** method is also called from the main class.</span></span> <span data-ttu-id="567ad-187">Si tratta del metodo in cui la pipeline grafica viene costruita ed elaborata per il frame mediante i metodi dell'istanza [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .</span><span class="sxs-lookup"><span data-stu-id="567ad-187">This is the method where the graphics pipeline is constructed and processed for the frame using methods on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) instance.</span></span> <span data-ttu-id="567ad-188">Questo culmine in una chiamata finale a [**sul ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span><span class="sxs-lookup"><span data-stu-id="567ad-188">This culminates in a final call to [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span></span> <span data-ttu-id="567ad-189">È importante tenere presente che questa chiamata (o altre **\* *chiamate di tipo di definizione di tipo _* sul ID3D11DeviceContext**) esegue effettivamente la pipeline.</span><span class="sxs-lookup"><span data-stu-id="567ad-189">It’s important to understand that this call (or other similar \**Draw\**_ calls defined on _\* ID3D11DeviceContext\*\*) actually executes the pipeline.</span></span> <span data-ttu-id="567ad-190">In particolare, quando Direct3D comunica con la GPU per impostare lo stato di disegno, esegue ogni fase della pipeline e scrive i risultati dei pixel nella risorsa del buffer di destinazione di rendering per la visualizzazione da parte della catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="567ad-190">Specifically, this is when Direct3D communicates with the GPU to set drawing state, runs each pipeline stage, and writes the pixel results into the render-target buffer resource for display by the swap chain.</span></span> <span data-ttu-id="567ad-191">Poiché la comunicazione tra la CPU e la GPU comporta un sovraccarico, combinare più chiamate di disegna in una sola, se possibile, soprattutto se la scena ha molti oggetti di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="567ad-191">Since communication between the CPU and GPU incurs overhead, combine multiple draw calls into a single one if you can, especially if your scene has a lot of rendered objects.</span></span>


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



<span data-ttu-id="567ad-192">È consigliabile impostare le varie fasi della pipeline grafica sul contesto in ordine.</span><span class="sxs-lookup"><span data-stu-id="567ad-192">It's good practice to set the various graphics pipeline stages on the context in order.</span></span> <span data-ttu-id="567ad-193">In genere, l'ordine è:</span><span class="sxs-lookup"><span data-stu-id="567ad-193">Typically, the order is:</span></span>

-   <span data-ttu-id="567ad-194">Aggiornare le risorse del buffer costante con nuovi dati in base alle esigenze (usando i dati dell' **aggiornamento**).</span><span class="sxs-lookup"><span data-stu-id="567ad-194">Refresh constant buffer resources with new data as needed (using data from **Update**).</span></span>
-   <span data-ttu-id="567ad-195">Assembly di input (IA): questa è la posizione in cui vengono collegati i buffer di Vertex e index che definiscono la geometria della scena.</span><span class="sxs-lookup"><span data-stu-id="567ad-195">Input assembly (IA): This is where we attach the vertex and index buffers that define the scene geometry.</span></span> <span data-ttu-id="567ad-196">È necessario alleghi ogni Vertex e buffer di indice per ogni oggetto nella scena.</span><span class="sxs-lookup"><span data-stu-id="567ad-196">You need to attach each vertex and index buffer for each object in the scene.</span></span> <span data-ttu-id="567ad-197">Poiché questo esempio ha solo il cubo, è piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="567ad-197">Because this example has just the cube, it's pretty simple.</span></span>
-   <span data-ttu-id="567ad-198">Vertex shader (VS): alleghi tutti i vertex shader che trasformeranno i dati nei buffer dei vertici e allegherà i buffer costanti per il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="567ad-198">Vertex shader (VS): Attach any vertex shaders that will transform the data in the vertex buffers, and attach constant buffers for the vertex shader.</span></span>
-   <span data-ttu-id="567ad-199">Pixel shader (PS): alleghi qualsiasi pixel shader che eseguirà operazioni per pixel nella scena rasterizzata e collegherà le risorse del dispositivo per il pixel shader (buffer costanti, trame e così via).</span><span class="sxs-lookup"><span data-stu-id="567ad-199">Pixel shader (PS): Attach any pixel shaders that will perform per-pixel operations in the rasterized scene, and attach device resources for the pixel shader (constant buffers, textures, and so on).</span></span>
-   <span data-ttu-id="567ad-200">Merge di output (OM): questa è la fase in cui si fondono i pixel, al termine degli shader.</span><span class="sxs-lookup"><span data-stu-id="567ad-200">Output merger (OM): This is the stage where pixels are blended, after the shaders are finished.</span></span> <span data-ttu-id="567ad-201">Si tratta di un'eccezione alla regola, perché si allineano gli stencil di profondità e le destinazioni di rendering prima di impostare le altre fasi.</span><span class="sxs-lookup"><span data-stu-id="567ad-201">This is an exception to the rule, because you attach your depth stencils and render targets before setting any of the other stages.</span></span> <span data-ttu-id="567ad-202">È possibile disporre di più stencil e destinazioni se si dispone di vertex shader e pixel shader aggiuntivi che generano trame, ad esempio mappe Shadow, mappe di altezza o altre tecniche di campionamento, in questo caso, per ogni passaggio di disegno sarà necessario impostare la destinazione o le destinazioni appropriate prima di chiamare una funzione di disegno.</span><span class="sxs-lookup"><span data-stu-id="567ad-202">You may have multiple stencils and targets if you have additional vertex and pixel shaders that generate textures such as shadow maps, height maps, or other sampling techniques - in this case, each drawing pass will need the appropriate target(s) set before you call a draw function.</span></span>

<span data-ttu-id="567ad-203">Successivamente, nella sezione finale ([usare shader e risorse shader](work-with-shaders-and-shader-resources.md)) verranno esaminati gli shader e verrà illustrato come Direct3D li esegue.</span><span class="sxs-lookup"><span data-stu-id="567ad-203">Next, in the final section ([Work with shaders and shader resources](work-with-shaders-and-shader-resources.md)), we'll look at the shaders and discuss how Direct3D executes them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="567ad-204">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="567ad-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="567ad-205">**Successivo**</span><span class="sxs-lookup"><span data-stu-id="567ad-205">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="567ad-206">Usare shader e risorse shader</span><span class="sxs-lookup"><span data-stu-id="567ad-206">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
