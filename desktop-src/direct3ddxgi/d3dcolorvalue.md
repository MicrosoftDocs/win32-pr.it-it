---
description: 'Struttura D3DCOLORVALUE (Dxgitype.h): rappresenta un valore di colore con alfa, usato per la trasparenza.'
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: Struttura D3DCOLORVALUE (Dxgitype.h)
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
ms.openlocfilehash: 83ca500493a04f04de5352185c240d20a19009f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107149"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="119cf-103">Struttura D3DCOLORVALUE (Dxgitype.h)</span><span class="sxs-lookup"><span data-stu-id="119cf-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="119cf-104">Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="119cf-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="119cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="119cf-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="119cf-106">Members</span><span class="sxs-lookup"><span data-stu-id="119cf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="119cf-107">**r**</span><span class="sxs-lookup"><span data-stu-id="119cf-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="119cf-108">Valore a virgola mobile che specifica il componente rosso di un colore.</span><span class="sxs-lookup"><span data-stu-id="119cf-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="119cf-109">Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="119cf-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="119cf-110">Il valore 0,0 indica l'assenza completa del componente rosso, mentre un valore pari a 1,0 indica che il rosso è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="119cf-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="119cf-111">**G**</span><span class="sxs-lookup"><span data-stu-id="119cf-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="119cf-112">Valore a virgola mobile che specifica il componente verde di un colore.</span><span class="sxs-lookup"><span data-stu-id="119cf-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="119cf-113">Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="119cf-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="119cf-114">Il valore 0,0 indica l'assenza completa del componente verde, mentre un valore pari a 1,0 indica che il verde è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="119cf-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="119cf-115">**b**</span><span class="sxs-lookup"><span data-stu-id="119cf-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="119cf-116">Valore a virgola mobile che specifica il componente blu di un colore.</span><span class="sxs-lookup"><span data-stu-id="119cf-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="119cf-117">Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="119cf-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="119cf-118">Il valore 0,0 indica l'assenza completa del componente blu, mentre un valore 1,0 indica che il blu è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="119cf-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="119cf-119">**Un**</span><span class="sxs-lookup"><span data-stu-id="119cf-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="119cf-120">Valore a virgola mobile che specifica il componente alfa di un colore.</span><span class="sxs-lookup"><span data-stu-id="119cf-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="119cf-121">Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="119cf-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="119cf-122">Un valore pari a 0,0 indica completamente trasparente, mentre un valore pari a 1,0 indica che è completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="119cf-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="119cf-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="119cf-123">Remarks</span></span>

<span data-ttu-id="119cf-124">È possibile impostare i membri di questa struttura su valori esterni all'intervallo compreso tra 0 e 1 per implementare alcuni effetti insoliti.</span><span class="sxs-lookup"><span data-stu-id="119cf-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="119cf-125">I valori maggiori di 1 producono luci forti che tendono a evase una scena.</span><span class="sxs-lookup"><span data-stu-id="119cf-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="119cf-126">I valori negativi producono luci scure che rimuovono effettivamente la luce da una scena.</span><span class="sxs-lookup"><span data-stu-id="119cf-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="119cf-127">L'intestazione DXGItype.h type definisce [**DXGI \_ RGBA**](dxgi-rgba.md) come alias **di D3DCOLORVALUE,** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="119cf-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="119cf-128">È possibile usare D3DCOLORVALUE o [**DXGI \_ RGBA**](dxgi-rgba.md) con [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e [**DXGI \_ ALPHA \_ MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="119cf-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="119cf-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="119cf-129">Requirements</span></span>



| <span data-ttu-id="119cf-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="119cf-130">Requirement</span></span> | <span data-ttu-id="119cf-131">Valore</span><span class="sxs-lookup"><span data-stu-id="119cf-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="119cf-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="119cf-132">Header</span></span><br/> | <dl> <span data-ttu-id="119cf-133"><dt>Dxgitype.h</dt></span><span class="sxs-lookup"><span data-stu-id="119cf-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="119cf-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="119cf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119cf-135">Strutture DXGI</span><span class="sxs-lookup"><span data-stu-id="119cf-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="119cf-136">**DXGI \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="119cf-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




