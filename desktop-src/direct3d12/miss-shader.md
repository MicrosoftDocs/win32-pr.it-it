---
description: Shader richiamato quando non vengono rilevate o accettate intersezioni di raggio.
ms.assetid: ''
title: Lo shader manca
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: fe8e2ec9cdbb8ef7567b9327ae5af1128597a601
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305246"
---
# <a name="miss-shader"></a><span data-ttu-id="c6ddd-103">Lo shader manca</span><span class="sxs-lookup"><span data-stu-id="c6ddd-103">Miss Shader</span></span>

<span data-ttu-id="c6ddd-104">Shader richiamato quando non vengono rilevate o accettate intersezioni di raggio.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-104">A shader that is invoked when no ray intersections are found or accepted.</span></span> <span data-ttu-id="c6ddd-105">Questa operazione è utile per l'ombreggiatura di background o Sky.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-105">This is useful for background or sky shading.</span></span>  <span data-ttu-id="c6ddd-106">Lo shader mancante può usare [**CallShader**](callshader-function.md) e **TraceRay** per pianificare altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-106">The miss shader may use [**CallShader**](callshader-function.md) and **TraceRay** to schedule more work.</span></span>

<span data-ttu-id="c6ddd-107">Il mancato shader deve includere un parametro di payload tipizzato della struttura definito dall'utente corrispondente a quello fornito a [**TraceRay**](traceray-function.md).</span><span class="sxs-lookup"><span data-stu-id="c6ddd-107">The miss shader must include a user-defined structure typed payload parameter matching the one supplied to [**TraceRay**](traceray-function.md).</span></span>


## <a name="shader-type-attribute"></a><span data-ttu-id="c6ddd-108">Attributo di tipo shader</span><span class="sxs-lookup"><span data-stu-id="c6ddd-108">Shader Type attribute</span></span>


```
[shader("miss")]
```



## <a name="example"></a><span data-ttu-id="c6ddd-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="c6ddd-109">Example</span></span>

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




