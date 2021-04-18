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
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a><span data-ttu-id="1dc34-105">Come caricare un'immagine in effetti Direct2D usando il Filepicker</span><span class="sxs-lookup"><span data-stu-id="1dc34-105">How to load an image into Direct2D effects using the FilePicker</span></span>

<span data-ttu-id="1dc34-106">Mostra come usare [**Windows:: Storage::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) per caricare un'immagine in [effetti Direct2D](effects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1dc34-106">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="1dc34-107">Se si vuole consentire all'utente di selezionare un file di immagine dalla risorsa di archiviazione in un'app di Windows Store, è consigliabile usare [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).</span><span class="sxs-lookup"><span data-stu-id="1dc34-107">If you want to let the user select an image file from storage in a Windows Store app, we recommend that you use the [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1dc34-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="1dc34-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1dc34-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="1dc34-109">Technologies</span></span>

-   [<span data-ttu-id="1dc34-110">Direct2D</span><span class="sxs-lookup"><span data-stu-id="1dc34-110">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="1dc34-111">Effetti Direct2D</span><span class="sxs-lookup"><span data-stu-id="1dc34-111">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="1dc34-112">**Windows:: Storage::P ickers:: FileOpenPicker**</span><span class="sxs-lookup"><span data-stu-id="1dc34-112">**Windows::Storage::Pickers::FileOpenPicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a><span data-ttu-id="1dc34-113">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="1dc34-113">Prerequisites</span></span>

-   <span data-ttu-id="1dc34-114">È necessario un oggetto [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) per la creazione di effetti.</span><span class="sxs-lookup"><span data-stu-id="1dc34-114">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object for creating effects.</span></span>
-   <span data-ttu-id="1dc34-115">Per la creazione di oggetti WIC è necessario un oggetto [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) .</span><span class="sxs-lookup"><span data-stu-id="1dc34-115">You need an [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) object for creating WIC objects.</span></span>

## <a name="instructions"></a><span data-ttu-id="1dc34-116">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="1dc34-116">Instructions</span></span>

### <a name="step-1-open-the-file-picker"></a><span data-ttu-id="1dc34-117">Passaggio 1: aprire il selettore file</span><span class="sxs-lookup"><span data-stu-id="1dc34-117">Step 1: Open the file picker</span></span>

<span data-ttu-id="1dc34-118">Creare un oggetto [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) e impostare *ViewMode*, *SuggestedStartLocation* e *fileTypeFilter* per la selezione di immagini.</span><span class="sxs-lookup"><span data-stu-id="1dc34-118">Create a [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) object and set the *ViewMode*, *SuggestedStartLocation*, and the *FileTypeFilter* for selecting images.</span></span> <span data-ttu-id="1dc34-119">Chiamare il metodo [**pickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) .</span><span class="sxs-lookup"><span data-stu-id="1dc34-119">Call the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) method.</span></span>


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



<span data-ttu-id="1dc34-120">Al termine del [**pickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) , si ottiene un flusso di file dall'interfaccia [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) che restituisce.</span><span class="sxs-lookup"><span data-stu-id="1dc34-120">After the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) completes, you get a file stream from the [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) interface it returns.</span></span>

### <a name="step-2-get-a-file-stream"></a><span data-ttu-id="1dc34-121">Passaggio 2: ottenere un flusso di file</span><span class="sxs-lookup"><span data-stu-id="1dc34-121">Step 2: Get a file stream</span></span>

