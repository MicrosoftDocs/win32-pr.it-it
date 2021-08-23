---
title: Metodi ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1.h)
description: Specifica un rettangolo in base al quale vengono ritagliate tutte le operazioni di disegno successive.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Metodi PushAxisAlignedClip Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3ce76db0608ccd79ecd8ea1be716f8cbdf4313f95bfdda9cfac7b63474e3f412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873991"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>Metodi ID2D1RenderTarget::P ushAxisAlignedClip

Specifica un rettangolo in base al quale vengono ritagliate tutte le operazioni di disegno successive.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                         | Descrizione                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**PushAxisAlignedClip(D2D1 \_ RECT \_ F&,D2D1 \_ ANTIALIAS \_ MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | Specifica un rettangolo in base al quale vengono ritagliate tutte le operazioni di disegno successive. <br/> |
| [**PushAxisAlignedClip(D2D1 \_ RECT \_ F \* ,D2D1 \_ ANTIALIAS \_ MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | Specifica un rettangolo in base al quale vengono ritagliate tutte le operazioni di disegno successive. <br/> |



## <a name="remarks"></a>Commenti

Una [**coppia PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) può verificarsi intorno o all'interno di [**pushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)ma non può sovrapporsi. Ad esempio, la sequenza di **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** è valida, ma la sequenza di **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** non è valida.

Questo metodo non restituisce un codice di errore se ha esito negativo. Per determinare se un'operazione di disegno (ad esempio **PushAxisAlignedClip)** non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget::Flush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)

## <a name="examples"></a>Esempio

Per un esempio, vedere [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1 \_ 1.h (includere D2d1.h)</dt> </dl> |
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
