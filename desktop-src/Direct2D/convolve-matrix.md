---
title: Effetto con matrice di convoluzione
description: Usare l'effetto matrice condensa per applicare un kernel 2D arbitrario a un'immagine. È possibile utilizzare questo effetto per sfocare, rilevare i bordi, goffrare o affinare un'immagine.
ms.assetid: D9C23AC4-0090-4F16-AC59-B952FB616FA9
keywords:
- effetto matrice condensa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27951f5b9145dc46188e6b3112892d1a61856236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104550512"
---
# <a name="convolve-matrix-effect"></a>Effetto con matrice di convoluzione

Usare l'effetto matrice condensa per applicare un kernel 2D arbitrario a un'immagine. È possibile utilizzare questo effetto per sfocare, rilevare i bordi, goffrare o affinare un'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1ConvolveMatrix.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità di ridimensionamento](#scale-modes)
-   [Modalità bordo](#border-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Nell'esempio riportato di seguito viene illustrato l'input e l'output dell'effetto matrice condensa con un kernel 3 x 3.



| Prima                                                         |
|----------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)     |
| After                                                          |
| ![immagine dopo la trasformazione.](images/6-convolvematrix.png) |



 


```C++
ComPtr<ID2D1Effect> convolveMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ConvolveMatrix, &convolveMatrixEffect);

convolveMatrixEffect->SetInput(0, bitmap);
float matrix[9] = {-1, -1, -1, -1, 9, -1, -1, -1, -1};
convolveMatrixEffect->SetValue(D2D1_CONVOLVEMATRIX_PROP_KERNEL_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(convolveMatrixEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KernelUnitLength<br/> \_ \_ \_ \_ Lunghezza unità kernel d2d1 CONVOLVEMATRIX \_<br/> | Dimensioni di un'unità nel kernel. Le unità si trovano in (DIP/unità kernel), in cui un'unità kernel corrisponde alla dimensione dell'elemento nel kernel di convoluzione. Il valore 1 (unità DIP/kernel) corrisponde a un pixel in un'immagine a 96 DPI.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                   |
| ScaleMode<br/> D2D1 \_ CONVOLVEMATRIX \_ - \_ modalità scala della Prop \_<br/>                 | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine alla lunghezza dell'unità kernel corrispondente. Sono disponibili sei modalità di ridimensionamento che variano in qualità e velocità.<br/> Il tipo è D2D1 \_ CONVOLVEMATRIX \_ scale \_ mode.<br/> Il valore predefinito è D2D1 \_ CONVOLVEMATRIX \_ scale \_ mode \_ Linear.<br/>                                                                                                                                                                                                                     |
| KernelSizeX<br/> \_ \_ Dimensioni kernel d2d1 CONVOLVEMATRIX Prop \_ \_ \_ X<br/>           | Larghezza della matrice di kernel. Le unità vengono specificate in unità kernel. Il tipo è UINT32.<br/> Il valore predefinito è 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| KernelSizeY<br/> \_Dimensioni del kernel d2d1 CONVOLVEMATRIX \_ prop \_ \_ \_ Y<br/>           | Altezza della matrice di kernel. Le unità vengono specificate in unità kernel. Il tipo è UINT32.<br/> Il valore predefinito è 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| KernelMatrix<br/> \_ \_ \_ Matrice kernel d2d1 CONVOLVEMATRIX \_ prop<br/>           | Matrice di kernel da applicare all'immagine. Gli elementi del kernel non sono limitati e vengono specificati come float.<br/> Il primo set di numeri *KernelSizeX* nel float \[ \] corrisponde alla prima riga nel kernel. Il secondo set di numeri *KernelSizeX* corrisponde alla seconda riga e così via fino a *KernelSizeY* righe.<br/> Il tipo è FLOAT \[ \] .<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f, 0,0 f, 1.0 f, 0,0 f, 0,0 f, 0,0 f, 0,0 f}.<br/>                                                       |
| Divisor<br/> \_ \_ Divisore prop CONVOLVEMATRIX d2d1 \_<br/>                       | La matrice del kernel viene applicata a un pixel e quindi il risultato viene diviso per questo valore. <br/> 0 si comporta come valore di float Epsilon.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                           |
| Bias<br/> \_ \_ Distorsione della prop CONVOLVEMATRIX d2d1 \_<br/>                             | L'effetto applica la matrice del kernel, il divisore, quindi la distorsione viene aggiunta al risultato. La distorsione è senza limiti e senza unità. Il tipo è FLOAT.<br/> Il valore predefinito è 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                              |
| KernelOffset<br/> \_ \_ \_ Offset kernel d2d1 CONVOLVEMATRIX \_ prop<br/>           | Sposta il kernel di convoluzione da una posizione centrata sul pixel di output a una posizione specificata a sinistra/a destra e a discesa. L'offset è definito in unità kernel.<br/> Con alcuni offset e dimensioni del kernel, gli esempi del kernel di convoluzione non verranno stabiliti in un centro immagini pixel. I valori pixel per l'esempio di kernel vengono calcolati in base all'interpolazione bilineare.<br/> Il tipo è D2D1 \_ vector \_ 2F.<br/> Il valore predefinito è {0,0 f, 0,0 f}.<br/>                                                          |
| PreserveAlpha<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_ Preserve \_ Alpha<br/>         | Specifica se il kernel di convoluzione viene applicato al canale alfa o solo ai canali dei colori.<br/> Se si imposta questa proprietà su **true** , il kernel di convoluzione viene applicato solo ai canali dei colori.<br/> Se si imposta questo valore su **false** , il kernel di convoluzione viene applicato a tutti i canali.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/>                                                                                                                                               |
| BorderMode<br/> \_ \_ \_ Modalità bordo prop CONVOLVEMATRIX \_ d2d1<br/>               | Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard. Per altre informazioni, vedere [Border modes](https://www.bing.com/search?q=Border+modes) .<br/> Il tipo è D2D1 \_ Border \_ mode.<br/> Il valore predefinito è D2D1 \_ Border \_ mode \_ .<br/>                                                                                                                                                                                                                                                                                     |
| ClampOutput<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_ \_ output Clamp<br/>             | Indica se l'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto blocca i valori prima di premoltiplicare l'alfa.<br/> Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto. Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/> |



 

## <a name="scale-modes"></a>Modalità di ridimensionamento



| Enumerazione                                              | Descrizione                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ CONVOLVEMATRIX \_ - \_ modalità scala \_ più \_ vicina     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ CONVOLVEMATRIX \_ - \_ modalità scala \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore rispetto alla modalità adiacente più vicina.                                                                              |
| D2D1 \_ CONVOLVEMATRIX- \_ modalità di ridimensionamento \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ CONVOLVEMATRIX- \_ modalità di scalabilità \_ \_ \_ multicampione \_ lineare | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.                                              |
| D2D1 \_ \_ modalità di ridimensionamento CONVOLVEMATRIX \_ \_           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ CONVOLVEMATRIX \_ - \_ modalità scala di \_ alta \_ qualità \_ cubica  | Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione. USA quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ CONVOLVEMATRIX \_ scale \_ mode \_ Linear.

 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modalità bordo \_ d2d1 \_ Soft | L'effetto riempie l'immagine di input con i pixel neri trasparenti per i campioni all'esterno dei limiti di input quando applica il kernel di convoluzione. Viene creato un bordo flessibile per l'immagine e il processo espande la bitmap di output in base alla dimensione del kernel.<br/> |
| \_Modalità bordo \_ d2d1 \_ | L'effetto estende l'immagine di input con una trasformazione del bordo di tipo mirror per i campioni all'esterno dei limiti di input. La dimensione della bitmap di output è uguale alla dimensione della bitmap di input.<br/>                                                                       |



 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni dell'output dell'effetto dipendono dalle dimensioni del kernel di convoluzione, dall'offset del kernel, dalla lunghezza dell'unità del kernel e dall'impostazione della modalità bordo.

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

 

