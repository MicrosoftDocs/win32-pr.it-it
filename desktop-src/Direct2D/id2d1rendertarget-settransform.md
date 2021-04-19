---
title: Metodi di trasformazione ID2D1RenderTarget
description: Applica la trasformazione specificata alla destinazione di rendering, sostituendo la trasformazione esistente. Tutte le operazioni di disegno successive si verificano nello spazio trasformato.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Metodi di trasformazione Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333504"
---
# <a name="id2d1rendertargetsettransform-methods"></a>Metodi ID2D1RenderTarget:: setransform

Applica la trasformazione specificata alla destinazione di rendering, sostituendo la trasformazione esistente. Tutte le operazioni di disegno successive si verificano nello spazio trasformato.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                              | Descrizione                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Setransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))  | Applica la trasformazione specificata alla destinazione di rendering, sostituendo la trasformazione esistente. Tutte le operazioni di disegno successive si verificano nello spazio trasformato. <br/> |
| [**Setransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f)) | Applica la trasformazione specificata alla destinazione di rendering, sostituendo la trasformazione esistente. Tutte le operazioni di disegno successive si verificano nello spazio trasformato.<br/>  |



## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzato il metodo **setransform** per applicare una rotazione alla destinazione di rendering. Per l'esempio completo, vedere [come ruotare un oggetto](how-to-rotate.md).


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



Per altri esempi che illustrano come trasformare una destinazione di rendering, vedere [come ridimensionare un oggetto](how-to-scale.md), [come inclinare un oggetto](how-to-skew.md)e [come tradurre un oggetto](how-to-translate.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Cenni preliminari sulle trasformazioni](direct2d-transforms-overview.md)
</dt> <dt>

[Come ruotare un oggetto](how-to-rotate.md)
</dt> <dt>

[Come ridimensionare un oggetto](how-to-scale.md)
</dt> <dt>

[Come inclinare un oggetto](how-to-skew.md)
</dt> <dt>

[Come tradurre un oggetto](how-to-translate.md)
</dt> <dt>

[Come applicare più trasformazioni a un oggetto](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

