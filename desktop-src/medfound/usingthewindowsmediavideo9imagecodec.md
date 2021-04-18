---
description: Uso della categoria di immagini Windows Media Video 9,1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Uso della categoria di immagini Windows Media Video 9,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b545d37b61a1c89ffdd69615b28f636aa98b32
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320743"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Uso della categoria di immagini Windows Media Video 9,1

La categoria di immagini Windows Media Video 9,1 è diversa dalle altre categorie di output supportate dal codificatore e dal decodificatore Windows Media Video 9. Anziché elaborare un video non compresso, sono necessari esempi di input speciali costituiti da dati di trasformazione strutturati e, occasionalmente, da immagini bitmap RGB in cui vengono eseguite le trasformazioni.

Il contenuto dell'immagine Windows Media Video 9,1 codificato è praticamente identico al contenuto normale con codifica Windows Media Video 9, ma è identificato dal relativo FOURCC ("WMVP").

Il tipo di output del codificatore per l'immagine video è esattamente uguale a quello del video Windows Media standard, ad eccezione del fatto che il sottotipo e i valori di compressione devono essere impostati sugli identificatori delle immagini video. Ciò include la necessità di ottenere i dati privati dei codec e di aggiungerli alla struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Per ulteriori informazioni, vedere [Configuring video encoding](configuringvideoencoding.md).

Anche la configurazione del tipo di input per l'immagine video è molto simile alla configurazione di input per gli altri codificatori video. È possibile recuperare un [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) parzialmente completato dal codificatore chiamando [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)o se si usa l'SDK Media Foundation, chiamando [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) e recuperando il **\_ \_ tipo di supporto DMO** usando [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). È quindi possibile impostare le dimensioni del frame e la struttura del formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , come per il video standard. Come nel caso del tipo di output, è necessario assicurarsi che il sottotipo e i valori di compressione siano impostati in modo appropriato.

## <a name="creating-input-samples"></a>Creazione di esempi di input

Gli esempi di input per il codec di immagini video sono strutturati. La definizione della struttura e delle costanti usate per l'immagine video non è inclusa con le interfacce del codec Windows Media Audio e video. Queste definizioni sono incluse in Windows Media Format SDK e il loro utilizzo è completamente illustrato nella documentazione di Windows Media Format SDK.

## <a name="decoding"></a>Decodifica

Non sono previsti requisiti speciali per la decodifica del video di acquisizione schermo. Diverso da un sottotipo diverso (MEDIASUBTYPE \_ WMVP) usato per l'input del decodificatore, il flusso di immagini video compresso è essenzialmente identico a un flusso di Windows Media video standard.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 
