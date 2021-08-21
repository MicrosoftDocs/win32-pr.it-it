---
title: Uso di shader in Direct3D 9
description: Uso di shader in Direct3D 9
ms.assetid: 8d8f5124-fbf3-4af5-8399-43ba28aa6eb9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1ef04c14682aa6e763222fd0c8db0e2eedf33abf747da97a16b2b1621e1c42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119745"
---
# <a name="using-shaders-in-direct3d-9"></a>Uso di shader in Direct3D 9

-   [Compilazione di uno shader per hardware specifico](#compiling-a-shader-for-specific-hardware)
-   [Inizializzazione delle costanti shader](#initializing-shader-constants)
-   [Associazione di un parametro shader a un registro specifico](#binding-a-shader-parameter-to-a-particular-register)
-   [Rendering di uno shader programmabile](#rendering-a-programmable-shader)
-   [Debug di shader](#debugging-shaders)
-   [Argomenti correlati](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a>Compilazione di uno shader per hardware specifico

Gli shader sono stati aggiunti per la prima volta a Microsoft DirectX in DirectX 8.0. A quel tempo, sono state definite diverse macchine shader virtuali, ognuna corrispondente approssimativamente a un particolare processore grafico prodotto dai principali fornitori di grafica 3D. Per ognuna di queste macchine shader virtuali, è stato progettato un linguaggio di assembly. I programmi scritti nei modelli shader (nomi vs \_ \_ 1 1 e ps \_ \_ 1 1 - ps \_ 1 \_ 4) erano relativamente brevi e in genere sono stati scritti dagli sviluppatori direttamente nel linguaggio di assembly appropriato. L'applicazione passa questo codice in linguaggio assembly leggibile dall'utente alla libreria D3DX usando [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) e ottiene una rappresentazione binaria dello shader che a sua volta verrebbe passata usando [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) [**o CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader). Per altre informazioni, vedere software development kit (SDK).

La situazione in Direct3D 9 è simile. Un'applicazione passa uno shader HLSL a D3DX usando [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) e ottiene una rappresentazione binaria dello shader compilato che a sua volta viene passato a Microsoft Direct3D usando [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) [**o CreateVertexShader.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) Il runtime non sa nulla di HLSL, ma solo dei modelli shader di assembly binari. Questo è un'operazione buona perché significa che il compilatore HLSL può essere aggiornato indipendentemente dal runtime Direct3D. È anche possibile compilare shader offline usando [fxc](/windows/desktop/direct3dtools/fxc).

Oltre allo sviluppo del compilatore HLSL, Direct3D 9 ha introdotto anche i modelli shader a livello di assembly per esporre le funzionalità dell'hardware grafico di ultima generazione. Gli sviluppatori di applicazioni possono lavorare in assembly per questi nuovi modelli (vs \_ 2 \_ 0, vs \_ 3 \_ 0, ps \_ 2 \_ 0, ps \_ 3 0), \_ ma ci si aspetta che la maggior parte degli sviluppatori si sposti in HLSL per lo sviluppo di shader.

Naturalmente, la possibilità di scrivere un programma HLSL per esprimere un particolare algoritmo di ombreggiatura non ne consente automaticamente l'esecuzione in un determinato hardware. Un'applicazione chiama D3DX per compilare uno shader in codice assembly binario [**con D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader). Una delle limitazioni di questo punto di ingresso è un parametro che definisce quale dei modelli a livello di assembly (o destinazioni di compilazione) il compilatore HLSL deve usare per esprimere il codice shader finale. Se un'applicazione esegue la compilazione dello shader HLSL in fase di esecuzione (anziché in fase di compilazione o offline), l'applicazione potrebbe esaminare le funzionalità del dispositivo Direct3D e selezionare la destinazione di compilazione per la corrispondenza. Se l'algoritmo espresso nello shader HLSL è troppo complesso per essere eseguito nella destinazione di compilazione selezionata, la compilazione avrà esito negativo. Ciò significa che, sebbene HLSL sia un vantaggio enorme per lo sviluppo di shader, non libera gli sviluppatori dalla realtà della spedizione di giochi a un pubblico di destinazione con dispositivi grafici di diverse funzionalità. Gli sviluppatori di giochi devono comunque gestire un approccio a livelli agli oggetti visivi. ciò significa scrivere shader migliori per schede grafiche più idonee e scrivere versioni più semplici per le schede meno recenti. Con HLSL ben scritto, tuttavia, questo carico di lavoro può essere notevolmente attenuato.

Invece di compilare shader HLSL usando D3DX nel computer del cliente in fase di caricamento dell'applicazione o al primo utilizzo, molti sviluppatori scelgono di compilare lo shader da HLSL al codice di assembly binario prima ancora di essere forniti. In questo modo il codice sorgente HLSL viene rimosso dagli occhi indiscreti e si assicura anche che tutti gli shader che verranno eseguiti dall'applicazione siano stati eseguiti nel processo interno di controllo della qualità. Una pratica utilità per la compilazione di shader offline è [fxc](/windows/desktop/direct3dtools/fxc). Questo strumento include diverse opzioni che è possibile usare per compilare il codice per la destinazione di compilazione specificata. Lo studio dell'output disassemblato può essere molto didattico durante lo sviluppo se si vogliono ottimizzare gli shader o semplicemente conoscere le funzionalità della macchina shader virtuale a un livello più dettagliato. Queste opzioni sono riepilogate di seguito:

## <a name="initializing-shader-constants"></a>Inizializzazione delle costanti shader

Le costanti shader sono contenute nella tabella delle costanti. È possibile accedervi con [**l'interfaccia ID3DXConstantTable.**](/windows/desktop/direct3d9/id3dxconstanttable) Le variabili shader globali possono essere inizializzate nel codice shader. Questi vengono inizializzati in fase di esecuzione chiamando [**SetDefaults**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults).

## <a name="binding-a-shader-parameter-to-a-particular-register"></a>Associazione di un parametro shader a un registro specifico

Il compilatore assegna automaticamente i registri alle variabili globali. Il compilatore assegnerebbe Environment al registro sampler s0, SparkleNoise al registro sampler s1 e k s al registro costante c0 (presupponendo che non siano già stati assegnati altri registri sampler o costanti) per le tre variabili globali \_ seguenti:


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



È anche possibile associare variabili a un registro specifico. Per forzare l'assegnazione del compilatore a un registro specifico, usare la sintassi seguente:


```
register(RegisterName)
```



dove RegisterName è il nome del registro specifico. Gli esempi seguenti illustrano la sintassi di assegnazione del registro specifica, in cui l'ambiente sampler verrà associato al registro sampler s1, SparkleNoise verrà associato al registro sampler s0 e k s verrà associato al registro \_ costante c12:


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a>Rendering di uno shader programmabile

Il rendering di uno shader viene eseguito impostando lo shader corrente nel dispositivo, inizializzando le costanti dello shader, indicando al dispositivo da dove arrivano i vari dati di input e infine visualizzando le primitive. Ognuna di queste operazioni può essere eseguita chiamando rispettivamente i metodi seguenti:

-   [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [**SetStreamSource**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [**DrawPrimitive**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a>Debug di shader

L'estensione DirectX per Microsoft Visual Studio .NET offre un debugger HLSL completamente integrato all'interno dell Visual Studio IDE (Integrated Development Environment) di .NET. Per preparare il debug dello shader, è necessario installare gli strumenti necessari nel computer (vedere [Debugging Shaders in Visual Studio (Direct3D 9)](dx-graphics-hlsl-debug-visual-studio.md)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 