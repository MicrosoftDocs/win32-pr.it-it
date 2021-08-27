---
title: Attività iniziali con la fase Stream-Output lavoro
description: Questa sezione descrive come usare uno shader geometry con la fase di output del flusso.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f00b469b28601322358f348de98354f15263483
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621877"
---
# <a name="getting-started-with-the-stream-output-stage"></a>Attività iniziali con la fase Stream-Output lavoro

Questa sezione descrive come usare uno shader geometry con la fase di output del flusso.

## <a name="compile-a-geometry-shader"></a>Compilare uno shader geometry

Questo geometry shader (GS) calcola una normale faccia per ogni triangolo e restituisce i dati relativi alla posizione, alla normale e alla coordinata della trama.


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



Tenere presente questo codice, tenere presente che un geometry shader è simile a un vertice o a un pixel shader, ma con le eccezioni seguenti: il tipo restituito dalla funzione, le dichiarazioni dei parametri di input e la funzione intrinseca.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Tipo restituito della funzione<br/></td>
<td>Il tipo restituito dalla funzione esegue un'unica cosa e dichiara il numero massimo di vertici che possono essere restituiti dallo shader. In questo caso <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

definisce che l'output deve essere un massimo di 12 vertici.</td>
</tr>
<tr class="even">
<td><p><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Dichiarazioni di parametri di input</p></td>
<td><p>Questa funzione accetta due parametri di input:</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream&lt;GSPS_INPUTT&gt; TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Il primo parametro è una matrice di vertici (3 in questo caso) definita da una struttura GSPS_INPUT (che definisce i dati per vertice come una posizione, una coordinata normale e una trama). Il primo parametro usa anche la parola chiave triangle, che significa che la fase dell'assembler di input deve determinare l'output dei dati nel geometry shader come uno dei tipi primitivi del triangolo (elenco di triangoli o striscia di triangoli).</p>
<p>Il secondo parametro è un flusso triangolare definito dal tipo TriangleStream &lt; GSPS_INPUTT &gt; . Ciò significa che il parametro è una matrice di triangoli, ognuno dei quali è costituito da tre vertici (che contengono i dati dei membri di GSPS_INPUT).</p>
<p>Usare le parole chiave triangle e trianglestream per identificare singoli triangoli o un flusso di triangoli in GS.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Funzione intrinseca</p></td>
<td><p>Le righe di codice nella funzione shader usano funzioni intrinseche HLSL comuni, ad eccezione delle ultime due righe, che chiamano Append e RestartStrip. Queste funzioni sono disponibili solo per uno shader geometry. Append indica al geometry shader di aggiungere l'output all'elenco corrente. RestartStrip crea una nuova striscia primitiva. Una nuova striscia viene creata in modo implicito in ogni chiamata della fase GS.</p></td>
</tr>
</tbody>
</table>



 

Il resto dello shader è molto simile a un vertice o a un pixel shader. Lo shader geometry usa una struttura per dichiarare i parametri di input e contrassegna il membro position con la semantica SV POSITION per indicare all'hardware che si tratta \_ di dati posizionali. La struttura di input identifica gli altri due parametri di input come coordinate di trama (anche se uno di essi conterrà una normale faccia). Se si preferisce, è possibile usare la semantica personalizzata per il viso normale.

Dopo aver progettato lo shader geometry, chiamare [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) per la compilazione, come illustrato nell'esempio di codice seguente.


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



Proprio come i vertex shader e i pixel shader, è necessario un flag di shader per indicare al compilatore come si vuole che lo shader sia compilato (per il debug, ottimizzato per la velocità e così via), la funzione del punto di ingresso e il modello di shader rispetto a cui eseguire la convalida. Questo esempio crea un geometry shader creato dal file Tutorial13.fx usando la funzione GS. Lo shader viene compilato per il modello di shader 4.0.

## <a name="create-a-geometry-shader-object-with-stream-output"></a>Creare un oggetto Geometry-Shader con output del flusso

