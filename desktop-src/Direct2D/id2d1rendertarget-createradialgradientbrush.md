---
title: Metodi CreateRadialGradientBrush di ID2D1RenderTarget (D2d1. h)
description: Crea un oggetto ID2D1RadialGradientBrush che può essere usato per disegnare aree con una sfumatura radiale.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Metodo CreateRadialGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 680cc981943e45eb32834e48151f391f6249cc1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326080"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a>Metodi ID2D1RenderTarget:: CreateRadialGradientBrush

Crea un oggetto [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che può essere usato per disegnare aree con una sfumatura radiale.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                       | Descrizione                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRadialGradientBrush ( \_ proprietà del \_ pennello sfumatura radiale d2d1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))                            | Crea un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che contiene i cursori sfumatura specificati, non ha alcuna trasformazione e ha un'opacità di base 1,0. <br/> |
| [**CreateRadialGradientBrush ( \_ proprietà del \_ pennello sfumatura radiale d2d1 \_ \_&, \_ proprietà del pennello d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))   | Crea un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che contiene i cursori sfumatura specificati e presenta la trasformazione e l'opacità di base specificate. <br/> |
| [**CreateRadialGradientBrush ( \_ proprietà del \_ pennello sfumatura radiale d2d1 \_ \_ \* , \_ proprietà del pennello d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) | Crea un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che contiene i cursori sfumatura specificati e presenta la trasformazione e l'opacità di base specificate. <br/> |



## <a name="examples"></a>Esempio

Per un esempio, vedere [come creare un pennello sfumatura radiale](how-to-create-a-radial-gradient-brush.md).

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

[Come creare un pennello sfumatura radiale](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> </dl>

�

�
