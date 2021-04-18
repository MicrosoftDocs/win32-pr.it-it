---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Descrive i componenti rosso, verde, blu e alfa di un colore. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321471"
---
# <a name="d2d1_color_f"></a>D2D1 \_ colore \_ F

Descrive i componenti rosso, verde, blu e alfa di un colore.


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a>Commenti

**D2d1 \_ COLOR \_ f** è un typedef per [**D2D \_ Color \_ f**](d2d-color-f.md), che è a sua volta un typedef per [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md). Per informazioni sui membri forniti da **d2d1 \_ Color \_ F**, vedere [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).

La classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) fornisce un set di colori e funzioni di supporto predefiniti per la definizione dei colori. Per ulteriori informazioni, vedere la Guida di riferimento a [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usata la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) per specificare un colore predefinito (nero) durante la creazione di un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



Nell'esempio seguente viene utilizzata la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) per specificare un colore utilizzando i valori rosso, verde, blu e alfa.


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2DBaseTypes. h (include D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

