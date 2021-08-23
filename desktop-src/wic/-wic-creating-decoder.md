---
description: L'argomento presenta il decodificatore bitmap, un componente core Windows codec WIC (Imaging Component) usato per decodificare i file di immagine da un flusso.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Cenni preliminari sulla decodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14300c9857702ceff5f07fcc127a4ef4182f9e77ad46f0598edc12abf91f240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711405"
---
# <a name="decoding-overview"></a>Cenni preliminari sulla decodifica

L'argomento presenta il decodificatore bitmap, un componente core Windows codec WIC (Imaging Component) usato per decodificare i file di immagine da un flusso.

In questo argomento sono contenute le sezioni seguenti.

-   [Introduzione](#introduction)
-   [Decodificatori bitmap nativi](#native-bitmap-decoders)
-   [Creazione di un decodificatore bitmap](#creating-a-bitmap-decoder)
-   [Estendibilità del decodificatore](#decoder-extensibility)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

I decodificatori bitmap possono essere visualizzati come contenitore esterno di un'immagine digitale e forniscono l'accesso a proprietà globali e fotogrammi immagine. Alcuni formati di immagine supportano anteprime globali, anteprime, contesti di colore o metadati, mentre altri forniscono queste proprietà solo a livello di fotogramma. Si noti, tuttavia, che molti dei formati di immagine standard non supportano queste proprietà globali. Di conseguenza, molte delle implementazioni native del codec fornite da WIC non supportano la maggior parte di queste proprietà globali. Per informazioni sul supporto delle proprietà globali, vedere la tabella nella sezione Native Bitmap Decoders di questo argomento.

In WIC i decodificatori bitmap sono rappresentati dall'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e forniscono l'accesso a queste proprietà globali della bitmap e, soprattutto, ai fotogrammi in essa contenuti. [**L'interfaccia IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) rappresenta un singolo frame bitmap ed è illustrata in dettaglio in [Cenni preliminari sulle origini bitmap.](-wic-bitmapsources.md)

## <a name="native-bitmap-decoders"></a>Decodificatori bitmap nativi

WIC offre diverse implementazioni native [**dell'interfaccia IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) per i formati di immagine Web standard e il formato HD Photo a intervallo dinamico elevato. Nella tabella seguente sono elencati i decodificatori nativi disponibili, il nome dell'identificatore di classe e il supporto per le proprietà globali. Anche se una funzionalità potrebbe non supportare una proprietà, ad esempio le anteprime a livello globale, il formato dell'immagine può supportare tali proprietà a livello di singolo fotogramma.



| Formato immagine | Nome CLSID            | Anteprime | Anteprime | Contesti dei colori | Metadati |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | CLSID \_ WICBmpDecoder  | No         | No       | No             | No       |
| GIF          | CLSID \_ WICGifDecoder  | No         | No       | No             | Sì      |
| ICO          | CLSID \_ WICIcoDecoder  | No         | No       | No             | No       |
| JPEG         | CLSID \_ WICJpegDecoder | No         | No       | No             | No       |
| PNG          | CLSID \_ WICPngDecoder  | No         | No       | No             | No       |
| TIFF         | CLSID \_ WICTiffDecoder | No         | No       | No             | No       |
| HD Photo     | CLSID \_ WICWmpDecoder  | No         | Sì      | No             | No       |



 

## <a name="creating-a-bitmap-decoder"></a>Creazione di un decodificatore bitmap

Per decodificare un'immagine usando WIC, è prima necessario creare un'istanza di [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) per il formato di immagine di destinazione. L'istanza del decodificatore consente di accedere alle proprietà e ai metadati globali, se supportati, nonché ai fotogrammi dell'immagine. La factory di creazione dell'immagine [**WIC, IWICImagingFactory,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)fornisce diversi metodi per la creazione di decodificatori bitmap. Per creare decodificatori bitmap, vengono forniti i metodi factory seguenti.

-   [**CreateDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

Il codice seguente illustra come creare un decodificatore bitmap usando un nome file di immagine e recuperare il primo fotogramma dell'immagine.


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a>Estendibilità del decodificatore

Una delle funzionalità principali di WIC è un framework di estendibilità che consente agli sviluppatori di codec di sviluppare codec immagine personalizzati e ottenere lo stesso supporto della piattaforma delle implementazioni native dei codec di immagine. Un singolo set coerente di interfacce viene usato per l'elaborazione di tutte le immagini, indipendentemente dal formato dell'immagine. Qualsiasi applicazione che usa WIC ottiene il supporto automatico per i nuovi formati di immagine non appena viene installato il codec. Per altre informazioni sullo sviluppo di codec, vedere gli argomenti in [Sviluppo di componenti.](-wic-component-development.md) Per altre informazioni sullo sviluppo di decodificatori, vedere [Implementazione di un WIC-Enabled decodificatore.](-wic-implementingwicdecoder.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Cenni preliminari sulla codifica](-wic-creating-encoder.md)
</dt> <dt>

[Sviluppo di componenti](-wic-component-development.md)
</dt> </dl>

 

 



