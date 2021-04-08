---
description: Importante deprecato.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Esempio MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880074"
---
# <a name="mfplayer2-sample"></a>Esempio MFPlayer2

> [!IMPORTANT]
> Deprecato. Questa API può essere rimossa dalle versioni successive di Windows. Le applicazioni devono usare la [sessione multimediale](media-session.md) per la riproduzione.

 

Vengono illustrate alcune delle funzionalità di riproduzione omesse dall'esempio [SimplePlay](simpleplay-sample.md) , ad esempio:

-   La ricerca
-   Controllo della frequenza (avanzamento rapido e riavvolgimento)
-   Volume audio e controlli di silenziamento
-   Zoom video

Nell'immagine seguente vengono illustrati i controlli utilizzati per queste funzionalità.

![screenshot dell'esempio mfplayer ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le API seguenti.

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [**IAudioSessionManager**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
