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
# <a name="work-with-shaders-and-shader-resources"></a>Usare shader e risorse shader

È giunto il momento di imparare a usare shader e risorse dello shader per lo sviluppo di Microsoft DirectX Game per Windows 8. È stato illustrato come configurare il dispositivo e le risorse di grafica ed è possibile che sia stata avviata anche la modifica della pipeline. Verranno ora esaminati i pixel e i vertex shader.

Se non si ha familiarità con i linguaggi shader, una discussione rapida è in ordine. Gli shader sono piccoli programmi di basso livello compilati ed eseguiti in fasi specifiche della pipeline grafica. La loro specialità è operazioni matematiche a virgola mobile molto veloci. I programmi shader più comuni sono i seguenti:

-   **Vertex shader**: eseguito per ogni vertice in una scena. Questo shader agisce sugli elementi del buffer dei vertici forniti dall'app chiamante e produce almeno un vettore di posizione a 4 componenti che verrà rasterizzato in una posizione in pixel.
-   **Pixel shader**: eseguito per ogni pixel in una destinazione di rendering. Questo shader riceve le coordinate rasterizzate dalle fasi precedenti dello shader (nelle pipeline più semplici, questo sarebbe il vertex shader) e restituisce un colore (o un altro valore a 4 componenti) per tale posizione in pixel, che viene quindi scritta in una destinazione di rendering.

Questo esempio include vertex shader e pixel shader di base che attingono solo la geometria e shader più complessi che aggiungono calcoli di illuminazione di base.

I programmi shader sono scritti in Microsoft High Level Shader Language (HLSL). La sintassi di HLSL ha un aspetto molto simile a C, ma senza i puntatori. I programmi shader devono essere molto compatta ed efficiente. Se lo shader viene compilato in un numero eccessivo di istruzioni, non può essere eseguito e viene restituito un errore. Si noti che il numero esatto di istruzioni consentito è parte del [livello di funzionalità Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).

In Direct3D gli shader non vengono compilati in fase di esecuzione. vengono compilati quando viene compilato il resto del programma. Quando si compila l'app con Microsoft Visual Studio 2013, i file HLSL vengono compilati in file CSO (. CSO) che l'app deve caricare e inserire nella memoria GPU prima del disegno. Quando si crea un pacchetto, assicurarsi di includere i file CSO con l'app. si tratta di asset come mesh e trame.

## <a name="understand-hlsl-semantics"></a>Comprendere la semantica di HLSL

Prima di continuare, è importante esaminare la semantica di HLSL, perché spesso si tratta di un punto di confusione per i nuovi sviluppatori Direct3D. La semantica di HLSL sono stringhe che identificano un valore passato tra l'app e un programma shader. Sebbene possano essere diverse stringhe possibili, la procedura consigliata consiste nell'usare una stringa come `POSITION` o `COLOR` che indichi l'utilizzo. Questa semantica viene assegnata quando si costruisce un buffer costante o un layout di input. Puoi anche aggiungere un numero compreso tra 0 e 7 alla semantica in modo da usare registri separati per valori simili. Ad esempio: COLOR0, COLOR1, COLOR2...

La semantica che è preceduta da "SV \_ " è la semantica del *valore di sistema* che viene scritta dal programma shader; il gioco stesso (in esecuzione sulla CPU) non può modificarli. In genere, queste semantiche contengono valori che sono input o output di un'altra fase shader nella pipeline grafica o che vengono generati interamente dalla GPU.

Inoltre, `SV_` la semantica ha comportamenti diversi quando vengono usati per specificare l'input o l'output da una fase dello shader. Ad esempio, `SV_POSITION` (output) contiene i dati dei vertici trasformati durante la fase vertex shader e `SV_POSITION` (*input*) contiene i valori di posizione dei pixel interpolati dalla GPU durante la fase di rasterizzazione.

Ecco alcune comuni semantica di HLSL:

-   `POSITION`(*n*) per i dati del buffer del vertice. `SV_POSITION` fornisce una posizione in pixel per la pixel shader e non può essere scritta dal gioco.
-   `NORMAL`(*n*) per i dati normali forniti dal buffer dei vertici.
-   `TEXCOORD`(*n*) per i dati della coordinata UV della trama forniti a uno shader.
-   `COLOR`(n) per i dati dei colori RGBA forniti a uno shader. Si noti che viene trattato in modo identico per le coordinate dei dati, inclusa l'interpolazione del valore durante la rasterizzazione; la semantica semplifica semplicemente l'identificazione dei dati di colore.
-   `SV_Target`\[n \] per la scrittura da un pixel shader a una trama di destinazione o un altro buffer pixel.

Verranno illustrati alcuni esempi di semantica di HLSL quando si esamina l'esempio.

## <a name="read-from-the-constant-buffers"></a>Lettura dai buffer costanti

Qualsiasi shader può leggere da un buffer costante se tale buffer è collegato alla propria fase come risorsa. In questo esempio solo al vertex shader viene assegnato un buffer costante.

