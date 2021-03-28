---
title: Riferimento per HLSL
description: La documentazione di riferimento di HLSL specifica le caratteristiche del linguaggio. È suddiviso in diverse sezioni.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045101"
---
# <a name="reference-for-hlsl"></a><span data-ttu-id="73879-104">Riferimento per HLSL</span><span class="sxs-lookup"><span data-stu-id="73879-104">Reference for HLSL</span></span>

<span data-ttu-id="73879-105">La documentazione di riferimento di HLSL specifica le caratteristiche del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="73879-105">The HLSL reference documentation specifies the language characteristics.</span></span> <span data-ttu-id="73879-106">È suddiviso in diverse sezioni.</span><span class="sxs-lookup"><span data-stu-id="73879-106">It is broken into several sections.</span></span>

-   <span data-ttu-id="73879-107">[Sintassi del linguaggio (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) : per la programmazione di shader in HLSL è necessario comprendere la sintassi del linguaggio, ovvero la modalità di scrittura del codice HLSL.</span><span class="sxs-lookup"><span data-stu-id="73879-107">[Language Syntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) - Programming shaders in HLSL requires that you understand the language syntax, that is, how you write HLSL code.</span></span> <span data-ttu-id="73879-108">Questo include il codice per dichiarare e inizializzare variabili, scrivere funzioni shader definite dall'utente e aggiungere istruzioni di controllo di flusso per rendere le funzioni più potenti.</span><span class="sxs-lookup"><span data-stu-id="73879-108">This includes code to declare and initialize variables, write user-defined shader functions, and add flow control statements to make your functions more powerful.</span></span>
-   <span data-ttu-id="73879-109">[Modelli shader rispetto ai profili shader](dx-graphics-hlsl-models.md) : il compilatore HLSL implementa regole e restrizioni in base ai modelli shader.</span><span class="sxs-lookup"><span data-stu-id="73879-109">[Shader Models vs Shader Profiles](dx-graphics-hlsl-models.md) - The HLSL compiler implements rules and restrictions based on shader models.</span></span> <span data-ttu-id="73879-110">Il codice in ogni vertex shader, geometry shader (se si utilizza Direct3D 10) e pixel shader vengono convalidati in base a un modello di shader, fornito in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="73879-110">The code in each vertex shader, geometry shader (if you are using Direct3D 10) and pixel shader are validated against a shader model, which you supply at compile time.</span></span>
-   <span data-ttu-id="73879-111">[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) -HLSL ha molte funzioni intrinseche.</span><span class="sxs-lookup"><span data-stu-id="73879-111">[**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) - HLSL has many intrinsic functions.</span></span> <span data-ttu-id="73879-112">Vengono implementati e testati in modo che sia possibile utilizzarli sapendo che sono già sottoposti a debug e che offrono prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="73879-112">These are implemented and tested so that you can use them knowing that they are already debugged and they perform well.</span></span> <span data-ttu-id="73879-113">Se si sceglie di scrivere funzioni personalizzate, vedere la sezione relativa alla sintassi del linguaggio per la scrittura di funzioni definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="73879-113">If you choose to write your own functions, see the language syntax section for writing user-defined functions.</span></span>
-   <span data-ttu-id="73879-114">Informazioni di [riferimento su ASM shader](dx9-graphics-reference-asm.md) : istruzioni per gli assembly che è possibile usare per programmare ed eseguire il debug degli shader.</span><span class="sxs-lookup"><span data-stu-id="73879-114">[Asm Shader Reference](dx9-graphics-reference-asm.md) - Assembly instructions that you can use to program and debug shaders.</span></span>
-   <span data-ttu-id="73879-115">[Riferimento a D3DCompiler](dx-graphics-d3dcompiler-reference.md) : compila l'origine HLSL non elaborata.</span><span class="sxs-lookup"><span data-stu-id="73879-115">[D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) - Compiles raw HLSL source.</span></span>
-   <span data-ttu-id="73879-116">[Riferimenti per la conversione di formato inline](inline-format-conversion-reference.md) : il \_ file D3DX DXGIFormatConvert. inl contiene funzioni di conversione di formato inline che è possibile usare in compute shader o pixel shader su hardware Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="73879-116">[Inline Format Conversion Reference](inline-format-conversion-reference.md) - The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="73879-117">È possibile usare queste funzioni nell'applicazione per eseguire contemporaneamente la lettura e la scrittura in una trama.</span><span class="sxs-lookup"><span data-stu-id="73879-117">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="73879-118">Ovvero, è possibile eseguire la modifica dell'immagine sul posto.</span><span class="sxs-lookup"><span data-stu-id="73879-118">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="73879-119">Per usare queste funzioni di conversione del formato inline, includere il \_ file D3DX DXGIFormatConvert. inl nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73879-119">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>
-   <span data-ttu-id="73879-120">[Appendice (DirectX HLSL)](dx-graphics-hlsl-appendix.md) : l'appendice è inclusa per completezza.</span><span class="sxs-lookup"><span data-stu-id="73879-120">[Appendix (DirectX HLSL)](dx-graphics-hlsl-appendix.md) - The appendix is included for completeness.</span></span> <span data-ttu-id="73879-121">Include un elenco delle parole chiave e delle parole riservate. queste parole non possono essere usate come identificatori nei programmi.</span><span class="sxs-lookup"><span data-stu-id="73879-121">It includes a listing of the keywords and reserved words; these words cannot be used as identifiers in your programs.</span></span> <span data-ttu-id="73879-122">Include inoltre un elenco della grammatica del linguaggio per riferimento.</span><span class="sxs-lookup"><span data-stu-id="73879-122">It also includes a listing of the language grammar for reference.</span></span>
-   <span data-ttu-id="73879-123">[**Errori e avvisi di HLSL**](hlsl-errors-and-warnings.md) : fornisce codici di errore e di avviso che possono essere restituiti da uno shader.</span><span class="sxs-lookup"><span data-stu-id="73879-123">[**HLSL errors and warnings**](hlsl-errors-and-warnings.md) - Provides error and warning codes that a shader can return.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73879-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73879-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73879-125">HLSL</span><span class="sxs-lookup"><span data-stu-id="73879-125">HLSL</span></span>](dx-graphics-hlsl.md)
</dt> <dt>

[<span data-ttu-id="73879-126">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="73879-126">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




