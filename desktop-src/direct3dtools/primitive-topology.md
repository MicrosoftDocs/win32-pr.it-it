---
description: Enumerazione utilizzata per indicare la topologia di una mesh. Vedere MeshDataVertCallback.
MS-HAID: vspixengine.PRIMITIVE\_TOPOLOGY
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione PRIMITIVE_TOPOLOGY
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A845DD10-C735-4EA1-82D3-07F3B26508E7
api_name:
- PRIMITIVE_TOPOLOGY
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7e448fcaaeaa2b1b50bd77b18ac4b3ac3f5e122a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049052"
---
# <a name="span-idvspixengineprimitive_topologyspanprimitive_topology-enumeration"></a><span data-ttu-id="b1139-104"><span id="vspixengine.primitive_topology"></span>\_Enumerazione della topologia primitiva</span><span class="sxs-lookup"><span data-stu-id="b1139-104"><span id="vspixengine.primitive_topology"></span>PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="b1139-105">Enumerazione utilizzata per indicare la topologia di una mesh.</span><span class="sxs-lookup"><span data-stu-id="b1139-105">An enum used to indicate the topology of a mesh.</span></span> <span data-ttu-id="b1139-106">Vedere MeshDataVertCallback.</span><span class="sxs-lookup"><span data-stu-id="b1139-106">See MeshDataVertCallback.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1139-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1139-107">Syntax</span></span>


```C++
} PRIMITIVE_TOPOLOGY;
```

## <a name="constants"></a><span data-ttu-id="b1139-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="b1139-108">Constants</span></span>

<span data-ttu-id="b1139-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**topologia PRIMItiva non \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="b1139-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>  
<span data-ttu-id="b1139-110">La topologia della mesh non è definita.</span><span class="sxs-lookup"><span data-stu-id="b1139-110">The topology of the mesh is undefined.</span></span>

<span data-ttu-id="b1139-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**\_endpoint topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>  
<span data-ttu-id="b1139-112">La topologia della mesh è un elenco di punti.</span><span class="sxs-lookup"><span data-stu-id="b1139-112">The topology of the mesh is a point list.</span></span>

<span data-ttu-id="b1139-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**\_linea di topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>  
<span data-ttu-id="b1139-114">La topologia della mesh è un elenco di righe.</span><span class="sxs-lookup"><span data-stu-id="b1139-114">The topology of the mesh is a line list.</span></span>

<span data-ttu-id="b1139-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**\_topologia primitiva \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="b1139-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>  
<span data-ttu-id="b1139-116">La topologia della mesh è un'striscia di linea.</span><span class="sxs-lookup"><span data-stu-id="b1139-116">The topology of the mesh is a line strip.</span></span>

<span data-ttu-id="b1139-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**\_TRIangolino topologia primitive \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>  
<span data-ttu-id="b1139-118">La topologia della mesh è un elenco di triangolo.</span><span class="sxs-lookup"><span data-stu-id="b1139-118">The topology of the mesh is a triangle list.</span></span>

<span data-ttu-id="b1139-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**\_topologia primitiva \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="b1139-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>  
<span data-ttu-id="b1139-120">La topologia della mesh è una striscia di triangolo.</span><span class="sxs-lookup"><span data-stu-id="b1139-120">The topology of the mesh is a triangle strip.</span></span>

<span data-ttu-id="b1139-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**\_topologia primitiva \_ TRIANGLEFAN**</span><span class="sxs-lookup"><span data-stu-id="b1139-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLEFAN**</span></span>  
<span data-ttu-id="b1139-122">La topologia della mesh è una ventola del triangolo.</span><span class="sxs-lookup"><span data-stu-id="b1139-122">The topology of the mesh is a triangle fan.</span></span>

<span data-ttu-id="b1139-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**\_ADJ per topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>  
<span data-ttu-id="b1139-124">La topologia della mesh è un elenco di righe con adiacenza.</span><span class="sxs-lookup"><span data-stu-id="b1139-124">The topology of the mesh is a line list with adjacency.</span></span>

<span data-ttu-id="b1139-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**\_LINESTRIP di topologia primitive \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>  
<span data-ttu-id="b1139-126">La topologia della mesh è un'elenco di righe con adiacenza.</span><span class="sxs-lookup"><span data-stu-id="b1139-126">The topology of the mesh is a line strip with adjacency.</span></span>

