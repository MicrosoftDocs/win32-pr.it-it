---
title: Errore di scaricamento D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Una chiamata flush da una destinazione di rendering non è riuscita
keywords:
- Errore di scaricamento D1110 Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 721fb27e8cfd5e83f94b93079ee66e4a1c35992d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549926"
---
# <a name="d1110-flush-failure"></a><span data-ttu-id="0df89-104">D1110: Errore di scaricamento</span><span class="sxs-lookup"><span data-stu-id="0df89-104">D1110: Flush Failure</span></span>

<span data-ttu-id="0df89-105">Una chiamata Flush da parte di una risorsa di destinazione di rendering non \[ *è riuscita.* \]</span><span class="sxs-lookup"><span data-stu-id="0df89-105">A Flush call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="0df89-106">Tag \[ *tag1,* *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="0df89-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="0df89-107">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="0df89-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="0df89-108"><span id="resource"></span><span id="RESOURCE"></span>*Risorsa*</span><span class="sxs-lookup"><span data-stu-id="0df89-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="0df89-109">Indirizzo della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="0df89-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="0df89-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="0df89-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="0df89-111">Primo valore del tag.</span><span class="sxs-lookup"><span data-stu-id="0df89-111">The first tag value.</span></span> <span data-ttu-id="0df89-112">Per [**altre informazioni, vedere SetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)</span><span class="sxs-lookup"><span data-stu-id="0df89-112">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="0df89-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="0df89-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="0df89-114">Secondo valore del tag.</span><span class="sxs-lookup"><span data-stu-id="0df89-114">The second tag value.</span></span> <span data-ttu-id="0df89-115">Per [**altre informazioni, vedere SetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)</span><span class="sxs-lookup"><span data-stu-id="0df89-115">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="0df89-116">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="0df89-116">Error Level</span></span> | <span data-ttu-id="0df89-117">Avviso</span><span class="sxs-lookup"><span data-stu-id="0df89-117">Warning</span></span> |



 

## <a name="examples"></a><span data-ttu-id="0df89-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="0df89-118">Examples</span></span>

<span data-ttu-id="0df89-119">**Esempio 1:** Il codice seguente mostra che una chiamata di disegno è in uno stato non valido.</span><span class="sxs-lookup"><span data-stu-id="0df89-119">**Example 1:** The following code shows that a draw call is in an invalid state.</span></span> <span data-ttu-id="0df89-120">Per evitare il messaggio di avviso, usare [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) per impostare D2D1 \_ \_ ANTIALIAS MODE \_ ANTIALIASED prima di [**una chiamata a FillOpacityMask.**](id2d1rendertarget-fillopacitymask.md)</span><span class="sxs-lookup"><span data-stu-id="0df89-120">To avoid the warning message, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set D2D1\_ANTIALIAS\_MODE\_ANTIALIASED before a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) call.</span></span>


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





<span data-ttu-id="0df89-121">In questo esempio viene generato il messaggio di debug seguente:</span><span class="sxs-lookup"><span data-stu-id="0df89-121">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

<span data-ttu-id="0df89-122">**Esempio 2:** Il codice seguente mostra che [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) viene chiamato dopo la [**chiamata di EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)</span><span class="sxs-lookup"><span data-stu-id="0df89-122">**Example 2:** The following code shows that the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called after the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call.</span></span>


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



<span data-ttu-id="0df89-123">In questo esempio viene generato il messaggio di debug seguente:</span><span class="sxs-lookup"><span data-stu-id="0df89-123">This example produces the following debug message:</span></span>

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a><span data-ttu-id="0df89-124">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="0df89-124">Possible Causes</span></span>

<span data-ttu-id="0df89-125">La [**chiamata Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) può avere esito negativo per uno dei due motivi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0df89-125">The [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call can fail for one of two reasons.</span></span> <span data-ttu-id="0df89-126">L'operazione potrebbe non riuscire perché [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)il metodo è stato chiamato all'esterno della chiamata / [**BeginDraw EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oppure perché si è verificato un errore generato da una delle operazioni di destinazione di rendering elaborate dopo l'ultima chiamata **Flush** o **EndDraw.**</span><span class="sxs-lookup"><span data-stu-id="0df89-126">It may fail because the method was called outside of the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)/[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call, or it may fail because there was an error produced by one of the render target operations that have been processed since the last **Flush** call or **EndDraw** call.</span></span> <span data-ttu-id="0df89-127">Per risolvere il problema, l'applicazione deve determinare la causa dell'errore ed eseguire l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="0df89-127">To fix the issue, the application should determine the cause of the error and take the appropriate action.</span></span>

## <a name="fixes"></a><span data-ttu-id="0df89-128">Correzioni</span><span class="sxs-lookup"><span data-stu-id="0df89-128">Fixes</span></span>

<span data-ttu-id="0df89-129">Esistono molti motivi per cui una [**chiamata Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="0df89-129">There are many reasons that a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call might fail.</span></span> <span data-ttu-id="0df89-130">L'applicazione deve determinare la causa dell'errore ed eseguire l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="0df89-130">The application should determine the cause of the error and take the appropriate action.</span></span>

 

 