---
title: Metodi CreateHwndRenderTarget di ID2D1Factory (D2d1. h)
description: Crea un ID2D1HwndRenderTarget, una destinazione di rendering che esegue il rendering in una finestra.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Metodo CreateHwndRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329880"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a>Metodi ID2D1Factory:: CreateHwndRenderTarget

Crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), una destinazione di rendering che esegue il rendering in una finestra.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                                                                              | Descrizione                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**CreateHwndRenderTarget ( \_ \_ proprietà destinazione rendering \_ d2d1 \* , \_ \_ proprietà destinazione rendering HWND d2d1 \_ \_ \* , ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) | Crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), una destinazione di rendering che esegue il rendering in una finestra.<br/> |
| [**CreateHwndRenderTarget ( \_ \_ proprietà destinazione rendering d2d1 \_&, \_ proprietà di \_ destinazione rendering HWND d2d1 \_ \_&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))   | Crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), una destinazione di rendering che esegue il rendering in una finestra.<br/> |



## <a name="remarks"></a>Commenti

Quando si crea una destinazione di rendering e l'accelerazione hardware è disponibile, è necessario allocare risorse sulla GPU del computer. Creando una destinazione di rendering una volta e mantenendola il più a lungo possibile, si ottengono vantaggi in termini di prestazioni. L'applicazione deve creare le destinazioni di rendering una volta e mantenerle per la durata dell'applicazione o fino a quando non viene ricevuto l'errore di [**\_ \_ destinazione D2DERR ricreate**](direct2d-error-codes.md) . Quando si riceve questo errore, è necessario ricreare la destinazione di rendering (e tutte le risorse create).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