<span data-ttu-id="b1139-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**registrazione \_ triangoli topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>  
<span data-ttu-id="b1139-128">La topologia della mesh è un elenco di triangolo con adiacenza.</span><span class="sxs-lookup"><span data-stu-id="b1139-128">The topology of the mesh is a triangle list with adjacency.</span></span>

<span data-ttu-id="b1139-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**\_TRIANGLESTRIP di topologia primitive \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>  
<span data-ttu-id="b1139-130">La topologia della mesh è una striscia di triangolo con adiacenza.</span><span class="sxs-lookup"><span data-stu-id="b1139-130">The topology of the mesh is a triangle strip with adjacency.</span></span>

<span data-ttu-id="b1139-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**\_Primo punto di controllo della topologia primitiva \_ 1 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-132">La topologia della mesh è un elenco di patch con 1 punto di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-132">The topology of the mesh is a patch list with 1 control point.</span></span>

<span data-ttu-id="b1139-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**Patch per la \_ topologia primitiva \_ 2 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-134">La topologia della mesh è un elenco di patch con 2 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-134">The topology of the mesh is a patch list with 2 control points.</span></span>

<span data-ttu-id="b1139-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**\_ \_ 5 punti di \_ controllo \_ topologia primitiva 3 \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-136">La topologia della mesh è un elenco di patch con 3 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-136">The topology of the mesh is a patch list with 3 control points.</span></span>

<span data-ttu-id="b1139-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**\_ \_ 5 punti di \_ controllo \_ topologia primitiva 4 \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-138">La topologia della mesh è un elenco di patch con 4 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-138">The topology of the mesh is a patch list with 4 control points.</span></span>

<span data-ttu-id="b1139-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**\_ \_ 5 punti di \_ controllo \_ topologia primitiva 5 \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-140">La topologia della mesh è un elenco di patch con 5 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-140">The topology of the mesh is a patch list with 5 control points.</span></span>

<span data-ttu-id="b1139-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**\_ \_ 5 punti di \_ controllo \_ topologia primitiva 6 \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-142">La topologia della mesh è un elenco di patch con 6 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-142">The topology of the mesh is a patch list with 6 control points.</span></span>

<span data-ttu-id="b1139-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**Patch per la \_ topologia primitiva 7 del \_ \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-144">La topologia della mesh è un elenco di patch con 7 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-144">The topology of the mesh is a patch list with 7 control points.</span></span>

<span data-ttu-id="b1139-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**\_Topologia primitiva \_ 8 \_ punti di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-146">La topologia della mesh è un elenco di patch con 8 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-146">The topology of the mesh is a patch list with 8 control points.</span></span>

<span data-ttu-id="b1139-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**Patch per la \_ topologia primitiva \_ 9 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-148">La topologia della mesh è un elenco di patch con 9 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-148">The topology of the mesh is a patch list with 9 control points.</span></span>

<span data-ttu-id="b1139-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**Patch per la \_ topologia primitiva \_ 10 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-150">La topologia della mesh è un elenco di patch con 10 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-150">The topology of the mesh is a patch list with 10 control points.</span></span>

<span data-ttu-id="b1139-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**PRIMItiva \_ topologia \_ 11 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-152">La topologia della mesh è un elenco di patch con 11 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-152">The topology of the mesh is a patch list with 11 control points.</span></span>

<span data-ttu-id="b1139-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**\_Topologia primitiva \_ 12 \_ punti di controllo della \_ topologia \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-154">La topologia della mesh è un elenco di patch con 12 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-154">The topology of the mesh is a patch list with 12 control points.</span></span>

<span data-ttu-id="b1139-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**\_Topologia primitiva \_ 13 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-156">La topologia della mesh è un elenco di patch con 13 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-156">The topology of the mesh is a patch list with 13 control points.</span></span>

<span data-ttu-id="b1139-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**\_Topologia primitiva \_ 14 \_ punti di controllo della \_ topologia \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-158">La topologia della mesh è un elenco di patch con 14 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-158">The topology of the mesh is a patch list with 14 control points.</span></span>

<span data-ttu-id="b1139-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**\_Topologia primitiva \_ 15 \_ punto di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-160">La topologia della mesh è un elenco di patch con 15 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-160">The topology of the mesh is a patch list with 15 control points.</span></span>

