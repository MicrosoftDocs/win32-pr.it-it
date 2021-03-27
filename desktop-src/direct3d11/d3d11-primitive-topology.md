---
description: Il modo in cui la pipeline interpreta i dati dei vertici associati alla fase input-assembler. Questi valori di topologia primitivi determinano il rendering dei dati dei vertici sullo schermo.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: '\_Enumerazione della \_ topologia PRIMItiva d3d11'
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995269"
---
# <a name="d3d11_primitive_topology-enumeration"></a><span data-ttu-id="3d1df-104">\_Enumerazione della \_ topologia PRIMItiva d3d11</span><span class="sxs-lookup"><span data-stu-id="3d1df-104">D3D11\_PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="3d1df-105">Il modo in cui la pipeline interpreta i dati dei vertici associati alla fase input-assembler.</span><span class="sxs-lookup"><span data-stu-id="3d1df-105">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="3d1df-106">Questi valori di topologia primitivi determinano il rendering dei dati dei vertici sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="3d1df-106">These primitive topology values determine how the vertex data is rendered on screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1df-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d1df-107">Syntax</span></span>


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a><span data-ttu-id="3d1df-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="3d1df-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3d1df-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Topologia primitiva d3d11 non \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="3d1df-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-110">La fase IA non è stata inizializzata con una topologia primitiva.</span><span class="sxs-lookup"><span data-stu-id="3d1df-110">The IA stage has not been initialized with a primitive topology.</span></span> <span data-ttu-id="3d1df-111">La fase IA non funzionerà correttamente a meno che non sia stata definita una topologia primitiva.</span><span class="sxs-lookup"><span data-stu-id="3d1df-111">The IA stage will not function properly unless a primitive topology is defined.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ della \_ topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-113">Interpretare i dati dei vertici come un elenco di punti.</span><span class="sxs-lookup"><span data-stu-id="3d1df-113">Interpret the vertex data as a list of points.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**\_Linea di \_ topologia PRIMItiva d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-115">Interpretare i dati dei vertici come un elenco di righe.</span><span class="sxs-lookup"><span data-stu-id="3d1df-115">Interpret the vertex data as a list of lines.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11 \_ \_ topologia primitiva \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="3d1df-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-117">Interpretare i dati dei vertici come una striscia di linea.</span><span class="sxs-lookup"><span data-stu-id="3d1df-117">Interpret the vertex data as a line strip.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**Triangolo della \_ \_ topologia PRIMItiva d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-119">Interpretare i dati dei vertici come un elenco di triangoli.</span><span class="sxs-lookup"><span data-stu-id="3d1df-119">Interpret the vertex data as a list of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ \_ topologia primitiva \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="3d1df-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-121">Interpretare i dati dei vertici come una striscia di triangolo.</span><span class="sxs-lookup"><span data-stu-id="3d1df-121">Interpret the vertex data as a triangle strip.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ la \_ topologia primitiva di \_ linea \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-123">Interpretare i dati dei vertici come un elenco di righe con dati adiacenza.</span><span class="sxs-lookup"><span data-stu-id="3d1df-123">Interpret the vertex data as list of lines with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ \_ topologia primitiva \_ LINESTRIP \_ ADJ**</span><span class="sxs-lookup"><span data-stu-id="3d1df-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-125">Interpretare i dati dei vertici come striping con i dati adiacenza.</span><span class="sxs-lookup"><span data-stu-id="3d1df-125">Interpret the vertex data as line strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ \_ triangolico topologia primitive \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-127">Interpretare i dati dei vertici come un elenco di triangoli con dati adiacenza.</span><span class="sxs-lookup"><span data-stu-id="3d1df-127">Interpret the vertex data as list of triangles with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ \_ topologia primitiva \_ TRIANGLESTRIP \_ ADJ**</span><span class="sxs-lookup"><span data-stu-id="3d1df-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-129">Interpretare i dati dei vertici come strisce di triangolo con i dati adiacenza.</span><span class="sxs-lookup"><span data-stu-id="3d1df-129">Interpret the vertex data as triangle strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ primitive \_ topologia \_ 1 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-131">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-131">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 2 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-133">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-133">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 3 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-135">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-135">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 4 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-137">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-137">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 5 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-139">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-139">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 6 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-141">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-141">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**\_Patch del \_ punto di controllo della topologia primitiva d3d11 \_ 7 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-143">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-143">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 8 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-145">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-145">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ \_ punto di controllo topologia primitiva \_ 9 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-147">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-147">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 10 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-149">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-149">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 11 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-151">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-151">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 12 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-153">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-153">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 13 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-155">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-155">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 14 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-157">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-157">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 15 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-159">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-159">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 16 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-161">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-161">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 17 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-163">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-163">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 18 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-165">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-165">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 19 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-167">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-167">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 20 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-169">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-169">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 21 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-171">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-171">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 22 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-173">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-173">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 23 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-175">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-175">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 24 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-177">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-177">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 25 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-179">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-179">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 26 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-181">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-181">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 27 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-183">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-183">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 28 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-185">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-185">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 29 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-187">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-187">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 30 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-189">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-189">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 31 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-191">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-191">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="3d1df-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 32 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d1df-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="3d1df-193">Interpretare i dati dei vertici come un elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="3d1df-193">Interpret the vertex data as a patch list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d1df-194">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d1df-194">Remarks</span></span>

<span data-ttu-id="3d1df-195">L'enumerazione della **\_ \_ topologia primitiva d3d11** è definita nel file di intestazione d3d11. h come enumerazione di [**\_ \_ topologia primitiva D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , completamente definita nel file di intestazione D3DCommon. h.</span><span class="sxs-lookup"><span data-stu-id="3d1df-195">The **D3D11\_PRIMITIVE\_TOPOLOGY** enumeration is type defined in the D3D11.h header file as a [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) enumeration, which is fully defined in the D3DCommon.h header file.</span></span>
