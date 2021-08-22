---
title: Effetto matrice di colori
description: Usare l'effetto matrice di colori per modificare i valori RGBA di una bitmap.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- Effetto matrice di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8bb461698e4f8b39eef3bed57fc21947f3cc1175c1bdf4f990629db87e1c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653306"
---
# <a name="color-matrix-effect"></a>Effetto matrice di colori

Usare l'effetto matrice di colori per modificare i valori RGBA di una bitmap.

È possibile usare questo effetto per:

-   Rimuovere un canale di colore da un'immagine.
-   Ridurre il colore di un'immagine.
-   Scambiare i canali di colore.
-   Combinare i canali di colore.

Molti effetti predefiniti sono specializzazioni della matrice di colori ottimizzate per l'uso previsto degli effetti. Ad [esempio, saturazione,](saturation.md) [rotazione della tonalità,](hue-rotate.md) [seppia](sepia-effect.md)e [temperatura e tinta.](temperature-and-tint-effect.md)

Il CLSID per questo effetto è CLSID \_ D2D1ColorMatrix.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità alfa](#alpha-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'esempio seguente mostra le immagini di input e output dell'effetto matrice di colori che scambia i canali rosso e blu.



| Prima                                                       |
|--------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)   |
| After                                                        |
| ![l'immagine dopo la trasformazione.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



Questo effetto moltiplica i valori RGBA dell'immagine per una matrice principale di colonna 5x4, come illustrato in questa equazione.

![una definizione di matrice di esempio.](images/color-matrix-formula.png)

Questo effetto funziona su immagini alfa rette e premoltilied.

## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Colormatrix<br/> MATRICE DI COLORI \_ DI COLORMATRIX \_ PROP \_ D2D1 \_<br/> | Matrice 5x4 di valori float. Gli elementi nella matrice non sono delimitati e sono senza unità.<br/> Il valore predefinito è la matrice di identità.<br/> Il tipo è D2D1 \_ MATRIX \_ 5X4 \_ F.<br/> Il valore predefinito è Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0). <br/>                                                                                                                                                                                                                        |
| AlphaMode<br/> MODALITÀ ALFA \_ DI COLORMATRIX \_ PROP \_ D2D1 \_<br/>     | Modalità alfa dell'output. Per [altre informazioni, vedere](#alpha-modes) Modalità alfa. <br/> Il tipo è D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE.<br/> Il valore predefinito è D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ PREMULTIPLIED.<br/>                                                                                                                                                                                                                                                                                                    |
| ClampOutput<br/> OUTPUT DEL \_ CLAMP COLORMATRIX \_ PROP \_ D2D1 \_<br/> | Indica se l'effetto stringe i valori di colore tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto stringe i valori prima che premultipli il valore alfa.<br/> Se si imposta questa proprietà su TRUE, l'effetto si anteterà ai valori. Se si imposta questa opzione su FALSE, l'effetto non stringerà i valori di colore, ma altri effetti e la superficie di output potrebbero stringere i valori se non hanno una precisione sufficiente.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/> |



 

## <a name="alpha-modes"></a>Modalità alfa



| Nome                                          | Descrizione                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ PREMULTIPLIED | L'effetto annulla la premoltipla dell'input, applica la matrice di colori e premoltipla l'output.<br/> |
| D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ STRAIGHT      | L'effetto applica la matrice di colori direttamente all'input e non premoltimultipamente l'output.<br/> |



 

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

 

