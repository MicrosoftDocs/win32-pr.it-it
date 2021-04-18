---
description: Esempio WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Esempio WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310159"
---
# <a name="wavsink-sample"></a>Esempio WavSink

Viene illustrato come implementare un sink multimediale personalizzato in Microsoft Media Foundation. L'esempio implementa un sink di archiviazione che scrive audio PCM non compresso in un file WAV.

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Media Foundation seguenti:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>Utilizzo

L'esempio WavSink contiene due progetti di Visual Studio:

-   WavSink. vcproj compila una libreria statica che contiene l'implementazione del sink multimediale.
-   WriteWavFile. vcproj compila un'applicazione console che usa il sink multimediale per produrre un file WAV. Questa applicazione consente di collegarsi alla libreria creata dal progetto WavSink.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Sink di supporti](media-sinks.md)
</dt> </dl>

 

 



