---
title: Metodi di ID2D1RenderTarget CreateBitmapBrush
description: Crea un oggetto ID2D1BitmapBrush dalla bitmap specificata.
ms.assetid: 7f6ef07e-4271-4605-aced-f191a0fe65af
keywords:
- Metodi CreateBitmapBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 411ae2dd81fce88bec5d6a3717fe79d942de84f060c53a90b83cae461d6a49de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053091"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>Metodi id2D1RenderTarget::CreateBitmapBrush

Crea un [**oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapBrush(ID2D1Bitmap,D2D1 \* \_ BITMAP BRUSH PROPERTIES \_ \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | Crea un [**oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata.<br/>                                                                                                    |
| [**CreateBitmapBrush(ID2D1Bitmap,PROPRIETÀ PENNELLO \* \_ BITMAP \_ \_ \* D2D1, PROPRIETÀ PENNELLO D2D1, \_ \_ \* ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | Crea un [**oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata.<br/>                                                                                                    |
| [**CreateBitmapBrush(ID2D1Bitmap \* ,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | Crea un [**oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata. Il pennello usa i valori predefiniti per la modalità di estensione, la modalità di interpolazione, l'opacità e la trasformazione.<br/> |
| [**CreateBitmapBrush(ID2D1Bitmap,D2D1 \* \_ BITMAP BRUSH PROPERTIES \_ \_&,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | Crea un [**oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) dalla bitmap specificata. Il pennello usa i valori predefiniti per l'opacità e la trasformazione.<br/>                                   |



## <a name="examples"></a>Esempio

Per un esempio che illustra come disegnare un'area con un pennello bitmap, vedere [Come creare un pennello bitmap](how-to-create-a-bitmap-brush.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Come creare un pennello bitmap](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> </dl>

 

