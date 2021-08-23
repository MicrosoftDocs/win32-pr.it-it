---
title: Metodi ID2D1RenderTarget CreateCompatibleRenderTarget (D2d1.h)
description: Crea una nuova destinazione di rendering bitmap da usare durante il disegno intermedio fuori schermo compatibile con la destinazione di rendering corrente.
ms.assetid: 4a799a7c-0d2f-460f-99f9-24c6cf7c4537
keywords:
- Metodi CreateCompatibleRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9015586109ff5015743874d18b604de919a9464a655383cf4d47aabb7b7acf35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432781"
---
# <a name="id2d1rendertargetcreatecompatiblerendertarget-methods"></a>Metodi ID2D1RenderTarget::CreateCompatibleRenderTarget

Crea una nuova destinazione di rendering bitmap da usare durante il disegno intermedio fuori schermo compatibile con la destinazione di rendering corrente.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,D2D1 \_ SIZE \_ U,D2D1 \_ PIXEL \_ FORMAT,D2D1 \_ COMPATIBLE RENDER TARGET \_ \_ \_ OPTIONS,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget))       | Crea una destinazione di rendering bitmap da usare durante il disegno intermedio fuori schermo compatibile con la destinazione di rendering corrente.<br/>                                                                                                             |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F \* ,D2D1 \_ SIZE U \_ \* ,D2D1 \_ PIXEL FORMAT \_ \* ,D2D1 \_ COMPATIBLE RENDER TARGET \_ \_ \_ OPTIONS,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)) | Crea una destinazione di rendering bitmap da usare durante il disegno intermedio fuori schermo compatibile con la destinazione di rendering corrente. <br/>                                                                                                            |
| [**CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget) \* \***](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))                                                                                                 | Crea una nuova destinazione di rendering bitmap da usare durante il disegno intermedio fuori schermo compatibile con la destinazione di rendering corrente e con le stesse dimensioni, DPI e formato pixel (ma non la modalità alfa) della destinazione di rendering corrente. <br/>         |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_id2d1bitmaprendertarget))                                                                                   | Crea una nuova destinazione di rendering bitmap da usare durante il disegno intermedio fuori schermo compatibile con la destinazione di rendering corrente e con lo stesso formato pixel (ma non la modalità alfa) della destinazione di rendering corrente. <br/>                        |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,D2D1 \_ SIZE \_ U,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_id2d1bitmaprendertarget))                                                                     | Crea una destinazione di rendering bitmap da usare durante il disegno intermedio fuori schermo compatibile con la destinazione di rendering corrente. La nuova destinazione di rendering bitmap ha lo stesso formato pixel (ma non la modalità alfa) della destinazione di rendering corrente. <br/> |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,D2D1 \_ SIZE \_ U,D2D1 \_ PIXEL \_ FORMAT,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_id2d1bitmaprendertarget))                                                 | Crea una destinazione di rendering bitmap da usare durante il disegno intermedio fuori schermo compatibile con la destinazione di rendering corrente. <br/>                                                                                                            |



## <a name="examples"></a>Esempio

L'esempio seguente usa il **metodo CreateCompatibleRenderTarget** per creare un oggetto [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) e lo usa per disegnare un modello di griglia. Il motivo griglia viene usato come origine di un [**oggetto ID2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)


```C++
HRESULT DemoApp::CreateGridPatternBrush(
    ID2D1RenderTarget *pRenderTarget,
    ID2D1BitmapBrush **ppBitmapBrush
    )
{
    // Create a compatible render target.
    ID2D1BitmapRenderTarget *pCompatibleRenderTarget = NULL;
    HRESULT hr = pRenderTarget->CreateCompatibleRenderTarget(
        D2D1::SizeF(10.0f, 10.0f),
        &amp;pCompatibleRenderTarget
        );
    if (SUCCEEDED(hr))
    {
        // Draw a pattern.
        ID2D1SolidColorBrush *pGridBrush = NULL;
        hr = pCompatibleRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
            &amp;pGridBrush
            );
        if (SUCCEEDED(hr))
        {
            pCompatibleRenderTarget->BeginDraw();
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.0f, 10.0f, 1.0f), pGridBrush);
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.1f, 1.0f, 10.0f), pGridBrush);
            pCompatibleRenderTarget->EndDraw();

            // Retrieve the bitmap from the render target.
            ID2D1Bitmap *pGridBitmap = NULL;
            hr = pCompatibleRenderTarget->GetBitmap(&amp;pGridBitmap);
            if (SUCCEEDED(hr))
            {
                // Choose the tiling mode for the bitmap brush.
                D2D1_BITMAP_BRUSH_PROPERTIES brushProperties =
                    D2D1::BitmapBrushProperties(D2D1_EXTEND_MODE_WRAP, D2D1_EXTEND_MODE_WRAP);

                // Create the bitmap brush.
                hr = m_pRenderTarget->CreateBitmapBrush(pGridBitmap, brushProperties, ppBitmapBrush);

                pGridBitmap->Release();
            }

            pGridBrush->Release();
        }

        pCompatibleRenderTarget->Release();
    }

    return hr;
}
```



Nell'esempio di codice seguente viene utilizzato il pennello per disegnare un motivo.


```C++
// Paint a grid background.
m_pRenderTarget->FillRectangle(
    D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
    m_pGridPatternBitmapBrush
    );
```



Il codice è stato omesso da questo esempio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
