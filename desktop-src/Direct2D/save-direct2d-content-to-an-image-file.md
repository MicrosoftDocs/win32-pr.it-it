---
title: Come salvare il contenuto Direct2D in un file di immagine
description: Questo argomento illustra come usare IWICImageEncoder per salvare il contenuto sotto forma di ID2D1Image in un file di immagine codificato, ad esempio JPEG.
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6020b29be3771575919ccb0200718e8e608afded584471625cfa922aee8da8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160367"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a>Come salvare il contenuto Direct2D in un file di immagine

Questo argomento illustra come usare [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) per salvare il contenuto sotto forma di [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in un file di immagine codificato, ad esempio JPEG. Se si scrive un'app di Windows Store, è possibile fare in modo che l'utente seleziona un file di destinazione [**usando Windows::Archiviazione::P ickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Direct2D](./direct2d-portal.md)
-   [Effetti Direct2D](effects-overview.md)
-   [**Windows::Archiviazione::P ickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a>Prerequisiti

-   Sono necessari un [**oggetto ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e un oggetto contenente contenuto [Direct2D](./direct2d-portal.md) che implementa [**ID2D1Image,**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) ad esempio [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) o [**ID2D1Bitmap1.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-get-a-destination-file-and-stream"></a>Passaggio 1: Ottenere un file e un flusso di destinazione

Se si vuole consentire all'utente di selezionare un file di destinazione, è possibile usare [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), aprire il file restituito e ottenere un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) da usare con WIC.

Creare un [**Windows::Archiviazione::P ickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) e impostarne i parametri per i file di immagine. Chiamare il [**metodo PickSaveFileAsync.**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync)


```C++
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    savePicker->DefaultFileExtension = ".jpg";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
```



Dichiarare un gestore di completamento da eseguire dopo la fine dell'operazione asincrona di selezione file. Usare il [**metodo GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) per recuperare il file e per ottenere l'oggetto flusso di file.


```C++
    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }
```



Ottenere un [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) chiamando [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) sul file e ottenendo il risultato dell'operazione asincrona.


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



Usare infine il [**metodo CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) per convertire il flusso di file. Windows Le API di runtime rappresentano i flussi con [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), mentre WIC utilizza [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> Per usare [**la funzione CreateStreamOverRandomAccessStream,**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) è necessario includere **shcore.h** nel progetto.

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a>Passaggio 2: Ottenere la bitmap WIC e il codificatore di frame

[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) forniscono la funzionalità per salvare i dati di creazione dell'immagine in un formato di file codificato.

Creare e inizializzare gli oggetti del codificatore.


```C++
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );
```



### <a name="step-3-get-an-iwicimageencoder"></a>Passaggio 3: Ottenere un oggetto IWICImageEncoder

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) è una nuova interfaccia in Windows 8. Può essere creato da [**IWICImagingFactory2,**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2)che estende **IWICImagingFactory** ed è anche una novità per Windows 8.


```C++
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );
```



Chiamare [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder). Il primo parametro è [**id2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) e deve essere il dispositivo in cui è stata creata l'immagine da codificare. Non è possibile combinare immagini da domini di risorse diversi all'interno di un [**singolo IWICImageEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a>Passaggio 4: Scrivere il contenuto Direct2D usando IWICImageEncoder

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) può scrivere un'immagine [Direct2D](./direct2d-portal.md) in una cornice di immagine, in un'anteprima del frame o nell'anteprima del contenitore. È quindi possibile usare [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) per codificare i dati di creazione dell'immagine in un file come di consueto.

Scrivere [l'immagine Direct2D](./direct2d-portal.md) nel frame. In questo frammento di codice viene scritto [**un oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) che contiene contenuto Direct2D rasterizzato. Tuttavia, è possibile fornire qualsiasi interfaccia che implementa [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).


```C++
    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );
```



> [!Note]  
> Il [**parametro ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) deve essere stato creato nel dispositivo [**ID2D1 passato**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) a [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).

 

Eseguire il commit del WIC e trasmettere le risorse per finalizzare l'operazione.


```C++
    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
```



> [!Note]  
> Alcune implementazioni di [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) non implementano il [**metodo Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) e restituiscono **E \_ NOTIMPL.**

 

A questo punto è disponibile un file contenente [l'immagine Direct2D.](./direct2d-portal.md)

## <a name="complete-example"></a>Esempio completo

Qui il codice completo per questo esempio.

```cpp
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );

void SaveAsImageFile::SaveBitmapToFile()
{
    // Prepare a file picker for customers to input image file name.
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto pngExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    auto bmpExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    bmpExtensions->Append(".bmp");
    savePicker->FileTypeChoices->Insert("BMP file", bmpExtensions);
    savePicker->DefaultFileExtension = ".png";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            m_imageFileName = file->Name;
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".bmp")
            {
                wicFormat = GUID_ContainerFormatBmp;
            }
            else if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }

            // Retrieve a stream from the file.
            task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
            createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
                // Convert the RandomAccessStream to an IStream.
                ComPtr<IStream> stream;
                DX::ThrowIfFailed(
                    CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
                    );

                SaveBitmapToStream(m_d2dTargetBitmap, m_wicFactory, m_d2dContext, wicFormat, stream.Get());
            });
        }
    });
}

// Save render target bitmap to a stream using WIC.
void SaveAsImageFile::SaveBitmapToStream(
    _In_ ComPtr<ID2D1Bitmap1> d2dBitmap,
    _In_ ComPtr<IWICImagingFactory2> wicFactory2,
    _In_ ComPtr<ID2D1DeviceContext> d2dContext,
    _In_ REFGUID wicFormat,
    _In_ IStream* stream
    )
{
    // Create and initialize WIC Bitmap Encoder.
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    // Create and initialize WIC Frame Encoder.
    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );

    // Retrieve D2D Device.
    ComPtr<ID2D1Device> d2dDevice;
    d2dContext->GetDevice(&d2dDevice);

    // Create IWICImageEncoder.
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );

    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
}

```



 

 