---
title: Attività iniziali con la fase Stream-Output lavoro
description: Questa sezione descrive come usare uno shader geometry con la fase di output del flusso.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2e72d25177926c948f43996b6c57d42a7c557b
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587878"
---
# <a name="getting-started-with-the-stream-output-stage"></a><span data-ttu-id="d07d0-103">Attività iniziali con la fase Stream-Output lavoro</span><span class="sxs-lookup"><span data-stu-id="d07d0-103">Getting Started with the Stream-Output Stage</span></span>

<span data-ttu-id="d07d0-104">Questa sezione descrive come usare uno shader geometry con la fase di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="d07d0-104">This section describes how to use a geometry shader with the stream output stage.</span></span>

## <a name="compile-a-geometry-shader"></a><span data-ttu-id="d07d0-105">Compilare uno shader geometrico</span><span class="sxs-lookup"><span data-stu-id="d07d0-105">Compile a Geometry Shader</span></span>

<span data-ttu-id="d07d0-106">Questo geometry shader (GS) calcola una normale faccia per ogni triangolo e restituisce i dati delle coordinate di posizione, normale e trama.</span><span class="sxs-lookup"><span data-stu-id="d07d0-106">This geometry shader (GS) calculates a face normal for each triangle, and outputs position, normal and texture coordinate data.</span></span>


```
struct GSPS_INPUT
{
    float4 Pos : SV_POSITION;
    float3 Norm : TEXCOORD0;
    float2 Tex : TEXCOORD1;
};

[maxvertexcount(12)]
void GS( triangle GSPS_INPUT input[3], inout TriangleStream<GSPS_INPUT> TriStream )
{
    GSPS_INPUT output;
    
    //
    // Calculate the face normal
    //
    float3 faceEdgeA = input[1].Pos - input[0].Pos;
    float3 faceEdgeB = input[2].Pos - input[0].Pos;
    float3 faceNormal = normalize( cross(faceEdgeA, faceEdgeB) );
    float3 ExplodeAmt = faceNormal*Explode;
    
    //
    // Calculate the face center
    //
    float3 centerPos = (input[0].Pos.xyz + input[1].Pos.xyz + input[2].Pos.xyz)/3.0;
    float2 centerTex = (input[0].Tex + input[1].Tex + input[2].Tex)/3.0;
    centerPos += faceNormal*Explode;
    
    //
    // Output the pyramid
    //
    for( int i=0; i<3; i++ )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
        
        int iNext = (i+1)%3;
        output.Pos = input[iNext].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[iNext].Norm;
        output.Tex = input[iNext].Tex;
        TriStream.Append( output );
        
        output.Pos = float4(centerPos,1) + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = faceNormal;
        output.Tex = centerTex;
        TriStream.Append( output );
        
        TriStream.RestartStrip();
    }
    
    for( int i=2; i>=0; i-- )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = -input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
    }
    TriStream.RestartStrip();
}
```



