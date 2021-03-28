---
title: Compilare un effetto (Direct3D 11)
description: Dopo aver creato un effetto, il passaggio successivo consiste nel compilare il codice per verificare la presenza di problemi di sintassi.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963200"
---
# <a name="compile-an-effect-direct3d-11"></a><span data-ttu-id="b7e22-103">Compilare un effetto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="b7e22-103">Compile an Effect (Direct3D 11)</span></span>

<span data-ttu-id="b7e22-104">Dopo aver creato un effetto, il passaggio successivo consiste nel compilare il codice per verificare la presenza di problemi di sintassi.</span><span class="sxs-lookup"><span data-stu-id="b7e22-104">After an effect has been authored, the next step is to compile the code to check for syntax problems.</span></span>

<span data-ttu-id="b7e22-105">A tale scopo, chiamare una delle API di compilazione ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)o [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span><span class="sxs-lookup"><span data-stu-id="b7e22-105">You do so by calling one of the compile APIs ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md), or [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span></span> <span data-ttu-id="b7e22-106">Queste API richiamano l'effetto del compilatore fxc.exe, che compila il codice HLSL.</span><span class="sxs-lookup"><span data-stu-id="b7e22-106">These APIs invoke the effect compiler fxc.exe, which compiles HLSL code.</span></span> <span data-ttu-id="b7e22-107">Questo è il motivo per cui la sintassi per il codice in un effetto è molto simile a quella del codice HLSL.</span><span class="sxs-lookup"><span data-stu-id="b7e22-107">This is why the syntax for code in an effect looks very much like HLSL code.</span></span> <span data-ttu-id="b7e22-108">(Ci sono alcune eccezioni che verranno gestite successivamente).</span><span class="sxs-lookup"><span data-stu-id="b7e22-108">(There are a few exceptions that will be handled later).</span></span> <span data-ttu-id="b7e22-109">Il compilatore compilatore/HLSL di effetti, fxc.exe, è disponibile nell'SDK nella cartella Utilities, in modo che gli shader (o gli effetti) possano essere compilati offline se si sceglie.</span><span class="sxs-lookup"><span data-stu-id="b7e22-109">The effect compiler/hlsl compiler, fxc.exe, is available in the SDK in the utilities folder so that shaders (or effects) can be compiled offline if you choose.</span></span> <span data-ttu-id="b7e22-110">Vedere la documentazione per l'esecuzione del compilatore dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b7e22-110">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="b7e22-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="b7e22-111">Example</span></span>](#example)
-   [<span data-ttu-id="b7e22-112">Includes</span><span class="sxs-lookup"><span data-stu-id="b7e22-112">Includes</span></span>](#includes)
-   [<span data-ttu-id="b7e22-113">Ricerca di file di inclusione</span><span class="sxs-lookup"><span data-stu-id="b7e22-113">Searching for Include Files</span></span>](#searching-for-include-files)
-   [<span data-ttu-id="b7e22-114">Macro</span><span class="sxs-lookup"><span data-stu-id="b7e22-114">Macros</span></span>](#macros)
-   [<span data-ttu-id="b7e22-115">Flag shader HLSL</span><span class="sxs-lookup"><span data-stu-id="b7e22-115">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="b7e22-116">Flag FX</span><span class="sxs-lookup"><span data-stu-id="b7e22-116">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="b7e22-117">Verifica degli errori</span><span class="sxs-lookup"><span data-stu-id="b7e22-117">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="b7e22-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7e22-118">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="b7e22-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="b7e22-119">Example</span></span>

<span data-ttu-id="b7e22-120">Di seguito è riportato un esempio di compilazione di un file di effetti.</span><span class="sxs-lookup"><span data-stu-id="b7e22-120">Here's an example of compiling an effect file.</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a><span data-ttu-id="b7e22-121">Includes</span><span class="sxs-lookup"><span data-stu-id="b7e22-121">Includes</span></span>

<span data-ttu-id="b7e22-122">Un parametro delle API di compilazione è un'interfaccia di inclusione.</span><span class="sxs-lookup"><span data-stu-id="b7e22-122">One parameter of the compile APIs is an include interface.</span></span> <span data-ttu-id="b7e22-123">Generare uno di questi se si desidera includere un comportamento personalizzato quando il compilatore legge un file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="b7e22-123">Generate one of these if you want to include a customized behavior when the compiler reads an include file.</span></span> <span data-ttu-id="b7e22-124">Il compilatore esegue questo comportamento personalizzato ogni volta che crea o compila un effetto (che usa il puntatore di inclusione).</span><span class="sxs-lookup"><span data-stu-id="b7e22-124">The compiler executes this custom behavior each time it creates or compiles an effect (that uses the include pointer).</span></span> <span data-ttu-id="b7e22-125">Per implementare il comportamento di inclusione personalizzato, derivare una classe dall'interfaccia [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) .</span><span class="sxs-lookup"><span data-stu-id="b7e22-125">To implement customized include behavior, derive a class from the [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) interface.</span></span> <span data-ttu-id="b7e22-126">In questo modo viene fornita la classe con due metodi: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) e [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span><span class="sxs-lookup"><span data-stu-id="b7e22-126">This provides your class with two methods: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) and [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span></span> <span data-ttu-id="b7e22-127">Implementare il comportamento personalizzato in questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b7e22-127">Implement the custom behavior in these methods.</span></span>

## <a name="searching-for-include-files"></a><span data-ttu-id="b7e22-128">Ricerca di file di inclusione</span><span class="sxs-lookup"><span data-stu-id="b7e22-128">Searching for Include Files</span></span>

<span data-ttu-id="b7e22-129">Il puntatore passato dal compilatore nel parametro *pParentData* al metodo [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del gestore di inclusione potrebbe non puntare al contenitore che include il \# file di inclusione necessario al compilatore per compilare il codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="b7e22-129">The pointer that the compiler passes in the *pParentData* parameter to your include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method might not point to the container that includes the \#include file that the compiler needs to compile your shader code.</span></span> <span data-ttu-id="b7e22-130">Ovvero, il compilatore potrebbe passare **null** in *pParentData*.</span><span class="sxs-lookup"><span data-stu-id="b7e22-130">That is, the compiler might pass **NULL** in *pParentData*.</span></span> <span data-ttu-id="b7e22-131">Pertanto, è consigliabile che il gestore di inclusione cerchi un elenco di percorsi di inclusione per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="b7e22-131">Therefore, we recommend that your include handler search its own list of include locations for content.</span></span> <span data-ttu-id="b7e22-132">Il gestore di inclusione può aggiungere dinamicamente nuovi percorsi di inclusione poiché riceve tali percorsi nelle chiamate al metodo **Open** .</span><span class="sxs-lookup"><span data-stu-id="b7e22-132">Your include handler can dynamically add new include locations as it receives those locations in calls to its **Open** method.</span></span>

<span data-ttu-id="b7e22-133">Nell'esempio seguente si supponga che i file di inclusione del codice dello shader siano entrambi archiviati nella directory *somewhereelse*</span><span class="sxs-lookup"><span data-stu-id="b7e22-133">In the following example, suppose that the shader code's include files are both stored in the *somewhereelse* directory.</span></span> <span data-ttu-id="b7e22-134">Quando il compilatore chiama il metodo [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del gestore di inclusione per aprire e leggere il contenuto di *somewhereelse \\ foo. h*, il gestore di inclusione può salvare il percorso della directory **somewhereelse** .</span><span class="sxs-lookup"><span data-stu-id="b7e22-134">When the compiler calls the include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method to open and read the contents of *somewhereelse\\foo.h*, the include handler can save the location of the **somewhereelse** directory.</span></span> <span data-ttu-id="b7e22-135">Successivamente, quando il compilatore chiama il metodo **Open** del gestore di inclusione per aprire e leggere il contenuto di *bar. h*, il gestore di inclusione può eseguire automaticamente la ricerca nella directory *somewhereelse* per *barra. h*.</span><span class="sxs-lookup"><span data-stu-id="b7e22-135">Later, when the compiler calls the include handler's **Open** method to open and read the contents of *bar.h*, the include handler can automatically search in the *somewhereelse* directory for *bar.h*.</span></span>


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a><span data-ttu-id="b7e22-136">Macro</span><span class="sxs-lookup"><span data-stu-id="b7e22-136">Macros</span></span>

<span data-ttu-id="b7e22-137">La compilazione degli effetti può anche portare un puntatore a macro definite altrove.</span><span class="sxs-lookup"><span data-stu-id="b7e22-137">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="b7e22-138">Si supponga, ad esempio, di voler modificare l'effetto in BasicHLSL10 per usare due macro: zero e uno.</span><span class="sxs-lookup"><span data-stu-id="b7e22-138">For example, suppose you want to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="b7e22-139">Il codice di effetto che usa le due macro è illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b7e22-139">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="b7e22-140">Di seguito è illustrata la dichiarazione per le due macro.</span><span class="sxs-lookup"><span data-stu-id="b7e22-140">Here is the declaration for the two macros.</span></span>


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="b7e22-141">Le macro sono una matrice con terminazione NULL di macro. dove ogni macro viene definita utilizzando uno struct [**della \_ \_ macro dello shader D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="b7e22-141">The macros are a NULL-terminated array of macros; where each macro is defined by using a [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="b7e22-142">Modificare la chiamata dell'effetto di compilazione per portare un puntatore alle macro.</span><span class="sxs-lookup"><span data-stu-id="b7e22-142">Modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="b7e22-143">Flag shader HLSL</span><span class="sxs-lookup"><span data-stu-id="b7e22-143">HLSL Shader Flags</span></span>

<span data-ttu-id="b7e22-144">I flag shader specificano i vincoli dello shader per il compilatore HLSL.</span><span class="sxs-lookup"><span data-stu-id="b7e22-144">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="b7e22-145">Questi flag influiscono sul codice generato dal compilatore shader nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7e22-145">These flags affect the code generated by the shader compiler in the following ways:</span></span>

-   <span data-ttu-id="b7e22-146">Ottimizzare le dimensioni del codice.</span><span class="sxs-lookup"><span data-stu-id="b7e22-146">Optimize the code size.</span></span>
-   <span data-ttu-id="b7e22-147">Inclusione di informazioni di debug, che impedisce il controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="b7e22-147">Including debug information, which prevents flow control.</span></span>
-   <span data-ttu-id="b7e22-148">Influiscono sulla destinazione di compilazione e sul fatto che uno shader possa essere eseguito su hardware legacy.</span><span class="sxs-lookup"><span data-stu-id="b7e22-148">Affects the compile target and whether a shader can run on legacy hardware.</span></span>

<span data-ttu-id="b7e22-149">Questi flag possono essere combinati logicamente se non sono state specificate due caratteristiche in conflitto.</span><span class="sxs-lookup"><span data-stu-id="b7e22-149">These flags can be logically combined if you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="b7e22-150">Per un elenco dei flag, vedere [ \_ costanti shader D3D10](/windows/desktop/direct3d10/d3d10-shader).</span><span class="sxs-lookup"><span data-stu-id="b7e22-150">For a listing of the flags see [D3D10\_SHADER Constants](/windows/desktop/direct3d10/d3d10-shader).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="b7e22-151">Flag FX</span><span class="sxs-lookup"><span data-stu-id="b7e22-151">FX Flags</span></span>

<span data-ttu-id="b7e22-152">Usare questi flag quando si crea un effetto per definire il comportamento di compilazione o l'effetto di Runtime.</span><span class="sxs-lookup"><span data-stu-id="b7e22-152">Use these flags when you create an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="b7e22-153">Per un elenco dei flag, vedere [ \_ costanti degli effetti D3D10](/windows/desktop/direct3d10/d3d10-effect).</span><span class="sxs-lookup"><span data-stu-id="b7e22-153">For a listing of the flags see [D3D10\_EFFECT Constants](/windows/desktop/direct3d10/d3d10-effect).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="b7e22-154">Verifica degli errori</span><span class="sxs-lookup"><span data-stu-id="b7e22-154">Checking Errors</span></span>

<span data-ttu-id="b7e22-155">Se durante la compilazione si verifica un errore, l'API restituisce un'interfaccia che contiene gli errori del compilatore di effetti.</span><span class="sxs-lookup"><span data-stu-id="b7e22-155">If during compilation an error occurs, the API returns an interface that contains the errors from the effect compiler.</span></span> <span data-ttu-id="b7e22-156">Questa interfaccia è denominata [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7e22-156">This interface is called [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span></span> <span data-ttu-id="b7e22-157">Non è leggibile direttamente; Tuttavia, restituendo un puntatore al buffer che contiene i dati (ovvero una stringa), è possibile visualizzare gli eventuali errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="b7e22-157">It is not directly readable; however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="b7e22-158">Questo esempio contiene un errore in BasicHLSL. FX, la prima dichiarazione di variabile si verifica due volte.</span><span class="sxs-lookup"><span data-stu-id="b7e22-158">This example contains an error in the BasicHLSL.fx, the first variable declaration occurs twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="b7e22-159">Questo errore induce il compilatore a restituire l'errore seguente, come illustrato nello screenshot seguente del finestra Espressioni di controllo in Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b7e22-159">This error causes the compiler to return the following error, as shown in the following screen shot of the Watch window in Microsoft Visual Studio.</span></span>

![screenshot della finestra espressioni di controllo di Visual Studio con un errore 0x01997fb8](images/effect-compile-errors-2.jpg)

<span data-ttu-id="b7e22-161">Poiché il compilatore restituisce l'errore in un puntatore LPVOID, eseguirne il cast in una stringa di caratteri nell'finestra Espressioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="b7e22-161">Because the compiler returns the error in a LPVOID pointer, cast it to a character string in the Watch window.</span></span>

<span data-ttu-id="b7e22-162">Ecco il codice che restituisce l'errore dalla compilazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="b7e22-162">Here is the code that returns the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="b7e22-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7e22-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7e22-164">Rendering di un effetto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="b7e22-164">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 