---
title: Metodi CreateLinearGradientBrush di ID2D1RenderTarget (D2d1. h)
description: Crea un oggetto ID2D1LinearGradientBrush per le aree di disegno con una sfumatura lineare.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Metodo CreateLinearGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326081"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a>Metodi ID2D1RenderTarget:: CreateLinearGradientBrush

Crea un oggetto [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) per le aree di disegno con una sfumatura lineare.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                       | Descrizione                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLinearGradientBrush ( \_ proprietà del \_ pennello sfumatura lineare d2d1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))                            | Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) che contiene i cursori sfumatura specificati, non ha alcuna trasformazione e ha un'opacità di base 1,0. <br/> |
| [**CreateLinearGradientBrush ( \_ proprietà del \_ pennello sfumatura lineare d2d1 \_ \_&, \_ proprietà del pennello d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))   | Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) che contiene i cursori sfumatura specificati e presenta la trasformazione e l'opacità di base specificate. <br/> |
| [**CreateLinearGradientBrush ( \_ proprietà del \_ pennello sfumatura lineare d2d1 \_ \_ \* , \_ proprietà del pennello d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) | Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) che contiene i cursori sfumatura specificati e presenta la trasformazione e l'opacità di base specificate. <br/> |



## <a name="examples"></a>Esempio

Per un esempio che illustra come creare una raccolta di arresti sfumatura e usarla per definire una sfumatura lineare, vedere [How to create a linear gradient brush](how-to-create-a-linear-gradient-brush.md).

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

[**CreateGradientStopCollection**](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[Come creare un pennello sfumato lineare](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> </dl>

�

�
