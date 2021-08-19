---
title: Effetto composito
description: Usare l'effetto composito per combinare 2 o più immagini. Questo effetto ha 13 modalità composite diverse.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- effetto composito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cf326e5d0bfb33b3dc927ba7366eb6d2b343a1a50db462de58fac8ef648bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826589"
---
# <a name="composite-effect"></a>Effetto composito

Usare l'effetto composito per combinare 2 o più immagini. Questo effetto ha 13 modalità composite diverse. T

L'effetto composito accetta 2 o più input. Quando si specificano 2 immagini, destination è il primo input (indice 0) e l'origine è il secondo input (indice 1). Se si specificano più di 2 input, le immagini vengono composte a partire dal primo input e dal secondo e così via.

Questo effetto implementa tutte le modalità usando l'unità di fusione dell'unità di elaborazione grafica (GPU).

Il CLSID per questo effetto è CLSID \_ D2D1Composite.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Tipi di modalità](#mode-types)
-   [Codice di esempio](#sample-code)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'immagine mostra 2 rettangoli arrotondati delle stesse dimensioni che si sovrappongono. Il rettangolo blu è l'origine e il rettangolo rosso è la destinazione. Le immagini sono state composte con la modalità Source Over.

![immagine di esempio che mostra 2 rettangoli arrotondati della stessa dimensione che si sovrappongono usando la modalità source over.](images/composite-over.png)

Ecco un altro esempio che usa la modalità predefinita.



| Prima dell'immagine 1                                                          |
|-------------------------------------------------------------------------|
| ![la prima immagine di origine prima dell'effetto.](images/default-before.jpg) |
| Prima dell'immagine 2                                                          |
| ![seconda immagine prima dell'effetto.](images/3-composite(2of2).png)    |
| After                                                                   |
| ![l'immagine dopo la trasformazione.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                     | Tipo e valore predefinito                                                          | Descrizione                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| Mode<br/> Modalità COMPOSITE PROP D2D1 \_ \_ \_<br/> | MODALITÀ COMPOSITA D2D1 \_ \_<br/> ORIGINE IN MODALITÀ COMPOSITA D2D1 \_ \_ \_ \_ SU<br/> | Modalità utilizzata per l'effetto. |



 

## <a name="mode-types"></a>Tipi di modalità

La tabella seguente illustra le modalità di questo effetto. Le equazioni elencate nella tabella usano questi elementi:

-   O = Output
-   S = Origine
-   SA = Alfa di origine
-   D = Destinazione
-   DA = Alfa di destinazione



| Enumerazione                                  | Equazione                          | Dimensioni bitmap di output                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| ORIGINE IN MODALITÀ COMPOSITA D2D1 \_ \_ \_ \_ SU          | O = S + (1 SA) \* D             | Unione di bitmap di origine e di destinazione                                                                 |
| D2D1 \_ COMPOSITE \_ MODE \_ DESTINATION \_ OVER     | O = (1 DA) \* S + D             | Unione di bitmap di origine e di destinazione                                                                 |
| ORIGINE IN MODALITÀ COMPOSITA D2D1 \_ \_ \_ \_ IN            | O = DA \* S                       | Intersezione delle bitmap di origine e di destinazione                                                          |
| DESTINAZIONE DELLA MODALITÀ COMPOSITA D2D1 \_ \_ \_ \_ IN       | O = SA \* D                       | Intersezione delle bitmap di origine e di destinazione                                                          |
| ORIGINE IN MODALITÀ COMPOSITA D2D1 \_ \_ IN \_ \_ USCITA           | O = (1 - DA) \* S                 | Area della bitmap di origine                                                                             |
| DESTINAZIONE IN MODALITÀ COMPOSITA D2D1 \_ \_ IN \_ \_ USCITA      | O = (1 - SA) \* D                 | Area della bitmap di destinazione                                                                        |
| ORIGINE IN MODALITÀ COMPOSITA D2D1 \_ \_ IN \_ \_ ALTO          | O = DA \* S + (1 - SA) \* D       | Area della bitmap di destinazione                                                                        |
| D2D1 \_ COMPOSITE \_ MODE \_ DESTINATION \_ ATOP     | O = (1 - DA) \* S + SA \* D       | Area della bitmap di origine                                                                             |
| D2D1 \_ COMPOSITE \_ MODE \_ XOR                   | O = (1 - DA) \* S + (1 - SA) \* D | Unione di bitmap di origine e di destinazione                                                                 |
| MODALITÀ COMPOSITA D2D1 \_ \_ \_ PLUS                  | O = S + D                         | Unione di bitmap di origine e di destinazione                                                                 |
| COPIA DI ORIGINE IN \_ MODALITÀ COMPOSITA D2D1 \_ \_ \_          | O = S                             | Area della bitmap di origine                                                                             |
| COPIA DI ORIGINE \_ DELIMITATA \_ IN MODALITÀ \_ COMPOSITA \_ D2D1 \_ | O = S (solo dove è presente l'origine)  | Unione di bitmap di origine e di destinazione. La destinazione non viene sovrascritta dove l'origine non esiste. |
| MASCHERA IN MODALITÀ COMPOSITA D2D1 \_ \_ \_ \_ INVERT          | O = (1 D) \* S + (1 SA) \* D  | Unione di bitmap di origine e di destinazione. I valori alfa rimangono invariati.                                 |



 

La figura seguente mostra un esempio di ognuna delle modalità con immagini con opacità 1.0 o 0.5.

![immagine di esempio di ognuna delle modalità con opacità impostata su 1,0 o 0,5.](images/composite-types.png)

## <a name="sample-code"></a>Codice di esempio

Per un esempio di questo effetto, scaricare l'esempio [di modalità effetto composito Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

