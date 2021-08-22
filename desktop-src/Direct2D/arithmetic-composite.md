---
title: Effetto composito aritmetico
description: Usare l'effetto composito aritmetico per combinare 2 immagini usando una somma ponderata di pixel dalle immagini di input.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- effetto composito aritmetico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45976d577299bda7dfcef9bf20eff4980cc67ac105cb14fa793065d7ce1857f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641975"
---
# <a name="arithmetic-composite-effect"></a>Effetto composito aritmetico

Usare l'effetto composito aritmetico per combinare 2 immagini usando una somma ponderata di pixel dalle immagini di input.

Il CLSID per questo effetto è CLSID \_ D2D1ArithmeticComposite.

-   [Formula](#formula)
-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="formula"></a>Formula

La formula qui viene usata per calcolare questo effetto.

Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4

Dove C1, C2, C3, C4 sono coefficienti impostati.

I coefficienti vengono mappati ai valori in un vettore D2D1 \_ \_ 4F (x, y, z, w):

-   x = C1
-   y = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>Immagine di esempio

Un semplice esempio è l'aggiunta dei pixel di origine e di destinazione. Nell'esempio vengono compositi due rettangoli arrotondati. Il rettangolo di origine è blu e la destinazione è rossa.

L'immagine è l'output dell'effetto Composito aritmetico con i coefficienti dell'equazione impostati sui valori qui.

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![un'immagine di esempio che mostra 2 rettangoli arrotondati delle stesse dimensioni che si sovrappongono usando l'effetto composito aritmetico.](images/arithmetic-50-percent.png)

Il risultato è che vengono aggiunti i valori in pixel per l'origine e la destinazione. Le aree in cui i rettangoli non si sovrappongono ai valori RGBA sono tutte 0. Quando i rettangoli si sovrappongono, il colore è magenta perché i valori R e B sono entrambi al massimo.

Ecco un'altra immagine di esempio con codice.



| Prima dell'immagine 1                                                             |
|----------------------------------------------------------------------------|
| ![prima dell'effetto.](images/default-before.jpg)    |
| Prima dell'immagine 2                                                             |
| ![la seconda immagine prima dell'effetto.](images/4-arthimetic-composite2.jpg) |
| After                                                                      |
| ![l'immagine dopo la trasformazione.](images/4-arithmeticcomposite.png)        |



 


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



## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coefficienti<br/> COEFFICIENTI DELLE PROPRIETÀ \_ ARITMETICHE D2D1 \_ \_<br/> | Coefficienti per l'equazione usata per creare le due immagini di input. I coefficienti sono senza unità e non associati. Il tipo è D2D1 \_ VECTOR \_ 4F.<br/> Il valore predefinito è {1.0f, 0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                                                 |
| ClampOutput<br/> OUTPUT DEL CLAMP DELLA PROPRIETÀ \_ ARITHMETICCOMPOSITE D2D1 \_ \_ \_<br/> | L'effetto stringe i valori di colore tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. <br/> Se si imposta questa proprietà su TRUE, l'effetto anteterà i valori. Se si imposta questa opzione su FALSE, l'effetto non stringerà i valori di colore, ma altri effetti e la superficie di output potrebbero stringere i valori se non hanno una precisione sufficiente.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/> |



 

## <a name="output-bitmap"></a>Bitmap di output

La bitmap di output dipende dai valori del coefficiente. Queste sono le possibili dimensioni delle bitmap di output.

-   Se C1 è l'unico coefficiente diverso da zero, le dimensioni di output sono l'intersezione dei rettangoli di input.
-   Se C2 è l'unico coefficiente diverso da zero, le dimensioni di output sono le dimensioni del rettangolo di origine.
-   Se C3 è l'unico coefficiente diverso da zero, le dimensioni di output sono le dimensioni del rettangolo di destinazione.
-   Se tutti i coefficienti sono pari a zero, le dimensioni di output sono un rettangolo vuoto.
-   Per tutti gli altri valori di coefficiente, le dimensioni di output sono l'unione dei rettangoli di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

