---
description: Uso della Windows di immagini di Media Video 9.1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Uso della Windows di immagini di Media Video 9.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c630be78ec3edef1a47322b31f6a2331f15134a0cdffa4107b5a79daa86e9091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972630"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Uso della Windows di immagini di Media Video 9.1

La Windows Media Video 9.1 Image è diversa dalle altre categorie di output supportate dal codificatore e decodificatore Windows Media Video 9. Invece di elaborare video non compressi, accetta esempi di input speciali costituiti da dati di trasformazione strutturati e, occasionalmente, immagini bitmap RGB in cui vengono eseguite le trasformazioni.

Il contenuto Windows Media Video 9.1 Image è praticamente identico al normale contenuto codificato Windows Media Video 9, ma è identificato dal proprio FOURCC ("WMVP").

Il tipo di output del codificatore per l'immagine video è impostato esattamente come il video Windows Media standard, ad eccezione del fatto che il sottotipo e i valori di compressione devono essere impostati su identificatori di immagine video. Ciò include la necessità di ottenere dati privati del codec e di accodarlo alla [**struttura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) Per altre informazioni, vedere [Configurazione della codifica video.](configuringvideoencoding.md)

Anche la configurazione del tipo di input per l'immagine video è molto simile alla configurazione di input per gli altri codificatori video. È possibile recuperare un [**DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) parzialmente completato dal codificatore chiamando [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)oppure, se si usa Media Foundation SDK, chiamando [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) e recuperando **DMO MEDIA \_ \_ TYPE** usando [**MFCreateAMMediaTypeFromMFMediaType.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype) È quindi possibile impostare le dimensioni dei fotogrammi e la struttura del formato [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) esattamente come per il video standard. Come per il tipo di output, è necessario assicurarsi che il sottotipo e i valori di compressione siano impostati in modo appropriato.

## <a name="creating-input-samples"></a>Creazione di esempi di input

Gli esempi di input per il codec dell'immagine video sono strutturati. La definizione della struttura e delle costanti usate per l'immagine video non è inclusa nelle Windows codec audio e video multimediali. Queste definizioni sono incluse in Windows Media Format SDK e il relativo uso è completamente illustrato nella documentazione di Windows Media Format SDK.

## <a name="decoding"></a>Decodifica

Non sono necessari requisiti speciali per decodificare il video di acquisizione dello schermo. Oltre a un sottotipo diverso (MEDIASUBTYPE WMVP) usato per l'input del decodificatore, il flusso dell'immagine video compressa è essenzialmente identico a un flusso video \_ multimediale Windows standard.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 
