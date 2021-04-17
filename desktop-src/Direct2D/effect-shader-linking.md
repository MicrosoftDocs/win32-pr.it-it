---
title: Collegamento Effect shader
description: Direct2D usa un'ottimizzazione denominata Effect shader linking che combina il rendering del grafico a più effetti passa in un singolo passaggio.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a17691346649b2ddcde7ca4f3e343be6a35a90
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351751"
---
# <a name="effect-shader-linking"></a>Collegamento Effect shader

Direct2D usa un'ottimizzazione denominata Effect shader linking che combina il rendering del grafico a più effetti passa in un singolo passaggio.

-   [Panoramica del collegamento Effect shader](#overview-of-effect-shader-linking)
-   [Uso del collegamento Effect shader](#using-effect-shader-linking)
-   [Creazione di un effetto personalizzato compatibile con il collegamento dello shader](#authoring-a-shader-linking-compatible-custom-effect)
-   [Esempio di effetto di collegamento compatibile con lo shader](#example-linking-compatible-effect-shader)
-   [Compilazione di un compatibile con il collegamento-shader](#compiling-a-linking-compatible-shader)
    -   [Passaggio 1: compilare la funzione di esportazione](#step-1-compile-the-export-function)
    -   [Passaggio 2: compilare lo shader completo e incorporare la funzione di esportazione](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [Esporta specifiche delle funzioni](#export-function-specifications)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-effect-shader-linking"></a>Panoramica del collegamento Effect shader

Le ottimizzazioni di collegamento di Effect shader si basano sul collegamento a HLSL shader, una funzionalità Direct3D 11,2 che consente la generazione di pixel e vertex shader in fase di esecuzione tramite il collegamento di funzioni shader pre-compilate. Le figure seguenti illustrano il concetto di effetto dello shader sul collegamento in un grafico effetto. La prima figura mostra un grafo di effetto Direct2D tipico con quattro trasformazioni di rendering. Senza il collegamento dello shader, ogni trasformazione utilizza un passaggio di rendering e richiede una superficie intermedia; in totale, questo grafico richiede 4 passaggi e 3 intermedi.



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![trasforma il grafico senza collegamento dello shader: 4 passaggi e 3 intermedi.](images/shader-transform-graph.png) |



 

La seconda figura mostra lo stesso grafico di effetto in cui ogni trasformazione di rendering è stata sostituita con una versione di funzione collegabile. Direct2D è in grado di collegare l'intero grafico ed eseguirlo in un unico passaggio senza richiedere alcun intermedio. Ciò può comportare una riduzione significativa del tempo di esecuzione della GPU e della riduzione del consumo di memoria GPU massimo.



|                                                                                                   |
|---------------------------------------------------------------------------------------------------|
| ![trasforma grafico con collegamento shader: 1 passaggio, 0 intermedi.](images/shader-linking-graph.png) |



 

Il collegamento Effect shader opera sulle singole trasformazioni all'interno di un effetto; Ciò significa che anche un grafo con un singolo effetto può trarre vantaggio dal collegamento dello shader se tale effetto dispone di più trasformazioni valide.

## <a name="using-effect-shader-linking"></a>Uso del collegamento Effect shader

Se si compila un'applicazione Direct2D che usa gli effetti, non è necessario eseguire alcuna operazione per sfruttare il collegamento Effect shader. Direct2D analizza automaticamente il grafico degli effetti per determinare il modo più ottimale per collegare ogni trasformazione.

Gli autori degli effetti sono responsabili dell'implementazione del loro effetto in modo da supportare il collegamento Effect shader; Per ulteriori informazioni, vedere la sezione [creazione di un effetto personalizzato compatibile con il collegamento shader](#authoring-a-shader-linking-compatible-custom-effect) di seguito. Tutti gli effetti predefiniti supportano il collegamento dello shader.

Direct2D collegherà solo le trasformazioni di rendering adiacenti in situazioni in cui è utile. Prende in considerazione diversi fattori quando si determina se collegare due trasformazioni. Ad esempio, il collegamento dello shader non viene eseguito se una delle trasformazioni USA vertex o Compute Shaders, in quanto è possibile collegare solo i pixel shader. Inoltre, se un effetto non è stato creato per essere compatibile con il collegamento dello shader, le trasformazioni circostanti non verranno collegate.

Nel caso in cui esista un rischio di collegamento di questo tipo, Direct2D non collegherà le trasformazioni adiacenti al rischio, ma tenterà comunque di collegare il resto del grafo.



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![trasforma il grafico con un rischio di collegamento: 2 passaggi, 1 intermedio.](images/shader-linking-graph-hazard.png) |



 

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>Creazione di un effetto personalizzato compatibile con il collegamento dello shader

Se si crea un effetto Direct2D personalizzato, è necessario assicurarsi che le trasformazioni supportino il collegamento Effect shader. Questa operazione richiede alcune modifiche minime rispetto al modo in cui sono stati implementati gli effetti personalizzati precedenti. Se una trasformazione all'interno dell'effetto personalizzato non supporta il collegamento dello shader, Direct2D non lo collegherà con le trasformazioni adiacenti al grafico di effetto.

Come autore dell'effetto personalizzato, è necessario conoscere diversi concetti chiave e requisiti:

-   **Nessuna modifica alle implementazioni dell'interfaccia di effetto**

    Non è necessario modificare il codice che implementa le varie interfacce di effetto, ad esempio [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).

-   **Fornire una versione completa ed Esporta della funzione shader**

    È necessario fornire una versione della funzione Export degli shader dell'effetto che possono essere collegati da Direct2D. Inoltre, è necessario continuare a fornire lo shader originale completo; Questo perché Direct2D seleziona in fase di esecuzione la versione shader corretta, a seconda che il collegamento dello shader venga applicato a un particolare collegamento nel grafico.

    Se una trasformazione fornisce solo il BLOB pixel shader completo (tramite [ID2D1EffectContext:: LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), non verrà collegato a trasformazioni adiacenti.

- **Funzioni helper**

    Direct2D fornisce le funzioni e le macro [Helper HLSL](hlsl-helpers.md) che generano automaticamente le versioni della funzione complete ed export di uno shader. Questi helper si trovano in d2d1effecthelpers. hlsli. Inoltre, il compilatore HLSL (FXC) consente di inserire la funzione di esportazione shader in un campo privato dello shader completo. In questo modo, è sufficiente creare uno shader una sola volta e passare contemporaneamente entrambe le versioni a Direct2D. D2d1effecthelpers. hlsli e il compilatore FXC sono inclusi come parte del Windows SDK.

    Funzioni helper:

  - [D2DGetInput](d2dgetinput.md)  
  - [D2DSampleInput](d2dsampleinput.md)  
  - [D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
  - [D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
  - [D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
  - [D2DGetScenePosition](d2dgetsceneposition.md)  
  - [\_Voce D2D PS \_](d2d-ps-entry.md)  

  È anche possibile creare manualmente due versioni di ogni shader e compilarle due volte, purché vengano soddisfatte le specifiche descritte di seguito nelle [specifiche delle funzioni di esportazione](#export-function-specifications) .

-   **Solo pixel shader**

    Direct2D non supporta il collegamento di COMPUTE o vertex shader. Tuttavia, se l'effetto USA sia un vertice che un pixel shader, l'output del pixel shader può ancora essere collegato.

-   **Campionamento semplice e complesso**

    Il collegamento della funzione shader funziona connettendo l'output di uno pixel shader passare all'input di un passaggio di pixel shader successivo. Questa operazione è possibile solo quando il pixel shader di consumo richiede solo un singolo valore di input per eseguire il calcolo. Questo valore, in genere, proviene dal campionamento di una trama di input in corrispondenza della coordinata di trama emessa dal vertex shader. Questo pixel shader si afferma di eseguire un campionamento semplice.

    

    |                                                                                                                                                                                            |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![la conversione in scala di grigi è un esempio di campionamento semplice. il valore di un determinato pixel di output dipende solo dal valore del pixel di input corrispondente.](images/simple-sampling.png) |

    

     

    Alcuni pixel shader, ad esempio una sfocatura gaussiana, calcolano l'output da più campioni di input piuttosto che solo un singolo campione. Questo pixel shader si afferma di eseguire un campionamento complesso.

    

    |                                                                                                                                                           |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![la sfocatura gaussiana è un esempio di campionamento complesso. il valore del pixel di output centrale dipende da più pixel di input.](images/complex-sampling.png) |

    

     

    Solo le funzioni shader con input semplici possono avere un input fornito da un'altra funzione shader. Le funzioni shader con input complessi devono essere fornite con una trama di input da campionare. Questo significa che Direct2D non collegherà uno shader con input complessi al suo predecessore.

    Quando si usano gli [Helper HLSL Direct2D](hlsl-helpers.md), è necessario indicare in HLSL se uno shader usa input complessi o semplici.

## <a name="example-linking-compatible-effect-shader"></a>Esempio di effetto di collegamento compatibile con lo shader

Utilizzando gli helper D2D, il frammento di codice seguente rappresenta un semplice shader Effect compatibile con collegamento:

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

In questo breve esempio si noti che non vengono dichiarati parametri di funzione, che il numero di input e il tipo di ogni input sono dichiarati prima della funzione entry, che l'input viene recuperato chiamando [D2DGetInput](d2dgetinput.md)e che le direttive per il preprocessore devono essere definite prima che il file helper venga incluso.

Uno shader compatibile con il collegamento deve fornire sia un pixel shader a singolo passaggio normale che una funzione di esportazione dello shader. La macro di [ \_ \_ immissione D2D PS](d2d-ps-entry.md) consente la generazione di ognuno di questi dallo stesso codice, se usato insieme allo script di compilazione dello shader.

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

Quando si compila una versione della funzione Export dello stesso codice, viene generato il codice seguente:

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

Si noti che l'input di trama, generalmente recuperato tramite il campionamento di un Texture2D, è stato sostituito con un input di funzione (input0).

Per una descrizione completa, dettagliata delle operazioni da eseguire per scrivere un effetto compatibile con il collegamento, vedere l' [esercitazione sugli effetti personalizzati](custom-effects.md) e l' [esempio di effetti immagine personalizzati Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

## <a name="compiling-a-linking-compatible-shader"></a>Compilazione di un compatibile con il collegamento-shader

Per poter essere collegato, il BLOB pixel shader passato a D2D deve contenere sia la versione completa che la funzione di esportazione dello shader. Questa operazione viene eseguita incorporando la funzione di esportazione compilata \_ nell' \_ area dati privata del BLOB D3D \_ .

Quando gli shader vengono creati con le funzioni di supporto D2D, è necessario definire una destinazione di compilazione D2D in fase di compilazione. I tipi di destinazione di compilazione sono D2D \_ full \_ shader e D2D \_ funzione.

La compilazione di un effetto shader compatibile con il collegamento è un processo in due passaggi:

-   [Compilare la funzione di esportazione](#step-1-compile-the-export-function)
-   [Compilare lo shader completo e incorporare la funzione di esportazione](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> Quando si compila un effetto usando Visual Studio, è necessario creare un file batch che esegua entrambi i comandi FXC ed eseguire questo file batch come un'istruzione di compilazione personalizzata che viene eseguita prima del passaggio di compilazione.

 

### <a name="step-1-compile-the-export-function"></a>Passaggio 1: compilare la funzione di esportazione

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

Per compilare la versione della funzione di esportazione dello shader, è necessario passare i flag seguenti a FXC.



|                                |                                                                                                                                                                                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Contrassegno**                       | **Descrizione**                                                                                                                                                                                                                                           |
| /T <ShaderModel>         | Impostare sul <ShaderModel> profilo di pixel shader appropriato come definito nella [sintassi FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Deve essere uno dei profili elencati in "HLSL shader linking". |
| <MyShaderFile>.hlsl      | Impostare sul <MyShaderFile> nome del file HLSL.                                                                                                                                                                                                    |
| /D \_ funzione D2D               | Questa definizione indica a FXC di compilare la versione della funzione di esportazione dello shader.                                                                                                                                                                       |
| /D D2D \_ voce =<entry>    | Impostare sul <entry> nome del punto di ingresso HLSL definito all'interno della macro [di \_ \_ immissione D2D PS](d2d-ps-entry.md) .                                                                                                                                    |
| /FL <MyShaderFile> . fxlib | Impostare <MyShaderfile> la posizione in cui si desidera archiviare la versione della funzione di esportazione dello shader. Si noti che l'estensione. fxlib è solo per semplificare l'identificazione.                                                                                              |



 

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>Passaggio 2: compilare lo shader completo e incorporare la funzione di esportazione

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

Per compilare la versione completa dello shader con la versione di esportazione incorporata, è necessario passare i flag seguenti a FXC.



|                                        |                                                                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Contrassegno**                               | **Descrizione**                                                                                                                                                                                                                                                                      |
| /T <ShaderModel>                 | Impostare sul <ShaderModel> profilo di pixel shader appropriato come definito nella [sintassi FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Deve corrispondere al profilo pixel shader corrispondente al profilo di collegamento specificato nel passaggio 1. |
| <MyShaderFile>.hlsl              | Impostare sul <MyShaderFile> nome del file HLSL.                                                                                                                                                                                                                               |
| /D D2D \_ completo dello \_ shader                   | Questa definizione indica a FXC di compilare la versione completa dello shader.                                                                                                                                                                                                             |
| /D D2D \_ voce =<entry>            | Impostare sul <entry> nome del punto di ingresso HLSL definito all'interno della macro D2D \_ PS \_ entry ().                                                                                                                                                                                 |
| /E <entry>                       | Impostare sul <entry> nome del punto di ingresso HLSL definito all'interno della macro D2D \_ PS \_ entry ().                                                                                                                                                                                 |
| /SetPrivate <MyShaderFile> . fxlib | Questo argomento indica a FXC di incorporare la funzione di esportazione shader generata nel passaggio 1 nell' \_ \_ area dati privata del BLOB D3D \_ .                                                                                                                                                          |
| /Fo <MyShader> . cso               | Impostare <MyShader> la posizione in cui si desidera archiviare lo shader compilato combinato finale.                                                                                                                                                                                                 |
| /FH <MyShader> . h                 | Impostare <MyShader> la posizione in cui si desidera archiviare l'intestazione combinata finale.                                                                                                                                                                                                          |



 

## <a name="export-function-specifications"></a>Esporta specifiche delle funzioni

È possibile, sebbene non consigliato, creare uno shader con effetto compatibile senza usare gli helper forniti da D2D. È necessario prestare attenzione per assicurarsi che entrambe le firme di input complete dello shader e della funzione Export siano conformi alle specifiche D2D.

Le specifiche per gli shader completi sono le stesse delle versioni precedenti di Windows. In breve, i parametri di input pixel shader devono essere \_ posizione SV, posizione della scena \_ e un input TEXCOORD per effetto.

Per la funzione Export, la funzione deve restituire un float4 e i relativi input devono essere uno dei tipi seguenti:

-   Input semplice

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    Per gli input semplici, D2D inserisce una funzione di esempio tra la trama di input e la funzione shader oppure l'input viene fornito dall'output di un'altra funzione shader.

-   Input complesso

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    Per gli input complessi, D2D passa una coordinata di trama solo come descritto nella documentazione di Windows 8.

-   Percorso di output

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    \_È possibile definire solo un input di posizione della scena. Questo parametro deve essere incluso solo quando necessario, perché solo una funzione per shader collegato può utilizzare questo parametro.

La semantica deve essere definita come descritto in precedenza, poiché D2D controllerà la semantica per stabilire come collegare le funzioni. Se un input di funzione non corrisponde a uno dei tipi precedenti, la funzione verrà rifiutata per il collegamento dello shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Helper HLSL](hlsl-helpers.md)
</dt> <dt>

[Interfaccia ID3D11Linker](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[Interfaccia ID3D11FunctionLinkingGraph](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 