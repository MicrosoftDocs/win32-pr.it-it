---
title: Metodi ID2D1RenderTarget CreateRadialGradientBrush (D2d1.h)
description: Crea un oggetto ID2D1RadialGradientBrush che può essere usato per disegnare aree con una sfumatura radiale.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Metodi CreateRadialGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b32c384e55f8c6ac17551c290c36e1130c05d5939fd5cf56116410ddac37320f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108821"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a>Metodi ID2D1RenderTarget::CreateRadialGradientBrush

Crea un [**oggetto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che può essere usato per disegnare aree con una sfumatura radiale.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                       | Descrizione                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_&,ID2D1GradientStopCollection \* ,ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))                            | Crea un [**oggetto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che contiene i cursori sfumatura specificati, non ha alcuna trasformazione e ha un'opacità di base di 1,0. <br/> |
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1GradientStopCollection \* ,ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))   | Crea un [**oggetto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che contiene i cursori sfumatura specificati e ha la trasformazione e l'opacità di base specificate. <br/> |
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH \_ \_ \_ \* PROPERTIES,D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1GradientStopCollection,ID2D1RadialGradientBrush \* \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) | Crea un [**oggetto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che contiene i cursori sfumatura specificati e ha la trasformazione e l'opacità di base specificate. <br/> |



## <a name="examples"></a>Esempio

Per un esempio, vedere [How to Create a Radial Gradient Brush](how-to-create-a-radial-gradient-brush.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
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
