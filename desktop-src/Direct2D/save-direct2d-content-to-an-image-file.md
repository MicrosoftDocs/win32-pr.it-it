---
title: Come salvare il contenuto Direct2D in un file di immagine
description: Questo argomento illustra come usare IWICImageEncoder per salvare il contenuto sotto forma di ID2D1Image in un file di immagine codificato, ad esempio JPEG.
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19146d838474046fd634cb5524ddf2367fd1d6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872614"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a><span data-ttu-id="ce579-103">Come salvare il contenuto Direct2D in un file di immagine</span><span class="sxs-lookup"><span data-stu-id="ce579-103">How to save Direct2D content to an image file</span></span>

<span data-ttu-id="ce579-104">Questo argomento illustra come usare [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) per salvare il contenuto sotto forma di [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in un file di immagine codificato, ad esempio JPEG.</span><span class="sxs-lookup"><span data-stu-id="ce579-104">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span> <span data-ttu-id="ce579-105">Se si sta scrivendo un'app di Windows Store, l'utente può selezionare un file di destinazione usando [**Windows:: Storage::P ickers:: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span><span class="sxs-lookup"><span data-stu-id="ce579-105">If you are writing a Windows Store app, you can have the user select a destination file using [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ce579-106">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="ce579-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ce579-107">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="ce579-107">Technologies</span></span>

-   [<span data-ttu-id="ce579-108">Direct2D</span><span class="sxs-lookup"><span data-stu-id="ce579-108">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="ce579-109">Effetti Direct2D</span><span class="sxs-lookup"><span data-stu-id="ce579-109">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="ce579-110">**Windows:: Storage::P ickers:: FileSavePicker**</span><span class="sxs-lookup"><span data-stu-id="ce579-110">**Windows::Storage::Pickers::FileSavePicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a><span data-ttu-id="ce579-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="ce579-111">Prerequisites</span></span>

-   <span data-ttu-id="ce579-112">Sono necessari un oggetto [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e un oggetto che contiene contenuto [Direct2D](./direct2d-portal.md) che implementa [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) , ad esempio [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) o [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span><span class="sxs-lookup"><span data-stu-id="ce579-112">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object and an object containing [Direct2D](./direct2d-portal.md) content that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) such as [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) or [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span></span>

## <a name="instructions"></a><span data-ttu-id="ce579-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="ce579-113">Instructions</span></span>

### <a name="step-1-get-a-destination-file-and-stream"></a><span data-ttu-id="ce579-114">Passaggio 1: ottenere un file e un flusso di destinazione</span><span class="sxs-lookup"><span data-stu-id="ce579-114">Step 1: Get a destination file and stream</span></span>

<span data-ttu-id="ce579-115">Se si vuole consentire all'utente di selezionare un file di destinazione, è possibile usare [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), aprire il file restituito e ottenere un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) da usare con WIC.</span><span class="sxs-lookup"><span data-stu-id="ce579-115">If you want to allow the user to select a destination file, you can use [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), open the returned file, and obtain an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) to use with WIC.</span></span>

<span data-ttu-id="ce579-116">Creare [**Windows:: Storage::P ickers:: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) e impostarne i parametri per i file di immagine.</span><span class="sxs-lookup"><span data-stu-id="ce579-116">Create a [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) and set its parameters for image files.</span></span> <span data-ttu-id="ce579-117">Chiamare il metodo [**pickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) .</span><span class="sxs-lookup"><span data-stu-id="ce579-117">Call the [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) method.</span></span>


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



<span data-ttu-id="ce579-118">Dichiarare un gestore di completamento da eseguire dopo la restituzione dell'operazione asincrona di selezione file.</span><span class="sxs-lookup"><span data-stu-id="ce579-118">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="ce579-119">Usare il metodo [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) per recuperare il file e ottenere l'oggetto del flusso di file.</span><span class="sxs-lookup"><span data-stu-id="ce579-119">Use the [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) method to retrieve the file and to get the file stream object.</span></span>


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



<span data-ttu-id="ce579-120">Ottenere un [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) chiamando [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) sul file e ottenendo il risultato dell'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="ce579-120">Obtain an [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) by calling [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) on the file and getting the result of the async operation.</span></span>


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



<span data-ttu-id="ce579-121">Infine, usare il metodo [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) per convertire il flusso di file.</span><span class="sxs-lookup"><span data-stu-id="ce579-121">Finally, use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) method to convert the file stream.</span></span> <span data-ttu-id="ce579-122">Windows Runtime API rappresentano i flussi con [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), mentre WIC utilizza [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="ce579-122">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while WIC consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> <span data-ttu-id="ce579-123">Per usare la funzione [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , è necessario includere **shcore. h** nel progetto.</span><span class="sxs-lookup"><span data-stu-id="ce579-123">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include **shcore.h** in your project.</span></span>

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a><span data-ttu-id="ce579-124">Passaggio 2: ottenere la bitmap WIC e il codificatore di frame</span><span class="sxs-lookup"><span data-stu-id="ce579-124">Step 2: Get the WIC bitmap and frame encoder</span></span>

<span data-ttu-id="ce579-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) forniscono la funzionalità per salvare i dati dell'immagine in un formato di file codificato.</span><span class="sxs-lookup"><span data-stu-id="ce579-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) provide the functionality to save imaging data to an encoded file format.</span></span>

<span data-ttu-id="ce579-126">Creare e inizializzare gli oggetti del codificatore.</span><span class="sxs-lookup"><span data-stu-id="ce579-126">Create and initialize the encoder objects.</span></span>


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



### <a name="step-3-get-an-iwicimageencoder"></a><span data-ttu-id="ce579-127">Passaggio 3: ottenere un IWICImageEncoder</span><span class="sxs-lookup"><span data-stu-id="ce579-127">Step 3: Get an IWICImageEncoder</span></span>

<span data-ttu-id="ce579-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) è una nuova interfaccia di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ce579-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) is a new interface in Windows 8.</span></span> <span data-ttu-id="ce579-129">Può essere creato da [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), che estende **IWICImagingFactory** ed è inoltre nuovo per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ce579-129">It can be created from [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), which extends **IWICImagingFactory** and is also new for Windows 8.</span></span>


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



<span data-ttu-id="ce579-130">Chiamare [**IWICImagingFactory2:: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="ce579-130">Call [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span> <span data-ttu-id="ce579-131">Il primo parametro è un [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) e deve essere il dispositivo in cui è stata creata l'immagine che si vuole codificare. non è possibile combinare immagini da domini di risorse diversi all'interno di un singolo [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span><span class="sxs-lookup"><span data-stu-id="ce579-131">The first parameter is an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) and must be the device on which the image you want to encode was created – you cannot mix images from different resource domains within a single [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span></span>


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a><span data-ttu-id="ce579-132">Passaggio 4: scrivere il contenuto Direct2D usando IWICImageEncoder</span><span class="sxs-lookup"><span data-stu-id="ce579-132">Step 4: Write the Direct2D content using IWICImageEncoder</span></span>

<span data-ttu-id="ce579-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) può scrivere un'immagine [Direct2D](./direct2d-portal.md) in un frame immagine, un'anteprima del frame o l'anteprima del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ce579-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) can write a [Direct2D](./direct2d-portal.md) image into an image frame, a frame thumbnail, or the container thumbnail.</span></span> <span data-ttu-id="ce579-134">È quindi possibile usare [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) per codificare i dati di imaging in un file come di consueto.</span><span class="sxs-lookup"><span data-stu-id="ce579-134">You can then use [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) to encode the imaging data to a file as normal.</span></span>

<span data-ttu-id="ce579-135">Scrivere l'immagine [Direct2D](./direct2d-portal.md) nel frame.</span><span class="sxs-lookup"><span data-stu-id="ce579-135">Write the [Direct2D](./direct2d-portal.md) image to the frame.</span></span> <span data-ttu-id="ce579-136">In questo frammento viene scritto un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) che contiene contenuto Direct2D rasterizzato.</span><span class="sxs-lookup"><span data-stu-id="ce579-136">In this snippet we write an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) that contains rasterized Direct2D content.</span></span> <span data-ttu-id="ce579-137">Tuttavia, è possibile fornire qualsiasi interfaccia che implementi [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span><span class="sxs-lookup"><span data-stu-id="ce579-137">However, you can provide any interface that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span></span>


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
> <span data-ttu-id="ce579-138">Il parametro [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) deve essere stato creato in [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) passato a [**IWICImagingFactory2:: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="ce579-138">The [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) parameter must have been created on the [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) that was passed into [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span>

 

<span data-ttu-id="ce579-139">Eseguire il commit delle risorse WIC e Stream per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ce579-139">Commit the WIC and stream resources to finalize the operation.</span></span>


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
> <span data-ttu-id="ce579-140">Alcune implementazioni di [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) non implementano il metodo [**commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) e restituiscono **e \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="ce579-140">Some implementations of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) do not implement the [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) method and return **E\_NOTIMPL**.</span></span>

 

<span data-ttu-id="ce579-141">A questo punto si dispone di un file contenente l'immagine [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ce579-141">Now you have a file containing the [Direct2D](./direct2d-portal.md) image.</span></span>

## <a name="complete-example"></a><span data-ttu-id="ce579-142">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="ce579-142">Complete example</span></span>

<span data-ttu-id="ce579-143">Ecco il codice completo per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="ce579-143">Here the full code for this example.</span></span>

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



 

 