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
# <a name="using-shaders-in-direct3d-10"></a><span data-ttu-id="77e4b-103">Uso degli shader in Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="77e4b-103">Using Shaders in Direct3D 10</span></span>

<span data-ttu-id="77e4b-104">La pipeline ha tre fasi dello shader e ciascuna è programmata con uno shader HLSL.</span><span class="sxs-lookup"><span data-stu-id="77e4b-104">The pipeline has three shader stages and each one is programmed with an HLSL shader.</span></span> <span data-ttu-id="77e4b-105">Tutti gli shader Direct3D 10 sono scritti in HLSL, destinating Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="77e4b-105">All Direct3D 10 shaders are written in HLSL, targeting shader model 4.</span></span>



|                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e4b-106">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="77e4b-106">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="77e4b-107">A differenza dei modelli di shader Direct3D 9 che potrebbero essere creati in un linguaggio di assembly intermedio, lo Shader Model 4,0 shader viene creato solo in HLSL.</span><span class="sxs-lookup"><span data-stu-id="77e4b-107">Unlike Direct3D 9 shader models which could be authored in an intermediate assembly language, shader model 4.0 shaders are only authored in HLSL.</span></span> <span data-ttu-id="77e4b-108">Per la maggior parte degli scenari è ancora supportata la compilazione offline di shader in un bytecode utilizzabile dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77e4b-108">Offline compilation of shaders into device-consumable bytecode is still supported, and recommended for most scenarios.</span></span><br/> |



 

<span data-ttu-id="77e4b-109">Questo esempio usa solo un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-109">This example uses only a vertex shader.</span></span> <span data-ttu-id="77e4b-110">Poiché tutti gli shader sono compilati dal core dello shader comune, imparare a usare un vertex shader è molto simile all'uso di una geometria o di un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-110">Because all shaders are built from the common shader core, learning how to use a vertex shader is very similar to using a geometry or pixel shader.</span></span>

<span data-ttu-id="77e4b-111">Dopo aver creato uno shader HLSL (in questo esempio viene usato vertex shader HLSLWithoutFX. VSH), è necessario prepararlo per la fase della pipeline specifica che lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="77e4b-111">Once you have authored an HLSL shader (this example uses the vertex shader HLSLWithoutFX.vsh), you will need to prepare it for the particular pipeline stage that will use it.</span></span> <span data-ttu-id="77e4b-112">A tale scopo è necessario:</span><span class="sxs-lookup"><span data-stu-id="77e4b-112">To do this you need to:</span></span>

