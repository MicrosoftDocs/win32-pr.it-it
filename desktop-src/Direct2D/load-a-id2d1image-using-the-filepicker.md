---
title: Come caricare un'immagine in effetti Direct2D usando il Filepicker
description: Mostra come usare i selezionatori di archiviazione di Windows FileOpenPicker per caricare un'immagine in effetti Direct2D.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- Selezione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4346cc0e337374fa41313cb77debf4faca781669
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299994"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a>Come caricare un'immagine in effetti Direct2D usando il Filepicker

Mostra come usare [**Windows:: Storage::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) per caricare un'immagine in [effetti Direct2D](effects-overview.md). Se si vuole consentire all'utente di selezionare un file di immagine dalla risorsa di archiviazione in un'app di Windows Store, è consigliabile usare [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Direct2D](./direct2d-portal.md)
-   [Effetti Direct2D](effects-overview.md)
-   [**Windows:: Storage::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a>Prerequisiti

-   È necessario un oggetto [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) per la creazione di effetti.
-   Per la creazione di oggetti WIC è necessario un oggetto [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) .

## <a name="instructions"></a>Istruzioni

### <a name="step-1-open-the-file-picker"></a>Passaggio 1: aprire il selettore file

Creare un oggetto [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) e impostare *ViewMode*, *SuggestedStartLocation* e *fileTypeFilter* per la selezione di immagini. Chiamare il metodo [**pickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) .


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



Al termine del [**pickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) , si ottiene un flusso di file dall'interfaccia [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) che restituisce.

### <a name="step-2-get-a-file-stream"></a>Passaggio 2: ottenere un flusso di file

Dichiarare un gestore di completamento da eseguire dopo la restituzione dell'operazione asincrona di selezione file. Usare il metodo [**GetResults**](/previous-versions//br205815(v=vs.85)) per recuperare il file e ottenere l'oggetto del flusso di file.


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



Nel passaggio successivo si convertirà l'oggetto [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) in un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) che è possibile passare a [WIC](/windows/desktop/wic/-wic-api).

### <a name="step-3-convert-the-file-stream"></a>Passaggio 3: convertire il flusso di file

Utilizzare la funzione [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) per convertire il flusso di file. Windows Runtime API rappresentano i flussi con [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), mentre [WIC](/windows/desktop/wic/-wic-api) utilizza [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).


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
> Per usare la funzione [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , è necessario includere *shcore. h* nel progetto.

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a>Passaggio 4: creare un decodificatore WIC e ottenere il frame

Creare un oggetto [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) usando il metodo [**IWICImagingFactory:: CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .


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



Ottenere il primo frame dell'immagine dal decodificatore usando il metodo [**IWICBitmapDecoder:: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a>Passaggio 5: creare un convertitore WIC e inizializzare

Convertire l'immagine nel formato di colore BGRA utilizzando [WIC](/windows/desktop/wic/-wic-api). [IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) restituirà il formato pixel nativo dell'immagine, ad esempio i file JPEG vengono archiviati nel GUID \_ WICPixelFormat24bppBGR. Tuttavia, come ottimizzazione delle prestazioni con Direct2D si consiglia di eseguire la conversione in WICPixelFormat32bppPBGRA.

1.  Creare un oggetto [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) usando il metodo [**IWICImagingFactory:: CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .

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

    

L'interfaccia [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) è derivata dall'interfaccia [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) , quindi è possibile passare il convertitore all'effetto [origine bitmap](bitmap-source.md) .

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a>Passaggio 6: creare un effetto e passare un IWICBitmapSource

Usare il metodo [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) per creare un oggetto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) di [origine bitmap](bitmap-source.md) usando il [**contesto di periferica**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](getting-started-with-direct2d.md) .

Usare il metodo [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) per impostare la proprietà di *origine della bitmap di d2d1 \_ BITMAPSOURCE \_ prop \_ WIC \_ \_* sul [**convertitore di formato**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) [WIC](/windows/desktop/wic/-wic-api) .

> [!Note]  
> L'effetto [origine bitmap](bitmap-source.md) non accetta un input dal metodo [**seinput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) come molti [effetti Direct2D](effects-overview.md). L'oggetto [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) viene invece specificato come proprietà.

 


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



Ora che si dispone dell'effetto [origine bitmap](bitmap-source.md) , è possibile usarlo come input per qualsiasi [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e creare un grafico effetto.

## <a name="complete-example"></a>Esempio completo

Ecco il codice completo per questo esempio.


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



 

 