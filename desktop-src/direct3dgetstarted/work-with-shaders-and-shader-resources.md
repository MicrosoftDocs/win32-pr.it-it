---
title: Usare shader e risorse shader
description: È il momento di imparare a usare shader e risorse shader nello sviluppo di un gioco Microsoft DirectX per Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf0152ba74dcc8dd1c602b69d854634502c928a0deefe5521bcab8999954049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288551"
---
# <a name="work-with-shaders-and-shader-resources"></a>Usare shader e risorse shader

È il momento di imparare a usare shader e risorse shader nello sviluppo di un gioco Microsoft DirectX per Windows 8. Si è visto come configurare il dispositivo grafico e le risorse e forse si è anche iniziato a modificare la pipeline. Si esaminino ora i pixel shader e i vertex shader.

Se non si ha familiarità con i linguaggi di shader, è disponibile una rapida discussione. Gli shader sono piccoli programmi di basso livello compilati ed eseguiti in fasi specifiche della pipeline grafica. La loro specializzazione è operazioni matematiche a virgola mobile molto veloci. I programmi shader più comuni sono:

-   **Vertex shader:** eseguito per ogni vertice in una scena. Questo shader opera sugli elementi del buffer dei vertici forniti dall'app chiamante e comporta un vettore di posizione a 4 componenti che verrà rasterizzato in una posizione in pixel.
-   **Pixel shader: eseguito** per ogni pixel in una destinazione di rendering. Questo shader riceve coordinate rasterizzate dalle fasi precedenti dello shader (nelle pipeline più semplici, si tratta del vertex shader) e restituisce un colore (o un altro valore a 4 componenti) per la posizione del pixel, che viene quindi scritto in una destinazione di rendering.

Questo esempio include vertex shader e pixel shader molto semplici che disegnano solo geometria e shader più complessi che aggiungono calcoli di illuminazione di base.

I programmi shader sono scritti in HLSL (Microsoft High Level Shader Language). La sintassi HLSL è molto simile a C, ma senza i puntatori. I programmi shader devono essere molto compatti ed efficienti. Se lo shader viene compilato in un numero troppo grande di istruzioni, non può essere eseguito e viene restituito un errore. Si noti che il numero esatto di istruzioni consentite fa parte del [livello di funzionalità Direct3D.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)

In Direct3D gli shader non vengono compilati in fase di esecuzione. vengono compilati quando viene compilato il resto del programma. Quando si compila l'app con Microsoft Visual Studio 2013, i file HLSL vengono compilati in file CSO (con estensione cso) che l'app deve caricare e inserire nella memoria GPU prima del disegno. Assicurarsi di includere questi file CSO con l'app quando si crea il pacchetto; sono asset esattamente come mesh e trame.

## <a name="understand-hlsl-semantics"></a>Informazioni sulla semantica HLSL

È importante esaminare la semantica HLSL prima di continuare, perché spesso sono un punto di confusione per i nuovi sviluppatori Direct3D. La semantica HLSL è una stringa che identifica un valore passato tra l'app e un programma shader. Anche se possono essere diverse stringhe possibili, la procedura consigliata consiste nell'usare una stringa come `POSITION` o `COLOR` che indichi l'utilizzo. Questa semantica viene assegnata quando si costruisce un buffer costante o un layout di input. Puoi anche aggiungere un numero compreso tra 0 e 7 alla semantica in modo da usare registri separati per valori simili. Ad esempio: COLOR0, COLOR1, COLOR2...

La semantica preceduta da "SV" è una semantica dei valori di sistema scritta nel programma shader. Il gioco stesso (in esecuzione nella CPU) non può \_ modificarli.  In genere, questa semantica contiene valori che sono input o output da un'altra fase dello shader nella pipeline grafica o che vengono generati interamente dalla GPU.

Inoltre, la semantica ha comportamenti diversi quando vengono usate per specificare `SV_` l'input o l'output da una fase shader. Ad esempio, (output) contiene i dati dei vertici trasformati durante la fase vertex shader e ( input ) contiene i valori della posizione in pixel interpolati dalla GPU durante la fase di `SV_POSITION` `SV_POSITION` rasterizzazione.

Ecco alcune semantiche HLSL comuni:

-   `POSITION`(*n*) per i dati del vertex buffer. `SV_POSITION` fornisce una posizione in pixel al pixel shader e non può essere scritto dal gioco.
-   `NORMAL`(*n*) per i dati normali forniti dal vertex buffer.
-   `TEXCOORD`(*n*) per i dati delle coordinate UV della trama forniti a uno shader.
-   `COLOR`(n) per i dati di colore RGBA forniti a uno shader. Si noti che viene trattato in modo identico per coordinare i dati, inclusa l'interpolazione del valore durante la rasterizzazione; la semantica consente semplicemente di identificare che si tratta di dati di colore.
-   `SV_Target`\[n \] per la scrittura da un pixel shader in una trama di destinazione o in un altro buffer pixel.