<span data-ttu-id="d07d0-107">Tenere presente questo codice, tenere presente che un geometry shader è simile a un vertice o a un pixel shader, ma con le eccezioni seguenti: il tipo restituito dalla funzione, le dichiarazioni dei parametri di input e la funzione intrinseca.</span><span class="sxs-lookup"><span data-stu-id="d07d0-107">Keeping that code in mind, consider that a geometry shader looks much like a vertex or pixel shader, but with the following exceptions: the type returned by the function, the input parameter declarations, and the intrinsic function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d07d0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d07d0-108">Item</span></span></th>
<th><span data-ttu-id="d07d0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d07d0-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d07d0-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Tipo restituito della funzione</span><span class="sxs-lookup"><span data-stu-id="d07d0-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Function return type</span></span><br/></td>
<td><span data-ttu-id="d07d0-111">Il tipo restituito dalla funzione esegue un'unica cosa e dichiara il numero massimo di vertici che possono essere restituiti dallo shader.</span><span class="sxs-lookup"><span data-stu-id="d07d0-111">The function return type does one thing, declares the maximum number of vertices that can be output by the shader.</span></span> <span data-ttu-id="d07d0-112">In questo caso <span data-codelanguage=""></span>
</span><span class="sxs-lookup"><span data-stu-id="d07d0-112">In this case, <span data-codelanguage=""></span>
</span></span><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d07d0-113">definisce che l'output deve essere un massimo di 12 vertici.</span><span class="sxs-lookup"><span data-stu-id="d07d0-113">defines the output to be a maximum of 12 vertices.</span></span></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d07d0-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Dichiarazioni di parametri di input</span><span class="sxs-lookup"><span data-stu-id="d07d0-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Input parameter declarations</span></span></p></td>
<td><p><span data-ttu-id="d07d0-115">Questa funzione accetta due parametri di input:</span><span class="sxs-lookup"><span data-stu-id="d07d0-115">This function takes two input parameters:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream&lt;GSPS_INPUTT&gt; TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="d07d0-116">Il primo parametro è una matrice di vertici (3 in questo caso) definita da una struttura GSPS_INPUT (che definisce i dati per vertice come una posizione, una normale e una coordinata di trama).</span><span class="sxs-lookup"><span data-stu-id="d07d0-116">The first parameter is an array of vertices (3 in this case) defined by a GSPS_INPUT structure (which defines per-vertex data as a position, a normal and a texture coordinate).</span></span> <span data-ttu-id="d07d0-117">Il primo parametro usa anche la parola chiave triangle, il che significa che la fase dell'assembler di input deve determinare l'output dei dati al geometry shader come uno dei tipi primitivi del triangolo (elenco di triangoli o striscia di triangoli).</span><span class="sxs-lookup"><span data-stu-id="d07d0-117">The first parameter also uses the triangle keyword, which means the input assembler stage must output data to the geometry shader as one of the triangle primitive types (triangle list or triangle strip).</span></span></p>
<p><span data-ttu-id="d07d0-118">Il secondo parametro è un flusso triangolare definito dal tipo TriangleStream &lt; GSPS_INPUTT &gt; .</span><span class="sxs-lookup"><span data-stu-id="d07d0-118">The second parameter is a triangle stream defined by the type TriangleStream&lt;GSPS_INPUTT&gt;.</span></span> <span data-ttu-id="d07d0-119">Ciò significa che il parametro è una matrice di triangoli, ognuno dei quali è costituito da tre vertici (che contengono i dati dei membri di GSPS_INPUT).</span><span class="sxs-lookup"><span data-stu-id="d07d0-119">This means the parameter is an array of triangles, each of which is made up of three vertices (that contain the data from the members of GSPS_INPUT).</span></span></p>
<p><span data-ttu-id="d07d0-120">Usare le parole chiave triangle e trianglestream per identificare singoli triangoli o un flusso di triangoli in GS.</span><span class="sxs-lookup"><span data-stu-id="d07d0-120">Use the triangle and trianglestream keywords to identify individual triangles or a stream of triangles in a GS.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d07d0-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Funzione intrinseca</span><span class="sxs-lookup"><span data-stu-id="d07d0-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsic function</span></span></p></td>
<td><p><span data-ttu-id="d07d0-122">Le righe di codice nella funzione shader usano funzioni intrinseche HLSL common-shader-core, ad eccezione delle ultime due righe, che chiamano Append e RestartStrip.</span><span class="sxs-lookup"><span data-stu-id="d07d0-122">The lines of code in the shader function use common-shader-core HLSL intrinsic functions except the last two lines, which call Append and RestartStrip.</span></span> <span data-ttu-id="d07d0-123">Queste funzioni sono disponibili solo per uno shader geometrico.</span><span class="sxs-lookup"><span data-stu-id="d07d0-123">These functions are only available to a geometry shader.</span></span> <span data-ttu-id="d07d0-124">Append indica al geometry shader di aggiungere l'output all'elenco corrente. RestartStrip crea una nuova striscia primitiva.</span><span class="sxs-lookup"><span data-stu-id="d07d0-124">Append informs the geometry shader to append the output to the current strip; RestartStrip creates a new primitive strip.</span></span> <span data-ttu-id="d07d0-125">Una nuova striscia viene creata in modo implicito in ogni chiamata della fase GS.</span><span class="sxs-lookup"><span data-stu-id="d07d0-125">A new strip is implicitly created in every invocation of the GS stage.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d07d0-126">Il resto dello shader è molto simile a un vertice o a un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="d07d0-126">The rest of the shader looks very similar to a vertex or pixel shader.</span></span> <span data-ttu-id="d07d0-127">Lo shader geometry usa una struttura per dichiarare i parametri di input e contrassegna il membro position con la semantica SV POSITION per indicare all'hardware che si tratta \_ di dati posizionali.</span><span class="sxs-lookup"><span data-stu-id="d07d0-127">The geometry shader uses a structure to declare input parameters and marks the position member with the SV\_POSITION semantic to tell the hardware that this is positional data.</span></span> <span data-ttu-id="d07d0-128">La struttura di input identifica gli altri due parametri di input come coordinate di trama (anche se uno di essi conterrà una normale faccia).</span><span class="sxs-lookup"><span data-stu-id="d07d0-128">The input structure identifies the other two input parameters as texture coordinates (even though one of them will contain a face normal).</span></span> <span data-ttu-id="d07d0-129">Se si preferisce, è possibile usare la semantica personalizzata per il viso normale.</span><span class="sxs-lookup"><span data-stu-id="d07d0-129">You could use your own custom semantic for the face normal if you prefer.</span></span>

