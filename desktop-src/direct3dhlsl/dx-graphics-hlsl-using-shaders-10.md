---
title: Uso degli shader in Direct3D 10
description: Uso degli shader in Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0d6212851e4603aac4db7ec85dd20714dc87774
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826289"
---
# <a name="using-shaders-in-direct3d-10"></a>Uso degli shader in Direct3D 10

La pipeline ha tre fasi di shader e ognuna è programmata con uno shader HLSL. Tutti gli shader Direct3D 10 vengono scritti in HLSL e hanno come destinazione il modello shader 4.


Differenze tra Direct3D 9 e Direct3D 10:

- A differenza dei modelli di shader Direct3D 9 che possono essere creati in un linguaggio assembly intermedio, gli shader del modello shader 4.0 vengono creati solo in HLSL. La compilazione offline degli shader nel bytecode utilizzabile dal dispositivo è ancora supportata e consigliata per la maggior parte degli scenari.



 

Questo esempio usa solo un vertex shader. Poiché tutti gli shader sono compilati dalla base comune dello shader, imparare a usare un vertex shader è molto simile all'uso di una geometria o di pixel shader.

Dopo aver creato uno shader HLSL (questo esempio usa il vertex shader HLSLWithoutFX.vsh), è necessario prepararlo per la fase della pipeline specifica che lo userà. A tale scopo, è necessario:

-   [Compilare uno shader](#compile-a-shader)
-   [Creare un oggetto shader](#create-a-shader-object)
-   [Impostare l'oggetto shader](#set-the-shader-object)
-   [Ripeti per tutte e 3 le fasi dello shader](#repeat-for-all-3-shader-stages)

Questi passaggi devono essere ripetuti per ogni shader nella pipeline.

## <a name="compile-a-shader"></a>Compilare uno shader

Il primo passaggio consiste nel compilare lo shader per verificare che le istruzioni HLSL siano state codificate correttamente. Questa operazione viene eseguita chiamando D3D10CompileShader e fornendo diversi parametri, come illustrato di seguito:


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



Questa funzione accetta i parametri seguenti:

-   Nome del file ( e lunghezza della stringa del nome in byte) che contiene lo shader. Questo esempio usa solo un vertex shader (nel file HLSLWithoutFX.vsh in cui l'estensione vsh è un'abbreviazione per vertex shader).
-   Nome della funzione shader. Questo esempio compila un vertex shader dalla funzione Ripple che accetta un singolo input e restituisce uno struct di output (la funzione è dell'esempio HLSLWithoutFX):
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   Puntatore a tutte le macro usate dallo shader. Usare D3D10 SHADER MACRO per definire le macro. È sufficiente creare una stringa del nome contenente tutti i nomi delle macro (con ogni nome separato da uno spazio) e una stringa di definizione (con ogni corpo della macro separato da uno \_ \_ spazio). Entrambe le stringhe devono terminare con NULL.
-   Puntatore a qualsiasi altro file che è necessario includere per compilare gli shader. Viene utilizzata l'interfaccia ID3D10Include che dispone di due metodi implementati dall'utente: Open e Close. Per eseguire questa operazione, è necessario implementare il corpo dei metodi Open e Close. nel metodo Open aggiungere il codice da usare per aprire i file di inclusione desiderati. Al termine, nella funzione Close aggiungere il codice per chiudere i file.
-   Nome della funzione shader da compilare. Questo shader compila la funzione Ripple.
-   Profilo shader di destinazione durante la compilazione. Poiché è possibile compilare una funzione in un vertice, una geometria o un pixel shader, il profilo indica al compilatore il tipo di shader e il modello di shader con cui confrontare il codice.
-   Flag del compilatore shader. Questi flag segnalano al compilatore quali informazioni inserire nell'output compilato e come si vuole ottimizzare il codice di output: per la velocità, per il debug e così via. Per un elenco dei flag disponibili, vedere Costanti effetto [(Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) L'esempio contiene codice che è possibile usare per impostare i valori dei flag del compilatore per il progetto. Si tratta principalmente di stabilire se si vogliono generare o meno informazioni di debug.
-   Puntatore al buffer che contiene il codice dello shader compilato. Il buffer contiene anche le informazioni incorporate sulle tabelle di debug e simboli richieste dai flag del compilatore.
-   Puntatore a un buffer che contiene un elenco di errori e avvisi rilevati durante la compilazione, che sono gli stessi messaggi visualizzati nell'output di debug se si esegue il debugger durante la compilazione dello shader. **NULL** è un valore accettabile quando non si vuole che gli errori siano restituiti a un buffer.

Se lo shader viene compilato correttamente, viene restituito un puntatore al codice dello shader come interfaccia ID3D10Blob. Viene chiamata interfaccia BLOB perché il puntatore è a una posizione in memoria che è costituito da una matrice di DWORD. L'interfaccia viene fornita in modo che sia possibile ottenere un puntatore allo shader compilato che sarà necessario nel passaggio successivo.

A partire dall'SDK di dicembre 2006, il compilatore HLSL di DirectX 10 è ora il compilatore predefinito sia in DirectX 9 che in DirectX 10. Per [informazioni dettagliate, vedere Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) .

### <a name="get-a-pointer-to-a-compiled-shader"></a>Ottenere un puntatore a uno shader compilato

Diversi metodi API richiedono un puntatore a uno shader compilato. Questo argomento è in genere denominato *pShaderBytecode* perché punta a uno shader compilato rappresentato come sequenza di codici byte. Per ottenere un puntatore a uno shader compilato, compilare prima lo shader chiamando [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) o una funzione simile. Se la compilazione ha esito positivo, lo shader compilato viene restituito in [**un'interfaccia ID3D10Blob.**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) Usare infine il [**metodo GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) per restituire il puntatore.

## <a name="create-a-shader-object"></a>Creare un oggetto shader

Dopo aver compilato lo shader, chiamare CreateVertexShader per creare l'oggetto shader:


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



Per creare l'oggetto shader, passare il puntatore allo shader compilato in CreateVertexShader. Poiché è stato necessario prima compilare correttamente lo shader, questa chiamata passerà quasi certamente, a meno che non si sia verificato un problema di memoria nel computer.

È possibile creare tutti gli oggetti shader che si desidera e mantenere semplicemente i puntatori a essi. Questo stesso meccanismo funziona per geometry e pixel shader presupponendo che i profili shader (quando si chiama il metodo di compilazione) corrispondano ai nomi di interfaccia (quando si chiama il metodo create).

## <a name="set-the-shader-object"></a>Impostare l'oggetto shader

L'ultimo passaggio consiste nell'impostare lo shader sulla fase della pipeline. Poiché la pipeline ha tre fasi di shader, sarà necessario effettuare tre chiamate API, una per ogni fase.


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



La chiamata a VSSetShader accetta il puntatore al vertex shader creato nel passaggio 1. In questo modo viene impostato lo shader nel dispositivo. La fase vertex shader viene ora inizializzata con il relativo codice vertex shader, tutto ciò che rimane è l'inizializzazione di tutte le variabili di shader.

## <a name="repeat-for-all-3-shader-stages"></a>Ripeti per tutte e 3 le fasi dello shader

Ripetere lo stesso set di passaggi per compilare qualsiasi vertice o pixel shader o anche un geometry shader che restituisce l'output al pixel shader.

## <a name="related-topics"></a>Argomenti correlati

[Compilazione di shader](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

