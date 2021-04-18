---
title: Metodi DrawText ID2D1RenderTarget
description: Disegna il testo specificato utilizzando le informazioni sul formato fornite da un oggetto IDWriteTextFormat.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Metodi DrawText Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326069"
---
# <a name="id2d1rendertargetdrawtext-methods"></a>ID2D1RenderTarget::D Metodi rawText

Disegna il testo specificato utilizzando le informazioni sul formato fornite da un oggetto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                                                                               | Descrizione                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ Rect \_ F&, ID2D1Brush \* , d2d1 \_ , \_ \_ Opzioni di testo di, \_ metodo di misurazione del testo DWrite \_ \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))  | Disegna il testo specificato utilizzando le informazioni sul formato fornite da un oggetto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .<br/>  |
| [**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ Rect \_ F \* , ID2D1Brush \* , d2d1 \_ , \_ \_ Opzioni di testo di testo, DWrite \_ testo di \_ misurazione \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) | Disegna il testo specificato utilizzando le informazioni sul formato fornite da un oggetto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) . <br/> |



## <a name="remarks"></a>Commenti

Per creare testo con Direct2D, usare il metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) per il testo con un formato singolo oppure il metodo [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) quando sono necessari più formati, funzionalità OpenType avanzate o hit testing. Questi metodi usano l'API DirectWrite per fornire una visualizzazione di testo di alta qualità.

Questo metodo non restituisce un codice di errore se ha esito negativo. Per determinare se un'operazione di disegno (ad esempio **DrawText**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Esempio

Per un esempio, vedere [come creare testo](how-to--draw-text.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[Come creare testo](how-to--draw-text.md)
</dt> <dt>

[Cenni preliminari sulla formattazione e sul layout del testo](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

