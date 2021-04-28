---
description: 'Enumerazione D3DXMESH: flag usati per specificare le opzioni di creazione per una mesh.'
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Enumerazione D3DXMESH (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a312c2618960691184182039afe38acc8947eb6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098099"
---
# <a name="d3dxmesh-enumeration"></a><span data-ttu-id="cd54d-103">Enumerazione D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="cd54d-103">D3DXMESH enumeration</span></span>

<span data-ttu-id="cd54d-104">Flag usati per specificare le opzioni di creazione per una mesh.</span><span class="sxs-lookup"><span data-stu-id="cd54d-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd54d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd54d-105">Syntax</span></span>


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a><span data-ttu-id="cd54d-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="cd54d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cd54d-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 BIT**</span><span class="sxs-lookup"><span data-stu-id="cd54d-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH\_32BIT**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-108">La mesh ha indici a 32 bit anziché indici a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="cd54d-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="cd54d-109">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="cd54d-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**</span><span class="sxs-lookup"><span data-stu-id="cd54d-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH\_DONOTCLIP**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-111">Usare il flag [**di utilizzo D3DUSAGE \_ DONOTCLIP**](d3dusage.md) per i buffer dei vertici e degli indici.</span><span class="sxs-lookup"><span data-stu-id="cd54d-111">Use the [**D3DUSAGE\_DONOTCLIP**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**PUNTI D3DXMESH \_**</span><span class="sxs-lookup"><span data-stu-id="cd54d-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH\_POINTS**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-113">Usare il flag [**di utilizzo D3DUSAGE \_ POINTS**](d3dusage.md) per i buffer dei vertici e degli indici.</span><span class="sxs-lookup"><span data-stu-id="cd54d-113">Use the [**D3DUSAGE\_POINTS**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**</span><span class="sxs-lookup"><span data-stu-id="cd54d-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH\_RTPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-115">Usare il flag [**di utilizzo D3DUSAGE \_ RTPATCHES**](d3dusage.md) per i buffer dei vertici e degli indici.</span><span class="sxs-lookup"><span data-stu-id="cd54d-115">Use the [**D3DUSAGE\_RTPATCHES**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**</span><span class="sxs-lookup"><span data-stu-id="cd54d-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH\_NPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-117">Se si specifica questo flag, il vertice e index buffer della mesh vengono creati con il flag [**D3DUSAGE \_ NPATCHES.**](d3dusage.md)</span><span class="sxs-lookup"><span data-stu-id="cd54d-117">Specifying this flag causes the vertex and index buffer of the mesh to be created with [**D3DUSAGE\_NPATCHES**](d3dusage.md) flag.</span></span> <span data-ttu-id="cd54d-118">Questa operazione è necessaria se è necessario eseguire il rendering dell'oggetto mesh usando il miglioramento della patch N tramite Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cd54d-118">This is required if the mesh object is to be rendered using N-patch enhancement using Direct3D.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="cd54d-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH\_VB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-120">Usare il flag [**di utilizzo D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) per i vertex buffer.</span><span class="sxs-lookup"><span data-stu-id="cd54d-120">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ MANAGED**</span><span class="sxs-lookup"><span data-stu-id="cd54d-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH\_VB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-122">Usare il flag [**di utilizzo D3DPOOL \_ MANAGED**](./d3dpool.md) per i vertex buffer.</span><span class="sxs-lookup"><span data-stu-id="cd54d-122">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="cd54d-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH\_VB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-124">Usare il flag [**di utilizzo D3DUSAGE \_ WRITEONLY**](d3dusage.md) per i vertex buffer.</span><span class="sxs-lookup"><span data-stu-id="cd54d-124">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ DYNAMIC**</span><span class="sxs-lookup"><span data-stu-id="cd54d-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH\_VB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-126">Usare il flag [**D3DUSAGE \_ DYNAMIC**](d3dusage.md) usage per i vertex buffer.</span><span class="sxs-lookup"><span data-stu-id="cd54d-126">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="cd54d-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH\_VB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-128">Usare il flag [**di utilizzo D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) per i vertex buffer.</span><span class="sxs-lookup"><span data-stu-id="cd54d-128">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="cd54d-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH\_IB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-130">Usare il flag [**di utilizzo D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) per i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="cd54d-130">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ MANAGED**</span><span class="sxs-lookup"><span data-stu-id="cd54d-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH\_IB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-132">Usare il flag [**di utilizzo gestito D3DPOOL \_**](./d3dpool.md) per i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="cd54d-132">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="cd54d-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH\_IB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-134">Usare il flag [**di utilizzo D3DUSAGE \_ WRITEONLY**](d3dusage.md) per i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="cd54d-134">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ DYNAMIC**</span><span class="sxs-lookup"><span data-stu-id="cd54d-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH\_IB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-136">Usare il flag [**D3DUSAGE \_ DYNAMIC**](d3dusage.md) usage per i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="cd54d-136">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**SOFTWARE IB D3DXMESHPROCESSING \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd54d-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH\_IB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-138">Usare il flag [**di utilizzo D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) per i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="cd54d-138">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ VB \_ SHARE**</span><span class="sxs-lookup"><span data-stu-id="cd54d-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH\_VB\_SHARE**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-140">Forza le mesh clonate a condividere i vertex buffer.</span><span class="sxs-lookup"><span data-stu-id="cd54d-140">Forces the cloned meshes to share vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**</span><span class="sxs-lookup"><span data-stu-id="cd54d-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH\_USEHWONLY**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-142">Usare solo l'elaborazione hardware.</span><span class="sxs-lookup"><span data-stu-id="cd54d-142">Use hardware processing only.</span></span> <span data-ttu-id="cd54d-143">Per il dispositivo in modalità mista, questo flag fa sì che il sistema usi l'hardware (se supportato nell'hardware) o per impostazione predefinita l'elaborazione software.</span><span class="sxs-lookup"><span data-stu-id="cd54d-143">For mixed-mode device, this flag will cause the system to use hardware (if supported in hardware) or will default to software processing.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="cd54d-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-145">Equivale a specificare sia D3DXMESH \_ VB \_ SYSTEMMEM che D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="cd54d-145">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ GESTITO**</span><span class="sxs-lookup"><span data-stu-id="cd54d-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-147">Equivale a specificare sia D3DXMESH \_ VB \_ MANAGED che D3DXMESH \_ IB \_ MANAGED.</span><span class="sxs-lookup"><span data-stu-id="cd54d-147">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="cd54d-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-149">Equivale a specificare sia D3DXMESH \_ VB \_ WRITEONLY che D3DXMESH \_ IB \_ WRITEONLY.</span><span class="sxs-lookup"><span data-stu-id="cd54d-149">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ DYNAMIC**</span><span class="sxs-lookup"><span data-stu-id="cd54d-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-151">Equivale a specificare sia D3DXMESH \_ VB \_ DYNAMIC che D3DXMESH \_ IB \_ DYNAMIC.</span><span class="sxs-lookup"><span data-stu-id="cd54d-151">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>

</dd> <dt>

<span data-ttu-id="cd54d-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**SOFTWARE D3DXMESHPROCESSING \_**</span><span class="sxs-lookup"><span data-stu-id="cd54d-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="cd54d-153">Equivale a specificare sia D3DXMESH \_ VB \_ SOFTWAREPROCESSING che D3DXMESH \_ IB \_ SOFTWAREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="cd54d-153">Equivalent to specifying both D3DXMESH\_VB\_SOFTWAREPROCESSING and D3DXMESH\_IB\_SOFTWAREPROCESSING.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd54d-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd54d-154">Remarks</span></span>

<span data-ttu-id="cd54d-155">Una mesh a 32 bit (D3DXMESH 32BIT) può teoricamente \_ supportare (2^32)-1 visi e vertici.</span><span class="sxs-lookup"><span data-stu-id="cd54d-155">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2^32)-1 faces and vertices.</span></span> <span data-ttu-id="cd54d-156">Tuttavia, l'allocazione di memoria per una mesh di grandi dimensioni in un sistema operativo a 32 bit non è pratica.</span><span class="sxs-lookup"><span data-stu-id="cd54d-156">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd54d-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd54d-157">Requirements</span></span>



| <span data-ttu-id="cd54d-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd54d-158">Requirement</span></span> | <span data-ttu-id="cd54d-159">Valore</span><span class="sxs-lookup"><span data-stu-id="cd54d-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd54d-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd54d-160">Header</span></span><br/> | <dl> <span data-ttu-id="cd54d-161"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="cd54d-161"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd54d-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd54d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd54d-163">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="cd54d-163">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
