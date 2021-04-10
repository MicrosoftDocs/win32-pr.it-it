---
title: Effetti (Direct2D)
description: Panoramica degli effetti Direct2D.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047111"
---
# <a name="effects"></a>Effetti

## <a name="what-are-direct2d-effects"></a>Che cosa sono gli effetti Direct2D?

È possibile utilizzare Direct2D per applicare uno o più effetti di alta qualità a un'immagine o a un set di immagini. Le API degli effetti sono basate su [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) e sfruttano le funzionalità GPU per l'elaborazione delle immagini. È possibile concatenare gli effetti in un grafico effetto e comporre o fondere l'output degli effetti.

Un effetto Direct2D esegue un'attività di creazione di immagini, ad esempio la modifica della luminosità, la desaturazione di un'immagine o la creazione di un'ombreggiatura. Gli effetti possono accettare zero o più immagini di input, esporre più proprietà che controllano l'operazione e generare un'unica immagine di output.

Ogni effetto crea un grafo di trasformazione interno costituito da trasformazioni singole. Ogni trasformazione rappresenta una singola operazione di immagine. Lo scopo principale di una trasformazione è quello di ospitare gli shader eseguiti per ogni pixel di output. Questi shader possono includere pixel shader, vertex shader, la fase Blend di una GPU e compute shader.

Gli effetti [](./direct2d-portal.md) [predefiniti](built-in-effects.md) di Direct2D e gli effetti personalizzati che è possibile apportare usando l' [API degli effetti personalizzati](custom-effects.md) funzionano in questo modo.

Sono disponibili diversi [effetti predefiniti](built-in-effects.md) da categorie come quelle riportate di seguito. Per un elenco completo, vedere la sezione [effetti predefiniti](built-in-effects.md) .

-   [Filtro](built-in-effects.md)
-   [Composizione e fusione](built-in-effects.md)
-   [Trasparenza](built-in-effects.md)
-   [Colore](built-in-effects.md)
-   [Illuminazione e stilizzazione](built-in-effects.md)
-   [Trasformazione e scalabilità](built-in-effects.md)
-   [recenti](built-in-effects.md)

È possibile applicare effetti a qualsiasi bitmap, incluse le immagini caricate da [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitive disegnate da [Direct2D](./direct2d-portal.md), testo da [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)o scene sottoposte a rendering da [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).

Con gli effetti Direct2D è possibile scrivere gli effetti che è possibile usare per le applicazioni. Un Framework di effetto personalizzato consente di usare le funzionalità GPU come pixel shader, vertex shader e l'unità di fusione. È anche possibile includere altri effetti predefiniti o personalizzati nell'effetto personalizzato. Il Framework per la creazione di effetti personalizzati è identico a quello usato per creare gli effetti predefiniti di [Direct2D](./direct2d-portal.md). L' [API autore dell'effetto Direct2D](custom-effects.md) fornisce un set di interfacce per la creazione e la registrazione di effetti.

### <a name="more-effects-topics"></a>Argomenti per altri effetti

Nella parte restante di questo argomento vengono illustrate le nozioni di base degli effetti Direct2D, ad esempio l'applicazione di un effetto a un'immagine. La tabella contiene collegamenti ad argomenti aggiuntivi sugli effetti.

