---
description: Nell'esempio seguente viene illustrato come ricodificare un'immagine e i relativi metadati in un nuovo file dello stesso formato.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: Come ricodificare un'immagine JPEG con metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13851af04c6af742dbc68acc31fd674c3602ebeb16bec6903a3570f8cb1e0400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088163"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a>Come ricodificare un'immagine JPEG con metadati

Nell'esempio seguente viene illustrato come ricodificare un'immagine e i relativi metadati in un nuovo file dello stesso formato. Questo esempio aggiunge anche metadati per illustrare un'espressione a singolo elemento usata da un writer di query.

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Parte 1: Decodificare un'immagine](#part-1-decode-an-image)
-   [Parte 2: Creare e inizializzare il codificatore di immagini](#part-2-create-and-initialize-the-image-encoder)
-   [Parte 3: Copiare informazioni sui frame decodificati](#part-3-copy-decoded-frame-information)
-   [Parte 4: Copiare i metadati](#part-4-copy-the-metadata)
-   [Parte 5: Aggiungere metadati aggiuntivi](#part-5-add-additional-metadata)
-   [Parte 6: Finalizzare l'immagine codificata](#part-6-finalize-the-encoded-image)
-   [Codice di esempio di ricodifica JPEG](#jpeg-re-encode-example-code)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere familiarità con il sistema di metadati wic (Windows Imaging Component), come descritto in Panoramica dei metadati [WIC](-wic-about-metadata.md). È anche necessario avere familiarità con i componenti del codec WIC, come descritto nella Windows [cenni preliminari sul](-wic-about-windows-imaging-codec.md)componente di imaging.

## <a name="part-1-decode-an-image"></a>Parte 1: Decodificare un'immagine

Prima di poter copiare i dati o i metadati dell'immagine in un nuovo file di immagine, è necessario creare un decodificatore per l'immagine esistente che si vuole ricodificare. Il codice seguente illustra come creare un decodificatore WIC per il file di immagine test.jpg.


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



La chiamata a **CreateDecoderFromFilename** ha usato il valore WICDecodeMetadataCacheOnDemand dall'enumerazione [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) come quarto parametro. Ciò indica al decodificatore di memorizzare nella cache i metadati quando sono necessari, ottenendo un lettore di query o usando il lettore di metadati sottostante. L'uso di questa opzione consente di mantenere il flusso ai metadati, che è necessario per eseguire la codifica rapida dei metadati e consente la decodifica e la codifica senza perdita di dati delle immagini JPEG. In alternativa, è possibile usare l'altro valore **WICDecodeOptions,** WICDecodeMetadataCacheOnLoad, che memorizza nella cache i metadati dell'immagine incorporata non appena l'immagine viene caricata.

## <a name="part-2-create-and-initialize-the-image-encoder"></a>Parte 2: Creare e inizializzare il codificatore di immagini

Il codice seguente illustra la creazione del codificatore che verrà utilizzato per codificare l'immagine decodificata in precedenza.


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



Viene creato e inizializzato un flusso di file WIC piFileStream per la scrittura nel file di immagine "test2.jpg". piFileStream viene quindi usato per inizializzare il codificatore, indicando al codificatore dove scrivere i bit dell'immagine al termine della codifica.

## <a name="part-3-copy-decoded-frame-information"></a>Parte 3: Copiare informazioni sui frame decodificati

Il codice seguente copia ogni frame di un'immagine in un nuovo frame del codificatore. Questa copia include dimensioni, risoluzione e formato pixel. tutti necessari per creare un frame valido.

> [!Note]  
> Le immagini JPEG avranno un solo frame e il ciclo seguente non è tecnicamente necessario, ma è incluso per illustrare l'utilizzo di più fotogrammi per i formati che lo supportano.

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



Il codice seguente esegue un controllo rapido per determinare se i formati di immagine di origine e di destinazione sono uguali. Questa operazione è necessaria perché la parte 4 mostra un'operazione supportata solo quando il formato di origine e di destinazione è lo stesso.


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a>Parte 4: Copiare i metadati

> [!Note]  
> Il codice in questa sezione è valido solo quando i formati di immagine di origine e di destinazione sono uguali. Non è possibile copiare tutti i metadati di un'immagine in una singola operazione durante la codifica in un formato di immagine diverso.

 

Per mantenere i metadati durante la ri-codifica di un'immagine nello stesso formato di immagine, sono disponibili metodi per copiare tutti i metadati in una singola operazione. Ognuna di queste operazioni segue un modello simile. ognuno imposta i metadati del frame decodificato direttamente nel nuovo frame da codificare. Si noti che questa operazione viene eseguita per ogni singola cornice di immagine.

Il metodo preferito per la copia dei metadati è inizializzare il writer di blocchi del nuovo frame con il lettore di blocchi del frame decodificato. Il codice seguente illustra questo metodo.


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



In questo esempio si ottiene semplicemente il lettore di blocchi e il writer di blocchi rispettivamente dal frame di origine e dal frame di destinazione. Il writer di blocchi viene quindi inizializzato dal lettore di blocchi. Inizializza il writer di blocchi con i metadati precompilato del lettore di blocchi. Per informazioni sui metodi aggiuntivi per la copia dei metadati, vedere la sezione Scrittura di metadati in Panoramica della lettura e [della scrittura di metadati dell'immagine](-wic-codec-readingwritingmetadata.md).

Anche in questo caso, questa operazione funziona solo quando le immagini di origine e di destinazione hanno lo stesso formato. Questo perché formati di immagine diversi archiviano i blocchi di metadati in posizioni diverse. Ad esempio, sia JPEG che Tagged Image File Format (TIFF) supportano blocchi di metadati XMP (Extensible Metadata Platform). Nelle immagini JPEG, il blocco XMP si trova nel blocco di metadati radice, come illustrato nella panoramica [dei metadati WIC](-wic-about-metadata.md). Tuttavia, in un'immagine TIFF, il blocco XMP è incorporato nel blocco IFD radice.

## <a name="part-5-add-additional-metadata"></a>Parte 5: Aggiungere metadati aggiuntivi

Nell'esempio seguente viene illustrato come aggiungere metadati all'immagine di destinazione. Questa operazione viene eseguita chiamando il metodo **SetMetadataByName** del writer di query usando un'espressione di query e i dati archiviati in [un oggetto PROPVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



Per altre informazioni sull'espressione di query, vedere Panoramica [del linguaggio di query sui metadati](-wic-codec-metadataquerylanguage.md).

## <a name="part-6-finalize-the-encoded-image"></a>Parte 6: Finalizzare l'immagine codificata

I passaggi finali per la copia dell'immagine sono la scrittura dei dati pixel per il frame, il commit del frame nel codificatore e il commit del codificatore. Il commit del codificatore scrive il flusso dell'immagine nel file.


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



Il metodo **WriteSource** del frame viene usato per scrivere i dati pixel per l'immagine. Si noti che questa operazione viene eseguita dopo la scrittura dei metadati. Questa operazione è necessaria per garantire che i metadati abbia spazio sufficiente all'interno del file di immagine. Dopo aver scritto i dati pixel, il frame viene scritto nel flusso usando il metodo **Commit del** frame. Dopo l'elaborazione di tutti i fotogrammi, il codificatore (e quindi l'immagine) viene finalizzato usando il metodo **Commit del** codificatore.

Dopo aver eseguito il commit del frame, è necessario rilasciare gli oggetti COM creati nel ciclo .

## <a name="jpeg-re-encode-example-code"></a>Codice di esempio di ricodifica JPEG

Di seguito è riportato il codice delle parti da 1 a 6 in un blocco convieniente.


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica dei metadati WIC](-wic-about-metadata.md)
</dt> <dt>

[Panoramica del linguaggio di query sui metadati](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Panoramica della lettura e della scrittura di metadati dell'immagine](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Panoramica dell'estendibilità dei metadati](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
