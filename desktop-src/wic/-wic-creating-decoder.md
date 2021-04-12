---
description: In questo argomento viene introdotto il decodificatore bitmap, un componente di base del codec Windows Imaging Component (WIC) utilizzato per decodificare i file di immagine da un flusso.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Panoramica della decodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349871"
---
# <a name="decoding-overview"></a>Panoramica della decodifica

In questo argomento viene introdotto il decodificatore bitmap, un componente di base del codec Windows Imaging Component (WIC) utilizzato per decodificare i file di immagine da un flusso.

In questo argomento sono contenute le sezioni seguenti.

-   [Introduzione](#introduction)
-   [Decodificatori bitmap nativi](#native-bitmap-decoders)
-   [Creazione di un decodificatore bitmap](#creating-a-bitmap-decoder)
-   [Estensibilità del decodificatore](#decoder-extensibility)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

I decodificatori di bitmap possono essere visualizzati come contenitore esterno di un'immagine digitale e forniscono l'accesso alle proprietà globali e ai frame di immagine. Alcuni formati di immagine supportano anteprime globali, anteprime, contesti di colore o metadati, mentre altri forniscono tali proprietà solo a livello di frame. Si noti tuttavia che molti dei formati di immagine standard non supportano queste proprietà globali. Di conseguenza, molte delle implementazioni di codec native fornite da WIC non supportano la maggior parte di queste proprietà globali. Per informazioni sul supporto delle proprietà globali, vedere la tabella nella sezione decodificatori bitmap nativi di questo argomento.

In WIC i decodificatori di bitmap sono rappresentati dall'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e forniscono l'accesso a queste proprietà globali della bitmap e, più importante, i frame in esso contenuti. L'interfaccia [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) rappresenta un singolo frame bitmap ed è descritta in dettaglio nella [Panoramica delle origini bitmap](-wic-bitmapsources.md).

## <a name="native-bitmap-decoders"></a>Decodificatori bitmap nativi

WIC fornisce diverse implementazioni native dell'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) per i formati di immagine Web standard e il formato di foto HD con intervallo dinamico elevato. Nella tabella seguente sono elencati i decodificatori nativi disponibili, il nome dell'identificatore di classe e il supporto per le proprietà globali. Anche se una funzionalità potrebbe non supportare una proprietà, ad esempio anteprime a livello globale, il formato dell'immagine può supportare tali proprietà a livello di singolo frame.



| Formato immagine | Nome CLSID            | Anteprime | Anteprime | Contesti colori | Metadati |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | \_WICBMPDECODER CLSID  | No         | No       | No             | No       |
| GIF          | \_WICGIFDECODER CLSID  | No         | No       | No             | Sì      |
| ICO          | \_WICICODECODER CLSID  | No         | No       | No             | No       |
| JPEG         | \_WICJPEGDECODER CLSID | No         | No       | No             | No       |
| PNG          | \_WICPNGDECODER CLSID  | No         | No       | No             | No       |
| TIFF         | \_WICTIFFDECODER CLSID | No         | No       | No             | No       |
| Foto HD     | \_WICWMPDECODER CLSID  | No         | Sì      | No             | No       |



 

## <a name="creating-a-bitmap-decoder"></a>Creazione di un decodificatore bitmap

Per decodificare un'immagine usando WIC, è prima di tutto necessario creare un'istanza di [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) per il formato di immagine di destinazione. L'istanza del decodificatore consente di accedere alle proprietà e ai metadati globali, se supportati, nonché ai frame dell'immagine. WIC Imaging Factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), fornisce diversi metodi per la creazione di decodificatori di bitmap. Per creare i decodificatori di bitmap, vengono forniti i metodi factory seguenti.

-   [**CreateDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

Il codice seguente illustra come creare un decodificatore bitmap usando un nome file di immagine e recuperare il primo frame dell'immagine.


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



## <a name="decoder-extensibility"></a>Estensibilità del decodificatore

Una delle funzionalità principali di WIC è un Framework di estendibilità che consente agli sviluppatori di codec di sviluppare i propri codec di immagine e ottenere lo stesso supporto della piattaforma delle implementazioni native dei codec di immagine. Un unico set coerente di interfacce viene usato per l'elaborazione di tutte le immagini, indipendentemente dal formato di immagine. Qualsiasi applicazione che utilizza WIC ottiene il supporto automatico per i nuovi formati di immagine non appena viene installato il codec. Per ulteriori informazioni sullo sviluppo di codec, vedere gli argomenti relativi [allo sviluppo di componenti](-wic-component-development.md). Per ulteriori informazioni sullo sviluppo di decodificatori, vedere [implementazione di un Decodificatore WIC-Enabled](-wic-implementingwicdecoder.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica della codifica](-wic-creating-encoder.md)
</dt> <dt>

[Sviluppo di componenti](-wic-component-development.md)
</dt> </dl>

 

 



