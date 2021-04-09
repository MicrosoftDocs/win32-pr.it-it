---
title: D2D1_RECT_F (D2DBaseTypes. h)
description: Rappresenta un rettangolo definito dalle coordinate dell'angolo superiore sinistro (a sinistra, superiore) e le coordinate dell'angolo inferiore destro (a destra, in basso). | D2D1_RECT_F (D2DBaseTypes. h)
ms.assetid: a961c0e3-fb76-4c07-b76e-47d8c09ada08
keywords:
- D2D1_RECT_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93ce4700e093b9e82fd4334ae9e01485a7fcbb4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058510"
---
# <a name="d2d1_rect_f"></a><span data-ttu-id="448b2-105">D2D1 \_ Rect \_ F</span><span class="sxs-lookup"><span data-stu-id="448b2-105">D2D1\_RECT\_F</span></span>

<span data-ttu-id="448b2-106">Rappresenta un rettangolo definito dalle coordinate dell'angolo superiore sinistro (a sinistra, superiore) e le coordinate dell'angolo inferiore destro (a destra, in basso).</span><span class="sxs-lookup"><span data-stu-id="448b2-106">Represents a rectangle defined by the coordinates of the upper-left corner (left, top) and the coordinates of the lower-right corner (right, bottom).</span></span>


```C++
typedef D2D_RECT_F D2D1_RECT_F;
```



## <a name="remarks"></a><span data-ttu-id="448b2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="448b2-107">Remarks</span></span>

<span data-ttu-id="448b2-108">**D2d1 \_ RECT \_ f** è un nuovo nome per lo struct [**D2D \_ Rect \_ f**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) già definito.</span><span class="sxs-lookup"><span data-stu-id="448b2-108">**D2D1\_RECT\_F** is a new name for the already defined [**D2D\_RECT\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) struct.</span></span>

## <a name="examples"></a><span data-ttu-id="448b2-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="448b2-109">Examples</span></span>

<span data-ttu-id="448b2-110">Nell'esempio seguente viene usato un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) per creare e riempire diversi rettangoli.</span><span class="sxs-lookup"><span data-stu-id="448b2-110">The following example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw and fill several rectangles.</span></span> <span data-ttu-id="448b2-111">Questo esempio genera un output come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="448b2-111">This example produces output as shown in the following illustration.</span></span>

![illustrazione di due rettangoli sullo sfondo di una griglia](images/drawrectangleexample-small.png)


```C++
// This method discards device-specific
// resources if the Direct3D device dissapears during execution and
// recreates the resources the next time it's invoked.
HRESULT DemoApp::OnRender()
{
    HRESULT hr = S_OK;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();

        // Draw a grid background.
        int width = static_cast<int>(rtSize.width);
        int height = static_cast<int>(rtSize.height);

        for (int x = 0; x < width; x += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y < height; y += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        // Draw two rectangles.
        D2D1_RECT_F rectangle1 = D2D1::RectF(
            rtSize.width/2 - 50.0f,
            rtSize.height/2 - 50.0f,
            rtSize.width/2 + 50.0f,
            rtSize.height/2 + 50.0f
            );

        D2D1_RECT_F rectangle2 = D2D1::RectF(
            rtSize.width/2 - 100.0f,
            rtSize.height/2 - 100.0f,
            rtSize.width/2 + 100.0f,
            rtSize.height/2 + 100.0f
            );


        // Draw a filled rectangle.
        m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);

        hr = m_pRenderTarget->EndDraw();
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="448b2-113">Per un'esercitazione correlata, vedere [creazione di una semplice applicazione Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="448b2-113">For a related tutorial, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="448b2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="448b2-114">Requirements</span></span>



| <span data-ttu-id="448b2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="448b2-115">Requirement</span></span> | <span data-ttu-id="448b2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="448b2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="448b2-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="448b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="448b2-118">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="448b2-118">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="448b2-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="448b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="448b2-120">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="448b2-120">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="448b2-121">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="448b2-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="448b2-122">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="448b2-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="448b2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="448b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="448b2-124"><dt>D2DBaseTypes. h (include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="448b2-124"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="448b2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="448b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448b2-126">**D2D \_ Rect \_ F**</span><span class="sxs-lookup"><span data-stu-id="448b2-126">**D2D\_RECT\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f)
</dt> <dt>

[<span data-ttu-id="448b2-127">Creazione di un'applicazione Direct2D semplice</span><span class="sxs-lookup"><span data-stu-id="448b2-127">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

