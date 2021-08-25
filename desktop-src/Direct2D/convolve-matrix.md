---
title: Effetto con matrice di convoluzione
description: Usare l'effetto matrice convolva per applicare un kernel 2D arbitrario a un'immagine. È possibile usare questo effetto per sfocare, rilevare bordi, rilievi o affilare un'immagine.
ms.assetid: D9C23AC4-0090-4F16-AC59-B952FB616FA9
keywords:
- Effetto matrice convolva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3b988e0bd48fece4d767fad29b63fe021c82d49d07dae5ab3f1b10b3f9794f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833376"
---
# <a name="convolve-matrix-effect"></a>Effetto con matrice di convoluzione

Usare l'effetto matrice convolva per applicare un kernel 2D arbitrario a un'immagine. È possibile usare questo effetto per sfocare, rilevare bordi, rilievi o affilare un'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1ConvolveMatrix.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità di scalabilità](#scale-modes)
-   [Modalità bordo](#border-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'esempio seguente mostra l'input e l'output dell'effetto matrice convolva con un kernel 3 x 3.



| Prima                                                         |
|----------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)     |
| After                                                          |
| ![l'immagine dopo la trasformazione.](images/6-convolvematrix.png) |



 


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



## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KernelUnitLength<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/> | Dimensioni di un'unità nel kernel. Le unità sono in (DIP/unità kernel), dove un'unità kernel è la dimensione dell'elemento nel kernel di convoluzione. Il valore 1 (unità DIP/kernel) corrisponde a un pixel in un'immagine con 96 DPI.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                   |
| Scalemode<br/> MODALITÀ DI SCALA DELLE PROPRIETÀ \_ CONVOLVEMATRIX D2D1 \_ \_ \_<br/>                 | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine in base alla lunghezza dell'unità del kernel corrispondente. Esistono sei modalità di scalabilità che variano in qualità e velocità.<br/> Il tipo è D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE.<br/> Il valore predefinito è D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                                                                                                     |
| KernelSizeX<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ SIZE \_ X<br/>           | Larghezza della matrice del kernel. Le unità sono specificate in unità kernel. Il tipo è UINT32.<br/> Il valore predefinito è 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| KernelSizeY<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ SIZE \_ Y<br/>           | Altezza della matrice del kernel. Le unità sono specificate in unità kernel. Il tipo è UINT32.<br/> Il valore predefinito è 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| KernelMatrix<br/> MATRICE DEL \_ KERNEL CONVOLVEMATRIX \_ PROP \_ D2D1 \_<br/>           | Matrice del kernel da applicare all'immagine. Gli elementi del kernel non sono delimitati e vengono specificati come float.<br/> Il primo set *di numeri KernelSizeX* in FLOAT \[ \] corrisponde alla prima riga nel kernel. Il secondo set di *numeri KernelSizeX* corrisponde alla seconda riga e così via fino a *kernelSizeY* righe.<br/> Il tipo è \[ \] FLOAT.<br/> Il valore predefinito è {0.0f, 0.0f, 0.0f, 0.0f, 1.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f}.<br/>                                                       |
| Divisor<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ DIVISOR<br/>                       | La matrice del kernel viene applicata a un pixel e quindi il risultato viene diviso per questo valore. <br/> 0 si comporta come un valore float epsilon.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                                                                                                           |
| Bias<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ BIAS<br/>                             | L'effetto applica la matrice del kernel, il divisore e quindi la distorsione viene aggiunta al risultato. La distorsione è illimitata e senza unità. Il tipo è FLOAT.<br/> Il valore predefinito è 0,0f.<br/>                                                                                                                                                                                                                                                                                                                              |
| KernelOffset<br/> OFFSET DEL \_ KERNEL CONVOLVEMATRIX \_ PROP \_ D2D1 \_<br/>           | Sposta il kernel di convoluzione da una posizione centrata sul pixel di output a una posizione specificata a sinistra/destra e verso l'alto o verso il basso. L'offset è definito in unità del kernel.<br/> Con alcuni offset e dimensioni del kernel, gli esempi del kernel di convoluzione non atterrano su un centro immagine pixel. I valori in pixel per l'esempio del kernel vengono calcolati tramite interpolazione bilineare.<br/> Il tipo è D2D1 \_ VECTOR \_ 2F.<br/> Il valore predefinito è {0.0f, 0.0f}.<br/>                                                          |
| PreserveAlpha<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ PRESERVE \_ ALPHA<br/>         | Specifica se il kernel di convoluzione viene applicato al canale alfa o solo ai canali di colore.<br/> Se si imposta questa opzione su **TRUE,** il kernel di convoluzione viene applicato solo ai canali di colore.<br/> Se si imposta questa opzione su **FALSE,** il kernel di convoluzione viene applicato a tutti i canali.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/>                                                                                                                                               |
| BorderMode<br/> MODALITÀ BORDO \_ CONVOLVEMATRIX \_ \_ PROP \_ D2D1<br/>               | Modalità usata per calcolare il bordo dell'immagine, soft o hard. Per [altre informazioni, vedere](https://www.bing.com/search?q=Border+modes) Modalità bordo.<br/> Il tipo è D2D1 \_ BORDER \_ MODE.<br/> Il valore predefinito è D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                                                                                                                                                                                                                     |
| ClampOutput<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ CLAMP \_ OUTPUT<br/>             | Indica se l'effetto stringe i valori di colore tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto stringe i valori prima che premultipli il valore alfa .<br/> Se si imposta questa proprietà su TRUE, l'effetto si anteterà ai valori. Se si imposta questa opzione su FALSE, l'effetto non stringerà i valori di colore, ma altri effetti e la superficie di output potrebbero stringere i valori se non hanno una precisione sufficiente.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/> |



 

## <a name="scale-modes"></a>Modalità di scalabilità



| Enumerazione                                              | Descrizione                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Campioni il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ LINEAR                | Usa un campione di quattro punti e l'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore rispetto alla modalità adiacente più vicina.                                                                              |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ CUBIC                 | Usa un kernel cubico di 16 campioni per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing dei bordi valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.                                              |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE MODE \_ \_ ANISO STANDBY           | Usa il filtro anisotropo per campionare un criterio in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cubico di qualità elevata di dimensioni variabili per eseguire una scalabilità pre-ridimensionata dell'immagine se la scalabilità è coinvolta nella matrice di trasformazione. Usa quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ LINEAR.

 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODALITÀ BORDO D2D1 \_ \_ \_ SOFT | L'effetto riempire l'immagine di input con pixel neri trasparenti per i campioni al di fuori dei limiti di input quando applica il kernel di convoluzione. In questo modo viene creato un bordo soft per l'immagine e nel processo la bitmap di output viene espansa in base alle dimensioni del kernel.<br/> |
| MODALITÀ BORDO D2D1 \_ \_ \_ HARD | L'effetto estende l'immagine di input con una trasformazione del bordo di tipo speculare per i campioni esterni ai limiti di input. La dimensione della bitmap di output è uguale alla dimensione della bitmap di input.<br/>                                                                       |



 

## <a name="output-bitmap"></a>Bitmap di output

La dimensione dell'output dell'effetto dipende dalle dimensioni del kernel di convoluzione, dall'offset del kernel, dalla lunghezza dell'unità del kernel e dall'impostazione della modalità bordo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

