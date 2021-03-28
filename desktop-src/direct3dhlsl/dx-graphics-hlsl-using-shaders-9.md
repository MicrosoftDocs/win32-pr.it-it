---
title: Uso degli shader in Direct3D 9
description: Uso degli shader in Direct3D 9
ms.assetid: 8d8f5124-fbf3-4af5-8399-43ba28aa6eb9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6455b47d24c1c83683ce8b85c48990bb32e221ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993360"
---
# <a name="using-shaders-in-direct3d-9"></a>Uso degli shader in Direct3D 9

-   [Compilazione di uno shader per hardware specifico](#compiling-a-shader-for-specific-hardware)
-   [Inizializzazione di costanti shader](#initializing-shader-constants)
-   [Associazione di un parametro dello shader a un particolare registro](#binding-a-shader-parameter-to-a-particular-register)
-   [Rendering di uno shader programmabile](#rendering-a-programmable-shader)
-   [Debug di shader](#debugging-shaders)
-   [Argomenti correlati](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a>Compilazione di uno shader per hardware specifico

Gli shader sono stati aggiunti per la prima volta a Microsoft DirectX in DirectX 8,0. A questo punto, sono stati definiti diversi computer di shader virtuali, ognuno approssimativamente corrispondente a un particolare processore grafico prodotto dai principali fornitori di grafica 3D. Per ognuna di queste macchine virtuali shader è stato progettato un linguaggio assembly. I programmi scritti nei modelli shader (nomi rispetto a \_ 1 \_ 1 e PS \_ 1 \_ -PS \_ 1 \_ 4) erano relativamente brevi e sono stati scritti in genere dagli sviluppatori direttamente nel linguaggio assembly appropriato. L'applicazione passa il codice della lingua assembly leggibile alla libreria D3DX usando [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) e ottiene una rappresentazione binaria dello shader che a sua volta viene passata usando [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) o [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader). Per informazioni dettagliate, vedere la Software Development Kit (SDK).

La situazione in Direct3D 9 è simile. Un'applicazione passa uno shader HLSL a D3DX usando [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) e restituisce una rappresentazione binaria dello shader compilato che a sua volta viene passato a Microsoft Direct3D usando [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) o [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader). Il runtime non è in grado di conoscere HLSL, bensì solo i modelli di shader dell'assembly binario. Si tratta di un'operazione interessante perché significa che il compilatore HLSL può essere aggiornato indipendentemente dal runtime Direct3D. È anche possibile compilare shader offline usando [FXC](/windows/desktop/direct3dtools/fxc).

Oltre allo sviluppo del compilatore HLSL, in Direct3D 9 sono stati introdotti anche i modelli shader a livello di assembly per esporre la funzionalità dell'ultima generazione di hardware grafico. Gli sviluppatori di applicazioni possono lavorare nell'assembly per questi nuovi modelli (vs \_ 2 \_ 0, vs \_ 3 \_ 0, PS \_ 2 \_ 0, PS \_ 3 \_ 0), ma si prevede che la maggior parte degli sviluppatori passi a HLSL per lo sviluppo dello shader.

Naturalmente, la possibilità di scrivere un programma HLSL per esprimere un particolare algoritmo di ombreggiatura non lo abilita automaticamente per l'esecuzione in qualsiasi hardware specifico. Un'applicazione chiama D3DX per compilare uno shader in codice assembly binario con [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader). Una delle limitazioni di questo punto di ingresso è un parametro che definisce quali modelli a livello di assembly (o destinazioni di compilazione) il compilatore HLSL deve usare per esprimere il codice shader finale. Se un'applicazione sta eseguendo la compilazione dello shader HLSL in fase di esecuzione (anziché in fase di compilazione o non in linea), l'applicazione potrebbe esaminare le funzionalità del dispositivo Direct3D e selezionare la destinazione di compilazione di cui trovare la corrispondenza. Se l'algoritmo espresso in HLSL shader è troppo complesso per essere eseguito sulla destinazione di compilazione selezionata, la compilazione avrà esito negativo. Ciò significa che, anche se HLSL è un enorme vantaggio per lo sviluppo di shader, non libera gli sviluppatori dalla realtà dei giochi di spedizione a destinatari con dispositivi grafici di diverse funzionalità. Gli sviluppatori di giochi devono comunque gestire un approccio a più livelli per gli oggetti visivi. Ciò significa scrivere migliori shader per schede grafiche più idonee e scrivere più versioni di base per le schede meno recenti. Con HLSL ben scritti, tuttavia, questo fardello può essere notevolmente ridotto.

Invece di compilare shader HLSL usando D3DX sul computer del cliente al momento del caricamento dell'applicazione o al primo utilizzo, molti sviluppatori scelgono di compilare il proprio shader da HLSL a codice assembly binario prima di distribuirli. In questo modo, il codice sorgente di HLSL si allontana da sguardi indiscreti e garantisce inoltre che tutti gli shader che la loro applicazione eseguiranno sono passati attraverso il processo interno di controllo della qualità. Una comoda utilità per la compilazione offline degli shader è [FXC](/windows/desktop/direct3dtools/fxc). Questo strumento dispone di numerose opzioni che è possibile utilizzare per compilare il codice per la destinazione di compilazione specificata. Lo studio dell'output disassemblato può essere molto istruttivo durante lo sviluppo se si desidera ottimizzare gli shader o solo in genere ottenere informazioni sulle funzionalità del computer Virtual shader a un livello più dettagliato. Queste opzioni sono riepilogate di seguito:

## <a name="initializing-shader-constants"></a>Inizializzazione di costanti shader

Le costanti shader sono contenute nella tabella Constant. È possibile accedere a questa operazione con l'interfaccia [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) . Le variabili dello shader globale possono essere inizializzate nel codice dello shader. Questi vengono inizializzati in fase di esecuzione chiamando i [**valori predefiniti**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults).

## <a name="binding-a-shader-parameter-to-a-particular-register"></a>Associazione di un parametro dello shader a un particolare registro

Il compilatore assegna automaticamente i registri alle variabili globali. Il compilatore assegna l'ambiente al campionatore del campionatore S0, SparkleNoise al campionatore Register S1 e k \_ s al registro costante C0 (presupponendo che non siano stati già assegnati altri registri di campionatori o costanti) per le tre variabili globali seguenti:


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



È anche possibile associare le variabili a un registro specifico. Per forzare l'assegnazione del compilatore a un particolare registro, usare la sintassi seguente:


```
register(RegisterName)
```



dove RegisterName è il nome del registro specifico. Negli esempi seguenti viene illustrata la sintassi di assegnazione del registro specifica, in cui l'ambiente campionatore verrà associato al registro campionatore S1, SparkleNoise verrà associato al registro campionatore S0 e k \_ s verrà associato a constant register C12:


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a>Rendering di uno shader programmabile

Viene eseguito il rendering di uno shader impostando lo shader corrente nel dispositivo, inizializzando le costanti dello shader, indicando il dispositivo da cui provengono i dati di input variabili e infine eseguendo il rendering delle primitive. Ognuna di queste operazioni può essere eseguita chiamando rispettivamente i metodi seguenti:

-   [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [**SetStreamSource**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [**DrawPrimitive**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a>Debug di shader

L'estensione DirectX per Microsoft Visual Studio .NET fornisce un debugger HLSL completamente integrato all'interno dell'ambiente di sviluppo integrato (IDE) di Visual Studio .NET. Per preparare il debug dello shader, è necessario installare gli strumenti corretti nel computer. vedere [debug di shader in Visual Studio (Direct3D 9)](dx-graphics-hlsl-debug-visual-studio.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 