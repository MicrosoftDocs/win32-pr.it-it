---
title: Metodi DrawBitmap di ID2D1RenderTarget
description: Disegna l'oggetto ID2D1Bitmap specificato.
ms.assetid: 241df698-ca5e-4d94-902a-a9e140820c14
keywords:
- Metodo DrawBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: d82bbf557d7e53f06f614afbba578de40c789953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326073"
---
# <a name="id2d1rendertargetdrawbitmap-methods"></a>ID2D1RenderTarget::D Metodi rawBitmap

Disegna l'oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)specificato.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                       | Descrizione                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ f&, float, d2d1 \_ bitmap \_ Interpolation \_ mode, d2d1 \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))   | Disegna la bitmap specificata dopo averla ridimensionata fino alla dimensione del rettangolo specificato. <br/> |
| [**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ f&, float, d2d1 \_ bitmap \_ Interpolation \_ mode, d2d1 \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))  | Disegna la bitmap specificata dopo averla ridimensionata fino alla dimensione del rettangolo specificato. <br/> |
| [**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ Rect \_ f \* , float, d2d1 \_ bitmap \_ Interpolation \_ mode, d2d1 \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) | Disegna la bitmap specificata dopo averla ridimensionata fino alla dimensione del rettangolo specificato. <br/> |



## <a name="remarks"></a>Commenti

Questo metodo non restituisce un codice di errore se ha esito negativo. Per determinare se un'operazione di disegno (ad esempio **DrawBitmap**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Esempio

Per un esempio, vedere [come creare una bitmap](how-to-draw-a-bitmap.md). Per un esempio che illustra come caricare una bitmap da una risorsa o da un file, vedere [come caricare una bitmap](how-to-load-a-bitmap-from-a-resource.md) da una risorsa e [come caricare una bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Come creare una bitmap](how-to-draw-a-bitmap.md)
</dt> <dt>

[Come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md)
</dt> <dt>

[Come caricare una bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

