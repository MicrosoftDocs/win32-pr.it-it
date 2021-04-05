---
description: Definisce le costanti che descrivono il tipo di buffer nascosto.
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: Enumerazione D3DBACKBUFFER_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1641b37242339173fc5f591280d8e2beeff6a9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969321"
---
# <a name="d3dbackbuffer_type-enumeration"></a><span data-ttu-id="f507a-103">\_Enumerazione del tipo D3DBACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="f507a-103">D3DBACKBUFFER\_TYPE enumeration</span></span>

<span data-ttu-id="f507a-104">Definisce le costanti che descrivono il tipo di buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="f507a-104">Defines constants that describe the type of back buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f507a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f507a-105">Syntax</span></span>


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="f507a-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="f507a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f507a-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER di \_ tipo \_ mono**</span><span class="sxs-lookup"><span data-stu-id="f507a-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER\_TYPE\_MONO**</span></span>
</dt> <dd>

<span data-ttu-id="f507a-108">Specifica una catena di scambio non stereo.</span><span class="sxs-lookup"><span data-stu-id="f507a-108">Specifies a nonstereo swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="f507a-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**Tipo di D3DBACKBUFFER a \_ \_ sinistra**</span><span class="sxs-lookup"><span data-stu-id="f507a-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER\_TYPE\_LEFT**</span></span>
</dt> <dd>

<span data-ttu-id="f507a-110">Specifica il lato sinistro di una coppia stereo in una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="f507a-110">Specifies the left side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="f507a-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER \_ tipo a \_ destra**</span><span class="sxs-lookup"><span data-stu-id="f507a-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER\_TYPE\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="f507a-112">Specifica il lato destro di una coppia stereo in una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="f507a-112">Specifies the right side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="f507a-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**\_Tipo D3DBACKBUFFER \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f507a-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER\_TYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f507a-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f507a-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f507a-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f507a-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f507a-116">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f507a-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f507a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f507a-117">Remarks</span></span>

<span data-ttu-id="f507a-118">Direct3D 9 non supporta la visualizzazione stereo, quindi Direct3D non usa i \_ \_ valori di tipo D3DBACKBUFFER Left e \_ D3DBACKBUFFER \_ right di questo tipo enumerato.</span><span class="sxs-lookup"><span data-stu-id="f507a-118">Direct3D 9 does not support stereo view, so Direct3D does not use the D3DBACKBUFFER\_TYPE\_LEFT and D3DBACKBUFFER\_TYPE\_RIGHT values of this enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f507a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f507a-119">Requirements</span></span>



| <span data-ttu-id="f507a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f507a-120">Requirement</span></span> | <span data-ttu-id="f507a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f507a-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f507a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f507a-122">Header</span></span><br/> | <dl> <span data-ttu-id="f507a-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f507a-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f507a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f507a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f507a-125">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="f507a-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="f507a-126">**IDirect3DDevice9:: GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="f507a-126">**IDirect3DDevice9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[<span data-ttu-id="f507a-127">**IDirect3DSwapChain9:: GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="f507a-127">**IDirect3DSwapChain9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
