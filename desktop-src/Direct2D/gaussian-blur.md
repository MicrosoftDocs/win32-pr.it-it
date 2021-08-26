---
title: Effetto sfocatura gaussiano
description: Usare l'effetto sfocatura gaussiano per creare una sfocatura basata sulla funzione Gaussian sull'intera immagine di input.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Sfocatura gaussiana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b759ed0f5f70c4fc11ad902c7a45db3b3059847ce6895d25c3dbb9c9eee8330
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967086"
---
# <a name="gaussian-blur-effect"></a>Effetto sfocatura gaussiano

Usare l'effetto sfocatura gaussiano per creare una sfocatura basata sulla funzione Gaussian sull'intera immagine di input.

È possibile usare questo effetto per creare alone e ombreggiature e usare [l'effetto](composite.md) composito per applicare il risultato all'immagine originale. È utile nell'elaborazione di foto per filtri come evidenziazioni e ombreggiature. È possibile usare l'output di questo effetto [](specular-lighting.md) per l'input negli effetti di illuminazione, ad esempio gli effetti Illuminazione speculare o Illuminazione diffusa, perché anche il canale alfa è sfocato e gli effetti di illuminazione usano il canale alfa per determinare la geometria della superficie come mappa di altezza. [](diffuse-lighting.md)

Questo effetto viene usato dall'effetto [Ombreggiatura](drop-shadow.md) predefinito.

Il CLSID per questo effetto è CLSID \_ D2D1GaussianBlur.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità di ottimizzazione](#optimization-modes)
-   [Modalità bordo](#border-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                       |
|--------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)   |
| After                                                        |
| ![l'immagine dopo la trasformazione.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                                                    | Descrizione                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> DEVIAZIONE STANDARD DELLA PROPRIETÀ D2D1 \_ GAUSSIANBLUR \_ \_ \_<br/> | Quantità di sfocatura da applicare all'immagine. È possibile calcolare il raggio di sfocatura del kernel moltiplicando la deviazione standard per 3. Le unità della deviazione standard e del raggio della sfocatura sono DIP. Il valore zero DIP disabilita completamente questo effetto. Il tipo è FLOAT.<br/> Il valore predefinito è 3,0f.<br/> |
| Optimization<br/> OTTIMIZZAZIONE DELLA PROPRIETÀ D2D1 \_ GAUSSIANBLUR \_ \_<br/>             | Modalità di ottimizzazione. Per [altre informazioni, vedi](#optimization-modes) Modalità di ottimizzazione. Il tipo è D2D1 \_ GAUSSIANBLUR \_ OPTIMIZATION.<br/> Il valore predefinito è D2D1 \_ GAUSSIANBLUR \_ OPTIMIZATION \_ BALANCED.<br/>                                                                                                            |
| BorderMode<br/> MODALITÀ BORDO DELLA PROPRIETÀ D2D1 \_ GAUSSIANBLUR \_ \_ \_<br/>               | Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard. Per [altre informazioni, vedi](#border-modes) Modalità bordo. <br/> Il tipo è D2D1 \_ GAUSSIANBLUR \_ BORDER \_ MODE.<br/> Il valore predefinito è D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                   |



 

## <a name="optimization-modes"></a>Modalità di ottimizzazione



| Nome                                          | Descrizione                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ SPEED    | Applica le ottimizzazioni interne, ad esempio il pre-ridimensionamento a raggi relativamente piccoli. Usa il filtro lineare.                                  |
| OTTIMIZZAZIONE DI D2D1 \_ DIRECTIONALBLUR \_ \_ BILANCIATA | Usa le stesse soglie di ottimizzazione della modalità velocità, ma usa il filtro trilineare.                                                    |
| QUALITÀ DI OTTIMIZZAZIONE D2D1 \_ DIRECTIONALBLUR \_ \_  | Usa solo le ottimizzazioni interne con raggi di sfocatura di grandi dimensioni, in cui le approssimazioni hanno meno probabilità di essere visibili. Usa il filtro trilineare. |



 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODALITÀ BORDO D2D1 \_ \_ \_ SOFT | L'effetto riempire l'immagine con pixel neri trasparenti quando applica il kernel sfocatura, determinando un bordo sfuocato. <br/>                                                                                             |
| MODALITÀ BORDO D2D1 \_ \_ \_ HARD | L'effetto stringe l'output alle dimensioni dell'immagine di input. Quando l'effetto applica il kernel di sfocatura, estende l'immagine di input con una trasformazione del bordo di tipo speculare per i campioni al di fuori dei limiti di input.<br/> |



 

## <a name="output-bitmap"></a>Bitmap di output

L'output di questo effetto può essere maggiore della bitmap di input in base al raggio di sfocatura e alla modalità bordo. Se la modalità bordo è impostata su D2D1 BORDER MODE SOFT, le dimensioni della bitmap di output aumentano in base alle dimensioni del \_ kernel di sfocatura, \_ \_ rappresentate in pixel. Questa tabella fornisce un'equazione che è possibile usare per calcolare la bitmap di output.

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

Pertanto, se le dimensioni dell'immagine aumentano di 10 pixel in ogni direzione, l'angolo superiore sinistro dell'immagine si trova in corrispondenza di (-5, -5) mentre l'angolo inferiore destro si trova in corrispondenza di (105, 105).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

