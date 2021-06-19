---
title: Shader HLSL Raytracing Direct3D 12
description: Visualizzare i collegamenti agli articoli che descrivono gli shader HLSL (High-Level Shader Language) che supportano la pipeline di raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca19081b1ea963851e82d18912153434c3e38d1
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394836"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="1309b-103">Shader HLSL Raytracing Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1309b-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="1309b-104">Gli shader HLSL seguenti supportano la pipeline di raytracing Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="1309b-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="1309b-105">Questi shader sono funzioni compilate in una libreria, con modello di destinazione lib_6_3 e identificati da un attributo *[shader("shadertype")]* nella funzione shader.</span><span class="sxs-lookup"><span data-stu-id="1309b-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="1309b-106">Vedere **Intrinseci e** **valori di sistema** per vedere cosa è consentito per ogni tipo di shader.</span><span class="sxs-lookup"><span data-stu-id="1309b-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1309b-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1309b-107">In this section</span></span>



| <span data-ttu-id="1309b-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="1309b-108">Topic</span></span>                                                                                                       | <span data-ttu-id="1309b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1309b-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1309b-110">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="1309b-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="1309b-111">Shader richiamato quando le intersezioni dei raggi non sono opache.</span><span class="sxs-lookup"><span data-stu-id="1309b-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1309b-112">**Shader chiamabile**</span><span class="sxs-lookup"><span data-stu-id="1309b-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="1309b-113">Shader richiamato da un altro shader con la funzione **intrinseca CallShader.**</span><span class="sxs-lookup"><span data-stu-id="1309b-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1309b-114">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="1309b-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="1309b-115">Shader richiamato quando è abilitato ed è stato determinato l'hit più vicino o è terminata la ricerca di intersezione dei raggi.</span><span class="sxs-lookup"><span data-stu-id="1309b-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1309b-116">**Intersection Shader**</span><span class="sxs-lookup"><span data-stu-id="1309b-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="1309b-117">Shader usato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di selezione).</span><span class="sxs-lookup"><span data-stu-id="1309b-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1309b-118">**Miss Shader**</span><span class="sxs-lookup"><span data-stu-id="1309b-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="1309b-119">Shader richiamato quando non vengono trovate o accettate intersezioni di raggi.</span><span class="sxs-lookup"><span data-stu-id="1309b-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1309b-120">**Ray Generation Shader**</span><span class="sxs-lookup"><span data-stu-id="1309b-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="1309b-121">Shader che chiama [**TraceRay per**](traceray-function.md) generare raggi.</span><span class="sxs-lookup"><span data-stu-id="1309b-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="1309b-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1309b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1309b-123">Informazioni di riferimento di base</span><span class="sxs-lookup"><span data-stu-id="1309b-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="1309b-124">Informazioni di riferimento su Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1309b-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