Verranno visualizzati alcuni esempi di semantica HLSL durante la revisione dell'esempio.

## <a name="read-from-the-constant-buffers"></a>Leggere dai buffer costanti

Qualsiasi shader può leggere da un buffer costante se tale buffer è collegato alla fase come risorsa. In questo esempio solo al vertex shader viene assegnato un buffer costante.

Il buffer costante viene dichiarato in due posizioni: nel codice C++ e nei file HLSL corrispondenti che vi accederanno.

Ecco come viene dichiarato lo struct del buffer costante nel codice C++.


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



Quando si dichiara la struttura per il buffer costante nel codice C++, assicurarsi che tutti i dati siano allineati correttamente lungo i limiti di 16 byte. Il modo più semplice per eseguire questa operazione è usare i tipi [DirectXMath,](/windows/desktop/dxmath/directxmath-portal) ad esempio **XMFLOAT4** o **XMFLOAT4X4,** come illustrato nel codice di esempio. È anche possibile proteggersi da buffer non allineati dichiarando un'asserzione statica:


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



Questa riga di codice causerà un errore in fase di compilazione se **ConstantBufferStruct** non è allineato a 16 byte. Per altre informazioni sull'allineamento costante del buffer e sulla creazione di un pacchetto, vedere [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

Ecco come viene dichiarato il buffer costante nel vertex shader HLSL.


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



Tutti i buffer, ovvero costanti, trame, campionatori o altri, devono avere un registro definito in modo che la GPU possa accedervi. Ogni fase dello shader consente fino a 15 buffer costanti e ogni buffer può contenere fino a 4.096 variabili costanti. La sintassi di dichiarazione register-usage è la seguente:

-   **b** _\#_ : registro per un buffer costante (**cbuffer**).
-   **t** _\#_ : registro per un buffer di trama (**tbuffer**).
-   **s** _\#_ : registro per un campionatore. Un campionatore definisce il comportamento di ricerca per i texel nella risorsa trama.

Ad esempio, il file HLSL per un pixel shader potrebbe prendere una trama e un campionatore come input con una dichiarazione simile alla seguente.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

È necessario assegnare buffer costanti ai registri. Quando si configura la pipeline, si collega un buffer costante allo stesso slot a cui è stato assegnato nel file HLSL. Nell'argomento precedente, ad esempio, la chiamata a [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indica "0" per il primo parametro. Ciò indica a Direct3D di collegare la risorsa buffer costante per registrare 0, che corrisponde all'assegnazione del buffer a **register(b0)** nel file HLSL.

## <a name="read-from-the-vertex-buffers"></a>Leggere dai vertex buffer

Il buffer dei vertici fornisce i dati del triangolo per gli oggetti della scena ai vertex shader. Come per il buffer costante, lo struct vertex buffer viene dichiarato nel codice C++, usando regole di creazione di un pacchetto simili.


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



Non esiste un formato standard per i dati dei vertici in Direct3D 11. Al contrario, si definisce il proprio layout dei dati dei vertici usando un descrittore. I campi dati vengono definiti usando una matrice di strutture [**D3D11 \_ INPUT \_ ELEMENT \_ DESC.**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) In questo esempio viene illustrato un layout di input semplice che descrive lo stesso formato di vertice dello struct precedente:


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



Se si aggiungono dati al formato vertice quando si modifica il codice di esempio, assicurarsi di aggiornare anche il layout di input oppure lo shader non sarà in grado di interpretarlo. È possibile modificare il layout dei vertici nel modo seguente:


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



In tal caso, è necessario modificare la definizione del layout di input come indicato di seguito.


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



Ogni definizione di elemento di layout di input è preceduta da una stringa, ad esempio "POSITION" o "NORMAL", ovvero la semantica illustrata in precedenza in questo argomento. È simile a un handle che consente alla GPU di identificare tale elemento durante l'elaborazione del vertice. Scegliere nomi comuni e significativi per gli elementi vertice.

Come per il buffer costante, il vertex shader ha una definizione di buffer corrispondente per gli elementi vertice in ingresso. Per questo motivo è stato fornito un riferimento alla risorsa vertex shader durante la creazione del layout di input. Direct3D convalida il layout dei dati per vertice con lo struct di input dello shader. Si noti come la semantica corrisponda tra la definizione del layout di input e questa dichiarazione del buffer HLSL. Tuttavia, `COLOR` viene aggiunto "0". Non è necessario aggiungere il valore 0 se nel layout è dichiarato un solo elemento, ma è consigliabile aggiungerlo nel caso in cui si scenda di aggiungere altri elementi colore `COLOR` in futuro.


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a>Passare dati tra shader

Gli shader accettano tipi di input e restituiscono tipi di output dalle funzioni principali al momento dell'esecuzione. Per il vertex shader definito nella sezione precedente, il tipo di input era la struttura VS INPUT ed è stato definito un layout di input e uno \_ struct C++ corrispondenti. Una matrice di questo struct viene usata per creare un vertex buffer nel **metodo CreateCube.**

