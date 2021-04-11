---
description: Definisce i valori della trasformazione delle coordinate di trama.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Enumerazione D3DTEXTURETRANSFORMFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234959"
---
# <a name="d3dtexturetransformflags-enumeration"></a><span data-ttu-id="52610-103">Enumerazione D3DTEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="52610-103">D3DTEXTURETRANSFORMFLAGS enumeration</span></span>

<span data-ttu-id="52610-104">Definisce i valori della trasformazione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="52610-104">Defines texture coordinate transformation values.</span></span>

## <a name="syntax"></a><span data-ttu-id="52610-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52610-105">Syntax</span></span>


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a><span data-ttu-id="52610-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="52610-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="52610-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**\_Disabilitazione D3DTTFF**</span><span class="sxs-lookup"><span data-stu-id="52610-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="52610-108">Le coordinate di trama vengono passate direttamente al rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="52610-108">Texture coordinates are passed directly to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="52610-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**\_COUNT1 D3DTTFF**</span><span class="sxs-lookup"><span data-stu-id="52610-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF\_COUNT1**</span></span>
</dt> <dd>

<span data-ttu-id="52610-110">Il rasterizzatore dovrebbe prevedere le coordinate di trama 1D.</span><span class="sxs-lookup"><span data-stu-id="52610-110">The rasterizer should expect 1D texture coordinates.</span></span> <span data-ttu-id="52610-111">Questo valore viene usato dall'elaborazione del vertice della funzione fissa; deve essere impostato su 0 quando si utilizza un vertex shader programmabile.</span><span class="sxs-lookup"><span data-stu-id="52610-111">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="52610-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**\_COUNT2 D3DTTFF**</span><span class="sxs-lookup"><span data-stu-id="52610-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF\_COUNT2**</span></span>
</dt> <dd>

<span data-ttu-id="52610-113">Il rasterizzatore dovrebbe prevedere le coordinate di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="52610-113">The rasterizer should expect 2D texture coordinates.</span></span> <span data-ttu-id="52610-114">Questo valore viene usato dall'elaborazione del vertice della funzione fissa; deve essere impostato su 0 quando si utilizza un vertex shader programmabile.</span><span class="sxs-lookup"><span data-stu-id="52610-114">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="52610-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**\_COUNT3 D3DTTFF**</span><span class="sxs-lookup"><span data-stu-id="52610-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF\_COUNT3**</span></span>
</dt> <dd>

<span data-ttu-id="52610-116">Il rasterizzatore dovrebbe prevedere le coordinate di trama 3D.</span><span class="sxs-lookup"><span data-stu-id="52610-116">The rasterizer should expect 3D texture coordinates.</span></span> <span data-ttu-id="52610-117">Questo valore viene usato dall'elaborazione del vertice della funzione fissa; deve essere impostato su 0 quando si utilizza un vertex shader programmabile.</span><span class="sxs-lookup"><span data-stu-id="52610-117">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="52610-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**\_COUNT4 D3DTTFF**</span><span class="sxs-lookup"><span data-stu-id="52610-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF\_COUNT4**</span></span>
</dt> <dd>

<span data-ttu-id="52610-119">Il rasterizzatore dovrebbe prevedere le coordinate di trama 4D.</span><span class="sxs-lookup"><span data-stu-id="52610-119">The rasterizer should expect 4D texture coordinates.</span></span> <span data-ttu-id="52610-120">Questo valore viene usato dall'elaborazione del vertice della funzione fissa; deve essere impostato su 0 quando si utilizza un vertex shader programmabile.</span><span class="sxs-lookup"><span data-stu-id="52610-120">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="52610-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ proiettato**</span><span class="sxs-lookup"><span data-stu-id="52610-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF\_PROJECTED**</span></span>
</dt> <dd>

<span data-ttu-id="52610-122">Questo flag viene rispettato dalla pipeline di pixel della funzione fissa, nonché dalla pipeline di pixel programmabile nelle versioni PS \_ 1 \_ 1 a PS \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="52610-122">This flag is honored by the fixed function pixel pipeline, as well as the programmable pixel pipeline in versions ps\_1\_1 to ps\_1\_3.</span></span> <span data-ttu-id="52610-123">Quando è abilitata la proiezione di trama per una fase di trama, è necessario scrivere tutti i quattro valori a virgola mobile nel registro di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="52610-123">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span> <span data-ttu-id="52610-124">Ogni coordinata di trama è divisa per l'ultimo elemento prima del passaggio al rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="52610-124">Each texture coordinate is divided by the last element before being passed to the rasterizer.</span></span> <span data-ttu-id="52610-125">Se, ad esempio, questo flag viene specificato con il \_ flag D3DTTFF COUNT3, le coordinate della prima e della seconda trama vengono divise per la terza coordinata prima di essere passate al rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="52610-125">For example, if this flag is specified with the D3DTTFF\_COUNT3 flag, the first and second texture coordinates are divided by the third coordinate before being passed to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="52610-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="52610-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="52610-127">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="52610-127">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="52610-128">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="52610-128">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="52610-129">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="52610-129">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52610-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="52610-130">Remarks</span></span>

<span data-ttu-id="52610-131">È possibile trasformare le coordinate di trama usando una matrice 4 x 4 prima che i risultati vengano passati al rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="52610-131">Texture coordinates can be transformed using a 4 x 4 matrix before the results are passed to the rasterizer.</span></span> <span data-ttu-id="52610-132">Le trasformazioni delle coordinate di trama vengono impostate chiamando [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api)e passando lo \_ stato della fase della trama D3DTSS TEXTURETRANSFORMFLAGS e uno dei valori da **D3DTEXTURETRANSFORMFLAGS**.</span><span class="sxs-lookup"><span data-stu-id="52610-132">The texture coordinate transforms are set by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api), and by passing in the D3DTSS\_TEXTURETRANSFORMFLAGS texture stage state and one of the values from **D3DTEXTURETRANSFORMFLAGS**.</span></span> <span data-ttu-id="52610-133">Per altre informazioni sulle trasformazioni di trama, vedere [trasformazioni di coordinate di trama (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="52610-133">For more information about texture transforms, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52610-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52610-134">Requirements</span></span>



| <span data-ttu-id="52610-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="52610-135">Requirement</span></span> | <span data-ttu-id="52610-136">Valore</span><span class="sxs-lookup"><span data-stu-id="52610-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52610-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52610-137">Header</span></span><br/> | <dl> <span data-ttu-id="52610-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="52610-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52610-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52610-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52610-140">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="52610-140">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="52610-141">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="52610-141">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
