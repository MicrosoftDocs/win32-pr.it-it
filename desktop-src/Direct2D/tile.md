---
title: Effetto riquadro
description: Usare l'effetto riquadro per ripetere l'area specificata dell'immagine.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- effetto riquadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0df10143a727fb8ce6585264b65b6db46d75c731070f2ea46ff8e7dffd59dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430496"
---
# <a name="tile-effect"></a>Effetto riquadro

Usare l'effetto riquadro per ripetere l'area specificata dell'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1Tile.

## <a name="example-image"></a>Immagine di esempio



| Prima                                                     |
|------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg) |
| After                                                      |
| ![l'immagine dopo la trasformazione.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                | Tipo e valore predefinito                                              | Descrizione                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> RETTA DI PROP DEL RIQUADRO D2D1 \_ \_ \_<br/> | D2D1 \_ VECTOR \_ 4F<br/> {0.0f, 0.0f, 100.0f, 100.0f}<br/> | Area dell'immagine da affiancare. Questa proprietà è un vettore D2D1 \_ \_ 4F definito come: (a sinistra, in alto, a destra, in basso). Le unità sono in DIP.<br/> |



 

## <a name="output-bitmap"></a>Bitmap di output

Questo effetto genera una bitmap logicamente infinita.

È possibile affiancare un'immagine e ottenere un output di una determinata dimensione senza effetti aggiuntivi impostando le dimensioni quando si chiama [**ID2D1DeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

