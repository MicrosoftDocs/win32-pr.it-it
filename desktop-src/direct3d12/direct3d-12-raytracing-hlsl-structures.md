---
title: Strutture raytracing HLSL (Direct3D 12)
description: Le strutture HLSL seguenti supportano la pipeline raytracing di Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c48ad6bac76e200587ec76d42dfa9c86b23cd23
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "106299285"
---
# <a name="raytracing-hlsl-structures-direct3d-12"></a><span data-ttu-id="89cca-103">Strutture raytracing HLSL (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="89cca-103">Raytracing HLSL structures (Direct3D 12)</span></span>

<span data-ttu-id="89cca-104">Le strutture HLSL seguenti supportano la pipeline raytracing di Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="89cca-104">The following HLSL structures support the Direct3D 12 raytracing pipeline.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="89cca-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="89cca-105">In this section</span></span>



| <span data-ttu-id="89cca-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="89cca-106">Topic</span></span>                                                                                                       | <span data-ttu-id="89cca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89cca-107">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89cca-108">**Struttura di parametri di chiamata**</span><span class="sxs-lookup"><span data-stu-id="89cca-108">**Call Parameter Structure**</span></span>](call-parameter-structure.md)<br/>                              | <span data-ttu-id="89cca-109">Una struttura definita dall'utente fornita come argomento INOUT a una chiamata CallShader e come parametro inout per lo shader chiamabile.</span><span class="sxs-lookup"><span data-stu-id="89cca-109">A user-defined structure provided as an inout argument to a CallShader call, and as an inout parameter for the callable shader.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="89cca-110">**Struttura degli attributi di intersezione**</span><span class="sxs-lookup"><span data-stu-id="89cca-110">**Intersection Attributes Structure**</span></span>](intersection-attributes.md)<br/>                              | <span data-ttu-id="89cca-111">Struttura definita dall'utente fornita come argomento INOUT in una chiamata [**TraceRay**](traceray-function.md) e come parametro inout nei tipi shader che possono accedere al payload del raggio.</span><span class="sxs-lookup"><span data-stu-id="89cca-111">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="89cca-112">**Struttura di payload Ray**</span><span class="sxs-lookup"><span data-stu-id="89cca-112">**Ray Payload Structure**</span></span>](ray-payload.md)<br/>                              | <span data-ttu-id="89cca-113">Struttura definita dall'utente fornita come argomento INOUT in una chiamata [**TraceRay**](traceray-function.md) e come parametro inout nei tipi shader che possono accedere al payload del raggio.</span><span class="sxs-lookup"><span data-stu-id="89cca-113">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="89cca-114">**Struttura RayDesc**</span><span class="sxs-lookup"><span data-stu-id="89cca-114">**RayDesc Structure**</span></span>](raydesc.md)<br/>                              | <span data-ttu-id="89cca-115">Flag passati alla funzione [**TraceRay**](traceray-function.md) per eseguire l'override della trasparenza, dell'eliminazione e del comportamento iniziale.</span><span class="sxs-lookup"><span data-stu-id="89cca-115">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span><br/>                                                                                                                                                                                                                                              |





 

## <a name="related-topics"></a><span data-ttu-id="89cca-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89cca-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89cca-117">Riferimento principale</span><span class="sxs-lookup"><span data-stu-id="89cca-117">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="89cca-118">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="89cca-118">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





