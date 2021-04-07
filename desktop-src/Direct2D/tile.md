---
title: Effetto tessera
description: Usare l'effetto icona per ripetere l'area specificata dell'immagine.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- effetto tessera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048444"
---
# <a name="tile-effect"></a>Effetto tessera

Usare l'effetto icona per ripetere l'area specificata dell'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1Tile.

## <a name="example-image"></a>Immagine di esempio



| Prima                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| After                                                      |
| ![immagine dopo la trasformazione.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                | Tipo e valore predefinito                                              | Descrizione                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> D2D1 \_ riquadro \_ prop \_ Rect<br/> | D2D1 \_ vector \_ 4F<br/> {0,0 f, 0,0 f, 100.0 f, 100.0 f}<br/> | Area dell'immagine da affiancare. Questa proprietà è un \_ vettore d2d1 \_ 4F definito come: (Left, top, right, Bottom). Le unità sono in tuffi.<br/> |



 

## <a name="output-bitmap"></a>Bitmap di output

Questo effetto genera una bitmap di dimensioni infinite logicamente.

È possibile affiancare un'immagine e restituire una certa dimensione senza effetti aggiuntivi impostando le dimensioni quando si chiama [**ID2D1DeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

