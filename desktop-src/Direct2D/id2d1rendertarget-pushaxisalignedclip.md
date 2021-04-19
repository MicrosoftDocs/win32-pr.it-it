---
title: Metodi ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1. h)
description: Specifica un rettangolo in cui tutte le operazioni di disegno successive vengono ritagliate.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Metodo PushAxisAlignedClip Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333507"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>ID2D1RenderTarget::P metodi ushAxisAlignedClip

Specifica un rettangolo in cui tutte le operazioni di disegno successive vengono ritagliate.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                         | Descrizione                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**PushAxisAlignedClip (D2D1 \_ Rect \_ F&, \_ modalità antialias d2d1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | Specifica un rettangolo in cui tutte le operazioni di disegno successive vengono ritagliate. <br/> |
| [**PushAxisAlignedClip (D2D1 \_ Rect \_ F \* , d2d1 \_ antialias \_ mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | Specifica un rettangolo in cui tutte le operazioni di disegno successive vengono ritagliate. <br/> |



## <a name="remarks"></a>Commenti

Una coppia [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) può essere presente in un [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ma non può sovrapporsi. La sequenza di **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** , ad esempio, è valida, ma la sequenza di **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** non è valida.

Questo metodo non restituisce un codice di errore se ha esito negativo. Per determinare se un'operazione di disegno (ad esempio **PushAxisAlignedClip**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Esempio

Per un esempio, vedere la pagina relativa alla [clip con un rettangolo di ritaglio Axis-Aligned](how-to-clip-with-axis-aligned-rects.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1 \_ 1. h (include D2d1. h)</dt> </dl> |
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
