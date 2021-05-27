---
title: D1111 uso del livello quando la clip è sufficiente
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Un livello viene usato con una maschera di opacità NULL, un'opacità 1,0 e una maschera geometrica rettangolare allineata all'asse. L'API Push/Pop Clip dovrebbe ottenere gli stessi risultati con prestazioni più elevate.
keywords:
- D1111 Using Layer When Clip Is Sufficient Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8463cc3940b69e326f13df6be9602dd6073fec0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549906"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a><span data-ttu-id="8764b-105">D1111: Uso del livello quando la clip è sufficiente</span><span class="sxs-lookup"><span data-stu-id="8764b-105">D1111: Using Layer When Clip Is Sufficient</span></span>

<span data-ttu-id="8764b-106">PERF: un livello viene usato con una maschera di opacità **NULL,** un'opacità 1,0 e una maschera geometrica rettangolare allineata all'asse.</span><span class="sxs-lookup"><span data-stu-id="8764b-106">PERF - A layer is being used with a **NULL** opacity mask, 1.0 opacity, and an axis aligned rectangular geometric mask.</span></span> <span data-ttu-id="8764b-107">L'API Push/Pop Clip dovrebbe ottenere gli stessi risultati con prestazioni più elevate.</span><span class="sxs-lookup"><span data-stu-id="8764b-107">The Push/Pop Clip API should achieve the same results with higher performance.</span></span>

## <a name="placeholders"></a><span data-ttu-id="8764b-108">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="8764b-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="8764b-109"><span id="interface"></span><span id="INTERFACE"></span>*Interfaccia*</span><span class="sxs-lookup"><span data-stu-id="8764b-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="8764b-110">Indirizzo dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="8764b-110">The address of the interface.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="8764b-111">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="8764b-111">Error Level</span></span> | <span data-ttu-id="8764b-112">Informazioni</span><span class="sxs-lookup"><span data-stu-id="8764b-112">Information</span></span> |



 

## <a name="examples"></a><span data-ttu-id="8764b-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="8764b-113">Examples</span></span>

<span data-ttu-id="8764b-114">Il codice seguente usa [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) quando il livello contiene una sola primitiva (un rettangolo) e i campi della struttura [**D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sono impostati sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="8764b-114">The following code uses the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) when the layer contains only one primitive (a rectangle) and the fields of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to defaults.</span></span> <span data-ttu-id="8764b-115">Per i valori predefiniti della struttura **D2D1 \_ LAYER \_ PARAMETERS,** vedere [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span><span class="sxs-lookup"><span data-stu-id="8764b-115">For the default values of the **D2D1\_LAYER\_PARAMETERS** structure, see [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span></span>


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



<span data-ttu-id="8764b-116">In questo esempio viene generato il messaggio di debug seguente:</span><span class="sxs-lookup"><span data-stu-id="8764b-116">This example produces the following debug message:</span></span>

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a><span data-ttu-id="8764b-117">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="8764b-117">Possible Causes</span></span>

<span data-ttu-id="8764b-118">È stato usato un livello quando i metodi [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) sarebbero stati sufficiente.</span><span class="sxs-lookup"><span data-stu-id="8764b-118">A layer was used when the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) methods would have sufficed.</span></span>

 

 