| Argomento                                                                                                                    | Descrizione                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Collegamento Effect shader](effect-shader-linking.md)<br/>                                                            | Direct2D usa un'ottimizzazione denominata Effect shader linking che combina il rendering del grafico a più effetti passa in un singolo passaggio.<br/>                                               |
| [Effetti personalizzati](custom-effects.md)<br/>                                                                          | Viene illustrato come scrivere effetti personalizzati usando HLSL standard.<br/>                                                                                                                |
| [Come caricare un'immagine in effetti Direct2D usando il Filepicker](load-a-id2d1image-using-the-filepicker.md)<br/> | Mostra come usare [**Windows:: Storage::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) per caricare un'immagine in effetti Direct2D.<br/>                                      |
| [Come salvare il contenuto Direct2D in un file di immagine](save-direct2d-content-to-an-image-file.md)<br/>                   | Questo argomento illustra come usare [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) per salvare il contenuto sotto forma di [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in un file di immagine codificato, ad esempio JPEG.<br/> |
| [Come applicare effetti alle primitive](how-to-apply-effects-to-primitives.md)<br/>                                  | In questo argomento viene illustrato come applicare una serie di effetti alle primitive [Direct2D](./direct2d-portal.md) e [DirectWrite](direct2d-and-directwrite.md) .<br/>                           |
| [Controllo della precisione e ritaglio numerico nei grafici effettivi](precision-and-clipping-in-effect-graphs.md)<br/>  | Le applicazioni che eseguono il rendering degli effetti utilizzando Direct2D devono prestare attenzione a raggiungere il livello di qualità e prevedibilità desiderato rispetto alla precisione numerica. <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>Applicazione di un effetto a un'immagine

È possibile usare l'API di effetti Direct2D per applicare le trasformazioni alle immagini.

> [!Note]  
> In questo esempio si presuppone che siano già stati creati gli oggetti [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) . Per ulteriori informazioni sulla creazione di questi oggetti [, vedere come caricare un'immagine in effetti Direct2D utilizzando il FilePicker e i](load-a-id2d1image-using-the-filepicker.md) [dispositivi e i contesti di dispositivo](devices-and-device-contexts.md).

 

1.  Dichiarare una variabile [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e quindi creare un effetto di [origine bitmap](bitmap-source.md) usando il metodo [**ID2DDeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  Impostare la proprietà BitmapSource sull'origine bitmap WIC utilizzando [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  Dichiarare una variabile [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , quindi creare l'effetto di [sfocatura gaussiana](gaussian-blur.md) .

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  Impostare l'input per la ricezione dell'immagine dall'effetto origine bitmap. Impostare la quantità di sfocatura per il metodo [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) e la proprietà della deviazione standard.

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  Usare il contesto di dispositivo per tracciare l'output dell'immagine risultante.

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    Il metodo [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) deve essere chiamato tra le chiamate a [**ID2DDeviceContext:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) come ad altre operazioni di rendering Direct2D. **DrawImage** può utilizzare un'immagine o l'output di un effetto ed eseguirne il rendering nell'area di destinazione.

## <a name="spatial-transforms"></a>Trasformazioni spaziali

Direct2D fornisce effetti predefiniti che consentono di trasformare immagini nello spazio 2D e 3D, nonché di ridimensionare. Gli effetti di ridimensionamento e trasformazione offrono diversi livelli di qualità, ad esempio: Neighbor più vicino, lineare, cubico, lineare multiplo, anisotropico e cubi di alta qualità.

> [!Note]  
> La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che sono input della trasformazione, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.

 


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



Questo utilizzo dell'effetto di trasformazione affine 2D ruota leggermente la bitmap in senso antiorario.



| Prima                                                            |
|-------------------------------------------------------------------|
| ![effetto affine 2D prima dell'immagine.](images/default-before.jpg)      |
| After                                                             |
| ![effetto affine 2D dopo l'immagine.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>Composizione di immagini

Alcuni effetti accettano più input e li compostano in un'immagine risultante.

Gli effetti compositi incorporati e aritmetici composte forniscono varie modalità. per altre informazioni, vedere l'argomento [composito](composite.md) . Per l'effetto [Blend](blend.md) sono disponibili diverse modalità con accelerazione GPU.


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



L'effetto composito combina le immagini in modi diversi in base alla modalità specificata.

## <a name="pixel-adjustments"></a>Regolazioni pixel

Sono disponibili alcuni effetti Direct2D predefiniti che consentono di modificare i dati in pixel. È ad esempio possibile utilizzare l'effetto matrice colori per modificare il colore di un'immagine.


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



Questo codice acquisisce l'immagine e modifica il colore come illustrato nelle immagini di esempio.



| Prima                                                          |
|-----------------------------------------------------------------|
| ![effetto della matrice di colori prima dell'immagine.](images/default-before.jpg) |
| After                                                           |
| ![effetto matrice colore dopo l'immagine.](images/15-colormatrix.png)  |



 

Per altre informazioni, vedere la sezione [effetti sul colore predefinito](how-to-create-a-solid-color-brush.md) .

## <a name="building-effect-graphs"></a>Creazione di grafici degli effetti

È possibile concatenare gli effetti per trasformare le immagini. Ad esempio, il codice qui applica un'ombreggiatura e una trasformazione 2D, quindi compone i risultati insieme.


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

![output effetto ombreggiatura.](images/effect-overview-shadow.png)

Gli effetti accettano gli oggetti [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) come input. È possibile usare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) perché l'interfaccia è derivata da **ID2D1Image**. È anche possibile usare [**ID2D1Effect:: GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) per ottenere l'output di un oggetto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) come **ID2D1Image** o usare il metodo **SetInputEffect** , che converte l'output. Nella maggior parte dei casi un grafico effetto è costituito da oggetti **ID2D1Effect** direttamente concatenati, che semplifica l'applicazione di più effetti a un'immagine per la creazione di oggetti visivi accattivanti.

Per altre informazioni [, vedere come applicare effetti alle primitive](how-to-apply-effects-to-primitives.md) .

## <a name="related-topics"></a>Argomenti correlati

[Esempio di effetti immagine di base Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[Effetti predefiniti](built-in-effects.md)