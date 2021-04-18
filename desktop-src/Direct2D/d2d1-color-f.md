---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Descrive i componenti rosso, verde, blu e alfa di un colore. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321471"
---
# <a name="d2d1_color_f"></a><span data-ttu-id="2cbd3-105">D2D1 \_ colore \_ F</span><span class="sxs-lookup"><span data-stu-id="2cbd3-105">D2D1\_COLOR\_F</span></span>

<span data-ttu-id="2cbd3-106">Descrive i componenti rosso, verde, blu e alfa di un colore.</span><span class="sxs-lookup"><span data-stu-id="2cbd3-106">Describes the red, green, blue, and alpha components of a color.</span></span>


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a><span data-ttu-id="2cbd3-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cbd3-107">Remarks</span></span>

<span data-ttu-id="2cbd3-108">**D2d1 \_ COLOR \_ f** è un typedef per [**D2D \_ Color \_ f**](d2d-color-f.md), che è a sua volta un typedef per [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="2cbd3-108">**D2D1\_COLOR\_F** is a typedef for [**D2D\_COLOR\_F**](d2d-color-f.md), which is itself a typedef for [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span> <span data-ttu-id="2cbd3-109">Per informazioni sui membri forniti da **d2d1 \_ Color \_ F**, vedere [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="2cbd3-109">For information about the members provided by **D2D1\_COLOR\_F**, see [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span>

<span data-ttu-id="2cbd3-110">La classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) fornisce un set di colori e funzioni di supporto predefiniti per la definizione dei colori.</span><span class="sxs-lookup"><span data-stu-id="2cbd3-110">The [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class provides a set of predefined colors and helper functions for defining colors.</span></span> <span data-ttu-id="2cbd3-111">Per ulteriori informazioni, vedere la Guida di riferimento a [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="2cbd3-111">For more information, see the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) reference.</span></span>

## <a name="examples"></a><span data-ttu-id="2cbd3-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="2cbd3-112">Examples</span></span>

<span data-ttu-id="2cbd3-113">Nell'esempio seguente viene usata la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) per specificare un colore predefinito (nero) durante la creazione di un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="2cbd3-113">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a predefined color (black) when creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



<span data-ttu-id="2cbd3-114">Nell'esempio seguente viene utilizzata la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) per specificare un colore utilizzando i valori rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="2cbd3-114">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a color using red, green, blue, and alpha values.</span></span>


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a><span data-ttu-id="2cbd3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cbd3-115">Requirements</span></span>



| <span data-ttu-id="2cbd3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cbd3-116">Requirement</span></span> | <span data-ttu-id="2cbd3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2cbd3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbd3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cbd3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2cbd3-119">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2cbd3-119">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2cbd3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cbd3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2cbd3-121">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2cbd3-121">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2cbd3-122">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cbd3-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2cbd3-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="2cbd3-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="2cbd3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cbd3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cbd3-125"><dt>D2DBaseTypes. h (include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2cbd3-125"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2cbd3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cbd3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbd3-127">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="2cbd3-127">D3DCOLORVALUE</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="2cbd3-128">**ColorF**</span><span class="sxs-lookup"><span data-stu-id="2cbd3-128">**ColorF**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