<span data-ttu-id="b1139-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**PRIMItiva di \_ \_ 16 \_ punti di controllo \_ \_ della topologia**</span><span class="sxs-lookup"><span data-stu-id="b1139-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-162">La topologia della mesh è un elenco di patch con 16 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-162">The topology of the mesh is a patch list with 16 control points.</span></span>

<span data-ttu-id="b1139-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**\_Topologia primitiva \_ 17 \_ punti di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-164">La topologia della mesh è un elenco di patch con 17 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-164">The topology of the mesh is a patch list with 17 control points.</span></span>

<span data-ttu-id="b1139-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**PRIMItiva \_ \_ 18 \_ punti di controllo della \_ topologia \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-166">La topologia della mesh è un elenco di patch con 18 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-166">The topology of the mesh is a patch list with 18 control points.</span></span>

<span data-ttu-id="b1139-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**\_Topologia \_ del \_ punto di controllo 19 della topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-168">La topologia della mesh è un elenco di patch con 19 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-168">The topology of the mesh is a patch list with 19 control points.</span></span>

<span data-ttu-id="b1139-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**\_Topologia \_ del \_ punto di controllo 20 di topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-170">La topologia della mesh è un elenco di patch con 20 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-170">The topology of the mesh is a patch list with 20 control points.</span></span>

<span data-ttu-id="b1139-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**\_Topologia primitiva \_ 21 \_ punti di controllo della \_ topologia \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-172">La topologia della mesh è un elenco di patch con 21 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-172">The topology of the mesh is a patch list with 21 control points.</span></span>

<span data-ttu-id="b1139-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**\_Topologia primitiva \_ 22 \_ punto di controllo della \_ topologia \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-174">La topologia della mesh è un elenco di patch con 22 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-174">The topology of the mesh is a patch list with 22 control points.</span></span>

<span data-ttu-id="b1139-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**\_Topologia \_ del \_ punto di controllo 23 della topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-176">La topologia della mesh è un elenco di patch con 23 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-176">The topology of the mesh is a patch list with 23 control points.</span></span>

<span data-ttu-id="b1139-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**\_Topologia primitiva \_ 24 \_ punti di controllo della \_ topologia \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-178">La topologia della mesh è un elenco di patch con 24 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-178">The topology of the mesh is a patch list with 24 control points.</span></span>

<span data-ttu-id="b1139-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**\_Topologia \_ del \_ punto di controllo 25 della topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-180">La topologia della mesh è un elenco di patch con 25 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-180">The topology of the mesh is a patch list with 25 control points.</span></span>

<span data-ttu-id="b1139-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**\_Topologia \_ del \_ punto di controllo 26 della topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-182">La topologia della mesh è un elenco di patch con 26 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-182">The topology of the mesh is a patch list with 26 control points.</span></span>

<span data-ttu-id="b1139-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**\_Topologia primitiva \_ 27 \_ punti di controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-184">La topologia della mesh è un elenco di patch con 27 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-184">The topology of the mesh is a patch list with 27 control points.</span></span>

<span data-ttu-id="b1139-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**\_Topologia \_ del \_ punto di controllo 28 della topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-186">La topologia della mesh è un elenco di patch con 28 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-186">The topology of the mesh is a patch list with 28 control points.</span></span>

<span data-ttu-id="b1139-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**\_Topologia \_ del \_ punto di controllo 29 della topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-188">La topologia della mesh è un elenco di patch con 29 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-188">The topology of the mesh is a patch list with 29 control points.</span></span>

<span data-ttu-id="b1139-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**\_Topologia primitiva \_ 30 \_ punti di controllo della \_ topologia \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-190">La topologia della mesh è un elenco di patch con 30 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-190">The topology of the mesh is a patch list with 30 control points.</span></span>

<span data-ttu-id="b1139-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**\_Topologia primitiva \_ 31 del punto di \_ controllo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-192">La topologia della mesh è un elenco di patch con 31 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1139-192">The topology of the mesh is a patch list with 31 control points.</span></span>

<span data-ttu-id="b1139-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**\_Topologia \_ del \_ punto di controllo 32 \_ topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="b1139-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b1139-194">La topologia della mesh è un elenco di patch con punti di controllo 32.</span><span class="sxs-lookup"><span data-stu-id="b1139-194">The topology of the mesh is a patch list with 32 control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1139-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1139-195">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b1139-196">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1139-196">Header</span></span></p></td><td><span data-ttu-id="b1139-197">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b1139-197">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



