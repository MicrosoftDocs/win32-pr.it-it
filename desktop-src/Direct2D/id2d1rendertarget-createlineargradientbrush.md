---
title: Metodi ID2D1RenderTarget CreateLinearGradientBrush (D2d1.h)
description: Crea un oggetto ID2D1LinearGradientBrush per disegnare aree con una sfumatura lineare.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Metodi CreateLinearGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 74e3ba102b24b330f176189a66eae7ac9cd74ece194900f3d8997675bf486641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966871"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a>Metodi ID2D1RenderTarget::CreateLinearGradientBrush

Crea un [**oggetto ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) per disegnare aree con una sfumatura lineare.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                       | Descrizione                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLinearGradientBrush(D2D1 \_ LINEAR GRADIENT BRUSH PROPERTIES \_ \_ \_&,ID2D1GradientStopCollection \* ,ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))                            | Crea un [**oggetto ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) che contiene i cursori sfumatura specificati, non ha alcuna trasformazione e ha un'opacità di base di 1,0. <br/> |
| [**CreateLinearGradientBrush(D2D1 \_ LINEAR GRADIENT BRUSH PROPERTIES \_ \_ \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1GradientStopCollection \* ,ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))   | Crea un [**oggetto ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) che contiene i cursori sfumatura specificati e ha la trasformazione e l'opacità di base specificate. <br/> |
| [**CreateLinearGradientBrush(D2D1 \_ LINEAR GRADIENT BRUSH PROPERTIES \_ \_ \_ \* ,D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1GradientStopCollection,ID2D1LinearGradientBrush \* \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) | Crea un [**oggetto ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) che contiene i cursori sfumatura specificati e ha la trasformazione e l'opacità di base specificate. <br/> |



## <a name="examples"></a>Esempio

Per un esempio che illustra come creare una raccolta di cursori sfumatura e usarla per definire una sfumatura lineare, vedere [How to Create a Linear Gradient Brush](how-to-create-a-linear-gradient-brush.md).

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

[**CreateGradientStopCollection**](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[Come creare un pennello sfumatura lineare](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> </dl>

�

�
