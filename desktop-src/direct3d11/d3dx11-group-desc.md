---
title: Struttura D3DX11_GROUP_DESC (D3dx11effect. h)
description: Descrive un gruppo di effetti.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- Struttura D3DX11_GROUP_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058690"
---
# <a name="d3dx11_group_desc-structure"></a><span data-ttu-id="254a8-104">\_Struttura Desc del gruppo D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="254a8-104">D3DX11\_GROUP\_DESC structure</span></span>

<span data-ttu-id="254a8-105">Descrive un gruppo di effetti.</span><span class="sxs-lookup"><span data-stu-id="254a8-105">Describes an effect group.</span></span>

## <a name="syntax"></a><span data-ttu-id="254a8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="254a8-106">Syntax</span></span>


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a><span data-ttu-id="254a8-107">Members</span><span class="sxs-lookup"><span data-stu-id="254a8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="254a8-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="254a8-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="254a8-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="254a8-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="254a8-110">Nome del gruppo ( **null** solo se globale).</span><span class="sxs-lookup"><span data-stu-id="254a8-110">Name of this group (only **NULL** if global).</span></span>

</dd> <dt>

<span data-ttu-id="254a8-111">**Tecniche**</span><span class="sxs-lookup"><span data-stu-id="254a8-111">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="254a8-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="254a8-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="254a8-113">Numero di tecniche contenute nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="254a8-113">Number of techniques contained in group.</span></span>

</dd> <dt>

<span data-ttu-id="254a8-114">**annotazioni**</span><span class="sxs-lookup"><span data-stu-id="254a8-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="254a8-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="254a8-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="254a8-116">Numero di annotazioni in questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="254a8-116">Number of annotations on this group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="254a8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="254a8-117">Remarks</span></span>

<span data-ttu-id="254a8-118">Il \_ gruppo D3DX11 \_ desc viene usato con [**ID3DX11EffectTechnique:: getdesc**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="254a8-118">D3DX11\_GROUP\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="254a8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="254a8-119">Requirements</span></span>



| <span data-ttu-id="254a8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="254a8-120">Requirement</span></span> | <span data-ttu-id="254a8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="254a8-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="254a8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="254a8-122">Header</span></span><br/> | <dl> <span data-ttu-id="254a8-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="254a8-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="254a8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="254a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="254a8-125">Strutture Effects 11</span><span class="sxs-lookup"><span data-stu-id="254a8-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