Il buffer costante viene dichiarato in due posizioni: nel codice C++ e nei file HLSL corrispondenti che lo accederanno.

Di seguito viene illustrato il modo in cui viene dichiarata la struttura del buffer costante nel codice C++.


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



Quando si dichiara la struttura per il buffer costante nel codice C++, assicurarsi che tutti i dati siano allineati correttamente lungo i limiti di 16 byte. Il modo più semplice per eseguire questa operazione consiste nell'usare i tipi [DirectXMath](/windows/desktop/dxmath/directxmath-portal) , come **XMFLOAT4** o **XMFLOAT4X4**, come illustrato nel codice di esempio. È inoltre possibile proteggere i buffer non allineati dichiarando un'asserzione statica:


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



Questa riga di codice provocherà un errore in fase di compilazione se **ConstantBufferStruct** non è allineato a 16 byte. Per ulteriori informazioni sull'allineamento e la compressione costanti del buffer, vedere [regole di compressione per variabili costanti](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

A questo punto, di seguito viene illustrato il modo in cui viene dichiarato il buffer costante nel HLSL vertex shader.


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



Tutti i buffer: costante, trama, campionatore o altro, devono avere un registro definito in modo che la GPU possa accedervi. Ogni fase dello shader consente fino a 15 buffer costanti e ogni buffer può ospitare fino a 4.096 variabili costanti. La sintassi della dichiarazione Register-Usage è la seguente:

-   **b * * *\#* : un registro per un buffer costante (** cbuffer * *).
-   **t * * *\#* : un registro per un buffer di trama (** tbuffer * *).
-   **s * * * \#*: un registro per un campionatore. Un campionatore definisce il comportamento di ricerca per i Texel nella risorsa di trama.

Ad esempio, HLSL per un pixel shader potrebbe richiedere una trama e un campionatore come input con una dichiarazione come questa.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

