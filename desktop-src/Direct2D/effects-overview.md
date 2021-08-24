---
title: Effetti (Direct2D)
description: Panoramica degli effetti Direct2D.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0a88ff64721fc32955416dcfe108b1c9e87f7565a67fc2e1d8192a1eaf369d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317991"
---
# <a name="effects"></a>Effetti

## <a name="what-are-direct2d-effects"></a>Che cosa sono gli effetti Direct2D?

È possibile usare Direct2D per applicare uno o più effetti di alta qualità a un'immagine o a un set di immagini. Le API degli effetti sono create su [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) e sfruttano le funzionalità GPU per l'elaborazione delle immagini. È possibile concatenare gli effetti in un grafico degli effetti e comporre o unire l'output degli effetti.

Un effetto Direct2D esegue un'attività di creazione di immagini, ad esempio la modifica della luminosità, la deaturazione di un'immagine o la creazione di un'ombreggiatura. Gli effetti possono accettare zero o più immagini di input, esporre più proprietà che controllano il funzionamento e generare una singola immagine di output.

Ogni effetto crea un grafico di trasformazione interno costituito da singole trasformazioni. Ogni trasformazione rappresenta una singola operazione di immagine. Lo scopo principale di una trasformazione è ospitare gli shader eseguiti per ogni pixel di output. Questi shader possono includere pixel shader, vertex shader, la fase di fusione di una GPU e shader di calcolo.

Sia gli [effetti predefiniti Direct2D](./direct2d-portal.md) [](built-in-effects.md) che gli effetti personalizzati che è possibile creare usando l'API [degli effetti](custom-effects.md) personalizzati funzionano in questo modo.

Esistono una gamma di [effetti predefiniti di](built-in-effects.md) categorie come quelle qui. Per un [elenco completo,](built-in-effects.md) vedere la sezione Effetti predefiniti.

-   [Filtro](built-in-effects.md)
-   [Composizione e fusione](built-in-effects.md)
-   [Trasparenza](built-in-effects.md)
-   [Colore](built-in-effects.md)
-   [Illuminazione e stilizzazione](built-in-effects.md)
-   [Trasformazione e ridimensionamento](built-in-effects.md)
-   [recenti](built-in-effects.md)

È possibile applicare effetti a qualsiasi bitmap, tra cui: immagini caricate dal componente di imaging [Windows (WIC),](/windows/desktop/wic/-wic-api)primitive disegnate da [Direct2D,](./direct2d-portal.md)testo [da DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)o scene sottoposte a rendering [da Direct3D.](/windows/desktop/direct3d10/d3d10-graphics)

Con gli effetti Direct2D è possibile scrivere effetti personalizzati che è possibile usare per le applicazioni. Un framework di effetti personalizzato consente di usare funzionalità GPU come pixel shader, vertex shader e unità di fusione. È anche possibile includere altri effetti predefiniti o personalizzati nell'effetto personalizzato. Il framework per la compilazione di effetti personalizzati è lo stesso usato per creare gli effetti predefiniti di [Direct2D.](./direct2d-portal.md) [L'API direct2D effect author](custom-effects.md) fornisce un set di interfacce per creare e registrare gli effetti.

### <a name="more-effects-topics"></a>Altri argomenti sugli effetti

Il resto di questo argomento illustra le nozioni di base degli effetti Direct2D, ad esempio l'applicazione di un effetto a un'immagine. La tabella seguente contiene collegamenti ad argomenti aggiuntivi sugli effetti.

