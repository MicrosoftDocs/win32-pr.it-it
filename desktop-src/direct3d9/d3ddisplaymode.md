---
description: Descrive la modalità di visualizzazione.
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: Struttura D3DDISPLAYMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132310"
---
# <a name="d3ddisplaymode-structure"></a><span data-ttu-id="b3c39-103">Struttura D3DDISPLAYMODE</span><span class="sxs-lookup"><span data-stu-id="b3c39-103">D3DDISPLAYMODE structure</span></span>

<span data-ttu-id="b3c39-104">Descrive la modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b3c39-104">Describes the display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c39-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3c39-105">Syntax</span></span>


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a><span data-ttu-id="b3c39-106">Members</span><span class="sxs-lookup"><span data-stu-id="b3c39-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3c39-107">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="b3c39-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="b3c39-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3c39-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b3c39-109">Larghezza dello schermo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="b3c39-109">Screen width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b3c39-110">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="b3c39-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="b3c39-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3c39-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b3c39-112">Altezza dello schermo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="b3c39-112">Screen height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b3c39-113">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="b3c39-113">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="b3c39-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3c39-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b3c39-115">Frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b3c39-115">Refresh rate.</span></span> <span data-ttu-id="b3c39-116">Il valore 0 indica l'impostazione predefinita di un adapter.</span><span class="sxs-lookup"><span data-stu-id="b3c39-116">The value of 0 indicates an adapter default.</span></span>

</dd> <dt>

<span data-ttu-id="b3c39-117">**Formato**</span><span class="sxs-lookup"><span data-stu-id="b3c39-117">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="b3c39-118">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b3c39-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b3c39-119">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato di superficie della modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b3c39-119">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the display mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3c39-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3c39-120">Requirements</span></span>



| <span data-ttu-id="b3c39-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c39-121">Requirement</span></span> | <span data-ttu-id="b3c39-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b3c39-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c39-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3c39-123">Header</span></span><br/> | <dl> <span data-ttu-id="b3c39-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c39-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c39-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3c39-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c39-126">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="b3c39-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="b3c39-127">**EnumAdapterModes**</span><span class="sxs-lookup"><span data-stu-id="b3c39-127">**EnumAdapterModes**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[<span data-ttu-id="b3c39-128">**GetAdapterDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="b3c39-128">**GetAdapterDisplayMode**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[<span data-ttu-id="b3c39-129">**GetDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="b3c39-129">**GetDisplayMode**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