Il vertex shader restituisce una struttura PS INPUT, che deve contenere al minimo la posizione finale del vertice a \_ 4 componenti (float4). Per questo valore di posizione deve essere dichiarata la semantica del valore di sistema, , in modo che la GPU abbia i dati di cui ha bisogno `SV_POSITION` per eseguire il passaggio di disegno successivo. Si noti che non esiste una corrispondenza 1:1 tra l'output del vertex shader e pixel shader input; Il vertex shader restituisce una struttura per ogni vertice assegnato, ma il pixel shader viene eseguito una volta per ogni pixel. Questo perché i dati per vertice passano prima attraverso la fase di rasterizzazione. Questa fase decide quali pixel "coprono" la geometria che si sta disegnando, calcola i dati interpolati per vertice per ogni pixel e quindi chiama il pixel shader una volta per ognuno di questi pixel. L'interpolazione è il comportamento predefinito durante la rasterizzazione dei valori di output ed è essenziale in particolare per la corretta elaborazione dei dati vettoriali di output (vettori di luce, normali per vertice e tangenti e altri).


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a>Esaminare il vertex shader

Il vertex shader di esempio è molto semplice: prendere un vertice (posizione e colore), trasformare la posizione dalle coordinate del modello in coordinate prospetticamente proiettate e restituirla (insieme al colore) al rasterizzatore. Si noti che il valore del colore viene interpolato a destra insieme ai dati di posizione, fornendo un valore diverso per ogni pixel anche se il vertex shader non ha eseguito calcoli sul valore del colore.


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



Un vertex shader più complesso, ad esempio uno che configura i vertici di un oggetto per l'ombreggiatura Phong, potrebbe avere un aspetto più simile al seguente. In questo caso, si sfrutta il fatto che i vettori e le normali sono interpolati per approssimare una superficie dall'aspetto uniforme.

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

## <a name="review-the-pixel-shader"></a>Esaminare il pixel shader

Questo pixel shader in questo esempio è probabilmente la quantità minima assoluta di codice che è possibile avere in un pixel shader. Accetta i dati di colore pixel interpolati generati durante la rasterizzazione e li restituisce come output, dove verranno scritti in una destinazione di rendering. Che disdemente!


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



La parte importante è la `SV_TARGET` semantica del valore di sistema sul valore restituito. Indica che l'output deve essere scritto nella destinazione di rendering primaria, ovvero il buffer di trama fornito alla catena di scambio per la visualizzazione. Questa operazione è necessaria per i pixel shader: senza i dati sui colori pixel shader, Direct3D non avrebbe nulla da visualizzare.

Un esempio di un modello più pixel shader eseguire l'ombreggiatura Phong potrebbe essere simile al seguente. Poiché i vettori e le normali sono stati interpolati, non è necessario calcolarli in base al pixel. Tuttavia, è necessario ri normalizzarle a causa del funzionamento dell'interpolazione. Concettualmente, è necessario "ruotare" gradualmente il vettore dalla direzione in corrispondenza del vertice A alla direzione in corrispondenza del vertice B, mantenendone la lunghezza: l'interpolazione wheras taglia invece una linea retta tra i due endpoint del vettore.

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

In un altro esempio, il pixel shader accetta i propri buffer costanti che contengono informazioni leggere e materiali. Il layout di input nel vertex shader verrà espanso per includere dati normali e l'output di tale vertex shader includerà vettori trasformati per il vertice, la luce e la normale del vertice nel sistema di coordinate di visualizzazione.

Se si dispone di buffer di trama e campionatori con registri assegnati (**rispettivamente t** e **s**), è possibile accedervi anche nel pixel shader.

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

Gli shader sono strumenti molto potenti che possono essere usati per generare risorse procedurali come mappe ombreggiate o trame di disturbo. In effetti, le tecniche avanzate richiedono che le trame siano più astratte, non come elementi visivi ma come buffer. Contengono dati come informazioni sull'altezza o altri dati che possono essere campionati nel passaggio di pixel shader finale o in quel frame specifico come parte di un passaggio di effetti a più fasi. Il campionamento multiplo è uno strumento potente e la colonna portante di molti effetti visivi moderni.

## <a name="next-steps"></a>Passaggi successivi

Si spera di avere familiarità con DirectX 11 a questo punto e si è pronti per iniziare a lavorare al progetto. Ecco alcuni collegamenti che consentono di rispondere ad altre domande sullo sviluppo con DirectX e C++:

-   [Sviluppo di giochi](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Usare Visual Studio per la programmazione di giochi DirectX](/previous-versions/windows/apps/dn166877(v=win.10))
-   [Sviluppo di giochi DirectX e procedure dettagliate di esempio](/previous-versions/windows/apps/hh465149(v=win.10))
-   [Risorse aggiuntive per la programmazione di giochi](/previous-versions/windows/apps/dn194515(v=win.10))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Usare le risorse dei dispositivi DirectX](work-with-dxgi.md)
</dt> <dt>

[Informazioni sulla pipeline di rendering Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 