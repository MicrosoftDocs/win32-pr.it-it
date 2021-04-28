---
description: 'DXGI_RGBA struttura : rappresenta un valore di colore con alfa, usato per la trasparenza.'
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: DXGI_RGBA struttura (DXGItype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: b0447d6470401d4136fbfd36f6d9c089e331b14b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114269"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="345a7-103">Struttura DXGI \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="345a7-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="345a7-104">Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="345a7-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="345a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="345a7-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="345a7-106">Members</span><span class="sxs-lookup"><span data-stu-id="345a7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="345a7-107">**r**</span><span class="sxs-lookup"><span data-stu-id="345a7-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="345a7-108">Valore a virgola mobile che specifica il componente rosso di un colore.</span><span class="sxs-lookup"><span data-stu-id="345a7-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="345a7-109">Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="345a7-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="345a7-110">Il valore 0,0 indica l'assenza completa del componente rosso, mentre un valore pari a 1,0 indica che il rosso è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="345a7-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="345a7-111">**G**</span><span class="sxs-lookup"><span data-stu-id="345a7-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="345a7-112">Valore a virgola mobile che specifica il componente verde di un colore.</span><span class="sxs-lookup"><span data-stu-id="345a7-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="345a7-113">Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="345a7-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="345a7-114">Il valore 0,0 indica l'assenza completa del componente verde, mentre un valore pari a 1,0 indica che il verde è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="345a7-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="345a7-115">**b**</span><span class="sxs-lookup"><span data-stu-id="345a7-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="345a7-116">Valore a virgola mobile che specifica il componente blu di un colore.</span><span class="sxs-lookup"><span data-stu-id="345a7-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="345a7-117">Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="345a7-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="345a7-118">Il valore 0,0 indica l'assenza completa del componente blu, mentre un valore pari a 1,0 indica che il blu è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="345a7-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="345a7-119">**Un**</span><span class="sxs-lookup"><span data-stu-id="345a7-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="345a7-120">Valore a virgola mobile che specifica il componente alfa di un colore.</span><span class="sxs-lookup"><span data-stu-id="345a7-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="345a7-121">Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="345a7-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="345a7-122">Un valore pari a 0,0 indica completamente trasparente, mentre un valore pari a 1,0 indica che è completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="345a7-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="345a7-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="345a7-123">Remarks</span></span>

<span data-ttu-id="345a7-124">È possibile impostare i membri di questa struttura su valori esterni all'intervallo compreso tra 0 e 1 per implementare alcuni effetti insoliti.</span><span class="sxs-lookup"><span data-stu-id="345a7-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="345a7-125">I valori maggiori di 1 producono luci forti che tendono a evase una scena.</span><span class="sxs-lookup"><span data-stu-id="345a7-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="345a7-126">I valori negativi producono luci scure che rimuovono effettivamente la luce da una scena.</span><span class="sxs-lookup"><span data-stu-id="345a7-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="345a7-127">L'intestazione DXGItype.h type definisce **DXGI \_ RGBA** come alias [**di D3DCOLORVALUE,**](d3dcolorvalue.md)come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="345a7-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="345a7-128">È possibile usare **DXGI \_ RGBA** [**con IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e [**DXGI \_ ALPHA \_ MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="345a7-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="345a7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="345a7-129">Requirements</span></span>



| <span data-ttu-id="345a7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="345a7-130">Requirement</span></span> | <span data-ttu-id="345a7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="345a7-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="345a7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="345a7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="345a7-133">Windows 8 e l'aggiornamento della piattaforma per le app desktop di Windows 7 \[ \| app UWP\]</span><span class="sxs-lookup"><span data-stu-id="345a7-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="345a7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="345a7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="345a7-135">Windows Server 2012 e l'aggiornamento della piattaforma per le app desktop di Windows Server 2008 R2 \[ \| app UWP\]</span><span class="sxs-lookup"><span data-stu-id="345a7-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="345a7-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="345a7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="345a7-137"><dt>DXGItype.h</dt></span><span class="sxs-lookup"><span data-stu-id="345a7-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="345a7-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="345a7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345a7-139">Strutture DXGI</span><span class="sxs-lookup"><span data-stu-id="345a7-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="345a7-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="345a7-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="345a7-141">**D3DCOLORVALUE (in Direct3D 9)**</span><span class="sxs-lookup"><span data-stu-id="345a7-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
