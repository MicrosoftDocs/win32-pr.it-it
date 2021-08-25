---
title: Metodi di ID2D1RenderTarget FillOpacityMask
description: Applica la maschera di opacità descritta dalla bitmap specificata a un pennello e usa tale pennello per disegnare un'area della destinazione di rendering.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Metodi FillOpacityMask Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 362043696e4cbd21dd64783f210cf2e24066645e7dac5e303a16cd83abb31307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874081"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a>Metodi ID2D1RenderTarget::FillOpacityMask

Applica la maschera di opacità descritta dalla bitmap specificata a un pennello e usa tale pennello per disegnare un'area della destinazione di rendering.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                          | Descrizione                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\*FillOpacityMask(ID2D1Bitmap,ID2D1Brush,D2D1 \* \_ OPACITY \_ MASK \_ CONTENT,D2D \_ RECT F \_&,D2D \_ RECT F \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))       | Applica la maschera di opacità descritta dalla bitmap specificata a un pennello e usa tale pennello per disegnare un'area della destinazione di rendering. <br/> |
| [**\*FillOpacityMask(ID2D1Bitmap,ID2D1Brush,D2D1 \* \_ OPACITY \_ MASK \_ CONTENT,D2D \_ RECT \_ \* F,D2D \_ RECT F \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f)) | Applica la maschera di opacità descritta dalla bitmap specificata a un pennello e usa tale pennello per disegnare un'area della destinazione di rendering. <br/> |



## <a name="remarks"></a>Commenti

Per il corretto funzionamento di questo metodo, la destinazione di rendering deve usare la modalità [**antialias D2D1 \_ ANTIALIAS \_ MODE \_ ALIASED.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) È possibile impostare la modalità di antialiasing chiamando il [**metodo ID2D1RenderTarget::SetAntialiasMode.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode)

Questo metodo non restituisce un codice di errore se ha esito negativo. Per determinare se un'operazione di disegno (ad esempio **FillOpacityMask)** ha avuto esito negativo, controllare il risultato restituito dai metodi [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget::Flush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

