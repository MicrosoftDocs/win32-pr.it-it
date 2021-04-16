---
title: Effetto sfocatura gaussiana
description: Utilizzare l'effetto di sfocatura gaussiana per creare una sfocatura basata sulla funzione gaussiana sull'intera immagine di input.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Sfocatura gaussiana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104570870"
---
# <a name="gaussian-blur-effect"></a>Effetto sfocatura gaussiana

Utilizzare l'effetto di sfocatura gaussiana per creare una sfocatura basata sulla funzione gaussiana sull'intera immagine di input.

È possibile utilizzare questo effetto per creare bagliori e ombreggiature e utilizzare l'effetto [composito](composite.md) per applicare il risultato all'immagine originale. È utile nell'elaborazione di foto per filtri come evidenziazioni e ombre. È possibile usare l'output di questo effetto per l'input in effetti di illuminazione, ad esempio l' [illuminazione speculare](specular-lighting.md) o gli effetti di [illuminazione diffusa](diffuse-lighting.md) , perché il canale alfa è sfocato e gli effetti di illuminazione usano il canale alfa per determinare la geometria della superficie come mappa di altezza.

Questo effetto viene usato dall'effetto di [ombreggiatura](drop-shadow.md) incorporato.

Il CLSID per questo effetto è CLSID \_ D2D1GaussianBlur.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità di ottimizzazione](#optimization-modes)
-   [Modalità bordo](#border-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                       |
|--------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)   |
| After                                                        |
| ![immagine dopo la trasformazione.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                    | Descrizione                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> D2D1 \_ GAUSSIANBLUR \_ prop \_ \_ deviazione standard<br/> | Quantità di sfocatura da applicare all'immagine. È possibile calcolare il raggio di sfocatura del kernel moltiplicando la deviazione standard di 3. Le unità della deviazione standard e del raggio di sfocatura sono dip. Il valore zero DIP Disabilita interamente questo effetto. Il tipo è FLOAT.<br/> Il valore predefinito è 3.0 f.<br/> |
| Optimization<br/> \_Ottimizzazione della \_ prop \_ GAUSSIANBLUR d2d1<br/>             | Modalità di ottimizzazione. Per altre informazioni, vedere [modalità di ottimizzazione](#optimization-modes) . Il tipo è D2D1 \_ GAUSSIANBLUR \_ Optimization.<br/> Il valore predefinito è D2D1 \_ GAUSSIANBLUR \_ Optimization \_ Balanced.<br/>                                                                                                            |
| BorderMode<br/> \_ \_ \_ Modalità bordo prop GAUSSIANBLUR \_ d2d1<br/>               | Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard. Per altre informazioni, vedere [Border modes](#border-modes) . <br/> Il tipo è D2D1 \_ GAUSSIANBLUR \_ Border \_ mode.<br/> Il valore predefinito è D2D1 \_ Border \_ mode \_ .<br/>                                                                                   |



 

## <a name="optimization-modes"></a>Modalità di ottimizzazione



| Nome                                          | Descrizione                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| \_Velocità di \_ ottimizzazione \_ DIRECTIONALBLUR di d2d1    | Applica le ottimizzazioni interne, ad esempio la pre-scalabilità a raggi relativamente piccoli. Usa il filtro lineare.                                  |
| \_Ottimizzazione d2d1 \_ DIRECTIONALBLUR \_ | Usa le stesse soglie di ottimizzazione della modalità velocità, ma usa il filtro trilineare.                                                    |
| \_ \_ Qualità ottimizzazione DIRECTIONALBLUR \_ d2d1  | USA solo le ottimizzazioni interne con raggi di sfocatura grandi, in cui è meno probabile che le approssimazioni siano visibili. Usa il filtro trilineare. |



 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modalità bordo \_ d2d1 \_ Soft | L'effetto Ritaglia l'immagine con i pixel neri trasparenti quando applica il kernel di sfocatura, ottenendo un bordo flessibile. <br/>                                                                                             |
| \_Modalità bordo \_ d2d1 \_ | L'effetto fissa l'output alla dimensione dell'immagine di input. Quando l'effetto applica il kernel di sfocatura, estende l'immagine di input con una trasformazione del bordo di tipo mirror per i campioni all'esterno dei limiti di input.<br/> |



 

## <a name="output-bitmap"></a>Bitmap di output

L'output di questo effetto può essere maggiore della bitmap di input in base al raggio di sfocatura e alla modalità bordo. Se la modalità bordo è impostata su D2D1 \_ bordo \_ modalità \_ soft il ize della bitmap di output aumenta in base alle dimensioni del kernel di sfocatura, rappresentato in pixel. Questa tabella fornisce un'equazione che è possibile usare per calcolare la bitmap di output.

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

Quindi, se le dimensioni dell'immagine aumentano di 10 pixel in ogni direzione, l'angolo superiore sinistro dell'immagine si troverà in corrispondenza di (-5,-5) mentre la parte inferiore destra si trova in corrispondenza di (105, 105).

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

 

