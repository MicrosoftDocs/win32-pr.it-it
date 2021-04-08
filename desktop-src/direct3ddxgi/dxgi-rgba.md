---
description: Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: Struttura DXGI_RGBA (DXGItype. h)
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
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746767"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="4d76f-103">\_Struttura DXGI RGBA</span><span class="sxs-lookup"><span data-stu-id="4d76f-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="4d76f-104">Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="4d76f-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d76f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d76f-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="4d76f-106">Members</span><span class="sxs-lookup"><span data-stu-id="4d76f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d76f-107">**r**</span><span class="sxs-lookup"><span data-stu-id="4d76f-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="4d76f-108">Valore a virgola mobile che specifica il componente rosso di un colore.</span><span class="sxs-lookup"><span data-stu-id="4d76f-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="4d76f-109">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="4d76f-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="4d76f-110">Il valore 0,0 indica l'assenza completa del componente rosso, mentre un valore pari a 1,0 indica che il colore rosso è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="4d76f-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="4d76f-111">**g**</span><span class="sxs-lookup"><span data-stu-id="4d76f-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="4d76f-112">Valore a virgola mobile che specifica il componente verde di un colore.</span><span class="sxs-lookup"><span data-stu-id="4d76f-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="4d76f-113">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="4d76f-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="4d76f-114">Il valore 0,0 indica l'assenza completa del componente verde, mentre un valore pari a 1,0 indica che il verde è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="4d76f-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="4d76f-115">**b**</span><span class="sxs-lookup"><span data-stu-id="4d76f-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="4d76f-116">Valore a virgola mobile che specifica il componente blu di un colore.</span><span class="sxs-lookup"><span data-stu-id="4d76f-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="4d76f-117">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="4d76f-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="4d76f-118">Il valore 0,0 indica l'assenza completa del componente blu, mentre il valore 1,0 indica che il blu è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="4d76f-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="4d76f-119">**un**</span><span class="sxs-lookup"><span data-stu-id="4d76f-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="4d76f-120">Valore a virgola mobile che specifica il componente alfa di un colore.</span><span class="sxs-lookup"><span data-stu-id="4d76f-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="4d76f-121">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="4d76f-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="4d76f-122">Il valore 0,0 indica completamente trasparente, mentre un valore pari a 1,0 indica una piena opacità.</span><span class="sxs-lookup"><span data-stu-id="4d76f-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d76f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d76f-123">Remarks</span></span>

<span data-ttu-id="4d76f-124">È possibile impostare i membri di questa struttura su valori non compresi nell'intervallo compreso tra 0 e 1 per implementare alcuni effetti insoliti.</span><span class="sxs-lookup"><span data-stu-id="4d76f-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="4d76f-125">I valori maggiori di 1 producono luci forti che tendono a pulire una scena.</span><span class="sxs-lookup"><span data-stu-id="4d76f-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="4d76f-126">I valori negativi producono luci scure che effettivamente rimuovono la luce da una scena.</span><span class="sxs-lookup"><span data-stu-id="4d76f-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="4d76f-127">Il tipo di intestazione DXGItype. h definisce **DXGI \_ RGBA** come alias di [**D3DCOLORVALUE**](d3dcolorvalue.md), come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="4d76f-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="4d76f-128">È possibile usare **DXGI \_ RGBA** con la modalità [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e [**DXGI \_ Alpha \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="4d76f-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d76f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d76f-129">Requirements</span></span>



| <span data-ttu-id="4d76f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d76f-130">Requirement</span></span> | <span data-ttu-id="4d76f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="4d76f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d76f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d76f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4d76f-133">Windows 8 e aggiornamento della piattaforma per le app desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4d76f-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4d76f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d76f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4d76f-135">Windows Server 2012 e aggiornamento della piattaforma per le app desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4d76f-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="4d76f-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d76f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d76f-137"><dt>DXGItype. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d76f-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="4d76f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d76f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d76f-139">Strutture DXGI</span><span class="sxs-lookup"><span data-stu-id="4d76f-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="4d76f-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="4d76f-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="4d76f-141">**D3DCOLORVALUE (in Direct3D 9)**</span><span class="sxs-lookup"><span data-stu-id="4d76f-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
