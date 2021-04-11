---
title: Effetto composito
description: Usare l'effetto composito per combinare due o più immagini. Questo effetto ha 13 diverse modalità composite.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- effetto composito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964368"
---
# <a name="composite-effect"></a>Effetto composito

Usare l'effetto composito per combinare due o più immagini. Questo effetto ha 13 diverse modalità composite. T

L'effetto composito accetta due o più input. Quando si specificano 2 immagini, la destinazione è il primo input (indice 0) e l'origine è il secondo input (indice 1). Se si specificano più di 2 input, le immagini vengono composte a partire dal primo input e dal secondo e così via.

Questo effetto implementa tutte le modalità usando l'unità di fusione dell'unità di elaborazione grafica (GPU).

Il CLSID per questo effetto è CLSID \_ D2D1Composite.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Tipi di modalità](#mode-types)
-   [Codice di esempio](#sample-code)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'immagine mostra due rettangoli arrotondati delle stesse dimensioni sovrapposti. Il rettangolo blu è l'origine e il rettangolo rosso è la destinazione. Le immagini sono state composte con l'origine in modalità.

![immagine di esempio che mostra 2 rettangoli arrotondati delle stesse dimensioni che si sovrappongono usando la modalità di origine.](images/composite-over.png)

Ecco un altro esempio che usa la modalità predefinita.



| Prima dell'immagine 1                                                          |
|-------------------------------------------------------------------------|
| ![prima immagine di origine prima dell'effetto.](images/default-before.jpg) |
| Prima dell'immagine 2                                                          |
| ![seconda immagine prima dell'effetto.](images/3-composite(2of2).png)    |
| After                                                                   |
| ![immagine dopo la trasformazione.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                     | Tipo e valore predefinito                                                          | Descrizione                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| Mode<br/> \_Modalità prop composito d2d1 \_ \_<br/> | \_Modalità composita d2d1 \_<br/> \_ \_ Origine modalità COMPOSIta d2d1 \_ \_<br/> | Modalità utilizzata per l'effetto. |



 

## <a name="mode-types"></a>Tipi di modalità

La tabella seguente mostra le modalità di questo effetto. Le equazioni elencate nella tabella utilizzano questi elementi:

-   O = output
-   S = origine
-   SA = Alpha di origine
-   D = destinazione
-   DA = Alpha di destinazione



| Enumerazione                                  | Equazione                          | Dimensioni bitmap di output                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| \_ \_ Origine modalità COMPOSIta d2d1 \_ \_          | O = S + (1 SA) \* D             | Unione delle bitmap di origine e di destinazione                                                                 |
| \_ \_ Destinazione modalità COMPOSIta d2d1 \_ \_     | O = (1 DA) \* S + D             | Unione delle bitmap di origine e di destinazione                                                                 |
| \_Origine modalità composita d2d1 \_ \_ \_ in            | O = DA \* S                       | Intersezione delle bitmap di origine e di destinazione                                                          |
| \_Destinazione modalità composita d2d1 \_ \_ \_ in       | O = SA \* D                       | Intersezione delle bitmap di origine e di destinazione                                                          |
| \_ \_ Origine modalità COMPOSIta d2d1 \_ \_           | O = (1-DA) \* S                 | Area della bitmap di origine                                                                             |
| \_ \_ \_ Uscita dalla destinazione della modalità composita d2d1 \_      | O = (1-SA) \* D                 | Area della bitmap di destinazione                                                                        |
| \_Origine modalità composita d2d1 in \_ \_ \_ cima          | O = DA \* S + (1-SA) \* D       | Area della bitmap di destinazione                                                                        |
| \_Destinazione modalità composita d2d1 in \_ \_ \_ cima     | O = (1-DA) \* S + SA \* D       | Area della bitmap di origine                                                                             |
| \_Xor in \_ modalità COMPOSIta d2d1 \_                   | O = (1-DA) \* S + (1-SA) \* D | Unione delle bitmap di origine e di destinazione                                                                 |
| \_Modalità composita d2d1 \_ \_ Plus                  | O = S + D                         | Unione delle bitmap di origine e di destinazione                                                                 |
| \_Copia di \_ origine in modalità COMPOSIta d2d1 \_ \_          | O = S                             | Area della bitmap di origine                                                                             |
| \_Copia di \_ \_ origine vincolata in modalità composita \_ d2d1 \_ | O = S (solo dove esiste l'origine)  | Unione delle bitmap di origine e di destinazione. La destinazione non viene sovrascritta dove l'origine non esiste. |
| \_Maschera della modalità composita d2d1 \_ \_ \_ invertita          | O = (1 D) \* S + (1 SA) \* D  | Unione delle bitmap di origine e di destinazione. I valori alfa sono invariati.                                 |



 

Nella figura seguente viene illustrato un esempio di ogni modalità con immagini con un'opacità di 1,0 o 0,5.

![immagine di esempio di ciascuna modalità con opacità impostata su 1,0 o 0,5.](images/composite-types.png)

## <a name="sample-code"></a>Codice di esempio

Per un esempio di questo effetto, scaricare l' [esempio Direct2D composite Effect modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

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

 