-   [<span data-ttu-id="77e4b-113">Compilare uno shader</span><span class="sxs-lookup"><span data-stu-id="77e4b-113">Compile a Shader</span></span>](#compile-a-shader)
-   [<span data-ttu-id="77e4b-114">Creare un oggetto shader</span><span class="sxs-lookup"><span data-stu-id="77e4b-114">Create a Shader Object</span></span>](#create-a-shader-object)
-   [<span data-ttu-id="77e4b-115">Impostare l'oggetto shader</span><span class="sxs-lookup"><span data-stu-id="77e4b-115">Set the Shader Object</span></span>](#set-the-shader-object)
-   [<span data-ttu-id="77e4b-116">Ripeti per tutte e tre le fasi dello shader</span><span class="sxs-lookup"><span data-stu-id="77e4b-116">Repeat for all 3 Shader Stages</span></span>](#repeat-for-all-3-shader-stages)

<span data-ttu-id="77e4b-117">Questi passaggi devono essere ripetuti per ogni shader nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="77e4b-117">These steps need to be repeated for each shader in the pipeline.</span></span>

## <a name="compile-a-shader"></a><span data-ttu-id="77e4b-118">Compilare uno shader</span><span class="sxs-lookup"><span data-stu-id="77e4b-118">Compile a Shader</span></span>

<span data-ttu-id="77e4b-119">Il primo passaggio consiste nel compilare lo shader per verificare che siano state codificate correttamente le istruzioni HLSL.</span><span class="sxs-lookup"><span data-stu-id="77e4b-119">The first step is to compile the shader, to check to see that you have coded the HLSL statements correctly.</span></span> <span data-ttu-id="77e4b-120">Questa operazione viene eseguita chiamando D3D10CompileShader e fornendo diversi parametri, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="77e4b-120">This is done by calling D3D10CompileShader and supplying it with several parameters as shown here:</span></span>


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



<span data-ttu-id="77e4b-121">Questa funzione accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="77e4b-121">This function takes the following parameters:</span></span>

-   <span data-ttu-id="77e4b-122">Il nome del file (e la lunghezza della stringa del nome in byte) che contiene lo shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-122">The name of the file ( and length of the name string in bytes ) that contains the shader.</span></span> <span data-ttu-id="77e4b-123">Questo esempio usa solo un vertex shader (nel file HLSLWithoutFX. VSH in cui l'estensione di file. VSH è un'abbreviazione per vertex shader).</span><span class="sxs-lookup"><span data-stu-id="77e4b-123">This example uses a vertex shader only (in the file HLSLWithoutFX.vsh file where the file extension .vsh is an abbreviation for vertex shader).</span></span>
-   <span data-ttu-id="77e4b-124">Nome della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-124">The shader function name.</span></span> <span data-ttu-id="77e4b-125">Questo esempio compila un vertex shader dalla funzione Ripple che accetta un singolo input e restituisce uno struct di output (la funzione è dell'esempio HLSLWithoutFX):</span><span class="sxs-lookup"><span data-stu-id="77e4b-125">This example compiles a vertex shader from the Ripple function which takes a single input and returns an output struct (the function is from the HLSLWithoutFX sample):</span></span>
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   <span data-ttu-id="77e4b-126">Puntatore a tutte le macro utilizzate dallo shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-126">A pointer to all macros used by the shader.</span></span> <span data-ttu-id="77e4b-127">Usare la \_ macro dello shader D3D10 \_ per definire le macro. è sufficiente creare una stringa del nome che contenga tutti i nomi di macro (con ogni nome separato da uno spazio) e una stringa di definizione (con ogni corpo della macro separato da uno spazio).</span><span class="sxs-lookup"><span data-stu-id="77e4b-127">Use D3D10\_SHADER\_MACRO to help define your macros; simply create a name string that contains all the macro names (with each name separated by a space) and a definition string (with each macro body separated by a space).</span></span> <span data-ttu-id="77e4b-128">Entrambe le stringhe devono essere con terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="77e4b-128">Both strings need to be NULL terminated.</span></span>
-   <span data-ttu-id="77e4b-129">Puntatore a qualsiasi altro file necessario incluso per la compilazione degli shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-129">A pointer to any other files that you need included to get your shaders to compile.</span></span> <span data-ttu-id="77e4b-130">Viene utilizzata l'interfaccia ID3D10Include che dispone di due metodi implementati dall'utente: Open e Close.</span><span class="sxs-lookup"><span data-stu-id="77e4b-130">This uses the ID3D10Include interface which has two user-implemented methods: Open and Close.</span></span> <span data-ttu-id="77e4b-131">Per eseguire questa operazione, sarà necessario implementare il corpo dei metodi Open e Close; nel metodo Open aggiungere il codice da usare per aprire i file di inclusione desiderati, nella funzione close aggiungere il codice per chiudere i file al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="77e4b-131">To make this work, you will need to implement the body of the Open and Close methods; in the Open method add the code you would use to open whatever include files you want, in the Close function add the code to close the files when you are done with them.</span></span>
-   <span data-ttu-id="77e4b-132">Nome della funzione shader da compilare.</span><span class="sxs-lookup"><span data-stu-id="77e4b-132">The name of the shader function to compile.</span></span> <span data-ttu-id="77e4b-133">Questo shader compila la funzione Ripple.</span><span class="sxs-lookup"><span data-stu-id="77e4b-133">This shader compiles the Ripple function.</span></span>
-   <span data-ttu-id="77e4b-134">Profilo dello shader di destinazione durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="77e4b-134">The shader profile to target when compiling.</span></span> <span data-ttu-id="77e4b-135">Poiché è possibile compilare una funzione in un vertice, una geometria o una pixel shader, il profilo indica al compilatore il tipo di shader e il modello di shader con cui confrontare il codice.</span><span class="sxs-lookup"><span data-stu-id="77e4b-135">Since you can compile a function into a vertex, geometry, or pixel shader, the profile tells the compiler which type of shader and which shader model to compare the code against.</span></span>
-   <span data-ttu-id="77e4b-136">Flag del compilatore shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-136">Shader compiler flags.</span></span> <span data-ttu-id="77e4b-137">Questi flag indicano al compilatore quali informazioni inserire nell'output compilato e come si desidera ottimizzare il codice di output: per la velocità, per il debug e così via. Per un elenco dei flag disponibili, vedere [costanti degli effetti (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) .</span><span class="sxs-lookup"><span data-stu-id="77e4b-137">These flags tell the compiler what information to put into the compiled output and how you want the output code optimized: for speed, for debug, etc. See [Effect Constants (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) for a listing of the available flags.</span></span> <span data-ttu-id="77e4b-138">L'esempio contiene il codice che è possibile usare per impostare i valori dei flag del compilatore per il progetto. si tratta principalmente di una questione se si desidera o meno generare informazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="77e4b-138">The sample contains some code you can use to set the compiler flag values for your project - this is mainly a question of whether or not you want to generate debug information.</span></span>
-   <span data-ttu-id="77e4b-139">Puntatore al buffer che contiene il codice dello shader compilato.</span><span class="sxs-lookup"><span data-stu-id="77e4b-139">A pointer to the buffer that contains the compiled shader code.</span></span> <span data-ttu-id="77e4b-140">Il buffer contiene anche le informazioni di debug e tabella di simboli incorporate richieste dai flag del compilatore.</span><span class="sxs-lookup"><span data-stu-id="77e4b-140">The buffer also contains any embedded debug and symbol table information requested by the compiler flags.</span></span>
-   <span data-ttu-id="77e4b-141">Puntatore a un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione, che sono gli stessi messaggi visualizzati nell'output di debug se il debugger era in esecuzione durante la compilazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-141">A pointer to a buffer that contains a listing of errors and warnings that were encountered during the compile, which are the same messages you would see in the debug output if you were running the debugger while compiling the shader.</span></span> <span data-ttu-id="77e4b-142">**Null** è un valore accettabile se non si desidera che gli errori vengano restituiti a un buffer.</span><span class="sxs-lookup"><span data-stu-id="77e4b-142">**NULL** is an acceptable value when you don't want the errors returned to a buffer.</span></span>

<span data-ttu-id="77e4b-143">Se lo shader viene compilato correttamente, un puntatore al codice dello shader viene restituito come interfaccia ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="77e4b-143">If the shader compiles successfully, a pointer to the shader code is returned as a ID3D10Blob interface.</span></span> <span data-ttu-id="77e4b-144">Viene chiamato interfaccia BLOB perché il puntatore si trova in una posizione in memoria costituita da una matrice di DWORD.</span><span class="sxs-lookup"><span data-stu-id="77e4b-144">It is called the Blob interface because the pointer is to a location in memory that is made up of an array of DWORD's.</span></span> <span data-ttu-id="77e4b-145">L'interfaccia viene fornita in modo che sia possibile ottenere un puntatore allo shader compilato, che sarà necessario nel passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="77e4b-145">The interface is provided so that you can get a pointer to the compiled shader which you will need in the next step.</span></span>

<span data-ttu-id="77e4b-146">A partire da dicembre 2006 SDK, il compilatore DirectX 10 HLSL è ora il compilatore predefinito sia in DirectX 9 che in DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="77e4b-146">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="77e4b-147">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](/windows/desktop/direct3dtools/fxc) .</span><span class="sxs-lookup"><span data-stu-id="77e4b-147">See [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) for details.</span></span>

### <a name="get-a-pointer-to-a-compiled-shader"></a><span data-ttu-id="77e4b-148">Ottenere un puntatore a uno shader compilato</span><span class="sxs-lookup"><span data-stu-id="77e4b-148">Get a Pointer to a Compiled Shader</span></span>

<span data-ttu-id="77e4b-149">Diversi metodi API richiedono un puntatore a uno shader compilato.</span><span class="sxs-lookup"><span data-stu-id="77e4b-149">Several API methods require a pointer to a compiled shader.</span></span> <span data-ttu-id="77e4b-150">Questo argomento viene in genere chiamato *pShaderBytecode* perché punta a uno shader compilato rappresentato come sequenza di codici di byte.</span><span class="sxs-lookup"><span data-stu-id="77e4b-150">This argument is usually called *pShaderBytecode* because it points to a compiled shader represented as a sequence of byte codes.</span></span> <span data-ttu-id="77e4b-151">Per ottenere un puntatore a uno shader compilato, compilare innanzitutto lo shader chiamando [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) o una funzione simile.</span><span class="sxs-lookup"><span data-stu-id="77e4b-151">To get a pointer to a compiled shader, first compile the shader by calling [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) or a similar function.</span></span> <span data-ttu-id="77e4b-152">Se la compilazione ha esito positivo, lo shader compilato viene restituito in un'interfaccia [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) .</span><span class="sxs-lookup"><span data-stu-id="77e4b-152">If compilation is successful, the compiled shader is returned in an [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) interface.</span></span> <span data-ttu-id="77e4b-153">Infine, usare il metodo [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) per restituire il puntatore.</span><span class="sxs-lookup"><span data-stu-id="77e4b-153">Finally, use the [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) method to return the pointer.</span></span>

## <a name="create-a-shader-object"></a><span data-ttu-id="77e4b-154">Creare un oggetto shader</span><span class="sxs-lookup"><span data-stu-id="77e4b-154">Create a Shader Object</span></span>

<span data-ttu-id="77e4b-155">Una volta compilato lo shader, chiamare CreateVertexShader per creare l'oggetto shader:</span><span class="sxs-lookup"><span data-stu-id="77e4b-155">Once the shader is compiled, call CreateVertexShader to create the shader object:</span></span>


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



<span data-ttu-id="77e4b-156">Per creare l'oggetto shader, passare il puntatore allo shader compilato in CreateVertexShader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-156">To create the shader object, pass the pointer to the compiled shader into CreateVertexShader.</span></span> <span data-ttu-id="77e4b-157">Poiché è stato necessario compilare innanzitutto lo shader, questa chiamata verrà superata, a meno che non si sia verificato un problema di memoria nel computer.</span><span class="sxs-lookup"><span data-stu-id="77e4b-157">Since you had to successfully compile the shader first, this call will almost certainly pass, unless you have a memory problem on your machine.</span></span>

<span data-ttu-id="77e4b-158">È possibile creare tutti gli oggetti shader desiderati e mantenerne semplicemente i puntatori.</span><span class="sxs-lookup"><span data-stu-id="77e4b-158">You can create as many shader objects as you like and simply keep pointers to them.</span></span> <span data-ttu-id="77e4b-159">Lo stesso meccanismo funziona per la geometria e i pixel shader presupponendo che i profili dello shader (quando si chiama il metodo Compile) corrispondano ai nomi delle interfacce (quando si chiama il metodo Create).</span><span class="sxs-lookup"><span data-stu-id="77e4b-159">This same mechanism works for geometry and pixel shaders assuming you match the shader profiles (when you call the compile method) to the interface names (when you call the create method).</span></span>

## <a name="set-the-shader-object"></a><span data-ttu-id="77e4b-160">Impostare l'oggetto shader</span><span class="sxs-lookup"><span data-stu-id="77e4b-160">Set the Shader Object</span></span>

<span data-ttu-id="77e4b-161">L'ultimo passaggio consiste nell'impostare lo shader sulla fase della pipeline.</span><span class="sxs-lookup"><span data-stu-id="77e4b-161">The last step is set the shader to the pipeline stage.</span></span> <span data-ttu-id="77e4b-162">Poiché nella pipeline sono presenti tre fasi dello shader, sarà necessario effettuare tre chiamate API, una per ogni fase.</span><span class="sxs-lookup"><span data-stu-id="77e4b-162">Since there are three shader stages in the pipeline, you will need to make three API calls, one for each stage.</span></span>


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



<span data-ttu-id="77e4b-163">La chiamata a VSSetShader accetta il puntatore al vertex shader creato nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="77e4b-163">The call to VSSetShader takes the pointer to the vertex shader created in step 1.</span></span> <span data-ttu-id="77e4b-164">Questo consente di impostare lo shader nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77e4b-164">This sets the shader in the device.</span></span> <span data-ttu-id="77e4b-165">La fase vertex shader viene ora inizializzata con il relativo codice vertex shader, che rimane l'inizializzazione di eventuali variabili shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-165">The vertex shader stage is now initialized with its vertex shader code, all that remains is initializing any shader variables.</span></span>

## <a name="repeat-for-all-3-shader-stages"></a><span data-ttu-id="77e4b-166">Ripeti per tutte e tre le fasi dello shader</span><span class="sxs-lookup"><span data-stu-id="77e4b-166">Repeat for all 3 Shader Stages</span></span>

<span data-ttu-id="77e4b-167">Ripetere lo stesso set di passaggi per compilare qualsiasi vertice o pixel shader o anche un geometry shader che restituisce il pixel shader.</span><span class="sxs-lookup"><span data-stu-id="77e4b-167">Repeat these same set of steps to build any vertex or pixel shader or even a geometry shader that outputs to the pixel shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77e4b-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77e4b-168">Related Topics</span></span>

[<span data-ttu-id="77e4b-169">Compilazione di shader</span><span class="sxs-lookup"><span data-stu-id="77e4b-169">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a><span data-ttu-id="77e4b-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77e4b-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77e4b-171">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="77e4b-171">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