<span data-ttu-id="1dc34-122">Dichiarare un gestore di completamento da eseguire dopo la restituzione dell'operazione asincrona di selezione file.</span><span class="sxs-lookup"><span data-stu-id="1dc34-122">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="1dc34-123">Usare il metodo [**GetResults**](/previous-versions//br205815(v=vs.85)) per recuperare il file e ottenere l'oggetto del flusso di file.</span><span class="sxs-lookup"><span data-stu-id="1dc34-123">Use the [**GetResults**](/previous-versions//br205815(v=vs.85)) method to retrieve the file and to get the file stream object.</span></span>


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



<span data-ttu-id="1dc34-124">Nel passaggio successivo si convertirà l'oggetto [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) in un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) che è possibile passare a [WIC](/windows/desktop/wic/-wic-api).</span><span class="sxs-lookup"><span data-stu-id="1dc34-124">In the next step you convert the [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) object to an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) that you can pass to [WIC](/windows/desktop/wic/-wic-api).</span></span>

### <a name="step-3-convert-the-file-stream"></a><span data-ttu-id="1dc34-125">Passaggio 3: convertire il flusso di file</span><span class="sxs-lookup"><span data-stu-id="1dc34-125">Step 3: Convert the file stream</span></span>

<span data-ttu-id="1dc34-126">Utilizzare la funzione [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) per convertire il flusso di file.</span><span class="sxs-lookup"><span data-stu-id="1dc34-126">Use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function to convert the file stream.</span></span> <span data-ttu-id="1dc34-127">Windows Runtime API rappresentano i flussi con [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), mentre [WIC](/windows/desktop/wic/-wic-api) utilizza [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="1dc34-127">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while [WIC](/windows/desktop/wic/-wic-api) consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


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
> <span data-ttu-id="1dc34-128">Per usare la funzione [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , è necessario includere *shcore. h* nel progetto.</span><span class="sxs-lookup"><span data-stu-id="1dc34-128">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include *shcore.h* in your project.</span></span>

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a><span data-ttu-id="1dc34-129">Passaggio 4: creare un decodificatore WIC e ottenere il frame</span><span class="sxs-lookup"><span data-stu-id="1dc34-129">Step 4: Create a WIC decoder and get the frame</span></span>

<span data-ttu-id="1dc34-130">Creare un oggetto [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) usando il metodo [**IWICImagingFactory:: CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="1dc34-130">Create an [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) object using the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>


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



<span data-ttu-id="1dc34-131">Ottenere il primo frame dell'immagine dal decodificatore usando il metodo [**IWICBitmapDecoder:: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .</span><span class="sxs-lookup"><span data-stu-id="1dc34-131">Get the first frame of the image from the decoder using the [**IWICBitmapDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a><span data-ttu-id="1dc34-132">Passaggio 5: creare un convertitore WIC e inizializzare</span><span class="sxs-lookup"><span data-stu-id="1dc34-132">Step 5: Create a WIC converter and initialize</span></span>

<span data-ttu-id="1dc34-133">Convertire l'immagine nel formato di colore BGRA utilizzando [WIC](/windows/desktop/wic/-wic-api).</span><span class="sxs-lookup"><span data-stu-id="1dc34-133">Convert the image to the BGRA color format using [WIC](/windows/desktop/wic/-wic-api).</span></span> <span data-ttu-id="1dc34-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) restituirà il formato pixel nativo dell'immagine, ad esempio i file JPEG vengono archiviati nel GUID \_ WICPixelFormat24bppBGR.</span><span class="sxs-lookup"><span data-stu-id="1dc34-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) will return the native pixel format of the image, like JPEGs are stored in GUID\_WICPixelFormat24bppBGR.</span></span> <span data-ttu-id="1dc34-135">Tuttavia, come ottimizzazione delle prestazioni con Direct2D si consiglia di eseguire la conversione in WICPixelFormat32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="1dc34-135">However, as a performance optimization with Direct2D we recommend that you convert to WICPixelFormat32bppPBGRA.</span></span>

1.  <span data-ttu-id="1dc34-136">Creare un oggetto [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) usando il metodo [**IWICImagingFactory:: CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="1dc34-136">Create a [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) object using the [**IWICImagingFactory::CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  <span data-ttu-id="1dc34-137">Inizializzare il convertitore di formato per usare WICPixelFormat32bppPBGRA e passare il frame bitmap.</span><span class="sxs-lookup"><span data-stu-id="1dc34-137">Initialize the format converter to use the WICPixelFormat32bppPBGRA and pass in the bitmap frame.</span></span>

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

    

<span data-ttu-id="1dc34-138">L'interfaccia [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) è derivata dall'interfaccia [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) , quindi è possibile passare il convertitore all'effetto [origine bitmap](bitmap-source.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc34-138">The [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) interface is derived from the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) interface, so you can pass the converter to the [bitmap source](bitmap-source.md) effect.</span></span>

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a><span data-ttu-id="1dc34-139">Passaggio 6: creare un effetto e passare un IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="1dc34-139">Step 6: Create effect and pass in an IWICBitmapSource</span></span>

<span data-ttu-id="1dc34-140">Usare il metodo [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) per creare un oggetto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) di [origine bitmap](bitmap-source.md) usando il [**contesto di periferica**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](getting-started-with-direct2d.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc34-140">Use the [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method to create a [bitmap source](bitmap-source.md) [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object using the [Direct2D](getting-started-with-direct2d.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span>

<span data-ttu-id="1dc34-141">Usare il metodo [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) per impostare la proprietà di *origine della bitmap di d2d1 \_ BITMAPSOURCE \_ prop \_ WIC \_ \_* sul [**convertitore di formato**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) [WIC](/windows/desktop/wic/-wic-api) .</span><span class="sxs-lookup"><span data-stu-id="1dc34-141">Use the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method to set the *D2D1\_BITMAPSOURCE\_PROP\_WIC\_BITMAP\_SOURCE* property to the [WIC](/windows/desktop/wic/-wic-api) [**format converter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter).</span></span>

> [!Note]  
> <span data-ttu-id="1dc34-142">L'effetto [origine bitmap](bitmap-source.md) non accetta un input dal metodo [**seinput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) come molti [effetti Direct2D](effects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1dc34-142">The [bitmap source](bitmap-source.md) effect doesn't take an input from the [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method like many [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="1dc34-143">L'oggetto [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) viene invece specificato come proprietà.</span><span class="sxs-lookup"><span data-stu-id="1dc34-143">Instead, the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) object is specified as a property.</span></span>

 


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



<span data-ttu-id="1dc34-144">Ora che si dispone dell'effetto [origine bitmap](bitmap-source.md) , è possibile usarlo come input per qualsiasi [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e creare un grafico effetto.</span><span class="sxs-lookup"><span data-stu-id="1dc34-144">Now that you have the [bitmap source](bitmap-source.md) effect, you can use it as input to any [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) and create an effect graph.</span></span>

## <a name="complete-example"></a><span data-ttu-id="1dc34-145">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="1dc34-145">Complete example</span></span>

<span data-ttu-id="1dc34-146">Ecco il codice completo per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="1dc34-146">Here is the full code for this example.</span></span>


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



 

 