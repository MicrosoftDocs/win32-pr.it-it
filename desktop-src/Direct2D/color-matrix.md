---
title: Effetto matrice colori
description: Utilizzare l'effetto matrice colori per modificare i valori RGBA di una bitmap.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- effetto matrice colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048240"
---
# <a name="color-matrix-effect"></a>Effetto matrice colori

Utilizzare l'effetto matrice colori per modificare i valori RGBA di una bitmap.

È possibile utilizzare questo effetto per:

-   Rimuovere un canale di colore da un'immagine.
-   Ridurre il colore in un'immagine.
-   Scambia canali colori.
-   Combinare i canali colori.

Molti effetti predefiniti sono specializzazioni della matrice di colori ottimizzate per l'uso previsto degli effetti. Gli esempi includono [saturazione](saturation.md), [Rotazione tonalità](hue-rotate.md), [seppia](sepia-effect.md), [temperatura e tonalità](temperature-and-tint-effect.md).

Il CLSID per questo effetto è CLSID \_ D2D1ColorMatrix.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità Alpha](#alpha-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Nell'esempio riportato di seguito vengono illustrate le immagini di input e di output dell'effetto della matrice di colori che scambia i canali rosso e blu.



| Prima                                                       |
|--------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)   |
| After                                                        |
| ![immagine dopo la trasformazione.](images/15-colormatrix.png) |



 


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



Questo effetto moltiplica i valori RGBA dell'immagine in base a un 5x4, la matrice principale della colonna, come illustrato in questa equazione.

![definizione di matrice di esempio.](images/color-matrix-formula.png)

Questo effetto funziona su immagini alfa diritte e premoltiplicate.

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ColorMatrix<br/> \_Matrice di \_ colori della prop d2d1 COLORMATRIX \_ \_<br/> | Matrice 5x4 di valori float. Gli elementi nella matrice non sono limitati e sono senza unità.<br/> Il valore predefinito è la matrice di identità.<br/> Il tipo è D2D1 \_ Matrix \_ 5x4 \_ F.<br/> Il valore predefinito è Matrix5x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0). <br/>                                                                                                                                                                                                                        |
| AlphaMode<br/> D2D1 \_ la \_ \_ modalità Alpha della Prop \_<br/>     | Modalità Alpha dell'output. Per altre informazioni, vedere [modalità Alpha](#alpha-modes) . <br/> Il tipo è D2D1 \_ COLORMATRIX \_ Alpha \_ mode.<br/> Il valore predefinito è D2D1 \_ COLORMATRIX \_ Alpha \_ mode \_ premoltiplicato.<br/>                                                                                                                                                                                                                                                                                                    |
| ClampOutput<br/> \_Output d2d1 COLORMATRIX \_ prop \_ Clamp \_<br/> | Indica se l'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto blocca i valori prima di premoltiplicare l'alfa.<br/> Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto. Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/> |



 

## <a name="alpha-modes"></a>Modalità Alpha



| Nome                                          | Descrizione                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D2D1 \_ COLORMATRIX \_ \_ modalità alfa \_ premoltiplicata | L'effetto Annulla la premoltiplicazione dell'input, applica la matrice di colori e premoltiplica l'output.<br/> |
| D2D1 \_ \_ modalità Alpha \_ COLORMATRIX \_ lineare      | L'effetto applica la matrice di colori direttamente all'input e non premoltiplica l'output.<br/> |



 

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

 

