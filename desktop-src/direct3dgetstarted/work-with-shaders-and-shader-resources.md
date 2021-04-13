---
title: Usare shader e risorse shader
description: È giunto il momento di imparare a usare shader e risorse dello shader per lo sviluppo di Microsoft DirectX Game per Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac147971221b04b02f2a45af8e8d4f6855a5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399223"
---
# <a name="work-with-shaders-and-shader-resources"></a><span data-ttu-id="eb774-103">Usare shader e risorse shader</span><span class="sxs-lookup"><span data-stu-id="eb774-103">Work with shaders and shader resources</span></span>

<span data-ttu-id="eb774-104">È giunto il momento di imparare a usare shader e risorse dello shader per lo sviluppo di Microsoft DirectX Game per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eb774-104">It's time to learn how to work with shaders and shader resources in developing your Microsoft DirectX game for Windows 8.</span></span> <span data-ttu-id="eb774-105">È stato illustrato come configurare il dispositivo e le risorse di grafica ed è possibile che sia stata avviata anche la modifica della pipeline.</span><span class="sxs-lookup"><span data-stu-id="eb774-105">We've seen how to set up the graphics device and resources, and perhaps you've even started modifying its pipeline.</span></span> <span data-ttu-id="eb774-106">Verranno ora esaminati i pixel e i vertex shader.</span><span class="sxs-lookup"><span data-stu-id="eb774-106">So now let's look at pixel and vertex shaders.</span></span>

<span data-ttu-id="eb774-107">Se non si ha familiarità con i linguaggi shader, una discussione rapida è in ordine.</span><span class="sxs-lookup"><span data-stu-id="eb774-107">If you aren't familiar with shader languages, a quick discussion is in order.</span></span> <span data-ttu-id="eb774-108">Gli shader sono piccoli programmi di basso livello compilati ed eseguiti in fasi specifiche della pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="eb774-108">Shaders are small, low-level programs that are compiled and run at specific stages in the graphics pipeline.</span></span> <span data-ttu-id="eb774-109">La loro specialità è operazioni matematiche a virgola mobile molto veloci.</span><span class="sxs-lookup"><span data-stu-id="eb774-109">Their specialty is very fast floating-point mathematical operations.</span></span> <span data-ttu-id="eb774-110">I programmi shader più comuni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb774-110">The most common shader programs are:</span></span>

-   <span data-ttu-id="eb774-111">**Vertex shader**: eseguito per ogni vertice in una scena.</span><span class="sxs-lookup"><span data-stu-id="eb774-111">**Vertex shader**—Executed for each vertex in a scene.</span></span> <span data-ttu-id="eb774-112">Questo shader agisce sugli elementi del buffer dei vertici forniti dall'app chiamante e produce almeno un vettore di posizione a 4 componenti che verrà rasterizzato in una posizione in pixel.</span><span class="sxs-lookup"><span data-stu-id="eb774-112">This shader operates on vertex buffer elements provided to it by the calling app, and minimally results in a 4-component position vector that will be rasterized into a pixel position.</span></span>
-   <span data-ttu-id="eb774-113">**Pixel shader**: eseguito per ogni pixel in una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="eb774-113">**Pixel shader**—Executed for each pixel in a render target.</span></span> <span data-ttu-id="eb774-114">Questo shader riceve le coordinate rasterizzate dalle fasi precedenti dello shader (nelle pipeline più semplici, questo sarebbe il vertex shader) e restituisce un colore (o un altro valore a 4 componenti) per tale posizione in pixel, che viene quindi scritta in una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="eb774-114">This shader receives rasterized coordinates from previous shader stages (in the simplest pipelines, this would be the vertex shader) and returns a color (or other 4-component value) for that pixel position, which is then written into a render target.</span></span>

<span data-ttu-id="eb774-115">Questo esempio include vertex shader e pixel shader di base che attingono solo la geometria e shader più complessi che aggiungono calcoli di illuminazione di base.</span><span class="sxs-lookup"><span data-stu-id="eb774-115">This example includes very basic vertex and pixel shaders that only draw geometry, and more complex shaders that add basic lighting calculations.</span></span>

