---
title: Struttura D3DX11_TECHNIQUE_DESC (D3dx11effect. h)
description: Descrive una tecnica di effetto.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- Struttura D3DX11_TECHNIQUE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762179"
---
# <a name="d3dx11_technique_desc-structure"></a><span data-ttu-id="70141-104">\_Struttura D3DX11 Technique \_ DESC</span><span class="sxs-lookup"><span data-stu-id="70141-104">D3DX11\_TECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="70141-105">Descrive una tecnica di effetto.</span><span class="sxs-lookup"><span data-stu-id="70141-105">Describes an effect technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="70141-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70141-106">Syntax</span></span>


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="70141-107">Members</span><span class="sxs-lookup"><span data-stu-id="70141-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="70141-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="70141-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="70141-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70141-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="70141-110">Nome di questa tecnica (NULL se non anonimo).</span><span class="sxs-lookup"><span data-stu-id="70141-110">Name of this technique (NULL if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="70141-111">**Passa**</span><span class="sxs-lookup"><span data-stu-id="70141-111">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="70141-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70141-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="70141-113">Numero di passaggi contenuti nella tecnica.</span><span class="sxs-lookup"><span data-stu-id="70141-113">Number of passes contained in the technique.</span></span>

</dd> <dt>

<span data-ttu-id="70141-114">**annotazioni**</span><span class="sxs-lookup"><span data-stu-id="70141-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="70141-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70141-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="70141-116">Numero di annotazioni su questa tecnica.</span><span class="sxs-lookup"><span data-stu-id="70141-116">Number of annotations on this technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70141-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="70141-117">Remarks</span></span>

<span data-ttu-id="70141-118">D3DX11 \_ Technique \_ desc viene usato con [**ID3DX11EffectTechnique:: getdesc**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="70141-118">D3DX11\_TECHNIQUE\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70141-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70141-119">Requirements</span></span>



| <span data-ttu-id="70141-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="70141-120">Requirement</span></span> | <span data-ttu-id="70141-121">Valore</span><span class="sxs-lookup"><span data-stu-id="70141-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="70141-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70141-122">Header</span></span><br/> | <dl> <span data-ttu-id="70141-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="70141-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70141-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70141-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70141-125">Strutture Effects 11</span><span class="sxs-lookup"><span data-stu-id="70141-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

