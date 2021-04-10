---
title: Effetto Flood
description: Usare l'effetto Flood per generare una bitmap in base al colore e al valore alfa specificati. È possibile utilizzare questo effetto quando si desidera un colore specifico come input per un effetto, ad esempio un colore di sfondo.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- effetto Flood
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964603"
---
# <a name="flood-effect"></a>Effetto Flood

Usare l'effetto Flood per generare una bitmap in base al colore e al valore alfa specificati. È possibile utilizzare questo effetto quando si desidera un colore specifico come input per un effetto, ad esempio un colore di sfondo.

> [!Note]  
> L'effetto passa lungo il valore del colore specificato, come specificato. È necessario pre-moltiplicare manualmente i valori se si prevede di passare l'output agli effetti che prevedono un input pre-moltiplicato.

 

Il CLSID per questo effetto è CLSID \_ D2D1Flood.

L'effetto Flood non ha un'immagine di input.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![immagine di esempio dell'effetto Flood che produce l'effetto verde.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Colore<br/> \_Colore della \_ prop d2d1 Flood \_<br/> | Il colore e l'opacità della bitmap. Questa proprietà è un \_ vettore d2d1 \_ 4F. I singoli valori per ogni canale sono di tipo FLOAT, unbounded e senza unità. L'effetto non modifica i valori per i canali.<br/> I valori di RGBA per ogni canale variano da 0 a 1.<br/> Il tipo è D2D1 \_ vector \_ 4F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f, 1.0 f}.<br/> |



 

## <a name="output-bitmap"></a>Bitmap di output

Questo effetto genera una bitmap di dimensioni infinite logicamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

