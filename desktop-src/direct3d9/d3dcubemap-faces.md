---
description: Definisce le facce di un mappa cubi.
ms.assetid: 6d18b410-6f22-4202-86ae-6b3ef85e6f69
title: Enumerazione D3DCUBEMAP_FACES (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCUBEMAP_FACES
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: eaf482f6f98d695f3aea3198948616c05ed01f72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354404"
---
# <a name="d3dcubemap_faces-enumeration"></a><span data-ttu-id="b93ce-103">\_Enumerazione D3DCUBEMAP visi</span><span class="sxs-lookup"><span data-stu-id="b93ce-103">D3DCUBEMAP\_FACES enumeration</span></span>

<span data-ttu-id="b93ce-104">Definisce le facce di un mappa cubi.</span><span class="sxs-lookup"><span data-stu-id="b93ce-104">Defines the faces of a cubemap.</span></span>

## <a name="syntax"></a><span data-ttu-id="b93ce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b93ce-105">Syntax</span></span>


```C++
typedef enum D3DCUBEMAP_FACES { 
  D3DCUBEMAP_FACE_POSITIVE_X   = 0,
  D3DCUBEMAP_FACE_NEGATIVE_X   = 1,
  D3DCUBEMAP_FACE_POSITIVE_Y   = 2,
  D3DCUBEMAP_FACE_NEGATIVE_Y   = 3,
  D3DCUBEMAP_FACE_POSITIVE_Z   = 4,
  D3DCUBEMAP_FACE_NEGATIVE_Z   = 5,
  D3DCUBEMAP_FACE_FORCE_DWORD  = 0xffffffff
} D3DCUBEMAP_FACES, *LPD3DCUBEMAP_FACES;
```



## <a name="constants"></a><span data-ttu-id="b93ce-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="b93ce-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b93ce-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP \_ volto \_ positivo \_ X**</span><span class="sxs-lookup"><span data-stu-id="b93ce-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="b93ce-108">Faccia x positiva del mappa cubi.</span><span class="sxs-lookup"><span data-stu-id="b93ce-108">Positive x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="b93ce-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP \_ faccia \_ negativa \_ X**</span><span class="sxs-lookup"><span data-stu-id="b93ce-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="b93ce-110">La faccia x negativa del mappa cubi.</span><span class="sxs-lookup"><span data-stu-id="b93ce-110">Negative x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="b93ce-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**\_ \_ Y positivo D3DCUBEMAP \_ faccia**</span><span class="sxs-lookup"><span data-stu-id="b93ce-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="b93ce-112">Faccia y positiva del mappa cubi.</span><span class="sxs-lookup"><span data-stu-id="b93ce-112">Positive y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="b93ce-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**\_Y D3DCUBEMAP faccia \_ negativa \_**</span><span class="sxs-lookup"><span data-stu-id="b93ce-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="b93ce-114">Faccia y negativa del mappa cubi.</span><span class="sxs-lookup"><span data-stu-id="b93ce-114">Negative y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="b93ce-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP \_ volto \_ positivo \_ Z**</span><span class="sxs-lookup"><span data-stu-id="b93ce-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="b93ce-116">Quadrante z positivo del mappa cubi.</span><span class="sxs-lookup"><span data-stu-id="b93ce-116">Positive z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="b93ce-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP \_ faccia \_ \_ Z negativo**</span><span class="sxs-lookup"><span data-stu-id="b93ce-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="b93ce-118">Quadrante z negativo del mappa cubi.</span><span class="sxs-lookup"><span data-stu-id="b93ce-118">Negative z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="b93ce-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**\_DWORD D3DCUBEMAP Face \_ Force \_**</span><span class="sxs-lookup"><span data-stu-id="b93ce-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP\_FACE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b93ce-120">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b93ce-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b93ce-121">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b93ce-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b93ce-122">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b93ce-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b93ce-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b93ce-123">Requirements</span></span>



| <span data-ttu-id="b93ce-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b93ce-124">Requirement</span></span> | <span data-ttu-id="b93ce-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b93ce-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b93ce-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b93ce-126">Header</span></span><br/> | <dl> <span data-ttu-id="b93ce-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b93ce-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b93ce-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b93ce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b93ce-129">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="b93ce-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="b93ce-130">**IDirect3DCubeTexture9:: AddDirtyRect**</span><span class="sxs-lookup"><span data-stu-id="b93ce-130">**IDirect3DCubeTexture9::AddDirtyRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
</dt> <dt>

[<span data-ttu-id="b93ce-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span><span class="sxs-lookup"><span data-stu-id="b93ce-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
</dt> <dt>

[<span data-ttu-id="b93ce-132">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="b93ce-132">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="b93ce-133">**IDirect3DCubeTexture9::UnlockRect**</span><span class="sxs-lookup"><span data-stu-id="b93ce-133">**IDirect3DCubeTexture9::UnlockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-unlockrect)
</dt> </dl>

 

 
