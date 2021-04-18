---
title: Metodi CreateSolidColorBrush di ID2D1RenderTarget (D2d1. h)
description: Crea un nuovo ID2D1SolidColorBrush che può essere usato per disegnare aree con un colore a tinta unita.
ms.assetid: 3dbfe26f-cf36-47b0-925e-4934e0d7c390
keywords:
- Metodo CreateSolidColorBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: db0cf0913bc347cb36ac44cbd1befd7edb418a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326076"
---
# <a name="id2d1rendertargetcreatesolidcolorbrush-methods"></a>Metodi ID2D1RenderTarget:: CreateSolidColorBrush

Crea un nuovo [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush)) che può essere usato per disegnare aree con un colore a tinta unita.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                           | Descrizione                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSolidColorBrush (D2D1 \_ Color \_ F&, ID2D1SolidColorBrush \* \* )**](id2d1rendertarget-createsolidcolorbrush-ref-color-f-ptr-ptr-https://msdn.microsoft.com/library/Dd371867(v=VS.85).aspx)                                                      | Crea un nuovo [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush)) con il colore specificato e un'opacità di base di 1.0 f. <br/> |
| [**CreateSolidColorBrush (D2D1 \_ Color \_ F&, \_ proprietà del pennello d2d1 \_&, ID2D1SolidColorBrush \* \* )**](id2d1rendertarget-createsolidcolorbrush-ref-color-f-ref-d2d1-brush-properties-ptr-ptr-https://msdn.microsoft.com/library/Dd371867(v=VS.85).aspx)   | Crea un nuovo [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush)) con il colore e l'opacità specificati. <br/>                |
| [**CreateSolidColorBrush (D2D1 \_ Color \_ F \* , \_ proprietà del pennello d2d1 \_ \* , ID2D1SolidColorBrush \* \* )**](id2d1rendertarget-createsolidcolorbrush-ptr-color-f-ptr-d2d1-brush-properties-ptr-ptr-https://msdn.microsoft.com/library/Dd371867(v=VS.85).aspx) | Crea un nuovo [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush)) con il colore e l'opacità specificati. <br/>                |



## <a name="examples"></a>Esempio

Per un esempio, vedere [come creare un pennello tinta unita](how-to-create-a-solid-color-brush.md).

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

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> <dt>

[Avvio rapido di Direct2D](getting-started-with-direct2d.md)
</dt> </dl>

�

�
