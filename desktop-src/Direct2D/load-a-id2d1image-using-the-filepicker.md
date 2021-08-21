---
title: Come caricare un'immagine in effetti Direct2D usando FilePicker
description: Viene illustrato come usare il Windows Archiviazione di selezione dati fileOpenPicker per caricare un'immagine in effetti Direct2D.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- FilePicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bb23faf2b9d50f12219f3b99c07ec835558addc55e67d4843dee049946a60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160532"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a>Come caricare un'immagine in effetti Direct2D usando FilePicker

Viene illustrato come usare [**Windows::Archiviazione::P ickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) per caricare un'immagine in [effetti Direct2D.](effects-overview.md) Se si vuole consentire all'utente di selezionare un file di immagine dall'archiviazione in un'app Windows Store, è consigliabile usare [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Direct2D](./direct2d-portal.md)
-   [Effetti Direct2D](effects-overview.md)
-   [**Windows::Archiviazione::P ickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a>Prerequisiti

-   È necessario un [**oggetto ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) per la creazione di effetti.
-   È necessario un [**oggetto IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) per la creazione di oggetti WIC.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-open-the-file-picker"></a>Passaggio 1: Aprire la selezione file

Creare un [**oggetto FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) e impostare *ViewMode*, *SuggestedStartLocation* e *FileTypeFilter* per la selezione delle immagini. Chiamare il [**metodo PickSingleFileAsync.**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync)


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



Al termine [**di PickSingleFileAsync,**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) si ottiene un flusso di file dall'interfaccia [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) restituita.

### <a name="step-2-get-a-file-stream"></a>Passaggio 2: Ottenere un flusso di file

Dichiarare un gestore di completamento da eseguire dopo la fine dell'operazione asincrona di selezione file. Usare il [**metodo GetResults**](/previous-versions//br205815(v=vs.85)) per recuperare il file e per ottenere l'oggetto flusso di file.


```C++
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file) // If file == nullptr, the user did not select a file.
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
```



Nel passaggio successivo si converte [**l'oggetto IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) in [**un IStream**](/windows/desktop/api/objidl/nn-objidl-istream) che è possibile passare a [WIC.](/windows/desktop/wic/-wic-api)

### <a name="step-3-convert-the-file-stream"></a>Passaggio 3: Convertire il flusso di file

Usare la [**funzione CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) per convertire il flusso di file. Windows Le API di runtime rappresentano flussi con [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), mentre [WIC](/windows/desktop/wic/-wic-api) utilizza [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).


```C++
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
        reinterpret_cast<IUnknown*>(fileStream),
        IID_PPV_ARGS(&istream)
        )
    );
```



> [!Note]  
> Per usare [**la funzione CreateStreamOverRandomAccessStream,**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) è necessario includere *shcore.h* nel progetto.

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a>Passaggio 4: Creare un decodificatore WIC e ottenere il frame

Creare un [**oggetto IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) usando il [**metodo IWICImagingFactory::CreateDecoderFromStream.**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)


```C++
    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );
```



Ottenere il primo fotogramma dell'immagine dal decodificatore usando il [**metodo IWICBitmapDecoder::GetFrame.**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a>Passaggio 5: Creare un convertitore WIC e inizializzare

Convertire l'immagine nel formato di colore BGRA usando [WIC.](/windows/desktop/wic/-wic-api) [IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) restituirà il formato pixel nativo dell'immagine, ad esempio gli JPEG vengono archiviati nel GUID \_ WICPixelFormat24bppBGR. Tuttavia, come ottimizzazione delle prestazioni con Direct2D è consigliabile eseguire la conversione in WICPixelFormat32bppPBGRA.

1.  Creare un [**oggetto IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) usando il [**metodo IWICImagingFactory::CreateFormatConverter.**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter)

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  Inizializzare il convertitore di formato per usare WICPixelFormat32bppPBGRA e passare il frame bitmap.

    ```C++
       DX::ThrowIfFailed(
            converter->Initialize(
                frame.Get(),
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                nullptr,
                0.0f,
                WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
                )
            );
    ```

    

[**L'interfaccia IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) deriva dall'interfaccia [**IWICBitmapSource,**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) quindi è possibile passare il convertitore all'effetto [di origine della bitmap.](bitmap-source.md)

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a>Passaggio 6: Creare un effetto e passare un oggetto IWICBitmapSource

Usare il metodo [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) per creare un oggetto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) [di origine bitmap](bitmap-source.md) usando il [contesto di dispositivo Direct2D.](getting-started-with-direct2d.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

Usare il [**metodo ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) per impostare la proprietà *D2D1 \_ BITMAPSOURCE \_ PROP \_ WIC BITMAP \_ \_ SOURCE* sul [**convertitore**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)di formato [WIC.](/windows/desktop/wic/-wic-api)

> [!Note]  
> [L'effetto origine](bitmap-source.md) bitmap non accetta un input dal [**metodo SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) come molti [effetti Direct2D.](effects-overview.md) [**L'oggetto IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) viene invece specificato come proprietà.

 


```C++
    ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
```



Ora che si ha l'effetto [di origine bitmap,](bitmap-source.md) è possibile usarlo come input per [**qualsiasi oggetto ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e creare un grafico degli effetti.

## <a name="complete-example"></a>Esempio completo

Di seguito è riportato il codice completo per questo esempio.


```C++
ComPtr<ID2D1Effect> bitmapSourceEffect;

void OpenFilePicker()
{
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
    
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file)
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
}

void OpenFile(Windows::Storage::Streams::IRandomAccessStream^ fileStream)
{
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
            reinterpret_cast<IUnknown*>(fileStream),
            IID_PPV_ARGS(&istream)
            )
        );

    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );

    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );

    ComPtr<IWICFormatConverter> converter;
    DX::ThrowIfFailed(
        m_wicFactory->CreateFormatConverter(&converter)
        );

    DX::ThrowIfFailed(
        converter->Initialize(
            frame.Get(),
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            nullptr,
            0.0f,
            WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
            )
        );

       ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
}
```



 

 