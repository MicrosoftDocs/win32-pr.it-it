---
description: Una volta creato un effetto, il primo passaggio consiste nel compilare il codice per verificare la presenza di problemi di sintassi.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compilare un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225578"
---
# <a name="compile-an-effect-direct3d-10"></a><span data-ttu-id="8719b-103">Compilare un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8719b-103">Compile an Effect (Direct3D 10)</span></span>

<span data-ttu-id="8719b-104">Una volta creato un effetto, il primo passaggio consiste nel compilare il codice per verificare la presenza di problemi di sintassi.</span><span class="sxs-lookup"><span data-stu-id="8719b-104">Once an effect has been authored, the first step is to compile the code to check for syntax problems.</span></span> <span data-ttu-id="8719b-105">Questa operazione viene eseguita chiamando una delle API di compilazione, ad esempio D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory.</span><span class="sxs-lookup"><span data-stu-id="8719b-105">This is done by calling one of the compile APIs (like D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span></span> <span data-ttu-id="8719b-106">Queste API richiamano il compilatore Effect fxc.exe che è il compilatore usato per compilare il codice HLSL.</span><span class="sxs-lookup"><span data-stu-id="8719b-106">These API's invoke the effect compiler fxc.exe which is the compiler used to compile HLSL code.</span></span> <span data-ttu-id="8719b-107">Questo è il motivo per cui la sintassi per il codice in un effetto è molto simile a quella del codice HLSL (ci sono alcune eccezioni che verranno gestite successivamente).</span><span class="sxs-lookup"><span data-stu-id="8719b-107">This is why the syntax for code in an effect looks very much like HLSL code (there are a few exceptions that will be handled later).</span></span> <span data-ttu-id="8719b-108">Il compilatore HLSL (fxc.exe) Effect si trova nell'SDK nella cartella Utilities, in modo che sia possibile compilare gli shader (o gli effetti) offline se lo si sceglie.</span><span class="sxs-lookup"><span data-stu-id="8719b-108">By the way, the effect compiler/hlsl compiler (fxc.exe) is in the SDK in the utilities folder so that you can compile your shaders (or effects) offline if you choose.</span></span> <span data-ttu-id="8719b-109">Vedere la documentazione per l'esecuzione del compilatore dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="8719b-109">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="8719b-110">Includes</span><span class="sxs-lookup"><span data-stu-id="8719b-110">Includes</span></span>](#includes)
-   [<span data-ttu-id="8719b-111">Macro</span><span class="sxs-lookup"><span data-stu-id="8719b-111">Macros</span></span>](#macros)
-   [<span data-ttu-id="8719b-112">Flag shader HLSL</span><span class="sxs-lookup"><span data-stu-id="8719b-112">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="8719b-113">Flag FX</span><span class="sxs-lookup"><span data-stu-id="8719b-113">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="8719b-114">Verifica degli errori</span><span class="sxs-lookup"><span data-stu-id="8719b-114">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="8719b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8719b-115">Related topics</span></span>](#related-topics)

<span data-ttu-id="8719b-116">Di seguito è riportato un esempio di compilazione di un file di effetti (dall'esempio BasicHLSL10).</span><span class="sxs-lookup"><span data-stu-id="8719b-116">Here's an example of compiling an effect file (from the BasicHLSL10 sample).</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a><span data-ttu-id="8719b-117">Includes</span><span class="sxs-lookup"><span data-stu-id="8719b-117">Includes</span></span>

<span data-ttu-id="8719b-118">Un parametro è un'interfaccia di inclusione.</span><span class="sxs-lookup"><span data-stu-id="8719b-118">One parameter is an include interface.</span></span> <span data-ttu-id="8719b-119">Generare uno di questi se si desidera includere un comportamento personalizzato durante la lettura di un file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="8719b-119">Generate one of these if you want to include a customized behavior when reading an include file.</span></span> <span data-ttu-id="8719b-120">Questo comportamento personalizzato viene eseguito ogni volta che viene creato un effetto (che usa il puntatore di inclusione) o quando viene compilato un effetto (che usa il puntatore di inclusione).</span><span class="sxs-lookup"><span data-stu-id="8719b-120">This custom behavior is executed each time an effect (that uses the include pointer) is created or when an effect (that uses the include pointer) is compiled.</span></span> <span data-ttu-id="8719b-121">Per implementare il comportamento di inclusione personalizzato, derivare una classe dall'interfaccia di inclusione.</span><span class="sxs-lookup"><span data-stu-id="8719b-121">To implement customized include behavior, derive a class from the Include interface.</span></span> <span data-ttu-id="8719b-122">In questo modo sono disponibili i due metodi di classe: Open e Close.</span><span class="sxs-lookup"><span data-stu-id="8719b-122">This provides your class two methods: Open and Close.</span></span> <span data-ttu-id="8719b-123">Implementare il comportamento personalizzato nei metodi Open e Close.</span><span class="sxs-lookup"><span data-stu-id="8719b-123">Implement the custom behavior in the Open and Close methods.</span></span>

## <a name="macros"></a><span data-ttu-id="8719b-124">Macro</span><span class="sxs-lookup"><span data-stu-id="8719b-124">Macros</span></span>

<span data-ttu-id="8719b-125">La compilazione degli effetti può anche portare un puntatore a macro definite altrove.</span><span class="sxs-lookup"><span data-stu-id="8719b-125">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="8719b-126">Si supponga, ad esempio, di modificare l'effetto in BasicHLSL10 per usare due macro: zero e uno.</span><span class="sxs-lookup"><span data-stu-id="8719b-126">For example, suppose you were to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="8719b-127">Il codice di effetto che usa le due macro è illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8719b-127">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="8719b-128">Di seguito è illustrata la dichiarazione per le due macro.</span><span class="sxs-lookup"><span data-stu-id="8719b-128">Here is the declaration for the two macros.</span></span>


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="8719b-129">Le macro sono una matrice di macro con terminazione NULL. dove ogni macro viene definita con uno struct di [**\_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="8719b-129">The macros are a NULL terminated array of macros; where each macro is defined with a [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="8719b-130">Infine, modificare la chiamata dell'effetto di compilazione per portare un puntatore alle macro.</span><span class="sxs-lookup"><span data-stu-id="8719b-130">Lastly, modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="8719b-131">Flag shader HLSL</span><span class="sxs-lookup"><span data-stu-id="8719b-131">HLSL Shader Flags</span></span>

<span data-ttu-id="8719b-132">I flag shader specificano i vincoli dello shader per il compilatore HLSL.</span><span class="sxs-lookup"><span data-stu-id="8719b-132">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="8719b-133">Questi flag influiscano sul codice generato dal compilatore shader, tra cui:</span><span class="sxs-lookup"><span data-stu-id="8719b-133">These flags impact the code generated by the shader compiler including:</span></span>

-   <span data-ttu-id="8719b-134">Considerazioni sulle dimensioni: ottimizzare il codice.</span><span class="sxs-lookup"><span data-stu-id="8719b-134">Size considerations: optimize the code.</span></span>
-   <span data-ttu-id="8719b-135">Considerazioni sul debug: incluse le informazioni di debug, impedendo il controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="8719b-135">Debug considerations: including debug information, preventing flow control.</span></span>
-   <span data-ttu-id="8719b-136">Considerazioni sull'hardware: la destinazione di compilazione e se uno shader può essere eseguito su hardware legacy.</span><span class="sxs-lookup"><span data-stu-id="8719b-136">Hardware considerations: the compile target and whether or not a shader can run on legacy hardware.</span></span>

<span data-ttu-id="8719b-137">In generale, questi flag possono essere combinati logicamente, supponendo che non siano state specificate due caratteristiche in conflitto.</span><span class="sxs-lookup"><span data-stu-id="8719b-137">In general, these flags can be logically combined, assuming you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="8719b-138">Per un elenco dei flag, vedere [costanti degli effetti (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8719b-138">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="8719b-139">Flag FX</span><span class="sxs-lookup"><span data-stu-id="8719b-139">FX Flags</span></span>

<span data-ttu-id="8719b-140">Questi flag utilizzati durante la creazione di un effetto per definire il comportamento di compilazione o l'effetto di Runtime.</span><span class="sxs-lookup"><span data-stu-id="8719b-140">These flags used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="8719b-141">Per un elenco dei flag, vedere [costanti degli effetti (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8719b-141">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="8719b-142">Verifica degli errori</span><span class="sxs-lookup"><span data-stu-id="8719b-142">Checking Errors</span></span>

<span data-ttu-id="8719b-143">Se durante la compilazione si verifica un errore, l'API restituisce un'interfaccia che contiene gli errori restituiti dal compilatore di effetti.</span><span class="sxs-lookup"><span data-stu-id="8719b-143">If during compilation, an error occurs, the API returns an interface which contains the errors returned from the effect compiler.</span></span> <span data-ttu-id="8719b-144">Questa interfaccia è denominata ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="8719b-144">This interface is called ID3D10Blob.</span></span> <span data-ttu-id="8719b-145">Tuttavia, non è direttamente leggibile, restituendo un puntatore al buffer che contiene i dati (ovvero una stringa), è possibile visualizzare gli eventuali errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="8719b-145">It is not directly readable, however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="8719b-146">In questo esempio è stato introdotto un errore nell'effetto BasicHLSL. FX copiando la prima dichiarazione di variabile due volte.</span><span class="sxs-lookup"><span data-stu-id="8719b-146">In this example, an error was introduced into the BasicHLSL.fx effect by copying the first variable declaration twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="8719b-147">Questo errore ha impedito al compilatore di restituire l'errore seguente, come illustrato nello screenshot seguente della finestra espressioni di controllo in Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8719b-147">This error caused the compiler to return the following error, as shown in the following screen shot of the watch window in Microsoft Visual Studio.</span></span>

![screenshot della finestra espressioni di controllo di Visual Studio](images/effect-compile-errors-2.jpg)

<span data-ttu-id="8719b-149&quot;>Poiché l'errore viene restituito in un puntatore LPVOID, eseguirne il cast in una stringa di caratteri nella finestra espressioni di controllo.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8719b-149&quot;>Since the error is returned in a LPVOID pointer, cast it to a character string in the watch window.</span></span>

<span data-ttu-id=&quot;8719b-150&quot;>Di seguito è riportato il codice utilizzato per restituire l'errore dalla compilazione non riuscita.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8719b-150&quot;>Here is the code used to return the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L&quot;BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="8719b-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8719b-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8719b-152">Rendering di un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8719b-152">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



