---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Memorizza una coppia ordinata di interi, generalmente la larghezza e l'altezza di un rettangolo.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119311"
---
# <a name="d2d1_size_u"></a><span data-ttu-id="7bed5-104">D2D1 \_ dimensioni \_ U</span><span class="sxs-lookup"><span data-stu-id="7bed5-104">D2D1\_SIZE\_U</span></span>

<span data-ttu-id="7bed5-105">Memorizza una coppia ordinata di interi, generalmente la larghezza e l'altezza di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="7bed5-105">Stores an ordered pair of integers, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a><span data-ttu-id="7bed5-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bed5-106">Remarks</span></span>

<span data-ttu-id="7bed5-107">Analogamente ai punti, le dimensioni rappresentano un altro concetto di grafica importante.</span><span class="sxs-lookup"><span data-stu-id="7bed5-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="7bed5-108">In Direct2D le dimensioni sono rappresentate dalle strutture della dimensione **d2d1 \_ \_ U** o [**d2d1 \_ \_ F**](d2d1-size-f.md) .</span><span class="sxs-lookup"><span data-stu-id="7bed5-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_U** or [**D2D1\_SIZE\_F**](d2d1-size-f.md) structures.</span></span> <span data-ttu-id="7bed5-109">Entrambi contengono una coppia ordinata di numeri.</span><span class="sxs-lookup"><span data-stu-id="7bed5-109">They both contain an ordered pair of numbers.</span></span> <span data-ttu-id="7bed5-110">La struttura **d2d1 della \_ dimensione \_ U** contiene una coppia ordinata di valori **UInt32** e la struttura **d2d1 \_ size \_ F** contiene una coppia ordinata di valori **float** .</span><span class="sxs-lookup"><span data-stu-id="7bed5-110">The **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values, and the **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values.</span></span>

<span data-ttu-id="7bed5-111">La **struttura \_ \_ U della dimensione d2d1** rappresenta un modo pratico per archiviare una coppia ordinata di numeri, ad esempio la larghezza e l'altezza di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="7bed5-111">The **D2D1\_SIZE\_U** structure provides a convenient way for you to store an ordered pair of numbers, such as the width and height of a rectangle.</span></span>

<span data-ttu-id="7bed5-112">**D2d1 \_ SIZE \_ u** è un nuovo nome per un tipo già definito **D2D \_ size \_ u**.</span><span class="sxs-lookup"><span data-stu-id="7bed5-112">**D2D1\_SIZE\_U** is a new name for an already defined type **D2D\_SIZE\_U**.</span></span> <span data-ttu-id="7bed5-113">È possibile usare la funzione **D2D1:: dimensionat** per creare una **struttura \_ \_ U d2d1 size** .</span><span class="sxs-lookup"><span data-stu-id="7bed5-113">You can use the **D2D1::SizeU** function to create a **D2D1\_SIZE\_U** structure.</span></span> <span data-ttu-id="7bed5-114">Un uso comune di questa struttura è quello di specificare le dimensioni in pixel di una struttura di [**\_ proprietà della \_ \_ destinazione \_ di rendering HWND d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) .</span><span class="sxs-lookup"><span data-stu-id="7bed5-114">A common use for this structure is to specify the pixel size of a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) structure.</span></span> <span data-ttu-id="7bed5-115">Di seguito viene fornito un esempio di utilizzo di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="7bed5-115">The following provides an example of using this structure.</span></span>


```C++
    if (!m_pRenderTarget)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top
            );

        // Create a Direct2D render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



## <a name="requirements"></a><span data-ttu-id="7bed5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bed5-116">Requirements</span></span>



| <span data-ttu-id="7bed5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bed5-117">Requirement</span></span> | <span data-ttu-id="7bed5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7bed5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bed5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bed5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7bed5-120">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7bed5-120">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="7bed5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bed5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7bed5-122">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7bed5-122">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="7bed5-123">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bed5-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="7bed5-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="7bed5-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="7bed5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7bed5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bed5-126"><dt>D2DBaseTypes. h (include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bed5-126"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7bed5-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bed5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bed5-128">**D2D \_ dimensioni \_ U**</span><span class="sxs-lookup"><span data-stu-id="7bed5-128">**D2D\_SIZE\_U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[<span data-ttu-id="7bed5-129">**\_Dimensioni d2d1 \_ F**</span><span class="sxs-lookup"><span data-stu-id="7bed5-129">**D2D1\_SIZE\_F**</span></span>](d2d1-size-f.md)
</dt> <dt>

[<span data-ttu-id="7bed5-130">**D2D1:: HwndRenderTargetProperties**</span><span class="sxs-lookup"><span data-stu-id="7bed5-130">**D2D1::HwndRenderTargetProperties**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

