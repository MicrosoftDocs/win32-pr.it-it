---
title: Errore di scaricamento D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Una chiamata di scaricamento da una destinazione di rendering non è riuscita
keywords:
- Direct2D errore di scaricamento D1110
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4821ba291f3adc8d22d1d1298a88c74b47dc648b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399695"
---
# <a name="d1110-flush-failure"></a><span data-ttu-id="7944f-104">D1110: errore di svuotamento</span><span class="sxs-lookup"><span data-stu-id="7944f-104">D1110: Flush Failure</span></span>

<span data-ttu-id="7944f-105">Una chiamata di scaricamento da una destinazione di rendering non è riuscita \[  \] .</span><span class="sxs-lookup"><span data-stu-id="7944f-105">A Flush call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="7944f-106">Tag \[ *tag1*, *Tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="7944f-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="7944f-107">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="7944f-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="7944f-108"><span id="resource"></span><span id="RESOURCE"></span>*risorse*</span><span class="sxs-lookup"><span data-stu-id="7944f-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="7944f-109">Indirizzo della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="7944f-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="7944f-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="7944f-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="7944f-111">Primo valore del tag.</span><span class="sxs-lookup"><span data-stu-id="7944f-111">The first tag value.</span></span> <span data-ttu-id="7944f-112">Per ulteriori informazioni, vedere i [**tag**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="7944f-112">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="7944f-113"><span id="tag2"></span><span id="TAG2"></span>*Tag2*</span><span class="sxs-lookup"><span data-stu-id="7944f-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="7944f-114">Il secondo valore del tag.</span><span class="sxs-lookup"><span data-stu-id="7944f-114">The second tag value.</span></span> <span data-ttu-id="7944f-115">Per ulteriori informazioni, vedere i [**tag**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="7944f-115">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="7944f-116">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="7944f-116">Error Level</span></span> | <span data-ttu-id="7944f-117">Avviso</span><span class="sxs-lookup"><span data-stu-id="7944f-117">Warning</span></span> |



 

## <a name="examples"></a><span data-ttu-id="7944f-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="7944f-118">Examples</span></span>

<span data-ttu-id="7944f-119">**Esempio 1:** Il codice seguente mostra che una chiamata di progetto è in uno stato non valido.</span><span class="sxs-lookup"><span data-stu-id="7944f-119">**Example 1:** The following code shows that a draw call is in an invalid state.</span></span> <span data-ttu-id="7944f-120">Per evitare il messaggio di avviso, usare [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) per impostare \_ l' \_ antialiasing della modalità antialias d2d1 \_ prima di una chiamata a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="7944f-120">To avoid the warning message, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set D2D1\_ANTIALIAS\_MODE\_ANTIALIASED before a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) call.</span></span>


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





<span data-ttu-id="7944f-121">Questo esempio produce il seguente messaggio di debug:</span><span class="sxs-lookup"><span data-stu-id="7944f-121">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

<span data-ttu-id="7944f-122">**Esempio 2:** Il codice seguente mostra che lo [**scaricamento**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) viene chiamato dopo la chiamata a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="7944f-122">**Example 2:** The following code shows that the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called after the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call.</span></span>


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



<span data-ttu-id="7944f-123">Questo esempio produce il seguente messaggio di debug:</span><span class="sxs-lookup"><span data-stu-id="7944f-123">This example produces the following debug message:</span></span>

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a><span data-ttu-id="7944f-124">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="7944f-124">Possible Causes</span></span>

<span data-ttu-id="7944f-125">La chiamata di [**scaricamento**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) può non riuscire per uno dei due motivi.</span><span class="sxs-lookup"><span data-stu-id="7944f-125">The [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call can fail for one of two reasons.</span></span> <span data-ttu-id="7944f-126">Potrebbe non riuscire perché il metodo è stato chiamato al [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)di fuori della / [**chiamata EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) BeginDraw o potrebbe non riuscire a causa di un errore prodotto da una delle operazioni di destinazione di rendering elaborate dall'ultima chiamata di **scaricamento** o dalla chiamata a **EndDraw** .</span><span class="sxs-lookup"><span data-stu-id="7944f-126">It may fail because the method was called outside of the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)/[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call, or it may fail because there was an error produced by one of the render target operations that have been processed since the last **Flush** call or **EndDraw** call.</span></span> <span data-ttu-id="7944f-127">Per risolvere il problema, l'applicazione deve determinare la causa dell'errore e intraprendere l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="7944f-127">To fix the issue, the application should determine the cause of the error and take the appropriate action.</span></span>

## <a name="fixes"></a><span data-ttu-id="7944f-128">Correzioni</span><span class="sxs-lookup"><span data-stu-id="7944f-128">Fixes</span></span>

<span data-ttu-id="7944f-129">Esistono molti motivi per cui una chiamata di [**scaricamento**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="7944f-129">There are many reasons that a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call might fail.</span></span> <span data-ttu-id="7944f-130">L'applicazione deve determinare la causa dell'errore e intraprendere l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="7944f-130">The application should determine the cause of the error and take the appropriate action.</span></span>

 

 