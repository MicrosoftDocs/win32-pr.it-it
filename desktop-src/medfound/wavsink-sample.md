---
description: Esempio di WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Esempio di WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1bd754e426d848e9d84aea337225ea51940d8727c63d1e1c78c93aeea43110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737136"
---
# <a name="wavsink-sample"></a>Esempio di WavSink

Illustra come implementare un sink multimediale personalizzato in Microsoft Media Foundation. L'esempio implementa un sink di archivio che scrive audio PCM non compresso in un file wav.

## <a name="apis-demonstrated"></a>API illustrate

Questo esempio illustra le interfacce Media Foundation seguenti:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>Uso

L'esempio WavSink contiene due Visual Studio seguenti:

-   WavSink.vcproj compila una libreria statica che contiene l'implementazione del sink multimediale.
-   WriteWavFile.vcproj compila un'applicazione console che usa il sink multimediale per produrre un file wav. Questa applicazione è collegata alla libreria creata dal progetto WavSink.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository github Windows esempi classici](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Sink di supporti](media-sinks.md)
</dt> </dl>

 

 



