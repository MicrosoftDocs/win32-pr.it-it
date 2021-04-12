---
title: Effetto ombreggiatura
description: Usare l'effetto ombreggiatura per generare un'ombreggiatura dal canale alfa di un'immagine.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- effetto ombreggiatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340412"
---
# <a name="shadow-effect"></a>Effetto ombreggiatura

Usare l'effetto ombreggiatura per generare un'ombreggiatura dal canale alfa di un'immagine. L'ombreggiatura è più opaca per i valori alfa più elevati e più trasparente per i valori alfa inferiori. È possibile impostare la quantità di sfocatura e il colore dell'ombreggiatura.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità di ottimizzazione](#optimization-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

Il CLSID per questo effetto è CLSID \_ D2D1Shadow.

## <a name="example-image"></a>Immagine di esempio

Nell'esempio riportato di seguito viene illustrato l'output dell'effetto di ombreggiatura convertito verso il basso e verso destra con l'immagine di origine composita nel percorso originale. L'effetto di ombreggiatura restituisce solo l'ombreggiatura.



| Prima                                                  |
|---------------------------------------------------------|
| ![immagine prima dell'effetto.](images/8-crop.png)      |
| After                                                   |
| ![immagine dopo la trasformazione.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BlurStandardDeviation<br/> \_ \_ \_ Deviazione standard della sfocatura d2d1 Shadow Prop \_ \_<br/> | Quantità di sfocatura da applicare al canale alfa dell'immagine. È possibile calcolare il raggio di sfocatura del kernel moltiplicando la deviazione standard di 3. Le unità della deviazione standard e del raggio di sfocatura sono dip.<br/> Questa proprietà corrisponde alla proprietà della deviazione standard [sfocatura gaussiana](gaussian-blur.md) . <br/> Il tipo è FLOAT.<br/> Il valore predefinito è 3.0 f.<br/> |
| Colore<br/> \_Colore della \_ prop \_ shadow d2d1<br/>                                     | Colore dell'ombreggiatura. Questa proprietà è un \_ vettore d2d1 \_ 4F definito come: (R, G, B, a). È necessario specificare questo colore nell'Alpha lineare.<br/> Il tipo è D2D1 \_ vector \_ 4F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f, 1.0 f}.<br/>                                                                                                                                                                     |
| Optimization<br/> Ottimizzazione di D2D1 \_ shadow \_ prop \_<br/>                       | Livello di ottimizzazione delle prestazioni.<br/> Il tipo è l' \_ ottimizzazione dell'ombreggiatura d2d1 \_ .<br/> Il valore predefinito è l' \_ ottimizzazione dell'ombreggiatura d2d1 \_ \_ .<br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a>Modalità di ottimizzazione



| Nome                                          | Descrizione                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| \_Velocità di \_ ottimizzazione \_ DIRECTIONALBLUR di d2d1    | Applica le ottimizzazioni interne, ad esempio la pre-scalabilità a raggi relativamente piccoli. Usa il filtro lineare.                                  |
| \_Ottimizzazione d2d1 \_ DIRECTIONALBLUR \_ | Usa le stesse soglie di ottimizzazione della modalità velocità, ma usa il filtro trilineare.                                                    |
| \_ \_ Qualità ottimizzazione DIRECTIONALBLUR \_ d2d1  | USA solo le ottimizzazioni interne con raggi di sfocatura grandi, in cui è meno probabile che le approssimazioni siano visibili. Usa il filtro trilineare. |



 

## <a name="output-bitmap"></a>Bitmap di output

La dimensione della bitmap di output corrisponde alla dimensione dell'output di sfocatura. La quantità di dimensioni della bitmap di output rispetto alla bitmap originale può essere calcolata utilizzando l'equazione seguente:

Aumento dimensioni bitmap di output (X e Y) = BlurStandardDeviation (DIP) (device-independent pixel) \* 6 \* (dpi utente)/96

L'output aumenta in modo uniforme in tutte le direzioni, quindi, ad esempio, se le dimensioni aumentano di 10 pixel in ogni direzione, l'angolo superiore sinistro della bitmap si trova in corrispondenza di (-5,-5) e il diritto inferiore si trova in (105, 105), come illustrato nel diagramma.

![diagramma di crescita della dimensione dell'output dell'effetto ombreggiatura.](images/drop-shadow-output-growth.png)

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

 

