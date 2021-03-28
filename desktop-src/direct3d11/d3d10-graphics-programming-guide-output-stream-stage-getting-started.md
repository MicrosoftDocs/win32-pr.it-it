---
title: Introduzione con la fase di Stream-Output
description: Questa sezione descrive come usare un geometry shader con la fase di output del flusso.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909b3ba37e8b80201a4afc3e5bf18f016fed38a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976738"
---
# <a name="getting-started-with-the-stream-output-stage"></a>Introduzione con la fase di Stream-Output

Questa sezione descrive come usare un geometry shader con la fase di output del flusso.

## <a name="compile-a-geometry-shader"></a>Compilare un geometry shader

Questo geometry shader (GS) calcola una superficie normale per ogni triangolo e restituisce la posizione, i dati delle coordinate normali e di trama.


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



Tenendo presente questo codice, tenere presente che un geometry shader è simile a un vertice o a un pixel shader, ma con le eccezioni seguenti: il tipo restituito dalla funzione, le dichiarazioni dei parametri di input e la funzione intrinseca.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Il tipo restituito della funzione esegue una sola operazione, dichiara il numero massimo di vertici che possono essere restituiti dallo shader. In questo caso <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

definisce l'output in modo da ottenere un massimo di 12 vertici.</td>
</tr>
<tr class="even">
<td><p><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Dichiarazioni di parametri di input</p></td>
<td><p>Questa funzione accetta due parametri di input:</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream<GSPS_INPUT> TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Il primo parametro è una matrice di vertici (3 in questo caso) definita da una struttura GSPS_INPUT (che definisce i dati per vertice come una posizione, una coordinata normale e una coordinata di trama). Il primo parametro usa anche la parola chiave Triangle, che indica che la fase dell'assembler di input deve restituire i dati allo shader Geometry come uno dei tipi primitivi triangolari (elenco di triangolo o striscia di triangolo).</p>
<p>Il secondo parametro è un flusso di triangolo definito dal tipo TriangleStream <GSPS_INPUT> . Ciò significa che il parametro è una matrice di triangoli, ciascuno dei quali è costituito da tre vertici, che contengono i dati dei membri di GSPS_INPUT.</p>
<p>Usare le parole chiave Triangle e trianglestream per identificare singoli triangoli o un flusso di triangoli in una GS.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Funzione intrinseca</p></td>
<td><p>Le righe di codice nella funzione shader usano funzioni intrinseche HLSL di Common shader, ad eccezione delle ultime due righe, che chiamano Append e RestartStrip. Queste funzioni sono disponibili solo per un geometry shader. Append informa il geometry shader di accodare l'output alla striscia corrente; RestartStrip crea una nuova striscia primitiva. Una nuova striscia viene creata in modo implicito in ogni chiamata della fase GS.</p></td>
</tr>
</tbody>
</table>



 

Il resto dello shader ha un aspetto molto simile a un vertice o pixel shader. Geometry shader usa una struttura per dichiarare i parametri di input e contrassegna il membro position con la \_ semantica di posizione SV per indicare all'hardware che si tratta di dati posizionali. La struttura di input identifica gli altri due parametri di input come coordinate di trama (anche se uno di essi conterrà una superficie normale). Se si preferisce, è possibile usare la propria semantica personalizzata per il volto normale.

Dopo aver progettato il geometry shader, chiamare [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) per la compilazione, come illustrato nell'esempio di codice seguente.


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



Proprio come i vertex e i pixel shader, è necessario un flag shader per indicare al compilatore come si desidera che lo shader venga compilato (per il debug, ottimizzato per la velocità e così via), la funzione del punto di ingresso e il modello di shader in base al quale eseguire la convalida. In questo esempio viene creato un geometry shader creato dal file Tutorial13. FX, usando la funzione GS. Lo shader viene compilato per il modello di Shader 4,0.

## <a name="create-a-geometry-shader-object-with-stream-output"></a>Creare un oggetto Geometry-Shader con output di flusso

Quando si è certi che i dati verranno trasmessi dalla geometria e la compilazione dello shader è stata completata, il passaggio successivo consiste nel chiamare [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) per creare l'oggetto Geometry shader.

Prima di tutto, è necessario dichiarare la firma di input per la fase di output del vapore. Questa firma corrisponde o convalida gli output GS e gli input in modo che al momento della creazione dell'oggetto. Il codice seguente è un esempio della dichiarazione di.


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

-   Un puntatore al geometry shader compilato (o vertex shader se non è presente alcun geometry shader e i dati verranno trasmessi direttamente dal vertex shader). Per informazioni su come ottenere questo puntatore, vedere [recupero di un puntatore a uno shader compilato](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).
-   Puntatore a una matrice di dichiarazioni che descrivono i dati di input per la fase di output del flusso. (Vedere [**d3d11 \_ so \_ \_ entry della dichiarazione**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)). È possibile fornire fino a 64 dichiarazioni, una per ogni tipo di elemento diverso da restituire dalla fase SO. La matrice di voci di dichiarazione descrive il layout dei dati indipendentemente dal fatto che venga associato un solo buffer o più buffer per l'output del flusso.
-   Numero di elementi scritti dalla fase in questione.
-   Puntatore all'oggetto Geometry shader creato (vedere [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).

In questa situazione, lo stride del buffer è NULL, l'indice del flusso da inviare al rasterizzatore è 0 e l'interfaccia di collegamento di classe è NULL.

La dichiarazione di output del flusso definisce il modo in cui i dati vengono scritti in una risorsa del buffer. È possibile aggiungere tutti i componenti desiderati alla dichiarazione di output. Usare la fase così per scrivere in una risorsa buffer singola o in molte risorse del buffer. Per un singolo buffer, la fase SO può scrivere molti elementi diversi per ogni vertice. Per più buffer, la fase SO può scrivere solo un singolo elemento di dati per vertice in ogni buffer.

Per usare la fase SO senza usare un geometry shader, chiamare [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) e passare un puntatore a un vertex shader al parametro *pShaderBytecode* .

## <a name="set-the-output-targets"></a>Impostare le destinazioni di output

L'ultimo passaggio consiste nell'impostare i buffer di gestione temporanea. I dati possono essere trasmessi in uno o più buffer in memoria per essere usati in un secondo momento. Nel codice seguente viene illustrato come creare un singolo buffer che può essere utilizzato per i dati dei vertici, nonché per la fase in cui trasmettere i dati.


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



Creare un buffer chiamando [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer). Questo esempio illustra l'utilizzo predefinito, che è tipico per una risorsa di buffer che dovrebbe essere aggiornata abbastanza frequentemente dalla CPU. Il flag di associazione identifica la fase della pipeline a cui è possibile associare la risorsa. Tutte le risorse usate dalla fase SO devono anche essere create con il flag di binding D3D10 \_ binding \_ Stream \_ output.

Dopo aver creato correttamente il buffer, impostarlo sul dispositivo corrente chiamando [**sul ID3D11DeviceContext:: SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



Questa chiamata accetta il numero di buffer, un puntatore ai buffer e una matrice di offset (un offset in ognuno dei buffer che indica dove iniziare la scrittura dei dati). I dati verranno scritti nei buffer di output di streaming quando viene chiamata una funzione di traccia. Una variabile interna tiene traccia della posizione in cui iniziare a scrivere i dati nei buffer di flusso di output e le variabili continueranno ad aumentare fino a quando non viene chiamato di nuovo [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) e viene specificato un nuovo valore di offset.

Tutti i dati scritti nei buffer di destinazione saranno valori a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase flusso-output](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

