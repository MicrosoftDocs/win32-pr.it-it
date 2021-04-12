---
description: Attributi di flusso
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: Attributi di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527823"
---
# <a name="stream-attributes"></a>Attributi di flusso

Gli attributi seguenti si applicano ai flussi multimediali. Per ottenere gli attributi da un esempio multimediale, usare il metodo [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) .



| Attributo                                                                                   | Descrizione                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [\_CameraExtrinsics MFStreamExtension](mfstreamextension-cameraextrinsics.md)               | La fotocamera è estrinseca per il flusso.         |
| [\_PinholeCameraIntrinsics MFStreamExtension](mfstreamextension-pinholecameraintrinsics.md) | Funzioni intrinseche della fotocamera pinhole per il flusso. |



 

Non tutti i flussi multimediali contengono tutti gli attributi elencati di seguito. In alcuni casi, un attributo si applica solo a determinati tipi di dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> </dl>

 

 



