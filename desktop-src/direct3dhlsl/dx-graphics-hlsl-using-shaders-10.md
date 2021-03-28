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
ms.openlocfilehash: 0e19275532ce8fd034813d8574f6bdc04d72f966
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337535"
---
# <a name="using-shaders-in-direct3d-10"></a>Uso degli shader in Direct3D 10

La pipeline ha tre fasi dello shader e ciascuna è programmata con uno shader HLSL. Tutti gli shader Direct3D 10 sono scritti in HLSL, destinating Shader Model 4.



|                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> A differenza dei modelli di shader Direct3D 9 che potrebbero essere creati in un linguaggio di assembly intermedio, lo Shader Model 4,0 shader viene creato solo in HLSL. Per la maggior parte degli scenari è ancora supportata la compilazione offline di shader in un bytecode utilizzabile dal dispositivo.<br/> |



 

Questo esempio usa solo un vertex shader. Poiché tutti gli shader sono compilati dal core dello shader comune, imparare a usare un vertex shader è molto simile all'uso di una geometria o di un pixel shader.

Dopo aver creato uno shader HLSL (in questo esempio viene usato vertex shader HLSLWithoutFX. VSH), è necessario prepararlo per la fase della pipeline specifica che lo utilizzerà. A tale scopo è necessario:

-   [Compilare uno shader](#compile-a-shader)
-   [Creare un oggetto shader](#create-a-shader-object)
-   [Impostare l'oggetto shader](#set-the-shader-object)
-   [Ripeti per tutte e tre le fasi dello shader](#repeat-for-all-3-shader-stages)

Questi passaggi devono essere ripetuti per ogni shader nella pipeline.

## <a name="compile-a-shader"></a>Compilare uno shader

Il primo passaggio consiste nel compilare lo shader per verificare che siano state codificate correttamente le istruzioni HLSL. Questa operazione viene eseguita chiamando D3D10CompileShader e fornendo diversi parametri, come illustrato di seguito:


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



Questa funzione accetta i parametri seguenti:

-   Il nome del file (e la lunghezza della stringa del nome in byte) che contiene lo shader. Questo esempio usa solo un vertex shader (nel file HLSLWithoutFX. VSH in cui l'estensione di file. VSH è un'abbreviazione per vertex shader).
-   Nome della funzione shader. Questo esempio compila un vertex shader dalla funzione Ripple che accetta un singolo input e restituisce uno struct di output (la funzione è dell'esempio HLSLWithoutFX):
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   Puntatore a tutte le macro utilizzate dallo shader. Usare la \_ macro dello shader D3D10 \_ per definire le macro. è sufficiente creare una stringa del nome che contenga tutti i nomi di macro (con ogni nome separato da uno spazio) e una stringa di definizione (con ogni corpo della macro separato da uno spazio). Entrambe le stringhe devono essere con terminazione NULL.
-   Puntatore a qualsiasi altro file necessario incluso per la compilazione degli shader. Viene utilizzata l'interfaccia ID3D10Include che dispone di due metodi implementati dall'utente: Open e Close. Per eseguire questa operazione, sarà necessario implementare il corpo dei metodi Open e Close; nel metodo Open aggiungere il codice da usare per aprire i file di inclusione desiderati, nella funzione close aggiungere il codice per chiudere i file al termine dell'operazione.
-   Nome della funzione shader da compilare. Questo shader compila la funzione Ripple.
-   Profilo dello shader di destinazione durante la compilazione. Poiché è possibile compilare una funzione in un vertice, una geometria o una pixel shader, il profilo indica al compilatore il tipo di shader e il modello di shader con cui confrontare il codice.
-   Flag del compilatore shader. Questi flag indicano al compilatore quali informazioni inserire nell'output compilato e come si desidera ottimizzare il codice di output: per la velocità, per il debug e così via. Per un elenco dei flag disponibili, vedere [costanti degli effetti (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) . L'esempio contiene il codice che è possibile usare per impostare i valori dei flag del compilatore per il progetto. si tratta principalmente di una questione se si desidera o meno generare informazioni di debug.
-   Puntatore al buffer che contiene il codice dello shader compilato. Il buffer contiene anche le informazioni di debug e tabella di simboli incorporate richieste dai flag del compilatore.
-   Puntatore a un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione, che sono gli stessi messaggi visualizzati nell'output di debug se il debugger era in esecuzione durante la compilazione dello shader. **Null** è un valore accettabile se non si desidera che gli errori vengano restituiti a un buffer.

Se lo shader viene compilato correttamente, un puntatore al codice dello shader viene restituito come interfaccia ID3D10Blob. Viene chiamato interfaccia BLOB perché il puntatore si trova in una posizione in memoria costituita da una matrice di DWORD. L'interfaccia viene fornita in modo che sia possibile ottenere un puntatore allo shader compilato, che sarà necessario nel passaggio successivo.

A partire da dicembre 2006 SDK, il compilatore DirectX 10 HLSL è ora il compilatore predefinito sia in DirectX 9 che in DirectX 10. Per informazioni dettagliate, vedere [strumento del compilatore di effetti](/windows/desktop/direct3dtools/fxc) .

### <a name="get-a-pointer-to-a-compiled-shader"></a>Ottenere un puntatore a uno shader compilato

Diversi metodi API richiedono un puntatore a uno shader compilato. Questo argomento viene in genere chiamato *pShaderBytecode* perché punta a uno shader compilato rappresentato come sequenza di codici di byte. Per ottenere un puntatore a uno shader compilato, compilare innanzitutto lo shader chiamando [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) o una funzione simile. Se la compilazione ha esito positivo, lo shader compilato viene restituito in un'interfaccia [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) . Infine, usare il metodo [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) per restituire il puntatore.

## <a name="create-a-shader-object"></a>Creare un oggetto shader

Una volta compilato lo shader, chiamare CreateVertexShader per creare l'oggetto shader:


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



Per creare l'oggetto shader, passare il puntatore allo shader compilato in CreateVertexShader. Poiché è stato necessario compilare innanzitutto lo shader, questa chiamata verrà superata, a meno che non si sia verificato un problema di memoria nel computer.

È possibile creare tutti gli oggetti shader desiderati e mantenerne semplicemente i puntatori. Lo stesso meccanismo funziona per la geometria e i pixel shader presupponendo che i profili dello shader (quando si chiama il metodo Compile) corrispondano ai nomi delle interfacce (quando si chiama il metodo Create).

## <a name="set-the-shader-object"></a>Impostare l'oggetto shader

L'ultimo passaggio consiste nell'impostare lo shader sulla fase della pipeline. Poiché nella pipeline sono presenti tre fasi dello shader, sarà necessario effettuare tre chiamate API, una per ogni fase.


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



La chiamata a VSSetShader accetta il puntatore al vertex shader creato nel passaggio 1. Questo consente di impostare lo shader nel dispositivo. La fase vertex shader viene ora inizializzata con il relativo codice vertex shader, che rimane l'inizializzazione di eventuali variabili shader.

## <a name="repeat-for-all-3-shader-stages"></a>Ripeti per tutte e tre le fasi dello shader

Ripetere lo stesso set di passaggi per compilare qualsiasi vertice o pixel shader o anche un geometry shader che restituisce il pixel shader.

## <a name="related-topics"></a>Argomenti correlati

[Compilazione di shader](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

