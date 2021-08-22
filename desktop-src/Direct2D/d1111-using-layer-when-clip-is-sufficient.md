---
title: D1111 Uso del livello quando il clip è sufficiente
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
ms.openlocfilehash: b03a6c2a4806724cd7cfdc97354e29e86dc60e0f1729ee9efeca89d971ca0a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758101"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111: Uso del livello quando la clip è sufficiente

PERF: un livello viene usato con una maschera di opacità **NULL,** un'opacità 1,0 e una maschera geometrica rettangolare allineata all'asse. L'API Push/Pop Clip dovrebbe ottenere gli stessi risultati con prestazioni più elevate.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaccia*
</dt> <dd>

Indirizzo dell'interfaccia.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Livello di errore | Informazioni |



 

## <a name="examples"></a>Esempio

Il codice seguente usa [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) quando il livello contiene una sola primitiva (un rettangolo) e i campi della struttura [**D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sono impostati sui valori predefiniti. Per i valori predefiniti della struttura **D2D1 \_ LAYER \_ PARAMETERS,** vedere [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



In questo esempio viene generato il messaggio di debug seguente:

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a>Possibili cause

È stato usato un livello quando i metodi [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) sarebbero stati sufficiente.

 

 