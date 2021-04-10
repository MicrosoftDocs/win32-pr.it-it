---
title: Come creare un pennello tinta unita
description: Viene illustrato come creare un pennello tinta unita utilizzando Direct2D.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bc6fbf5df42386f5e0e5a843a1906d36d4fc8c71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963165"
---
# <a name="how-to-create-a-solid-color-brush"></a><span data-ttu-id="148b1-103">Come creare un pennello tinta unita</span><span class="sxs-lookup"><span data-stu-id="148b1-103">How to Create a Solid Color Brush</span></span>

<span data-ttu-id="148b1-104">Per creare un pennello tinta unita, utilizzare il metodo [**ID2DRenderTarget:: CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) e specificare il colore con cui si desidera disegnare.</span><span class="sxs-lookup"><span data-stu-id="148b1-104">To create a solid color brush, use the [**ID2DRenderTarget::CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method and specify the color with which you want to paint.</span></span> <span data-ttu-id="148b1-105">Alcuni overload di **CreateSolidColorBrush** consentono inoltre di specificare l'opacità del pennello.</span><span class="sxs-lookup"><span data-stu-id="148b1-105">Some of the **CreateSolidColorBrush** overloads also enable you to specify the opacity of the brush.</span></span>

<span data-ttu-id="148b1-106">Il codice seguente illustra come creare un pennello verde giallo per riempire un quadrato e un pennello nero a tinta unita per disegnare il contorno del quadrato.</span><span class="sxs-lookup"><span data-stu-id="148b1-106">The following code shows how to create a solid yellow-green brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="148b1-107">Il codice produce l'output illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="148b1-107">The code produces the output shown in the following illustration.</span></span>

![illustrazione di un rettangolo riempito con un colore giallo verde tinta unita](images/brushes-ovw-solidcolor.png)

1.  <span data-ttu-id="148b1-109">Dichiarare due puntatori [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) : uno per disegnare il nero e uno per disegnare il verde giallo.</span><span class="sxs-lookup"><span data-stu-id="148b1-109">Declare two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pointers: one for painting black and one for painting yellow green.</span></span>
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  <span data-ttu-id="148b1-110">Chiamare il metodo [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) per creare i pennelli:</span><span class="sxs-lookup"><span data-stu-id="148b1-110">Call the [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method to create the brushes:</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
            &m_pBlackBrush
            );
    }

    // Create a solid color brush with its rgb value 0x9ACD32.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
            &m_pYellowGreenBrush
            );
    }
    ```

    

3.  <span data-ttu-id="148b1-111">Chiamare il metodo [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) per disegnare l'interno del rettangolo con il pennello verde giallo e il metodo [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) per disegnare il contorno del rettangolo con il pennello nero:</span><span class="sxs-lookup"><span data-stu-id="148b1-111">Call the [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the rectangle with the yellow green brush and the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the rectangle with the black brush:</span></span>
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="148b1-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="148b1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="148b1-113">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="148b1-113">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 