---
title: Shader HLSL raytracing Direct3D 12
description: Gli shader HLSL seguenti supportano la pipeline raytracing di Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300884"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="e2b51-103">Shader HLSL raytracing Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e2b51-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="e2b51-104">Gli shader HLSL seguenti supportano la pipeline raytracing di Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e2b51-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="e2b51-105">Questi shader sono funzioni compilate in una libreria, con il modello di destinazione lib_6_3 e identificati da un attributo *[shader ("shadertype")]* nella funzione shader.</span><span class="sxs-lookup"><span data-stu-id="e2b51-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="e2b51-106">Vedere elementi **intrinseci** e **valori di sistema** per vedere cosa è consentito per ogni tipo di shader.</span><span class="sxs-lookup"><span data-stu-id="e2b51-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e2b51-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e2b51-107">In this section</span></span>



| <span data-ttu-id="e2b51-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="e2b51-108">Topic</span></span>                                                                                                       | <span data-ttu-id="e2b51-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2b51-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2b51-110">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="e2b51-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="e2b51-111">Shader richiamato quando le intersezioni del raggio non sono opache.</span><span class="sxs-lookup"><span data-stu-id="e2b51-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e2b51-112">**Richiamabile shader**</span><span class="sxs-lookup"><span data-stu-id="e2b51-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="e2b51-113">Shader richiamato da un altro shader con la funzione intrinseca **CallShader** .</span><span class="sxs-lookup"><span data-stu-id="e2b51-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e2b51-114">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="e2b51-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="e2b51-115">Uno shader che viene richiamato quando è abilitato e l'hit più vicino è stato determinato o la ricerca di intersezione del raggio è terminata.</span><span class="sxs-lookup"><span data-stu-id="e2b51-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e2b51-116">**Intersezione shader**</span><span class="sxs-lookup"><span data-stu-id="e2b51-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="e2b51-117">Shader utilizzato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di delimitazione).</span><span class="sxs-lookup"><span data-stu-id="e2b51-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e2b51-118">**Lo shader manca**</span><span class="sxs-lookup"><span data-stu-id="e2b51-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="e2b51-119">Shader richiamato quando non vengono rilevate o accettate intersezioni di raggio.</span><span class="sxs-lookup"><span data-stu-id="e2b51-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e2b51-120">**Shader di generazione del Ray**</span><span class="sxs-lookup"><span data-stu-id="e2b51-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="e2b51-121">Shader che chiama [**TraceRay**](traceray-function.md) per generare raggi.</span><span class="sxs-lookup"><span data-stu-id="e2b51-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="e2b51-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2b51-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2b51-123">Riferimento principale</span><span class="sxs-lookup"><span data-stu-id="e2b51-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="e2b51-124">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e2b51-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