Quando si è a sapere che i dati verranno streaming dalla geometria e che lo shader è stato compilato correttamente, il passaggio successivo consiste nel chiamare [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) per creare l'oggetto geometry shader.

Prima di tutto, tuttavia, è necessario dichiarare la firma di input della fase output a flusso (SO). Questa firma corrisponde o convalida gli output GS e gli input SO al momento della creazione dell'oggetto. Il codice seguente è un esempio della dichiarazione SO.


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



Questa funzione accetta diversi parametri, tra cui:

-   Puntatore al geometry shader compilato (o vertex shader se non è presente alcun geometry shader e i dati verranno trasmessi direttamente dal vertex shader). Per informazioni su come ottenere questo puntatore, vedere [Recupero di un puntatore a uno shader compilato.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10)
-   Puntatore a una matrice di dichiarazioni che descrivono i dati di input per la fase di output del flusso. Vedere [**D3D11 \_ SO DECLARATION ENTRY (VOCE DI DICHIARAZIONE \_ \_ SO D3D11).**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry) È possibile fornire fino a 64 dichiarazioni, una per ogni tipo di elemento diverso da visualizzare come output dalla fase SO. La matrice di voci di dichiarazione descrive il layout dei dati indipendentemente dal fatto che per l'output del flusso siano associati solo un singolo buffer o più buffer.
-   Numero di elementi scritti dalla fase SO.
-   Puntatore all'oggetto geometry shader creato (vedere [**ID3D11GeometryShader).**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)

In questo caso, lo stride del buffer è NULL, l'indice del flusso da inviare al rasterizzatore è 0 e l'interfaccia di collegamento della classe è NULL.

La dichiarazione di output del flusso definisce la modalità di scrittura dei dati in una risorsa buffer. È possibile aggiungere tutti i componenti desiderati alla dichiarazione di output. Usare la fase SO per scrivere in una singola risorsa buffer o in molte risorse buffer. Per un singolo buffer, la fase SO può scrivere molti elementi diversi per vertice. Per più buffer, la fase SO può scrivere solo un singolo elemento di dati per vertice in ogni buffer.

Per usare la fase SO senza usare uno shader geometry, chiamare [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) e passare un puntatore a un vertex shader al *parametro pShaderBytecode.*

## <a name="set-the-output-targets"></a>Impostare le destinazioni di output

L'ultimo passaggio consiste nell'impostare i buffer della fase SO. I dati possono essere trasmessi in uno o più buffer in memoria per un uso successivo. Il codice seguente illustra come creare un singolo buffer che può essere usato per i dati dei vertici, nonché per la fase SO in cui trasmettere i dati.


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



Creare un buffer chiamando [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer). Questo esempio illustra l'utilizzo predefinito, tipico di una risorsa buffer che si prevede verrà aggiornata con frequenza abbastanza frequente dalla CPU. Il flag di associazione identifica la fase della pipeline a cui è possibile associare la risorsa. Qualsiasi risorsa usata dalla fase SO deve essere creata anche con il flag di associazione D3D10 \_ BIND \_ STREAM \_ OUTPUT.

Dopo aver creato correttamente il buffer, impostarlo sul dispositivo corrente chiamando [**ID3D11DeviceContext::SOSetTargets:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets)


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



Questa chiamata accetta il numero di buffer, un puntatore ai buffer e una matrice di offset (un offset in ognuno dei buffer che indica dove iniziare a scrivere i dati). I dati verranno scritti in questi buffer di output di streaming quando viene chiamata una funzione di disegno. Una variabile interna tiene traccia della posizione in cui iniziare a scrivere i dati nei buffer di streaming-output e tale variabile continuerà a incrementare fino a quando [**soSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) non viene chiamato di nuovo e non viene specificato un nuovo valore di offset.

Tutti i dati scritti nei buffer di destinazione saranno valori a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase di output del flusso](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

