---
title: D1111 utilizzando il livello quando il clip è sufficiente
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Un livello viene utilizzato con una maschera di opacità NULL, un'opacità 1,0 e una maschera geometrica rettangolare allineata asse. L'API di ritaglio push/pop dovrebbe ottenere gli stessi risultati con prestazioni più elevate.
keywords:
- D1111 utilizzando il livello quando il clip è un Direct2D sufficiente
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: a30bbfd7b8ca448928249018a28bc4d6a8a2f57f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730071"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a><span data-ttu-id="ec320-105">D1111: utilizzo del livello quando il clip è sufficiente</span><span class="sxs-lookup"><span data-stu-id="ec320-105">D1111: Using Layer When Clip Is Sufficient</span></span>

<span data-ttu-id="ec320-106">PERF: viene usato un livello con una maschera di opacità **null** , un'opacità 1,0 e una maschera geometrica rettangolare allineata asse.</span><span class="sxs-lookup"><span data-stu-id="ec320-106">PERF - A layer is being used with a **NULL** opacity mask, 1.0 opacity, and an axis aligned rectangular geometric mask.</span></span> <span data-ttu-id="ec320-107">L'API di ritaglio push/pop dovrebbe ottenere gli stessi risultati con prestazioni più elevate.</span><span class="sxs-lookup"><span data-stu-id="ec320-107">The Push/Pop Clip API should achieve the same results with higher performance.</span></span>

## <a name="placeholders"></a><span data-ttu-id="ec320-108">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="ec320-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="ec320-109"><span id="interface"></span><span id="INTERFACE"></span>*interfaccia*</span><span class="sxs-lookup"><span data-stu-id="ec320-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="ec320-110">Indirizzo dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ec320-110">The address of the interface.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="ec320-111">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="ec320-111">Error Level</span></span> | <span data-ttu-id="ec320-112">Informazioni</span><span class="sxs-lookup"><span data-stu-id="ec320-112">Information</span></span> |



 

## <a name="examples"></a><span data-ttu-id="ec320-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="ec320-113">Examples</span></span>

<span data-ttu-id="ec320-114">Il codice seguente usa [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) quando il livello contiene solo una primitiva (un rettangolo) e i campi della struttura [**dei \_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sono impostati sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="ec320-114">The following code uses the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) when the layer contains only one primitive (a rectangle) and the fields of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to defaults.</span></span> <span data-ttu-id="ec320-115">Per i valori predefiniti della struttura **dei \_ \_ parametri del livello d2d1** , vedere [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span><span class="sxs-lookup"><span data-stu-id="ec320-115">For the default values of the **D2D1\_LAYER\_PARAMETERS** structure, see [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span></span>


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



<span data-ttu-id="ec320-116">Questo esempio produce il seguente messaggio di debug:</span><span class="sxs-lookup"><span data-stu-id="ec320-116">This example produces the following debug message:</span></span>

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a><span data-ttu-id="ec320-117">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="ec320-117">Possible Causes</span></span>

<span data-ttu-id="ec320-118">È stato usato un livello quando i metodi [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) sarebbero sufficienti.</span><span class="sxs-lookup"><span data-stu-id="ec320-118">A layer was used when the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) methods would have sufficed.</span></span>

 

 