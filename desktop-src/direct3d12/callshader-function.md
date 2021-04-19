---
description: Richiama un altro shader dall'interno di uno shader.
ms.assetid: ''
title: CallShader (funzione)
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304707"
---
# <a name="callshader-function"></a><span data-ttu-id="404c8-103">CallShader (funzione)</span><span class="sxs-lookup"><span data-stu-id="404c8-103">CallShader function</span></span>

<span data-ttu-id="404c8-104">Richiama un altro shader dall'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="404c8-104">Invokes another shader from within a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="404c8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="404c8-105">Syntax</span></span>
<span data-ttu-id="404c8-106">Questa definizione di funzione intrinseca è equivalente al modello di funzione seguente:</span><span class="sxs-lookup"><span data-stu-id="404c8-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a><span data-ttu-id="404c8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="404c8-107">Parameters</span></span>

`ShaderIndex`

<span data-ttu-id="404c8-108">Unsigned Integer che rappresenta l'indice nella tabella [shader chiamabile](callable-shader.md) specificata nella chiamata a [**DispatchRays**] (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.</span><span class="sxs-lookup"><span data-stu-id="404c8-108">An unsigned integer representing the index into the [callable shader](callable-shader.md) table specified in the call to [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.</span></span>

`Parameter`

<span data-ttu-id="404c8-109">Parametri definiti dall'utente da passare allo shader chiamabile.</span><span class="sxs-lookup"><span data-stu-id="404c8-109">The user-defined parameters to pass to the callable shader.</span></span>  <span data-ttu-id="404c8-110">Questa struttura di parametri deve corrispondere alla struttura del parametro utilizzata nello shader chiamabile a cui punta la tabella shader.</span><span class="sxs-lookup"><span data-stu-id="404c8-110">This parameter structure must match the parameter structure used in the callable shader pointed to in the shader table.</span></span>


## <a name="return-value"></a><span data-ttu-id="404c8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="404c8-111">Return Value</span></span>

<span data-ttu-id="404c8-112">**void**</span><span class="sxs-lookup"><span data-stu-id="404c8-112">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="404c8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="404c8-113">Remarks</span></span>

<span data-ttu-id="404c8-114">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="404c8-114">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="404c8-115">**Richiamabile shader**</span><span class="sxs-lookup"><span data-stu-id="404c8-115">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="404c8-116">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="404c8-116">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="404c8-117">**Lo shader manca**</span><span class="sxs-lookup"><span data-stu-id="404c8-117">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="404c8-118">**Shader di generazione del Ray**</span><span class="sxs-lookup"><span data-stu-id="404c8-118">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="404c8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="404c8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="404c8-120">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="404c8-120">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




