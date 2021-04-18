---
title: Metodi CreateBitmapBrush di ID2D1RenderTarget
description: Crea un ID2D1BitmapBrush dalla bitmap specificata.
ms.assetid: 7f6ef07e-4271-4605-aced-f191a0fe65af
keywords:
- Metodo CreateBitmapBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: fcd512393a3f037cd3def40d4aa55003d9fddcef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330054"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>Metodi ID2D1RenderTarget:: CreateBitmapBrush

Crea un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapBrush (ID2D1Bitmap \* , d2d1 \_ \_ proprietà pennello bitmap \_&, \_ proprietà del pennello d2d1 \_&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | Crea un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata.<br/>                                                                                                    |
| [**CreateBitmapBrush (ID2D1Bitmap \* , \_ proprietà del \_ pennello bitmap d2d1 \_ \* , \_ proprietà del pennello d2d1 \_ \* , ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | Crea un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata.<br/>                                                                                                    |
| [**CreateBitmapBrush (ID2D1Bitmap \* , ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | Crea un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata. Il pennello utilizza i valori predefiniti per la modalità di estensione, la modalità di interpolazione, l'opacità e la trasformazione.<br/> |
| [**CreateBitmapBrush (ID2D1Bitmap \* , d2d1 \_ \_ proprietà pennello bitmap \_&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | Crea un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata. Il pennello usa i valori predefiniti per la relativa opacità e trasformazione.<br/>                                   |



## <a name="examples"></a>Esempio

Per un esempio che illustra come disegnare un'area con un pennello bitmap, vedere [How to create a bitmap Brush](how-to-create-a-bitmap-brush.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Come creare un pennello bitmap](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> </dl>

 

