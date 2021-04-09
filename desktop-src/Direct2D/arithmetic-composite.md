---
title: Effetto composito aritmetico
description: Usare l'effetto composito aritmetico per combinare 2 immagini usando una somma ponderata dei pixel dalle immagini di input.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- effetto composito aritmetico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964690"
---
# <a name="arithmetic-composite-effect"></a>Effetto composito aritmetico

Usare l'effetto composito aritmetico per combinare 2 immagini usando una somma ponderata dei pixel dalle immagini di input.

Il CLSID per questo effetto è CLSID \_ D2D1ArithmeticComposite.

-   [Formula](#formula)
-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="formula"></a>Formula

Questa formula viene usata per calcolare questo effetto.

Output<sub>RGBA</sub> = C1 \* source<sub>RGBA</sub> \* Destination<sub>RGBA</sub> + C2 \* source<sub>RGBA</sub> + C3 \* Destination<sub>RGBA</sub> + C4

Dove C1, C2, C3, C4 sono coefficienti impostati.

Il mapping dei coefficienti ai valori in un \_ vettore d2d1 \_ 4F (x, y, z, w):

-   x = C1
-   y = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>Immagine di esempio

Un esempio semplice consiste nell'aggiungere i pixel di origine e di destinazione. Nell'esempio, 2 rettangoli arrotondati vengono composti insieme. Il rettangolo di origine è blu e la destinazione è rossa.

L'immagine è l'output dell'effetto composito aritmetico con i coefficienti dell'equazione impostati sui valori qui.

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![immagine di esempio che mostra 2 rettangoli arrotondati delle stesse dimensioni che si sovrappongono utilizzando l'effetto composito aritmetico.](images/arithmetic-50-percent.png)

Il risultato è che vengono aggiunti i valori dei pixel per l'origine e la destinazione. Le aree in cui i rettangoli non si sovrappongono i valori RGBA sono tutti 0. Laddove i rettangoli si sovrappongono, il colore è Magenta perché i valori R e B sono entrambi al massimo.

Ecco un'altra immagine di esempio con il codice.



| Prima dell'immagine 1                                                             |
|----------------------------------------------------------------------------|
| ![prima immagine di origine prima dell'effetto.](images/default-before.jpg)    |
| Prima dell'immagine 2                                                             |
| ![seconda immagine prima dell'effetto.](images/4-arthimetic-composite2.jpg) |
| After                                                                      |
| ![immagine dopo la trasformazione.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coefficienti<br/> \_COefficienti della prop ARITHMETICCOMPOSITE d2d1 \_ \_<br/> | Coefficienti per l'equazione utilizzata per comporre le due immagini di input. I coefficienti sono senza unità e senza limiti. Il tipo è D2D1 \_ vector \_ 4F.<br/> Il valore predefinito è {1.0 f, 0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                                                 |
| ClampOutput<br/> D2D1 \_ ARITHMETICCOMPOSITE \_ prop \_ \_ output Clamp<br/> | L'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. <br/> Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto. Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/> |



 

## <a name="output-bitmap"></a>Bitmap di output

La bitmap di output dipende dai valori coefficienti. Queste sono le possibili dimensioni della bitmap di output.

-   Se C1 è l'unico coefficiente diverso da zero, la dimensione di output è l'intersezione dei rettangoli di input.
-   Se C2 è l'unico coefficiente diverso da zero, la dimensione di output corrisponde alla dimensione del rettangolo di origine.
-   Se C3 è l'unico coefficiente diverso da zero, la dimensione di output corrisponde alla dimensione del rettangolo di destinazione.
-   Se tutti i coefficienti sono pari a zero, la dimensione di output è un rettangolo vuoto.
-   Per tutti gli altri valori coefficienti, le dimensioni di output sono l'Unione dei rettangoli di input.

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

 

