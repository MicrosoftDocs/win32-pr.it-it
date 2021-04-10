---
description: In questa pagina viene illustrato come generare e utilizzare un effetto.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Uso di un effetto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125574"
---
# <a name="using-an-effect-direct3d-9"></a>Uso di un effetto (Direct3D 9)

In questa pagina viene illustrato come generare e utilizzare un effetto. Gli argomenti trattati includono:

-   [Creazione di un effetto](#create-an-effect)
-   [Eseguire il rendering di un effetto](#render-an-effect)
-   [Usare la semantica per trovare i parametri degli effetti](#use-semantics-to-find-effect-parameters)
-   [Usare gli handle per ottenere e impostare i parametri in modo efficiente](#use-handles-to-get-and-set-parameters-efficiently)
-   [Aggiungere informazioni sui parametri con le annotazioni](#add-parameter-information-with-annotations)
-   [Parametri dell'effetto di condivisione](#share-effect-parameters)
-   [Compilare un effetto offline](#compile-an-effect-offline)
-   [Migliorare le prestazioni con i preshader](#improve-performance-with-preshaders)
-   [Usare i blocchi di parametri per gestire i parametri degli effetti](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a>Creazione di un effetto

Di seguito è riportato un esempio di creazione di un effetto tratto dall' [esempio BasicHLSL](../directx-sdk--august-2009-.md). Il codice di creazione dell'effetto per la creazione di uno shader di debug è da **OnCreateDevice**:


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



Questa funzione accetta gli argomenti seguenti:

-   Dispositivo.
-   Nome del file di effetti.
-   Puntatore a un elenco di definizioni con terminazione NULL \# da utilizzare durante l'analisi dello shader.
-   Puntatore facoltativo a un gestore di inclusione scritto dall'utente. Il gestore viene chiamato dal processore ogni volta che è necessario risolvere un' \# inclusione.
-   Flag di compilazione dello shader che fornisce gli hint del compilatore su come verrà utilizzato lo shader. Queste opzioni includono:
    -   La convalida verrà ignorata se sono stati compilati noti shader validi.
    -   Ottimizzazione ignorata (talvolta utilizzata quando le ottimizzazioni rendono più difficile il debug).
    -   La richiesta di informazioni di debug da includere nello shader, in modo che sia possibile eseguirne il debug.
-   Pool di effetti. Se più di un effetto utilizza lo stesso puntatore del pool di memoria, le variabili globali negli effetti vengono condivise tra loro. Se non è necessario condividere le variabili di effetto, il pool di memoria può essere impostato su **null**.
-   Puntatore al nuovo effetto.
-   Puntatore a un buffer a cui è possibile inviare gli errori di convalida. In questo esempio il parametro è stato impostato su **null** e non è stato utilizzato.

> [!Note]  
> A partire da dicembre 2006 SDK, il compilatore DirectX 10 HLSL è ora il compilatore predefinito sia in DirectX 9 che in DirectX 10. Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .

 

## <a name="render-an-effect"></a>Eseguire il rendering di un effetto

La sequenza di chiamate per applicare lo stato di effetto a un dispositivo è la seguente:

-   [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) imposta la tecnica attiva.
-   [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) imposta il passaggio attivo.
-   [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) aggiorna le modifiche apportate a qualsiasi chiamata set nel passaggio. Questo metodo deve essere chiamato prima di qualsiasi chiamata di progetto.
-   [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) termina un passaggio.
-   [**ID3DXEffect:: end**](id3dxeffect--end.md) termina la tecnica attiva.

Il codice di rendering degli effetti è anche più semplice del codice di rendering corrispondente senza alcun effetto. Ecco il codice di rendering con effetto:


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



Il ciclo di rendering è costituito dall'esecuzione di query sull'effetto per verificare il numero di passaggi che contiene e quindi sulla chiamata di tutti i passaggi per una tecnica. Il ciclo di rendering può essere espanso per chiamare più tecniche, ognuna con più sessioni.

## <a name="use-semantics-to-find-effect-parameters"></a>Usare la semantica per trovare i parametri degli effetti

Una semantica è un identificatore associato a un parametro Effect per consentire a un'applicazione di cercare il parametro. Un parametro può avere al massimo una semantica. La semantica si trova dopo i due punti (:) dopo il nome del parametro. Ad esempio:


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



Se è stata dichiarata la variabile globale Effect senza usare una semantica, il risultato sarà simile al seguente:


```
float4x4 matWorldViewProj;
```



L'interfaccia Effect può usare una semantica per ottenere un handle per un parametro di effetto specifico. Ad esempio, il codice seguente restituisce l'handle della matrice:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



Oltre a eseguire ricerche in base al nome semantico, l'interfaccia degli effetti ha molti altri metodi per la ricerca di parametri.

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a>Usare gli handle per ottenere e impostare i parametri in modo efficiente

Gli handle forniscono un modo efficiente per fare riferimento a parametri, tecniche, passaggi e annotazioni effettivi con effetto. Gli handle (che sono di tipo D3DXHANDLE) sono puntatori di stringa. Gli handle passati in funzioni quali GetParameterxxx o GetAnnotationxxx possono essere in uno dei tre formati seguenti:

-   Handle restituito da una funzione, ad esempio GetParameterxxx.
-   Stringa contenente il nome del parametro, tecnica, passaggio o annotazione.
-   Handle impostato su **null**.

In questo esempio viene restituito un handle al parametro a cui è associata la semantica WORLDVIEWPROJ:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a>Aggiungere informazioni sui parametri con le annotazioni

Le annotazioni sono dati specifici dell'utente che possono essere collegati a qualsiasi tecnica, passaggio o parametro. Un'annotazione è un modo flessibile per aggiungere informazioni a singoli parametri. Le informazioni possono essere lette e usate in qualsiasi modo scelto dall'applicazione. Un'annotazione può essere di qualsiasi tipo di dati e può essere aggiunta dinamicamente. Le dichiarazioni di annotazione sono delimitate da parentesi angolari. Un'annotazione contiene:

-   Tipo di dati.
-   Nome della variabile.
-   Segno di uguale (=).
-   Valore dei dati.
-   Punto e virgola finale (;).

Ad esempio, entrambi gli esempi precedenti di questo documento contengono questa annotazione:


```
texture Tex0 < string name = "tiger.bmp"; >;
```



L'annotazione è collegata all'oggetto trama e specifica il file di trama da usare per inizializzare l'oggetto trama. L'annotazione non Inizializza l'oggetto trama. si tratta semplicemente di una parte di informazioni utente collegata alla variabile. Un'applicazione può leggere l'annotazione con [**ID3DXBaseEffect:: GetAnnotation**](id3dxbaseeffect--getannotation.md) o [**ID3DXBaseEffect:: GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) per restituire la stringa. È inoltre possibile aggiungere annotazioni dall'applicazione.

Ogni annotazione:

-   Deve essere numerico o stringhe.
-   Deve sempre essere inizializzato con un valore predefinito.
-   Può essere associato a [tecniche e passaggi (Direct3D 9)](techniques-and-passes.md) e ai parametri di [effetto](/previous-versions/windows/desktop/ee417539(v=vs.85))di primo livello.
-   È possibile scrivere e leggere da con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).
-   Può essere aggiunto con [**ID3DXEffect**](id3dxeffect.md).
-   Non è possibile fare riferimento all'interno dell'effetto.
-   Non è possibile avere una semantica o annotazioni secondarie.

## <a name="share-effect-parameters"></a>Parametri dell'effetto di condivisione

I parametri degli effetti sono tutte le variabili non statiche dichiarate in un effetto. Possono essere incluse le variabili globali e le annotazioni. I parametri effetti possono essere condivisi tra diversi effetti dichiarando i parametri con la parola chiave "Shared" e quindi creando l'effetto con un pool di effetti.

Un pool di effetti contiene i parametri degli effetti condivisi. Il pool viene creato chiamando [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), che restituisce un'interfaccia [**ID3DXEffectPool**](id3dxeffectpool.md) . L'interfaccia può essere fornita come input per qualsiasi funzione D3DXCreateEffectxxx quando viene creato un effetto. Affinché un parametro venga condiviso tra più effetti, il parametro deve avere lo stesso nome, tipo e semantica in ciascuno degli effetti condivisi.


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



Gli effetti che condividono i parametri devono usare lo stesso dispositivo. Questa operazione viene applicata per evitare la condivisione di parametri dipendenti dal dispositivo, ad esempio shader o trame, in dispositivi diversi. I parametri vengono eliminati dal pool ogni volta che vengono rilasciati gli effetti che contengono i parametri condivisi. Se non è necessario condividere parametri, specificare **null** per il pool di effetti quando viene creato un effetto.

Gli effetti clonati utilizzano lo stesso pool di effetti dell'effetto da cui vengono clonati. La clonazione di un effetto crea una copia esatta di un effetto, incluse le variabili globali, le tecniche, i passaggi e le annotazioni.

## <a name="compile-an-effect-offline"></a>Compilare un effetto offline

È possibile compilare un effetto in fase di esecuzione con [**D3DXCreateEffect**](d3dxcreateeffect.md)oppure è possibile compilare un effetto offline usando lo strumento compilatore della riga di comando fxc.exe. L'effetto nell' [esempio CompiledEffect](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contiene un vertex shader, un pixel shader e una tecnica:


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



Usando lo [strumento del compilatore degli effetti](../direct3dtools/fxc.md) per compilare lo shader per vs \_ 1 \_ 1, sono state generate le seguenti istruzioni per gli shader di assembly:


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a>Migliorare le prestazioni con i preshader

Un preshader è una tecnica che consente di aumentare l'efficienza dello shader tramite il pre-calcolo delle espressioni di shader costanti. Il compilatore Effect estrae automaticamente i calcoli dello shader dal corpo di uno shader e li esegue sulla CPU prima dello shader che esegue. Di conseguenza, i preshader funzionano solo con effetti. Ad esempio, queste due espressioni possono essere valutate all'esterno dello shader prima dell'esecuzione.


```
mul(World,mul(View, Projection));
sin(time)
```



I calcoli dello shader che è possibile spostare sono quelli associati a parametri uniformi; ovvero, i calcoli non cambiano per ogni vertice o pixel. Se si usano gli effetti, il compilatore Effect genera automaticamente ed esegue un preshader. Nessun flag da abilitare. I preshader possono ridurre il numero di istruzioni per shader e possono anche ridurre il numero di registri costanti utilizzati da uno shader.

Il compilatore degli effetti può essere considerato come un tipo di compilatore multiprocessore perché compila il codice dello shader per due tipi di processori: una CPU e una GPU. Inoltre, il compilatore Effect è progettato per spostare il codice dalla GPU alla CPU e quindi migliorare le prestazioni dello shader. Questa operazione è molto simile all'estrazione di un'espressione statica da un ciclo. Uno shader che trasforma la posizione dallo spazio globale allo spazio di proiezione e copia le coordinate di trama hanno un aspetto simile al seguente in HLSL:


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



L'uso [dello strumento compilatore effetti](../direct3dtools/fxc.md) per compilare lo shader per vs \_ 1 \_ 1 genera le istruzioni di assembly seguenti:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Questa operazione utilizza circa 14 slot e utilizza 9 registri costanti. Con un preshader, il compilatore sposta le espressioni statiche fuori dallo shader e nell'oggetto preshader. Lo stesso shader avrà un aspetto simile al seguente con un preshader:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Un effetto esegue un preshader immediatamente prima dell'esecuzione di uno shader. Il risultato è la stessa funzionalità con un aumento delle prestazioni dello shader poiché il numero di istruzioni da eseguire (per ogni vertice o pixel a seconda del tipo di shader) è stato ridotto. Inoltre, un numero inferiore di registri costanti viene utilizzato dallo shader come risultato delle espressioni statiche spostate nel preshader. Ciò significa che gli shader precedentemente limitati dal numero di registri costanti richiesti possono ora essere compilati perché richiedono un minor numero di registri costanti. È ragionevole prevedere un miglioramento delle prestazioni del 5% e del 20% rispetto ai preshader.

Tenere presente che le costanti di input sono diverse dalle costanti di output in un preshader. L'output C1 non corrisponde al registro C1 di input. La scrittura in un registro costante in un preshader scrive effettivamente nello slot di input (costante) dello shader corrispondente.


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



Con l'istruzione CMP precedente verrà letto il valore C1 preshader, mentre l'istruzione mul scriverà nei registri dell'hardware shader che verranno usati dal vertex shader.

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a>Usare i blocchi di parametri per gestire i parametri degli effetti

I blocchi di parametri sono blocchi delle modifiche allo stato dell'effetto. Un blocco di parametri può registrare le modifiche di stato, in modo che possano essere applicate in un secondo momento con una singola chiamata. Creare un blocco di parametri chiamando [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md):


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



Il blocco di parametri Salva quattro modifiche applicate dalle chiamate API. La chiamata di [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md) avvia la registrazione delle modifiche dello stato. [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md) interrompe l'aggiunta delle modifiche al blocco di parametri e restituisce un handle. L'handle verrà usato durante la chiamata di [**ID3DXEffect:: ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).

Nell' [esempio EffectParam](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), il blocco di parametri viene applicato nella sequenza di rendering:


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



Il blocco di parametri imposta il valore di tutte e quattro le modifiche dello stato appena prima della chiamata a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) . I blocchi di parametri sono un modo pratico per impostare più modifiche di stato con una singola chiamata API.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti](effects.md)
</dt> </dl>

 

 
