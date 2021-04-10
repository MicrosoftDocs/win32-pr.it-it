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
# <a name="using-an-effect-direct3d-9"></a><span data-ttu-id="bb058-103">Uso di un effetto (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bb058-103">Using an Effect (Direct3D 9)</span></span>

<span data-ttu-id="bb058-104">In questa pagina viene illustrato come generare e utilizzare un effetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-104">This page will show you how to generate and use an effect.</span></span> <span data-ttu-id="bb058-105">Gli argomenti trattati includono:</span><span class="sxs-lookup"><span data-stu-id="bb058-105">The topics covered include how to:</span></span>

-   [<span data-ttu-id="bb058-106">Creazione di un effetto</span><span class="sxs-lookup"><span data-stu-id="bb058-106">Create an Effect</span></span>](#create-an-effect)
-   [<span data-ttu-id="bb058-107">Eseguire il rendering di un effetto</span><span class="sxs-lookup"><span data-stu-id="bb058-107">Render an Effect</span></span>](#render-an-effect)
-   [<span data-ttu-id="bb058-108">Usare la semantica per trovare i parametri degli effetti</span><span class="sxs-lookup"><span data-stu-id="bb058-108">Use Semantics to Find Effect Parameters</span></span>](#use-semantics-to-find-effect-parameters)
-   [<span data-ttu-id="bb058-109">Usare gli handle per ottenere e impostare i parametri in modo efficiente</span><span class="sxs-lookup"><span data-stu-id="bb058-109">Use Handles to Get and Set Parameters Efficiently</span></span>](#use-handles-to-get-and-set-parameters-efficiently)
-   [<span data-ttu-id="bb058-110">Aggiungere informazioni sui parametri con le annotazioni</span><span class="sxs-lookup"><span data-stu-id="bb058-110">Add Parameter Information with Annotations</span></span>](#add-parameter-information-with-annotations)
-   [<span data-ttu-id="bb058-111">Parametri dell'effetto di condivisione</span><span class="sxs-lookup"><span data-stu-id="bb058-111">Share Effect Parameters</span></span>](#share-effect-parameters)
-   [<span data-ttu-id="bb058-112">Compilare un effetto offline</span><span class="sxs-lookup"><span data-stu-id="bb058-112">Compile an Effect Offline</span></span>](#compile-an-effect-offline)
-   [<span data-ttu-id="bb058-113">Migliorare le prestazioni con i preshader</span><span class="sxs-lookup"><span data-stu-id="bb058-113">Improve Performance with Preshaders</span></span>](#improve-performance-with-preshaders)
-   [<span data-ttu-id="bb058-114">Usare i blocchi di parametri per gestire i parametri degli effetti</span><span class="sxs-lookup"><span data-stu-id="bb058-114">Use Parameter Blocks to Manage Effect Parameters</span></span>](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a><span data-ttu-id="bb058-115">Creazione di un effetto</span><span class="sxs-lookup"><span data-stu-id="bb058-115">Create an Effect</span></span>

<span data-ttu-id="bb058-116">Di seguito è riportato un esempio di creazione di un effetto tratto dall' [esempio BasicHLSL](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="bb058-116">Here is an example of creating an effect taken from the [BasicHLSL Sample](../directx-sdk--august-2009-.md).</span></span> <span data-ttu-id="bb058-117">Il codice di creazione dell'effetto per la creazione di uno shader di debug è da **OnCreateDevice**:</span><span class="sxs-lookup"><span data-stu-id="bb058-117">The effect creation code for creating a debug shader is from **OnCreateDevice**:</span></span>


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



<span data-ttu-id="bb058-118">Questa funzione accetta gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb058-118">This function takes these arguments:</span></span>

-   <span data-ttu-id="bb058-119">Dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb058-119">The device.</span></span>
-   <span data-ttu-id="bb058-120">Nome del file di effetti.</span><span class="sxs-lookup"><span data-stu-id="bb058-120">The file name of the effect file.</span></span>
-   <span data-ttu-id="bb058-121">Puntatore a un elenco di definizioni con terminazione NULL \# da utilizzare durante l'analisi dello shader.</span><span class="sxs-lookup"><span data-stu-id="bb058-121">A pointer to a NULL-terminated list of \#defines, to be used while parsing the shader.</span></span>
-   <span data-ttu-id="bb058-122">Puntatore facoltativo a un gestore di inclusione scritto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bb058-122">An optional pointer to a user-written include handler.</span></span> <span data-ttu-id="bb058-123">Il gestore viene chiamato dal processore ogni volta che è necessario risolvere un' \# inclusione.</span><span class="sxs-lookup"><span data-stu-id="bb058-123">The handler is called by the processor whenever it needs to resolve a \#include.</span></span>
-   <span data-ttu-id="bb058-124">Flag di compilazione dello shader che fornisce gli hint del compilatore su come verrà utilizzato lo shader.</span><span class="sxs-lookup"><span data-stu-id="bb058-124">A shader compile flag that gives the compiler hints about how the shader will be used.</span></span> <span data-ttu-id="bb058-125">Queste opzioni includono:</span><span class="sxs-lookup"><span data-stu-id="bb058-125">The options include:</span></span>
    -   <span data-ttu-id="bb058-126">La convalida verrà ignorata se sono stati compilati noti shader validi.</span><span class="sxs-lookup"><span data-stu-id="bb058-126">Skipping validation, if known good shaders are being compiled.</span></span>
    -   <span data-ttu-id="bb058-127">Ottimizzazione ignorata (talvolta utilizzata quando le ottimizzazioni rendono più difficile il debug).</span><span class="sxs-lookup"><span data-stu-id="bb058-127">Skipping optimization (sometimes used when optimizations make debugging harder).</span></span>
    -   <span data-ttu-id="bb058-128">La richiesta di informazioni di debug da includere nello shader, in modo che sia possibile eseguirne il debug.</span><span class="sxs-lookup"><span data-stu-id="bb058-128">Requesting debug information to be included in the shader so it can be debugged.</span></span>
-   <span data-ttu-id="bb058-129">Pool di effetti.</span><span class="sxs-lookup"><span data-stu-id="bb058-129">The effect pool.</span></span> <span data-ttu-id="bb058-130">Se più di un effetto utilizza lo stesso puntatore del pool di memoria, le variabili globali negli effetti vengono condivise tra loro.</span><span class="sxs-lookup"><span data-stu-id="bb058-130">If more than one effect uses the same memory pool pointer, the global variables in the effects are shared with each other.</span></span> <span data-ttu-id="bb058-131">Se non è necessario condividere le variabili di effetto, il pool di memoria può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="bb058-131">If there is no need to share effect variables, the memory pool can be set to **NULL**.</span></span>
-   <span data-ttu-id="bb058-132">Puntatore al nuovo effetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-132">A pointer to the new effect.</span></span>
-   <span data-ttu-id="bb058-133">Puntatore a un buffer a cui è possibile inviare gli errori di convalida.</span><span class="sxs-lookup"><span data-stu-id="bb058-133">A pointer to a buffer to which validation errors can be sent.</span></span> <span data-ttu-id="bb058-134">In questo esempio il parametro è stato impostato su **null** e non è stato utilizzato.</span><span class="sxs-lookup"><span data-stu-id="bb058-134">In this example, the parameter was set to **NULL** and not used.</span></span>

> [!Note]  
> <span data-ttu-id="bb058-135">A partire da dicembre 2006 SDK, il compilatore DirectX 10 HLSL è ora il compilatore predefinito sia in DirectX 9 che in DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="bb058-135">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="bb058-136">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="bb058-136">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

 

## <a name="render-an-effect"></a><span data-ttu-id="bb058-137">Eseguire il rendering di un effetto</span><span class="sxs-lookup"><span data-stu-id="bb058-137">Render an Effect</span></span>

<span data-ttu-id="bb058-138">La sequenza di chiamate per applicare lo stato di effetto a un dispositivo è la seguente:</span><span class="sxs-lookup"><span data-stu-id="bb058-138">The sequence of calls for applying effect state to a device is:</span></span>

-   <span data-ttu-id="bb058-139">[**ID3DXEffect:: Begin**](id3dxeffect--begin.md) imposta la tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="bb058-139">[**ID3DXEffect::Begin**](id3dxeffect--begin.md) sets the active technique.</span></span>
-   <span data-ttu-id="bb058-140">[**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) imposta il passaggio attivo.</span><span class="sxs-lookup"><span data-stu-id="bb058-140">[**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) sets the active pass.</span></span>
-   <span data-ttu-id="bb058-141">[**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) aggiorna le modifiche apportate a qualsiasi chiamata set nel passaggio.</span><span class="sxs-lookup"><span data-stu-id="bb058-141">[**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) updates changes to any set calls in the pass.</span></span> <span data-ttu-id="bb058-142">Questo metodo deve essere chiamato prima di qualsiasi chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-142">This should be called before any draw call.</span></span>
-   <span data-ttu-id="bb058-143">[**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) termina un passaggio.</span><span class="sxs-lookup"><span data-stu-id="bb058-143">[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) ends a pass.</span></span>
-   <span data-ttu-id="bb058-144">[**ID3DXEffect:: end**](id3dxeffect--end.md) termina la tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="bb058-144">[**ID3DXEffect::End**](id3dxeffect--end.md) ends the active technique.</span></span>

<span data-ttu-id="bb058-145">Il codice di rendering degli effetti è anche più semplice del codice di rendering corrispondente senza alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-145">Effect render code is also simpler than the corresponding render code without an effect.</span></span> <span data-ttu-id="bb058-146">Ecco il codice di rendering con effetto:</span><span class="sxs-lookup"><span data-stu-id="bb058-146">Here's the render code with an effect:</span></span>


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



<span data-ttu-id="bb058-147">Il ciclo di rendering è costituito dall'esecuzione di query sull'effetto per verificare il numero di passaggi che contiene e quindi sulla chiamata di tutti i passaggi per una tecnica.</span><span class="sxs-lookup"><span data-stu-id="bb058-147">The render loop consists of querying the effect to see how many passes it contains, and then calling all the passes for a technique.</span></span> <span data-ttu-id="bb058-148">Il ciclo di rendering può essere espanso per chiamare più tecniche, ognuna con più sessioni.</span><span class="sxs-lookup"><span data-stu-id="bb058-148">The render loop could be expanded to call multiple techniques, each with multiple passes.</span></span>

## <a name="use-semantics-to-find-effect-parameters"></a><span data-ttu-id="bb058-149">Usare la semantica per trovare i parametri degli effetti</span><span class="sxs-lookup"><span data-stu-id="bb058-149">Use Semantics to Find Effect Parameters</span></span>

<span data-ttu-id="bb058-150">Una semantica è un identificatore associato a un parametro Effect per consentire a un'applicazione di cercare il parametro.</span><span class="sxs-lookup"><span data-stu-id="bb058-150">A semantic is an identifier that is attached to an effect parameter to allow an application to search for the parameter.</span></span> <span data-ttu-id="bb058-151">Un parametro può avere al massimo una semantica.</span><span class="sxs-lookup"><span data-stu-id="bb058-151">A parameter can have at most one semantic.</span></span> <span data-ttu-id="bb058-152">La semantica si trova dopo i due punti (:) dopo il nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="bb058-152">The semantic is located following a colon (:) after the parameter name.</span></span> <span data-ttu-id="bb058-153">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="bb058-153">For instance:</span></span>


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



<span data-ttu-id="bb058-154">Se è stata dichiarata la variabile globale Effect senza usare una semantica, il risultato sarà simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="bb058-154">If you declared the effect global variable without using a semantic, it would look like this instead:</span></span>


```
float4x4 matWorldViewProj;
```



<span data-ttu-id="bb058-155">L'interfaccia Effect può usare una semantica per ottenere un handle per un parametro di effetto specifico.</span><span class="sxs-lookup"><span data-stu-id="bb058-155">The effect interface can use a semantic to get a handle to a particular effect parameter.</span></span> <span data-ttu-id="bb058-156">Ad esempio, il codice seguente restituisce l'handle della matrice:</span><span class="sxs-lookup"><span data-stu-id="bb058-156">For instance, the following returns the handle of the matrix:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



<span data-ttu-id="bb058-157">Oltre a eseguire ricerche in base al nome semantico, l'interfaccia degli effetti ha molti altri metodi per la ricerca di parametri.</span><span class="sxs-lookup"><span data-stu-id="bb058-157">In addition to searching by semantic name, the effect interface has many other methods to search for parameters.</span></span>

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a><span data-ttu-id="bb058-158">Usare gli handle per ottenere e impostare i parametri in modo efficiente</span><span class="sxs-lookup"><span data-stu-id="bb058-158">Use Handles to Get and Set Parameters Efficiently</span></span>

<span data-ttu-id="bb058-159">Gli handle forniscono un modo efficiente per fare riferimento a parametri, tecniche, passaggi e annotazioni effettivi con effetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-159">Handles provide an efficient means for referencing effect parameters, techniques, passes, and annotations with an effect.</span></span> <span data-ttu-id="bb058-160">Gli handle (che sono di tipo D3DXHANDLE) sono puntatori di stringa.</span><span class="sxs-lookup"><span data-stu-id="bb058-160">Handles (which are of type D3DXHANDLE) are string pointers.</span></span> <span data-ttu-id="bb058-161">Gli handle passati in funzioni quali GetParameterxxx o GetAnnotationxxx possono essere in uno dei tre formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb058-161">The handles that are passed into functions such as GetParameterxxx or GetAnnotationxxx can be in one of three forms:</span></span>

-   <span data-ttu-id="bb058-162">Handle restituito da una funzione, ad esempio GetParameterxxx.</span><span class="sxs-lookup"><span data-stu-id="bb058-162">A handle returned by a function such as GetParameterxxx.</span></span>
-   <span data-ttu-id="bb058-163">Stringa contenente il nome del parametro, tecnica, passaggio o annotazione.</span><span class="sxs-lookup"><span data-stu-id="bb058-163">A string containing the name of the parameter, technique, pass, or annotation.</span></span>
-   <span data-ttu-id="bb058-164">Handle impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="bb058-164">A handle set to **NULL**.</span></span>

<span data-ttu-id="bb058-165">In questo esempio viene restituito un handle al parametro a cui è associata la semantica WORLDVIEWPROJ:</span><span class="sxs-lookup"><span data-stu-id="bb058-165">This example returns a handle to the parameter that has the WORLDVIEWPROJ semantic attached to it:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a><span data-ttu-id="bb058-166">Aggiungere informazioni sui parametri con le annotazioni</span><span class="sxs-lookup"><span data-stu-id="bb058-166">Add Parameter Information with Annotations</span></span>

<span data-ttu-id="bb058-167">Le annotazioni sono dati specifici dell'utente che possono essere collegati a qualsiasi tecnica, passaggio o parametro.</span><span class="sxs-lookup"><span data-stu-id="bb058-167">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="bb058-168">Un'annotazione è un modo flessibile per aggiungere informazioni a singoli parametri.</span><span class="sxs-lookup"><span data-stu-id="bb058-168">An annotation is a flexible way to add information to individual parameters.</span></span> <span data-ttu-id="bb058-169">Le informazioni possono essere lette e usate in qualsiasi modo scelto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bb058-169">The information can be read back and used any way the application chooses.</span></span> <span data-ttu-id="bb058-170">Un'annotazione può essere di qualsiasi tipo di dati e può essere aggiunta dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="bb058-170">An annotation can be of any data type and can be added dynamically.</span></span> <span data-ttu-id="bb058-171">Le dichiarazioni di annotazione sono delimitate da parentesi angolari.</span><span class="sxs-lookup"><span data-stu-id="bb058-171">Annotation declarations are delimited by angle brackets.</span></span> <span data-ttu-id="bb058-172">Un'annotazione contiene:</span><span class="sxs-lookup"><span data-stu-id="bb058-172">An annotation contains:</span></span>

-   <span data-ttu-id="bb058-173">Tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="bb058-173">A data type.</span></span>
-   <span data-ttu-id="bb058-174">Nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="bb058-174">A variable name.</span></span>
-   <span data-ttu-id="bb058-175">Segno di uguale (=).</span><span class="sxs-lookup"><span data-stu-id="bb058-175">An equals sign (=).</span></span>
-   <span data-ttu-id="bb058-176">Valore dei dati.</span><span class="sxs-lookup"><span data-stu-id="bb058-176">The data value.</span></span>
-   <span data-ttu-id="bb058-177">Punto e virgola finale (;).</span><span class="sxs-lookup"><span data-stu-id="bb058-177">A ending semicolon (;).</span></span>

<span data-ttu-id="bb058-178">Ad esempio, entrambi gli esempi precedenti di questo documento contengono questa annotazione:</span><span class="sxs-lookup"><span data-stu-id="bb058-178">For instance, both of the previous examples in this paper contain this annotation:</span></span>


```
texture Tex0 < string name = "tiger.bmp"; >;
```



<span data-ttu-id="bb058-179">L'annotazione è collegata all'oggetto trama e specifica il file di trama da usare per inizializzare l'oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="bb058-179">The annotation is attached to the texture object and specifies the texture file that should be used to initialize the texture object.</span></span> <span data-ttu-id="bb058-180">L'annotazione non Inizializza l'oggetto trama. si tratta semplicemente di una parte di informazioni utente collegata alla variabile.</span><span class="sxs-lookup"><span data-stu-id="bb058-180">The annotation does not initialize the texture object, it is simply a piece of user information that is attached to the variable.</span></span> <span data-ttu-id="bb058-181">Un'applicazione può leggere l'annotazione con [**ID3DXBaseEffect:: GetAnnotation**](id3dxbaseeffect--getannotation.md) o [**ID3DXBaseEffect:: GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) per restituire la stringa.</span><span class="sxs-lookup"><span data-stu-id="bb058-181">An application can read the annotation with either [**ID3DXBaseEffect::GetAnnotation**](id3dxbaseeffect--getannotation.md) or [**ID3DXBaseEffect::GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) to return the string.</span></span> <span data-ttu-id="bb058-182">È inoltre possibile aggiungere annotazioni dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bb058-182">Annotations can also be added by the application.</span></span>

<span data-ttu-id="bb058-183">Ogni annotazione:</span><span class="sxs-lookup"><span data-stu-id="bb058-183">Each annotation:</span></span>

-   <span data-ttu-id="bb058-184">Deve essere numerico o stringhe.</span><span class="sxs-lookup"><span data-stu-id="bb058-184">Must be either numeric or strings.</span></span>
-   <span data-ttu-id="bb058-185">Deve sempre essere inizializzato con un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="bb058-185">Must always be initialized with a default value.</span></span>
-   <span data-ttu-id="bb058-186">Può essere associato a [tecniche e passaggi (Direct3D 9)](techniques-and-passes.md) e ai parametri di [effetto](/previous-versions/windows/desktop/ee417539(v=vs.85))di primo livello.</span><span class="sxs-lookup"><span data-stu-id="bb058-186">Can be associated with [Techniques and Passes (Direct3D 9)](techniques-and-passes.md) and top-level [Effect Parameters](/previous-versions/windows/desktop/ee417539(v=vs.85)).</span></span>
-   <span data-ttu-id="bb058-187">È possibile scrivere e leggere da con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="bb058-187">Can be written to and read from with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>
-   <span data-ttu-id="bb058-188">Può essere aggiunto con [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="bb058-188">Can be added with [**ID3DXEffect**](id3dxeffect.md).</span></span>
-   <span data-ttu-id="bb058-189">Non è possibile fare riferimento all'interno dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-189">Cannot be referenced inside the effect.</span></span>
-   <span data-ttu-id="bb058-190">Non è possibile avere una semantica o annotazioni secondarie.</span><span class="sxs-lookup"><span data-stu-id="bb058-190">Cannot have sub-semantics or sub-annotations.</span></span>

## <a name="share-effect-parameters"></a><span data-ttu-id="bb058-191">Parametri dell'effetto di condivisione</span><span class="sxs-lookup"><span data-stu-id="bb058-191">Share Effect Parameters</span></span>

<span data-ttu-id="bb058-192">I parametri degli effetti sono tutte le variabili non statiche dichiarate in un effetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-192">Effect parameters are all the non-static variables declared in an effect.</span></span> <span data-ttu-id="bb058-193">Possono essere incluse le variabili globali e le annotazioni.</span><span class="sxs-lookup"><span data-stu-id="bb058-193">This can include global variables and annotations.</span></span> <span data-ttu-id="bb058-194">I parametri effetti possono essere condivisi tra diversi effetti dichiarando i parametri con la parola chiave "Shared" e quindi creando l'effetto con un pool di effetti.</span><span class="sxs-lookup"><span data-stu-id="bb058-194">Effect parameters can be shared between different effects by declaring parameters with the "shared" keyword and then creating the effect with an effect pool.</span></span>

<span data-ttu-id="bb058-195">Un pool di effetti contiene i parametri degli effetti condivisi.</span><span class="sxs-lookup"><span data-stu-id="bb058-195">An effect pool contains shared effect parameters.</span></span> <span data-ttu-id="bb058-196">Il pool viene creato chiamando [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), che restituisce un'interfaccia [**ID3DXEffectPool**](id3dxeffectpool.md) .</span><span class="sxs-lookup"><span data-stu-id="bb058-196">The pool is created by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), which returns an [**ID3DXEffectPool**](id3dxeffectpool.md) interface.</span></span> <span data-ttu-id="bb058-197">L'interfaccia può essere fornita come input per qualsiasi funzione D3DXCreateEffectxxx quando viene creato un effetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-197">The interface can be supplied as an input to any of the D3DXCreateEffectxxx functions when an effect is created.</span></span> <span data-ttu-id="bb058-198">Affinché un parametro venga condiviso tra più effetti, il parametro deve avere lo stesso nome, tipo e semantica in ciascuno degli effetti condivisi.</span><span class="sxs-lookup"><span data-stu-id="bb058-198">For a parameter to be shared across multiple effects, the parameter must have the same name, type, and semantic in each of the shared effects.</span></span>


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



<span data-ttu-id="bb058-199">Gli effetti che condividono i parametri devono usare lo stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb058-199">Effects that share parameters must use the same device.</span></span> <span data-ttu-id="bb058-200">Questa operazione viene applicata per evitare la condivisione di parametri dipendenti dal dispositivo, ad esempio shader o trame, in dispositivi diversi.</span><span class="sxs-lookup"><span data-stu-id="bb058-200">This is enforced to prevent the sharing of device-dependent parameters (such as shaders or textures) across different devices.</span></span> <span data-ttu-id="bb058-201">I parametri vengono eliminati dal pool ogni volta che vengono rilasciati gli effetti che contengono i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="bb058-201">Parameters are deleted from the pool whenever the effects that contain the shared parameters are released.</span></span> <span data-ttu-id="bb058-202">Se non è necessario condividere parametri, specificare **null** per il pool di effetti quando viene creato un effetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-202">If sharing parameters is not necessary, supply **NULL** for the effect pool when an effect is created.</span></span>

<span data-ttu-id="bb058-203">Gli effetti clonati utilizzano lo stesso pool di effetti dell'effetto da cui vengono clonati.</span><span class="sxs-lookup"><span data-stu-id="bb058-203">Cloned effects use the same effect pool as the effect from which they are cloned.</span></span> <span data-ttu-id="bb058-204">La clonazione di un effetto crea una copia esatta di un effetto, incluse le variabili globali, le tecniche, i passaggi e le annotazioni.</span><span class="sxs-lookup"><span data-stu-id="bb058-204">Cloning an effect makes an exact copy of an effect, including global variables, techniques, passes, and annotations.</span></span>

## <a name="compile-an-effect-offline"></a><span data-ttu-id="bb058-205">Compilare un effetto offline</span><span class="sxs-lookup"><span data-stu-id="bb058-205">Compile an Effect Offline</span></span>

<span data-ttu-id="bb058-206">È possibile compilare un effetto in fase di esecuzione con [**D3DXCreateEffect**](d3dxcreateeffect.md)oppure è possibile compilare un effetto offline usando lo strumento compilatore della riga di comando fxc.exe.</span><span class="sxs-lookup"><span data-stu-id="bb058-206">You can compile an effect at run time with [**D3DXCreateEffect**](d3dxcreateeffect.md), or you can compile an effect offline using the command-line compiler tool fxc.exe.</span></span> <span data-ttu-id="bb058-207">L'effetto nell' [esempio CompiledEffect](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contiene un vertex shader, un pixel shader e una tecnica:</span><span class="sxs-lookup"><span data-stu-id="bb058-207">The effect in the [CompiledEffect Sample](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contains a vertex shader, a pixel shader, and one technique:</span></span>


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



<span data-ttu-id="bb058-208">Usando lo [strumento del compilatore degli effetti](../direct3dtools/fxc.md) per compilare lo shader per vs \_ 1 \_ 1, sono state generate le seguenti istruzioni per gli shader di assembly:</span><span class="sxs-lookup"><span data-stu-id="bb058-208">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generated the following assembly shader instructions:</span></span>


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



## <a name="improve-performance-with-preshaders"></a><span data-ttu-id="bb058-209">Migliorare le prestazioni con i preshader</span><span class="sxs-lookup"><span data-stu-id="bb058-209">Improve Performance with Preshaders</span></span>

<span data-ttu-id="bb058-210">Un preshader è una tecnica che consente di aumentare l'efficienza dello shader tramite il pre-calcolo delle espressioni di shader costanti.</span><span class="sxs-lookup"><span data-stu-id="bb058-210">A preshader is a technique for increasing shader efficiency by pre-calculating constant shader expressions.</span></span> <span data-ttu-id="bb058-211">Il compilatore Effect estrae automaticamente i calcoli dello shader dal corpo di uno shader e li esegue sulla CPU prima dello shader che esegue.</span><span class="sxs-lookup"><span data-stu-id="bb058-211">The effect compiler automatically pulls out shader computations from the body of a shader and executes them on the CPU prior to the shader running.</span></span> <span data-ttu-id="bb058-212">Di conseguenza, i preshader funzionano solo con effetti.</span><span class="sxs-lookup"><span data-stu-id="bb058-212">Consequently, preshaders only work with effects.</span></span> <span data-ttu-id="bb058-213">Ad esempio, queste due espressioni possono essere valutate all'esterno dello shader prima dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bb058-213">For instance, these two expressions can be evaluated outside of the shader before it runs.</span></span>


```
mul(World,mul(View, Projection));
sin(time)
```



<span data-ttu-id="bb058-214">I calcoli dello shader che è possibile spostare sono quelli associati a parametri uniformi; ovvero, i calcoli non cambiano per ogni vertice o pixel.</span><span class="sxs-lookup"><span data-stu-id="bb058-214">Shader computations that can be moved are those associated with uniform parameters; that is, the computations do not change for each vertex or pixel.</span></span> <span data-ttu-id="bb058-215">Se si usano gli effetti, il compilatore Effect genera automaticamente ed esegue un preshader. Nessun flag da abilitare.</span><span class="sxs-lookup"><span data-stu-id="bb058-215">If you are using effects, the effect compiler automatically generates and runs a preshader for you; there are no flags to enable.</span></span> <span data-ttu-id="bb058-216">I preshader possono ridurre il numero di istruzioni per shader e possono anche ridurre il numero di registri costanti utilizzati da uno shader.</span><span class="sxs-lookup"><span data-stu-id="bb058-216">Preshaders can reduce the number of instructions per shader and can also reduce the number of constant registers a shader consumes.</span></span>

<span data-ttu-id="bb058-217">Il compilatore degli effetti può essere considerato come un tipo di compilatore multiprocessore perché compila il codice dello shader per due tipi di processori: una CPU e una GPU.</span><span class="sxs-lookup"><span data-stu-id="bb058-217">Think of the effect compiler as a sort of multi-processor compiler because it compiles shader code for two types of processors: a CPU and a GPU.</span></span> <span data-ttu-id="bb058-218">Inoltre, il compilatore Effect è progettato per spostare il codice dalla GPU alla CPU e quindi migliorare le prestazioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="bb058-218">In addition, the effect compiler is designed to move code from the GPU to the CPU and therefore improve shader performance.</span></span> <span data-ttu-id="bb058-219">Questa operazione è molto simile all'estrazione di un'espressione statica da un ciclo.</span><span class="sxs-lookup"><span data-stu-id="bb058-219">This is very similar to pulling a static expression out of a loop.</span></span> <span data-ttu-id="bb058-220">Uno shader che trasforma la posizione dallo spazio globale allo spazio di proiezione e copia le coordinate di trama hanno un aspetto simile al seguente in HLSL:</span><span class="sxs-lookup"><span data-stu-id="bb058-220">A shader that transforms position from world space to projection space, and copies texture coordinates would look like this in HLSL:</span></span>


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



<span data-ttu-id="bb058-221">L'uso [dello strumento compilatore effetti](../direct3dtools/fxc.md) per compilare lo shader per vs \_ 1 \_ 1 genera le istruzioni di assembly seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb058-221">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generates the following assembly instructions:</span></span>


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



<span data-ttu-id="bb058-222">Questa operazione utilizza circa 14 slot e utilizza 9 registri costanti.</span><span class="sxs-lookup"><span data-stu-id="bb058-222">This uses up approximately 14 slots and consumes 9 constant registers.</span></span> <span data-ttu-id="bb058-223">Con un preshader, il compilatore sposta le espressioni statiche fuori dallo shader e nell'oggetto preshader.</span><span class="sxs-lookup"><span data-stu-id="bb058-223">With a preshader, the compiler moves the static expressions out of the shader and into the preshader.</span></span> <span data-ttu-id="bb058-224">Lo stesso shader avrà un aspetto simile al seguente con un preshader:</span><span class="sxs-lookup"><span data-stu-id="bb058-224">The same shader would look like this with a preshader:</span></span>


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



<span data-ttu-id="bb058-225">Un effetto esegue un preshader immediatamente prima dell'esecuzione di uno shader.</span><span class="sxs-lookup"><span data-stu-id="bb058-225">An effect executes a preshader just before executing a shader.</span></span> <span data-ttu-id="bb058-226">Il risultato è la stessa funzionalità con un aumento delle prestazioni dello shader poiché il numero di istruzioni da eseguire (per ogni vertice o pixel a seconda del tipo di shader) è stato ridotto.</span><span class="sxs-lookup"><span data-stu-id="bb058-226">The result is the same functionality with increased shader performance because the number of instructions that need to be executed (for each vertex or pixel depending on the type of shader) has been reduced.</span></span> <span data-ttu-id="bb058-227">Inoltre, un numero inferiore di registri costanti viene utilizzato dallo shader come risultato delle espressioni statiche spostate nel preshader.</span><span class="sxs-lookup"><span data-stu-id="bb058-227">In addition, fewer constant registers are consumed by the shader as a result of the static expressions being moved to the preshader.</span></span> <span data-ttu-id="bb058-228">Ciò significa che gli shader precedentemente limitati dal numero di registri costanti richiesti possono ora essere compilati perché richiedono un minor numero di registri costanti.</span><span class="sxs-lookup"><span data-stu-id="bb058-228">This means that shaders previously limited by the number of constant registers they required may now compile because they require fewer constant registers.</span></span> <span data-ttu-id="bb058-229">È ragionevole prevedere un miglioramento delle prestazioni del 5% e del 20% rispetto ai preshader.</span><span class="sxs-lookup"><span data-stu-id="bb058-229">It is reasonable to expect a 5 percent and a 20 percent performance improvement from preshaders.</span></span>

<span data-ttu-id="bb058-230">Tenere presente che le costanti di input sono diverse dalle costanti di output in un preshader.</span><span class="sxs-lookup"><span data-stu-id="bb058-230">Keep in mind that the input constants are different from the output constants in a preshader.</span></span> <span data-ttu-id="bb058-231">L'output C1 non corrisponde al registro C1 di input.</span><span class="sxs-lookup"><span data-stu-id="bb058-231">The output c1 is not the same as the input c1 register.</span></span> <span data-ttu-id="bb058-232">La scrittura in un registro costante in un preshader scrive effettivamente nello slot di input (costante) dello shader corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bb058-232">Writing to a constant register in a preshader actually writes into the corresponding shader's input (constant) slot.</span></span>


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



<span data-ttu-id="bb058-233">Con l'istruzione CMP precedente verrà letto il valore C1 preshader, mentre l'istruzione mul scriverà nei registri dell'hardware shader che verranno usati dal vertex shader.</span><span class="sxs-lookup"><span data-stu-id="bb058-233">The cmp instruction above will read the preshader c1 value, while the mul instruction will write to the hardware shader registers to be used by the vertex shader.</span></span>

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a><span data-ttu-id="bb058-234">Usare i blocchi di parametri per gestire i parametri degli effetti</span><span class="sxs-lookup"><span data-stu-id="bb058-234">Use Parameter Blocks to Manage Effect Parameters</span></span>

<span data-ttu-id="bb058-235">I blocchi di parametri sono blocchi delle modifiche allo stato dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="bb058-235">Parameter blocks are blocks of effect state changes.</span></span> <span data-ttu-id="bb058-236">Un blocco di parametri può registrare le modifiche di stato, in modo che possano essere applicate in un secondo momento con una singola chiamata.</span><span class="sxs-lookup"><span data-stu-id="bb058-236">A parameter block can record state changes, so that they can be applied later on with a single call.</span></span> <span data-ttu-id="bb058-237">Creare un blocco di parametri chiamando [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span><span class="sxs-lookup"><span data-stu-id="bb058-237">Create a parameter block by calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span></span>


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



<span data-ttu-id="bb058-238">Il blocco di parametri Salva quattro modifiche applicate dalle chiamate API.</span><span class="sxs-lookup"><span data-stu-id="bb058-238">The parameter block saves four changes applied by the API calls.</span></span> <span data-ttu-id="bb058-239">La chiamata di [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md) avvia la registrazione delle modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="bb058-239">Calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md) starts recording the state changes.</span></span> <span data-ttu-id="bb058-240">[**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md) interrompe l'aggiunta delle modifiche al blocco di parametri e restituisce un handle.</span><span class="sxs-lookup"><span data-stu-id="bb058-240">[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md) stops adding the changes to the parameter block and returns a handle.</span></span> <span data-ttu-id="bb058-241">L'handle verrà usato durante la chiamata di [**ID3DXEffect:: ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="bb058-241">The handle will be used when calling [**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span></span>

<span data-ttu-id="bb058-242">Nell' [esempio EffectParam](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), il blocco di parametri viene applicato nella sequenza di rendering:</span><span class="sxs-lookup"><span data-stu-id="bb058-242">In the [EffectParam Sample](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), the parameter block is applied in the render sequence:</span></span>


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



<span data-ttu-id="bb058-243">Il blocco di parametri imposta il valore di tutte e quattro le modifiche dello stato appena prima della chiamata a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="bb058-243">The parameter block sets the value of all four of the state changes just before [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called.</span></span> <span data-ttu-id="bb058-244">I blocchi di parametri sono un modo pratico per impostare più modifiche di stato con una singola chiamata API.</span><span class="sxs-lookup"><span data-stu-id="bb058-244">Parameter blocks are a handy way to set multiple state changes with a single API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb058-245">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bb058-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb058-246">Effetti</span><span class="sxs-lookup"><span data-stu-id="bb058-246">Effects</span></span>](effects.md)
</dt> </dl>

 

 
