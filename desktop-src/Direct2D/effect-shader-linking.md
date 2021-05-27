---
title: Collegamento degli shader degli effetti
description: Direct2D usa un'ottimizzazione denominata collegamento effect shader che combina più passaggi di rendering del grafico degli effetti in un singolo passaggio.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6bad2170f2b897a5cf8ac3086a74945efa8bf
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549236"
---
# <a name="effect-shader-linking"></a>Collegamento degli shader degli effetti

Direct2D usa un'ottimizzazione denominata collegamento effect shader che combina più passaggi di rendering del grafico degli effetti in un singolo passaggio.

-   [Panoramica del collegamento degli shader degli effetti](#overview-of-effect-shader-linking)
-   [Uso del collegamento degli shader degli effetti](#using-effect-shader-linking)
-   [Creazione di un effetto personalizzato compatibile con il collegamento di shader](#authoring-a-shader-linking-compatible-custom-effect)
-   [Esempio di shader con effetto compatibile con il collegamento](#example-linking-compatible-effect-shader)
-   [Compilazione di un linking compatible-shader](#compiling-a-linking-compatible-shader)
    -   [Passaggio 1: Compilare la funzione di esportazione](#step-1-compile-the-export-function)
    -   [Passaggio 2: Compilare lo shader completo e incorporare la funzione di esportazione](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [Esportare le specifiche della funzione](#export-function-specifications)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-effect-shader-linking"></a>Panoramica del collegamento degli shader degli effetti

Le ottimizzazioni di collegamento degli effetti shader si basano sul collegamento dello shader HLSL, una funzionalità Direct3D 11.2 che consente di generare pixel e vertex shader in fase di esecuzione collegando funzioni shader precompilato. Le figure seguenti illustrano il concetto di collegamento degli shader degli effetti in un grafico degli effetti. La prima figura mostra un tipico grafico degli effetti Direct2D con quattro trasformazioni di rendering. Senza il collegamento dello shader, ogni trasformazione utilizza un passaggio di rendering e richiede una superficie intermedia. in totale, questo grafo richiede 4 passaggi e 3 intermedi.

![Grafico di trasformazione senza collegamento shader: 4 passaggi e 3 intermedi.](images/shader-transform-graph.png)

La seconda figura mostra lo stesso grafico degli effetti in cui ogni trasformazione di rendering è stata sostituita con una versione di funzione collegabile. Direct2D è in grado di collegare l'intero grafo ed eseguirlo in un unico passaggio senza richiedere alcun elemento intermedio. Ciò può fornire una riduzione significativa del tempo di esecuzione della GPU e una riduzione del consumo di memoria GPU di picco.

![Grafico di trasformazione con collegamento shader: 1 passaggio, 0 intermedi.](images/shader-linking-graph.png)



 

Il collegamento degli effetti shader funziona su singole trasformazioni all'interno di un effetto; Ciò significa che anche un grafo con un singolo effetto può trarre vantaggio dal collegamento dello shader se tale effetto ha più trasformazioni valide.

## <a name="using-effect-shader-linking"></a>Uso del collegamento degli shader degli effetti

Se si sta creando un'applicazione Direct2D che usa gli effetti, non è necessario eseguire alcun'operazione per sfruttare i vantaggi del collegamento degli shader degli effetti. Direct2D analizza automaticamente il grafico degli effetti per determinare il modo più ottimale per collegare ogni trasformazione.

Gli autori di effetti sono responsabili dell'implementazione del loro effetto in modo che supporti il collegamento degli shader degli effetti; Per altre informazioni, vedere la sezione [Creazione di un](#authoring-a-shader-linking-compatible-custom-effect) effetto personalizzato compatibile con il collegamento di uno shader di seguito. Tutti gli effetti predefiniti supportano il collegamento dello shader.

Direct2D collega solo trasformazioni di rendering adiacenti in situazioni in cui è utile. Tiene conto di più fattori quando si determina se collegare due trasformazioni. Ad esempio, il collegamento dello shader non viene eseguito se una delle trasformazioni usa vertex o compute shader, perché è possibile collegare solo pixel shader. Inoltre, se un effetto non è stato creato per essere compatibile con il collegamento dello shader, le trasformazioni circostanti non verranno collegate ad esso.

Nel caso in cui esista un tale rischio di collegamento, Direct2D non collega alcuna trasformazione adiacente al pericolo, ma tenta comunque di collegare il resto del grafico.

![grafico di trasformazione con un pericolo di collegamento: 2 passaggi, 1 intermedio.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>Creazione di un effetto personalizzato compatibile con il collegamento di shader

Se si crea un effetto Direct2D personalizzato, è necessario assicurarsi che le relative trasformazioni supportino il collegamento degli shader degli effetti. Ciò richiede alcune modifiche secondarie rispetto alla modalità di implementazione degli effetti personalizzati precedenti. Se una trasformazione all'interno dell'effetto personalizzato non supporta il collegamento dello shader, Direct2D non la collega alle trasformazioni adiacenti nel grafico degli effetti.

L'autore di un effetto personalizzato deve essere a conoscenza di diversi concetti e requisiti chiave:

-   **Nessuna modifica alle implementazioni dell'interfaccia effettive**

    Non è necessario modificare il codice che implementa le varie interfacce di effetto, ad esempio [ID2D1DrawTransform.](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)

-   **Fornire sia una versione completa che una versione della funzione di esportazione degli shader**

    È necessario fornire una versione della funzione di esportazione degli shader dell'effetto collegabili da Direct2D. È anche necessario continuare a fornire lo shader originale completo. Ciò è dovuto al fatto che Direct2D seleziona in fase di esecuzione la versione corretta dello shader a seconda che il collegamento dello shader sia applicato a un particolare collegamento nel grafico.

    Se una trasformazione fornisce solo il BLOB pixel shader completo (tramite [ID2D1EffectContext::LoadPixelShader),](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)non verrà collegato alle trasformazioni adiacenti.

- **Funzioni helper**

    Direct2D fornisce macro [e funzioni helper HLSL](hlsl-helpers.md) che generano automaticamente le versioni delle funzioni complete ed esportate di uno shader. Questi helper sono disponibili in d2d1effecthelpers.hlsli. Inoltre, il compilatore HLSL (FXC) consente di inserire lo shader della funzione di esportazione in un campo privato nello shader completo. In questo modo, è necessario creare uno shader una sola volta e passare entrambe le versioni a Direct2D contemporaneamente. Sia d2d1effecthelpers.hlsli che il compilatore FXC sono inclusi come parte del Windows SDK.

    Le funzioni helper:

  - [D2DGetInput](d2dgetinput.md)  
  - [D2DSampleInput](d2dsampleinput.md)  
  - [D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
  - [D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
  - [D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
  - [D2DGetScenePosition](d2dgetsceneposition.md)  
  - [VOCE D2D \_ \_ PS](d2d-ps-entry.md)  

  È anche possibile creare manualmente due versioni di ogni shader e compilarle due volte, purché siano soddisfatte le specifiche descritte di seguito in [Esportare](#export-function-specifications) le specifiche della funzione.

-   **Solo pixel shader**

    Direct2D non supporta il collegamento di calcolo o vertex shader. Tuttavia, se l'effetto usa sia un vertice che pixel shader, l'output del pixel shader può comunque essere collegato.

-   **Campionamento semplice e complesso**

    Il collegamento della funzione shader funziona connettendo l'output di pixel shader passaggio all'input di un passaggio pixel shader successivo. Ciò è possibile solo quando l'pixel shader richiede un solo valore di input per eseguire il calcolo. questo valore deriva in genere dal campionamento di una trama di input in corrispondenza della coordinata di trama emessa dal vertex shader. Tale pixel shader si dice che eseere un campionamento semplice.

    ![La conversione in scala di grigi è un esempio di campionamento semplice. il valore di un particolare pixel di output dipende solo dal valore del pixel di input corrispondente.](images/simple-sampling.png)

    Alcuni pixel shader, ad esempio una sfocatura gaussiana, calcolano l'output da più campioni di input anziché da un singolo campione. Tale pixel shader si dice che eseere un campionamento complesso.

    

    ![La sfocatura gaussiana è un esempio di campionamento complesso. il valore del pixel di output centrale dipende da più pixel di input.](images/complex-sampling.png)

    
    Solo le funzioni shader con input semplici possono avere l'input fornito da un'altra funzione shader. Le funzioni shader con input complessi devono essere fornite con una trama di input da campionare. Ciò significa che Direct2D non collega uno shader con input complessi al relativo predecessore.

    Quando si usano [gli helper HLSL Direct2D,](hlsl-helpers.md)è necessario indicare in HLSL se uno shader usa input complessi o semplici.

## <a name="example-linking-compatible-effect-shader"></a>Esempio di shader con effetto compatibile con il collegamento

Usando gli helper D2D, il frammento di codice seguente rappresenta un semplice shader con effetto compatibile con il collegamento:

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

In questo breve esempio si noti che non viene dichiarato alcun parametro di funzione, che il numero di input e il tipo di ogni input vengono dichiarati prima della funzione di immissione, l'input viene recuperato chiamando [D2DGetInput](d2dgetinput.md)e che le direttive del preprocessore devono essere definite prima dell'inserimento del file helper.

Uno shader compatibile con il collegamento deve fornire sia una normale funzione a pixel shader che una funzione di esportazione shader. La macro [D2D \_ PS \_ ENTRY](d2d-ps-entry.md) consente di generare ognuno di questi elementi dallo stesso codice, se usato in combinazione con lo script di compilazione dello shader.

Quando si compila uno shader completo, le macro vengono espanse nel codice seguente, che ha una firma di input compatibile con gli effetti D2D.

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

Quando si compila una versione della funzione di esportazione dello stesso codice, viene generato il codice seguente:

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

Si noti che l'input della trama, normalmente recuperato tramite campionamento di texture2D, è stato sostituito con un input di funzione (input0).

Per una descrizione dettagliata completa delle operazioni da eseguire per scrivere un effetto [](custom-effects.md) compatibile con il collegamento, vedere l'esercitazione sugli effetti personalizzati e l'esempio di effetti immagine personalizzati [Direct2D.](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

## <a name="compiling-a-linking-compatible-shader"></a>Compilazione di uno shader compatibile con il collegamento

Per poter essere collegabile, pixel shader BLOB passato a D2D deve contenere sia la versione completa che la versione della funzione di esportazione dello shader. Questa operazione viene eseguita incorporando la funzione di esportazione compilata nell'area DATI \_ PRIVATI DEL BLOB D3D. \_ \_

Quando gli shader vengono creati con le funzioni helper D2D, è necessario definire una destinazione di compilazione D2D in fase di compilazione. I tipi di destinazione di compilazione sono D2D \_ FULL \_ SHADER e D2D \_ FUNCTION.

La compilazione di uno shader con effetto compatibile con il collegamento è un processo in due passaggi:

-   [Compilare la funzione di esportazione](#step-1-compile-the-export-function)
-   [Compilare lo shader completo e incorporare la funzione di esportazione](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> Quando si compila un effetto usando Visual Studio, è necessario creare un file batch che esegue entrambi i comandi FXC ed eseguire questo file batch come istruzione di compilazione personalizzata che viene eseguita prima del passaggio di compilazione.

 

### <a name="step-1-compile-the-export-function"></a>Passaggio 1: Compilare la funzione di esportazione

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

Per compilare la versione della funzione di esportazione dello shader, è necessario passare i flag seguenti a FXC.



|    Flag                            |    Descrizione                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /t <ShaderModel>         | Impostare <ShaderModel> sul profilo di pixel shader appropriato, come definito in [Sintassi FXC.](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) Deve trattarsi di uno dei profili elencati in "Collegamento dello shader HLSL". |
| <MyShaderFile>.hlsl      | Impostare <MyShaderFile> sul nome del file HLSL.                                                                                                                                                                                                    |
| FUNZIONE /D \_ D2D               | Questa definizione indica a FXC di compilare la versione della funzione di esportazione dello shader.                                                                                                                                                                       |
| /D D D2D \_ ENTRY=<entry>    | Impostare <entry> sul nome del punto di ingresso HLSL definito all'interno della macro [D2D \_ PS \_ ENTRY.](d2d-ps-entry.md)                                                                                                                                    |
| /Fl <MyShaderFile> .fxlib | Impostare <MyShaderfile> su in cui archiviare la versione della funzione di esportazione dello shader. Si noti che l'estensione .fxlib è solo per facilitare l'identificazione.                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>Passaggio 2: Compilare lo shader completo e incorporare la funzione di esportazione

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

Per compilare la versione completa dello shader con la versione di esportazione incorporata, è necessario passare i flag seguenti a FXC.



|    Flag                                    |    Descrizione                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /t <ShaderModel>                 | Impostare <ShaderModel> sul profilo di pixel shader appropriato, come definito in [Sintassi FXC.](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) Deve essere il profilo pixel shader corrispondente al profilo di collegamento specificato nel passaggio 1. |
| <MyShaderFile>.hlsl              | Impostare <MyShaderFile> sul nome del file HLSL.                                                                                                                                                                                                                               |
| /D D D2D \_ FULL \_ SHADER                   | Questa definizione indica a FXC di compilare la versione completa dello shader.                                                                                                                                                                                                             |
| /D D D2D \_ ENTRY=<entry>            | Impostare <entry> sul nome del punto di ingresso HLSL definito all'interno della macro D2D PS \_ \_ ENTRY().                                                                                                                                                                                 |
| /e <entry>                       | Impostare <entry> sul nome del punto di ingresso HLSL definito all'interno della macro D2D \_ PS \_ ENTRY().                                                                                                                                                                                 |
| /setprivate <MyShaderFile> .fxlib | Questo argomento indica a FXC di incorporare lo shader della funzione di esportazione generato nel passaggio 1 nell'area DATI PRIVATI \_ DEL BLOB D3D. \_ \_                                                                                                                                                          |
| /Fo <MyShader> .cso               | Impostare <MyShader> su dove si vuole archiviare lo shader compilato finale combinato.                                                                                                                                                                                                 |
| /Fh <MyShader> .h                 | Impostare <MyShader> su dove si vuole archiviare l'intestazione finale combinata.                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a>Esportare le specifiche della funzione

È possibile, anche se non consigliato, creare uno shader con effetto compatibile senza usare gli helper forniti da D2D. È necessario assicurarsi che sia lo shader completo che le firme di input della funzione di esportazione siano conformi alle specifiche D2D.

Le specifiche per gli shader completi sono le stesse delle versioni precedenti di Windows. In breve, i pixel shader di input devono essere SV POSITION, SCENE POSITION e \_ \_ un TEXCOORD per ogni input dell'effetto.

Per la funzione di esportazione, la funzione deve restituire un valore float4 e i relativi input devono essere di uno dei tipi seguenti:

-   Input semplice

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    Per gli input semplici, D2D inserirà una funzione Sample tra la trama di input e la funzione shader oppure l'input verrà fornito dall'output di un'altra funzione shader.

-   Input complesso

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    Per gli input complessi, D2D passerà solo una coordinata di trama, come descritto Windows 8 documentazione.

-   Percorso di output

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    È possibile definire \_ un solo input SCENE POSITION. Questo parametro deve essere incluso solo quando necessario, perché solo una funzione per shader collegato può usare questo parametro.

La semantica deve essere definita come sopra, perché D2D ispeziona la semantica per decidere come collegare le funzioni. Se un input di funzione non corrisponde a uno dei tipi precedenti, la funzione verrà rifiutata per il collegamento dello shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Helper HLSL](hlsl-helpers.md)
</dt> <dt>

[Interfaccia ID3D11Linker](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[Interfaccia ID3D11FunctionLinkingGraph](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 