<span data-ttu-id="d07d0-130">Dopo aver progettato lo shader geometry, chiamare [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) per la compilazione, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d07d0-130">Having designed the geometry shader, call [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) to compile as shown in the following code example.</span></span>


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



<span data-ttu-id="d07d0-131">Proprio come i vertex shader e i pixel shader, è necessario un flag di shader per indicare al compilatore come si vuole che lo shader sia compilato (per il debug, ottimizzato per la velocità e così via), la funzione del punto di ingresso e il modello di shader rispetto a cui eseguire la convalida.</span><span class="sxs-lookup"><span data-stu-id="d07d0-131">Just like vertex and pixel shaders, you need a shader flag to tell the compiler how you want the shader compiled (for debugging, optimized for speed, and so on), the entry point function, and the shader model to validate against.</span></span> <span data-ttu-id="d07d0-132">Questo esempio crea un geometry shader creato dal file Tutorial13.fx usando la funzione GS.</span><span class="sxs-lookup"><span data-stu-id="d07d0-132">This example creates a geometry shader built from the Tutorial13.fx file, by using the GS function.</span></span> <span data-ttu-id="d07d0-133">Lo shader viene compilato per il modello di shader 4.0.</span><span class="sxs-lookup"><span data-stu-id="d07d0-133">The shader is compiled for shader model 4.0.</span></span>

## <a name="create-a-geometry-shader-object-with-stream-output"></a><span data-ttu-id="d07d0-134">Creare un oggetto Geometry-Shader con output del flusso</span><span class="sxs-lookup"><span data-stu-id="d07d0-134">Create a Geometry-Shader Object with Stream Output</span></span>

<span data-ttu-id="d07d0-135">Quando si è a sapere che i dati verranno streaming dalla geometria e che lo shader è stato compilato correttamente, il passaggio successivo consiste nel chiamare [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) per creare l'oggetto geometry shader.</span><span class="sxs-lookup"><span data-stu-id="d07d0-135">Once you know that you will be streaming the data from the geometry, and you have successfully compiled the shader, the next step is to call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) to create the geometry shader object.</span></span>

<span data-ttu-id="d07d0-136">Prima di tutto, tuttavia, è necessario dichiarare la firma di input della fase output a flusso (SO).</span><span class="sxs-lookup"><span data-stu-id="d07d0-136">But first, you need to declare the steam output (SO) stage input signature.</span></span> <span data-ttu-id="d07d0-137">Questa firma corrisponde o convalida gli output GS e gli input SO al momento della creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d07d0-137">This signature matches or validates the GS outputs and the SO inputs at the time of object creation.</span></span> <span data-ttu-id="d07d0-138">Il codice seguente è un esempio della dichiarazione SO.</span><span class="sxs-lookup"><span data-stu-id="d07d0-138">The following code is an example of the SO declaration.</span></span>


```
D3D11_SO_DECLARATION_ENTRY pDecl[] =
{
    // semantic name, semantic index, start component, component count, output slot
    { "SV_POSITION", 0, 0, 4, 0 },   // output all components of position
    { "TEXCOORD0", 0, 0, 3, 0 },     // output the first 3 of the normal
    { "TEXCOORD1", 0, 0, 2, 0 },     // output the first 2 texture coordinates
};

D3D11Device->CreateGeometryShaderWithStreamOut( pShaderBytecode, ShaderBytecodesize, pDecl, 
    sizeof(pDecl), NULL, 0, 0, NULL, &pStreamOutGS );
```



<span data-ttu-id="d07d0-139">Questa funzione accetta diversi parametri, tra cui:</span><span class="sxs-lookup"><span data-stu-id="d07d0-139">This function takes several parameters including:</span></span>