<span data-ttu-id="eb774-116">I programmi shader sono scritti in Microsoft High Level Shader Language (HLSL).</span><span class="sxs-lookup"><span data-stu-id="eb774-116">Shader programs are written in Microsoft High Level Shader Language (HLSL).</span></span> <span data-ttu-id="eb774-117">La sintassi di HLSL ha un aspetto molto simile a C, ma senza i puntatori.</span><span class="sxs-lookup"><span data-stu-id="eb774-117">HLSL syntax looks a lot like C, but without the pointers.</span></span> <span data-ttu-id="eb774-118">I programmi shader devono essere molto compatta ed efficiente.</span><span class="sxs-lookup"><span data-stu-id="eb774-118">Shader programs must be very compact and efficient.</span></span> <span data-ttu-id="eb774-119">Se lo shader viene compilato in un numero eccessivo di istruzioni, non può essere eseguito e viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="eb774-119">If your shader compiles to too many instructions, it cannot be run and an error is returned.</span></span> <span data-ttu-id="eb774-120">Si noti che il numero esatto di istruzioni consentito è parte del [livello di funzionalità Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).</span><span class="sxs-lookup"><span data-stu-id="eb774-120">(Note that the exact number of instructions allowed is part of the [Direct3D feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span></span>

<span data-ttu-id="eb774-121">In Direct3D gli shader non vengono compilati in fase di esecuzione. vengono compilati quando viene compilato il resto del programma.</span><span class="sxs-lookup"><span data-stu-id="eb774-121">In Direct3D, shaders are not compiled at run time; they are compiled when the rest of the program is compiled.</span></span> <span data-ttu-id="eb774-122">Quando si compila l'app con Microsoft Visual Studio 2013, i file HLSL vengono compilati in file CSO (. CSO) che l'app deve caricare e inserire nella memoria GPU prima del disegno.</span><span class="sxs-lookup"><span data-stu-id="eb774-122">When you compile your app with Microsoft Visual Studio 2013, the HLSL files are compiled to CSO (.cso) files that your app must load and place in GPU memory prior to drawing.</span></span> <span data-ttu-id="eb774-123">Quando si crea un pacchetto, assicurarsi di includere i file CSO con l'app. si tratta di asset come mesh e trame.</span><span class="sxs-lookup"><span data-stu-id="eb774-123">Make sure you include these CSO files with your app when you package it; they are assets just like meshes and textures.</span></span>

## <a name="understand-hlsl-semantics"></a><span data-ttu-id="eb774-124">Comprendere la semantica di HLSL</span><span class="sxs-lookup"><span data-stu-id="eb774-124">Understand HLSL semantics</span></span>

<span data-ttu-id="eb774-125">Prima di continuare, è importante esaminare la semantica di HLSL, perché spesso si tratta di un punto di confusione per i nuovi sviluppatori Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb774-125">It's important to take a moment to discuss HLSL semantics before we continue, because they are often a point of confusion for new Direct3D developers.</span></span> <span data-ttu-id="eb774-126">La semantica di HLSL sono stringhe che identificano un valore passato tra l'app e un programma shader.</span><span class="sxs-lookup"><span data-stu-id="eb774-126">HLSL semantics are strings that identify a value passed between the app and a shader program.</span></span> <span data-ttu-id="eb774-127">Sebbene possano essere diverse stringhe possibili, la procedura consigliata consiste nell'usare una stringa come `POSITION` o `COLOR` che indichi l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="eb774-127">Although they can be any of a variety of possible strings, the best practice is to use a string like `POSITION` or `COLOR` that indicates the usage.</span></span> <span data-ttu-id="eb774-128">Questa semantica viene assegnata quando si costruisce un buffer costante o un layout di input.</span><span class="sxs-lookup"><span data-stu-id="eb774-128">You assign these semantics when you are constructing a constant buffer or input layout.</span></span> <span data-ttu-id="eb774-129">Puoi anche aggiungere un numero compreso tra 0 e 7 alla semantica in modo da usare registri separati per valori simili.</span><span class="sxs-lookup"><span data-stu-id="eb774-129">You can also append a number between 0 and 7 to the semantic so that you use separate registers for similar values.</span></span> <span data-ttu-id="eb774-130">Ad esempio: COLOR0, COLOR1, COLOR2...</span><span class="sxs-lookup"><span data-stu-id="eb774-130">For example: COLOR0, COLOR1, COLOR2...</span></span>

<span data-ttu-id="eb774-131">La semantica che è preceduta da "SV \_ " è la semantica del *valore di sistema* che viene scritta dal programma shader; il gioco stesso (in esecuzione sulla CPU) non può modificarli.</span><span class="sxs-lookup"><span data-stu-id="eb774-131">Semantics that are prefixed with "SV\_" are *system value* semantics that are written to by your shader program; your game itself (running on the CPU) cannot modify them.</span></span> <span data-ttu-id="eb774-132">In genere, queste semantiche contengono valori che sono input o output di un'altra fase shader nella pipeline grafica o che vengono generati interamente dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="eb774-132">Typically, these semantics contain values that are inputs or outputs from another shader stage in the graphics pipeline, or that are generated entirely by the GPU.</span></span>

<span data-ttu-id="eb774-133">Inoltre, `SV_` la semantica ha comportamenti diversi quando vengono usati per specificare l'input o l'output da una fase dello shader.</span><span class="sxs-lookup"><span data-stu-id="eb774-133">Additionally, `SV_` semantics have different behaviors when they are used to specify input to or output from a shader stage.</span></span> <span data-ttu-id="eb774-134">Ad esempio, `SV_POSITION` (output) contiene i dati dei vertici trasformati durante la fase vertex shader e `SV_POSITION` (*input*) contiene i valori di posizione dei pixel interpolati dalla GPU durante la fase di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="eb774-134">For example, `SV_POSITION` (output) contains the vertex data transformed during the vertex shader stage, and `SV_POSITION` (*input*) contains the pixel position values that were interpolated by the GPU during the rasterization stage.</span></span>

<span data-ttu-id="eb774-135">Ecco alcune comuni semantica di HLSL:</span><span class="sxs-lookup"><span data-stu-id="eb774-135">Here are a few common HLSL semantics:</span></span>

-   <span data-ttu-id="eb774-136">`POSITION`(*n*) per i dati del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="eb774-136">`POSITION`(*n*) for vertex buffer data.</span></span> <span data-ttu-id="eb774-137">`SV_POSITION` fornisce una posizione in pixel per la pixel shader e non può essere scritta dal gioco.</span><span class="sxs-lookup"><span data-stu-id="eb774-137">`SV_POSITION` provides a pixel position to the pixel shader and cannot be written by your game.</span></span>
-   <span data-ttu-id="eb774-138">`NORMAL`(*n*) per i dati normali forniti dal buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="eb774-138">`NORMAL`(*n*) for normal data provided by the vertex buffer.</span></span>
-   <span data-ttu-id="eb774-139">`TEXCOORD`(*n*) per i dati della coordinata UV della trama forniti a uno shader.</span><span class="sxs-lookup"><span data-stu-id="eb774-139">`TEXCOORD`(*n*) for texture UV coordinate data supplied to a shader.</span></span>
-   <span data-ttu-id="eb774-140">`COLOR`(n) per i dati dei colori RGBA forniti a uno shader.</span><span class="sxs-lookup"><span data-stu-id="eb774-140">`COLOR`(n) for RGBA color data supplied to a shader.</span></span> <span data-ttu-id="eb774-141">Si noti che viene trattato in modo identico per le coordinate dei dati, inclusa l'interpolazione del valore durante la rasterizzazione; la semantica semplifica semplicemente l'identificazione dei dati di colore.</span><span class="sxs-lookup"><span data-stu-id="eb774-141">Note that it is treated identically to coordinate data, including interpolating the value during rasterization; the semantic simply helps you identify that it is color data.</span></span>
-   <span data-ttu-id="eb774-142">`SV_Target`\[n \] per la scrittura da un pixel shader a una trama di destinazione o un altro buffer pixel.</span><span class="sxs-lookup"><span data-stu-id="eb774-142">`SV_Target`\[n\] for writing from a pixel shader to a target texture or other pixel buffer.</span></span>

<span data-ttu-id="eb774-143">Verranno illustrati alcuni esempi di semantica di HLSL quando si esamina l'esempio.</span><span class="sxs-lookup"><span data-stu-id="eb774-143">We'll see some examples of HLSL semantics as we review the example.</span></span>

## <a name="read-from-the-constant-buffers"></a><span data-ttu-id="eb774-144">Lettura dai buffer costanti</span><span class="sxs-lookup"><span data-stu-id="eb774-144">Read from the constant buffers</span></span>

<span data-ttu-id="eb774-145">Qualsiasi shader può leggere da un buffer costante se tale buffer è collegato alla propria fase come risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb774-145">Any shader can read from a constant buffer if that buffer is attached to its stage as a resource.</span></span> <span data-ttu-id="eb774-146">In questo esempio solo al vertex shader viene assegnato un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="eb774-146">In this example, only the vertex shader is assigned a constant buffer.</span></span>

<span data-ttu-id="eb774-147">Il buffer costante viene dichiarato in due posizioni: nel codice C++ e nei file HLSL corrispondenti che lo accederanno.</span><span class="sxs-lookup"><span data-stu-id="eb774-147">The constant buffer is declared in two places: in the C++ code, and in the corresponding HLSL files that will access it.</span></span>

<span data-ttu-id="eb774-148">Di seguito viene illustrato il modo in cui viene dichiarata la struttura del buffer costante nel codice C++.</span><span class="sxs-lookup"><span data-stu-id="eb774-148">Here's how the constant buffer struct is declared in the C++ code.</span></span>


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



<span data-ttu-id="eb774-149">Quando si dichiara la struttura per il buffer costante nel codice C++, assicurarsi che tutti i dati siano allineati correttamente lungo i limiti di 16 byte.</span><span class="sxs-lookup"><span data-stu-id="eb774-149">When declaring the structure for the constant buffer in your C++ code, ensure that all of the data is correctly aligned along 16-byte boundaries.</span></span> <span data-ttu-id="eb774-150">Il modo più semplice per eseguire questa operazione consiste nell'usare i tipi [DirectXMath](/windows/desktop/dxmath/directxmath-portal) , come **XMFLOAT4** o **XMFLOAT4X4**, come illustrato nel codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="eb774-150">The easiest way to do this is to use [DirectXMath](/windows/desktop/dxmath/directxmath-portal) types, like **XMFLOAT4** or **XMFLOAT4X4**, as seen in the example code.</span></span> <span data-ttu-id="eb774-151">È inoltre possibile proteggere i buffer non allineati dichiarando un'asserzione statica:</span><span class="sxs-lookup"><span data-stu-id="eb774-151">You can also guard against misaligned buffers by declaring a static assert:</span></span>


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



<span data-ttu-id="eb774-152">Questa riga di codice provocherà un errore in fase di compilazione se **ConstantBufferStruct** non è allineato a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="eb774-152">This line of code will cause an error at compile time if **ConstantBufferStruct** is not 16-byte aligned.</span></span> <span data-ttu-id="eb774-153">Per ulteriori informazioni sull'allineamento e la compressione costanti del buffer, vedere [regole di compressione per variabili costanti](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="eb774-153">For more information about constant buffer alignment and packing, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

<span data-ttu-id="eb774-154">A questo punto, di seguito viene illustrato il modo in cui viene dichiarato il buffer costante nel HLSL vertex shader.</span><span class="sxs-lookup"><span data-stu-id="eb774-154">Now, here's how the constant buffer is declared in the vertex shader HLSL.</span></span>


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



<span data-ttu-id="eb774-155">Tutti i buffer: costante, trama, campionatore o altro, devono avere un registro definito in modo che la GPU possa accedervi.</span><span class="sxs-lookup"><span data-stu-id="eb774-155">All buffers—constant, texture, sampler, or other—must have a register defined so the GPU can access them.</span></span> <span data-ttu-id="eb774-156">Ogni fase dello shader consente fino a 15 buffer costanti e ogni buffer può ospitare fino a 4.096 variabili costanti.</span><span class="sxs-lookup"><span data-stu-id="eb774-156">Each shader stage allows up to 15 constant buffers, and each buffer can hold up to 4,096 constant variables.</span></span> <span data-ttu-id="eb774-157">La sintassi della dichiarazione Register-Usage è la seguente:</span><span class="sxs-lookup"><span data-stu-id="eb774-157">The register-usage declaration syntax is as follows:</span></span>

-   <span data-ttu-id="eb774-158">**b \* \* *\#* : un registro per un buffer costante (** cbuffer \* \*).</span><span class="sxs-lookup"><span data-stu-id="eb774-158">**b\*\**\#*: A register for a constant buffer (** cbuffer\*\*).</span></span>
-   <span data-ttu-id="eb774-159">**t \* \* *\#* : un registro per un buffer di trama (** tbuffer \* \*).</span><span class="sxs-lookup"><span data-stu-id="eb774-159">**t\*\**\#*: A register for a texture buffer (** tbuffer\*\*).</span></span>
-   <span data-ttu-id="eb774-160">\**s \* \* \* \#*: un registro per un campionatore.</span><span class="sxs-lookup"><span data-stu-id="eb774-160">\**s\*\*\*\#*: A register for a sampler.</span></span> <span data-ttu-id="eb774-161">Un campionatore definisce il comportamento di ricerca per i Texel nella risorsa di trama.</span><span class="sxs-lookup"><span data-stu-id="eb774-161">(A sampler defines the lookup behavior for texels in the texture resource.)</span></span>

<span data-ttu-id="eb774-162">Ad esempio, HLSL per un pixel shader potrebbe richiedere una trama e un campionatore come input con una dichiarazione come questa.</span><span class="sxs-lookup"><span data-stu-id="eb774-162">For example, the HLSL for a pixel shader might take a texture and a sampler as input with a declaration like this.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

<span data-ttu-id="eb774-163">È compito dell'utente assegnare i buffer costanti ai registri: quando si configura la pipeline, si associa un buffer costante allo stesso slot a cui è stato assegnato il file HLSL.</span><span class="sxs-lookup"><span data-stu-id="eb774-163">It's up to you to assign constant buffers to registers—when you set up the pipeline, you attach a constant buffer to the same slot you assigned it to in the HLSL file.</span></span> <span data-ttu-id="eb774-164">Nell'argomento precedente, ad esempio, la chiamata a [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indica ' 0' per il primo parametro.</span><span class="sxs-lookup"><span data-stu-id="eb774-164">For example, in the previous topic the call to [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indicates '0' for the first parameter.</span></span> <span data-ttu-id="eb774-165">Che indica a Direct3D di alleghiare la risorsa del buffer costante al registro 0, che corrisponde all'assegnazione del buffer per la **registrazione (B0)** nel file HLSL.</span><span class="sxs-lookup"><span data-stu-id="eb774-165">That tells Direct3D to attach the constant buffer resource to register 0, which matches the buffer's assignment to **register(b0)** in the HLSL file.</span></span>

## <a name="read-from-the-vertex-buffers"></a><span data-ttu-id="eb774-166">Lettura dai buffer dei vertici</span><span class="sxs-lookup"><span data-stu-id="eb774-166">Read from the vertex buffers</span></span>

<span data-ttu-id="eb774-167">Il buffer dei vertici fornisce i dati del triangolo per gli oggetti della scena ai vertex shader.</span><span class="sxs-lookup"><span data-stu-id="eb774-167">The vertex buffer supplies the triangle data for the scene objects to the vertex shader(s).</span></span> <span data-ttu-id="eb774-168">Come per il buffer costante, lo struct del buffer dei vertici viene dichiarato nel codice C++, usando regole di compressione simili.</span><span class="sxs-lookup"><span data-stu-id="eb774-168">As with the constant buffer, the vertex buffer struct is declared in the C++ code, using similar packing rules.</span></span>


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



<span data-ttu-id="eb774-169">Non esiste un formato standard per i dati dei vertici in Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="eb774-169">There is no standard format for vertex data in Direct3D 11.</span></span> <span data-ttu-id="eb774-170">Si definisce invece il layout dei dati dei vertici usando un descrittore; i campi dati vengono definiti mediante una matrice di [**strutture \_ d3d11 \_ input \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) .</span><span class="sxs-lookup"><span data-stu-id="eb774-170">Instead, we define our own vertex data layout using a descriptor; the data fields are defined using an array of [**D3D11\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) structures.</span></span> <span data-ttu-id="eb774-171">In questo esempio viene illustrato un layout di input semplice che descrive lo stesso formato di vertex dello struct precedente:</span><span class="sxs-lookup"><span data-stu-id="eb774-171">Here, we show a simple input layout that describes the same vertex format as the preceding struct:</span></span>


```C++
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
```



<span data-ttu-id="eb774-172">Se si aggiungono dati al formato vertex quando si modifica il codice di esempio, assicurarsi di aggiornare anche il layout di input oppure lo shader non sarà in grado di interpretarlo.</span><span class="sxs-lookup"><span data-stu-id="eb774-172">If you add data to the vertex format when modifying the example code, be sure to update the input layout as well, or the shader will not be able to interpret it.</span></span> <span data-ttu-id="eb774-173">È possibile modificare il layout dei vertici in questo modo:</span><span class="sxs-lookup"><span data-stu-id="eb774-173">You might modify the vertex layout like this:</span></span>


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



<span data-ttu-id="eb774-174">In tal caso, modificare la definizione del layout di input come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="eb774-174">In that case, you'd modify the input-layout definition as follows.</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



<span data-ttu-id="eb774-175">Ognuna delle definizioni degli elementi di layout di input è preceduta da una stringa, ad esempio "POSITION" o "NORMAL", che è la semantica descritta in precedenza in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="eb774-175">Each of the input-layout element definitions is prefixed with a string, like "POSITION" or "NORMAL"—that is the semantic we discussed earlier in this topic.</span></span> <span data-ttu-id="eb774-176">È come un handle che consente alla GPU di identificare tale elemento durante l'elaborazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="eb774-176">It's like a handle that helps the GPU identify that element when processing the vertex.</span></span> <span data-ttu-id="eb774-177">Scegliere nomi comuni e significativi per gli elementi del vertice.</span><span class="sxs-lookup"><span data-stu-id="eb774-177">Choose common, meaningful names for your vertex elements.</span></span>

<span data-ttu-id="eb774-178">Proprio come per il buffer costante, il vertex shader ha una definizione di buffer corrispondente per gli elementi del vertice in ingresso.</span><span class="sxs-lookup"><span data-stu-id="eb774-178">Just as with the constant buffer, the vertex shader has a corresponding buffer definition for incoming vertex elements.</span></span> <span data-ttu-id="eb774-179">Per questo motivo è stato fornito un riferimento alla risorsa vertex shader quando si crea il layout di input. Direct3D convalida il layout dei dati per vertice con lo struct di input dello shader. Si noti come la semantica corrisponda tra la definizione del layout di input e questa dichiarazione del buffer HLSL.</span><span class="sxs-lookup"><span data-stu-id="eb774-179">(That's why we provided a reference to the vertex shader resource when creating the input layout - Direct3D validates the per-vertex data layout with the shader's input struct.) Note how the semantics match between the input layout definition and this HLSL buffer declaration.</span></span> <span data-ttu-id="eb774-180">Viene tuttavia `COLOR` aggiunto un valore "0".</span><span class="sxs-lookup"><span data-stu-id="eb774-180">However, `COLOR` has a "0" appended to it.</span></span> <span data-ttu-id="eb774-181">Non è necessario aggiungere 0 se nel layout è dichiarato un solo `COLOR` elemento, ma è consigliabile aggiungerlo nel caso in cui si scelga di aggiungere altri elementi di colore in futuro.</span><span class="sxs-lookup"><span data-stu-id="eb774-181">It isn't necessary to add the 0 if you have only one `COLOR` element declared in the layout, but it's a good practice to append it in case you you choose to add more color elements in the future.</span></span>


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a><span data-ttu-id="eb774-182">Passare i dati tra gli shader</span><span class="sxs-lookup"><span data-stu-id="eb774-182">Pass data between shaders</span></span>

<span data-ttu-id="eb774-183">Gli shader accettano i tipi di input e restituiscono i tipi di output dalle funzioni principali al momento dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="eb774-183">Shaders take input types and return output types from their main functions upon execution.</span></span> <span data-ttu-id="eb774-184">Per il vertex shader definito nella sezione precedente, il tipo di input è la struttura di input di Visual Studio ed è stato \_ definito un layout di input e uno struct C++ corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="eb774-184">For the vertex shader defined in the previous section, the input type was the VS\_INPUT structure, and we defined a matching input layout and C++ struct.</span></span> <span data-ttu-id="eb774-185">Una matrice di questo struct viene utilizzata per creare un buffer vertex nel metodo **CreateCube** .</span><span class="sxs-lookup"><span data-stu-id="eb774-185">An array of this struct is used to create a vertex buffer in the **CreateCube** method.</span></span>

<span data-ttu-id="eb774-186">Il vertex shader restituisce una struttura di \_ input PS, che deve contenere almeno la posizione del vertice finale a 4 componenti (float4).</span><span class="sxs-lookup"><span data-stu-id="eb774-186">The vertex shader returns a PS\_INPUT structure, which must minimally contain the 4-component (float4) final vertex position.</span></span> <span data-ttu-id="eb774-187">Questo valore di posizione deve avere la semantica del valore di sistema, `SV_POSITION` , dichiarata in modo che la GPU disponga dei dati necessari per eseguire il passaggio successivo del disegno.</span><span class="sxs-lookup"><span data-stu-id="eb774-187">This position value must have the system value semantic, `SV_POSITION`, declared for it so the GPU has the data it needs to perform the next drawing step.</span></span> <span data-ttu-id="eb774-188">Si noti che non esiste una corrispondenza 1:1 tra l'output del vertex shader e l'input pixel shader; il vertex shader restituisce una struttura per ogni vertice assegnato, ma il pixel shader viene eseguito una volta per ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="eb774-188">Notice that there is not a 1:1 correspondence between vertex shader output and pixel shader input; the vertex shader returns one structure for each vertex it is given, but the pixel shader runs once for each pixel.</span></span> <span data-ttu-id="eb774-189">Ciò è dovuto al fatto che i dati per vertice passano per primo attraverso la fase di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="eb774-189">That's because the per-vertex data first passes through the rasterization stage.</span></span> <span data-ttu-id="eb774-190">Questa fase decide quali pixel "coprire" la geometria che si sta disegnando, calcola i dati per vertice interpolati per ogni pixel, quindi chiama il pixel shader una volta per ognuno di questi pixel.</span><span class="sxs-lookup"><span data-stu-id="eb774-190">This stage decides which pixels "cover" the geometry you're drawing, computes interpolated per-vertex data for each pixel, and then calls the pixel shader once for each of those pixels.</span></span> <span data-ttu-id="eb774-191">L'interpolazione è il comportamento predefinito quando si rasterizzano i valori di output ed è essenziale in particolare per l'elaborazione corretta dei dati vettoriali di output (vettori di luce, normali e tangenti per vertice e altri).</span><span class="sxs-lookup"><span data-stu-id="eb774-191">Interpolation is the default behavior when rasterizing output values, and is essential in particular for the correct processing of output vector data (light vectors, per-vertex normals and tangents, and others).</span></span>


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a><span data-ttu-id="eb774-192">Esaminare il vertex shader</span><span class="sxs-lookup"><span data-stu-id="eb774-192">Review the vertex shader</span></span>

<span data-ttu-id="eb774-193">Il vertex shader di esempio è molto semplice: assumere un vertice (posizione e colore), trasformare la posizione dalle coordinate del modello in coordinate proiettate prospettiche e restituirla (insieme al colore) al rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="eb774-193">The example vertex shader is very simple: take in a vertex (position and color), transform the position from model coordinates into perspective projected coordinates, and return it (along with the color) to the rasterizer.</span></span> <span data-ttu-id="eb774-194">Si noti che il valore del colore è interpolato a destra insieme ai dati di posizione, fornendo un valore diverso per ogni pixel anche se il vertex shader non ha eseguito calcoli sul valore del colore.</span><span class="sxs-lookup"><span data-stu-id="eb774-194">Notice that the color value is interpolated right along with the position data, providing a different value for each pixel even though the vertex shader didn't perform any calculations on the color value.</span></span>


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



<span data-ttu-id="eb774-195">Un vertex shader più complesso, ad esempio uno che imposta i vertici di un oggetto per l'ombreggiatura Phong, potrebbe avere un aspetto simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="eb774-195">A more complex vertex shader, such as one that sets up an object's vertices for Phong shading, might look more like this.</span></span> <span data-ttu-id="eb774-196">In questo caso, si sta sfruttando il fatto che i vettori e le normali vengono interpolati per approssimarsi a una superficie di aspetto uniforme.</span><span class="sxs-lookup"><span data-stu-id="eb774-196">In this case, we're taking advantage of the fact that the vectors and normals are interpolated to approximate a smooth-looking surface.</span></span>

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a><span data-ttu-id="eb774-197">Esaminare il pixel shader</span><span class="sxs-lookup"><span data-stu-id="eb774-197">Review the pixel shader</span></span>

<span data-ttu-id="eb774-198">Questo pixel shader in questo esempio è probabilmente la quantità minima assoluta di codice che è possibile avere in una pixel shader.</span><span class="sxs-lookup"><span data-stu-id="eb774-198">This pixel shader in this example is quite possibly the absolute minimum amount of code you can have in a pixel shader.</span></span> <span data-ttu-id="eb774-199">Accetta i dati del colore del pixel interpolati generati durante la rasterizzazione e li restituisce come output, dove verranno scritti in una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="eb774-199">It takes the interpolated pixel color data generated during rasterization and returns it as output, where it will be written to a render target.</span></span> <span data-ttu-id="eb774-200">Quanto è noioso!</span><span class="sxs-lookup"><span data-stu-id="eb774-200">How boring!</span></span>


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



<span data-ttu-id="eb774-201">La parte importante è la `SV_TARGET` semantica del valore del sistema sul valore restituito.</span><span class="sxs-lookup"><span data-stu-id="eb774-201">The important part is the `SV_TARGET` system-value semantic on the return value.</span></span> <span data-ttu-id="eb774-202">Indica che l'output deve essere scritto nella destinazione di rendering primaria, ovvero il buffer di trama fornito alla catena di scambio per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="eb774-202">It indicates that the output is to be written to the primary render target, which is the texture buffer supplied to the swap chain for display.</span></span> <span data-ttu-id="eb774-203">Questa operazione è necessaria per i pixel shader, senza i dati relativi al colore dal pixel shader, Direct3D non avrà alcun elemento da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="eb774-203">This is required for pixel shaders - without the color data from the pixel shader, Direct3D wouldn't have anything to display!</span></span>

<span data-ttu-id="eb774-204">Un esempio di pixel shader più complesso per eseguire l'ombreggiatura Phong potrebbe essere simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="eb774-204">An example of a more complex pixel shader to perform Phong shading might look like this.</span></span> <span data-ttu-id="eb774-205">Poiché i vettori e le normali sono stati interpolati, non è necessario calcolarli in base ai singoli pixel.</span><span class="sxs-lookup"><span data-stu-id="eb774-205">Since the vectors and normals were interpolated, we don't have to compute them on a per-pixel basis.</span></span> <span data-ttu-id="eb774-206">Tuttavia, è necessario rinormalizzarli a causa del funzionamento dell'interpolazione. dal punto di vista concettuale, è necessario "ruotare" gradualmente il vettore dalla direzione del vertice a fino alla direzione del vertice B, mantenendo la relativa lunghezza. l'interpolazione considerando taglia invece una linea retta tra i due endpoint vettoriali.</span><span class="sxs-lookup"><span data-stu-id="eb774-206">However, we do have to re-normalize them because of how interpolation works; conceptually, we need to gradually "spin" the vector from direction at vertex A to direction at vertex B, maintaining its length—wheras interpolation instead cuts across a straight line between the two vector endpoints.</span></span>

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

<span data-ttu-id="eb774-207">In un altro esempio, il pixel shader prende i propri buffer costanti che contengono informazioni leggere e materiali.</span><span class="sxs-lookup"><span data-stu-id="eb774-207">In another example, the pixel shader takes its own constant buffers that contain light and material information.</span></span> <span data-ttu-id="eb774-208">Il layout di input nel vertex shader verrebbe espanso in modo da includere i dati normali e l'output del vertex shader dovrebbe includere vettori trasformati per il vertice, la luce e il vertice normale nel sistema di coordinate di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="eb774-208">The input layout in the vertex shader would be expanded to include normal data, and the output from that vertex shader is expected to include transformed vectors for the vertex, the light, and the vertex normal in the view coordinate system.</span></span>

<span data-ttu-id="eb774-209">Se sono presenti buffer di trama e sampler con registri assegnati (rispettivamente **t** e **s**), è possibile accedervi anche nel pixel shader.</span><span class="sxs-lookup"><span data-stu-id="eb774-209">If you have texture buffers and samplers with assigned registers (**t** and **s**, respectively), you can access them in the pixel shader also.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

<span data-ttu-id="eb774-210">Gli shader sono strumenti molto potenti che possono essere usati per generare risorse procedurali come mappe Shadow o trame non significative.</span><span class="sxs-lookup"><span data-stu-id="eb774-210">Shaders are very powerful tools that can be used to generate procedural resources like shadow maps or noise textures.</span></span> <span data-ttu-id="eb774-211">Infatti, le tecniche avanzate richiedono che si pensi alle trame in modo più astratto, non come elementi visivi, ma come buffer.</span><span class="sxs-lookup"><span data-stu-id="eb774-211">In fact, advanced techniques require that you think of textures more abstractly, not as visual elements but as buffers.</span></span> <span data-ttu-id="eb774-212">Mantengono i dati, ad esempio le informazioni sull'altezza, o altri dati che possono essere campionati nel passaggio finale pixel shader o in quel particolare frame come parte di una sessione di effetti in più fasi.</span><span class="sxs-lookup"><span data-stu-id="eb774-212">They hold data like height information, or other data that can be sampled in the final pixel shader pass or in that particular frame as part of a multi-stage effects pass.</span></span> <span data-ttu-id="eb774-213">Il campionamento multiplo è uno strumento potente e il backbone di molti effetti visivi moderni.</span><span class="sxs-lookup"><span data-stu-id="eb774-213">Multi-sampling is a powerful tool and the backbone of many modern visual effects.</span></span>

## <a name="next-steps"></a><span data-ttu-id="eb774-214">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="eb774-214">Next steps</span></span>

<span data-ttu-id="eb774-215">È probabile che l'utente abbia familiarità con DirectX 11at questo punto e sia pronto per iniziare a lavorare sul progetto.</span><span class="sxs-lookup"><span data-stu-id="eb774-215">Hopefully, you're comfortable with DirectX 11at this point and are ready to start working on your project.</span></span> <span data-ttu-id="eb774-216">Di seguito sono riportati alcuni collegamenti che consentono di rispondere ad altre domande che possono verificarsi sullo sviluppo con DirectX e C++:</span><span class="sxs-lookup"><span data-stu-id="eb774-216">Here are some links to help answer other questions you may have about development with DirectX and C++:</span></span>

-   <span data-ttu-id="eb774-217">[Sviluppo di giochi](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="eb774-217">[Developing games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="eb774-218">[Usare gli strumenti di Visual Studio per la programmazione dei giochi DirectX](/previous-versions/windows/apps/dn166877(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="eb774-218">[Use Visual Studio tools for DirectX game programming](/previous-versions/windows/apps/dn166877(v=win.10))</span></span>
-   <span data-ttu-id="eb774-219">[Procedure dettagliate per lo sviluppo di giochi DirectX e esempi](/previous-versions/windows/apps/hh465149(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="eb774-219">[DirectX game development and sample walkthroughs](/previous-versions/windows/apps/hh465149(v=win.10))</span></span>
-   <span data-ttu-id="eb774-220">[Risorse aggiuntive per la programmazione di giochi](/previous-versions/windows/apps/dn194515(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="eb774-220">[Additional game programming resources](/previous-versions/windows/apps/dn194515(v=win.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb774-221">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb774-221">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb774-222">Usare le risorse del dispositivo DirectX</span><span class="sxs-lookup"><span data-stu-id="eb774-222">Work with DirectX device resources</span></span>](work-with-dxgi.md)
</dt> <dt>

[<span data-ttu-id="eb774-223">Informazioni sulla pipeline di rendering Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="eb774-223">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 