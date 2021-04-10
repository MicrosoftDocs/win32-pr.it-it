---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Memorizza una coppia ordinata di interi, generalmente la larghezza e l'altezza di un rettangolo.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119311"
---
# <a name="d2d1_size_u"></a>D2D1 \_ dimensioni \_ U

Memorizza una coppia ordinata di interi, generalmente la larghezza e l'altezza di un rettangolo.


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a>Commenti

Analogamente ai punti, le dimensioni rappresentano un altro concetto di grafica importante. In Direct2D le dimensioni sono rappresentate dalle strutture della dimensione **d2d1 \_ \_ U** o [**d2d1 \_ \_ F**](d2d1-size-f.md) . Entrambi contengono una coppia ordinata di numeri. La struttura **d2d1 della \_ dimensione \_ U** contiene una coppia ordinata di valori **UInt32** e la struttura **d2d1 \_ size \_ F** contiene una coppia ordinata di valori **float** .

La **struttura \_ \_ U della dimensione d2d1** rappresenta un modo pratico per archiviare una coppia ordinata di numeri, ad esempio la larghezza e l'altezza di un rettangolo.

**D2d1 \_ SIZE \_ u** è un nuovo nome per un tipo già definito **D2D \_ size \_ u**. È possibile usare la funzione **D2D1:: dimensionat** per creare una **struttura \_ \_ U d2d1 size** . Un uso comune di questa struttura è quello di specificare le dimensioni in pixel di una struttura di [**\_ proprietà della \_ \_ destinazione \_ di rendering HWND d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) . Di seguito viene fornito un esempio di utilizzo di questa struttura.


```C++
    if (!m_pRenderTarget)
    {
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
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2DBaseTypes. h (include D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D2D \_ dimensioni \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[**\_Dimensioni d2d1 \_ F**](d2d1-size-f.md)
</dt> <dt>

[**D2D1:: HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