-   <span data-ttu-id="d07d0-140">Puntatore al geometry shader compilato (o vertex shader se non è presente alcun geometry shader e i dati verranno trasmessi direttamente dal vertex shader).</span><span class="sxs-lookup"><span data-stu-id="d07d0-140">A pointer to the compiled geometry shader (or vertex shader if no geometry shader will be present and data will be streamed out directly from the vertex shader).</span></span> <span data-ttu-id="d07d0-141">Per informazioni su come ottenere questo puntatore, vedere [Recupero di un puntatore a uno shader compilato.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10)</span><span class="sxs-lookup"><span data-stu-id="d07d0-141">For information about how to get this pointer, see [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span></span>
-   <span data-ttu-id="d07d0-142">Puntatore a una matrice di dichiarazioni che descrivono i dati di input per la fase di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="d07d0-142">A pointer to an array of declarations that describe the input data for the stream output stage.</span></span> <span data-ttu-id="d07d0-143">Vedere [**D3D11 \_ SO DECLARATION ENTRY (VOCE DI DICHIARAZIONE \_ \_ SO D3D11).**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry) È possibile fornire fino a 64 dichiarazioni, una per ogni tipo di elemento diverso da visualizzare come output dalla fase SO.</span><span class="sxs-lookup"><span data-stu-id="d07d0-143">(See [**D3D11\_SO\_DECLARATION\_ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) You can supply up to 64 declarations, one for each different type of element to be output from the SO stage.</span></span> <span data-ttu-id="d07d0-144">La matrice di voci di dichiarazione descrive il layout dei dati indipendentemente dal fatto che sia necessario eseguire l'associazione di un solo buffer o di più buffer per l'output del flusso.</span><span class="sxs-lookup"><span data-stu-id="d07d0-144">The array of declaration entries describes the data layout regardless of whether only a single buffer or multiple buffers are to be bound for stream output.</span></span>
-   <span data-ttu-id="d07d0-145">Numero di elementi scritti dalla fase SO.</span><span class="sxs-lookup"><span data-stu-id="d07d0-145">The number of elements that are written out by the SO stage.</span></span>
-   <span data-ttu-id="d07d0-146">Puntatore all'oggetto geometry shader creato (vedere [**ID3D11GeometryShader).**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)</span><span class="sxs-lookup"><span data-stu-id="d07d0-146">A pointer to the geometry shader object that is created (see [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span></span>

<span data-ttu-id="d07d0-147">In questo caso, lo stride del buffer è NULL, l'indice del flusso da inviare al rasterizzatore è 0 e l'interfaccia di collegamento della classe è NULL.</span><span class="sxs-lookup"><span data-stu-id="d07d0-147">In this situation, the buffer stride is NULL, the index of the stream to be sent to the rasterizer is 0, and the class linkage interface is NULL.</span></span>

<span data-ttu-id="d07d0-148">La dichiarazione di output del flusso definisce la modalità di scrittura dei dati in una risorsa buffer.</span><span class="sxs-lookup"><span data-stu-id="d07d0-148">The stream output declaration defines the way that data is written to a buffer resource.</span></span> <span data-ttu-id="d07d0-149">È possibile aggiungere tutti i componenti desiderati alla dichiarazione di output.</span><span class="sxs-lookup"><span data-stu-id="d07d0-149">You can add as many components as you want to the output declaration.</span></span> <span data-ttu-id="d07d0-150">Usare la fase SO per scrivere in una singola risorsa buffer o in molte risorse buffer.</span><span class="sxs-lookup"><span data-stu-id="d07d0-150">Use the SO stage to write to a single buffer resource or many buffer resources.</span></span> <span data-ttu-id="d07d0-151">Per un singolo buffer, la fase SO può scrivere molti elementi diversi per vertice.</span><span class="sxs-lookup"><span data-stu-id="d07d0-151">For a single buffer, the SO stage can write many different elements per-vertex.</span></span> <span data-ttu-id="d07d0-152">Per più buffer, la fase SO può scrivere solo un singolo elemento di dati per vertice in ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="d07d0-152">For multiple buffers, the SO stage can only write a single element of per-vertex data to each buffer.</span></span>

<span data-ttu-id="d07d0-153">Per usare la fase SO senza usare uno shader geometry, chiamare [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) e passare un puntatore a un vertex shader al *parametro pShaderBytecode.*</span><span class="sxs-lookup"><span data-stu-id="d07d0-153">To use the SO stage without using a geometry shader, call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) and pass a pointer to a vertex shader to the *pShaderBytecode* parameter.</span></span>

## <a name="set-the-output-targets"></a><span data-ttu-id="d07d0-154">Impostare le destinazioni di output</span><span class="sxs-lookup"><span data-stu-id="d07d0-154">Set the Output Targets</span></span>

<span data-ttu-id="d07d0-155">L'ultimo passaggio consiste nell'impostare i buffer della fase SO.</span><span class="sxs-lookup"><span data-stu-id="d07d0-155">The last step is to set the SO stage buffers.</span></span> <span data-ttu-id="d07d0-156">I dati possono essere trasmessi in uno o più buffer in memoria per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="d07d0-156">Data can be streamed into one or more buffers in memory for use later.</span></span> <span data-ttu-id="d07d0-157">Il codice seguente illustra come creare un singolo buffer che può essere usato per i dati dei vertici, nonché per la fase SO in cui trasmettere i dati.</span><span class="sxs-lookup"><span data-stu-id="d07d0-157">The following code shows how to create a single buffer that can be used for vertex data, as well as for the SO stage to stream data into.</span></span>


```
ID3D11Buffer *m_pBuffer;
int m_nBufferSize = 1000000;

D3D11_BUFFER_DESC bufferDesc =
{
    m_nBufferSize,
    D3D11_USAGE_DEFAULT,
    D3D11_BIND_STREAM_OUTPUT,
    0,
    0,
    0
};
D3D11Device->CreateBuffer( &bufferDesc, NULL, &m_pBuffer );
```



<span data-ttu-id="d07d0-158">Creare un buffer chiamando [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span><span class="sxs-lookup"><span data-stu-id="d07d0-158">Create a buffer by calling [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span> <span data-ttu-id="d07d0-159">Questo esempio illustra l'utilizzo predefinito, tipico di una risorsa buffer che si prevede verrà aggiornata con frequenza abbastanza frequente dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="d07d0-159">This example illustrates default usage, which is typical for a buffer resource that is expected to be updated fairly frequently by the CPU.</span></span> <span data-ttu-id="d07d0-160">Il flag di associazione identifica la fase della pipeline a cui è possibile associare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d07d0-160">The binding flag identifies the pipeline stage that the resource can be bound to.</span></span> <span data-ttu-id="d07d0-161">Qualsiasi risorsa usata dalla fase SO deve essere creata anche con il flag di associazione D3D10 \_ BIND \_ STREAM \_ OUTPUT.</span><span class="sxs-lookup"><span data-stu-id="d07d0-161">Any resource used by the SO stage must also be created with the bind flag D3D10\_BIND\_STREAM\_OUTPUT.</span></span>

<span data-ttu-id="d07d0-162">Dopo aver creato correttamente il buffer, impostarlo sul dispositivo corrente chiamando [**ID3D11DeviceContext::SOSetTargets:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets)</span><span class="sxs-lookup"><span data-stu-id="d07d0-162">Once the buffer is successfully created, set it to the current device by calling [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span></span>


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



<span data-ttu-id="d07d0-163">Questa chiamata accetta il numero di buffer, un puntatore ai buffer e una matrice di offset (un offset in ognuno dei buffer che indica dove iniziare a scrivere i dati).</span><span class="sxs-lookup"><span data-stu-id="d07d0-163">This call takes the number of buffers, a pointer to the buffers, and an array of offsets (one offset into each of the buffers that indicates where to begin writing data).</span></span> <span data-ttu-id="d07d0-164">I dati verranno scritti in questi buffer di output di streaming quando viene chiamata una funzione di disegno.</span><span class="sxs-lookup"><span data-stu-id="d07d0-164">Data will be written to these streaming-output buffers when a draw function is called.</span></span> <span data-ttu-id="d07d0-165">Una variabile interna tiene traccia della posizione in cui iniziare a scrivere i dati nei buffer di streaming-output e tale variabile continuerà a incrementare fino a quando [**soSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) non viene chiamato di nuovo e non viene specificato un nuovo valore di offset.</span><span class="sxs-lookup"><span data-stu-id="d07d0-165">An internal variable keeps track of the position for where to begin writing data to the streaming-output buffers, and that variables will continue to increment until [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) is called again and a new offset value is specified.</span></span>

<span data-ttu-id="d07d0-166">Tutti i dati scritti nei buffer di destinazione saranno valori a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d07d0-166">All data written out to the target buffers will be 32-bit values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d07d0-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d07d0-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d07d0-168">Fase di output del flusso</span><span class="sxs-lookup"><span data-stu-id="d07d0-168">Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

