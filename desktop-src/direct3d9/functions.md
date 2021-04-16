---
description: Una funzione è il blocco predefinito per uno shader creato nel linguaggio di alto livello. Se si preferisce scrivere shader in un linguaggio di tipo C anziché in un linguaggio assembly, è opportuno scrivere funzioni.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintassi della funzione Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520906"
---
# <a name="effect-function-syntax-direct3d-9"></a><span data-ttu-id="08b80-104">Sintassi della funzione Effect (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="08b80-104">Effect Function Syntax (Direct3D 9)</span></span>

<span data-ttu-id="08b80-105">Una funzione è il blocco predefinito per uno shader creato nel linguaggio di alto livello.</span><span class="sxs-lookup"><span data-stu-id="08b80-105">A function is the building block for a shader created in the high-level language.</span></span> <span data-ttu-id="08b80-106">Se si preferisce scrivere shader in un linguaggio di tipo C anziché in un linguaggio assembly, è opportuno scrivere funzioni.</span><span class="sxs-lookup"><span data-stu-id="08b80-106">If you prefer to write shaders in a C-style language instead of in assembly language, you will want to write functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b80-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08b80-107">Syntax</span></span>


```
type id ( [ parameters ] )  
    { body }
```



<span data-ttu-id="08b80-108">Le funzioni non modificano i valori dei parametri in un effetto.</span><span class="sxs-lookup"><span data-stu-id="08b80-108">Functions do not change parameter values in an effect.</span></span>

-   <span data-ttu-id="08b80-109">Type: qualsiasi [riferimento valido per](../direct3dhlsl/dx-graphics-hlsl-reference.md) il tipo HLSL.</span><span class="sxs-lookup"><span data-stu-id="08b80-109">type - Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span>
-   <span data-ttu-id="08b80-110">ID: nome univoco.</span><span class="sxs-lookup"><span data-stu-id="08b80-110">id - A unique name.</span></span>
-   <span data-ttu-id="08b80-111">Parameters-parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="08b80-111">parameters - Function parameters.</span></span>
-   <span data-ttu-id="08b80-112">Body: corpo della funzione.</span><span class="sxs-lookup"><span data-stu-id="08b80-112">body - The body of the function.</span></span>

<span data-ttu-id="08b80-113">Le funzioni sono compilate dal linguaggio di alto livello.</span><span class="sxs-lookup"><span data-stu-id="08b80-113">Functions are built from the high-level language.</span></span> <span data-ttu-id="08b80-114">Vedere informazioni [di riferimento per HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="08b80-114">See [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="08b80-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08b80-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08b80-116">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="08b80-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
