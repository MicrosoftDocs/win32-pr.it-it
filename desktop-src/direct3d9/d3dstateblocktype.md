---
description: Set predefiniti di stato della pipeline usato dai blocchi di stato (vedere lo stato di salvataggio e ripristino del blocco di stato (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Enumerazione D3DSTATEBLOCKTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104562357"
---
# <a name="d3dstateblocktype-enumeration"></a><span data-ttu-id="d982b-103">Enumerazione D3DSTATEBLOCKTYPE</span><span class="sxs-lookup"><span data-stu-id="d982b-103">D3DSTATEBLOCKTYPE enumeration</span></span>

<span data-ttu-id="d982b-104">Set predefiniti di stato della pipeline usato dai blocchi di stato (vedere lo stato di [salvataggio e ripristino del blocco di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="d982b-104">Predefined sets of pipeline state used by state blocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="d982b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d982b-105">Syntax</span></span>


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a><span data-ttu-id="d982b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="d982b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d982b-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ tutto**</span><span class="sxs-lookup"><span data-stu-id="d982b-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="d982b-108">Acquisisce lo [stato](saving-all-device-states-with-a-stateblock.md)corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d982b-108">Capture the current [device state](saving-all-device-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="d982b-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**\_PIXELSTATE D3DSBT**</span><span class="sxs-lookup"><span data-stu-id="d982b-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT\_PIXELSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="d982b-110">Acquisisce lo [stato](saving-pixel-states-with-a-stateblock.md)corrente dei pixel.</span><span class="sxs-lookup"><span data-stu-id="d982b-110">Capture the current [pixel state](saving-pixel-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="d982b-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**\_VERTEXSTATE D3DSBT**</span><span class="sxs-lookup"><span data-stu-id="d982b-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT\_VERTEXSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="d982b-112">Acquisisce lo [stato del vertice](saving-vertex-states-with-a-stateblock.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="d982b-112">Capture the current [vertex state](saving-vertex-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="d982b-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d982b-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d982b-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d982b-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d982b-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d982b-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d982b-116">Non usare questo valore.</span><span class="sxs-lookup"><span data-stu-id="d982b-116">Do not use this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d982b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d982b-117">Remarks</span></span>

<span data-ttu-id="d982b-118">Come illustrato nel diagramma seguente, lo stato del vertice e del pixel è costituito da entrambi i subset dello stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d982b-118">As the following diagram shows, vertex and pixel state are both subsets of device state.</span></span>

![diagramma dello stato del dispositivo, con stato del vertice e stato del pixel come subset](images/statesets.png)

<span data-ttu-id="d982b-120">Esistono solo alcuni Stati che sono considerati lo stato del vertice e del pixel.</span><span class="sxs-lookup"><span data-stu-id="d982b-120">There are only a few states that are considered both vertex and pixel state.</span></span> <span data-ttu-id="d982b-121">Questi stati sono:</span><span class="sxs-lookup"><span data-stu-id="d982b-121">These states are:</span></span>

-   <span data-ttu-id="d982b-122">Stato di rendering: D3DRS \_ FOGDENSITY</span><span class="sxs-lookup"><span data-stu-id="d982b-122">Render state: D3DRS\_FOGDENSITY</span></span>
-   <span data-ttu-id="d982b-123">Stato di rendering: D3DRS \_ FOGSTART</span><span class="sxs-lookup"><span data-stu-id="d982b-123">Render state: D3DRS\_FOGSTART</span></span>
-   <span data-ttu-id="d982b-124">Stato di rendering: D3DRS \_ FOGEND</span><span class="sxs-lookup"><span data-stu-id="d982b-124">Render state: D3DRS\_FOGEND</span></span>
-   <span data-ttu-id="d982b-125">Stato trama: D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="d982b-125">Texture state: D3DTSS\_TEXCOORDINDEX</span></span>
-   <span data-ttu-id="d982b-126">Stato trama: D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="d982b-126">Texture state: D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>

## <a name="requirements"></a><span data-ttu-id="d982b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d982b-127">Requirements</span></span>



| <span data-ttu-id="d982b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d982b-128">Requirement</span></span> | <span data-ttu-id="d982b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d982b-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d982b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d982b-130">Header</span></span><br/> | <dl> <span data-ttu-id="d982b-131"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d982b-131"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d982b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d982b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d982b-133">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="d982b-133">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d982b-134">**IDirect3DDevice9:: CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="d982b-134">**IDirect3DDevice9::CreateStateBlock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

<span data-ttu-id="d982b-135">**IDirect3DDevice9:: CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="d982b-135">**IDirect3DDevice9::CreateStateBlock**</span></span>
</dt> </dl>

 

 