È compito dell'utente assegnare i buffer costanti ai registri: quando si configura la pipeline, si associa un buffer costante allo stesso slot a cui è stato assegnato il file HLSL. Nell'argomento precedente, ad esempio, la chiamata a [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indica ' 0' per il primo parametro. Che indica a Direct3D di alleghiare la risorsa del buffer costante al registro 0, che corrisponde all'assegnazione del buffer per la **registrazione (B0)** nel file HLSL.

## <a name="read-from-the-vertex-buffers"></a>Lettura dai buffer dei vertici

Il buffer dei vertici fornisce i dati del triangolo per gli oggetti della scena ai vertex shader. Come per il buffer costante, lo struct del buffer dei vertici viene dichiarato nel codice C++, usando regole di compressione simili.


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



Non esiste un formato standard per i dati dei vertici in Direct3D 11. Si definisce invece il layout dei dati dei vertici usando un descrittore; i campi dati vengono definiti mediante una matrice di [**strutture \_ d3d11 \_ input \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) . In questo esempio viene illustrato un layout di input semplice che descrive lo stesso formato di vertex dello struct precedente:


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



Se si aggiungono dati al formato vertex quando si modifica il codice di esempio, assicurarsi di aggiornare anche il layout di input oppure lo shader non sarà in grado di interpretarlo. È possibile modificare il layout dei vertici in questo modo:


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



In tal caso, modificare la definizione del layout di input come indicato di seguito.


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



Ognuna delle definizioni degli elementi di layout di input è preceduta da una stringa, ad esempio "POSITION" o "NORMAL", che è la semantica descritta in precedenza in questo argomento. È come un handle che consente alla GPU di identificare tale elemento durante l'elaborazione del vertice. Scegliere nomi comuni e significativi per gli elementi del vertice.

Proprio come per il buffer costante, il vertex shader ha una definizione di buffer corrispondente per gli elementi del vertice in ingresso. Per questo motivo è stato fornito un riferimento alla risorsa vertex shader quando si crea il layout di input. Direct3D convalida il layout dei dati per vertice con lo struct di input dello shader. Si noti come la semantica corrisponda tra la definizione del layout di input e questa dichiarazione del buffer HLSL. Viene tuttavia `COLOR` aggiunto un valore "0". Non è necessario aggiungere 0 se nel layout è dichiarato un solo `COLOR` elemento, ma è consigliabile aggiungerlo nel caso in cui si scelga di aggiungere altri elementi di colore in futuro.


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a>Passare i dati tra gli shader

Gli shader accettano i tipi di input e restituiscono i tipi di output dalle funzioni principali al momento dell'esecuzione. Per il vertex shader definito nella sezione precedente, il tipo di input è la struttura di input di Visual Studio ed è stato \_ definito un layout di input e uno struct C++ corrispondenti. Una matrice di questo struct viene utilizzata per creare un buffer vertex nel metodo **CreateCube** .

Il vertex shader restituisce una struttura di \_ input PS, che deve contenere almeno la posizione del vertice finale a 4 componenti (float4). Questo valore di posizione deve avere la semantica del valore di sistema, `SV_POSITION` , dichiarata in modo che la GPU disponga dei dati necessari per eseguire il passaggio successivo del disegno. Si noti che non esiste una corrispondenza 1:1 tra l'output del vertex shader e l'input pixel shader; il vertex shader restituisce una struttura per ogni vertice assegnato, ma il pixel shader viene eseguito una volta per ogni pixel. Ciò è dovuto al fatto che i dati per vertice passano per primo attraverso la fase di rasterizzazione. Questa fase decide quali pixel "coprire" la geometria che si sta disegnando, calcola i dati per vertice interpolati per ogni pixel, quindi chiama il pixel shader una volta per ognuno di questi pixel. L'interpolazione è il comportamento predefinito quando si rasterizzano i valori di output ed è essenziale in particolare per l'elaborazione corretta dei dati vettoriali di output (vettori di luce, normali e tangenti per vertice e altri).


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a>Esaminare il vertex shader

Il vertex shader di esempio è molto semplice: assumere un vertice (posizione e colore), trasformare la posizione dalle coordinate del modello in coordinate proiettate prospettiche e restituirla (insieme al colore) al rasterizzatore. Si noti che il valore del colore è interpolato a destra insieme ai dati di posizione, fornendo un valore diverso per ogni pixel anche se il vertex shader non ha eseguito calcoli sul valore del colore.


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



Un vertex shader più complesso, ad esempio uno che imposta i vertici di un oggetto per l'ombreggiatura Phong, potrebbe avere un aspetto simile al seguente. In questo caso, si sta sfruttando il fatto che i vettori e le normali vengono interpolati per approssimarsi a una superficie di aspetto uniforme.

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

Questo pixel shader in questo esempio è probabilmente la quantità minima assoluta di codice che è possibile avere in una pixel shader. Accetta i dati del colore del pixel interpolati generati durante la rasterizzazione e li restituisce come output, dove verranno scritti in una destinazione di rendering. Quanto è noioso!


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



La parte importante è la `SV_TARGET` semantica del valore del sistema sul valore restituito. Indica che l'output deve essere scritto nella destinazione di rendering primaria, ovvero il buffer di trama fornito alla catena di scambio per la visualizzazione. Questa operazione è necessaria per i pixel shader, senza i dati relativi al colore dal pixel shader, Direct3D non avrà alcun elemento da visualizzare.

Un esempio di pixel shader più complesso per eseguire l'ombreggiatura Phong potrebbe essere simile al seguente. Poiché i vettori e le normali sono stati interpolati, non è necessario calcolarli in base ai singoli pixel. Tuttavia, è necessario rinormalizzarli a causa del funzionamento dell'interpolazione. dal punto di vista concettuale, è necessario "ruotare" gradualmente il vettore dalla direzione del vertice a fino alla direzione del vertice B, mantenendo la relativa lunghezza. l'interpolazione considerando taglia invece una linea retta tra i due endpoint vettoriali.

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

In un altro esempio, il pixel shader prende i propri buffer costanti che contengono informazioni leggere e materiali. Il layout di input nel vertex shader verrebbe espanso in modo da includere i dati normali e l'output del vertex shader dovrebbe includere vettori trasformati per il vertice, la luce e il vertice normale nel sistema di coordinate di visualizzazione.

Se sono presenti buffer di trama e sampler con registri assegnati (rispettivamente **t** e **s**), è possibile accedervi anche nel pixel shader.

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

Gli shader sono strumenti molto potenti che possono essere usati per generare risorse procedurali come mappe Shadow o trame non significative. Infatti, le tecniche avanzate richiedono che si pensi alle trame in modo più astratto, non come elementi visivi, ma come buffer. Mantengono i dati, ad esempio le informazioni sull'altezza, o altri dati che possono essere campionati nel passaggio finale pixel shader o in quel particolare frame come parte di una sessione di effetti in più fasi. Il campionamento multiplo è uno strumento potente e il backbone di molti effetti visivi moderni.

## <a name="next-steps"></a>Passaggi successivi

È probabile che l'utente abbia familiarità con DirectX 11at questo punto e sia pronto per iniziare a lavorare sul progetto. Di seguito sono riportati alcuni collegamenti che consentono di rispondere ad altre domande che possono verificarsi sullo sviluppo con DirectX e C++:

-   [Sviluppo di giochi](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Usare gli strumenti di Visual Studio per la programmazione dei giochi DirectX](/previous-versions/windows/apps/dn166877(v=win.10))
-   [Procedure dettagliate per lo sviluppo di giochi DirectX e esempi](/previous-versions/windows/apps/hh465149(v=win.10))
-   [Risorse aggiuntive per la programmazione di giochi](/previous-versions/windows/apps/dn194515(v=win.10))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Usare le risorse del dispositivo DirectX](work-with-dxgi.md)
</dt> <dt>

[Informazioni sulla pipeline di rendering Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 