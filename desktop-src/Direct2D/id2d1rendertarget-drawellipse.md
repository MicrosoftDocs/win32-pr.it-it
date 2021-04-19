---
title: Metodi DrawEllipse di ID2D1RenderTarget (D2d1. h)
description: Disegna il contorno di un'ellisse con le dimensioni e il tratto specificati.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- Metodo DrawEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326072"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a>ID2D1RenderTarget::D Metodi rawEllipse

Disegna il contorno di un'ellisse con le dimensioni e il tratto specificati.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                 | Descrizione                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**DrawEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))  | Disegna il contorno dell'ellisse specificata utilizzando lo stile del tratto specificato. <br/> |
| [**DrawEllipse (D2D1 \_ ellisse \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) | Disegna il contorno dell'ellisse specificata utilizzando lo stile del tratto specificato. <br/> |



## <a name="remarks"></a>Commenti

Se ha esito negativo, il metodo **DrawEllipse** non restituisce un codice di errore. Per determinare se un'operazione di disegno (ad esempio **DrawEllipse**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Esempio

Per un esempio, vedere [How to disegnare and Fill a Basic Shape](how-to-draw-an-ellipse.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))
</dt> </dl>

�

�
