---
description: Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: Struttura D3DCOLORVALUE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354759"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="671a6-103">Struttura D3DCOLORVALUE (Dxgitype. h)</span><span class="sxs-lookup"><span data-stu-id="671a6-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="671a6-104">Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="671a6-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="671a6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="671a6-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="671a6-106">Members</span><span class="sxs-lookup"><span data-stu-id="671a6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="671a6-107">**r**</span><span class="sxs-lookup"><span data-stu-id="671a6-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="671a6-108">Valore a virgola mobile che specifica il componente rosso di un colore.</span><span class="sxs-lookup"><span data-stu-id="671a6-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="671a6-109">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="671a6-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="671a6-110">Il valore 0,0 indica l'assenza completa del componente rosso, mentre un valore pari a 1,0 indica che il colore rosso è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="671a6-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="671a6-111">**g**</span><span class="sxs-lookup"><span data-stu-id="671a6-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="671a6-112">Valore a virgola mobile che specifica il componente verde di un colore.</span><span class="sxs-lookup"><span data-stu-id="671a6-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="671a6-113">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="671a6-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="671a6-114">Il valore 0,0 indica l'assenza completa del componente verde, mentre un valore pari a 1,0 indica che il verde è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="671a6-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="671a6-115">**b**</span><span class="sxs-lookup"><span data-stu-id="671a6-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="671a6-116">Valore a virgola mobile che specifica il componente blu di un colore.</span><span class="sxs-lookup"><span data-stu-id="671a6-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="671a6-117">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="671a6-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="671a6-118">Il valore 0,0 indica l'assenza completa del componente blu, mentre il valore 1,0 indica che il blu è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="671a6-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="671a6-119">**un**</span><span class="sxs-lookup"><span data-stu-id="671a6-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="671a6-120">Valore a virgola mobile che specifica il componente alfa di un colore.</span><span class="sxs-lookup"><span data-stu-id="671a6-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="671a6-121">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="671a6-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="671a6-122">Il valore 0,0 indica completamente trasparente, mentre un valore pari a 1,0 indica una piena opacità.</span><span class="sxs-lookup"><span data-stu-id="671a6-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="671a6-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="671a6-123">Remarks</span></span>

<span data-ttu-id="671a6-124">È possibile impostare i membri di questa struttura su valori non compresi nell'intervallo compreso tra 0 e 1 per implementare alcuni effetti insoliti.</span><span class="sxs-lookup"><span data-stu-id="671a6-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="671a6-125">I valori maggiori di 1 producono luci forti che tendono a pulire una scena.</span><span class="sxs-lookup"><span data-stu-id="671a6-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="671a6-126">I valori negativi producono luci scure che effettivamente rimuovono la luce da una scena.</span><span class="sxs-lookup"><span data-stu-id="671a6-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="671a6-127">Il tipo di intestazione DXGItype. h definisce [**DXGI \_ RGBA**](dxgi-rgba.md) come alias di **D3DCOLORVALUE**, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="671a6-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="671a6-128">È possibile usare D3DCOLORVALUE o [**DXGI \_ RGBA**](dxgi-rgba.md) con la modalità [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e [**DXGI \_ Alpha \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="671a6-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="671a6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="671a6-129">Requirements</span></span>



| <span data-ttu-id="671a6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="671a6-130">Requirement</span></span> | <span data-ttu-id="671a6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="671a6-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="671a6-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="671a6-132">Header</span></span><br/> | <dl> <span data-ttu-id="671a6-133"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="671a6-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671a6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="671a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671a6-135">Strutture DXGI</span><span class="sxs-lookup"><span data-stu-id="671a6-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="671a6-136">**\_RGBA DXGI**</span><span class="sxs-lookup"><span data-stu-id="671a6-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