| Argomento                                                                                                                    | Descrizione                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Collegamento degli shader degli effetti](effect-shader-linking.md)<br/>                                                            | Direct2D usa un'ottimizzazione denominata collegamento effect shader che combina più passaggi di rendering del grafico degli effetti in un singolo passaggio.<br/>                                               |
| [Effetti personalizzati](custom-effects.md)<br/>                                                                          | Illustra come scrivere effetti personalizzati usando HLSL standard.<br/>                                                                                                                |
| [Come caricare un'immagine in Direct2D Effects usando FilePicker](load-a-id2d1image-using-the-filepicker.md)<br/> | Illustra come usare [**l'Windows::Archiviazione::P ickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) per caricare un'immagine in effetti Direct2D.<br/>                                      |
| [Come salvare il contenuto Direct2D in un file di immagine](save-direct2d-content-to-an-image-file.md)<br/>                   | Questo argomento illustra come usare [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) per salvare il contenuto sotto forma di [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in un file di immagine codificato, ad esempio JPEG.<br/> |
| [Come applicare effetti alle primitive](how-to-apply-effects-to-primitives.md)<br/>                                  | Questo argomento illustra come applicare una serie di effetti a [Direct2D](./direct2d-portal.md) [e DirectWrite](direct2d-and-directwrite.md) primitive.<br/>                           |
| [Controllo della precisione e del ritaglio numerico nei grafici degli effetti](precision-and-clipping-in-effect-graphs.md)<br/>  | Le applicazioni che eseguono il rendering degli effetti con Direct2D devono garantire il livello desiderato di qualità e prevedibilità rispetto alla precisione numerica. <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>Applicazione di un effetto a un'immagine

È possibile usare l'API effetti Direct2D per applicare trasformazioni alle immagini.

> [!Note]  
> Questo esempio presuppone che siano già stati creati [**oggetti ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e [IWICBitmapSource.](/windows/desktop/wic/-wic-imp-iwicbitmapsource) Per altre informazioni sulla creazione di questi oggetti, vedere [How to load an image into Direct2D effects using the FilePicker](load-a-id2d1image-using-the-filepicker.md) and Devices and Device [Contexts](devices-and-device-contexts.md).

 

1.  Dichiarare una [**variabile ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e quindi creare un effetto di origine [bitmap](bitmap-source.md) usando il [**metodo ID2DDeviceContext::CreateEffect.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  Impostare la proprietà BitmapSource sull'origine bitmap WIC usando [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  Dichiarare una [**variabile ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e quindi creare l'effetto [sfocatura gaussiana.](gaussian-blur.md)

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  Impostare l'input per ricevere l'immagine dall'effetto di origine bitmap. Impostare la quantità di sfocatura [**con il metodo SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) e la proprietà deviazione standard.

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  Usare il contesto di dispositivo per disegnare l'output dell'immagine risultante.

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    Il [**metodo DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) deve essere chiamato tra le chiamate [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) ed [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) come altre operazioni di rendering Direct2D. **DrawImage** può prendere un'immagine o l'output di un effetto ed eseguirne il rendering sulla superficie di destinazione.

## <a name="spatial-transforms"></a>Trasformazioni spaziali

Direct2D offre effetti predefiniti in grado di trasformare le immagini nello spazio 2D e 3D, nonché di ridimensionamento. Gli effetti di scala e trasformazione offrono vari livelli di qualità, ad esempio: vicino più vicino, lineare, cubico, lineare multi-campione, anisotropo e cubico di alta qualità.

> [!Note]  
> La modalità anisotrop genera mipmap durante il ridimensionamento, tuttavia, se si imposta la proprietà **Cached** su true sugli effetti input per la trasformazione, le mipmap non verranno generate ogni volta per immagini sufficientemente piccole.

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



Questo uso dell'effetto di trasformazione affine 2D ruota leggermente la bitmap in senso antiorario.



| Prima                                                            |
|-------------------------------------------------------------------|
| ![Effetto affine 2d prima dell'immagine.](images/default-before.jpg)      |
| After                                                             |
| ![Effetto affine 2d dopo l'immagine.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>Composizione di immagini

Alcuni effetti accettano più input e li compositi in un'unica immagine risultante.

Gli effetti compositi e aritmetici predefiniti forniscono diverse modalità. Per altre informazioni, vedere [l'argomento composito.](composite.md) [L'effetto](blend.md) di fusione ha un'ampia gamma di modalità di accelerazione GPU disponibili.


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



L'effetto composito combina le immagini in diversi modi in base alla modalità specificata.

## <a name="pixel-adjustments"></a>Regolazioni dei pixel

Esistono alcuni effetti Direct2D predefiniti che consentono di modificare i dati pixel. Ad esempio, l'effetto matrice di colori può essere usato per modificare il colore di un'immagine.


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



Questo codice accetta l'immagine e modifica il colore come illustrato nelle immagini di esempio qui.



| Prima                                                          |
|-----------------------------------------------------------------|
| ![effetto matrice di colori prima dell'immagine.](images/default-before.jpg) |
| After                                                           |
| ![effetto matrice di colori dopo l'immagine.](images/15-colormatrix.png)  |



 

Per altre [informazioni,](how-to-create-a-solid-color-brush.md) vedere la sezione relativa agli effetti predefiniti a colori.

## <a name="building-effect-graphs"></a>Creazione di grafici degli effetti

È possibile concatenare gli effetti per trasformare le immagini. Ad esempio, il codice qui applica un'ombreggiatura e una trasformazione 2D, quindi compositi i risultati.


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Risultato:

![output dell'effetto ombreggiatura.](images/effect-overview-shadow.png)

Gli effetti [**accettano oggetti ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) come input. È possibile usare [**id2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) perché l'interfaccia è derivata da **ID2D1Image**. È anche possibile usare [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) per ottenere l'output di un oggetto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) come **ID2D1Image** o usare il **metodo SetInputEffect,** che converte automaticamente l'output. Nella maggior parte dei casi un grafo degli effetti è costituito da oggetti **ID2D1Effect** concatenati direttamente tra loro, semplificando l'applicazione di più effetti a un'immagine per creare oggetti visivi accattivanti.

Per [altre informazioni, vedere](how-to-apply-effects-to-primitives.md) Come applicare gli effetti alle primitive.

## <a name="related-topics"></a>Argomenti correlati

[Esempio di effetti immagine di base Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[Effetti predefiniti](built-in-effects.md)