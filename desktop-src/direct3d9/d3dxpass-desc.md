---
description: Descrive un passaggio per un oggetto effetto.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: Struttura D3DXPASS_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354149"
---
# <a name="d3dxpass_desc-structure"></a><span data-ttu-id="e8431-103">\_Struttura D3DXPASS DESC</span><span class="sxs-lookup"><span data-stu-id="e8431-103">D3DXPASS\_DESC structure</span></span>

<span data-ttu-id="e8431-104">Descrive un passaggio per un oggetto effetto.</span><span class="sxs-lookup"><span data-stu-id="e8431-104">Describes a pass for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8431-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8431-105">Syntax</span></span>


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a><span data-ttu-id="e8431-106">Members</span><span class="sxs-lookup"><span data-stu-id="e8431-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e8431-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e8431-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="e8431-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8431-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e8431-109">Valore stringa utilizzato per il passaggio.</span><span class="sxs-lookup"><span data-stu-id="e8431-109">String value used for the pass.</span></span>

</dd> <dt>

<span data-ttu-id="e8431-110">**annotazioni**</span><span class="sxs-lookup"><span data-stu-id="e8431-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="e8431-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8431-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e8431-112">Le annotazioni sono dati specifici dell'utente che possono essere collegati a qualsiasi tecnica, passaggio o parametro.</span><span class="sxs-lookup"><span data-stu-id="e8431-112">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="e8431-113">Vedere [aggiungere informazioni ai parametri di effetto con le \_ annotazioni](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="e8431-113">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8431-114">**pVertexShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="e8431-114">**pVertexShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="e8431-115">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8431-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="e8431-116">Puntatore alla funzione vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e8431-116">Pointer to the vertex shader function.</span></span> <span data-ttu-id="e8431-117">Se viene creato un effetto con [D3DXFX \_ non \_ clonabile](d3dxfx.md), questa struttura restituirà un puntatore **null** quando viene chiamato da [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="e8431-117">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8431-118">**pPixelShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="e8431-118">**pPixelShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="e8431-119">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8431-119">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="e8431-120">Puntatore alla funzione pixel shader.</span><span class="sxs-lookup"><span data-stu-id="e8431-120">Pointer to the pixel shader function.</span></span> <span data-ttu-id="e8431-121">Se viene creato un effetto con [D3DXFX \_ non \_ clonabile](d3dxfx.md), questa struttura restituirà un puntatore **null** quando viene chiamato da [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="e8431-121">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8431-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8431-122">Requirements</span></span>



| <span data-ttu-id="e8431-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8431-123">Requirement</span></span> | <span data-ttu-id="e8431-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e8431-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8431-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8431-125">Header</span></span><br/> | <dl> <span data-ttu-id="e8431-126"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8431-126"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8431-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8431-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8431-128">Strutture degli effetti</span><span class="sxs-lookup"><span data-stu-id="e8431-128">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="e8431-129">**GetPassDesc**</span><span class="sxs-lookup"><span data-stu-id="e8431-129">**GetPassDesc**</span></span>](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
