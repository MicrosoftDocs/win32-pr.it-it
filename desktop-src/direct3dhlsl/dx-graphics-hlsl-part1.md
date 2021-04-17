---
title: Compilazione di shader
description: Verranno ora esaminati i vari modi per compilare il codice e le convenzioni dello shader per le estensioni di file per il codice dello shader.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337998"
---
# <a name="compiling-shaders"></a><span data-ttu-id="23be2-103">Compilazione di shader</span><span class="sxs-lookup"><span data-stu-id="23be2-103">Compiling shaders</span></span>

> [!NOTE]
> <span data-ttu-id="23be2-104">Questo argomento descrive il `FXC.EXE` compilatore usato per i modelli shader da 2 a 5,1.</span><span class="sxs-lookup"><span data-stu-id="23be2-104">This topic covers the `FXC.EXE` compiler used for Shader Models 2 through 5.1.</span></span> <span data-ttu-id="23be2-105">Per il modello di shader 6, usare `DXC.EXE` invece, che è documentato in [uso di dxc.exe e dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span><span class="sxs-lookup"><span data-stu-id="23be2-105">For Shader Model 6, you use `DXC.EXE` instead, which is documented in [Using dxc.exe and dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span></span>

<span data-ttu-id="23be2-106">Microsoft Visual Studio 2012 ora può compilare il codice dello shader dai \* file HLSL inclusi nel progetto C++.</span><span class="sxs-lookup"><span data-stu-id="23be2-106">Microsoft Visual Studio 2012 can now compile shader code from \*.hlsl files that you include in your C++ project.</span></span>

<span data-ttu-id="23be2-107">Come parte del processo di compilazione, Visual Studio 2012 USA il compilatore di codice [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL per compilare i file con estensione HLSL in file oggetto shader binari o in matrici di byte definite nei file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="23be2-107">As part of the build process, Visual Studio 2012 uses the [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL code compiler to compile the .hlsl files into binary shader object files or into byte arrays that are defined in header files.</span></span> <span data-ttu-id="23be2-108">Il modo in cui il compilatore di codice HLSL compila ogni file con estensione HLSL nel progetto dipende dalla modalità con cui si specifica la proprietà dei **file ouput** per il file.</span><span class="sxs-lookup"><span data-stu-id="23be2-108">How the HLSL code compiler compiles each .hlsl file in your project depends on how you specify the **Ouput Files** property for that file.</span></span> <span data-ttu-id="23be2-109">Per altre informazioni sulle pagine delle proprietà di HLSL, vedere [pagine delle proprietà di HLSL](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span><span class="sxs-lookup"><span data-stu-id="23be2-109">For more info about HLSL property pages, see [HLSL Property Pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span></span>

<span data-ttu-id="23be2-110">Il metodo Compile usato in genere dipende dalle dimensioni del \* file con estensione HLSL.</span><span class="sxs-lookup"><span data-stu-id="23be2-110">The compile method that you use typically depends on the size of your \*.hlsl file.</span></span> <span data-ttu-id="23be2-111">Se si include una grande quantità di codice byte in un'intestazione, si aumentano le dimensioni e il tempo di caricamento iniziale dell'app.</span><span class="sxs-lookup"><span data-stu-id="23be2-111">If you include a large amount of byte code in a header, you increase the size and the initial load time of your app.</span></span> <span data-ttu-id="23be2-112">Si impone anche che tutto il codice byte risieda in memoria anche dopo la creazione dello shader, che spreca le risorse.</span><span class="sxs-lookup"><span data-stu-id="23be2-112">You also force all byte code to reside in memory even after the shader is created, which wastes resources.</span></span> <span data-ttu-id="23be2-113">Tuttavia, quando si include il codice byte in un'intestazione, è possibile ridurre la complessità del codice e semplificare la creazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="23be2-113">But when you include byte code in a header, you can reduce code complexity and simplify shader creation.</span></span>

<span data-ttu-id="23be2-114">Verranno ora esaminati i vari modi per compilare il codice e le convenzioni dello shader per le estensioni di file per il codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="23be2-114">Let's now look at various ways to compile your shader code and conventions for file extensions for shader code.</span></span>

-   [<span data-ttu-id="23be2-115">Uso delle estensioni di file di codice dello shader</span><span class="sxs-lookup"><span data-stu-id="23be2-115">Using shader code file extensions</span></span>](#using-shader-code-file-extensions)
-   [<span data-ttu-id="23be2-116">Compilazione in fase di compilazione in file oggetto</span><span class="sxs-lookup"><span data-stu-id="23be2-116">Compiling at build time to object files</span></span>](#compiling-at-build-time-to-object-files)
-   [<span data-ttu-id="23be2-117">Compilazione in fase di compilazione in file di intestazione</span><span class="sxs-lookup"><span data-stu-id="23be2-117">Compiling at build time to header files</span></span>](#compiling-at-build-time-to-header-files)
-   [<span data-ttu-id="23be2-118">Compilazione con D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="23be2-118">Compiling with D3DCompileFromFile</span></span>](#compiling-with-d3dcompilefromfile)
-   [<span data-ttu-id="23be2-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23be2-119">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="23be2-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23be2-120">Related topics</span></span>](#related-topics)

## <a name="using-shader-code-file-extensions"></a><span data-ttu-id="23be2-121">Uso delle estensioni di file di codice dello shader</span><span class="sxs-lookup"><span data-stu-id="23be2-121">Using shader code file extensions</span></span>

<span data-ttu-id="23be2-122">Per conformarsi alla convenzione Microsoft, usare le estensioni di file seguenti per il codice dello shader:</span><span class="sxs-lookup"><span data-stu-id="23be2-122">To conform to Microsoft convention, use these file extensions for your shader code:</span></span>

-   <span data-ttu-id="23be2-123">Un file con estensione HLSL include il codice sorgente[HLSL](dx-graphics-hlsl-reference.md)(High Level Shading Language).</span><span class="sxs-lookup"><span data-stu-id="23be2-123">A file with the .hlsl extension holds High Level Shading Language ([HLSL](dx-graphics-hlsl-reference.md)) source code.</span></span>
-   <span data-ttu-id="23be2-124">Un file con estensione CSO include un oggetto shader compilato.</span><span class="sxs-lookup"><span data-stu-id="23be2-124">A file with the .cso extension holds a compiled shader object.</span></span>
-   <span data-ttu-id="23be2-125">Un file con estensione h è un file di intestazione, ma in un contesto di codice dello shader questo file di intestazione definisce una matrice di byte che include i dati dello shader.</span><span class="sxs-lookup"><span data-stu-id="23be2-125">A file with the .h extension is a header file, but in a shader code context, this header file defines a byte array that holds shader data.</span></span>

## <a name="compiling-at-build-time-to-object-files"></a><span data-ttu-id="23be2-126">Compilazione in fase di compilazione in file oggetto</span><span class="sxs-lookup"><span data-stu-id="23be2-126">Compiling at build time to object files</span></span>

<span data-ttu-id="23be2-127">Se si compilano i file con estensione HLSL in file oggetto shader binari, l'app deve leggere i dati dei file oggetto (. CSO è l'estensione predefinita per questi file oggetto), assegnare i dati a matrici di byte e creare oggetti shader da tali matrici di byte.</span><span class="sxs-lookup"><span data-stu-id="23be2-127">If you compile your .hlsl files into binary shader object files, your app needs to read the data from those object files (.cso is the default extension for these object files), assign the data to byte arrays, and create shader objects from those byte arrays.</span></span> <span data-ttu-id="23be2-128">Per creare, ad esempio, un vertex shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), chiamare il metodo [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) con una matrice di byte che contiene il codice byte del vertex shader compilato.</span><span class="sxs-lookup"><span data-stu-id="23be2-128">For example, to create a vertex shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)\*\*), call the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method with a byte array that contains compiled vertex shader byte code.</span></span> <span data-ttu-id="23be2-129">Nell' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) viene illustrato come creare oggetti shader da matrici di byte ottenute da file oggetto shader binari. cso.</span><span class="sxs-lookup"><span data-stu-id="23be2-129">The [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) shows how to create shader objects from byte arrays that it obtained from .cso binary shader object files.</span></span> <span data-ttu-id="23be2-130">In questo esempio di codice dell' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), la proprietà **file ouput** per il file SimpleVertexShader. HLSL specifica di compilare il file oggetto SimpleVertexShader. cso.</span><span class="sxs-lookup"><span data-stu-id="23be2-130">In this example code from the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), the **Ouput Files** property for the SimpleVertexShader.hlsl file specifies to compile into the SimpleVertexShader.cso object file.</span></span>

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a><span data-ttu-id="23be2-131">Compilazione in fase di compilazione in file di intestazione</span><span class="sxs-lookup"><span data-stu-id="23be2-131">Compiling at build time to header files</span></span>

<span data-ttu-id="23be2-132">Se si compilano i file con estensione HLSL in matrici di byte definite nei file di intestazione, è necessario includere i file di intestazione nel codice.</span><span class="sxs-lookup"><span data-stu-id="23be2-132">If you compile your .hlsl files into byte arrays that are defined in header files, you need to include those header files in your code.</span></span> <span data-ttu-id="23be2-133">L' [esempio Media Extensions](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) Mostra come creare oggetti shader dalle matrici di byte definite nei file di intestazione e da includere nel progetto in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="23be2-133">The [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) shows how to create shader objects from byte arrays that are defined in header files and that you include in your project at compile time.</span></span> <span data-ttu-id="23be2-134">In questo esempio di codice dell' [esempio Media Extensions](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)la proprietà **file ouput** per il file PixelShader. HLSL specifica di compilare la matrice di byte *g \_ Psshader* definita nel file di intestazione PixelShader. h.</span><span class="sxs-lookup"><span data-stu-id="23be2-134">In this example code from the [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), the **Ouput Files** property for the PixelShader.hlsl file specifies to compile into the *g\_psshader* byte array that is defined in the PixelShader.h header file.</span></span>


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a><span data-ttu-id="23be2-135">Compilazione con D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="23be2-135">Compiling with D3DCompileFromFile</span></span>

<span data-ttu-id="23be2-136">È anche possibile usare la funzione [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) in fase di esecuzione per compilare il codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="23be2-136">You can also use the [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function at run time to compile shader code.</span></span> <span data-ttu-id="23be2-137">Per altre informazioni su come eseguire questa operazione, vedere [procedura: compilare uno shader](/windows/desktop/direct3d11/how-to--compile-a-shader).</span><span class="sxs-lookup"><span data-stu-id="23be2-137">For more info about how to do this, see [How To: Compile a Shader](/windows/desktop/direct3d11/how-to--compile-a-shader).</span></span>

> [!Note]  
> <span data-ttu-id="23be2-138">Le app di Windows Store supportano l'uso di [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) per lo sviluppo, ma non per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="23be2-138">Windows Store apps support using [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) for development but not for deployment.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="23be2-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23be2-139">Related Topics</span></span>

[<span data-ttu-id="23be2-140">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="23be2-140">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="23be2-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23be2-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23be2-142">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="23be2-142">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 