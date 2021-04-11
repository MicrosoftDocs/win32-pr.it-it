---
description: Descrive una destinazione di rendering fuori schermo utilizzata da un'istanza di ID3DXRenderToEnvMap.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: Struttura D3DXRTE_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235005"
---
# <a name="d3dxrte_desc-structure"></a><span data-ttu-id="57898-103">\_Struttura D3DXRTE DESC</span><span class="sxs-lookup"><span data-stu-id="57898-103">D3DXRTE\_DESC structure</span></span>

<span data-ttu-id="57898-104">Descrive una destinazione di rendering fuori schermo utilizzata da un'istanza di [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span><span class="sxs-lookup"><span data-stu-id="57898-104">Describes an off-screen render target used by an instance of [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="57898-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57898-105">Syntax</span></span>


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a><span data-ttu-id="57898-106">Members</span><span class="sxs-lookup"><span data-stu-id="57898-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="57898-107">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="57898-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="57898-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57898-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57898-109">Larghezza e altezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="57898-109">Width and height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="57898-110">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="57898-110">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="57898-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57898-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57898-112">Numero massimo di livelli di dettaglio (LOD).</span><span class="sxs-lookup"><span data-stu-id="57898-112">Maximum level of detail (LOD) number.</span></span>

</dd> <dt>

<span data-ttu-id="57898-113">**Formato**</span><span class="sxs-lookup"><span data-stu-id="57898-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="57898-114">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="57898-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57898-115">Formato del buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="57898-115">Color buffer format.</span></span>

</dd> <dt>

<span data-ttu-id="57898-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="57898-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="57898-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57898-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57898-118">Indica se il buffer z è necessario.</span><span class="sxs-lookup"><span data-stu-id="57898-118">Indicates if the z-buffer is needed.</span></span>

</dd> <dt>

<span data-ttu-id="57898-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="57898-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="57898-120">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="57898-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57898-121">Formato del buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="57898-121">Format of the depth buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57898-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="57898-122">Remarks</span></span>

<span data-ttu-id="57898-123">Questo metodo viene utilizzato per restituire i parametri di creazione utilizzati durante la creazione di un oggetto [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="57898-123">This method is used to return the creation parameters used when creating an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="57898-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57898-124">Requirements</span></span>



| <span data-ttu-id="57898-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="57898-125">Requirement</span></span> | <span data-ttu-id="57898-126">Valore</span><span class="sxs-lookup"><span data-stu-id="57898-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57898-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57898-127">Header</span></span><br/> | <dl> <span data-ttu-id="57898-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="57898-128"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57898-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57898-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57898-130">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="57898-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
