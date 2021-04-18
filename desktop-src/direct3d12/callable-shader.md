---
description: Shader richiamato da un altro shader con la funzione intrinseca CallShader.
ms.assetid: ''
title: Richiamabile shader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: 65df547c5e40a46cc4c35361b88ceb797c2e8852
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304595"
---
# <a name="callable-shader"></a><span data-ttu-id="ef7a2-103">Richiamabile shader</span><span class="sxs-lookup"><span data-stu-id="ef7a2-103">Callable Shader</span></span>

<span data-ttu-id="ef7a2-104">Shader richiamato da un altro shader con la funzione intrinseca [**CallShader**](callshader-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ef7a2-104">A shader that is invoked from another shader with the [**CallShader**](callshader-function.md) intrinsic.</span></span>

<span data-ttu-id="ef7a2-105">Nel sito di chiamata **CallShader** è presente una struttura di parametri che deve corrispondere alla struttura del parametro utilizzata nello shader chiamabile a cui fa riferimento l'indice richiesto nella tabella shader chiamabile fornita tramite il metodo [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .</span><span class="sxs-lookup"><span data-stu-id="ef7a2-105">There is a parameter structure supplied at the **CallShader** call site that must match the parameter structure used in the callable shader pointed to by the requested index into the callable shader table supplied through the [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) method.</span></span>  <span data-ttu-id="ef7a2-106">Lo shader chiamabile deve dichiarare questo parametro come *InOut*.</span><span class="sxs-lookup"><span data-stu-id="ef7a2-106">The callable shader must declare this parameter as *inout*.</span></span>  <span data-ttu-id="ef7a2-107">Inoltre, il Callable shader può leggere gli input dell'indice di avvio e della dimensione.</span><span class="sxs-lookup"><span data-stu-id="ef7a2-107">Additionally, the callable shader may read launch index and dimension inputs.</span></span> <span data-ttu-id="ef7a2-108">Per ulteriori informazioni, vedere [**intrinseci dei valori di sistema**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span><span class="sxs-lookup"><span data-stu-id="ef7a2-108">For more information, see [**System Value Intrinsics**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span></span> 


## <a name="shader-type-attribute"></a><span data-ttu-id="ef7a2-109">Attributo di tipo shader</span><span class="sxs-lookup"><span data-stu-id="ef7a2-109">Shader Type attribute</span></span>


```
[shader("callable")]
```



## <a name="example"></a><span data-ttu-id="ef7a2-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="ef7a2-110">Example</span></span>

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




