---
title: Come ritagliare con un rettangolo di ritaglio Axis-Aligned
description: Mostra come ritagliare un'area con un rettangolo di ritaglio allineato all'asse.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551595"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a><span data-ttu-id="45f05-103">Come ritagliare con un rettangolo di ritaglio Axis-Aligned</span><span class="sxs-lookup"><span data-stu-id="45f05-103">How to Clip with an Axis-Aligned Clip Rectangle</span></span>

<span data-ttu-id="45f05-104">In questo argomento viene descritto come ritagliare un'immagine con un rettangolo di ritaglio allineato all'asse.</span><span class="sxs-lookup"><span data-stu-id="45f05-104">This topic describes how to clip an image with an axis-aligned clip rectangle.</span></span> <span data-ttu-id="45f05-105">Questo approccio produce solo clip rettangolari, perché i limiti del contenuto sono allineati all'asse del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="45f05-105">This approach produces only rectangular clips, because the content bounds are aligned to the axis of the rectangle.</span></span> <span data-ttu-id="45f05-106">Questo approccio è più efficiente rispetto all'uso di livelli con i limiti di contenuto.</span><span class="sxs-lookup"><span data-stu-id="45f05-106">This approach is more efficient than using layers with the content bounds.</span></span> <span data-ttu-id="45f05-107">Per altre informazioni, vedere[Cenni preliminari sui livelli](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="45f05-107">For more information, see[Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="45f05-108">**Per ritagliare un rettangolo di ritaglio allineato all'asse**</span><span class="sxs-lookup"><span data-stu-id="45f05-108">**To clip with an axis-aligned clip rectangle**</span></span>

1.  <span data-ttu-id="45f05-109">Caricare l'immagine originale da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="45f05-109">Load the original image from a resource.</span></span> <span data-ttu-id="45f05-110">Per informazioni su come caricare una bitmap, vedere [come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="45f05-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="45f05-111">Chiamare [**ID2D1RenderTarget::P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) per specificare un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="45f05-111">Call [**ID2D1RenderTarget::PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) to specify a rectangle.</span></span> <span data-ttu-id="45f05-112">I comandi di rendering vengono ritagliati nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="45f05-112">The rendering commands are clipped to the rectangle.</span></span>

3.  <span data-ttu-id="45f05-113">Disegnare l'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="45f05-113">Paint the original image.</span></span>
4.  <span data-ttu-id="45f05-114">Chiamare [**ID2D1RenderTarget::P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) per rimuovere l'ultimo clip allineato all'asse dalla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="45f05-114">Call [**ID2D1RenderTarget::PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the last axis-aligned clip from the render target.</span></span>

<span data-ttu-id="45f05-115">Nella figura seguente, ad esempio, la bitmap originale a sinistra è 200 \* 130 pixel.</span><span class="sxs-lookup"><span data-stu-id="45f05-115">For example, in the following illustration, the original bitmap on the left is 200\*130 pixels.</span></span> <span data-ttu-id="45f05-116">La bitmap a destra è la bitmap originale ritagliata nel rettangolo di ritaglio allineato all'asse.</span><span class="sxs-lookup"><span data-stu-id="45f05-116">The bitmap on the right is the original bitmap clipped to the axis-aligned clip rectangle.</span></span> <span data-ttu-id="45f05-117">Le dimensioni sono (20, 20) in (100, 100).</span><span class="sxs-lookup"><span data-stu-id="45f05-117">The dimensions are (20, 20) to (100, 100).</span></span>

![illustrazione di una bitmap Goldfish prima e dopo il ritaglio della bitmap](images/cliparegion-axisalignedclip.png)

<span data-ttu-id="45f05-119">Per creare l'immagine ritagliata, creare una struttura Rectangle come area di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="45f05-119">To create the clipped image, create a rectangle structure as the clipping area.</span></span> <span data-ttu-id="45f05-120">Chiamare [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) con l'area di ridimensionamento e disegnare l'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="45f05-120">Call [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) with the clipping area and paint the original image.</span></span> <span data-ttu-id="45f05-121">Chiamare [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) per rimuovere il clip dalla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="45f05-121">Call [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the clip from the render target.</span></span> <span data-ttu-id="45f05-122">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="45f05-122">The following code shows how to do this.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a><span data-ttu-id="45f05-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="45f05-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45f05-124">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="45f05-124">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 