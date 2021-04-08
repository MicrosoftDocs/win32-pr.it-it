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
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111: utilizzo del livello quando il clip è sufficiente

PERF: viene usato un livello con una maschera di opacità **null** , un'opacità 1,0 e una maschera geometrica rettangolare allineata asse. L'API di ritaglio push/pop dovrebbe ottenere gli stessi risultati con prestazioni più elevate.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interfaccia*
</dt> <dd>

Indirizzo dell'interfaccia.

</dd> </dl> 

|             |             |
|-------------|-------------|
| Livello di errore | Informazioni |



 

## <a name="examples"></a>Esempio

Il codice seguente usa [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) quando il livello contiene solo una primitiva (un rettangolo) e i campi della struttura [**dei \_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sono impostati sui valori predefiniti. Per i valori predefiniti della struttura **dei \_ \_ parametri del livello d2d1** , vedere [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



Questo esempio produce il seguente messaggio di debug:

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a>Possibili cause

È stato usato un livello quando i metodi [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) sarebbero sufficienti.

 

 